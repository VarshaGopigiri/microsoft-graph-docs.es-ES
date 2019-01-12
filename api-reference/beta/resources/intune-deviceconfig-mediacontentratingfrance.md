---
title: Tipo de recurso mediaContentRatingFrance
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7aa3c16df6b32f5c5c50f53959aaccc767b39bbd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27928146"
---
# <a name="mediacontentratingfrance-resource-type"></a><span data-ttu-id="5229f-103">Tipo de recurso mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="5229f-103">mediaContentRatingFrance resource type</span></span>

> <span data-ttu-id="5229f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5229f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5229f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5229f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5229f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5229f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5229f-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="5229f-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="5229f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5229f-108">Properties</span></span>
|<span data-ttu-id="5229f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5229f-109">Property</span></span>|<span data-ttu-id="5229f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5229f-110">Type</span></span>|<span data-ttu-id="5229f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5229f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5229f-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="5229f-112">movieRating</span></span>|[<span data-ttu-id="5229f-113">ratingFranceMoviesType</span><span class="sxs-lookup"><span data-stu-id="5229f-113">ratingFranceMoviesType</span></span>](../resources/intune-deviceconfig-ratingfrancemoviestype.md)|<span data-ttu-id="5229f-114">Películas de clasificación seleccionado para Francia.</span><span class="sxs-lookup"><span data-stu-id="5229f-114">Movies rating selected for France.</span></span> <span data-ttu-id="5229f-115">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="5229f-115">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|
|<span data-ttu-id="5229f-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="5229f-116">tvRating</span></span>|[<span data-ttu-id="5229f-117">ratingFranceTelevisionType</span><span class="sxs-lookup"><span data-stu-id="5229f-117">ratingFranceTelevisionType</span></span>](../resources/intune-deviceconfig-ratingfrancetelevisiontype.md)|<span data-ttu-id="5229f-118">Clasificación de TV seleccionada para Francia.</span><span class="sxs-lookup"><span data-stu-id="5229f-118">TV rating selected for France.</span></span> <span data-ttu-id="5229f-119">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="5229f-119">Possible values are: `allAllowed`, `allBlocked`, `agesAbove10`, `agesAbove12`, `agesAbove16`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5229f-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5229f-120">Relationships</span></span>
<span data-ttu-id="5229f-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5229f-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5229f-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5229f-122">JSON Representation</span></span>
<span data-ttu-id="5229f-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5229f-123">Here is a JSON representation of the resource.</span></span>
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





