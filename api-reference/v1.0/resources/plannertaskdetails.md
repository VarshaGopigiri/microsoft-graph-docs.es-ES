---
title: Tipo de recurso plannerTaskDetails
description: El recurso **plannerTaskDetails** representa la información adicional de una tarea. Cada objeto task tiene un objeto details.
localization_priority: Normal
ms.openlocfilehash: a183ba0f9b19ea2de700913d29e9586442ba2c03
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27806578"
---
# <a name="plannertaskdetails-resource-type"></a>Tipo de recurso plannerTaskDetails

El recurso **plannerTaskDetails** representa la información adicional de una tarea. Cada objeto [task](plannertask.md) tiene un objeto details.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener plannerTaskDetails](../api/plannertaskdetails-get.md) | [plannerTaskDetails](plannertaskdetails.md) |Leer las propiedades y las relaciones del objeto **plannerTaskDetails**.|
|[Update](../api/plannertaskdetails-update.md) | [plannerTaskDetails](plannertaskdetails.md)    |Actualizar el objeto **plannerTaskDetails**. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|checklist|[plannerChecklistItems](plannerchecklistitems.md)|Colección de elementos de la lista de comprobación de la tarea.|
|description|Cadena|Descripción de la tarea|
|id|Cadena| Solo lectura. Identificador de los detalles de la tarea. Es 28 caracteres de largo y entre mayúsculas y minúsculas. [Validación de formato](planner-identifiers-disclaimer.md) se realiza en el servicio.|
|previewType|string|Esto establece el tipo de vista previa que se muestra en la tarea. Los valores posibles son: `automatic`, `noPreview`, `checklist`, `description`, `reference`. Cuando se establece en `automatic` la vista previa que se muestra es elegida por la aplicación de visualización de la tarea.|
|references|[plannerExternalReferences](plannerexternalreferences.md)|La colección de referencias de la tarea.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.plannerTaskDetails"
}-->

```json
{
  "checklist": {"@odata.type": "microsoft.graph.plannerChecklistItems"},
  "description": "String",
  "id": "String (identifier)",
  "previewType": "string",
  "references": {"@odata.type": "microsoft.graph.plannerExternalReferences"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerTaskDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
