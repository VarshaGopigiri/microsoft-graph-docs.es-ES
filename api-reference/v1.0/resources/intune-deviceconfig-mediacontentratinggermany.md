---
title: Tipo de recurso mediaContentRatingGermany
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 8add327725e5d3886d381b63c7debc16c256d810
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27327702"
---
# <a name="mediacontentratinggermany-resource-type"></a><span data-ttu-id="73639-103">Tipo de recurso mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="73639-103">mediaContentRatingGermany resource type</span></span>

> <span data-ttu-id="73639-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="73639-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="73639-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="73639-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="73639-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="73639-106">Properties</span></span>
|<span data-ttu-id="73639-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="73639-107">Property</span></span>|<span data-ttu-id="73639-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="73639-108">Type</span></span>|<span data-ttu-id="73639-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="73639-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="73639-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="73639-110">movieRating</span></span>|[<span data-ttu-id="73639-111">ratingGermanyMoviesType</span><span class="sxs-lookup"><span data-stu-id="73639-111">ratingGermanyMoviesType</span></span>](../resources/intune-deviceconfig-ratinggermanymoviestype.md)|<span data-ttu-id="73639-112">Películas de clasificación seleccionado para Alemania.</span><span class="sxs-lookup"><span data-stu-id="73639-112">Movies rating selected for Germany.</span></span> <span data-ttu-id="73639-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="73639-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|
|<span data-ttu-id="73639-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="73639-114">tvRating</span></span>|[<span data-ttu-id="73639-115">ratingGermanyTelevisionType</span><span class="sxs-lookup"><span data-stu-id="73639-115">ratingGermanyTelevisionType</span></span>](../resources/intune-deviceconfig-ratinggermanytelevisiontype.md)|<span data-ttu-id="73639-116">Clasificación de TV seleccionada para Alemania.</span><span class="sxs-lookup"><span data-stu-id="73639-116">TV rating selected for Germany.</span></span> <span data-ttu-id="73639-117">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="73639-117">Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="73639-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="73639-118">Relationships</span></span>
<span data-ttu-id="73639-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="73639-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="73639-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="73639-120">JSON Representation</span></span>
<span data-ttu-id="73639-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="73639-121">Here is a JSON representation of the resource.</span></span>
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



