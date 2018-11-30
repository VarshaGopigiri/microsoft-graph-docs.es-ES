---
title: Tipo de recurso licenseUnitsDetail
description: La propiedad **prepaidUnits** de la entidad subscribedSku es de tipo **licenseUnitsDetail**.
ms.openlocfilehash: e8cf5253676dab8a4b31c3ab33faa0af3ddfd527
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028769"
---
# <a name="licenseunitsdetail-resource-type"></a><span data-ttu-id="b85a8-103">Tipo de recurso licenseUnitsDetail</span><span class="sxs-lookup"><span data-stu-id="b85a8-103">licenseUnitsDetail resource type</span></span>

<span data-ttu-id="b85a8-104">La propiedad **prepaidUnits** de la entidad [subscribedSku](subscribedsku.md) es de tipo **licenseUnitsDetail**.</span><span class="sxs-lookup"><span data-stu-id="b85a8-104">The **prepaidUnits** property of the [subscribedSku](subscribedsku.md) entity is of type **licenseUnitsDetail**.</span></span>

## <a name="properties"></a><span data-ttu-id="b85a8-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b85a8-105">Properties</span></span>
| <span data-ttu-id="b85a8-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b85a8-106">Property</span></span>     | <span data-ttu-id="b85a8-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="b85a8-107">Type</span></span>   |<span data-ttu-id="b85a8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="b85a8-108">Description</span></span>|
|:-------------|:-----|:----------|
|<span data-ttu-id="b85a8-109">enabled</span><span class="sxs-lookup"><span data-stu-id="b85a8-109">enabled</span></span>|<span data-ttu-id="b85a8-110">Int32</span><span class="sxs-lookup"><span data-stu-id="b85a8-110">Int32</span></span>| <span data-ttu-id="b85a8-111">El número de unidades habilitadas.</span><span class="sxs-lookup"><span data-stu-id="b85a8-111">The number of units that are enabled.</span></span> |
|<span data-ttu-id="b85a8-112">suspended</span><span class="sxs-lookup"><span data-stu-id="b85a8-112">suspended</span></span>|<span data-ttu-id="b85a8-113">Int32</span><span class="sxs-lookup"><span data-stu-id="b85a8-113">Int32</span></span>| <span data-ttu-id="b85a8-114">El número de unidades suspendidas.</span><span class="sxs-lookup"><span data-stu-id="b85a8-114">The number of units that are suspended.</span></span> |
|<span data-ttu-id="b85a8-115">warning</span><span class="sxs-lookup"><span data-stu-id="b85a8-115">warning</span></span>|<span data-ttu-id="b85a8-116">Int32</span><span class="sxs-lookup"><span data-stu-id="b85a8-116">Int32</span></span>| <span data-ttu-id="b85a8-117">El número de unidades que se encuentran en estado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="b85a8-117">The number of units that are in warning status.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="b85a8-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b85a8-118">JSON representation</span></span>

<span data-ttu-id="b85a8-119">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b85a8-119">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.licenseUnitsDetail"
}-->

```json
{
  "enabled": 1024,
  "suspended": 1024,
  "warning": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "licenseUnitsDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
