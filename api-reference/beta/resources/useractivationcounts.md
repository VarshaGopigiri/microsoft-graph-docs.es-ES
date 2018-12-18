---
title: tipo de recurso userActivationCounts
description: La siguiente es una representación JSON del recurso
author: dkershaw10
ms.openlocfilehash: 396f6182d000df6d701e8c0cbad3dd02a258c4c0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27322921"
---
# <a name="useractivationcounts-resource-type"></a><span data-ttu-id="b9e93-103">tipo de recurso userActivationCounts</span><span class="sxs-lookup"><span data-stu-id="b9e93-103">userActivationCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="b9e93-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b9e93-104">Properties</span></span>

| <span data-ttu-id="b9e93-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b9e93-105">Property</span></span>          | <span data-ttu-id="b9e93-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="b9e93-106">Type</span></span>   | <span data-ttu-id="b9e93-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b9e93-107">Description</span></span>                              |
| :---------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="b9e93-108">ProductType ofrece</span><span class="sxs-lookup"><span data-stu-id="b9e93-108">productType</span></span>       | <span data-ttu-id="b9e93-109">String</span><span class="sxs-lookup"><span data-stu-id="b9e93-109">String</span></span> | <span data-ttu-id="b9e93-110">El tipo de producto, como "Office 365 ProPlus", "Cliente del proyecto" o "Visio Pro para Office 365".</span><span class="sxs-lookup"><span data-stu-id="b9e93-110">The product type, such as "Office 365 ProPlus", "Project Client", or "Visio Pro for Office 365".</span></span> |
| <span data-ttu-id="b9e93-111">lastActivatedDate</span><span class="sxs-lookup"><span data-stu-id="b9e93-111">lastActivatedDate</span></span> | <span data-ttu-id="b9e93-112">Date</span><span class="sxs-lookup"><span data-stu-id="b9e93-112">Date</span></span>   | <span data-ttu-id="b9e93-113">La fecha de la última activación.</span><span class="sxs-lookup"><span data-stu-id="b9e93-113">The date of the latest activation.</span></span>       |
| <span data-ttu-id="b9e93-114">Windows</span><span class="sxs-lookup"><span data-stu-id="b9e93-114">windows</span></span>           | <span data-ttu-id="b9e93-115">Int64</span><span class="sxs-lookup"><span data-stu-id="b9e93-115">Int64</span></span>  | <span data-ttu-id="b9e93-116">El número de activación en Windows.</span><span class="sxs-lookup"><span data-stu-id="b9e93-116">The activation count on Windows.</span></span> <span data-ttu-id="b9e93-117">Este número incluye cada activación en cualquier equipo de Windows.</span><span class="sxs-lookup"><span data-stu-id="b9e93-117">This number includes every activation on any Windows computer.</span></span> |
| <span data-ttu-id="b9e93-118">mac</span><span class="sxs-lookup"><span data-stu-id="b9e93-118">mac</span></span>               | <span data-ttu-id="b9e93-119">Int64</span><span class="sxs-lookup"><span data-stu-id="b9e93-119">Int64</span></span>  | <span data-ttu-id="b9e93-120">El número de activación en Mac OS.</span><span class="sxs-lookup"><span data-stu-id="b9e93-120">The activation count on Mac OS.</span></span>          |
| <span data-ttu-id="b9e93-121">windows10Mobile</span><span class="sxs-lookup"><span data-stu-id="b9e93-121">windows10Mobile</span></span>   | <span data-ttu-id="b9e93-122">Int64</span><span class="sxs-lookup"><span data-stu-id="b9e93-122">Int64</span></span>  | <span data-ttu-id="b9e93-123">La activación contar en 10 de Windows mobile.</span><span class="sxs-lookup"><span data-stu-id="b9e93-123">The activation count on Windows 10 mobile.</span></span> |
| <span data-ttu-id="b9e93-124">IOS</span><span class="sxs-lookup"><span data-stu-id="b9e93-124">ios</span></span>               | <span data-ttu-id="b9e93-125">Int64</span><span class="sxs-lookup"><span data-stu-id="b9e93-125">Int64</span></span>  | <span data-ttu-id="b9e93-126">El número de activación en iOS.</span><span class="sxs-lookup"><span data-stu-id="b9e93-126">The activation count on iOS.</span></span>             |
| <span data-ttu-id="b9e93-127">Android</span><span class="sxs-lookup"><span data-stu-id="b9e93-127">android</span></span>           | <span data-ttu-id="b9e93-128">Int64</span><span class="sxs-lookup"><span data-stu-id="b9e93-128">Int64</span></span>  | <span data-ttu-id="b9e93-129">El número de activación en un dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="b9e93-129">The activation count on an Android device.</span></span>  |
| <span data-ttu-id="b9e93-130">activatedOnSharedComputer</span><span class="sxs-lookup"><span data-stu-id="b9e93-130">activatedOnSharedComputer</span></span>   | <span data-ttu-id="b9e93-131">Boolean</span><span class="sxs-lookup"><span data-stu-id="b9e93-131">Boolean</span></span> | <span data-ttu-id="b9e93-132">True si el usuario utiliza el producto en un equipo compartido antes.</span><span class="sxs-lookup"><span data-stu-id="b9e93-132">True if the user used the product on a shared computer before.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="b9e93-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b9e93-133">JSON representation</span></span>

<span data-ttu-id="b9e93-134">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b9e93-134">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.userActivationCounts"
} -->

```json
{
  "productType": "String", 
  "lastActivatedDate": "Date", 
  "windows": 1024, 
  "mac": 1024, 
  "windows10Mobile": 1024, 
  "ios": 1024, 
  "android": 1024,
  "activatedOnSharedComputer": true 
}
```
