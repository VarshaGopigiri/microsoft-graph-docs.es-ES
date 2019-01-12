---
title: Tipo de recurso mediaContentRatingAustralia
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5f3f12cc233c1accfad05ccec92d412c75426d1a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27952849"
---
# <a name="mediacontentratingaustralia-resource-type"></a><span data-ttu-id="9f44c-103">Tipo de recurso mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="9f44c-103">mediaContentRatingAustralia resource type</span></span>

> <span data-ttu-id="9f44c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9f44c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9f44c-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9f44c-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="9f44c-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f44c-106">Properties</span></span>
|<span data-ttu-id="9f44c-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f44c-107">Property</span></span>|<span data-ttu-id="9f44c-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f44c-108">Type</span></span>|<span data-ttu-id="9f44c-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f44c-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9f44c-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="9f44c-110">movieRating</span></span>|[<span data-ttu-id="9f44c-111">ratingAustraliaMoviesType</span><span class="sxs-lookup"><span data-stu-id="9f44c-111">ratingAustraliaMoviesType</span></span>](../resources/intune-deviceconfig-ratingaustraliamoviestype.md)|<span data-ttu-id="9f44c-112">Películas de clasificación seleccionado para Australia.</span><span class="sxs-lookup"><span data-stu-id="9f44c-112">Movies rating selected for Australia.</span></span> <span data-ttu-id="9f44c-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="9f44c-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="9f44c-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="9f44c-114">tvRating</span></span>|[<span data-ttu-id="9f44c-115">ratingAustraliaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="9f44c-115">ratingAustraliaTelevisionType</span></span>](../resources/intune-deviceconfig-ratingaustraliatelevisiontype.md)|<span data-ttu-id="9f44c-116">Clasificación de TV seleccionada para Australia.</span><span class="sxs-lookup"><span data-stu-id="9f44c-116">TV rating selected for Australia.</span></span> <span data-ttu-id="9f44c-117">Los valores posibles son: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove15AdultViolence`.</span><span class="sxs-lookup"><span data-stu-id="9f44c-117">Possible values are: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove15AdultViolence`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9f44c-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9f44c-118">Relationships</span></span>
<span data-ttu-id="9f44c-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9f44c-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9f44c-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9f44c-120">JSON Representation</span></span>
<span data-ttu-id="9f44c-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9f44c-121">Here is a JSON representation of the resource.</span></span>
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



