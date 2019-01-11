---
title: Tipo de recurso personType
description: Representa el tipo de contacto.
localization_priority: Normal
ms.openlocfilehash: d30441a9eab3f51b63e31e5c3c627444312449ba
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27831496"
---
# <a name="persontype-resource-type"></a><span data-ttu-id="dfad0-103">Tipo de recurso personType</span><span class="sxs-lookup"><span data-stu-id="dfad0-103">personType resource type</span></span>

<span data-ttu-id="dfad0-104">Representa el tipo de contacto.</span><span class="sxs-lookup"><span data-stu-id="dfad0-104">Represents the type of person.</span></span>


## <a name="json-representation"></a><span data-ttu-id="dfad0-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dfad0-105">JSON representation</span></span>

<span data-ttu-id="dfad0-106">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="dfad0-106">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.personType"
}-->

```json
{
  "class": "string",
  "subclass": "string"
}

```
## <a name="properties"></a><span data-ttu-id="dfad0-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dfad0-107">Properties</span></span>
| <span data-ttu-id="dfad0-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dfad0-108">Property</span></span>     | <span data-ttu-id="dfad0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="dfad0-109">Type</span></span>   |<span data-ttu-id="dfad0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfad0-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dfad0-111">class</span><span class="sxs-lookup"><span data-stu-id="dfad0-111">class</span></span>|<span data-ttu-id="dfad0-112">String</span><span class="sxs-lookup"><span data-stu-id="dfad0-112">String</span></span>|<span data-ttu-id="dfad0-113">El tipo de origen de datos, como Person.</span><span class="sxs-lookup"><span data-stu-id="dfad0-113">The type of data source, such as Person.</span></span>|
|<span data-ttu-id="dfad0-114">subclass</span><span class="sxs-lookup"><span data-stu-id="dfad0-114">subclass</span></span>|<span data-ttu-id="dfad0-115">String</span><span class="sxs-lookup"><span data-stu-id="dfad0-115">String</span></span>|<span data-ttu-id="dfad0-116">El tipo secundario del origen de datos, como OrganizationUser.</span><span class="sxs-lookup"><span data-stu-id="dfad0-116">The secondary type of data source, such as OrganizationUser.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "personType resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
