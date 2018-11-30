---
title: Tipo de recurso mediaContentRatingJapan
description: Todavía no documentado
ms.openlocfilehash: 15e905355133545db2cdf0864fcbba7e9c226183
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029977"
---
# <a name="mediacontentratingjapan-resource-type"></a><span data-ttu-id="9dd34-103">Tipo de recurso mediaContentRatingJapan</span><span class="sxs-lookup"><span data-stu-id="9dd34-103">mediaContentRatingJapan resource type</span></span>

> <span data-ttu-id="9dd34-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9dd34-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9dd34-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9dd34-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="9dd34-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9dd34-106">Properties</span></span>
|<span data-ttu-id="9dd34-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9dd34-107">Property</span></span>|<span data-ttu-id="9dd34-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9dd34-108">Type</span></span>|<span data-ttu-id="9dd34-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dd34-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9dd34-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="9dd34-110">movieRating</span></span>|[<span data-ttu-id="9dd34-111">ratingJapanMoviesType</span><span class="sxs-lookup"><span data-stu-id="9dd34-111">ratingJapanMoviesType</span></span>](../resources/intune-deviceconfig-ratingjapanmoviestype.md)|<span data-ttu-id="9dd34-112">Películas de clasificación seleccionado para Japón.</span><span class="sxs-lookup"><span data-stu-id="9dd34-112">Movies rating selected for Japan.</span></span> <span data-ttu-id="9dd34-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove15`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="9dd34-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="9dd34-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="9dd34-114">tvRating</span></span>|[<span data-ttu-id="9dd34-115">ratingJapanTelevisionType</span><span class="sxs-lookup"><span data-stu-id="9dd34-115">ratingJapanTelevisionType</span></span>](../resources/intune-deviceconfig-ratingjapantelevisiontype.md)|<span data-ttu-id="9dd34-116">Clasificación de TV seleccionada para Japón.</span><span class="sxs-lookup"><span data-stu-id="9dd34-116">TV rating selected for Japan.</span></span> <span data-ttu-id="9dd34-117">Los valores posibles son: `allAllowed`, `allBlocked` y `explicitAllowed`.</span><span class="sxs-lookup"><span data-stu-id="9dd34-117">Possible values are: `allAllowed`, `allBlocked`, `explicitAllowed`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9dd34-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9dd34-118">Relationships</span></span>
<span data-ttu-id="9dd34-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9dd34-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9dd34-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9dd34-120">JSON Representation</span></span>
<span data-ttu-id="9dd34-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9dd34-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingJapan"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingJapan",
  "movieRating": "String",
  "tvRating": "String"
}
```



