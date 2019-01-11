---
title: tipo de recurso convertIdResult
description: El resultado de una conversión de formato de identificador realizado por la función translateExchangeIds.
localization_priority: Normal
ms.openlocfilehash: 7e1878de3d3b7ddee36d799c928d6a130b578200
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27821458"
---
# <a name="convertidresult-resource-type"></a>tipo de recurso convertIdResult

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El resultado de una conversión de formato de identificador realizado por la función [translateExchangeIds](../api/user-translateexchangeids.md) .

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Description |
|:---------|:-----|:------------|
| sourceId | Cadena | El identificador que se va a convertir. Este valor es el identificador original, reactivar convertido. |
| targetId | Cadena | El identificador convertido. Este valor no está presente si la conversión produjo un error. |
| errorDetails | [Error genérico](genericerror.md) | Un objeto de error que indica el motivo del error de conversión. Este valor no está presente si la conversión se ha realizado correctamente. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "targetId",
    "errorDetails"
  ],
  "@odata.type": "microsoft.graph.convertIdResult"
}-->

```json
{
  "sourceId": "String",
  "targetId": "String",
  "errorDetails": {
    "@odata.type": "microsoft.graph.genericError"
  }
}
```
