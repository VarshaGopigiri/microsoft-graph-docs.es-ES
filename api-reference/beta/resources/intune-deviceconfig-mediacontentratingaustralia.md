---
title: Tipo de recurso mediaContentRatingAustralia
description: Todavía no documentado
ms.openlocfilehash: ff8cb3e6bc389e7a99b84e9aa248871b5830a7e9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088749"
---
# <a name="mediacontentratingaustralia-resource-type"></a><span data-ttu-id="8db1d-103">Tipo de recurso mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="8db1d-103">mediaContentRatingAustralia resource type</span></span>

> <span data-ttu-id="8db1d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8db1d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8db1d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8db1d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8db1d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8db1d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8db1d-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="8db1d-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="8db1d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8db1d-108">Properties</span></span>
|<span data-ttu-id="8db1d-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8db1d-109">Property</span></span>|<span data-ttu-id="8db1d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8db1d-110">Type</span></span>|<span data-ttu-id="8db1d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8db1d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8db1d-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="8db1d-112">movieRating</span></span>|[<span data-ttu-id="8db1d-113">ratingAustraliaMoviesType</span><span class="sxs-lookup"><span data-stu-id="8db1d-113">ratingAustraliaMoviesType</span></span>](../resources/intune-deviceconfig-ratingaustraliamoviestype.md)|<span data-ttu-id="8db1d-114">Películas de clasificación seleccionado para Australia.</span><span class="sxs-lookup"><span data-stu-id="8db1d-114">Movies rating selected for Australia.</span></span> <span data-ttu-id="8db1d-115">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove18`.</span><span class="sxs-lookup"><span data-stu-id="8db1d-115">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove18`.</span></span>|
|<span data-ttu-id="8db1d-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="8db1d-116">tvRating</span></span>|[<span data-ttu-id="8db1d-117">ratingAustraliaTelevisionType</span><span class="sxs-lookup"><span data-stu-id="8db1d-117">ratingAustraliaTelevisionType</span></span>](../resources/intune-deviceconfig-ratingaustraliatelevisiontype.md)|<span data-ttu-id="8db1d-118">Clasificación de TV seleccionada para Australia.</span><span class="sxs-lookup"><span data-stu-id="8db1d-118">TV rating selected for Australia.</span></span> <span data-ttu-id="8db1d-119">Los valores posibles son: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15` y `agesAbove15AdultViolence`.</span><span class="sxs-lookup"><span data-stu-id="8db1d-119">Possible values are: `allAllowed`, `allBlocked`, `preschoolers`, `children`, `general`, `parentalGuidance`, `mature`, `agesAbove15`, `agesAbove15AdultViolence`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="8db1d-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8db1d-120">Relationships</span></span>
<span data-ttu-id="8db1d-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="8db1d-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="8db1d-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8db1d-122">JSON Representation</span></span>
<span data-ttu-id="8db1d-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8db1d-123">Here is a JSON representation of the resource.</span></span>
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





