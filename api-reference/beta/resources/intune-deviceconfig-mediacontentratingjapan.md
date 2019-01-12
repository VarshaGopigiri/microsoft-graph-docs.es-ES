---
title: Tipo de recurso mediaContentRatingJapan
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 202b778fefe1236577f61058025714ea0f337826
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943021"
---
# <a name="mediacontentratingjapan-resource-type"></a><span data-ttu-id="57d05-103">Tipo de recurso mediaContentRatingJapan</span><span class="sxs-lookup"><span data-stu-id="57d05-103">mediaContentRatingJapan resource type</span></span>

> <span data-ttu-id="57d05-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="57d05-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="57d05-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="57d05-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="57d05-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="57d05-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="57d05-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="57d05-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="57d05-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="57d05-108">Properties</span></span>
|<span data-ttu-id="57d05-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="57d05-109">Property</span></span>|<span data-ttu-id="57d05-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="57d05-110">Type</span></span>|<span data-ttu-id="57d05-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="57d05-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="57d05-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="57d05-112">movieRating</span></span>|[<span data-ttu-id="57d05-113">ratingJapanMoviesType</span><span class="sxs-lookup"><span data-stu-id="57d05-113">ratingJapanMoviesType</span></span>](../resources/intune-deviceconfig-ratingjapanmoviestype.md)|<span data-ttu-id="57d05-114">Películas de clasificación seleccionado para Japón.</span><span class="sxs-lookup"><span data-stu-id="57d05-114">Movies rating selected for Japan.</span></span> <span data-ttu-id="57d05-115">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove15`, `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="57d05-115">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="57d05-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="57d05-116">tvRating</span></span>|[<span data-ttu-id="57d05-117">ratingJapanTelevisionType</span><span class="sxs-lookup"><span data-stu-id="57d05-117">ratingJapanTelevisionType</span></span>](../resources/intune-deviceconfig-ratingjapantelevisiontype.md)|<span data-ttu-id="57d05-118">Clasificación de TV seleccionada para Japón.</span><span class="sxs-lookup"><span data-stu-id="57d05-118">TV rating selected for Japan.</span></span> <span data-ttu-id="57d05-119">Los valores posibles son: `allAllowed`, `allBlocked` y `explicitAllowed`.</span><span class="sxs-lookup"><span data-stu-id="57d05-119">Possible values are: `allAllowed`, `allBlocked`, `explicitAllowed`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="57d05-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="57d05-120">Relationships</span></span>
<span data-ttu-id="57d05-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="57d05-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="57d05-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="57d05-122">JSON Representation</span></span>
<span data-ttu-id="57d05-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="57d05-123">Here is a JSON representation of the resource.</span></span>
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





