---
title: Tipo de recurso mediaContentRatingGermany
description: Todavía no documentado
ms.openlocfilehash: 40ad8d4794b44a41614d9ed02341a00bdb4df86d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030396"
---
# <a name="mediacontentratinggermany-resource-type"></a><span data-ttu-id="73f2d-103">Tipo de recurso mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="73f2d-103">mediaContentRatingGermany resource type</span></span>

> <span data-ttu-id="73f2d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="73f2d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="73f2d-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="73f2d-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="73f2d-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73f2d-106">Properties</span></span>
|<span data-ttu-id="73f2d-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="73f2d-107">Property</span></span>|<span data-ttu-id="73f2d-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="73f2d-108">Type</span></span>|<span data-ttu-id="73f2d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="73f2d-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="73f2d-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="73f2d-110">movieRating</span></span>|[<span data-ttu-id="73f2d-111">ratingGermanyMoviesType</span><span class="sxs-lookup"><span data-stu-id="73f2d-111">ratingGermanyMoviesType</span></span>](../resources/intune-deviceconfig-ratinggermanymoviestype.md)|<span data-ttu-id="73f2d-112">Películas de clasificación seleccionado para Alemania.</span><span class="sxs-lookup"><span data-stu-id="73f2d-112">Movies rating selected for Germany.</span></span> <span data-ttu-id="73f2d-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="73f2d-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|
|<span data-ttu-id="73f2d-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="73f2d-114">tvRating</span></span>|[<span data-ttu-id="73f2d-115">ratingGermanyTelevisionType</span><span class="sxs-lookup"><span data-stu-id="73f2d-115">ratingGermanyTelevisionType</span></span>](../resources/intune-deviceconfig-ratinggermanytelevisiontype.md)|<span data-ttu-id="73f2d-116">Clasificación de TV seleccionada para Alemania.</span><span class="sxs-lookup"><span data-stu-id="73f2d-116">TV rating selected for Germany.</span></span> <span data-ttu-id="73f2d-117">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="73f2d-117">Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="73f2d-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="73f2d-118">Relationships</span></span>
<span data-ttu-id="73f2d-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="73f2d-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="73f2d-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="73f2d-120">JSON Representation</span></span>
<span data-ttu-id="73f2d-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="73f2d-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingGermany"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingGermany",
  "movieRating": "String",
  "tvRating": "String"
}
```



