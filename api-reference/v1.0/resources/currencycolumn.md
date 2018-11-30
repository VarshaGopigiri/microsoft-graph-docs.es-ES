---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: CurrencyColumn
ms.openlocfilehash: 796bd9fc7bf379ea38dc2d2f602411740caf4b86
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032373"
---
# <a name="currencycolumn-resource-type"></a>Tipo de recurso CurrencyColumn

El recurso **currencyColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna representan una moneda.

## <a name="json-representation"></a>Representación JSON

A continuación se incluye una representación JSON de un recurso **currencyColumn**.
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.currencyColumn" } -->

```json
{
  "locale": "en-us"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad | Tipo   | Descripción
|:--------------|:-------|:----------------------------------------------------
| **locale**    | string | Especifica la configuración regional desde la que inferir el símbolo de moneda.

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/CurrencyColumn"
} -->
