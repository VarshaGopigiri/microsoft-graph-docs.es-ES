---
title: Tipo de recurso mediaContentRatingCanada
description: Todavía no documentado
ms.openlocfilehash: 764bea688c5c7d86f675caafdc47fa42d4a7d37a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031587"
---
# <a name="mediacontentratingcanada-resource-type"></a><span data-ttu-id="4d675-103">Tipo de recurso mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="4d675-103">mediaContentRatingCanada resource type</span></span>

> <span data-ttu-id="4d675-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4d675-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4d675-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4d675-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="4d675-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d675-106">Properties</span></span>
|<span data-ttu-id="4d675-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4d675-107">Property</span></span>|<span data-ttu-id="4d675-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d675-108">Type</span></span>|<span data-ttu-id="4d675-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d675-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4d675-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="4d675-110">movieRating</span></span>|[<span data-ttu-id="4d675-111">ratingCanadaMoviesType</span><span class="sxs-lookup"><span data-stu-id="4d675-111">ratingCanadaMoviesType</span></span>](../resources/intune-deviceconfig-ratingcanadamoviestype.md)|<span data-ttu-id="4d675-112">Películas de clasificación seleccionado para Canadá.</span><span class="sxs-lookup"><span data-stu-id="4d675-112">Movies rating selected for Canada.</span></span> <span data-ttu-id="4d675-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18` y `restricted`.</span><span class="sxs-lookup"><span data-stu-id="4d675-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`, `restricted`.</span></span>|
|<span data-ttu-id="4d675-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="4d675-114">tvRating</span></span>|[<span data-ttu-id="4d675-115">ratingCanadaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="4d675-115">ratingCanadaTelevisionType</span></span>](../resources/intune-deviceconfig-ratingcanadatelevisiontype.md)|<span data-ttu-id="4d675-116">Clasificación de TV seleccionada para Canadá.</span><span class="sxs-lookup"><span data-stu-id="4d675-116">TV rating selected for Canada.</span></span> <span data-ttu-id="4d675-117">Los valores posibles son: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="4d675-117">Possible values are: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4d675-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4d675-118">Relationships</span></span>
<span data-ttu-id="4d675-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4d675-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4d675-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4d675-120">JSON Representation</span></span>
<span data-ttu-id="4d675-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4d675-121">Here is a JSON representation of the resource.</span></span>
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



