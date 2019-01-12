---
title: Tipo de recurso mediaContentRatingUnitedStates
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 3e37a707b7ad190ddc1f3206f149d0dcc3c1aad3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27959228"
---
# <a name="mediacontentratingunitedstates-resource-type"></a><span data-ttu-id="2ba21-103">Tipo de recurso mediaContentRatingUnitedStates</span><span class="sxs-lookup"><span data-stu-id="2ba21-103">mediaContentRatingUnitedStates resource type</span></span>

> <span data-ttu-id="2ba21-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2ba21-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2ba21-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2ba21-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="2ba21-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2ba21-106">Properties</span></span>
|<span data-ttu-id="2ba21-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2ba21-107">Property</span></span>|<span data-ttu-id="2ba21-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ba21-108">Type</span></span>|<span data-ttu-id="2ba21-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ba21-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2ba21-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="2ba21-110">movieRating</span></span>|[<span data-ttu-id="2ba21-111">ratingUnitedStatesMoviesType</span><span class="sxs-lookup"><span data-stu-id="2ba21-111">ratingUnitedStatesMoviesType</span></span>](../resources/intune-deviceconfig-ratingunitedstatesmoviestype.md)|<span data-ttu-id="2ba21-112">Películas de clasificación seleccionado para Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="2ba21-112">Movies rating selected for United States.</span></span> <span data-ttu-id="2ba21-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `parentalGuidance13`, `restricted` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="2ba21-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `parentalGuidance13`, `restricted`, `adults`.</span></span>|
|<span data-ttu-id="2ba21-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="2ba21-114">tvRating</span></span>|[<span data-ttu-id="2ba21-115">ratingUnitedStatesTelevisionType</span><span class="sxs-lookup"><span data-stu-id="2ba21-115">ratingUnitedStatesTelevisionType</span></span>](../resources/intune-deviceconfig-ratingunitedstatestelevisiontype.md)|<span data-ttu-id="2ba21-116">Clasificación de TV seleccionada para Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="2ba21-116">TV rating selected for United States.</span></span> <span data-ttu-id="2ba21-117">Los valores posibles son: `allAllowed`, `allBlocked`, `childrenAll`, `childrenAbove7`, `general`, `parentalGuidance`, `childrenAbove14` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="2ba21-117">Possible values are: `allAllowed`, `allBlocked`, `childrenAll`, `childrenAbove7`, `general`, `parentalGuidance`, `childrenAbove14`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2ba21-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2ba21-118">Relationships</span></span>
<span data-ttu-id="2ba21-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2ba21-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2ba21-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2ba21-120">JSON Representation</span></span>
<span data-ttu-id="2ba21-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2ba21-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingUnitedStates",
  "movieRating": "String",
  "tvRating": "String"
}
```



