---
title: Tipo de recurso assignedLicense
description: Representa una licencia asignada a un usuario. La propiedad **assignedLicenses** de la entidad user es una colección de **assignedLicense**.
ms.openlocfilehash: 48863a9acdcfa173a3f0c1a2a008516360ffdf9b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029738"
---
# <a name="assignedlicense-resource-type"></a><span data-ttu-id="4d6e3-104">Tipo de recurso assignedLicense</span><span class="sxs-lookup"><span data-stu-id="4d6e3-104">assignedLicense resource type</span></span>

<span data-ttu-id="4d6e3-p102">Representa una licencia asignada a un usuario. La propiedad **assignedLicenses** de la entidad [user](user.md) es una colección de **assignedLicense**.</span><span class="sxs-lookup"><span data-stu-id="4d6e3-p102">Represents a license assigned to a user. The **assignedLicenses** property of the [user](user.md) entity is a collection of **assignedLicense**.</span></span>

## <a name="properties"></a><span data-ttu-id="4d6e3-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d6e3-107">Properties</span></span>
| <span data-ttu-id="4d6e3-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4d6e3-108">Property</span></span>     | <span data-ttu-id="4d6e3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d6e3-109">Type</span></span>   |<span data-ttu-id="4d6e3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d6e3-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4d6e3-111">disabledPlans</span><span class="sxs-lookup"><span data-stu-id="4d6e3-111">disabledPlans</span></span>|<span data-ttu-id="4d6e3-112">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="4d6e3-112">Guid collection</span></span>|<span data-ttu-id="4d6e3-113">Colección de los identificadores únicos para los planes que se han deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="4d6e3-113">A collection of the unique identifiers for plans that have been disabled.</span></span>|
|<span data-ttu-id="4d6e3-114">skuId</span><span class="sxs-lookup"><span data-stu-id="4d6e3-114">skuId</span></span>|<span data-ttu-id="4d6e3-115">Guid</span><span class="sxs-lookup"><span data-stu-id="4d6e3-115">Guid</span></span>|<span data-ttu-id="4d6e3-116">Identificador único de la SKU.</span><span class="sxs-lookup"><span data-stu-id="4d6e3-116">The unique identifier for the SKU.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4d6e3-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4d6e3-117">JSON representation</span></span>

<span data-ttu-id="4d6e3-118">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="4d6e3-118">Here is a JSON representation of the resource</span></span>

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
