---
title: tipo de recurso networkLocationDetail
description: Indica los detalles asociados con la ubicación de red. .
ms.openlocfilehash: 5dd1410318d380a1b943de6a7dbb0d739172cc76
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087629"
---
# <a name="networklocationdetail-resource-type"></a><span data-ttu-id="b2a07-104">tipo de recurso networkLocationDetail</span><span class="sxs-lookup"><span data-stu-id="b2a07-104">networkLocationDetail resource type</span></span>
<span data-ttu-id="b2a07-105">Indica los detalles asociados con la ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="b2a07-105">Indicates details associated with the network location.</span></span> <span data-ttu-id="b2a07-106">.</span><span class="sxs-lookup"><span data-stu-id="b2a07-106"></span></span>



## <a name="properties"></a><span data-ttu-id="b2a07-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2a07-107">Properties</span></span>
| <span data-ttu-id="b2a07-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b2a07-108">Property</span></span>     | <span data-ttu-id="b2a07-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2a07-109">Type</span></span>   |<span data-ttu-id="b2a07-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2a07-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b2a07-111">networkType</span><span class="sxs-lookup"><span data-stu-id="b2a07-111">networkType</span></span>|<span data-ttu-id="b2a07-112">String</span><span class="sxs-lookup"><span data-stu-id="b2a07-112">String</span></span>|<span data-ttu-id="b2a07-113">Proporciona el tipo de la red.</span><span class="sxs-lookup"><span data-stu-id="b2a07-113">Provides the type of the network.</span></span> <span data-ttu-id="b2a07-114">Los valores posibles son `intranet`, `extranet`, `namedNetwork`, y `trusted`.</span><span class="sxs-lookup"><span data-stu-id="b2a07-114">Possible values are `intranet`, `extranet`, `namedNetwork`, and `trusted`.</span></span>|
|<span data-ttu-id="b2a07-115">networkName</span><span class="sxs-lookup"><span data-stu-id="b2a07-115">networkName</span></span>|<span data-ttu-id="b2a07-116">String</span><span class="sxs-lookup"><span data-stu-id="b2a07-116">String</span></span>|<span data-ttu-id="b2a07-117">Nombre de la red.</span><span class="sxs-lookup"><span data-stu-id="b2a07-117">Name of the network.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="b2a07-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b2a07-118">JSON representation</span></span>

<span data-ttu-id="b2a07-119">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b2a07-119">Here is a JSON representation of the resource.</span></span>

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