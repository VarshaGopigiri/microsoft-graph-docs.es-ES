---
title: tipo de recurso educationOrganization
description: 'Entidades abstractas que se utiliza para modelar la uniformidad entre los tipos de organización diferentes en el sector de educación.  '
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: a1e3f82e2d777b1d32cc445f543e7beed570a8b0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949524"
---
# <a name="educationorganization-resource-type"></a><span data-ttu-id="aaedd-103">tipo de recurso educationOrganization</span><span class="sxs-lookup"><span data-stu-id="aaedd-103">educationOrganization resource type</span></span>

> <span data-ttu-id="aaedd-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="aaedd-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="aaedd-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="aaedd-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="aaedd-106">Entidades abstractas que se utiliza para modelar la uniformidad entre los tipos de organización diferentes en el sector de educación.</span><span class="sxs-lookup"><span data-stu-id="aaedd-106">Abstract entity used to model the commonality between different organization types within the education sector.</span></span>  

## <a name="properties"></a><span data-ttu-id="aaedd-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aaedd-107">Properties</span></span>
| <span data-ttu-id="aaedd-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aaedd-108">Property</span></span>     | <span data-ttu-id="aaedd-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="aaedd-109">Type</span></span>   |<span data-ttu-id="aaedd-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="aaedd-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="aaedd-111">description</span><span class="sxs-lookup"><span data-stu-id="aaedd-111">description</span></span>|<span data-ttu-id="aaedd-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="aaedd-112">String</span></span>| <span data-ttu-id="aaedd-113">Descripción de la organización.</span><span class="sxs-lookup"><span data-stu-id="aaedd-113">Organization description.</span></span>|
|<span data-ttu-id="aaedd-114">displayName</span><span class="sxs-lookup"><span data-stu-id="aaedd-114">displayName</span></span>|<span data-ttu-id="aaedd-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="aaedd-115">String</span></span>| <span data-ttu-id="aaedd-116">Nombre para mostrar de organización.</span><span class="sxs-lookup"><span data-stu-id="aaedd-116">Organization display name.</span></span>|
|<span data-ttu-id="aaedd-117">externalSource</span><span class="sxs-lookup"><span data-stu-id="aaedd-117">externalSource</span></span>|<span data-ttu-id="aaedd-118">string</span><span class="sxs-lookup"><span data-stu-id="aaedd-118">string</span></span>| <span data-ttu-id="aaedd-119">Origen donde se creó esta organización.</span><span class="sxs-lookup"><span data-stu-id="aaedd-119">Source where this organization was created from.</span></span> <span data-ttu-id="aaedd-120">Los valores posibles son: `sis`, `manual` y `unknownFutureValue`.</span><span class="sxs-lookup"><span data-stu-id="aaedd-120">Possible values are: `sis`, `manual`, `unknownFutureValue`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="aaedd-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="aaedd-121">Relationships</span></span>
<span data-ttu-id="aaedd-122">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aaedd-122">None.</span></span>


## <a name="json-representation"></a><span data-ttu-id="aaedd-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="aaedd-123">JSON representation</span></span>

<span data-ttu-id="aaedd-124">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="aaedd-124">The following is a JSON representation of the resource.</span></span>

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
