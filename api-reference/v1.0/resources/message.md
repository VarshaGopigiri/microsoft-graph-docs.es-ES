---
title: tipo de recurso de mensaje
description: Un mensaje en un mailFolder.
ms.openlocfilehash: 146418a03944eb7bc3c1b537f359887b5515906f
ms.sourcegitcommit: f3d479edf03935d0edbbc7668a65f7cde2a56c92
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/15/2018
ms.locfileid: "27283678"
---
# <a name="message-resource-type"></a>tipo de recurso de mensaje

Un mensaje en un mailFolder.

Este recurso admite:

- Adición de sus propios datos como encabezados de mensaje de Internet personalizados. Agregar encabezados personalizados sólo cuando se crea un mensaje y asignarle un nombre comenzando con "x-". Una vez que se ha enviado el mensaje, no se puede modificar los encabezados. Para obtener los encabezados de un mensaje, se aplican la `$select` parámetro en una operación de [obtener el mensaje](../api/message-get.md) de consulta.
- Adición de sus propios datos como propiedades personalizadas como [extensiones](/graph/extensibility-overview).
- Suscribirse a [las notificaciones de cambios](/graph/webhooks).
- que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/message-delta.md).

## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Enumerar mensajes](../api/user-list-messages.md) |Colección [message](message.md) | Obtiene todos los mensajes del buzón del usuario que ha iniciado sesión (incluidas las carpetas Elementos eliminados y Otros correos). |
|[Crear mensaje](../api/user-post-messages.md) | [mensaje](message.md) | [Crea](../api/user-post-messages.md#request-1) un borrador de un mensaje nuevo. |
|[Obtener mensaje](../api/message-get.md) | [mensaje](message.md) |Lee las propiedades y las relaciones del objeto de mensaje.|
|[Actualizar](../api/message-update.md) | [mensaje](message.md) |Actualiza el objeto de mensaje.|
|[Eliminar](../api/message-delete.md) | Ninguno |Elimina el objeto de mensaje. |
|[copy](../api/message-copy.md)|[Mensaje](message.md)|Copia un mensaje a una carpeta.|
|[createForward](../api/message-createforward.md)|[Mensaje](message.md)|Crea un borrador del mensaje que de reenvío. Después puede [actualizar](../api/message-update.md) o [enviar](../api/message-send.md) el borrador.|
|[createReply](../api/message-createreply.md)|[Mensaje](message.md)|Crea un borrador del mensaje de respuesta. Después puede [actualizar](../api/message-update.md) o [enviar](../api/message-send.md) el borrador.|
|[createReplyAll](../api/message-createreplyall.md)|[Mensaje](message.md)|Crea un borrador del mensaje de respuesta a todos. Después puede [actualizar](../api/message-update.md) o [enviar](../api/message-send.md) el borrador.|
|[delta](../api/message-delta.md)|Colección [message](message.md)| Obtenga un conjunto de mensajes que se hayan agregado, eliminado o actualizado en una carpeta determinada.|
|[forward](../api/message-forward.md)|Ninguno|Reenvía un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[move](../api/message-move.md)|[Mensaje](message.md)|Mueve un mensaje a una carpeta. Se crea una nueva copia del mensaje en la carpeta de destino.|
|[reply](../api/message-reply.md)|Ninguno|Responde al remitente de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[replyAll](../api/message-replyall.md)|Ninguno|Responde a todos los remitentes de un mensaje. El mensaje se guarda en la carpeta Elementos enviados.|
|[send](../api/message-send.md)|Ninguno|Envía un borrador de mensaje creado anteriormente. El mensaje se guarda en la carpeta Elementos enviados.|
|**Datos adjuntos**| | |
|[Enumerar datos adjuntos](../api/message-list-attachments.md) |Colección [attachment](attachment.md)| Obtiene todos los datos adjuntos en un mensaje.|
|[Agregar datos adjuntos](../api/message-post-attachments.md) |[Dato adjunto](attachment.md)| Agrega un dato adjunto nuevo a un mensaje publicándolo en la colección de datos adjuntos.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.|
|[Obtener extensión abierta](../api/opentypeextension-get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtenga un objeto u objetos de extensión abierta identificados por nombre o por nombre completo.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](/graph/extensibility-schema-groups) || Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[mensaje](message.md)  |Crea una o más propiedades extendidas de valor único en un mensaje nuevo o existente.   |
|[Obtener mensaje con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-get.md)  | [mensaje](message.md) | Obtiene mensajes que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [mensaje](message.md) | Crea una o más propiedades extendidas de varios valores en un mensaje nuevo o existente.  |
|[Obtener mensaje con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-get.md)  | [mensaje](message.md) | Obtiene un mensaje que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|bccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cco: del mensaje.|
|body|[itemBody](itembody.md)|El cuerpo del mensaje. Puede ser en formato HTML o de texto. Obtenga información acerca de [HTML seguro en el cuerpo de un mensaje](/graph/outlook-create-send-messages#reading-messages-with-control-over-the-body-format-returned).|
|bodyPreview|String|Los primeros 255 caracteres del cuerpo del mensaje. Se muestran en formato de texto.|
|categories|Colección String|Las categorías asociadas al mensaje.|
|ccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cc: del mensaje.|
|changeKey|String|La versión del mensaje.|
|conversationId|String|El identificador de la conversación a la que pertenece el correo electrónico.|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación del mensaje.|
|flag|[followupFlag](followupflag.md)|Valor de marca que indica el estado, la fecha de inicio, la fecha de vencimiento o la fecha de finalización del mensaje.|
|from|[recipient](recipient.md)|El propietario del buzón y el remitente del mensaje. El valor debe corresponder al buzón real que se usa. Obtenga más información acerca de [configuración de la desde y propiedades de remitente](/graph/outlook-create-send-messages#setting-the-from-and-sender-properties) de un mensaje.|
|hasAttachments|Booleano|Indica si el mensaje tiene datos adjuntos. Esta propiedad no incluye datos adjuntos insertados, por lo que si un mensaje contiene solo datos adjuntos insertados, esta propiedad es igual a false. Para comprobar si hay datos adjuntos insertados, analice la propiedad **body** en busca de un atributo `src`, como `<IMG src="cid:image001.jpg@01D26CD8.6C05F070">`.|
|id|String|Identificador único del mensaje (tenga en cuenta que este valor puede cambiar si se mueve o se altera un mensaje)|
|importance|importance| La importancia del mensaje: `Low`, `Normal` y `High`.|
|inferenceClassification | inferenceClassificationType | La clasificación del mensaje para el usuario, basándose en la relevancia inferida o importancia, o en un reemplazo explícito. Los valores posibles son: `focused` o `other`. |
|internetMessageHeaders | Colección [internetMessageHeader](internetmessageheader.md) | Una colección de encabezados de mensaje definido por [RFC5322](https://www.ietf.org/rfc/rfc5322.txt). El conjunto incluye los encabezados de mensaje que indica la ruta de acceso de red realizada por un mensaje desde el remitente al destinatario. También puede contener encabezados de mensaje personalizado que contienen datos de aplicación para el mensaje. |
|internetMessageId |String |El identificador del mensaje en el formato especificado por [RFC2822](https://www.ietf.org/rfc/rfc2822.txt). |
|isDeliveryReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|isDraft|Boolean|Indica si el mensaje es un borrador. Un mensaje es un borrador si no se ha enviado todavía.|
|isRead|Booleano|Indica si se ha leído el mensaje.|
|isReadReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora de la última modificación del mensaje.|
|parentFolderId|String|El identificador único para el mailFolder principal del mensaje.|
|receivedDateTime|DateTimeOffset|La fecha y la hora en las que se recibió el mensaje.|
|replyTo|Colección [recipient](recipient.md)|Las direcciones de correo electrónico que se utilizan al responder.|
|sender|[recipient](recipient.md)|La cuenta que se utiliza realmente para generar el mensaje. En la mayoría de los casos, este valor es el mismo que la propiedad **from** . Puede establecer esta propiedad en un valor distinto al enviar un mensaje desde un [buzón compartido](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes)o enviar un mensaje como un [delegado](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926). En cualquier caso, el valor debe corresponder al buzón real que se usa. Obtenga más información acerca de [configuración de la desde y propiedades de remitente](/graph/outlook-create-send-messages#setting-the-from-and-sender-properties) de un mensaje.|
|sentDateTime|DateTimeOffset|La fecha y la hora de envío del mensaje.|
|subject|String|El asunto del mensaje.|
|toRecipients|Colección [recipient](recipient.md)|Los destinatarios Para: del mensaje.|
|uniqueBody|[itemBody](itembody.md)|La parte del cuerpo del mensaje que es única del mensaje actual. El elemento **uniqueBody** no se devuelve de manera predeterminada, pero puede recuperarse para cualquier mensaje con la consulta `?$select=uniqueBody`. Puede mostrarse en formato de texto o HTML.|
|webLink|String|La dirección URL para abrir el mensaje en Outlook Web App.<br><br>Puede anexar un argumento ispopout al final de la dirección URL para cambiar cómo se muestra el mensaje. Si ispopout no está presente o se establece en 1, se muestra el mensaje en una ventana emergente. Si ispopout se establece en 0, el navegador mostrará el mensaje en el panel de revisión de Outlook Web App.<br><br>El mensaje se abrirá en el navegador si está conectado a su buzón mediante Outlook Web App. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.<br><br>Se puede acceder a esta dirección URL desde un iFrame.|


## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attachments|Colección [attachment](attachment.md)|Los datos adjuntos [fileAttachment](fileattachment.md) y [itemAttachment](itemattachment.md) del mensaje.|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para el mensaje. Solo lectura. Admite valores NULL.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el mensaje. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el mensaje. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.outlookItem",
  "openType": true,
  "optionalProperties": [
    "attachments",
    "extensions",
    "singleValueExtendedProperties",
    "multiValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.message",
  "@odata.annotations": [
    {
      "property": "attachments",
      "capabilities": {
        "changeTracking": false,
        "searchable": false
      }
    },
    {
      "property": "extensions",
      "capabilities": {
        "changeTracking": false,
        "searchable": false
      }
    }
  ]
}-->

```json
{
  "bccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "body": {"@odata.type": "microsoft.graph.itemBody"},
  "bodyPreview": "string",
  "categories": ["string"],
  "ccRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "changeKey": "string",
  "conversationId": "string",
  "createdDateTime": "String (timestamp)",
  "flag": {"@odata.type": "microsoft.graph.followupFlag"},
  "from": {"@odata.type": "microsoft.graph.recipient"},
  "hasAttachments": true,
  "id": "string (identifier)",
  "importance": "String",
  "inferenceClassification": "String",
  "internetMessageHeaders": [{"@odata.type": "microsoft.graph.internetMessageHeader"}],
  "internetMessageId": "String",
  "isDeliveryReceiptRequested": true,
  "isDraft": true,
  "isRead": true,
  "isReadReceiptRequested": true,
  "lastModifiedDateTime": "String (timestamp)",
  "parentFolderId": "string",
  "receivedDateTime": "String (timestamp)",
  "replyTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "sender": {"@odata.type": "microsoft.graph.recipient"},
  "sentDateTime": "String (timestamp)",
  "subject": "string",
  "toRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "uniqueBody": {"@odata.type": "microsoft.graph.itemBody"},
  "webLink": "string",

  "attachments": [{"@odata.type": "microsoft.graph.attachment"}],
  "extensions": [{"@odata.type": "microsoft.graph.extension"}],
  "multiValueExtendedProperties": [{"@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty"}],
  "singleValueExtendedProperties": [{"@odata.type": "microsoft.graph.singleValueLegacyExtendedProperty"}]
}

```

## <a name="see-also"></a>Vea también

- [Obtener configuración del buzón](../api/user-get-mailboxsettings.md) 
- [Actualizar configuración del buzón](../api/user-update-mailboxsettings.md)
- [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview)
- [Obtener los cambios incrementales en los mensajes de una carpeta](/graph/delta-query-messages)
- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
