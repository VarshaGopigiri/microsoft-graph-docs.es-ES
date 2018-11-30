---
title: Tipo de recurso mediaContentRatingIreland
description: Todavía no documentado
ms.openlocfilehash: b4348e6f73730d59e6e67b3e102b9ad9caa98add
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028920"
---
# <a name="mediacontentratingireland-resource-type"></a><span data-ttu-id="89c37-103">Tipo de recurso mediaContentRatingIreland</span><span class="sxs-lookup"><span data-stu-id="89c37-103">mediaContentRatingIreland resource type</span></span>

> <span data-ttu-id="89c37-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="89c37-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="89c37-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="89c37-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="89c37-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="89c37-106">Properties</span></span>
|<span data-ttu-id="89c37-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="89c37-107">Property</span></span>|<span data-ttu-id="89c37-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="89c37-108">Type</span></span>|<span data-ttu-id="89c37-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="89c37-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="89c37-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="89c37-110">movieRating</span></span>|[<span data-ttu-id="89c37-111">ratingIrelandMoviesType</span><span class="sxs-lookup"><span data-stu-id="89c37-111">ratingIrelandMoviesType</span></span>](../resources/intune-deviceconfig-ratingirelandmoviestype.md)|<span data-ttu-id="89c37-112">Películas de clasificación seleccionado para Irlanda.</span><span class="sxs-lookup"><span data-stu-id="89c37-112">Movies rating selected for Ireland.</span></span> <span data-ttu-id="89c37-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove12`, `agesAbove15`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="89c37-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove12`, `agesAbove15`, `agesAbove16`, `adults`.</span></span>|
|<span data-ttu-id="89c37-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="89c37-114">tvRating</span></span>|[<span data-ttu-id="89c37-115">ratingIrelandTelevisionType</span><span class="sxs-lookup"><span data-stu-id="89c37-115">ratingIrelandTelevisionType</span></span>](../resources/intune-deviceconfig-ratingirelandtelevisiontype.md)|<span data-ttu-id="89c37-116">Clasificación de TV seleccionada para Irlanda.</span><span class="sxs-lookup"><span data-stu-id="89c37-116">TV rating selected for Ireland.</span></span> <span data-ttu-id="89c37-117">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `children`, `youngAdults`, `parentalSupervision` y `mature`.</span><span class="sxs-lookup"><span data-stu-id="89c37-117">Possible values are: `allAllowed`, `allBlocked`, `general`, `children`, `youngAdults`, `parentalSupervision`, `mature`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="89c37-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="89c37-118">Relationships</span></span>
<span data-ttu-id="89c37-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="89c37-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="89c37-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="89c37-120">JSON Representation</span></span>
<span data-ttu-id="89c37-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="89c37-121">Here is a JSON representation of the resource.</span></span>
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



