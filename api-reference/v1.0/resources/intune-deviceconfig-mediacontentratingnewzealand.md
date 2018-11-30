---
title: Tipo de recurso mediaContentRatingNewZealand
description: Todavía no documentado
ms.openlocfilehash: 0d34843ef7cc624b222694cc8fbe0fa7a7c1b74c
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030397"
---
# <a name="mediacontentratingnewzealand-resource-type"></a><span data-ttu-id="9d677-103">Tipo de recurso mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="9d677-103">mediaContentRatingNewZealand resource type</span></span>

> <span data-ttu-id="9d677-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9d677-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9d677-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="9d677-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="9d677-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9d677-106">Properties</span></span>
|<span data-ttu-id="9d677-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9d677-107">Property</span></span>|<span data-ttu-id="9d677-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d677-108">Type</span></span>|<span data-ttu-id="9d677-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d677-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9d677-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="9d677-110">movieRating</span></span>|[<span data-ttu-id="9d677-111">ratingNewZealandMoviesType</span><span class="sxs-lookup"><span data-stu-id="9d677-111">ratingNewZealandMoviesType</span></span>](../resources/intune-deviceconfig-ratingnewzealandmoviestype.md)|<span data-ttu-id="9d677-112">Películas de clasificación seleccionado para Nueva Zelanda.</span><span class="sxs-lookup"><span data-stu-id="9d677-112">Movies rating selected for New Zealand.</span></span> <span data-ttu-id="9d677-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted` y `agesAbove16Restricted`.</span><span class="sxs-lookup"><span data-stu-id="9d677-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted`, `agesAbove16Restricted`.</span></span>|
|<span data-ttu-id="9d677-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="9d677-114">tvRating</span></span>|[<span data-ttu-id="9d677-115">ratingNewZealandTelevisionType</span><span class="sxs-lookup"><span data-stu-id="9d677-115">ratingNewZealandTelevisionType</span></span>](../resources/intune-deviceconfig-ratingnewzealandtelevisiontype.md)|<span data-ttu-id="9d677-116">Clasificación de TV seleccionada para Nueva Zelanda.</span><span class="sxs-lookup"><span data-stu-id="9d677-116">TV rating selected for New Zealand.</span></span> <span data-ttu-id="9d677-117">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="9d677-117">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9d677-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9d677-118">Relationships</span></span>
<span data-ttu-id="9d677-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9d677-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9d677-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9d677-120">JSON Representation</span></span>
<span data-ttu-id="9d677-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9d677-121">Here is a JSON representation of the resource.</span></span>
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



