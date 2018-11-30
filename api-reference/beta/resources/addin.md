---
title: tipo de recurso addIn
description: Aquí tiene una representación JSON del recurso.
ms.openlocfilehash: c95f6bcc7fa26d77bc5a9595a6c80d0c4a94769c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088808"
---
# <a name="addin-resource-type"></a><span data-ttu-id="43f1c-103">tipo de recurso addIn</span><span class="sxs-lookup"><span data-stu-id="43f1c-103">addIn resource type</span></span>

> <span data-ttu-id="43f1c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="43f1c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="43f1c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="43f1c-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="json-representation"></a><span data-ttu-id="43f1c-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="43f1c-106">JSON representation</span></span>

<span data-ttu-id="43f1c-107">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="43f1c-107">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="43f1c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="43f1c-108">Properties</span></span>
| <span data-ttu-id="43f1c-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="43f1c-109">Property</span></span>     | <span data-ttu-id="43f1c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="43f1c-110">Type</span></span>   |<span data-ttu-id="43f1c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="43f1c-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="43f1c-112">id</span><span class="sxs-lookup"><span data-stu-id="43f1c-112">id</span></span>|<span data-ttu-id="43f1c-113">GUID</span><span class="sxs-lookup"><span data-stu-id="43f1c-113">guid</span></span>||
|<span data-ttu-id="43f1c-114">propiedades</span><span class="sxs-lookup"><span data-stu-id="43f1c-114">properties</span></span>|<span data-ttu-id="43f1c-115">colección [keyValue](keyvalue.md)</span><span class="sxs-lookup"><span data-stu-id="43f1c-115">[keyValue](keyvalue.md) collection</span></span>||
|<span data-ttu-id="43f1c-116">type</span><span class="sxs-lookup"><span data-stu-id="43f1c-116">type</span></span>|<span data-ttu-id="43f1c-117">cadena</span><span class="sxs-lookup"><span data-stu-id="43f1c-117">string</span></span>||

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "addIn resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->