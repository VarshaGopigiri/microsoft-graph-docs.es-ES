---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: CurrencyColumn
ms.openlocfilehash: 4f3ae97e5abfb84ad523caf74fa70b1f1ec0322a
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="currencycolumn-resource-type"></a>Tipo de recurso CurrencyColumn

El recurso **currencyColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna representan una moneda.

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
