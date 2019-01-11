---
title: Tipo de recurso mediaContentRatingUnitedStates
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 28229d14f5914bcae9a014fca587ad03b6236647
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879607"
---
# <a name="mediacontentratingunitedstates-resource-type"></a><span data-ttu-id="baf4f-103">Tipo de recurso mediaContentRatingUnitedStates</span><span class="sxs-lookup"><span data-stu-id="baf4f-103">mediaContentRatingUnitedStates resource type</span></span>

> <span data-ttu-id="baf4f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="baf4f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="baf4f-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="baf4f-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="baf4f-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="baf4f-106">Properties</span></span>
|<span data-ttu-id="baf4f-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="baf4f-107">Property</span></span>|<span data-ttu-id="baf4f-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="baf4f-108">Type</span></span>|<span data-ttu-id="baf4f-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="baf4f-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="baf4f-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="baf4f-110">movieRating</span></span>|[<span data-ttu-id="baf4f-111">ratingUnitedStatesMoviesType</span><span class="sxs-lookup"><span data-stu-id="baf4f-111">ratingUnitedStatesMoviesType</span></span>](../resources/intune-deviceconfig-ratingunitedstatesmoviestype.md)|<span data-ttu-id="baf4f-112">Películas de clasificación seleccionado para Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="baf4f-112">Movies rating selected for United States.</span></span> <span data-ttu-id="baf4f-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `parentalGuidance13`, `restricted` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="baf4f-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `parentalGuidance13`, `restricted`, `adults`.</span></span>|
|<span data-ttu-id="baf4f-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="baf4f-114">tvRating</span></span>|[<span data-ttu-id="baf4f-115">ratingUnitedStatesTelevisionType</span><span class="sxs-lookup"><span data-stu-id="baf4f-115">ratingUnitedStatesTelevisionType</span></span>](../resources/intune-deviceconfig-ratingunitedstatestelevisiontype.md)|<span data-ttu-id="baf4f-116">Clasificación de TV seleccionada para Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="baf4f-116">TV rating selected for United States.</span></span> <span data-ttu-id="baf4f-117">Los valores posibles son: `allAllowed`, `allBlocked`, `childrenAll`, `childrenAbove7`, `general`, `parentalGuidance`, `childrenAbove14` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="baf4f-117">Possible values are: `allAllowed`, `allBlocked`, `childrenAll`, `childrenAbove7`, `general`, `parentalGuidance`, `childrenAbove14`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="baf4f-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="baf4f-118">Relationships</span></span>
<span data-ttu-id="baf4f-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="baf4f-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="baf4f-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="baf4f-120">JSON Representation</span></span>
<span data-ttu-id="baf4f-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="baf4f-121">Here is a JSON representation of the resource.</span></span>
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



