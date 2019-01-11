---
title: Tipo de recurso assignedLicense
description: Representa una licencia asignada a un usuario. La propiedad **assignedLicenses** de la entidad user es una colección de **assignedLicense**.
localization_priority: Normal
ms.openlocfilehash: dfb93075fe62a0cfb479e12554e9078e876c4529
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27853788"
---
# <a name="assignedlicense-resource-type"></a><span data-ttu-id="ebd9d-104">Tipo de recurso assignedLicense</span><span class="sxs-lookup"><span data-stu-id="ebd9d-104">assignedLicense resource type</span></span>

> <span data-ttu-id="ebd9d-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ebd9d-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ebd9d-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ebd9d-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ebd9d-p103">Representa una licencia asignada a un usuario. La propiedad **assignedLicenses** de la entidad [user](user.md) es una colección de **assignedLicense**.</span><span class="sxs-lookup"><span data-stu-id="ebd9d-p103">Represents a license assigned to a user. The **assignedLicenses** property of the [user](user.md) entity is a collection of **assignedLicense**.</span></span>

## <a name="properties"></a><span data-ttu-id="ebd9d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ebd9d-109">Properties</span></span>
| <span data-ttu-id="ebd9d-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ebd9d-110">Property</span></span>     | <span data-ttu-id="ebd9d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="ebd9d-111">Type</span></span>   |<span data-ttu-id="ebd9d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ebd9d-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ebd9d-113">disabledPlans</span><span class="sxs-lookup"><span data-stu-id="ebd9d-113">disabledPlans</span></span>|<span data-ttu-id="ebd9d-114">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="ebd9d-114">Guid collection</span></span>|<span data-ttu-id="ebd9d-115">Colección de los identificadores únicos para los planes que se han deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="ebd9d-115">A collection of the unique identifiers for plans that have been disabled.</span></span>|
|<span data-ttu-id="ebd9d-116">skuId</span><span class="sxs-lookup"><span data-stu-id="ebd9d-116">skuId</span></span>|<span data-ttu-id="ebd9d-117">Guid</span><span class="sxs-lookup"><span data-stu-id="ebd9d-117">Guid</span></span>|<span data-ttu-id="ebd9d-118">Identificador único de la SKU.</span><span class="sxs-lookup"><span data-stu-id="ebd9d-118">The unique identifier for the SKU.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ebd9d-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ebd9d-119">JSON representation</span></span>

<span data-ttu-id="ebd9d-120">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ebd9d-120">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.assignedLicense"
}-->

```json
{
  "disabledPlans": ["guid"],
  "skuId": "guid"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "assignedLicense resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
