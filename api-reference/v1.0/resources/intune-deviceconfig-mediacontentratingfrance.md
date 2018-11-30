---
title: Tipo de recurso mediaContentRatingFrance
description: Todavía no documentado
ms.openlocfilehash: bd2f4933ea05c7db193d700799cdcbdc79490356
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029218"
---
# <a name="mediacontentratingfrance-resource-type"></a><span data-ttu-id="0bd77-103">Tipo de recurso mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="0bd77-103">mediaContentRatingFrance resource type</span></span>

> <span data-ttu-id="0bd77-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0bd77-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0bd77-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="0bd77-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="0bd77-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0bd77-106">Properties</span></span>
|<span data-ttu-id="0bd77-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0bd77-107">Property</span></span>|<span data-ttu-id="0bd77-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="0bd77-108">Type</span></span>|<span data-ttu-id="0bd77-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="0bd77-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0bd77-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="0bd77-110">movieRating</span></span>|[<span data-ttu-id="0bd77-111">ratingFranceMoviesType</span><span class="sxs-lookup"><span data-stu-id="0bd77-111">ratingFranceMoviesType</span></span>](../resources/intune-deviceconfig-ratingfrancemoviestype.md)|<span data-ttu-id="0bd77-112">Películas de clasificación seleccionado para Francia.</span><span class="sxs-lookup"><span data-stu-id="0bd77-112">Movies rating selected for France.</span></span> <span data-ttu-id="0bd77-113">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="0bd77-113">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|
|<span data-ttu-id="0bd77-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="0bd77-114">tvRating</span></span>|[<span data-ttu-id="0bd77-115">ratingFranceTelevisionType</span><span class="sxs-lookup"><span data-stu-id="0bd77-115">ratingFranceTelevisionType</span></span>](../resources/intune-deviceconfig-ratingfrancetelevisiontype.md)|<span data-ttu-id="0bd77-116">Clasificación de TV seleccionada para Francia.</span><span class="sxs-lookup"><span data-stu-id="0bd77-116">TV rating selected for France.</span></span> <span data-ttu-id="0bd77-117">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="0bd77-117">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="0bd77-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0bd77-118">Relationships</span></span>
<span data-ttu-id="0bd77-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="0bd77-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="0bd77-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0bd77-120">JSON Representation</span></span>
<span data-ttu-id="0bd77-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0bd77-121">Here is a JSON representation of the resource.</span></span>
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



