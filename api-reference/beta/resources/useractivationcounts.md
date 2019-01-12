---
title: tipo de recurso userActivationCounts
description: La siguiente es una representación JSON del recurso
author: dkershaw10
localization_priority: Normal
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 535355d6be3f6b617d7eb293890aa05a517cfc3b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980352"
---
# <a name="useractivationcounts-resource-type"></a><span data-ttu-id="8fe9d-103">tipo de recurso userActivationCounts</span><span class="sxs-lookup"><span data-stu-id="8fe9d-103">userActivationCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="8fe9d-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8fe9d-104">Properties</span></span>

| <span data-ttu-id="8fe9d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8fe9d-105">Property</span></span>          | <span data-ttu-id="8fe9d-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fe9d-106">Type</span></span>   | <span data-ttu-id="8fe9d-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fe9d-107">Description</span></span>                              |
| :---------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="8fe9d-108">ProductType ofrece</span><span class="sxs-lookup"><span data-stu-id="8fe9d-108">productType</span></span>       | <span data-ttu-id="8fe9d-109">Cadena</span><span class="sxs-lookup"><span data-stu-id="8fe9d-109">String</span></span> | <span data-ttu-id="8fe9d-110">El tipo de producto, como "Office 365 ProPlus", "Cliente del proyecto" o "Visio Pro para Office 365".</span><span class="sxs-lookup"><span data-stu-id="8fe9d-110">The product type, such as "Office 365 ProPlus", "Project Client", or "Visio Pro for Office 365".</span></span> |
| <span data-ttu-id="8fe9d-111">lastActivatedDate</span><span class="sxs-lookup"><span data-stu-id="8fe9d-111">lastActivatedDate</span></span> | <span data-ttu-id="8fe9d-112">Fecha</span><span class="sxs-lookup"><span data-stu-id="8fe9d-112">Date</span></span>   | <span data-ttu-id="8fe9d-113">La fecha de la última activación.</span><span class="sxs-lookup"><span data-stu-id="8fe9d-113">The date of the latest activation.</span></span>       |
| <span data-ttu-id="8fe9d-114">Windows</span><span class="sxs-lookup"><span data-stu-id="8fe9d-114">windows</span></span>           | <span data-ttu-id="8fe9d-115">Int64</span><span class="sxs-lookup"><span data-stu-id="8fe9d-115">Int64</span></span>  | <span data-ttu-id="8fe9d-116">El número de activación en Windows.</span><span class="sxs-lookup"><span data-stu-id="8fe9d-116">The activation count on Windows.</span></span> <span data-ttu-id="8fe9d-117">Este número incluye cada activación en cualquier equipo de Windows.</span><span class="sxs-lookup"><span data-stu-id="8fe9d-117">This number includes every activation on any Windows computer.</span></span> |
| <span data-ttu-id="8fe9d-118">mac</span><span class="sxs-lookup"><span data-stu-id="8fe9d-118">mac</span></span>               | <span data-ttu-id="8fe9d-119">Int64</span><span class="sxs-lookup"><span data-stu-id="8fe9d-119">Int64</span></span>  | <span data-ttu-id="8fe9d-120">El número de activación en Mac OS.</span><span class="sxs-lookup"><span data-stu-id="8fe9d-120">The activation count on Mac OS.</span></span>          |
| <span data-ttu-id="8fe9d-121">windows10Mobile</span><span class="sxs-lookup"><span data-stu-id="8fe9d-121">windows10Mobile</span></span>   | <span data-ttu-id="8fe9d-122">Int64</span><span class="sxs-lookup"><span data-stu-id="8fe9d-122">Int64</span></span>  | <span data-ttu-id="8fe9d-123">La activación contar en 10 de Windows mobile.</span><span class="sxs-lookup"><span data-stu-id="8fe9d-123">The activation count on Windows 10 mobile.</span></span> |
| <span data-ttu-id="8fe9d-124">IOS</span><span class="sxs-lookup"><span data-stu-id="8fe9d-124">ios</span></span>               | <span data-ttu-id="8fe9d-125">Int64</span><span class="sxs-lookup"><span data-stu-id="8fe9d-125">Int64</span></span>  | <span data-ttu-id="8fe9d-126">El número de activación en iOS.</span><span class="sxs-lookup"><span data-stu-id="8fe9d-126">The activation count on iOS.</span></span>             |
| <span data-ttu-id="8fe9d-127">Android</span><span class="sxs-lookup"><span data-stu-id="8fe9d-127">android</span></span>           | <span data-ttu-id="8fe9d-128">Int64</span><span class="sxs-lookup"><span data-stu-id="8fe9d-128">Int64</span></span>  | <span data-ttu-id="8fe9d-129">El número de activación en un dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="8fe9d-129">The activation count on an Android device.</span></span>  |
| <span data-ttu-id="8fe9d-130">activatedOnSharedComputer</span><span class="sxs-lookup"><span data-stu-id="8fe9d-130">activatedOnSharedComputer</span></span>   | <span data-ttu-id="8fe9d-131">Booleano</span><span class="sxs-lookup"><span data-stu-id="8fe9d-131">Boolean</span></span> | <span data-ttu-id="8fe9d-132">True si el usuario utiliza el producto en un equipo compartido antes.</span><span class="sxs-lookup"><span data-stu-id="8fe9d-132">True if the user used the product on a shared computer before.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="8fe9d-133">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8fe9d-133">JSON representation</span></span>

<span data-ttu-id="8fe9d-134">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8fe9d-134">The following is a JSON representation of the resource.</span></span>

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
