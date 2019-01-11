---
title: Tipo de recurso mediaContentRatingFrance
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 502abcae283b7e97e04ab2c342e6b526b41f64f4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829886"
---
# <a name="mediacontentratingfrance-resource-type"></a><span data-ttu-id="a8d0d-103">Tipo de recurso mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="a8d0d-103">mediaContentRatingFrance resource type</span></span>

> <span data-ttu-id="a8d0d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a8d0d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a8d0d-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a8d0d-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="a8d0d-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8d0d-106">Properties</span></span>
|<span data-ttu-id="a8d0d-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a8d0d-107">Property</span></span>|<span data-ttu-id="a8d0d-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a8d0d-108">Type</span></span>|<span data-ttu-id="a8d0d-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a8d0d-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a8d0d-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="a8d0d-110">movieRating</span></span>|[<span data-ttu-id="a8d0d-111">ratingFranceMoviesType</span><span class="sxs-lookup"><span data-stu-id="a8d0d-111">ratingFranceMoviesType</span></span>](../resources/intune-deviceconfig-ratingfrancemoviestype.md)|<span data-ttu-id="a8d0d-112">Películas de clasificación seleccionado para Francia.</span><span class="sxs-lookup"><span data-stu-id="a8d0d-112">Movies rating selected for France.</span></span> <span data-ttu-id="a8d0d-113">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="a8d0d-113">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|
|<span data-ttu-id="a8d0d-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="a8d0d-114">tvRating</span></span>|[<span data-ttu-id="a8d0d-115">ratingFranceTelevisionType</span><span class="sxs-lookup"><span data-stu-id="a8d0d-115">ratingFranceTelevisionType</span></span>](../resources/intune-deviceconfig-ratingfrancetelevisiontype.md)|<span data-ttu-id="a8d0d-116">Clasificación de TV seleccionada para Francia.</span><span class="sxs-lookup"><span data-stu-id="a8d0d-116">TV rating selected for France.</span></span> <span data-ttu-id="a8d0d-117">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="a8d0d-117">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a8d0d-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a8d0d-118">Relationships</span></span>
<span data-ttu-id="a8d0d-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a8d0d-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a8d0d-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a8d0d-120">JSON Representation</span></span>
<span data-ttu-id="a8d0d-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a8d0d-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingFrance"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingFrance",
  "movieRating": "String",
  "tvRating": "String"
}
```



