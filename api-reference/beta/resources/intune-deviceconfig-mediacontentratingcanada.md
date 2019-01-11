---
title: Tipo de recurso mediaContentRatingCanada
description: Todavía no documentado
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 430baf0e6adaf53d922dc6cf94c8640107869ec4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27879936"
---
# <a name="mediacontentratingcanada-resource-type"></a><span data-ttu-id="be347-103">Tipo de recurso mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="be347-103">mediaContentRatingCanada resource type</span></span>

> <span data-ttu-id="be347-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="be347-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="be347-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="be347-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="be347-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="be347-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="be347-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="be347-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="be347-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="be347-108">Properties</span></span>
|<span data-ttu-id="be347-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="be347-109">Property</span></span>|<span data-ttu-id="be347-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="be347-110">Type</span></span>|<span data-ttu-id="be347-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="be347-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="be347-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="be347-112">movieRating</span></span>|[<span data-ttu-id="be347-113">ratingCanadaMoviesType</span><span class="sxs-lookup"><span data-stu-id="be347-113">ratingCanadaMoviesType</span></span>](../resources/intune-deviceconfig-ratingcanadamoviestype.md)|<span data-ttu-id="be347-114">Películas de clasificación seleccionado para Canadá.</span><span class="sxs-lookup"><span data-stu-id="be347-114">Movies rating selected for Canada.</span></span> <span data-ttu-id="be347-115">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18` y `restricted`.</span><span class="sxs-lookup"><span data-stu-id="be347-115">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`, `restricted`.</span></span>|
|<span data-ttu-id="be347-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="be347-116">tvRating</span></span>|[<span data-ttu-id="be347-117">ratingCanadaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="be347-117">ratingCanadaTelevisionType</span></span>](../resources/intune-deviceconfig-ratingcanadatelevisiontype.md)|<span data-ttu-id="be347-118">Clasificación de TV seleccionada para Canadá.</span><span class="sxs-lookup"><span data-stu-id="be347-118">TV rating selected for Canada.</span></span> <span data-ttu-id="be347-119">Los valores posibles son: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="be347-119">Possible values are: `allAllowed`, `allBlocked`, `children`, `childrenAbove8`, `general`, `parentalGuidance`, `agesAbove14`, `agesAbove18`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="be347-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="be347-120">Relationships</span></span>
<span data-ttu-id="be347-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="be347-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="be347-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="be347-122">JSON Representation</span></span>
<span data-ttu-id="be347-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="be347-123">Here is a JSON representation of the resource.</span></span>
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





