---
title: tipo de recurso office365ActivationsUserCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: f57393a538631664be8845fdaeda9f35d07c986f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27849311"
---
# <a name="office365activationsusercounts-resource-type"></a><span data-ttu-id="bf7ef-103">tipo de recurso office365ActivationsUserCounts</span><span class="sxs-lookup"><span data-stu-id="bf7ef-103">office365ActivationsUserCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="bf7ef-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf7ef-104">Properties</span></span>

| <span data-ttu-id="bf7ef-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bf7ef-105">Property</span></span>                 | <span data-ttu-id="bf7ef-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf7ef-106">Type</span></span>   | <span data-ttu-id="bf7ef-107">Description</span><span class="sxs-lookup"><span data-stu-id="bf7ef-107">Description</span></span>                              |
| :----------------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="bf7ef-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="bf7ef-108">reportRefreshDate</span></span>        | <span data-ttu-id="bf7ef-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="bf7ef-109">Date</span></span>   | <span data-ttu-id="bf7ef-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="bf7ef-111">ProductType ofrece</span><span class="sxs-lookup"><span data-stu-id="bf7ef-111">productType</span></span>              | <span data-ttu-id="bf7ef-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="bf7ef-112">String</span></span> | <span data-ttu-id="bf7ef-113">El tipo de producto, como "Office 365 ProPlus", "Cliente del proyecto" o "Visio Pro para Office 365".</span><span class="sxs-lookup"><span data-stu-id="bf7ef-113">The product type such as "Office 365 ProPlus", "Project Client", or "Visio Pro for Office 365".</span></span> |
| <span data-ttu-id="bf7ef-114">asignado</span><span class="sxs-lookup"><span data-stu-id="bf7ef-114">assigned</span></span>                 | <span data-ttu-id="bf7ef-115">Int64</span><span class="sxs-lookup"><span data-stu-id="bf7ef-115">Int64</span></span>  | <span data-ttu-id="bf7ef-116">El número de usuarios se han asignado para la licencia del producto.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-116">The number of users have been assigned for the product license.</span></span> |
| <span data-ttu-id="bf7ef-117">activado</span><span class="sxs-lookup"><span data-stu-id="bf7ef-117">activated</span></span>                | <span data-ttu-id="bf7ef-118">Int64</span><span class="sxs-lookup"><span data-stu-id="bf7ef-118">Int64</span></span>  | <span data-ttu-id="bf7ef-119">El número de usuarios que ha activado el producto.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-119">The number of users who have activated the product.</span></span> |
| <span data-ttu-id="bf7ef-120">sharedComputerActivation</span><span class="sxs-lookup"><span data-stu-id="bf7ef-120">sharedComputerActivation</span></span> | <span data-ttu-id="bf7ef-121">Int64</span><span class="sxs-lookup"><span data-stu-id="bf7ef-121">Int64</span></span>  | <span data-ttu-id="bf7ef-122">El número de usuarios que han usado el producto en un equipo compartido.</span><span class="sxs-lookup"><span data-stu-id="bf7ef-122">The number of users who have used the product on a shared computer.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="bf7ef-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bf7ef-123">JSON representation</span></span>

<span data-ttu-id="bf7ef-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="bf7ef-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365ActivationsUserCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "productType": "String", 
  "assigned": 1024, 
  "activated": 1024,
  "sharedComputerActivation": 1024
}
```
