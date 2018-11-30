---
title: Tipo de recurso licenseUnitsDetail
description: La propiedad **prepaidUnits** de la entidad subscribedSku es de tipo **licenseUnitsDetail**.
ms.openlocfilehash: 5f3d62c39248739746923195945efbc3322d5686
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083208"
---
# <a name="licenseunitsdetail-resource-type"></a><span data-ttu-id="cd169-103">Tipo de recurso licenseUnitsDetail</span><span class="sxs-lookup"><span data-stu-id="cd169-103">licenseUnitsDetail resource type</span></span>

> <span data-ttu-id="cd169-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cd169-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cd169-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cd169-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="cd169-106">La propiedad **prepaidUnits** de la entidad [subscribedSku](subscribedsku.md) es de tipo **licenseUnitsDetail**.</span><span class="sxs-lookup"><span data-stu-id="cd169-106">The **prepaidUnits** property of the [subscribedSku](subscribedsku.md) entity is of type **licenseUnitsDetail**.</span></span>

## <a name="properties"></a><span data-ttu-id="cd169-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cd169-107">Properties</span></span>
| <span data-ttu-id="cd169-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cd169-108">Property</span></span>     | <span data-ttu-id="cd169-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd169-109">Type</span></span>   |<span data-ttu-id="cd169-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd169-110">Description</span></span>|
|:-------------|:-----|:----------|
|<span data-ttu-id="cd169-111">enabled</span><span class="sxs-lookup"><span data-stu-id="cd169-111">enabled</span></span>|<span data-ttu-id="cd169-112">Int32</span><span class="sxs-lookup"><span data-stu-id="cd169-112">Int32</span></span>| <span data-ttu-id="cd169-113">El número de unidades habilitadas.</span><span class="sxs-lookup"><span data-stu-id="cd169-113">The number of units that are enabled.</span></span> |
|<span data-ttu-id="cd169-114">suspended</span><span class="sxs-lookup"><span data-stu-id="cd169-114">suspended</span></span>|<span data-ttu-id="cd169-115">Int32</span><span class="sxs-lookup"><span data-stu-id="cd169-115">Int32</span></span>| <span data-ttu-id="cd169-116">El número de unidades suspendidas.</span><span class="sxs-lookup"><span data-stu-id="cd169-116">The number of units that are suspended.</span></span> |
|<span data-ttu-id="cd169-117">warning</span><span class="sxs-lookup"><span data-stu-id="cd169-117">warning</span></span>|<span data-ttu-id="cd169-118">Int32</span><span class="sxs-lookup"><span data-stu-id="cd169-118">Int32</span></span>| <span data-ttu-id="cd169-119">El número de unidades que se encuentran en estado de advertencia.</span><span class="sxs-lookup"><span data-stu-id="cd169-119">The number of units that are in warning status.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="cd169-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cd169-120">JSON representation</span></span>

<span data-ttu-id="cd169-121">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="cd169-121">Here is a JSON representation of the resource</span></span>

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
