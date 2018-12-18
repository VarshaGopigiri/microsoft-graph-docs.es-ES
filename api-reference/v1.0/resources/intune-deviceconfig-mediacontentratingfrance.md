---
title: Tipo de recurso mediaContentRatingFrance
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 0981a73fdc1e8468d9e8ab8590387dfa357a39c9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27361645"
---
# <a name="mediacontentratingfrance-resource-type"></a><span data-ttu-id="90ccf-103">Tipo de recurso mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="90ccf-103">mediaContentRatingFrance resource type</span></span>

> <span data-ttu-id="90ccf-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="90ccf-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="90ccf-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="90ccf-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="90ccf-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="90ccf-106">Properties</span></span>
|<span data-ttu-id="90ccf-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90ccf-107">Property</span></span>|<span data-ttu-id="90ccf-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="90ccf-108">Type</span></span>|<span data-ttu-id="90ccf-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="90ccf-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="90ccf-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="90ccf-110">movieRating</span></span>|[<span data-ttu-id="90ccf-111">ratingFranceMoviesType</span><span class="sxs-lookup"><span data-stu-id="90ccf-111">ratingFranceMoviesType</span></span>](../resources/intune-deviceconfig-ratingfrancemoviestype.md)|<span data-ttu-id="90ccf-112">Películas de clasificación seleccionado para Francia.</span><span class="sxs-lookup"><span data-stu-id="90ccf-112">Movies rating selected for France.</span></span> <span data-ttu-id="90ccf-113">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="90ccf-113">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|
|<span data-ttu-id="90ccf-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="90ccf-114">tvRating</span></span>|[<span data-ttu-id="90ccf-115">ratingFranceTelevisionType</span><span class="sxs-lookup"><span data-stu-id="90ccf-115">ratingFranceTelevisionType</span></span>](../resources/intune-deviceconfig-ratingfrancetelevisiontype.md)|<span data-ttu-id="90ccf-116">Clasificación de TV seleccionada para Francia.</span><span class="sxs-lookup"><span data-stu-id="90ccf-116">TV rating selected for France.</span></span> <span data-ttu-id="90ccf-117">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="90ccf-117">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="90ccf-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="90ccf-118">Relationships</span></span>
<span data-ttu-id="90ccf-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="90ccf-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="90ccf-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="90ccf-120">JSON Representation</span></span>
<span data-ttu-id="90ccf-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="90ccf-121">Here is a JSON representation of the resource.</span></span>
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



