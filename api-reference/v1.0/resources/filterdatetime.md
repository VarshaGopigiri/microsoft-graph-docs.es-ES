---
title: Tipo de recurso FilterDatetime
description: Representa cómo se filtra una fecha cuando se filtran valores.
ms.openlocfilehash: 8156b9f5779dd8d70ff3a839d8a6ef4f5753bacd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028737"
---
# <a name="filterdatetime-resource-type"></a>Tipo de recurso FilterDatetime

Representa cómo se filtra una fecha cuando se filtran valores.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|fecha|string|La fecha en formato ISO8601 usada para filtrar los datos.|
|specificity|string|¿Cómo específica la fecha debe usarse para mantener los datos. Por ejemplo, si la fecha es 2005-04-02 y el specifity se establece en "mes", la operación de filtrado mantener todas las filas con una fecha en el mes de abril de 2009. Los valores posibles son: `Year`, `Monday`, `Day`, `Hour`, `Minute`, `Second`.|

## <a name="relationships"></a>Relaciones
Ninguno


## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookFilterDateTime"
}-->

```json
{
  "date": "string",
  "specificity": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "FilterDatetime resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->