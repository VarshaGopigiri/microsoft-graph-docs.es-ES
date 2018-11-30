---
title: Tipo de recurso mediaContentRatingAustralia
description: Todavía no documentado
ms.openlocfilehash: f60df6c4948d0e0208b545a8a25e31ca29247879
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030401"
---
# <a name="mediacontentratingaustralia-resource-type"></a><span data-ttu-id="20440-103">Tipo de recurso mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="20440-103">mediaContentRatingAustralia resource type</span></span>

> <span data-ttu-id="20440-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="20440-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="20440-105">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="20440-105">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="20440-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="20440-106">Properties</span></span>
|<span data-ttu-id="20440-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="20440-107">Property</span></span>|<span data-ttu-id="20440-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="20440-108">Type</span></span>|<span data-ttu-id="20440-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="20440-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="20440-110">movieRating</span><span class="sxs-lookup"><span data-stu-id="20440-110">movieRating</span></span>|[<span data-ttu-id="20440-111">ratingAustraliaMoviesType</span><span class="sxs-lookup"><span data-stu-id="20440-111">ratingAustraliaMoviesType</span></span>](../resources/intune-deviceconfig-ratingaustraliamoviestype.md)|<span data-ttu-id="20440-112">Películas de clasificación seleccionado para Australia.</span><span class="sxs-lookup"><span data-stu-id="20440-112">Movies rating selected for Australia.</span></span> <span data-ttu-id="20440-113">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="20440-113">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="20440-114">tvRating</span><span class="sxs-lookup"><span data-stu-id="20440-114">tvRating</span></span>|[<span data-ttu-id="20440-115">ratingAustraliaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="20440-115">ratingAustraliaTelevisionType</span></span>](../resources/intune-deviceconfig-ratingaustraliatelevisiontype.md)|<span data-ttu-id="20440-116">Clasificación de TV seleccionada para Australia.</span><span class="sxs-lookup"><span data-stu-id="20440-116">TV rating selected for Australia.</span></span> <span data-ttu-id="20440-117">Los valores posibles son: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove15AdultViolence`.</span><span class="sxs-lookup"><span data-stu-id="20440-117">Possible values are: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove15AdultViolence`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="20440-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="20440-118">Relationships</span></span>
<span data-ttu-id="20440-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="20440-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="20440-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="20440-120">JSON Representation</span></span>
<span data-ttu-id="20440-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="20440-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingAustralia"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingAustralia",
  "movieRating": "String",
  "tvRating": "String"
}
```



