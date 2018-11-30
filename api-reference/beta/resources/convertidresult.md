---
title: tipo de recurso convertIdResult
description: El resultado de una conversión de formato de identificador realizado por la función translateExchangeIds.
ms.openlocfilehash: 3a17399ffe44c43c78f7b50933b2e847a3e64f32
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084474"
---
# <a name="convertidresult-resource-type"></a>tipo de recurso convertIdResult

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El resultado de una conversión de formato de identificador realizado por la función [translateExchangeIds](../api/user-translateexchangeids.md) .

## <a name="properties"></a>Propiedades

| Propiedad | Tipo | Descripción |
|:---------|:-----|:------------|
| sourceId | String | El identificador que se va a convertir. Este valor es el identificador original, reactivar convertido. |
| targetId | String | El identificador convertido. Este valor no está presente si la conversión produjo un error. |
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