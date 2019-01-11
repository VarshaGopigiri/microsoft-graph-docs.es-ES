---
title: tipo de recurso userActivationCounts
description: La siguiente es una representación JSON del recurso
author: dkershaw10
localization_priority: Normal
ms.openlocfilehash: cae194545f13d312ee78b572659017752e43a6a6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27845293"
---
# <a name="useractivationcounts-resource-type"></a><span data-ttu-id="1583c-103">tipo de recurso userActivationCounts</span><span class="sxs-lookup"><span data-stu-id="1583c-103">userActivationCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="1583c-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1583c-104">Properties</span></span>

| <span data-ttu-id="1583c-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1583c-105">Property</span></span>          | <span data-ttu-id="1583c-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="1583c-106">Type</span></span>   | <span data-ttu-id="1583c-107">Description</span><span class="sxs-lookup"><span data-stu-id="1583c-107">Description</span></span>                              |
| :---------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="1583c-108">ProductType ofrece</span><span class="sxs-lookup"><span data-stu-id="1583c-108">productType</span></span>       | <span data-ttu-id="1583c-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="1583c-109">String</span></span> | <span data-ttu-id="1583c-110">El tipo de producto, como "Office 365 ProPlus", "Cliente del proyecto" o "Visio Pro para Office 365".</span><span class="sxs-lookup"><span data-stu-id="1583c-110">The product type, such as "Office 365 ProPlus", "Project Client", or "Visio Pro for Office 365".</span></span> |
| <span data-ttu-id="1583c-111">lastActivatedDate</span><span class="sxs-lookup"><span data-stu-id="1583c-111">lastActivatedDate</span></span> | <span data-ttu-id="1583c-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="1583c-112">Date</span></span>   | <span data-ttu-id="1583c-113">La fecha de la última activación.</span><span class="sxs-lookup"><span data-stu-id="1583c-113">The date of the latest activation.</span></span>       |
| <span data-ttu-id="1583c-114">Windows</span><span class="sxs-lookup"><span data-stu-id="1583c-114">windows</span></span>           | <span data-ttu-id="1583c-115">Int64</span><span class="sxs-lookup"><span data-stu-id="1583c-115">Int64</span></span>  | <span data-ttu-id="1583c-116">El número de activación en Windows.</span><span class="sxs-lookup"><span data-stu-id="1583c-116">The activation count on Windows.</span></span> <span data-ttu-id="1583c-117">Este número incluye cada activación en cualquier equipo de Windows.</span><span class="sxs-lookup"><span data-stu-id="1583c-117">This number includes every activation on any Windows computer.</span></span> |
| <span data-ttu-id="1583c-118">mac</span><span class="sxs-lookup"><span data-stu-id="1583c-118">mac</span></span>               | <span data-ttu-id="1583c-119">Int64</span><span class="sxs-lookup"><span data-stu-id="1583c-119">Int64</span></span>  | <span data-ttu-id="1583c-120">El número de activación en Mac OS.</span><span class="sxs-lookup"><span data-stu-id="1583c-120">The activation count on Mac OS.</span></span>          |
| <span data-ttu-id="1583c-121">windows10Mobile</span><span class="sxs-lookup"><span data-stu-id="1583c-121">windows10Mobile</span></span>   | <span data-ttu-id="1583c-122">Int64</span><span class="sxs-lookup"><span data-stu-id="1583c-122">Int64</span></span>  | <span data-ttu-id="1583c-123">La activación contar en 10 de Windows mobile.</span><span class="sxs-lookup"><span data-stu-id="1583c-123">The activation count on Windows 10 mobile.</span></span> |
| <span data-ttu-id="1583c-124">IOS</span><span class="sxs-lookup"><span data-stu-id="1583c-124">ios</span></span>               | <span data-ttu-id="1583c-125">Int64</span><span class="sxs-lookup"><span data-stu-id="1583c-125">Int64</span></span>  | <span data-ttu-id="1583c-126">El número de activación en iOS.</span><span class="sxs-lookup"><span data-stu-id="1583c-126">The activation count on iOS.</span></span>             |
| <span data-ttu-id="1583c-127">Android</span><span class="sxs-lookup"><span data-stu-id="1583c-127">android</span></span>           | <span data-ttu-id="1583c-128">Int64</span><span class="sxs-lookup"><span data-stu-id="1583c-128">Int64</span></span>  | <span data-ttu-id="1583c-129">El número de activación en un dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="1583c-129">The activation count on an Android device.</span></span>  |
| <span data-ttu-id="1583c-130">activatedOnSharedComputer</span><span class="sxs-lookup"><span data-stu-id="1583c-130">activatedOnSharedComputer</span></span>   | <span data-ttu-id="1583c-131">Booleano</span><span class="sxs-lookup"><span data-stu-id="1583c-131">Boolean</span></span> | <span data-ttu-id="1583c-132">True si el usuario utiliza el producto en un equipo compartido antes.</span><span class="sxs-lookup"><span data-stu-id="1583c-132">True if the user used the product on a shared computer before.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="1583c-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1583c-133">JSON representation</span></span>

<span data-ttu-id="1583c-134">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="1583c-134">The following is a JSON representation of the resource.</span></span>

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
