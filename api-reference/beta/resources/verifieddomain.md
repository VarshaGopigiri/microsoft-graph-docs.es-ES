---
title: Tipo de recurso verifiedDomain
description: Especifica un dominio para un inquilino. La propiedad **verifiedDomains** de la entidad organization es una colección de **VerifiedDomain**.
ms.openlocfilehash: 810b5fea0fbaf82eeb452c0f5c6032679590ff49
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088433"
---
# <a name="verifieddomain-resource-type"></a>Tipo de recurso verifiedDomain

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Especifica un dominio para un inquilino. La propiedad **verifiedDomains** de la entidad [organization](organization.md) es una colección de **VerifiedDomain**.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|capabilities|String|Por ejemplo, "Email", "OfficeCommunicationsOnline".|
|isDefault|Boolean|                **true** si se trata del dominio predeterminado asociado al inquilino; de lo contrario, **false**.            |
|isInitial|Boolean|**true** si se trata del dominio inicial asociado al inquilino; de lo contrario, **false**.|
|name|String|Nombre del dominio; por ejemplo, "contoso.onmicrosoft.com".|
|type|String|Por ejemplo, "Administrado".|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.verifieddomain"
}-->

```json
{
  "capabilities": "string",
  "isDefault": true,
  "isInitial": true,
  "name": "string",
  "type": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "verifiedDomain resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
