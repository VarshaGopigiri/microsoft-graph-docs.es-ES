---
title: Tipo de recurso mediaContentRatingAustralia
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 01d809b43bc8ce68ffc92600d3634c8bd437a954
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27319505"
---
# <a name="mediacontentratingaustralia-resource-type"></a><span data-ttu-id="cbc8a-103">Tipo de recurso mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="cbc8a-103">mediaContentRatingAustralia resource type</span></span>

> <span data-ttu-id="cbc8a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cbc8a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cbc8a-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="cbc8a-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="cbc8a-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="cbc8a-106">Properties</span></span>
|<span data-ttu-id="cbc8a-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cbc8a-107">Property</span></span>|<span data-ttu-id="cbc8a-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="cbc8a-108">Type</span></span>|<span data-ttu-id="cbc8a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="cbc8a-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cbc8a-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="cbc8a-110">movieRating</span></span>|[<span data-ttu-id="cbc8a-111">ratingAustraliaMoviesType</span><span class="sxs-lookup"><span data-stu-id="cbc8a-111">ratingAustraliaMoviesType</span></span>](../resources/intune-deviceconfig-ratingaustraliamoviestype.md)|<span data-ttu-id="cbc8a-112">Películas de clasificación seleccionado para Australia.</span><span class="sxs-lookup"><span data-stu-id="cbc8a-112">Movies rating selected for Australia.</span></span> <span data-ttu-id="cbc8a-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="cbc8a-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="cbc8a-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="cbc8a-114">tvRating</span></span>|[<span data-ttu-id="cbc8a-115">ratingAustraliaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="cbc8a-115">ratingAustraliaTelevisionType</span></span>](../resources/intune-deviceconfig-ratingaustraliatelevisiontype.md)|<span data-ttu-id="cbc8a-116">Clasificación de TV seleccionada para Australia.</span><span class="sxs-lookup"><span data-stu-id="cbc8a-116">TV rating selected for Australia.</span></span> <span data-ttu-id="cbc8a-117">Los valores posibles son: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove15AdultViolence`.</span><span class="sxs-lookup"><span data-stu-id="cbc8a-117">Possible values are: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove15AdultViolence`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="cbc8a-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="cbc8a-118">Relationships</span></span>
<span data-ttu-id="cbc8a-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="cbc8a-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="cbc8a-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="cbc8a-120">JSON Representation</span></span>
<span data-ttu-id="cbc8a-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="cbc8a-121">Here is a JSON representation of the resource.</span></span>
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



