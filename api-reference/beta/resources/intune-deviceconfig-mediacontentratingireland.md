---
title: Tipo de recurso mediaContentRatingIreland
description: Todavía no documentado
ms.openlocfilehash: 2d1f2d2fa03084e2999eb35e6ab0ec19ff555106
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083312"
---
# <a name="mediacontentratingireland-resource-type"></a><span data-ttu-id="110f4-103">Tipo de recurso mediaContentRatingIreland</span><span class="sxs-lookup"><span data-stu-id="110f4-103">mediaContentRatingIreland resource type</span></span>

> <span data-ttu-id="110f4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="110f4-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="110f4-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="110f4-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="110f4-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="110f4-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="110f4-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="110f4-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="110f4-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="110f4-108">Properties</span></span>
|<span data-ttu-id="110f4-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="110f4-109">Property</span></span>|<span data-ttu-id="110f4-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="110f4-110">Type</span></span>|<span data-ttu-id="110f4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="110f4-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="110f4-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="110f4-112">movieRating</span></span>|[<span data-ttu-id="110f4-113">ratingIrelandMoviesType</span><span class="sxs-lookup"><span data-stu-id="110f4-113">ratingIrelandMoviesType</span></span>](../resources/intune-deviceconfig-ratingirelandmoviestype.md)|<span data-ttu-id="110f4-114">Películas de clasificación seleccionado para Irlanda.</span><span class="sxs-lookup"><span data-stu-id="110f4-114">Movies rating selected for Ireland.</span></span> <span data-ttu-id="110f4-115">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove12`, `agesAbove15`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="110f4-115">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove12`, `agesAbove15`, `agesAbove16`, `adults`.</span></span>|
|<span data-ttu-id="110f4-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="110f4-116">tvRating</span></span>|[<span data-ttu-id="110f4-117">ratingIrelandTelevisionType</span><span class="sxs-lookup"><span data-stu-id="110f4-117">ratingIrelandTelevisionType</span></span>](../resources/intune-deviceconfig-ratingirelandtelevisiontype.md)|<span data-ttu-id="110f4-118">Clasificación de TV seleccionada para Irlanda.</span><span class="sxs-lookup"><span data-stu-id="110f4-118">TV rating selected for Ireland.</span></span> <span data-ttu-id="110f4-119">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `children`, `youngAdults`, `parentalSupervision` y `mature`.</span><span class="sxs-lookup"><span data-stu-id="110f4-119">Possible values are: `allAllowed`, `allBlocked`, `general`, `children`, `youngAdults`, `parentalSupervision`, `mature`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="110f4-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="110f4-120">Relationships</span></span>
<span data-ttu-id="110f4-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="110f4-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="110f4-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="110f4-122">JSON Representation</span></span>
<span data-ttu-id="110f4-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="110f4-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingIreland"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingIreland",
  "movieRating": "String",
  "tvRating": "String"
}
```





