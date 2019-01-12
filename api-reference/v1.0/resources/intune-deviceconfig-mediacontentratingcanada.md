---
title: Tipo de recurso mediaContentRatingCanada
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9b4151b810fcfbc56c652492fff9fa1f3f841189
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932185"
---
# <a name="mediacontentratingcanada-resource-type"></a><span data-ttu-id="4a03b-103">Tipo de recurso mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="4a03b-103">mediaContentRatingCanada resource type</span></span>

> <span data-ttu-id="4a03b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4a03b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4a03b-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4a03b-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="4a03b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a03b-106">Properties</span></span>
|<span data-ttu-id="4a03b-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a03b-107">Property</span></span>|<span data-ttu-id="4a03b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a03b-108">Type</span></span>|<span data-ttu-id="4a03b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a03b-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4a03b-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="4a03b-110">movieRating</span></span>|[<span data-ttu-id="4a03b-111">ratingCanadaMoviesType</span><span class="sxs-lookup"><span data-stu-id="4a03b-111">ratingCanadaMoviesType</span></span>](../resources/intune-deviceconfig-ratingcanadamoviestype.md)|<span data-ttu-id="4a03b-112">Películas de clasificación seleccionado para Canadá.</span><span class="sxs-lookup"><span data-stu-id="4a03b-112">Movies rating selected for Canada.</span></span> <span data-ttu-id="4a03b-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18` y `restricted`.</span><span class="sxs-lookup"><span data-stu-id="4a03b-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`, `restricted`.</span></span>|
|<span data-ttu-id="4a03b-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="4a03b-114">tvRating</span></span>|[<span data-ttu-id="4a03b-115">ratingCanadaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="4a03b-115">ratingCanadaTelevisionType</span></span>](../resources/intune-deviceconfig-ratingcanadatelevisiontype.md)|<span data-ttu-id="4a03b-116">Clasificación de TV seleccionada para Canadá.</span><span class="sxs-lookup"><span data-stu-id="4a03b-116">TV rating selected for Canada.</span></span> <span data-ttu-id="4a03b-117">Los valores posibles son: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="4a03b-117">Possible values are: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4a03b-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4a03b-118">Relationships</span></span>
<span data-ttu-id="4a03b-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4a03b-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4a03b-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4a03b-120">JSON Representation</span></span>
<span data-ttu-id="4a03b-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4a03b-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingCanada"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingCanada",
  "movieRating": "String",
  "tvRating": "String"
}
```



