---
title: Tipo de recurso alternativeSecurityId
description: Solo para uso interno.
localization_priority: Normal
ms.openlocfilehash: 23ef74085a4a3cc383f0854e9139c9a0b63e3d40
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853805"
---
# <a name="alternativesecurityid-resource-type"></a><span data-ttu-id="1ddfa-103">Tipo de recurso alternativeSecurityId</span><span class="sxs-lookup"><span data-stu-id="1ddfa-103">alternativeSecurityId resource type</span></span>

<span data-ttu-id="1ddfa-104">Solo para uso interno.</span><span class="sxs-lookup"><span data-stu-id="1ddfa-104">For internal use only.</span></span>

## <a name="json-representation"></a><span data-ttu-id="1ddfa-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1ddfa-105">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="1ddfa-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1ddfa-106">Properties</span></span>
| <span data-ttu-id="1ddfa-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1ddfa-107">Property</span></span>         | <span data-ttu-id="1ddfa-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ddfa-108">Type</span></span>       | <span data-ttu-id="1ddfa-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ddfa-109">Description</span></span>
|:-----------------|:-----------|:---------------------
| <span data-ttu-id="1ddfa-110">type</span><span class="sxs-lookup"><span data-stu-id="1ddfa-110">type</span></span>             | <span data-ttu-id="1ddfa-111">Int32</span><span class="sxs-lookup"><span data-stu-id="1ddfa-111">Int32</span></span>      | <span data-ttu-id="1ddfa-112">Sólo para uso interno</span><span class="sxs-lookup"><span data-stu-id="1ddfa-112">For internal use only</span></span>
| <span data-ttu-id="1ddfa-113">identityProvider</span><span class="sxs-lookup"><span data-stu-id="1ddfa-113">identityProvider</span></span> | <span data-ttu-id="1ddfa-114">string</span><span class="sxs-lookup"><span data-stu-id="1ddfa-114">string</span></span>     | <span data-ttu-id="1ddfa-115">Sólo para uso interno</span><span class="sxs-lookup"><span data-stu-id="1ddfa-115">For internal use only</span></span>
| <span data-ttu-id="1ddfa-116">Key</span><span class="sxs-lookup"><span data-stu-id="1ddfa-116">key</span></span>              | <span data-ttu-id="1ddfa-117">Edm.Binary</span><span class="sxs-lookup"><span data-stu-id="1ddfa-117">Edm.Binary</span></span> | <span data-ttu-id="1ddfa-118">Sólo para uso interno</span><span class="sxs-lookup"><span data-stu-id="1ddfa-118">For internal use only</span></span>
