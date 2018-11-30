---
title: tipo de recurso office365ActivationCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: e53a979ac627735ef63a24e1823d83f4c9fe9f7a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089762"
---
# <a name="office365activationcounts-resource-type"></a><span data-ttu-id="212c7-103">tipo de recurso office365ActivationCounts</span><span class="sxs-lookup"><span data-stu-id="212c7-103">office365ActivationCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="212c7-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="212c7-104">Properties</span></span>

| <span data-ttu-id="212c7-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="212c7-105">Property</span></span>          | <span data-ttu-id="212c7-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="212c7-106">Type</span></span>   | <span data-ttu-id="212c7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="212c7-107">Description</span></span>                              |
| :---------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="212c7-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="212c7-108">reportRefreshDate</span></span> | <span data-ttu-id="212c7-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="212c7-109">Date</span></span>   | <span data-ttu-id="212c7-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="212c7-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="212c7-111">ProductType ofrece</span><span class="sxs-lookup"><span data-stu-id="212c7-111">productType</span></span>       | <span data-ttu-id="212c7-112">String</span><span class="sxs-lookup"><span data-stu-id="212c7-112">String</span></span> | <span data-ttu-id="212c7-113">El tipo de producto, como "Office 365 ProPlus", "Cliente del proyecto" o "Visio Pro para Office 365".</span><span class="sxs-lookup"><span data-stu-id="212c7-113">The product type, such as "Office 365 ProPlus", "Project Client", or "Visio Pro for Office 365".</span></span> |
| <span data-ttu-id="212c7-114">Windows</span><span class="sxs-lookup"><span data-stu-id="212c7-114">windows</span></span>           | <span data-ttu-id="212c7-115">Int64</span><span class="sxs-lookup"><span data-stu-id="212c7-115">Int64</span></span>  | <span data-ttu-id="212c7-116">El número de activación en Windows.</span><span class="sxs-lookup"><span data-stu-id="212c7-116">The activation count on Windows.</span></span> <span data-ttu-id="212c7-117">Este número incluye cada activación en cualquier equipo de Windows.</span><span class="sxs-lookup"><span data-stu-id="212c7-117">This number includes every activation on any Windows computer.</span></span> |
| <span data-ttu-id="212c7-118">mac</span><span class="sxs-lookup"><span data-stu-id="212c7-118">mac</span></span>               | <span data-ttu-id="212c7-119">Int64</span><span class="sxs-lookup"><span data-stu-id="212c7-119">Int64</span></span>  | <span data-ttu-id="212c7-120">El número de activación en Mac OS.</span><span class="sxs-lookup"><span data-stu-id="212c7-120">The activation count on Mac OS.</span></span>          |
| <span data-ttu-id="212c7-121">Android</span><span class="sxs-lookup"><span data-stu-id="212c7-121">android</span></span>           | <span data-ttu-id="212c7-122">Int64</span><span class="sxs-lookup"><span data-stu-id="212c7-122">Int64</span></span>  | <span data-ttu-id="212c7-123">El número de activación en un dispositivo Android.</span><span class="sxs-lookup"><span data-stu-id="212c7-123">The activation count on an Android device.</span></span>  |
| <span data-ttu-id="212c7-124">IOS</span><span class="sxs-lookup"><span data-stu-id="212c7-124">ios</span></span>               | <span data-ttu-id="212c7-125">Int64</span><span class="sxs-lookup"><span data-stu-id="212c7-125">Int64</span></span>  | <span data-ttu-id="212c7-126">El número de activación en iOS.</span><span class="sxs-lookup"><span data-stu-id="212c7-126">The activation count on iOS.</span></span>             |
| <span data-ttu-id="212c7-127">windows10Mobile</span><span class="sxs-lookup"><span data-stu-id="212c7-127">windows10Mobile</span></span>   | <span data-ttu-id="212c7-128">Int64</span><span class="sxs-lookup"><span data-stu-id="212c7-128">Int64</span></span>  | <span data-ttu-id="212c7-129">La activación contar en 10 de Windows mobile.</span><span class="sxs-lookup"><span data-stu-id="212c7-129">The activation count on Windows 10 mobile.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="212c7-130">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="212c7-130">JSON representation</span></span>

<span data-ttu-id="212c7-131">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="212c7-131">The following is a JSON representation of the resource.</span></span>

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
