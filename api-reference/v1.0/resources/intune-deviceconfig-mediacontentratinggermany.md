---
title: Tipo de recurso mediaContentRatingGermany
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5dd25a8bd29211fd593daf3ecea20a7808384bc1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860007"
---
# <a name="mediacontentratinggermany-resource-type"></a><span data-ttu-id="a0c81-103">Tipo de recurso mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="a0c81-103">mediaContentRatingGermany resource type</span></span>

> <span data-ttu-id="a0c81-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a0c81-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a0c81-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a0c81-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="a0c81-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a0c81-106">Properties</span></span>
|<span data-ttu-id="a0c81-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a0c81-107">Property</span></span>|<span data-ttu-id="a0c81-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a0c81-108">Type</span></span>|<span data-ttu-id="a0c81-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0c81-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a0c81-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="a0c81-110">movieRating</span></span>|[<span data-ttu-id="a0c81-111">ratingGermanyMoviesType</span><span class="sxs-lookup"><span data-stu-id="a0c81-111">ratingGermanyMoviesType</span></span>](../resources/intune-deviceconfig-ratinggermanymoviestype.md)|<span data-ttu-id="a0c81-112">Películas de clasificación seleccionado para Alemania.</span><span class="sxs-lookup"><span data-stu-id="a0c81-112">Movies rating selected for Germany.</span></span> <span data-ttu-id="a0c81-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="a0c81-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|
|<span data-ttu-id="a0c81-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="a0c81-114">tvRating</span></span>|[<span data-ttu-id="a0c81-115">ratingGermanyTelevisionType</span><span class="sxs-lookup"><span data-stu-id="a0c81-115">ratingGermanyTelevisionType</span></span>](../resources/intune-deviceconfig-ratinggermanytelevisiontype.md)|<span data-ttu-id="a0c81-116">Clasificación de TV seleccionada para Alemania.</span><span class="sxs-lookup"><span data-stu-id="a0c81-116">TV rating selected for Germany.</span></span> <span data-ttu-id="a0c81-117">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="a0c81-117">Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a0c81-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a0c81-118">Relationships</span></span>
<span data-ttu-id="a0c81-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a0c81-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a0c81-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a0c81-120">JSON Representation</span></span>
<span data-ttu-id="a0c81-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a0c81-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingGermany"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingGermany",
  "movieRating": "String",
  "tvRating": "String"
}
```



