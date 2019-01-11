---
title: tipo de recurso networkLocationDetail
description: Indica los detalles asociados con la ubicación de red. .
localization_priority: Normal
ms.openlocfilehash: bfa84591f543253ed794016bbc2d25d325cd0bcc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834324"
---
# <a name="networklocationdetail-resource-type"></a><span data-ttu-id="8d1cb-104">tipo de recurso networkLocationDetail</span><span class="sxs-lookup"><span data-stu-id="8d1cb-104">networkLocationDetail resource type</span></span>
<span data-ttu-id="8d1cb-105">Indica los detalles asociados con la ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="8d1cb-105">Indicates details associated with the network location.</span></span> <span data-ttu-id="8d1cb-106">.</span><span class="sxs-lookup"><span data-stu-id="8d1cb-106"></span></span>



## <a name="properties"></a><span data-ttu-id="8d1cb-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8d1cb-107">Properties</span></span>
| <span data-ttu-id="8d1cb-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d1cb-108">Property</span></span>     | <span data-ttu-id="8d1cb-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d1cb-109">Type</span></span>   |<span data-ttu-id="8d1cb-110">Description</span><span class="sxs-lookup"><span data-stu-id="8d1cb-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8d1cb-111">networkType</span><span class="sxs-lookup"><span data-stu-id="8d1cb-111">networkType</span></span>|<span data-ttu-id="8d1cb-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="8d1cb-112">String</span></span>|<span data-ttu-id="8d1cb-113">Proporciona el tipo de la red.</span><span class="sxs-lookup"><span data-stu-id="8d1cb-113">Provides the type of the network.</span></span> <span data-ttu-id="8d1cb-114">Los valores posibles son `intranet`, `extranet`, `namedNetwork`, y `trusted`.</span><span class="sxs-lookup"><span data-stu-id="8d1cb-114">Possible values are `intranet`, `extranet`, `namedNetwork`, and `trusted`.</span></span>|
|<span data-ttu-id="8d1cb-115">networkName</span><span class="sxs-lookup"><span data-stu-id="8d1cb-115">networkName</span></span>|<span data-ttu-id="8d1cb-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="8d1cb-116">String</span></span>|<span data-ttu-id="8d1cb-117">Nombre de la red.</span><span class="sxs-lookup"><span data-stu-id="8d1cb-117">Name of the network.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="8d1cb-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8d1cb-118">JSON representation</span></span>

<span data-ttu-id="8d1cb-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8d1cb-119">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.deviceDetail"
}-->

```json
{
  "networkTypes": "namedNetork",
  "networkName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "deviceDetail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
