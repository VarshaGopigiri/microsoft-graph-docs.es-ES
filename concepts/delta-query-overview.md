---
title: Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph
description: La consulta de delta permite a las aplicaciones detectar entidades recién creadas, actualizadas o eliminadas sin realizar una operación de lectura completa del recurso de destino con cada solicitud. Las aplicaciones de Microsoft Graph pueden usar consultas de delta para sincronizar los cambios de forma eficaz con un almacén de datos local.
author: piotrci
localization_priority: Priority
ms.openlocfilehash: 77f5a4eae74e40655d858fb839697aca80851afb
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823870"
---
# <a name="use-delta-query-to-track-changes-in-microsoft-graph-data"></a>Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph

La consulta de delta permite a las aplicaciones detectar entidades recién creadas, actualizadas o eliminadas sin realizar una operación de lectura completa del recurso de destino con cada solicitud. Las aplicaciones de Microsoft Graph pueden usar consultas de delta para sincronizar los cambios de forma eficaz con un almacén de datos local.

## <a name="use-delta-query-to-track-changes-in-a-resource-collection"></a>Usar la consulta de delta para realizar el seguimiento de los cambios en una colección de recursos

El patrón de llamada típico es el siguiente:

1. La aplicación empieza con una llamada a una solicitud GET con la función delta en el recurso deseado.
2. Microsoft Graph envía una respuesta que contiene el recurso solicitado y un [token de estado](#state-tokens).

     a.  Si se devuelve una dirección URL `nextLink`, podría haber más páginas de datos para recuperar en la sesión. La aplicación continúa realizando solicitudes mediante la dirección URL `nextLink` para recuperar todas las páginas de datos hasta que se incluya una dirección URL `deltaLink` en la respuesta.

     b.  Si se devuelve dirección URL `deltaLink`, no hay más datos sobre el estado existente del recurso para devolver. Para las solicitudes futuras, la aplicación usa la dirección URL `deltaLink` para obtener información sobre los cambios en el recurso.

3. Cuando la aplicación necesita obtener información sobre los cambios en el recurso, realiza una nueva solicitud con la dirección URL `deltaLink` recibida en el paso 2. Esta solicitud *puede* realizarse inmediatamente después de completar el paso 2, o cuando la aplicación comprueba los cambios.
4. Microsoft Graph devuelve una respuesta que describe los cambios en el recurso desde la solicitud anterior, y una dirección URL `nextLink` o `deltaLink`.

>**Nota:** Los recursos almacenados en Azure Active Directory (por ejemplo, usuarios y grupos) admiten los escenarios de "sincronizar desde ahora". Esto le permite omitir los pasos 1 y 2 anteriores (si no le interesa recuperar el estado del recurso completo) y solicitar la última `deltaLink` en su lugar. Anexar `$deltaToken=latest` a la función `delta` y la respuesta contendrá un `deltaLink` sin datos de recursos.

### <a name="state-tokens"></a>Tokens de estado

Una respuesta GET de consulta de delta siempre incluye una dirección URL especificada en un encabezado de respuesta `nextLink` o `deltaLink`. La dirección URL `nextLink` incluye un _skipToken_ y una dirección URL `deltaLink` incluye un _deltaToken_.

Estos tokens son opacos para el cliente. A continuación se muestra la información que necesita saber sobre ellos:

- Cada token refleja el estado y representa una instantánea del recurso en esa ronda de seguimiento de cambios.

- Los tokens de estado también codifican e incluyen otros parámetros de consulta (como `$select`) especificados en la solicitud de consulta de delta inicial. Por lo tanto, no es necesario repetirlos en las solicitudes de consulta de delta siguientes.

- Al llevar a cabo consultas de delta, puede copiar y aplicar las direcciones URL `nextLink` o `deltaLink` a la siguiente llamada a función **delta** sin tener que examinar el contenido de la dirección URL, incluido su token de estado.

### <a name="optional-query-parameters"></a>Parámetros de consulta opcionales

Si un cliente usa un parámetro de consulta, debe especificarse en la solicitud inicial. Microsoft Graph codifica automáticamente el parámetro especificado en los `nextLink` o `deltaLink` proporcionados en la respuesta. La aplicación de llamada solo necesita especificar los parámetros de consulta deseados una vez por adelantado. Microsoft Graph agrega los parámetros especificados automáticamente para todas las solicitudes subsiguientes.

Para los usuarios y grupos, existen restricciones en el uso de algunos parámetros de la consulta:

- Si se usa un parámetro de consulta `$select`, este indica que el cliente prefiere registrar los cambios solo en las propiedades o relaciones especificadas en la instrucción `$select`. Si se produce un cambio en una propiedad que no está activada, el recurso en el que se ha producido el cambio no aparecerá en la respuesta de delta tras una solicitud posterior.
- `$expand` solo es compatible para las propiedades de navegación `manager` y `members` para usuarios y grupos respectivamente.

- Definir el ámbito de los filtros le permite controlar los cambios realizados en uno o más usuarios o grupos específicos mediante objectId. Por ejemplo, la siguiente solicitud: https://graph.microsoft.com/beta/groups/delta/?$filter= id eq '477e9fc6-5de7-4406-bb2a-7e5c83c9ae5f' o id eq '004d6a07-fe70-4b92-add5-e6e37b8acd8e' devuelve cambios para los grupos que coinciden con los identificadores especificados en el filtro de consulta.

## <a name="resource-representation-in-the-delta-query-response"></a>Representación de recursos en la respuesta de consulta delta

- Las instancias de un recurso compatible recién creadas se representan en la respuesta de consulta de delta con su representación estándar.

- Las instancias actualizadas están representadas por sus **id.** con *al menos* las propiedades que se han actualizado, pero pueden incluirse otras propiedades.

- Las relaciones de usuarios y grupos se representan como anotaciones en la representación de recursos estándar. Estas anotaciones utilizan el formato `propertyName@delta`. Las anotaciones se incluyen en la respuesta de la solicitud de consulta inicial de delta.

Las instancias eliminadas se representan mediante sus **id.** y un objeto `@removed`. El objeto `@removed` puede incluir información adicional sobre por qué se eliminó la instancia. Por ejemplo, "@removed": {"reason": "changed"}.

Las razones posibles de "@removed" (eliminación) pueden ser *changed* (cambios) o *deleted* (eliminaciones).

- *Changed* indica que el elemento se eliminó y puede restaurarse desde [deletedItems](/graph/api/resources/directory?view=graph-rest-beta).

- *Deleted* indica que el elemento se ha eliminado y no se puede restaurar.

El objeto `@removed` se puede devolver en la respuesta de la consulta inicial de delta y en las respuestas de seguimiento (deltaLink). Los clientes con solicitudes de consulta delta deben diseñarse para administrar estos objetos en las respuestas.

## <a name="supported-resources"></a>Recursos admitidos

Actualmente, la consulta delta es compatible con los siguientes recursos.

| **Colección de recursos** | **API** |
|:------ | :------ |
| Aplicaciones (versión preliminar) | Función [delta](/graph/api/application-delta?view=graph-rest-beta) del recurso [application](/graph/api/resources/application?view=graph-rest-beta) (versión preliminar) |
| Objetos de directorio | Función [delta](/graph/api/directoryobject-delta?view=graph-rest-beta) del recurso [directoryObjects](/graph/api/resources/directoryobject?view=graph-rest-beta) (versión preliminar) |
| Roles de directorio | Función [delta](/graph/api/directoryrole-delta?view=graph-rest-1.0) del recurso [directoryRole](/graph/api/resources/directoryrole?view=graph-rest-1.0) |
| Eventos en una vista de calendario (intervalo de fechas) del calendario principal | La función [delta](/graph/api/event-delta?view=graph-rest-1.0) del recurso [event](/graph/api/resources/event?view=graph-rest-1.0) |
| Grupos | La función [delta](/graph/api/group-delta?view=graph-rest-1.0) del recurso [group](/graph/api/resources/group?view=graph-rest-1.0) |
| Carpetas de correo | La función [delta](/graph/api/mailfolder-delta?view=graph-rest-1.0) del recurso [mailFolder](/graph/api/resources/mailfolder?view=graph-rest-1.0) |
| Mensajes de una carpeta | La función [delta](/graph/api/message-delta?view=graph-rest-1.0) del recurso [message](/graph/api/resources/message?view=graph-rest-1.0) |
| Carpetas de contactos personales | La función [delta](/graph/api/contactfolder-delta?view=graph-rest-1.0) del recurso [contactFolder](/graph/api/resources/contactfolder?view=graph-rest-1.0) |
| Contactos personales en una carpeta | La función [delta](/graph/api/contact-delta?view=graph-rest-1.0) del recurso [contact](/graph/api/resources/contact?view=graph-rest-1.0) |
| Entidades de servicio (versión preliminar) | Función[delta](/graph/api/serviceprincipal-delta?view=graph-rest-beta) del recurso[servicePrincipal](/graph/api/resources/serviceprincipal?view=graph-rest-beta) (versión preliminar) |
| Usuarios | La función [delta](/graph/api/user-delta?view=graph-rest-1.0) del recurso [user](/graph/api/resources/user?view=graph-rest-1.0) |
| Elementos de la unidad\* | Función [delta](/graph/api/driveitem-delta?view=graph-rest-1.0) del recurso [driveItem](/graph/api/resources/driveitem?view=graph-rest-1.0) |
| Elementos de Planner\*\* | Función [delta](/graph/api/planneruser-list-delta?view=graph-rest-beta) de todos los segmentos del recurso [plannerUser](/graph/api/resources/planneruser?view=graph-rest-beta) (vista previa) |

> \* El patrón de uso para los recursos de OneDrive es similar a los demás recursos admitidos, con algunas diferencias secundarias de sintaxis. La consulta delta para unidades se actualizará en el futuro para que sea coherente con otros tipos de recursos. Para obtener más información sobre la sintaxis actual, vea [Control de cambios de una unidad](/graph/api/item-delta?view=graph-rest-1.0).

> \*\* El patrón de uso de los recursos de Planner es similar a otros recursos admitidos, con algunas diferencias.  Para obtener más información, vea [Control de cambios en Planner](/graph/api/planneruser-list-delta?view=graph-rest-beta).

## <a name="prerequisites"></a>Requisitos previos

Los mismos [permisos](./permissions-reference.md) que se requieren para leer un recurso específico también son necesarios para realizar la consulta delta en ellos.

## <a name="delta-query-request-examples"></a>Ejemplos de solicitud de consulta delta

- [Obtener los cambios incrementales en los eventos en una vista de calendario](delta-query-events.md)
- [Obtener los cambios incrementales en los mensajes de una carpeta](./delta-query-messages.md)
- [Obtener los cambios incrementales en los grupos](./delta-query-groups.md)
- [Obtener los cambios incrementales en los usuarios](./delta-query-users.md)
