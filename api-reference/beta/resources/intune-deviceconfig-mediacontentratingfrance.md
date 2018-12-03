---
title: Tipo de recurso mediaContentRatingFrance
description: Todavía no documentado
ms.openlocfilehash: dabadb4d03181d3cd66db582005c4ec58f28aa9d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085067"
---
# <a name="mediacontentratingfrance-resource-type"></a><span data-ttu-id="784e2-103">Tipo de recurso mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="784e2-103">mediaContentRatingFrance resource type</span></span>

> <span data-ttu-id="784e2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="784e2-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="784e2-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="784e2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="784e2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="784e2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="784e2-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="784e2-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="784e2-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="784e2-108">Properties</span></span>
|<span data-ttu-id="784e2-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="784e2-109">Property</span></span>|<span data-ttu-id="784e2-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="784e2-110">Type</span></span>|<span data-ttu-id="784e2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="784e2-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="784e2-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="784e2-112">movieRating</span></span>|[<span data-ttu-id="784e2-113">ratingFranceMoviesType</span><span class="sxs-lookup"><span data-stu-id="784e2-113">ratingFranceMoviesType</span></span>](../resources/intune-deviceconfig-ratingfrancemoviestype.md)|<span data-ttu-id="784e2-114">Películas de clasificación seleccionado para Francia.</span><span class="sxs-lookup"><span data-stu-id="784e2-114">Movies rating selected for France.</span></span> <span data-ttu-id="784e2-115">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="784e2-115">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|
|<span data-ttu-id="784e2-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="784e2-116">tvRating</span></span>|[<span data-ttu-id="784e2-117">ratingFranceTelevisionType</span><span class="sxs-lookup"><span data-stu-id="784e2-117">ratingFranceTelevisionType</span></span>](../resources/intune-deviceconfig-ratingfrancetelevisiontype.md)|<span data-ttu-id="784e2-118">Clasificación de TV seleccionada para Francia.</span><span class="sxs-lookup"><span data-stu-id="784e2-118">TV rating selected for France.</span></span> <span data-ttu-id="784e2-119">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="784e2-119">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="784e2-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="784e2-120">Relationships</span></span>
<span data-ttu-id="784e2-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="784e2-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="784e2-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="784e2-122">JSON Representation</span></span>
<span data-ttu-id="784e2-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="784e2-123">Here is a JSON representation of the resource.</span></span>
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




