---
title: Tipo de recurso sizeRange
description: Especifica los tamaños máximo y mínimo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.
ms.openlocfilehash: c84843116055c8ef13b7961b6ee180c4c896c80f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088660"
---
# <a name="sizerange-resource-type"></a><span data-ttu-id="b5412-103">Tipo de recurso sizeRange</span><span class="sxs-lookup"><span data-stu-id="b5412-103">sizeRange resource type</span></span>

> <span data-ttu-id="b5412-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b5412-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b5412-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b5412-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="b5412-106">Especifica los tamaños máximo y mínimo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.</span><span class="sxs-lookup"><span data-stu-id="b5412-106">Specifies the maximum and minimum sizes (in kilobytes) that an incoming message must have in order for a condition or exception to apply.</span></span>

## <a name="properties"></a><span data-ttu-id="b5412-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5412-107">Properties</span></span>
| <span data-ttu-id="b5412-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b5412-108">Property</span></span>     | <span data-ttu-id="b5412-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5412-109">Type</span></span>   |<span data-ttu-id="b5412-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5412-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b5412-111">maximumSize</span><span class="sxs-lookup"><span data-stu-id="b5412-111">maximumSize</span></span> | <span data-ttu-id="b5412-112">Int32</span><span class="sxs-lookup"><span data-stu-id="b5412-112">Int32</span></span> | <span data-ttu-id="b5412-113">Tamaño máximo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.</span><span class="sxs-lookup"><span data-stu-id="b5412-113">The maximum size (in kilobytes) that an incoming message must have in order for a condition or exception to apply.</span></span> |
| <span data-ttu-id="b5412-114">minimumSize</span><span class="sxs-lookup"><span data-stu-id="b5412-114">minimumSize</span></span> | <span data-ttu-id="b5412-115">Int32</span><span class="sxs-lookup"><span data-stu-id="b5412-115">Int32</span></span> | <span data-ttu-id="b5412-116">Tamaño mínimo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.</span><span class="sxs-lookup"><span data-stu-id="b5412-116">The minimum size (in kilobytes) that an incoming message must have in order for a condition or exception to apply.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="b5412-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b5412-117">JSON representation</span></span>
<span data-ttu-id="b5412-118">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b5412-118">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.sizeRange"
}-->

```json
{
  "maximumSize": "Int32",
  "minimumSize": "Int32"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sizeRange resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->