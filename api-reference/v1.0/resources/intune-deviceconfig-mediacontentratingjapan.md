---
title: Tipo de recurso mediaContentRatingJapan
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a0f394b85af0fd1f1c85a8db34025b2e1f139521
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822137"
---
# <a name="mediacontentratingjapan-resource-type"></a><span data-ttu-id="2808d-103">Tipo de recurso mediaContentRatingJapan</span><span class="sxs-lookup"><span data-stu-id="2808d-103">mediaContentRatingJapan resource type</span></span>

> <span data-ttu-id="2808d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2808d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2808d-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="2808d-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="2808d-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2808d-106">Properties</span></span>
|<span data-ttu-id="2808d-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2808d-107">Property</span></span>|<span data-ttu-id="2808d-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="2808d-108">Type</span></span>|<span data-ttu-id="2808d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2808d-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2808d-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="2808d-110">movieRating</span></span>|[<span data-ttu-id="2808d-111">ratingJapanMoviesType</span><span class="sxs-lookup"><span data-stu-id="2808d-111">ratingJapanMoviesType</span></span>](../resources/intune-deviceconfig-ratingjapanmoviestype.md)|<span data-ttu-id="2808d-112">Películas de clasificación seleccionado para Japón.</span><span class="sxs-lookup"><span data-stu-id="2808d-112">Movies rating selected for Japan.</span></span> <span data-ttu-id="2808d-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove15`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="2808d-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="2808d-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="2808d-114">tvRating</span></span>|[<span data-ttu-id="2808d-115">ratingJapanTelevisionType</span><span class="sxs-lookup"><span data-stu-id="2808d-115">ratingJapanTelevisionType</span></span>](../resources/intune-deviceconfig-ratingjapantelevisiontype.md)|<span data-ttu-id="2808d-116">Clasificación de TV seleccionada para Japón.</span><span class="sxs-lookup"><span data-stu-id="2808d-116">TV rating selected for Japan.</span></span> <span data-ttu-id="2808d-117">Los valores posibles son: `allAllowed`, `allBlocked` y `explicitAllowed`.</span><span class="sxs-lookup"><span data-stu-id="2808d-117">Possible values are: `allAllowed`, `allBlocked`, `explicitAllowed`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="2808d-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2808d-118">Relationships</span></span>
<span data-ttu-id="2808d-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2808d-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="2808d-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2808d-120">JSON Representation</span></span>
<span data-ttu-id="2808d-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2808d-121">Here is a JSON representation of the resource.</span></span>
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



