---
title: Tipo de recurso mailFolder
description: Carpeta de recurso en el buzón de un usuario, como Bandeja de entrada y Borradores. Las carpetas de correo pueden contener mensajes, otros elementos de Outlook y carpetas de correo secundarias.
ms.openlocfilehash: 49fd4571e3ebe35e04e4da4276c1816829ebc599
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085819"
---
# <a name="mailfolder-resource-type"></a>Tipo de recurso mailFolder

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Carpeta de recurso en el buzón de un usuario, como Bandeja de entrada y Borradores. Las carpetas de correo pueden contener mensajes, otros elementos de Outlook y carpetas de correo secundarias.

Este recurso es compatible con el uso de una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de las adiciones incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/mailfolder-delta.md).

**Nombres de carpeta conocidos**

Outlook crea determinadas carpetas para los usuarios de manera predeterminada. En lugar de usar el valor de **identificador de** carpeta correspondiente, para su comodidad, puede usar los nombres de carpeta conocidas de la siguiente tabla al obtener acceso a estas carpetas. Por ejemplo, puede obtener la carpeta Borradores utilizando su nombre Well-known con la siguiente consulta.

<!-- { "blockType": "ignored" } -->
```http
GET /me/mailFolders/drafts
```

Nombres conocidos trabajar independientemente de la configuración regional del buzón de correo del usuario, por lo que la consulta anterior devolverá siempre carpeta de borradores del usuario, independientemente de cómo se denomina.

| Nombre de la carpeta conocidos | Descripción |
|:-----------------------|:------------|
| archivo | Los mensajes de la carpeta de archivo se envían a cuando se usa la característica de archivo de One_Click en los clientes de Outlook que lo admitan. **Nota:** no es el mismo que la característica de buzón de archivo de Exchange online. |
| desorden | Los mensajes con prioridad baja desorden carpeta se mueven a cuando se usa la característica de desorden. |
| conflictos | La carpeta que contiene los elementos en conflicto en el buzón de correo. |
| conversationhistory | La carpeta donde Skype guarda las conversaciones de mensajería instantánea (si está configurada Skype para ello). |
| deleteditems | Cuando se eliminan, se mueven los elementos de carpeta a. |
| borradores | La carpeta que contiene los mensajes no enviados. |
| Bandeja de entrada | La carpeta Bandeja de entrada. |
| junkemail | La carpeta correo electrónico no deseado. |
| localfailures | La carpeta que contiene los elementos que existen en el cliente local pero no se podrían cargar en el servidor. |
| msgfolderroot | La carpeta "Parte superior del almacén de información". Esta carpeta es la carpeta principal para las carpetas que se muestran en los clientes de correo normal, como la Bandeja de entrada. |
| Bandeja de salida | La carpeta Bandeja de salida. |
| recoverableitemsdeletions | La carpeta que contiene elementos eliminados temporalmente: eliminado desde la carpeta Elementos eliminados, o al presionar MAYÚS + SUPR en Outlook. Esta carpeta no está visible en cualquier cliente de correo electrónico de Outlook, pero los usuarios finales pueden interactuar con él a través de la característica **Recuperar elementos eliminados del servidor** en Outlook o Outlook en el web. |
| programado | La carpeta que contiene los mensajes que están programados para volver a aparecer en la Bandeja de entrada mediante la característica de programación de Outlook para iOS. |
| SearchFolders | La carpeta principal para todas las carpetas de búsqueda definidas en el buzón del usuario. |
| elementos enviados | La carpeta Elementos enviados. |
| serverfailures | La carpeta que contiene los elementos que existen en el servidor, pero no se pudieron sincronizar para el cliente local. |
| syncissues | La carpeta que contiene los registros de sincronización creados por Outlook. |

## <a name="methods"></a>Métodos

