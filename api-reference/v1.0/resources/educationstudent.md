---
title: Tipo de recurso educationStudent
description: Información adicional que se agrega a un educationUser que se presenta cuando el primaryRole de un usuario es `student`.
ms.openlocfilehash: 4865831872f2ec9fe15c44692ed4e175c01befa5
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029235"
---
# <a name="educationstudent-resource-type"></a>Tipo de recurso educationStudent

Información adicional que se agrega a un [educationUser](educationuser.md) que se presenta cuando el primaryRole de un usuario es `student`.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|birthDate|Date| Fecha de nacimiento del alumno.|
|externalId|String| Identificador del alumno en el sistema de origen.|
|gender|educationGender| Los valores posibles son: `female`, `male`, `other`, `unknownFutureValue`.|
|grade|String|Curso actual del alumno.|
|graduationYear|String| Año de graduación del alumno en el centro educativo.|
|studentNumber|String| Número de alumno.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationStudent"
}-->

```json
{
  "birthDate": "String (timestamp)",
  "externalId": "String",
  "gender": "educationGender",
  "grade": "String",
  "graduationYear": "String",
  "studentNumber": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationStudent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
