---
title: Tipo de recurso onenoteOperation
description: Estado de ciertas operaciones de OneNote de larga duración.
ms.openlocfilehash: af7da970a148d4b70385487503e3abf6431c430a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084227"
---
# <a name="onenoteoperation-resource-type"></a>Tipo de recurso onenoteOperation

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Estado de ciertas operaciones de OneNote de larga duración.

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
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
