---
title: tipo de recurso emailActivityUserDetail
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 16512c3a8a4dab62d4a71406d6c33d52a5a9bc08
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818007"
---
# <a name="emailactivityuserdetail-resource-type"></a><span data-ttu-id="8bf91-103">tipo de recurso emailActivityUserDetail</span><span class="sxs-lookup"><span data-stu-id="8bf91-103">emailActivityUserDetail resource type</span></span>

## <a name="properties"></a><span data-ttu-id="8bf91-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bf91-104">Properties</span></span>

| <span data-ttu-id="8bf91-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8bf91-105">Property</span></span>          | <span data-ttu-id="8bf91-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="8bf91-106">Type</span></span>              |
| :---------------- | :---------------- |
| <span data-ttu-id="8bf91-107">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="8bf91-107">reportRefreshDate</span></span> | <span data-ttu-id="8bf91-108">Fecha</span><span class="sxs-lookup"><span data-stu-id="8bf91-108">Date</span></span>              |
| <span data-ttu-id="8bf91-109">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="8bf91-109">userPrincipalName</span></span> | <span data-ttu-id="8bf91-110">Cadena</span><span class="sxs-lookup"><span data-stu-id="8bf91-110">String</span></span>            |
| <span data-ttu-id="8bf91-111">displayName</span><span class="sxs-lookup"><span data-stu-id="8bf91-111">displayName</span></span>       | <span data-ttu-id="8bf91-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="8bf91-112">String</span></span>            |
| <span data-ttu-id="8bf91-113">isDeleted</span><span class="sxs-lookup"><span data-stu-id="8bf91-113">isDeleted</span></span>         | <span data-ttu-id="8bf91-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="8bf91-114">Boolean</span></span>           |
| <span data-ttu-id="8bf91-115">deletedDate</span><span class="sxs-lookup"><span data-stu-id="8bf91-115">deletedDate</span></span>       | <span data-ttu-id="8bf91-116">Fecha</span><span class="sxs-lookup"><span data-stu-id="8bf91-116">Date</span></span>              |
| <span data-ttu-id="8bf91-117">lastActivityDate</span><span class="sxs-lookup"><span data-stu-id="8bf91-117">lastActivityDate</span></span>  | <span data-ttu-id="8bf91-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="8bf91-118">Date</span></span>              |
| <span data-ttu-id="8bf91-119">sendCount</span><span class="sxs-lookup"><span data-stu-id="8bf91-119">sendCount</span></span>         | <span data-ttu-id="8bf91-120">Int64</span><span class="sxs-lookup"><span data-stu-id="8bf91-120">Int64</span></span>             |
| <span data-ttu-id="8bf91-121">receiveCount</span><span class="sxs-lookup"><span data-stu-id="8bf91-121">receiveCount</span></span>      | <span data-ttu-id="8bf91-122">Int64</span><span class="sxs-lookup"><span data-stu-id="8bf91-122">Int64</span></span>             |
| <span data-ttu-id="8bf91-123">readCount</span><span class="sxs-lookup"><span data-stu-id="8bf91-123">readCount</span></span>         | <span data-ttu-id="8bf91-124">Int64</span><span class="sxs-lookup"><span data-stu-id="8bf91-124">Int64</span></span>             |
| <span data-ttu-id="8bf91-125">assignedProducts</span><span class="sxs-lookup"><span data-stu-id="8bf91-125">assignedProducts</span></span>  | <span data-ttu-id="8bf91-126">Colección String</span><span class="sxs-lookup"><span data-stu-id="8bf91-126">String collection</span></span> |
| <span data-ttu-id="8bf91-127">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="8bf91-127">reportPeriod</span></span>      | <span data-ttu-id="8bf91-128">String</span><span class="sxs-lookup"><span data-stu-id="8bf91-128">String</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="8bf91-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8bf91-129">JSON representation</span></span>

<span data-ttu-id="8bf91-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8bf91-130">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.emailActivityUserDetail"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "userPrincipalName": "String", 
  "displayName": "String", 
  "isDeleted": true, 
  "deletedDate": "Date", 
  "lastActivityDate": "Date", 
  "sendCount": 1024, 
  "receiveCount": 1024, 
  "readCount": 1024, 
  "assignedProducts": ["String"], 
  "reportPeriod": "String"
}
```
