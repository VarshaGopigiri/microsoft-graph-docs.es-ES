---
title: tipo de recurso office365GroupsActivityGroupCounts
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 12dc0121c8f37c694265fce0d6cb5f58e56e0966
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085835"
---
# <a name="office365groupsactivitygroupcounts-resource-type"></a><span data-ttu-id="32a19-103">tipo de recurso office365GroupsActivityGroupCounts</span><span class="sxs-lookup"><span data-stu-id="32a19-103">office365GroupsActivityGroupCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="32a19-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32a19-104">Properties</span></span>

| <span data-ttu-id="32a19-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32a19-105">Property</span></span>          | <span data-ttu-id="32a19-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="32a19-106">Type</span></span>   | <span data-ttu-id="32a19-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="32a19-107">Description</span></span>                              |
| :---------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="32a19-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="32a19-108">reportRefreshDate</span></span> | <span data-ttu-id="32a19-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="32a19-109">Date</span></span>   | <span data-ttu-id="32a19-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="32a19-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="32a19-111">total</span><span class="sxs-lookup"><span data-stu-id="32a19-111">total</span></span>             | <span data-ttu-id="32a19-112">Int64</span><span class="sxs-lookup"><span data-stu-id="32a19-112">Int64</span></span>  | <span data-ttu-id="32a19-113">El número total de grupos.</span><span class="sxs-lookup"><span data-stu-id="32a19-113">The total number of groups.</span></span>              |
| <span data-ttu-id="32a19-114">activo</span><span class="sxs-lookup"><span data-stu-id="32a19-114">active</span></span>            | <span data-ttu-id="32a19-115">Int64</span><span class="sxs-lookup"><span data-stu-id="32a19-115">Int64</span></span>  | <span data-ttu-id="32a19-116">El número de grupos de active.</span><span class="sxs-lookup"><span data-stu-id="32a19-116">The number of active groups.</span></span> <span data-ttu-id="32a19-117">Un grupo se considera activo si se ha producido cualquiera de los siguientes: grupo de correo electrónico del buzón de correo recibido; usuario ve, edita, compartidos o sincronizados los archivos de biblioteca de documentos de SharePoint; usuario ve las páginas de SharePoint; usuario registrado, lea o había gustado los mensajes en grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="32a19-117">A group is considered active if any of the following occurred: group mailbox received email; user viewed, edited, shared, or synced files in SharePoint document library; user viewed SharePoint pages; user posted, read, or liked messages in Yammer groups.</span></span> |
| <span data-ttu-id="32a19-118">reportDate</span><span class="sxs-lookup"><span data-stu-id="32a19-118">reportDate</span></span>        | <span data-ttu-id="32a19-119">Fecha</span><span class="sxs-lookup"><span data-stu-id="32a19-119">Date</span></span>   | <span data-ttu-id="32a19-120">La fecha en la que estaba activo un número de grupos.</span><span class="sxs-lookup"><span data-stu-id="32a19-120">The date on which a number of groups were active.</span></span> |
| <span data-ttu-id="32a19-121">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="32a19-121">reportPeriod</span></span>      | <span data-ttu-id="32a19-122">String</span><span class="sxs-lookup"><span data-stu-id="32a19-122">String</span></span> | <span data-ttu-id="32a19-123">El número de días que cubre el informe.</span><span class="sxs-lookup"><span data-stu-id="32a19-123">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="32a19-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="32a19-124">JSON representation</span></span>

<span data-ttu-id="32a19-125">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="32a19-125">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365GroupsActivityGroupCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "total": 1024, 
  "active": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
