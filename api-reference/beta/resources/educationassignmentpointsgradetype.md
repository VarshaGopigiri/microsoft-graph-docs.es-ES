---
title: tipo de recurso educationAssignmentPointsGradeType
description: Se utiliza con la propiedad **assignments.grading** . Esto es una subclase de educationAssignmentGradeType.
ms.openlocfilehash: 5c170540e99003a78df0550d4d6542c07df8f1ff
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090155"
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