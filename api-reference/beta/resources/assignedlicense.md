---
title: Tipo de recurso assignedLicense
description: Representa una licencia asignada a un usuario. La propiedad **assignedLicenses** de la entidad user es una colección de **assignedLicense**.
ms.openlocfilehash: a41ece17882e6b85da009b4e29292e4b9a7965af
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090456"
---
# <a name="assignedlicense-resource-type"></a>Tipo de recurso assignedLicense

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Representa una licencia asignada a un usuario. La propiedad **assignedLicenses** de la entidad [user](user.md) es una colección de **assignedLicense**.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|disabledPlans|Colección Guid|Colección de los identificadores únicos para los planes que se han deshabilitado.|
|skuId|Guid|Identificador único de la SKU.|

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.assignedLicense"
}-->

```json
{
  "disabledPlans": ["guid"],
  "skuId": "guid"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "assignedLicense resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
