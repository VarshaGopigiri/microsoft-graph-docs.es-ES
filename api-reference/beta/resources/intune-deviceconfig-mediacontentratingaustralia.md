---
title: Tipo de recurso mediaContentRatingAustralia
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 916257d83e28f3877773a6fcc7d7aefadab41af8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884227"
---
# <a name="mediacontentratingaustralia-resource-type"></a><span data-ttu-id="307ae-103">Tipo de recurso mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="307ae-103">mediaContentRatingAustralia resource type</span></span>

> <span data-ttu-id="307ae-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="307ae-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="307ae-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="307ae-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="307ae-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="307ae-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="307ae-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="307ae-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="307ae-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="307ae-108">Properties</span></span>
|<span data-ttu-id="307ae-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="307ae-109">Property</span></span>|<span data-ttu-id="307ae-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="307ae-110">Type</span></span>|<span data-ttu-id="307ae-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="307ae-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="307ae-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="307ae-112">movieRating</span></span>|[<span data-ttu-id="307ae-113">ratingAustraliaMoviesType</span><span class="sxs-lookup"><span data-stu-id="307ae-113">ratingAustraliaMoviesType</span></span>](../resources/intune-deviceconfig-ratingaustraliamoviestype.md)|<span data-ttu-id="307ae-114">Películas de clasificación seleccionado para Australia.</span><span class="sxs-lookup"><span data-stu-id="307ae-114">Movies rating selected for Australia.</span></span> <span data-ttu-id="307ae-115">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="307ae-115">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="307ae-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="307ae-116">tvRating</span></span>|[<span data-ttu-id="307ae-117">ratingAustraliaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="307ae-117">ratingAustraliaTelevisionType</span></span>](../resources/intune-deviceconfig-ratingaustraliatelevisiontype.md)|<span data-ttu-id="307ae-118">Clasificación de TV seleccionada para Australia.</span><span class="sxs-lookup"><span data-stu-id="307ae-118">TV rating selected for Australia.</span></span> <span data-ttu-id="307ae-119">Los valores posibles son: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove15AdultViolence`.</span><span class="sxs-lookup"><span data-stu-id="307ae-119">Possible values are: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove15AdultViolence`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="307ae-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="307ae-120">Relationships</span></span>
<span data-ttu-id="307ae-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="307ae-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="307ae-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="307ae-122">JSON Representation</span></span>
<span data-ttu-id="307ae-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="307ae-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingAustralia"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingAustralia",
  "movieRating": "String",
  "tvRating": "String"
}
```





