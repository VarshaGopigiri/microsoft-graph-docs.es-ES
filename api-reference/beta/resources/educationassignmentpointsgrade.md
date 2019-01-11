---
title: tipo de recurso educationAssignmentPointsGrade
description: Cuando se establece una asignación a un tipo de categoría de puntos, cada envío tendrá este objeto asociado con la propiedad **submission.grade** . Esto crea una subclase de educationAssignmentGrade,
localization_priority: Normal
ms.openlocfilehash: 2084a1bda6784165576c3ec454fa9ee88601c952
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27861407"
---
# <a name="educationassignmentpointsgrade-resource-type"></a>tipo de recurso educationAssignmentPointsGrade

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Cuando se establece una asignación a un tipo de categoría de puntos, cada envío tendrá este objeto asociado con la propiedad **submission.grade** . Esto crea una subclase de [educationAssignmentGrade](educationassignmentgrade.md), que el que va a agregar datos a esta propiedad. Los puntos máx. se almacena en la propiedad **assignments.grading** .


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|points|Single|Número de puntos de un profesor es dar a este objeto de envío.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationAssignmentPointsGrade"
}-->

```json
{
  "points": "Single"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationAssignmentPointsGrade resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
