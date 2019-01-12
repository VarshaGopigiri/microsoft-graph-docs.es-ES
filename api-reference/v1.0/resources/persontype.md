---
title: Tipo de recurso personType
description: Representa el tipo de contacto.
localization_priority: Normal
author: simonhult
ms.prod: insights
ms.openlocfilehash: 270fa800242ae7a25ed0f5959a97b6a70f7cedd3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27917275"
---
# <a name="persontype-resource-type"></a><span data-ttu-id="57b0c-103">Tipo de recurso personType</span><span class="sxs-lookup"><span data-stu-id="57b0c-103">personType resource type</span></span>

<span data-ttu-id="57b0c-104">Representa el tipo de contacto.</span><span class="sxs-lookup"><span data-stu-id="57b0c-104">Represents the type of person.</span></span>


## <a name="json-representation"></a><span data-ttu-id="57b0c-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="57b0c-105">JSON representation</span></span>

<span data-ttu-id="57b0c-106">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="57b0c-106">The following is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="57b0c-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="57b0c-107">Properties</span></span>
| <span data-ttu-id="57b0c-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="57b0c-108">Property</span></span>     | <span data-ttu-id="57b0c-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="57b0c-109">Type</span></span>   |<span data-ttu-id="57b0c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="57b0c-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="57b0c-111">class</span><span class="sxs-lookup"><span data-stu-id="57b0c-111">class</span></span>|<span data-ttu-id="57b0c-112">String</span><span class="sxs-lookup"><span data-stu-id="57b0c-112">String</span></span>|<span data-ttu-id="57b0c-113">El tipo de origen de datos, como Person.</span><span class="sxs-lookup"><span data-stu-id="57b0c-113">The type of data source, such as Person.</span></span>|
|<span data-ttu-id="57b0c-114">subclass</span><span class="sxs-lookup"><span data-stu-id="57b0c-114">subclass</span></span>|<span data-ttu-id="57b0c-115">String</span><span class="sxs-lookup"><span data-stu-id="57b0c-115">String</span></span>|<span data-ttu-id="57b0c-116">El tipo secundario del origen de datos, como OrganizationUser.</span><span class="sxs-lookup"><span data-stu-id="57b0c-116">The secondary type of data source, such as OrganizationUser.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "personType resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
