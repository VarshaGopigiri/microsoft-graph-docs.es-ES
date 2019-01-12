---
title: tipo de recurso office365ActivationCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.prod: reports
ms.openlocfilehash: 4787672df6462e8d1f343e4dace43ede7c79ff37
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991184"
---
# <a name="office365activationcounts-resource-type"></a><span data-ttu-id="55b21-103">tipo de recurso office365ActivationCounts</span><span class="sxs-lookup"><span data-stu-id="55b21-103">office365ActivationCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="55b21-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="55b21-104">Properties</span></span>

| <span data-ttu-id="55b21-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="55b21-105">Property</span></span>          | <span data-ttu-id="55b21-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="55b21-106">Type</span></span>   | <span data-ttu-id="55b21-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="55b21-107">Description</span></span>                              |
| :---------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="55b21-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="55b21-108">reportRefreshDate</span></span> | <span data-ttu-id="55b21-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="55b21-109">Date</span></span>   | <span data-ttu-id="55b21-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="55b21-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="55b21-111">ProductType ofrece</span><span class="sxs-lookup"><span data-stu-id="55b21-111">productType</span></span>       | <span data-ttu-id="55b21-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="55b21-112">String</span></span> | <span data-ttu-id="55b21-113">El tipo de producto, como "Office 365 ProPlus", "Cliente del proyecto" o "Visio Pro para Office 365".</span><span class="sxs-lookup"><span data-stu-id="55b21-113">The product type, such as "Office 365 ProPlus", "Project Client", or "Visio Pro for Office 365".</span></span> |
| <span data-ttu-id="55b21-114">Windows</span><span class="sxs-lookup"><span data-stu-id="55b21-114">windows</span></span>           | <span data-ttu-id="55b21-115">Int64</span><span class="sxs-lookup"><span data-stu-id="55b21-115">Int64</span></span>  | <span data-ttu-id="55b21-116">El número de activación en Windows.</span><span class="sxs-lookup"><span data-stu-id="55b21-116">The activation count on Windows.</span></span> <span data-ttu-id="55b21-117">Este número incluye cada activación en cualquier equipo de Windows.</span><span class="sxs-lookup"><span data-stu-id="55b21-117">This number includes every activation on any Windows computer.</span></span> |
| <span data-ttu-id="55b21-118">mac</span><span class="sxs-lookup"><span data-stu-id="55b21-118">mac</span></span>               | <span data-ttu-id="55b21-119">Int64</span><span class="sxs-lookup"><span data-stu-id="55b21-119">Int64</span></span>  | <span data-ttu-id="55b21-120">El número de activación en Mac OS.</span><span class="sxs-lookup"><span data-stu-id="55b21-120">The activation count on Mac OS.</span></span>          |
| <span data-ttu-id="55b21-121">Android</span><span class="sxs-lookup"><span data-stu-id="55b21-121">android</span></span>           | <span data-ttu-id="55b21-122">Int64</span><span class="sxs-lookup"><span data-stu-id="55b21-122">Int64</span></span>  | <span data-ttu-id="55b21-123">El número de activación en un dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="55b21-123">The activation count on an Android device.</span></span>  |
| <span data-ttu-id="55b21-124">IOS</span><span class="sxs-lookup"><span data-stu-id="55b21-124">ios</span></span>               | <span data-ttu-id="55b21-125">Int64</span><span class="sxs-lookup"><span data-stu-id="55b21-125">Int64</span></span>  | <span data-ttu-id="55b21-126">El número de activación en iOS.</span><span class="sxs-lookup"><span data-stu-id="55b21-126">The activation count on iOS.</span></span>             |
| <span data-ttu-id="55b21-127">windows10Mobile</span><span class="sxs-lookup"><span data-stu-id="55b21-127">windows10Mobile</span></span>   | <span data-ttu-id="55b21-128">Int64</span><span class="sxs-lookup"><span data-stu-id="55b21-128">Int64</span></span>  | <span data-ttu-id="55b21-129">La activación contar en 10 de Windows mobile.</span><span class="sxs-lookup"><span data-stu-id="55b21-129">The activation count on Windows 10 mobile.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="55b21-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="55b21-130">JSON representation</span></span>

<span data-ttu-id="55b21-131">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="55b21-131">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365ActivationCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "productType": "String", 
  "windows": 1024, 
  "mac": 1024, 
  "android": 1024, 
  "ios": 1024, 
  "windows10Mobile": 1024
}
```
