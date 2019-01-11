---
title: Tipo de recurso licenseUnitsDetail
description: La propiedad **prepaidUnits** de la entidad subscribedSku es de tipo **licenseUnitsDetail**.
localization_priority: Normal
ms.openlocfilehash: 8c2a4e995c7e1afa63b7f9daea6b61cbaf974958
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27810699"
---
# <a name="licenseunitsdetail-resource-type"></a><span data-ttu-id="26315-103">Tipo de recurso licenseUnitsDetail</span><span class="sxs-lookup"><span data-stu-id="26315-103">licenseUnitsDetail resource type</span></span>

<span data-ttu-id="26315-104">La propiedad **prepaidUnits** de la entidad [subscribedSku](subscribedsku.md) es de tipo **licenseUnitsDetail**.</span><span class="sxs-lookup"><span data-stu-id="26315-104">The **prepaidUnits** property of the [subscribedSku](subscribedsku.md) entity is of type **licenseUnitsDetail**.</span></span>

## <a name="properties"></a><span data-ttu-id="26315-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="26315-105">Properties</span></span>
| <span data-ttu-id="26315-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26315-106">Property</span></span>     | <span data-ttu-id="26315-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="26315-107">Type</span></span>   |<span data-ttu-id="26315-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="26315-108">Description</span></span>|
|:-------------|:-----|:----------|
|<span data-ttu-id="26315-109">enabled</span><span class="sxs-lookup"><span data-stu-id="26315-109">enabled</span></span>|<span data-ttu-id="26315-110">Int32</span><span class="sxs-lookup"><span data-stu-id="26315-110">Int32</span></span>| <span data-ttu-id="26315-111">El número de unidades habilitadas.</span><span class="sxs-lookup"><span data-stu-id="26315-111">The number of units that are enabled.</span></span> |
|<span data-ttu-id="26315-112">suspended</span><span class="sxs-lookup"><span data-stu-id="26315-112">suspended</span></span>|<span data-ttu-id="26315-113">Int32</span><span class="sxs-lookup"><span data-stu-id="26315-113">Int32</span></span>| <span data-ttu-id="26315-114">El número de unidades suspendidas.</span><span class="sxs-lookup"><span data-stu-id="26315-114">The number of units that are suspended.</span></span> |
|<span data-ttu-id="26315-115">warning</span><span class="sxs-lookup"><span data-stu-id="26315-115">warning</span></span>|<span data-ttu-id="26315-116">Int32</span><span class="sxs-lookup"><span data-stu-id="26315-116">Int32</span></span>| <span data-ttu-id="26315-117">El número de unidades que se encuentran en estado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="26315-117">The number of units that are in warning status.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="26315-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="26315-118">JSON representation</span></span>

<span data-ttu-id="26315-119">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="26315-119">Here is a JSON representation of the resource</span></span>

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
