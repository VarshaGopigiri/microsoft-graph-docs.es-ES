---
title: Tipo de recurso mediaContentRatingNewZealand
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5d4a22f9510a615dab746912aed1de5123184ca3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27850550"
---
# <a name="mediacontentratingnewzealand-resource-type"></a><span data-ttu-id="8ef78-103">Tipo de recurso mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="8ef78-103">mediaContentRatingNewZealand resource type</span></span>

> <span data-ttu-id="8ef78-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8ef78-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8ef78-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="8ef78-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="8ef78-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8ef78-106">Properties</span></span>
|<span data-ttu-id="8ef78-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8ef78-107">Property</span></span>|<span data-ttu-id="8ef78-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ef78-108">Type</span></span>|<span data-ttu-id="8ef78-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ef78-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8ef78-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="8ef78-110">movieRating</span></span>|[<span data-ttu-id="8ef78-111">ratingNewZealandMoviesType</span><span class="sxs-lookup"><span data-stu-id="8ef78-111">ratingNewZealandMoviesType</span></span>](../resources/intune-deviceconfig-ratingnewzealandmoviestype.md)|<span data-ttu-id="8ef78-112">Películas de clasificación seleccionado para Nueva Zelanda.</span><span class="sxs-lookup"><span data-stu-id="8ef78-112">Movies rating selected for New Zealand.</span></span> <span data-ttu-id="8ef78-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted` y `agesAbove16Restricted`.</span><span class="sxs-lookup"><span data-stu-id="8ef78-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted`, `agesAbove16Restricted`.</span></span>|
|<span data-ttu-id="8ef78-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="8ef78-114">tvRating</span></span>|[<span data-ttu-id="8ef78-115">ratingNewZealandTelevisionType</span><span class="sxs-lookup"><span data-stu-id="8ef78-115">ratingNewZealandTelevisionType</span></span>](../resources/intune-deviceconfig-ratingnewzealandtelevisiontype.md)|<span data-ttu-id="8ef78-116">Clasificación de TV seleccionada para Nueva Zelanda.</span><span class="sxs-lookup"><span data-stu-id="8ef78-116">TV rating selected for New Zealand.</span></span> <span data-ttu-id="8ef78-117">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="8ef78-117">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8ef78-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8ef78-118">Relationships</span></span>
<span data-ttu-id="8ef78-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8ef78-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8ef78-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8ef78-120">JSON Representation</span></span>
<span data-ttu-id="8ef78-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8ef78-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingNewZealand"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingNewZealand",
  "movieRating": "String",
  "tvRating": "String"
}
```



