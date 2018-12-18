---
title: Tipo de recurso mediaContentRatingNewZealand
description: Todavía no documentado
author: tfitzmac
ms.openlocfilehash: 5daba568ee435c32cc0b3d491c1cedcc61294603
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27356108"
---
# <a name="mediacontentratingnewzealand-resource-type"></a><span data-ttu-id="3692e-103">Tipo de recurso mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="3692e-103">mediaContentRatingNewZealand resource type</span></span>

> <span data-ttu-id="3692e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3692e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3692e-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="3692e-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="3692e-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3692e-106">Properties</span></span>
|<span data-ttu-id="3692e-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3692e-107">Property</span></span>|<span data-ttu-id="3692e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="3692e-108">Type</span></span>|<span data-ttu-id="3692e-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="3692e-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="3692e-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="3692e-110">movieRating</span></span>|[<span data-ttu-id="3692e-111">ratingNewZealandMoviesType</span><span class="sxs-lookup"><span data-stu-id="3692e-111">ratingNewZealandMoviesType</span></span>](../resources/intune-deviceconfig-ratingnewzealandmoviestype.md)|<span data-ttu-id="3692e-112">Películas de clasificación seleccionado para Nueva Zelanda.</span><span class="sxs-lookup"><span data-stu-id="3692e-112">Movies rating selected for New Zealand.</span></span> <span data-ttu-id="3692e-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted` y `agesAbove16Restricted`.</span><span class="sxs-lookup"><span data-stu-id="3692e-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove13`, `agesAbove15`, `agesAbove16`, `agesAbove18`, `restricted`, `agesAbove16Restricted`.</span></span>|
|<span data-ttu-id="3692e-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="3692e-114">tvRating</span></span>|[<span data-ttu-id="3692e-115">ratingNewZealandTelevisionType</span><span class="sxs-lookup"><span data-stu-id="3692e-115">ratingNewZealandTelevisionType</span></span>](../resources/intune-deviceconfig-ratingnewzealandtelevisiontype.md)|<span data-ttu-id="3692e-116">Clasificación de TV seleccionada para Nueva Zelanda.</span><span class="sxs-lookup"><span data-stu-id="3692e-116">TV rating selected for New Zealand.</span></span> <span data-ttu-id="3692e-117">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="3692e-117">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="3692e-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3692e-118">Relationships</span></span>
<span data-ttu-id="3692e-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="3692e-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="3692e-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3692e-120">JSON Representation</span></span>
<span data-ttu-id="3692e-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3692e-121">Here is a JSON representation of the resource.</span></span>
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



