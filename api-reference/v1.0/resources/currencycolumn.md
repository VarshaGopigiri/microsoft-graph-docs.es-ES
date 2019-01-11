---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: CurrencyColumn
localization_priority: Normal
ms.openlocfilehash: e4ee085882cadafc0102ee31e17841978cef7822
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27836459"
---
# <a name="currencycolumn-resource-type"></a><span data-ttu-id="8e912-102">Tipo de recurso CurrencyColumn</span><span class="sxs-lookup"><span data-stu-id="8e912-102">CurrencyColumn resource type</span></span>

<span data-ttu-id="8e912-103">El recurso **currencyColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna representan una moneda.</span><span class="sxs-lookup"><span data-stu-id="8e912-103">The **currencyColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values represent currency.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8e912-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8e912-104">JSON representation</span></span>

<span data-ttu-id="8e912-105">A continuación se incluye una representación JSON de un recurso **currencyColumn**.</span><span class="sxs-lookup"><span data-stu-id="8e912-105">Here is a JSON representation of a **currencyColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.currencyColumn" } -->

```json
{
  "locale": "en-us"
}
```

## <a name="properties"></a><span data-ttu-id="8e912-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e912-106">Properties</span></span>

| <span data-ttu-id="8e912-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="8e912-107">Property name</span></span> | <span data-ttu-id="8e912-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e912-108">Type</span></span>   | <span data-ttu-id="8e912-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e912-109">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="8e912-110">**locale**</span><span class="sxs-lookup"><span data-stu-id="8e912-110">**locale**</span></span>    | <span data-ttu-id="8e912-111">string</span><span class="sxs-lookup"><span data-stu-id="8e912-111">string</span></span> | <span data-ttu-id="8e912-112">Especifica la configuración regional desde la que inferir el símbolo de moneda.</span><span class="sxs-lookup"><span data-stu-id="8e912-112">Specifies the locale from which to infer the currency symbol.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/CurrencyColumn"
} -->
