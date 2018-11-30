---
author: rgregg
ms.author: rgregg
ms.date: 09/11/2017
title: CurrencyColumn
ms.openlocfilehash: 21c95026eb61eb68c98010d8ac288be115e95ec8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090858"
---
# <a name="currencycolumn-resource-type"></a><span data-ttu-id="c258b-102">Tipo de recurso CurrencyColumn</span><span class="sxs-lookup"><span data-stu-id="c258b-102">CurrencyColumn resource type</span></span>

> <span data-ttu-id="c258b-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c258b-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c258b-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c258b-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c258b-105">El recurso **currencyColumn** en un recurso [columnDefinition](columndefinition.md) indica que los valores de la columna representan una moneda.</span><span class="sxs-lookup"><span data-stu-id="c258b-105">The **currencyColumn** on a [columnDefinition](columndefinition.md) resource indicates that the column's values represent currency.</span></span>

## <a name="json-representation"></a><span data-ttu-id="c258b-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c258b-106">JSON representation</span></span>

<span data-ttu-id="c258b-107">A continuación se incluye una representación JSON de un recurso **currencyColumn**.</span><span class="sxs-lookup"><span data-stu-id="c258b-107">Here is a JSON representation of a **currencyColumn** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.currencyColumn" } -->

```json
{
  "locale": "en-us"
}
```

## <a name="properties"></a><span data-ttu-id="c258b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c258b-108">Properties</span></span>

| <span data-ttu-id="c258b-109">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="c258b-109">Property name</span></span> | <span data-ttu-id="c258b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c258b-110">Type</span></span>   | <span data-ttu-id="c258b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c258b-111">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="c258b-112">**locale**</span><span class="sxs-lookup"><span data-stu-id="c258b-112">**locale**</span></span>    | <span data-ttu-id="c258b-113">string</span><span class="sxs-lookup"><span data-stu-id="c258b-113">string</span></span> | <span data-ttu-id="c258b-114">Especifica la configuración regional desde la que inferir el símbolo de moneda.</span><span class="sxs-lookup"><span data-stu-id="c258b-114">Specifies the locale from which to infer the currency symbol.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/CurrencyColumn"
} -->
