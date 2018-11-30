---
title: Tipo de recurso plannerChecklistItems
description: El recurso **plannerChecklistItemCollection** representa la colección de elementos de la lista de comprobación de una tarea. Es un tipo abierto. Forma parte del objeto task details. El valor del par propiedad-valor es el objeto checklistItem.
ms.openlocfilehash: 3a08fe5bea1c7aaf493500b503e9ff85dc460acc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031584"
---
# <a name="plannerchecklistitems-resource-type"></a>Tipo de recurso plannerChecklistItems

El recurso **plannerChecklistItemCollection** representa la colección de elementos de la lista de comprobación de una tarea. Es un tipo abierto. Forma parte del objeto [task details](plannertaskdetails.md). El valor del par propiedad-valor es el objeto [checklistItem](plannerchecklistitem.md).


## <a name="properties"></a>Propiedades
El cliente puede definir las propiedades de un tipo abierto. En este caso, el cliente debe proporcionar los **GUID** como propiedades y sus valores deben ser objetos [checklistItem](plannerchecklistitem.md). A continuación se muestra un ejemplo. Para quitar un elemento de la lista de comprobación, establezca el valor de la propiedad en `null`.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [ "String-value" ],
  "@odata.type": "microsoft.graph.plannerChecklistItems"
}-->

```json
{
  "String-value":
  {
    "isChecked": true,
    "lastModifiedBy": "String-value",
    "lastModifiedByDateTime": "String(timestamp)",
    "orderHint": "String-value",
    "title": "String-value"
  }
}
```
// Ejemplo

```json
{
  "3a73c9dd-fb47-4230-9c0f-b80788fb0f9b": // client-generated GUID
  {
    "@odata.type": "microsoft.graph.checklistItem", // required in PATCH requests to edit the checklist on a task
    "isChecked": true,
    "lastModifiedBy": {
      "user": {
        "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
      }
    },
    "lastModifiedByDateTime": "2015-09-21T17:45:12.039Z",
    "orderHint": "0009005756397228702",
    "title": "Get stamps"
  },
  "5f36f5b2-1ec0-4c48-9c75-ed59429516c5":
  {
     "@odata.type": "microsoft.graph.checklistItem",
    "isChecked": false,
    "lastModifiedBy": {
      "user": {
        "id": "ebf3b108-5234-4e22-b93d-656d7dae5874"
      }
    },
    "lastModifiedByDateTime": "2015-09-21T17:45:12.039Z",
    "orderHint": "0004105723397228784",
    "title": "Mail card at UPS"
  }
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "plannerChecklistItems resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->