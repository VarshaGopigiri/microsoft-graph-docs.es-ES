---
title: Tipo de recurso recipient
description: 'Representa información sobre un usuario en la finalización del envío o la recepción de un evento, un mensaje o una publicación de grupo. '
ms.openlocfilehash: 2ecf92f314c8b29da529b8dc07cada71dd8571f2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088885"
---
# <a name="recipient-resource-type"></a>Tipo de recurso recipient

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa información sobre un usuario en la finalización del envío o la recepción de un evento, un mensaje o una publicación de grupo. 

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|emailAddress|[EmailAddress](emailaddress.md)|Dirección de correo del destinatario.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recipient"
}-->

```json
{
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recipient resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->