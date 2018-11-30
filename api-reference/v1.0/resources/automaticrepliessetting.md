---
title: Tipo de recurso automaticRepliesSetting
description: 'Opciones de configuración para notificar automáticamente al remitente de un correo electrónico entrante con un mensaje desde la '
ms.openlocfilehash: 983f5062c5a7bacaccfdca4687705aed5aa7a604
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028605"
---
# <a name="automaticrepliessetting-resource-type"></a>Tipo de recurso automaticRepliesSetting

Opciones de configuración para notificar de forma automática al remitente de un mensaje de correo entrante con un mensaje del usuario que ha iniciado sesión. Por ejemplo, una respuesta automática para notificar que el usuario que ha iniciado sesión no está disponible para responder a correos electrónicos. 


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|externalAudience|externalAudienceScope| El conjunto de audiencia externo a la organización del usuario que ha iniciado sesión que va a recibir el **ExternalReplyMessage**, si el **estado** es `AlwaysEnabled` o `Scheduled`. Los valores posibles son: `none`, `contactsOnly`, `all`.|
|externalReplyMessage|string|La respuesta automática para enviar a la audiencia externa especificada, si **Status** es `AlwaysEnabled` o `Scheduled`.|
|internalReplyMessage|string|La respuesta automática para enviar a la audiencia interna de la organización del usuario que ha iniciado sesión, si **Status** es `AlwaysEnabled` o `Scheduled`. |
|scheduledEndDateTime|[dateTimeTimeZone](datetimetimezone.md)|La fecha y hora en que se establece la finalización de las respuestas automáticas, si **Status** se establece en `Scheduled`. |
|scheduledStartDateTime|[dateTimeTimeZone](datetimetimezone.md)|La fecha y hora en que se establece el inicio de las respuestas automáticas, si **Status** se establece en `Scheduled`.|
|status|automaticRepliesStatus|Estado de las configuraciones de las respuestas automáticas. Los valores posibles son: `disabled`, `alwaysEnabled`, `scheduled`.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.automaticRepliesSetting"
}-->

```json
{
  "externalAudience": "String",
  "externalReplyMessage": "string",
  "internalReplyMessage": "string",
  "scheduledEndDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "scheduledStartDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "status": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "automaticRepliesSetting resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
