---
title: Tipo de recurso mediaContentRatingCanada
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: efdc88934e46c849f48c0eb24ddd49535b824044
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331958"
---
# <a name="mediacontentratingcanada-resource-type"></a><span data-ttu-id="f53eb-103">Tipo de recurso mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="f53eb-103">mediaContentRatingCanada resource type</span></span>

> <span data-ttu-id="f53eb-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f53eb-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f53eb-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f53eb-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f53eb-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f53eb-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f53eb-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="f53eb-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="f53eb-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f53eb-108">Properties</span></span>
|<span data-ttu-id="f53eb-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f53eb-109">Property</span></span>|<span data-ttu-id="f53eb-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f53eb-110">Type</span></span>|<span data-ttu-id="f53eb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f53eb-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f53eb-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="f53eb-112">movieRating</span></span>|[<span data-ttu-id="f53eb-113">ratingCanadaMoviesType</span><span class="sxs-lookup"><span data-stu-id="f53eb-113">ratingCanadaMoviesType</span></span>](../resources/intune-deviceconfig-ratingcanadamoviestype.md)|<span data-ttu-id="f53eb-114">Películas de clasificación seleccionado para Canadá.</span><span class="sxs-lookup"><span data-stu-id="f53eb-114">Movies rating selected for Canada.</span></span> <span data-ttu-id="f53eb-115">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18` y `restricted`.</span><span class="sxs-lookup"><span data-stu-id="f53eb-115">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`, `restricted`.</span></span>|
|<span data-ttu-id="f53eb-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="f53eb-116">tvRating</span></span>|[<span data-ttu-id="f53eb-117">ratingCanadaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="f53eb-117">ratingCanadaTelevisionType</span></span>](../resources/intune-deviceconfig-ratingcanadatelevisiontype.md)|<span data-ttu-id="f53eb-118">Clasificación de TV seleccionada para Canadá.</span><span class="sxs-lookup"><span data-stu-id="f53eb-118">TV rating selected for Canada.</span></span> <span data-ttu-id="f53eb-119">Los valores posibles son: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="f53eb-119">Possible values are: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f53eb-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f53eb-120">Relationships</span></span>
<span data-ttu-id="f53eb-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="f53eb-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="f53eb-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f53eb-122">JSON Representation</span></span>
<span data-ttu-id="f53eb-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f53eb-123">Here is a JSON representation of the resource.</span></span>
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





