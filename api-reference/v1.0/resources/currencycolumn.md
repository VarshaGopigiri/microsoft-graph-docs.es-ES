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
# <a name="currencycolumn-resource-type"></a><span data-ttu-id="2a1a3-102">Tipo de recurso CurrencyColumn</span><span class="sxs-lookup"><span data-stu-id="2a1a3-102">CurrencyColumn resource type</span></span>

<span data-ttu-id="2a1a3-103">El recurso **currencyColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna representan una moneda.</span><span class="sxs-lookup"><span data-stu-id="2a1a3-103">The **currencyColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values represent currency.</span></span>

## <a name="json-representation"></a><span data-ttu-id="2a1a3-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2a1a3-104">JSON representation</span></span>

<span data-ttu-id="2a1a3-105">A continuación se incluye una representación JSON de un recurso **currencyColumn**.</span><span class="sxs-lookup"><span data-stu-id="2a1a3-105">Here is a JSON representation of a **currencyColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.currencyColumn" } -->

```json
{
  "locale": "en-us"
}
```

## <a name="properties"></a><span data-ttu-id="2a1a3-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2a1a3-106">Properties</span></span>

| <span data-ttu-id="2a1a3-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="2a1a3-107">Property name</span></span> | <span data-ttu-id="2a1a3-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2a1a3-108">Type</span></span>   | <span data-ttu-id="2a1a3-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a1a3-109">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="2a1a3-110">**locale**</span><span class="sxs-lookup"><span data-stu-id="2a1a3-110">**locale**</span></span>    | <span data-ttu-id="2a1a3-111">string</span><span class="sxs-lookup"><span data-stu-id="2a1a3-111">string</span></span> | <span data-ttu-id="2a1a3-112">Especifica la configuración regional desde la que inferir el símbolo de moneda.</span><span class="sxs-lookup"><span data-stu-id="2a1a3-112">Specifies the locale from which to infer the currency symbol.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/CurrencyColumn"
} -->
