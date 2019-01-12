---
title: Tipo de recurso mediaContentRatingIreland
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 531768883b88e8fc89fe00c1df7a8a9e8767a408
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27934880"
---
# <a name="mediacontentratingireland-resource-type"></a><span data-ttu-id="b4f6a-103">Tipo de recurso mediaContentRatingIreland</span><span class="sxs-lookup"><span data-stu-id="b4f6a-103">mediaContentRatingIreland resource type</span></span>

> <span data-ttu-id="b4f6a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b4f6a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b4f6a-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b4f6a-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="b4f6a-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4f6a-106">Properties</span></span>
|<span data-ttu-id="b4f6a-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4f6a-107">Property</span></span>|<span data-ttu-id="b4f6a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4f6a-108">Type</span></span>|<span data-ttu-id="b4f6a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4f6a-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b4f6a-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="b4f6a-110">movieRating</span></span>|[<span data-ttu-id="b4f6a-111">ratingIrelandMoviesType</span><span class="sxs-lookup"><span data-stu-id="b4f6a-111">ratingIrelandMoviesType</span></span>](../resources/intune-deviceconfig-ratingirelandmoviestype.md)|<span data-ttu-id="b4f6a-112">Películas de clasificación seleccionado para Irlanda.</span><span class="sxs-lookup"><span data-stu-id="b4f6a-112">Movies rating selected for Ireland.</span></span> <span data-ttu-id="b4f6a-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove12`, `agesAbove15`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="b4f6a-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove12`, `agesAbove15`, `agesAbove16`, `adults`.</span></span>|
|<span data-ttu-id="b4f6a-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="b4f6a-114">tvRating</span></span>|[<span data-ttu-id="b4f6a-115">ratingIrelandTelevisionType</span><span class="sxs-lookup"><span data-stu-id="b4f6a-115">ratingIrelandTelevisionType</span></span>](../resources/intune-deviceconfig-ratingirelandtelevisiontype.md)|<span data-ttu-id="b4f6a-116">Clasificación de TV seleccionada para Irlanda.</span><span class="sxs-lookup"><span data-stu-id="b4f6a-116">TV rating selected for Ireland.</span></span> <span data-ttu-id="b4f6a-117">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `children`, `youngAdults`, `parentalSupervision` y `mature`.</span><span class="sxs-lookup"><span data-stu-id="b4f6a-117">Possible values are: `allAllowed`, `allBlocked`, `general`, `children`, `youngAdults`, `parentalSupervision`, `mature`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b4f6a-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b4f6a-118">Relationships</span></span>
<span data-ttu-id="b4f6a-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b4f6a-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b4f6a-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b4f6a-120">JSON Representation</span></span>
<span data-ttu-id="b4f6a-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b4f6a-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingIreland"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingIreland",
  "movieRating": "String",
  "tvRating": "String"
}
```



