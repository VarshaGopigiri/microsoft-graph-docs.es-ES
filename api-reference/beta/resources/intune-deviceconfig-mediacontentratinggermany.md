---
title: Tipo de recurso mediaContentRatingGermany
description: Todavía no documentado
ms.openlocfilehash: 821a648f839e531c2efaa3da4b4b1aead65c9673
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086601"
---
# <a name="mediacontentratinggermany-resource-type"></a><span data-ttu-id="b3ef2-103">Tipo de recurso mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="b3ef2-103">mediaContentRatingGermany resource type</span></span>

> <span data-ttu-id="b3ef2-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b3ef2-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b3ef2-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b3ef2-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b3ef2-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b3ef2-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b3ef2-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="b3ef2-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="b3ef2-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b3ef2-108">Properties</span></span>
|<span data-ttu-id="b3ef2-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b3ef2-109">Property</span></span>|<span data-ttu-id="b3ef2-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="b3ef2-110">Type</span></span>|<span data-ttu-id="b3ef2-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b3ef2-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b3ef2-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="b3ef2-112">movieRating</span></span>|[<span data-ttu-id="b3ef2-113">ratingGermanyMoviesType</span><span class="sxs-lookup"><span data-stu-id="b3ef2-113">ratingGermanyMoviesType</span></span>](../resources/intune-deviceconfig-ratinggermanymoviestype.md)|<span data-ttu-id="b3ef2-114">Películas de clasificación seleccionado para Alemania.</span><span class="sxs-lookup"><span data-stu-id="b3ef2-114">Movies rating selected for Germany.</span></span> <span data-ttu-id="b3ef2-115">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="b3ef2-115">Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|
|<span data-ttu-id="b3ef2-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="b3ef2-116">tvRating</span></span>|[<span data-ttu-id="b3ef2-117">ratingGermanyTelevisionType</span><span class="sxs-lookup"><span data-stu-id="b3ef2-117">ratingGermanyTelevisionType</span></span>](../resources/intune-deviceconfig-ratinggermanytelevisiontype.md)|<span data-ttu-id="b3ef2-118">Clasificación de TV seleccionada para Alemania.</span><span class="sxs-lookup"><span data-stu-id="b3ef2-118">TV rating selected for Germany.</span></span> <span data-ttu-id="b3ef2-119">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="b3ef2-119">Possible values are: `allAllowed`, `allBlocked`, `general`, `agesAbove6`, `agesAbove12`, `agesAbove16`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b3ef2-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b3ef2-120">Relationships</span></span>
<span data-ttu-id="b3ef2-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b3ef2-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b3ef2-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b3ef2-122">JSON Representation</span></span>
<span data-ttu-id="b3ef2-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b3ef2-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingGermany"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingGermany",
  "movieRating": "String",
  "tvRating": "String"
}
```





