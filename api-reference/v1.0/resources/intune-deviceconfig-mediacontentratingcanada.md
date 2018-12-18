---
title: Tipo de recurso mediaContentRatingCanada
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 310d68ea3ee0fa563b9fe413e26bace51251025a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27312498"
---
# <a name="mediacontentratingcanada-resource-type"></a><span data-ttu-id="a9ea7-103">Tipo de recurso mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="a9ea7-103">mediaContentRatingCanada resource type</span></span>

> <span data-ttu-id="a9ea7-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a9ea7-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a9ea7-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="a9ea7-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a9ea7-106">Properties</span></span>
|<span data-ttu-id="a9ea7-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a9ea7-107">Property</span></span>|<span data-ttu-id="a9ea7-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a9ea7-108">Type</span></span>|<span data-ttu-id="a9ea7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="a9ea7-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a9ea7-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="a9ea7-110">movieRating</span></span>|[<span data-ttu-id="a9ea7-111">ratingCanadaMoviesType</span><span class="sxs-lookup"><span data-stu-id="a9ea7-111">ratingCanadaMoviesType</span></span>](../resources/intune-deviceconfig-ratingcanadamoviestype.md)|<span data-ttu-id="a9ea7-112">Películas de clasificación seleccionado para Canadá.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-112">Movies rating selected for Canada.</span></span> <span data-ttu-id="a9ea7-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18` y `restricted`.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`, `restricted`.</span></span>|
|<span data-ttu-id="a9ea7-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="a9ea7-114">tvRating</span></span>|[<span data-ttu-id="a9ea7-115">ratingCanadaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="a9ea7-115">ratingCanadaTelevisionType</span></span>](../resources/intune-deviceconfig-ratingcanadatelevisiontype.md)|<span data-ttu-id="a9ea7-116">Clasificación de TV seleccionada para Canadá.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-116">TV rating selected for Canada.</span></span> <span data-ttu-id="a9ea7-117">Los valores posibles son: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-117">Possible values are: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a9ea7-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a9ea7-118">Relationships</span></span>
<span data-ttu-id="a9ea7-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="a9ea7-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="a9ea7-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a9ea7-120">JSON Representation</span></span>
<span data-ttu-id="a9ea7-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a9ea7-121">Here is a JSON representation of the resource.</span></span>
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



