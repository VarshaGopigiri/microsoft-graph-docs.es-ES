---
title: Tipo de recurso mediaContentRatingAustralia
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0860a17671b2923c2be9b5b469f93d443e808f53
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891486"
---
# <a name="mediacontentratingaustralia-resource-type"></a><span data-ttu-id="abef1-103">Tipo de recurso mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="abef1-103">mediaContentRatingAustralia resource type</span></span>

> <span data-ttu-id="abef1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="abef1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="abef1-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="abef1-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="abef1-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="abef1-106">Properties</span></span>
|<span data-ttu-id="abef1-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="abef1-107">Property</span></span>|<span data-ttu-id="abef1-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="abef1-108">Type</span></span>|<span data-ttu-id="abef1-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="abef1-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="abef1-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="abef1-110">movieRating</span></span>|[<span data-ttu-id="abef1-111">ratingAustraliaMoviesType</span><span class="sxs-lookup"><span data-stu-id="abef1-111">ratingAustraliaMoviesType</span></span>](../resources/intune-deviceconfig-ratingaustraliamoviestype.md)|<span data-ttu-id="abef1-112">Películas de clasificación seleccionado para Australia.</span><span class="sxs-lookup"><span data-stu-id="abef1-112">Movies rating selected for Australia.</span></span> <span data-ttu-id="abef1-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="abef1-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="abef1-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="abef1-114">tvRating</span></span>|[<span data-ttu-id="abef1-115">ratingAustraliaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="abef1-115">ratingAustraliaTelevisionType</span></span>](../resources/intune-deviceconfig-ratingaustraliatelevisiontype.md)|<span data-ttu-id="abef1-116">Clasificación de TV seleccionada para Australia.</span><span class="sxs-lookup"><span data-stu-id="abef1-116">TV rating selected for Australia.</span></span> <span data-ttu-id="abef1-117">Los valores posibles son: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove15AdultViolence`.</span><span class="sxs-lookup"><span data-stu-id="abef1-117">Possible values are: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove15AdultViolence`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="abef1-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="abef1-118">Relationships</span></span>
<span data-ttu-id="abef1-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="abef1-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="abef1-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="abef1-120">JSON Representation</span></span>
<span data-ttu-id="abef1-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="abef1-121">Here is a JSON representation of the resource.</span></span>
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



