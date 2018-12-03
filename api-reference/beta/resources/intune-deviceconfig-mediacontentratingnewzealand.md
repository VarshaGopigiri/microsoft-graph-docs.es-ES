---
title: Tipo de recurso mediaContentRatingNewZealand
description: Todavía no documentado
ms.openlocfilehash: e7650d7155c06ff30b541d873830865bed1d92ee
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090442"
---
# <a name="mediacontentratingnewzealand-resource-type"></a><span data-ttu-id="5d988-103">Tipo de recurso mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="5d988-103">mediaContentRatingNewZealand resource type</span></span>

> <span data-ttu-id="5d988-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5d988-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5d988-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5d988-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5d988-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5d988-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5d988-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="5d988-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="5d988-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d988-108">Properties</span></span>
|<span data-ttu-id="5d988-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5d988-109">Property</span></span>|<span data-ttu-id="5d988-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d988-110">Type</span></span>|<span data-ttu-id="5d988-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d988-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5d988-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="5d988-112">movieRating</span></span>|[<span data-ttu-id="5d988-113">ratingNewZealandMoviesType</span><span class="sxs-lookup"><span data-stu-id="5d988-113">ratingNewZealandMoviesType</span></span>](../resources/intune-deviceconfig-ratingnewzealandmoviestype.md)|<span data-ttu-id="5d988-114">Películas de clasificación seleccionado para Nueva Zelanda.</span><span class="sxs-lookup"><span data-stu-id="5d988-114">Movies rating selected for New Zealand.</span></span> <span data-ttu-id="5d988-115">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted` y `agesAbove16Restricted`.</span><span class="sxs-lookup"><span data-stu-id="5d988-115">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted`, `agesAbove16Restricted`.</span></span>|
|<span data-ttu-id="5d988-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="5d988-116">tvRating</span></span>|[<span data-ttu-id="5d988-117">ratingNewZealandTelevisionType</span><span class="sxs-lookup"><span data-stu-id="5d988-117">ratingNewZealandTelevisionType</span></span>](../resources/intune-deviceconfig-ratingnewzealandtelevisiontype.md)|<span data-ttu-id="5d988-118">Clasificación de TV seleccionada para Nueva Zelanda.</span><span class="sxs-lookup"><span data-stu-id="5d988-118">TV rating selected for New Zealand.</span></span> <span data-ttu-id="5d988-119">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="5d988-119">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5d988-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5d988-120">Relationships</span></span>
<span data-ttu-id="5d988-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="5d988-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="5d988-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5d988-122">JSON Representation</span></span>
<span data-ttu-id="5d988-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5d988-123">Here is a JSON representation of the resource.</span></span>
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




