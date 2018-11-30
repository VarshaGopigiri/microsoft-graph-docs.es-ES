---
title: tipo de recurso office365GroupsActivityStorage
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 23ff4d112373f52c4c19d6631ac89bac22399b29
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089926"
---
# <a name="office365groupsactivitystorage-resource-type"></a><span data-ttu-id="a0512-103">tipo de recurso office365GroupsActivityStorage</span><span class="sxs-lookup"><span data-stu-id="a0512-103">office365GroupsActivityStorage resource type</span></span>

## <a name="properties"></a><span data-ttu-id="a0512-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0512-104">Properties</span></span>

| <span data-ttu-id="a0512-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a0512-105">Property</span></span>                  | <span data-ttu-id="a0512-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0512-106">Type</span></span>   | <span data-ttu-id="a0512-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0512-107">Description</span></span>                              |
| :------------------------ | :----- | ---------------------------------------- |
| <span data-ttu-id="a0512-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="a0512-108">reportRefreshDate</span></span>         | <span data-ttu-id="a0512-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="a0512-109">Date</span></span>   | <span data-ttu-id="a0512-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="a0512-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="a0512-111">mailboxStorageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="a0512-111">mailboxStorageUsedInBytes</span></span> | <span data-ttu-id="a0512-112">Int64</span><span class="sxs-lookup"><span data-stu-id="a0512-112">Int64</span></span>  | <span data-ttu-id="a0512-113">El almacenamiento usado en el buzón de correo de grupo.</span><span class="sxs-lookup"><span data-stu-id="a0512-113">The storage used in group mailbox.</span></span>       |
| <span data-ttu-id="a0512-114">siteStorageUsedInBytes</span><span class="sxs-lookup"><span data-stu-id="a0512-114">siteStorageUsedInBytes</span></span>    | <span data-ttu-id="a0512-115">Int64</span><span class="sxs-lookup"><span data-stu-id="a0512-115">Int64</span></span>  | <span data-ttu-id="a0512-116">El almacenamiento utilizado en la biblioteca de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="a0512-116">The storage used in SharePoint document library.</span></span> |
| <span data-ttu-id="a0512-117">reportDate</span><span class="sxs-lookup"><span data-stu-id="a0512-117">reportDate</span></span>                | <span data-ttu-id="a0512-118">Fecha</span><span class="sxs-lookup"><span data-stu-id="a0512-118">Date</span></span>   | <span data-ttu-id="a0512-119">La fecha de instantánea para Exchange y SharePoint utiliza almacenamiento de información.</span><span class="sxs-lookup"><span data-stu-id="a0512-119">The snapshot date for Exchange and SharePoint used storage.</span></span> |
| <span data-ttu-id="a0512-120">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="a0512-120">reportPeriod</span></span>              | <span data-ttu-id="a0512-121">String</span><span class="sxs-lookup"><span data-stu-id="a0512-121">String</span></span> | <span data-ttu-id="a0512-122">El número de días que cubre el informe.</span><span class="sxs-lookup"><span data-stu-id="a0512-122">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="a0512-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a0512-123">JSON representation</span></span>

<span data-ttu-id="a0512-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a0512-124">The following is a JSON representation of the resource.</span></span>

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
