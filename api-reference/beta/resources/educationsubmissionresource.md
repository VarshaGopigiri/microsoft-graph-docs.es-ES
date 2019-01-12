---
title: tipo de recurso educationSubmissionResource
description: 'Un contenedor alrededor de un recurso para su uso en una presentación. El contenedor agrega un puntero al recurso de asignación si esto se copió desde la asignación.  '
author: dipakboyed
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: f242e4206c174634a3a8c3248942284798bb1550
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27979183"
---
# <a name="educationsubmissionresource-resource-type"></a>tipo de recurso educationSubmissionResource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un contenedor alrededor de un recurso para su uso en una presentación. El contenedor agrega un puntero al recurso de asignación si esto se copió desde la asignación.  


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener educationSubmissionResource](../api/educationsubmissionresource-get.md) | [educationSubmissionResource](educationsubmissionresource.md) |Leer las propiedades y relaciones de un objeto **educationSubmissionResource** .|
|[Delete](../api/educationsubmissionresource-delete.md) | Ninguno |Eliminación de un objeto **educationSubmissionResource** . |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|assignmentResourceUrl|Cadena|Puntero a la asignación desde la que se ha copiado este recurso. Si es null, el alumno carga el recurso.|
|id|Cadena| Solo lectura.|
|resource|[educationResource](educationresource.md)|Objeto de recurso.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationSubmissionResource"
}-->

```json
{
  "assignmentResourceUrl": "String",
  "id": "String (identifier)",
  "resource": {"@odata.type": "microsoft.graph.educationResource"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationSubmissionResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
