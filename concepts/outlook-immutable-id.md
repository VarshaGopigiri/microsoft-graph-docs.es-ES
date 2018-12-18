---
title: Obtener identificadores inmutables para recursos de Outlook
description: 'Los elementos de Outlook (mensajes, eventos, contactos, tareas) tienen un comportamiento interesante que probablemente no ha observado nunca o le ha provocado gran frustración: el cambio de ID. No sucede con frecuencia, solo si se mueve el elemento, pero puede provocar problemas reales para las aplicaciones que almacenan identificadores sin conexión para su uso posterior. Los identificadores inmutables permiten que la aplicación obtenga un ID que no cambia durante toda la duración del elemento.'
author: angelgolfer-ms
ms.openlocfilehash: 34d88ed2cbc39902f1240757367beb112cc007b4
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315200"
---
# <a name="get-immutable-identifiers-for-outlook-resources"></a>Obtener identificadores inmutables para recursos de Outlook

Los elementos de Outlook (mensajes, eventos, contactos, tareas) tienen un comportamiento interesante que probablemente no ha observado nunca o le ha provocado gran frustración: el cambio de ID. No sucede con frecuencia, solo si se mueve el elemento, pero puede provocar problemas reales para las aplicaciones que almacenan identificadores sin conexión para su uso posterior. Los identificadores inmutables permiten que la aplicación obtenga un ID que no cambia durante toda la duración del elemento.

> **Importante:** Los identificadores inmutables son solo disponibles en la versión /beta de Microsoft Graph.

## <a name="how-it-works"></a>Funcionamiento

El Identificador inmutable es una característica opcional de Microsoft Graph. Para habilitarla, la aplicación debe enviar un encabezado HTTP adicional en sus solicitudes de API:

```http
Prefer: IdType="ImmutableId"
```

Este encabezado solo se aplica a la solicitud en la que está incluido. Si quiere usar siempre identificadores inmutables, debe incluir este encabezado en cada solicitud de API.

## <a name="lifetime-of-immutable-ids"></a>Duración de los ID inmutables

Un identificador inmutable de un elemento no cambiará siempre y cuando el elemento permanece en el mismo buzón. Eso significa que el identificador inmutable no cambiará si el elemento se mueve a otra carpeta del buzón. Pero, el identificador inmutable cambiará si:

- El usuario mueve el elemento a un buzón de archivo
- El usuario exporta el elemento (a un archivo PST, como un archivo MSG, etc.) y vuelve a importarlo a su buzón

## <a name="items-that-support-immutable-id"></a>Elementos que admiten el identificador inmutable

Los siguientes elementos admiten los identificadores inmutables:

- [Tipo de recurso message](/graph/api/resources/message?view=graph-rest-beta)
- [Tipo de recurso attachment](/graph/api/resources/attachment?view=graph-rest-beta)
- [Tipo de recurso event](/graph/api/resources/event?view=graph-rest-beta)
- [Tipo de recurso eventMessage](/graph/api/resources/eventmessage?view=graph-rest-beta)
- [Tipo de recurso contact](/graph/api/resources/contact?view=graph-rest-beta)
- [Tipo de recurso outlookTask](/graph/api/resources/outlooktask?view=graph-rest-beta)

Los tipos de contenedor (mailFolder, calendario, etc.) no admiten los identificadores inmutables, pero sus identificadores normales ya eran constantes.

## <a name="immutable-id-with-change-notifications"></a>El identificador inmutable con las notificaciones de cambios

Puede solicitar que Microsoft Graph envíe ID inmutables en las notificaciones de cambios incluyendo el encabezado `Prefer: IdType="ImmutableId"` al [crear una suscripción](/graph/api/subscription-post-subscriptions?view=graph-rest-beta). Las suscripciones existentes creadas sin el encabezado seguirán usando el formato ID predeterminado. Para pasar de una suscripción existente a usar identificadores inmutables, debe eliminarlos y volver a crearlos con el encabezado.

## <a name="immutable-id-with-delta-query"></a>El identificador inmutable con consulta delta

Puede solicitar que Microsoft Graph devuelva identificadores inmutables en [respuestas de consultas delta](delta-query-overview.md) para los tipos de recursos admitidos, incluyendo el encabezado `Prefer: IdType="ImmutableId"`. Los valores `nextLink` y `deltaLink` devueltos por las consultas de delta son compatibles con ambos formatos ID, por lo que no es necesario volver a sincronizar la aplicación para aprovechar del ID inmutable. Puede usar el encabezado para obtener los identificadores inmutables en el futuro y puede [actualizar el almacenamiento de la aplicación](#updating-existing-data) por separado.

## <a name="updating-existing-data"></a>Actualizar los datos existentes

Si ya tiene una base de datos con miles de identificadores normales, puede migrar esos ID para usar el formato inmutable con la función [translateExchangeIds](/graph/api/user-translateexchangeids?view=graph-rest-beta). Puede proporcionar una matriz de hasta 1000 identificadores para convertir en un formato de destino.

> **Nota:** También puede usar `translateExchangeIds` para migrar aplicaciones de servicios Web Exchange a Microsoft Graph.

### <a name="example"></a>Ejemplo

En el ejemplo siguiente se convierte un ID de Graph normal a un ID de Graph inmutable.

#### <a name="request"></a>Solicitud

```http
POST https://graph.microsoft.com/beta/me/translateExchangeIds

{
  "inputIds" :
  [
    "AQMkAGM2…"
  ],
  "targetIdType" : "restImmutableEntryId",
  "sourceIdType" : "restId"
}
```

#### <a name="response"></a>Respuesta

```http
HTTP 200 OK

{
  "value": [
    {
      "targetId": "AAkALgAA...",
      "sourceId": "AQMkAGM2..."
    }
  ]
}
```