---
title: tipo de recurso addIn
description: Aquí tiene una representación JSON del recurso.
localization_priority: Normal
ms.openlocfilehash: 6e76b8f7981be5da9a2ac8437ff21d4a59dbbe73
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884220"
---
# <a name="addin-resource-type"></a><span data-ttu-id="a3911-103">tipo de recurso addIn</span><span class="sxs-lookup"><span data-stu-id="a3911-103">addIn resource type</span></span>

> <span data-ttu-id="a3911-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a3911-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a3911-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a3911-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="json-representation"></a><span data-ttu-id="a3911-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a3911-106">JSON representation</span></span>

<span data-ttu-id="a3911-107">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a3911-107">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.addIn"
}-->

```json
{
  "id": "guid",
  "properties": [{"@odata.type": "microsoft.graph.keyvalue"}],
  "type": "string"
}

```
## <a name="properties"></a><span data-ttu-id="a3911-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3911-108">Properties</span></span>
| <span data-ttu-id="a3911-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a3911-109">Property</span></span>     | <span data-ttu-id="a3911-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a3911-110">Type</span></span>   |<span data-ttu-id="a3911-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3911-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a3911-112">id</span><span class="sxs-lookup"><span data-stu-id="a3911-112">id</span></span>|<span data-ttu-id="a3911-113">GUID</span><span class="sxs-lookup"><span data-stu-id="a3911-113">guid</span></span>||
|<span data-ttu-id="a3911-114">propiedades</span><span class="sxs-lookup"><span data-stu-id="a3911-114">properties</span></span>|<span data-ttu-id="a3911-115">colección [keyValue](keyvalue.md)</span><span class="sxs-lookup"><span data-stu-id="a3911-115">[keyValue](keyvalue.md) collection</span></span>||
|<span data-ttu-id="a3911-116">type</span><span class="sxs-lookup"><span data-stu-id="a3911-116">type</span></span>|<span data-ttu-id="a3911-117">cadena</span><span class="sxs-lookup"><span data-stu-id="a3911-117">string</span></span>||

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "addIn resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
