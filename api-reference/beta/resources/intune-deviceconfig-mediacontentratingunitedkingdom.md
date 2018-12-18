---
title: Tipo de recurso mediaContentRatingUnitedKingdom
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: cd4285f3be40961d2368da180c52e16b0ff6ea47
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27332567"
---
# <a name="mediacontentratingunitedkingdom-resource-type"></a><span data-ttu-id="673b1-103">Tipo de recurso mediaContentRatingUnitedKingdom</span><span class="sxs-lookup"><span data-stu-id="673b1-103">mediaContentRatingUnitedKingdom resource type</span></span>

> <span data-ttu-id="673b1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="673b1-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="673b1-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="673b1-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="673b1-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="673b1-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="673b1-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="673b1-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="673b1-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="673b1-108">Properties</span></span>
|<span data-ttu-id="673b1-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="673b1-109">Property</span></span>|<span data-ttu-id="673b1-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="673b1-110">Type</span></span>|<span data-ttu-id="673b1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="673b1-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="673b1-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="673b1-112">movieRating</span></span>|[<span data-ttu-id="673b1-113">ratingUnitedKingdomMoviesType</span><span class="sxs-lookup"><span data-stu-id="673b1-113">ratingUnitedKingdomMoviesType</span></span>](../resources/intune-deviceconfig-ratingunitedkingdommoviestype.md)|<span data-ttu-id="673b1-114">Películas de clasificación seleccionado para el Reino Unido.</span><span class="sxs-lookup"><span data-stu-id="673b1-114">Movies rating selected for United Kingdom.</span></span> <span data-ttu-id="673b1-115">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `universalChildren`, `parentalGuidance`, `agesAbove12Video`, `agesAbove12Cinema`, `agesAbove15` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="673b1-115">Possible values are: `allAllowed`, `allBlocked`, `general`, `universalChildren`, `parentalGuidance`, `agesAbove12Video`, `agesAbove12Cinema`, `agesAbove15`, `adults`.</span></span>|
|<span data-ttu-id="673b1-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="673b1-116">tvRating</span></span>|[<span data-ttu-id="673b1-117">ratingUnitedKingdomTelevisionType</span><span class="sxs-lookup"><span data-stu-id="673b1-117">ratingUnitedKingdomTelevisionType</span></span>](../resources/intune-deviceconfig-ratingunitedkingdomtelevisiontype.md)|<span data-ttu-id="673b1-118">Clasificación de TV seleccionada para el Reino Unido.</span><span class="sxs-lookup"><span data-stu-id="673b1-118">TV rating selected for United Kingdom.</span></span> <span data-ttu-id="673b1-119">Los valores posibles son: `allAllowed`, `allBlocked` y `caution`.</span><span class="sxs-lookup"><span data-stu-id="673b1-119">Possible values are: `allAllowed`, `allBlocked`, `caution`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="673b1-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="673b1-120">Relationships</span></span>
<span data-ttu-id="673b1-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="673b1-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="673b1-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="673b1-122">JSON Representation</span></span>
<span data-ttu-id="673b1-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="673b1-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingUnitedKingdom",
  "movieRating": "String",
  "tvRating": "String"
}
```





