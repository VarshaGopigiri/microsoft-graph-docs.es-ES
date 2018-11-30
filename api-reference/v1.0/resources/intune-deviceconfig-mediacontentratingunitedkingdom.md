---
title: Tipo de recurso mediaContentRatingUnitedKingdom
description: Todavía no documentado
ms.openlocfilehash: 8bc3b7cf1de10a6ef5b72feb7e633018766b0397
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029741"
---
# <a name="mediacontentratingunitedkingdom-resource-type"></a><span data-ttu-id="e6698-103">Tipo de recurso mediaContentRatingUnitedKingdom</span><span class="sxs-lookup"><span data-stu-id="e6698-103">mediaContentRatingUnitedKingdom resource type</span></span>

> <span data-ttu-id="e6698-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6698-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6698-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="e6698-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="e6698-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e6698-106">Properties</span></span>
|<span data-ttu-id="e6698-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e6698-107">Property</span></span>|<span data-ttu-id="e6698-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6698-108">Type</span></span>|<span data-ttu-id="e6698-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6698-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e6698-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="e6698-110">movieRating</span></span>|[<span data-ttu-id="e6698-111">ratingUnitedKingdomMoviesType</span><span class="sxs-lookup"><span data-stu-id="e6698-111">ratingUnitedKingdomMoviesType</span></span>](../resources/intune-deviceconfig-ratingunitedkingdommoviestype.md)|<span data-ttu-id="e6698-112">Películas de clasificación seleccionado para el Reino Unido.</span><span class="sxs-lookup"><span data-stu-id="e6698-112">Movies rating selected for United Kingdom.</span></span> <span data-ttu-id="e6698-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `universalChildren`, `parentalGuidance`, `agesAbove12Video`, `agesAbove12Cinema`, `agesAbove15` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="e6698-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `universalChildren`, `parentalGuidance`, `agesAbove12Video`, `agesAbove12Cinema`, `agesAbove15`, `adults`.</span></span>|
|<span data-ttu-id="e6698-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="e6698-114">tvRating</span></span>|[<span data-ttu-id="e6698-115">ratingUnitedKingdomTelevisionType</span><span class="sxs-lookup"><span data-stu-id="e6698-115">ratingUnitedKingdomTelevisionType</span></span>](../resources/intune-deviceconfig-ratingunitedkingdomtelevisiontype.md)|<span data-ttu-id="e6698-116">Clasificación de TV seleccionada para el Reino Unido.</span><span class="sxs-lookup"><span data-stu-id="e6698-116">TV rating selected for United Kingdom.</span></span> <span data-ttu-id="e6698-117">Los valores posibles son: `allAllowed`, `allBlocked` y `caution`.</span><span class="sxs-lookup"><span data-stu-id="e6698-117">Possible values are: `allAllowed`, `allBlocked`, `caution`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="e6698-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="e6698-118">Relationships</span></span>
<span data-ttu-id="e6698-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="e6698-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="e6698-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e6698-120">JSON Representation</span></span>
<span data-ttu-id="e6698-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e6698-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingUnitedKingdom",
  "movieRating": "String",
  "tvRating": "String"
}
```



