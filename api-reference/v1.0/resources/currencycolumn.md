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
# <a name="currencycolumn-resource-type"></a><span data-ttu-id="b59de-102">Tipo de recurso CurrencyColumn</span><span class="sxs-lookup"><span data-stu-id="b59de-102">CurrencyColumn resource type</span></span>

<span data-ttu-id="b59de-103">El recurso **currencyColumn** en un recurso [columnDefinition](columnDefinition.md) indica que los valores de la columna representan una moneda.</span><span class="sxs-lookup"><span data-stu-id="b59de-103">The **currencyColumn** on a [columnDefinition](columnDefinition.md) resource indicates that the column's values represent currency.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b59de-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b59de-104">JSON representation</span></span>

<span data-ttu-id="b59de-105">A continuación se incluye una representación JSON de un recurso **currencyColumn**.</span><span class="sxs-lookup"><span data-stu-id="b59de-105">Here is a JSON representation of a **baseItem** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.currencyColumn" } -->

```json
{
  "locale": "en-us"
}
```

## <a name="properties"></a><span data-ttu-id="b59de-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b59de-106">Properties</span></span>

| <span data-ttu-id="b59de-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="b59de-107">Property name</span></span> | <span data-ttu-id="b59de-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b59de-108">Type</span></span>   | <span data-ttu-id="b59de-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b59de-109">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="b59de-110">**locale**</span><span class="sxs-lookup"><span data-stu-id="b59de-110">**locale**</span></span>    | <span data-ttu-id="b59de-111">string</span><span class="sxs-lookup"><span data-stu-id="b59de-111">string</span></span> | <span data-ttu-id="b59de-112">Especifica la configuración regional desde la que inferir el símbolo de moneda.</span><span class="sxs-lookup"><span data-stu-id="b59de-112">Specifies the locale from which to infer the currency symbol.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/CurrencyColumn"
} -->