| Método | Tipo de valor devuelto | Descripción |
|:-------|:------------|:------------|
|[Obtener mailFolder](../api/mailfolder-get.md) | [mailFolder](mailfolder.md) |Lea las propiedades y las relaciones del objeto mailFolder.|
|[Crear MailFolder](../api/mailfolder-post-childfolders.md) |[mailFolder](mailfolder.md)| Cree un nuevo recurso mailFolder en el actual; para ello, publique en la colección childFolders.|
|[Enumerar childFolders](../api/mailfolder-list-childfolders.md) |Colección [mailFolder](mailfolder.md)| Obtenga la colección de carpetas en la carpeta especificada. Puede usar el acceso directo `.../me/MailFolders` para obtener la colección de carpetas de nivel superior y navegar a otra carpeta.|
|[Crear mensaje](../api/mailfolder-post-messages.md) |[message](message.md)| Cree un nuevo mensaje en el recurso mailFolder actual; para ello, publique en la colección de mensajes.|
|[Enumerar mensajes](../api/mailfolder-list-messages.md) |Colección [message](message.md)| Obtenga todos los mensajes del buzón del usuario que ha iniciado sesión o esos mensajes en una carpeta especificada del buzón.|
|[Actualizar](../api/mailfolder-update.md) | [mailFolder](mailfolder.md)|Actualice el objeto mailFolder especificado. |
|[Eliminar](../api/mailfolder-delete.md) | Ninguno |Elimine el objeto mailFolder especificado. |
|[copy](../api/mailfolder-copy.md)|[mailFolder](mailfolder.md)|Copie un objeto mailFolder y su contenido en otro objeto mailFolder.|
|[delta](../api/mailfolder-delta.md)|Colección [mailFolder](mailfolder.md)|Obtenga un conjunto de carpetas de correo que se hayan agregado, eliminado o quitado del buzón del usuario.|
|[move](../api/mailfolder-move.md)|[mailFolder](mailfolder.md)|Mueva un objeto mailFolder y su contenido a otro objeto mailFolder.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[mailFolder](mailfolder.md)  |Cree una o varias propiedades extendidas de valor único en un objeto mailFolder nuevo o existente.   |
|[Obtener mailFolder con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-get.md)  | [mailFolder](mailfolder.md) | Obtenga objetos mailFolder que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [mailFolder](mailfolder.md) | Cree una o varias propiedades extendidas de varios valores en un objeto mailFolder nuevo o existente.  |
|[Obtener mailFolder con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-get.md)  | [mailFolder](mailfolder.md) | Obtenga un objeto mailFolder que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------|:-----|:------------|
|childFolderCount|Int32|El número de objetos mailFolder secundarios inmediatos en el objeto mailFolder actual.|
|displayName|String|El nombre para mostrar del objeto mailFolder.|
|id|String|Identificador único del mailFolder.|
|parentFolderId|String|El identificador único del objeto mailFolder principal del objeto mailFolder.|
|totalItemCount|Int32|El número de elementos en el objeto mailFolder.|
|unreadItemCount|Int32|El número de elementos en el objeto mailFolder marcados como no leídos.|
|wellKnownName|String|El nombre de la carpeta conocida para la carpeta. Los valores posibles indicados anteriormente. Esta propiedad sólo se establece para carpetas predeterminadas creadas por Outlook. Para otras carpetas, esta propiedad es **null**.|

**Acceder a recuentos de elementos de forma eficaz**

El `TotalItemCount` y `UnreadItemCount` las propiedades de una carpeta permiten calcular fácilmente el número de elementos de lectura en la carpeta.
Le permiten evitar las consultas como el siguiente que puede provocar una latencia elevada:

```http
https://outlook.office.com/api/beta/me/folders/inbox/messages?$count=true&$filter=isread%20eq%20false
```

Las carpetas de correo en Outlook pueden contener más de un tipo de elementos, por ejemplo, puede contener la Bandeja de entrada los elementos de solicitud que son distintos de los elementos de correo de la reunión. `TotalItemCount`y `UnreadItemCount` incluir elementos de una carpeta de correo con independencia de su tipo de elemento.

## <a name="relationships"></a>Relaciones

| Relación | Tipo | Descripción |
|:-------------|:-----|:------------|
|childFolders|Colección [MailFolder](mailfolder.md)|La colección de carpetas secundarias del objeto mailFolder.|
|messageRules | Colección [messageRule](messagerule.md) | Conjunto de reglas que se aplican a la Bandeja de entrada del usuario. |
|messages|Colección [Message](message.md)|La colección de mensajes del objeto mailFolder.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el objeto mailFolder. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el objeto mailFolder. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Esta es una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "childFolders",
    "messageRules",
    "messages",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mailFolder"
}-->

```json
{
  "childFolderCount": 1024,
  "displayName": "string",
  "id": "string (identifier)",
  "parentFolderId": "string",
  "totalItemCount": 1024,
  "unreadItemCount": 1024,
  "wellKnownName": "string",
  "childFolders": [ { "@odata.type": "microsoft.graph.mailFolder" } ],
  "messageRules": [ { "@odata.type": "microsoft.graph.messageRule" } ],
  "messages": [ { "@odata.type": "microsoft.graph.message" } ],
  "multiValueExtendedProperties": [ { "@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty" }],
  "singleValueExtendedProperties": [ { "@odata.type": "microsoft.graph.singleValueLegacyExtendedProperty" }]
}
```

## <a name="see-also"></a>Vea también

- [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview)
- [Obtener los cambios incrementales en los mensajes de una carpeta](/graph/delta-query-messages)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
