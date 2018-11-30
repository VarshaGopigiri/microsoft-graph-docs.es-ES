---
title: tipo de recurso de mensaje
description: Un mensaje en una carpeta de buzón de correo.
ms.openlocfilehash: 02c315bce639d2ee951d8f1aedca2e13231b0edf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085587"
---
# <a name="message-resource-type"></a>tipo de recurso de mensaje

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un mensaje en una carpeta de buzón de correo.

Este recurso admite:

- Adición de sus propios datos como encabezados de mensaje de Internet personalizados. Agregar encabezados personalizados sólo cuando se crea un mensaje y asignarle un nombre comenzando con "x-". Una vez que se ha enviado el mensaje, no se puede modificar los encabezados. Para obtener los encabezados de un mensaje, se aplican la `$select` parámetro en una operación de [obtener el mensaje](../api/message-get.md) de consulta.
- Adición de sus propios datos como propiedades personalizadas como [extensiones](/graph/extensibility-overview).
- Suscribirse a [las notificaciones de cambios](/graph/webhooks).
- que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/message-delta.md).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "attachments",
    "extensions",
    "singleValueExtendedProperties",
    "multiValueExtendedProperties",
    "mentions"
  ],
  "@odata.type": "microsoft.graph.message"
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
  "conversationIndex": "binary",
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
  "mentionsPreview": {"@odata.type": "microsoft.graph.mentionsPreview"},
  "parentFolderId": "string",
  "receivedDateTime": "String (timestamp)",
  "replyTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "sender": {"@odata.type": "microsoft.graph.recipient"},
  "sentDateTime": "String (timestamp)",
  "subject": "string",
  "toRecipients": [{"@odata.type": "microsoft.graph.recipient"}],
  "uniqueBody": {"@odata.type": "microsoft.graph.itemBody"},
  "unsubscribeData": "string",
  "unsubscribeEnabled": true,
  "webLink": "string",

  "attachments": [{"@odata.type": "microsoft.graph.attachment"}],
  "extensions": [{"@odata.type": "microsoft.graph.extension"}],
  "mentions": [{"@odata.type": "microsoft.graph.mention"}],
  "multiValueExtendedProperties": [{"@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty"}],
  "singleValueExtendedProperties": [{"@odata.type": "microsoft.graph.singleValueLegacyExtendedProperty"}]
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|bccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cco: del mensaje.|
|body|[itemBody](itembody.md)|El cuerpo del mensaje. Puede mostrarse en formato de texto o HTML.|
|bodyPreview|String|Los primeros 255 caracteres del cuerpo del mensaje. Está en formato de texto. Si el mensaje contiene instancias de [mencionar](mention.md), esta propiedad contendrá una concatenación de estas menciones así como. |
|categories|Colección String|Las categorías asociadas al mensaje. Cada categoría corresponde a la propiedad **displayName** de un [outlookCategory](outlookcategory.md) definidos para el usuario. |
|ccRecipients|Colección [recipient](recipient.md)|Los destinatarios Cc: del mensaje.|
|changeKey|String|La versión del mensaje.|
|conversationId|String|El identificador de la conversación a la que pertenece el correo electrónico.|
|conversationIndex|Binario|El índice de la conversación del correo electrónico al que pertenece.|
|createdDateTime|DateTimeOffset|La fecha y la hora de creación del mensaje.|
|flag|[followUpFlag](followupflag.md)|Valor de marca que indica el estado, la fecha de inicio, la fecha de vencimiento o la fecha de finalización del mensaje.|
|from|[recipient](recipient.md)|El propietario del buzón y el remitente del mensaje. El valor debe corresponder al buzón real que se usa.|
|hasAttachments|Booleano|Indica si el mensaje tiene datos adjuntos. Esta propiedad no incluye datos adjuntos insertados, por lo que si un mensaje contiene solo datos adjuntos insertados, esta propiedad es igual a false. Para comprobar si hay datos adjuntos insertados, analice la propiedad **body** en busca de un atributo `src`, como `<IMG src="cid:image001.jpg@01D26CD8.6C05F070">`. |
|id|String|Identificador único del mensaje (tenga en cuenta que este valor puede cambiar si se mueve o se altera un mensaje)|
|importance|String| La importancia del mensaje: `Low`, `Normal` y `High`.|
|inferenceClassification|String| La clasificación del mensaje para el usuario, basándose en la relevancia inferida o importancia, o en un reemplazo explícito. Los valores posibles son: `focused` y `other`.|
|internetMessageHeaders | Colección [internetMessageHeader](internetmessageheader.md) | Una colección de encabezados de mensaje definido por [RFC5322](https://www.ietf.org/rfc/rfc5322.txt). El conjunto incluye los encabezados de mensaje que indica la ruta de acceso de red realizada por un mensaje desde el remitente al destinatario. También puede contener encabezados de mensaje personalizado que contienen datos de aplicación para el mensaje. |
|internetMessageId | String | El identificador de mensaje en el formato especificado por [RFC5322](https://www.ietf.org/rfc/rfc5322.txt). Actualizable sólo si **isDraft** es true.|
|isDeliveryReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|isDraft|Booleano|Indica si el mensaje es un borrador. Un mensaje es un borrador si no se ha enviado todavía.|
|isRead|Booleano|Indica si se ha leído el mensaje.|
|isReadReceiptRequested|Booleano|Indica si se solicita confirmación de lectura para el mensaje.|
|lastModifiedDateTime|DateTimeOffset|La fecha y la hora de la última modificación del mensaje.|
|mentionsPreview|[mentionsPreview](mentionspreview.md)|Información acerca de menciones en el mensaje. Cuando se procesa una `GET` /messages solicitud, el servidor establece esta propiedad e incluye en la respuesta de forma predeterminada. El servidor devuelve null si no hay ningún menciones en el mensaje. Opcional. |
|parentFolderId|String|El identificador único para el mailFolder principal del mensaje.|
|receivedDateTime|DateTimeOffset|La fecha y la hora en las que se recibió el mensaje.|
|replyTo|Colección [recipient](recipient.md)|Las direcciones de correo electrónico que se utilizan al responder.|
|sender|[recipient](recipient.md)|La cuenta que se utiliza realmente para generar el mensaje. En la mayoría de los casos, este valor es el mismo que la propiedad **from** . Puede establecer esta propiedad en un valor distinto al enviar un mensaje desde un [buzón compartido](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes)o enviar un mensaje como un [delegado](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926). En cualquier caso, el valor debe corresponder al buzón real que se usa. |
|sentDateTime|DateTimeOffset|La fecha y la hora de envío del mensaje.|
|subject|String|El asunto del mensaje.|
|toRecipients|Colección [recipient](recipient.md)|Los destinatarios Para: del mensaje.|
|uniqueBody|[itemBody](itembody.md)|La parte del cuerpo del mensaje que es única del mensaje actual. El elemento **uniqueBody** no se devuelve de manera predeterminada, pero puede recuperarse para cualquier mensaje con la consulta `?$select=uniqueBody`. Puede mostrarse en formato de texto o HTML.|
|unsubscribeData|String|Las entradas válidas se analizan desde el encabezado cancelar su suscripción de lista.  Se trata de los datos para el comando de correo en el encabezado de cancelar su suscripción de lista si la propiedad UnsubscribeEnabled es true.|
|unsubscribeEnabled|Booleano|Indica si el mensaje está habilitado para cancelar la suscripción.  Su valueTrue si la cancelación de suscripción de lista de encabezado se ajusta al rfc 2369.|
|webLink|String|La dirección URL para abrir el mensaje en Outlook Web App.<br><br>Puede anexar un argumento ispopout al final de la dirección URL para cambiar cómo se muestra el mensaje. Si ispopout no está presente o se establece en 1, se muestra el mensaje en una ventana emergente. Si ispopout se establece en 0, el navegador mostrará el mensaje en el panel de revisión de Outlook Web App.<br><br>El mensaje se abrirá en el navegador si está conectado a su buzón mediante Outlook Web App. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.<br><br>Se puede obtener acceso a esta dirección URL desde un iFrame.|

**Quitar un script de la propiedad body**

El cuerpo del mensaje puede mostrarse en formato de texto o HTML. Si el cuerpo se muestra en HTML, de forma predeterminada, cualquier código HTML potencialmente peligroso (por ejemplo, JavaScript) insertado en la propiedad **body** se quitará antes de que el contenido del cuerpo se devuelva en una respuesta REST. Para obtener todo el contenido HTML original, incluya el siguiente encabezado de solicitud HTTP:
```
Prefer: outlook.allow-unsafe-html
```

**Configuración de las propiedades from y sender**

Cuando se redacta un mensaje, en la mayoría de los casos, las propiedades From y Sender representan al mismo usuario que inició sesión, a menos que alguno esté actualizado como se describe en los siguientes escenarios:

- La propiedad **from** se puede cambiar si el administrador de Exchange ha asignado los derechos **sendAs** del buzón a otros usuarios. El administrador puede realizar esta acción si selecciona **Permisos del buzón** del propietario del buzón en Azure Portal, o si usa el Centro de administración de Exchange o un cmdlet Add-ADPermission de Windows PowerShell. Después, puede configurar mediante programación la propiedad **from** para uno de los usuarios que tiene derechos **sendAs** de ese buzón.
- La propiedad **sender** se puede cambiar si el propietario del buzón ha delegado uno o más usuarios para que puedan enviar mensajes desde ese buzón. El propietario del buzón puede delegar en Outlook. Cuando un delegado envía un mensaje en nombre del propietario del buzón, la propiedad **sender** está establecida en la cuenta del delegado y la propiedad **from** sigue siendo el propietario del buzón. Mediante programación, puede configurar la propiedad **sender** para un usuario que tiene derechos de delegado en ese buzón.

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attachments|Colección [attachment](attachment.md)|Los datos adjuntos [fileAttachment](fileattachment.md) y [itemAttachment](itemattachment.md) del mensaje.|
|extensions|Colección [Extension](extension.md)| La colección de extensiones de open definidas para el mensaje. Admite valores NULL.|
|menciones|[mencione](mention.md) colección | Una colección de menciones en el mensaje, ordenadas por la **createdDateTime** desde la más reciente a la más antigua. De forma predeterminada, un `GET` /mensajes no devuelve esta propiedad a menos que aplique `$expand` en la propiedad.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el mensaje. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el mensaje. Solo lectura. Admite valores NULL.|

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Enumerar mensajes](../api/user-list-messages.md) |Colección [message](message.md) | Obtiene todos los mensajes del buzón del usuario que ha iniciado sesión (incluidas las carpetas Elementos eliminados y Otros correos). |
|[Crear mensaje](../api/user-post-messages.md) | [mensaje](message.md) | Crea un borrador de un mensaje nuevo. |
|[Obtener mensaje](../api/message-get.md) | [mensaje](message.md) |Lee las propiedades y las relaciones del objeto de mensaje.|
|[Actualizar](../api/message-update.md) | [mensaje](message.md) |Actualiza el objeto de mensaje. |
|[Eliminar](../api/message-delete.md) | Ninguno |Elimina el objeto de mensaje. |
|[copy](../api/message-copy.md)|[Mensaje](message.md)|Copia un mensaje a una carpeta.|
|[createForward](../api/message-createforward.md)|[Mensaje](message.md)|Cree un borrador de mensaje de reenvío para incluir un comentario o actualizar las propiedades de mensaje todo en una sola llamada **createForward** . A continuación, puede [Actualizar](../api/message-update.md) o [Enviar](../api/message-send.md) el borrador.|
|[createReply](../api/message-createreply.md)|[Mensaje](message.md)|Cree un borrador de un mensaje de respuesta para incluir un comentario o actualizar las propiedades de mensaje todo en una sola llamada **createReply** . A continuación, puede [Actualizar](../api/message-update.md) o [Enviar](../api/message-send.md) el borrador.|
|[createReplyAll](../api/message-createreplyall.md)|[Mensaje](message.md)|Cree un borrador de un mensaje de responder a todos para incluir un comentario o actualizar las propiedades del mensaje, todo en una sola llamada **createReplyAll** . A continuación, puede [Actualizar](../api/message-update.md) o [Enviar](../api/message-send.md) el borrador.|
|[delta](../api/message-delta.md)|Colección [message](message.md)| Obtenga un conjunto de mensajes que se hayan agregado, eliminado o actualizado en una carpeta determinada.|
|[forward](../api/message-forward.md)|Ninguno|Reenviar un mensaje, agregar un comentario o modificar las propiedades actualizables todo en una sola llamada **hacia delante** . A continuación, se guarda el mensaje en la carpeta Elementos enviados.|
|[move](../api/message-move.md)|[Mensaje](message.md)|Mueve un mensaje a una carpeta. Se crea una nueva copia del mensaje en la carpeta de destino.|
|[reply](../api/message-reply.md)|Ninguno|Responder al remitente de un mensaje, agregar un comentario o modificar las propiedades actualizables todo en una **respuesta** de llamada. A continuación, se guarda el mensaje en la carpeta Elementos enviados.|
|[replyAll](../api/message-replyall.md)|Ninguno|Responder a todos los destinatarios de un mensaje mediante la especificación de un comentario y modificación de las propiedades para la respuesta, puede actualizables todos los mediante el método **replyAll** . A continuación, se guarda el mensaje en la carpeta Elementos enviados.|
|[send](../api/message-send.md)|Ninguno|Envía un borrador de mensaje creado anteriormente. El mensaje se guarda en la carpeta Elementos enviados.|
|[anular la suscripción](../api/message-unsubscribe.md)|Ninguno|Enviar un mensaje con la dirección especificada en el primer comando mailto en el encabezado de cancelar su suscripción de lista y los datos.|
|**Datos adjuntos**| | |
|[Enumerar datos adjuntos](../api/message-list-attachments.md) |Colección [attachment](attachment.md)| Obtener todos los datos adjuntos en un mensaje.|
|[Agregar datos adjuntos](../api/message-post-attachments.md) |[Dato adjunto](attachment.md)| Agrega un dato adjunto nuevo a un mensaje publicándolo en la colección de datos adjuntos.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o un recurso existente.|
|[Obtener extensión abierta](../api/opentypeextension-get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene una extensión abierta identificada por el nombre de extensión.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](/graph/extensibility-schema-groups) || Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[mensaje](message.md)  |Crea una o más propiedades extendidas de valor único en un mensaje nuevo o existente.   |
|[Obtener mensaje con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-get.md)  | [mensaje](message.md) | Obtiene mensajes que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [mensaje](message.md) | Crea una o más propiedades extendidas de varios valores en un mensaje nuevo o existente.  |
|[Obtener mensaje con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-get.md)  | [mensaje](message.md) | Obtiene un mensaje que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |

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