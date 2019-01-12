---
title: tipo de recurso educationAssignmentPointsGradeType
description: Se utiliza con la propiedad **assignments.grading** . Esto es una subclase de educationAssignmentGradeType.
localization_priority: Normal
author: dipakboyed
ms.prod: education
ms.openlocfilehash: b603ccec0ddd5be5003353a5062e51554cb61c53
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952667"
---
# <a name="educationassignmentpointsgradetype-resource-type"></a>tipo de recurso educationAssignmentPointsGradeType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Se utiliza con la propiedad **assignments.grading** . Esto es una subclase de [educationAssignmentGradeType](educationassignmentgradetype.md).

Esto indica que la asignación es clasificada y almacena el número máximo de puntos de que cada alumno puede lograr en este elemento de trabajo. Cuando se establece en una asignación, cada envío obtendrá una propiedad [educationAssignmentPointsGrade](educationassignmentpointsgrade.md) asociada para el almacenamiento de los puntos de cada alumno.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|maxPoints|Single| Max puntos posibles para esta asignación.  |

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationAssignmentPointsGradeType"
}-->

```json
{
  "maxPoints": "Single"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationAssignmentPointsGradeType resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
