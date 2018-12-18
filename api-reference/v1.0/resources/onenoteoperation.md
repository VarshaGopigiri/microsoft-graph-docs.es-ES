---
title: Tipo de recurso onenoteOperation
description: Estado de ciertas operaciones de OneNote de larga duración.
author: Jewan-microsoft
ms.openlocfilehash: bbb7b9457ce5a3d7ba9faf45d893ae86cdfd8b32
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326911"
---
# <a name="onenoteoperation-resource-type"></a>Tipo de recurso onenoteOperation

Estado de ciertas operaciones de OneNote de larga duración.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.operation",
  "@odata.type": "microsoft.graph.onenoteOperation"
}-->

```json
{
  "createdDateTime": "String (timestamp)",
  "error": {"@odata.type": "microsoft.graph.onenoteOperationError"},
  "id": "string (identifier)",
  "lastActionDateTime": "String (timestamp)",
  "resourceId": "string",
  "resourceLocation": "string",
  "status": "string",
  "percentComplete": "string"
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|createdDateTime| DateTimeOffset |La hora de inicio de la operación.|
|error|[onenoteOperationError](onenoteoperationerror.md)|Error devuelto por la operación.|
|id|string|Id. de operación. Solo lectura.|
|lastActionDateTime| DateTimeOffset |Hora de la última acción de la operación.|
|resourceId|string|Identificador del recurso.|
|resourceLocation|string|URI de recurso del objeto. Por ejemplo, el URI de recurso de una página o sección copiada. |
|status|cadena|Estado actual de la operación: `notstarted`, `running`, `completed` o `failed` |
|percentComplete|cadena|El porcentaje de operación completada si la operación todavía tiene el estado `running`

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener operation](../api/onenoteoperation-get.md) | [onenoteOperation](onenoteoperation.md) |Obtener el estado actual de la operación. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onenoteOperation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
