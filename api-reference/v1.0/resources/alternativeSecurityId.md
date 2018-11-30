---
title: Tipo de recurso alternativeSecurityId
description: Solo para uso interno.
ms.openlocfilehash: 9d941469da133d9a3e7149dfca55c813f60b3ce8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028615"
---
# <a name="alternativesecurityid-resource-type"></a><span data-ttu-id="2c517-103">Tipo de recurso alternativeSecurityId</span><span class="sxs-lookup"><span data-stu-id="2c517-103">alternativeSecurityId resource type</span></span>

<span data-ttu-id="2c517-104">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="2c517-104">For internal use only.</span></span>

## <a name="json-representation"></a><span data-ttu-id="2c517-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2c517-105">JSON representation</span></span>

<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.alternativeSecurityId"
}-->

```json
{
  "type": 12345,
  "identityProvider": "string",
  "key": {"@odata.type": "Edm.Binary"}
}
```

## <a name="properties"></a><span data-ttu-id="2c517-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2c517-106">Properties</span></span>
| <span data-ttu-id="2c517-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2c517-107">Property</span></span>         | <span data-ttu-id="2c517-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2c517-108">Type</span></span>       | <span data-ttu-id="2c517-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2c517-109">Description</span></span>
|:-----------------|:-----------|:---------------------
| <span data-ttu-id="2c517-110">type</span><span class="sxs-lookup"><span data-stu-id="2c517-110">type</span></span>             | <span data-ttu-id="2c517-111">Int32</span><span class="sxs-lookup"><span data-stu-id="2c517-111">Int32</span></span>      | <span data-ttu-id="2c517-112">Sólo para uso interno</span><span class="sxs-lookup"><span data-stu-id="2c517-112">For internal use only</span></span>
| <span data-ttu-id="2c517-113">identityProvider</span><span class="sxs-lookup"><span data-stu-id="2c517-113">identityProvider</span></span> | <span data-ttu-id="2c517-114">string</span><span class="sxs-lookup"><span data-stu-id="2c517-114">string</span></span>     | <span data-ttu-id="2c517-115">Sólo para uso interno</span><span class="sxs-lookup"><span data-stu-id="2c517-115">For internal use only</span></span>
| <span data-ttu-id="2c517-116">Key</span><span class="sxs-lookup"><span data-stu-id="2c517-116">key</span></span>              | <span data-ttu-id="2c517-117">Edm.Binary</span><span class="sxs-lookup"><span data-stu-id="2c517-117">Edm.Binary</span></span> | <span data-ttu-id="2c517-118">Sólo para uso interno</span><span class="sxs-lookup"><span data-stu-id="2c517-118">For internal use only</span></span>
