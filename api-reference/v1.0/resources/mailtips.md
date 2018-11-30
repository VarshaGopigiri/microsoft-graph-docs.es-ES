---
title: tipo de recurso de sugerencias de correo electrónico
description: 'Mensajes informativos acerca de un destinatario, que se muestran a los usuarios mientras que redactan un mensaje. Por ejemplo, un mensaje de fuera de la oficina '
ms.openlocfilehash: 6c5d64248aa940b9449a93caad952bc7b4d13ca6
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029615"
---
# <a name="mailtips-resource-type"></a>tipo de recurso de sugerencias de correo electrónico

Mensajes informativos acerca de un destinatario, que se muestran a los usuarios mientras que redactan un mensaje. Por ejemplo, un mensaje de fuera de la oficina como respuesta automática para un destinatario del mensaje.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
| automaticReplies | [automaticRepliesMailTips](../resources/automaticrepliesmailtips.md) | Si se ha configurado el destinatario de correo sugerencias para la respuesta automática. |
| customMailTip | String | Una sugerencia de correo personalizado que se puede establecer en el buzón del destinatario. |
| deliveryRestricted| Booleano | Si el buzón del destinatario está restringido, por ejemplo, aceptación de los mensajes de sólo una lista predefinida de remitentes, rechazar los mensajes de una lista predefinida de remitentes o aceptación de los mensajes de los remitentes autenticados sólo. |
| emailAddress | [emailAddress](../resources/emailaddress.md) | La dirección de correo electrónico del destinatario para obtener sugerencias de correo electrónico para. |
| error | [mailTipsError](../resources/mailtipserror.md) | Errores que se producen durante la acción [getMailTips](../api/user-getmailtips.md) . |
| externalMemberCount | Int32 | El número de miembros externos si el destinatario es una lista de distribución. |
| isModerated |Booleano  | Si requiere aprobación del envío de mensajes al destinatario. Por ejemplo, si el destinatario es una lista de distribución grande y un moderador se ha establecido hasta aprobar los mensajes enviados a esa lista de distribución, o si el envío de mensajes a un destinatario requiere aprobación del administrador del destinatario. |
| mailboxFull | Booleano | El estado completo del buzón de correo del destinatario. |
| maxMessageSize | Int32 | El tamaño máximo de mensaje que se ha configurado para la organización o el buzón de correo del destinatario. |
| recipientScope | recipientScopeType | El ámbito del destinatario. Los valores posibles son: `none`, `internal`, `external`, `externalPartner` y `externalNonParther`. Por ejemplo, un administrador puede establecer otra organización como su "socio". El ámbito es útil si un administrador desea limitar algunas sugerencias de correo electrónico puedan tener acceso a determinados ámbitos. También es útil para los remitentes para informarles de que su mensaje puede salir de la organización, ayudarlos a tomar las decisiones correctas acerca de redacción, tono y contenido.|
| recipientSuggestions | Colección [recipient](../resources/recipient.md) | Destinatarios sugieren en función de contextos anteriores donde aparecen en el mismo mensaje. |
| totalMemberCount | Int32 | El número de miembros si el destinatario es una lista de distribución. |

### <a name="recipientscopetype-values"></a>valores de recipientScopeType

| Valor
|:-------------------------
| ninguno
| interno
| externo
| externalPartner
| externalNonPartner


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "automaticReplies",
    "customMailTip",
    "deliveryRestricted",
    "emailAddress",
    "error",
    "externalMemberCount",
    "isModerated",
    "mailboxFull",
    "maxMessageSize",
    "recipientScope",
    "recipientSuggestions",
    "totalMemberCount"
  ],
  "@odata.type": "microsoft.graph.mailTips"
}-->

```json
{
  "automaticReplies": {"@odata.type": "microsoft.graph.automaticRepliesMailTips"},
  "customMailTip": "string",
  "deliveryRestricted": "boolean",
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"},
  "error": {"@odata.type": "microsoft.graph.mailTipsError"},
  "externalMemberCount": 1024,
  "isModerated": "boolean",
  "mailboxFull": "boolean",
  "maxMessageSize": 1024,
  "recipientScope": "string",
  "recipientSuggestions": [{"@odata.type": "microsoft.graph.recipient"}],
  "totalMemberCount": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailtips resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
