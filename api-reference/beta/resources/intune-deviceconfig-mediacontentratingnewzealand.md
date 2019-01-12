---
title: Tipo de recurso mediaContentRatingNewZealand
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a1866a6bf0c8d1849eb2fbf478b4f5d14fa3e5c0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916939"
---
# <a name="mediacontentratingnewzealand-resource-type"></a><span data-ttu-id="285c8-103">Tipo de recurso mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="285c8-103">mediaContentRatingNewZealand resource type</span></span>

> <span data-ttu-id="285c8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="285c8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="285c8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="285c8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="285c8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="285c8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="285c8-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="285c8-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="285c8-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="285c8-108">Properties</span></span>
|<span data-ttu-id="285c8-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="285c8-109">Property</span></span>|<span data-ttu-id="285c8-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="285c8-110">Type</span></span>|<span data-ttu-id="285c8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="285c8-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="285c8-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="285c8-112">movieRating</span></span>|[<span data-ttu-id="285c8-113">ratingNewZealandMoviesType</span><span class="sxs-lookup"><span data-stu-id="285c8-113">ratingNewZealandMoviesType</span></span>](../resources/intune-deviceconfig-ratingnewzealandmoviestype.md)|<span data-ttu-id="285c8-114">Películas de clasificación seleccionado para Nueva Zelanda.</span><span class="sxs-lookup"><span data-stu-id="285c8-114">Movies rating selected for New Zealand.</span></span> <span data-ttu-id="285c8-115">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted` y `agesAbove16Restricted`.</span><span class="sxs-lookup"><span data-stu-id="285c8-115">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted`, `agesAbove16Restricted`.</span></span>|
|<span data-ttu-id="285c8-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="285c8-116">tvRating</span></span>|[<span data-ttu-id="285c8-117">ratingNewZealandTelevisionType</span><span class="sxs-lookup"><span data-stu-id="285c8-117">ratingNewZealandTelevisionType</span></span>](../resources/intune-deviceconfig-ratingnewzealandtelevisiontype.md)|<span data-ttu-id="285c8-118">Clasificación de TV seleccionada para Nueva Zelanda.</span><span class="sxs-lookup"><span data-stu-id="285c8-118">TV rating selected for New Zealand.</span></span> <span data-ttu-id="285c8-119">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="285c8-119">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="285c8-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="285c8-120">Relationships</span></span>
<span data-ttu-id="285c8-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="285c8-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="285c8-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="285c8-122">JSON Representation</span></span>
<span data-ttu-id="285c8-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="285c8-123">Here is a JSON representation of the resource.</span></span>
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





