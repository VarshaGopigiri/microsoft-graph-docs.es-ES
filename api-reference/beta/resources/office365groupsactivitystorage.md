---
title: tipo de recurso office365GroupsActivityStorage
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 9824d3d172a8578f8a25a049c2d0d3b407bbc47e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862254"
---
# <a name="office365groupsactivitystorage-resource-type"></a><span data-ttu-id="962fc-103">tipo de recurso office365GroupsActivityStorage</span><span class="sxs-lookup"><span data-stu-id="962fc-103">office365GroupsActivityStorage resource type</span></span>

## <a name="properties"></a><span data-ttu-id="962fc-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="962fc-104">Properties</span></span>

| <span data-ttu-id="962fc-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="962fc-105">Property</span></span>                  | <span data-ttu-id="962fc-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="962fc-106">Type</span></span>   | <span data-ttu-id="962fc-107">Description</span><span class="sxs-lookup"><span data-stu-id="962fc-107">Description</span></span>                              |
| :------------------------ | :----- | ---------------------------------------- |
| <span data-ttu-id="962fc-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="962fc-108">reportRefreshDate</span></span>         | <span data-ttu-id="962fc-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="962fc-109">Date</span></span>   | <span data-ttu-id="962fc-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="962fc-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="962fc-111">mailboxStorageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="962fc-111">mailboxStorageUsedInBytes</span></span> | <span data-ttu-id="962fc-112">Int64</span><span class="sxs-lookup"><span data-stu-id="962fc-112">Int64</span></span>  | <span data-ttu-id="962fc-113">El almacenamiento usado en el buzón de correo de grupo.</span><span class="sxs-lookup"><span data-stu-id="962fc-113">The storage used in group mailbox.</span></span>       |
| <span data-ttu-id="962fc-114">siteStorageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="962fc-114">siteStorageUsedInBytes</span></span>    | <span data-ttu-id="962fc-115">Int64</span><span class="sxs-lookup"><span data-stu-id="962fc-115">Int64</span></span>  | <span data-ttu-id="962fc-116">El almacenamiento utilizado en la biblioteca de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="962fc-116">The storage used in SharePoint document library.</span></span> |
| <span data-ttu-id="962fc-117">reportDate</span><span class="sxs-lookup"><span data-stu-id="962fc-117">reportDate</span></span>                | <span data-ttu-id="962fc-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="962fc-118">Date</span></span>   | <span data-ttu-id="962fc-119">La fecha de instantánea para Exchange y SharePoint utiliza almacenamiento de información.</span><span class="sxs-lookup"><span data-stu-id="962fc-119">The snapshot date for Exchange and SharePoint used storage.</span></span> |
| <span data-ttu-id="962fc-120">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="962fc-120">reportPeriod</span></span>              | <span data-ttu-id="962fc-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="962fc-121">String</span></span> | <span data-ttu-id="962fc-122">El número de días que cubre el informe.</span><span class="sxs-lookup"><span data-stu-id="962fc-122">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="962fc-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="962fc-123">JSON representation</span></span>

<span data-ttu-id="962fc-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="962fc-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365GroupsActivityStorage"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "mailboxStorageUsedInBytes": 1024, 
  "siteStorageUsedInBytes": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
