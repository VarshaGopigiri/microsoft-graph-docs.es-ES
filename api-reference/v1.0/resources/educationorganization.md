---
title: tipo de recurso educationOrganization
description: Entidades abstractas que se utiliza para modelar la uniformidad entre los tipos de organización diferentes en el sector de educación.
author: mmast-msft
ms.openlocfilehash: e4c0f69d63108cc88b88f530e99cbd55b23f49ed
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326148"
---
# <a name="educationorganization-resource-type"></a><span data-ttu-id="ec4c7-103">tipo de recurso educationOrganization</span><span class="sxs-lookup"><span data-stu-id="ec4c7-103">educationOrganization resource type</span></span>

<span data-ttu-id="ec4c7-104">Entidades abstractas que se utiliza para modelar la uniformidad entre los tipos de organización diferentes en el sector de educación.</span><span class="sxs-lookup"><span data-stu-id="ec4c7-104">Abstract entity used to model the commonality between different organization types within the education sector.</span></span>

## <a name="properties"></a><span data-ttu-id="ec4c7-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec4c7-105">Properties</span></span>
| <span data-ttu-id="ec4c7-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ec4c7-106">Property</span></span>     | <span data-ttu-id="ec4c7-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec4c7-107">Type</span></span>   |<span data-ttu-id="ec4c7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec4c7-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ec4c7-109">description</span><span class="sxs-lookup"><span data-stu-id="ec4c7-109">description</span></span>|<span data-ttu-id="ec4c7-110">String</span><span class="sxs-lookup"><span data-stu-id="ec4c7-110">String</span></span>| <span data-ttu-id="ec4c7-111">Descripción de la organización.</span><span class="sxs-lookup"><span data-stu-id="ec4c7-111">Organization description.</span></span>|
|<span data-ttu-id="ec4c7-112">displayName</span><span class="sxs-lookup"><span data-stu-id="ec4c7-112">displayName</span></span>|<span data-ttu-id="ec4c7-113">String</span><span class="sxs-lookup"><span data-stu-id="ec4c7-113">String</span></span>| <span data-ttu-id="ec4c7-114">Nombre para mostrar de organización.</span><span class="sxs-lookup"><span data-stu-id="ec4c7-114">Organization display name.</span></span>|
|<span data-ttu-id="ec4c7-115">externalSource</span><span class="sxs-lookup"><span data-stu-id="ec4c7-115">externalSource</span></span>|<span data-ttu-id="ec4c7-116">educationExternalSource</span><span class="sxs-lookup"><span data-stu-id="ec4c7-116">educationExternalSource</span></span>| <span data-ttu-id="ec4c7-117">Origen donde se creó esta organización.</span><span class="sxs-lookup"><span data-stu-id="ec4c7-117">Source where this organization was created from.</span></span> <span data-ttu-id="ec4c7-118">Los valores posibles son: `sis`, `manual`, `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="ec4c7-118">The possible values are: `sis`, `manual`, `unknownFutureValue`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ec4c7-119">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ec4c7-119">Relationships</span></span>
<span data-ttu-id="ec4c7-120">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="ec4c7-120">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="ec4c7-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ec4c7-121">JSON representation</span></span>

<span data-ttu-id="ec4c7-122">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ec4c7-122">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationOrganization"
}-->

```json
{
  "description": "String",
  "displayName": "String",
  "externalSource": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationOrganization resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->