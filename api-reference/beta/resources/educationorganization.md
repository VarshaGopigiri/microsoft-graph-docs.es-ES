---
title: tipo de recurso educationOrganization
description: 'Entidades abstractas que se utiliza para modelar la uniformidad entre los tipos de organización diferentes en el sector de educación.  '
author: mmast-msft
ms.openlocfilehash: 54f281de29033418b6acb2f9821c5ebd1eaf4db0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27349892"
---
# <a name="educationorganization-resource-type"></a><span data-ttu-id="42b9f-103">tipo de recurso educationOrganization</span><span class="sxs-lookup"><span data-stu-id="42b9f-103">educationOrganization resource type</span></span>

> <span data-ttu-id="42b9f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="42b9f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="42b9f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="42b9f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="42b9f-106">Entidades abstractas que se utiliza para modelar la uniformidad entre los tipos de organización diferentes en el sector de educación.</span><span class="sxs-lookup"><span data-stu-id="42b9f-106">Abstract entity used to model the commonality between different organization types within the education sector.</span></span>  

## <a name="properties"></a><span data-ttu-id="42b9f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="42b9f-107">Properties</span></span>
| <span data-ttu-id="42b9f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="42b9f-108">Property</span></span>     | <span data-ttu-id="42b9f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="42b9f-109">Type</span></span>   |<span data-ttu-id="42b9f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="42b9f-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="42b9f-111">description</span><span class="sxs-lookup"><span data-stu-id="42b9f-111">description</span></span>|<span data-ttu-id="42b9f-112">String</span><span class="sxs-lookup"><span data-stu-id="42b9f-112">String</span></span>| <span data-ttu-id="42b9f-113">Descripción de la organización.</span><span class="sxs-lookup"><span data-stu-id="42b9f-113">Organization description.</span></span>|
|<span data-ttu-id="42b9f-114">displayName</span><span class="sxs-lookup"><span data-stu-id="42b9f-114">displayName</span></span>|<span data-ttu-id="42b9f-115">String</span><span class="sxs-lookup"><span data-stu-id="42b9f-115">String</span></span>| <span data-ttu-id="42b9f-116">Nombre para mostrar de organización.</span><span class="sxs-lookup"><span data-stu-id="42b9f-116">Organization display name.</span></span>|
|<span data-ttu-id="42b9f-117">externalSource</span><span class="sxs-lookup"><span data-stu-id="42b9f-117">externalSource</span></span>|<span data-ttu-id="42b9f-118">string</span><span class="sxs-lookup"><span data-stu-id="42b9f-118">string</span></span>| <span data-ttu-id="42b9f-119">Origen donde se creó esta organización.</span><span class="sxs-lookup"><span data-stu-id="42b9f-119">Source where this organization was created from.</span></span> <span data-ttu-id="42b9f-120">Los valores posibles son: `sis`, `manual` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="42b9f-120">Possible values are: `sis`, `manual`, `unknownFutureValue`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="42b9f-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="42b9f-121">Relationships</span></span>
<span data-ttu-id="42b9f-122">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="42b9f-122">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="42b9f-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="42b9f-123">JSON representation</span></span>

<span data-ttu-id="42b9f-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="42b9f-124">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
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