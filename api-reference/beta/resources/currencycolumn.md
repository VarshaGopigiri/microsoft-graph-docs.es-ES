---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: CurrencyColumn
localization_priority: Normal
ms.openlocfilehash: 179c0bb1e5c82d7f2af17dcbcae08be8726f2ecd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888938"
---
# <a name="currencycolumn-resource-type"></a><span data-ttu-id="63947-102">Tipo de recurso CurrencyColumn</span><span class="sxs-lookup"><span data-stu-id="63947-102">CurrencyColumn resource type</span></span>

> <span data-ttu-id="63947-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="63947-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="63947-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="63947-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="63947-105">El recurso **currencyColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna representan una moneda.</span><span class="sxs-lookup"><span data-stu-id="63947-105">The **currencyColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values represent currency.</span></span>

## <a name="json-representation"></a><span data-ttu-id="63947-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="63947-106">JSON representation</span></span>

<span data-ttu-id="63947-107">A continuación se incluye una representación JSON de un recurso **currencyColumn**.</span><span class="sxs-lookup"><span data-stu-id="63947-107">Here is a JSON representation of a **currencyColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.currencyColumn" } -->

```json
{
  "locale": "en-us"
}
```

## <a name="properties"></a><span data-ttu-id="63947-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63947-108">Properties</span></span>

| <span data-ttu-id="63947-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="63947-109">Property name</span></span> | <span data-ttu-id="63947-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="63947-110">Type</span></span>   | <span data-ttu-id="63947-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="63947-111">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="63947-112">**locale**</span><span class="sxs-lookup"><span data-stu-id="63947-112">**locale**</span></span>    | <span data-ttu-id="63947-113">string</span><span class="sxs-lookup"><span data-stu-id="63947-113">string</span></span> | <span data-ttu-id="63947-114">Especifica la configuración regional desde la que inferir el símbolo de moneda.</span><span class="sxs-lookup"><span data-stu-id="63947-114">Specifies the locale from which to infer the currency symbol.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/CurrencyColumn"
} -->
