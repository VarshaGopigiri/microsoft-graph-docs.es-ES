---
title: Tipo de recurso mediaContentRatingUnitedStates
description: Todavía no documentado
ms.openlocfilehash: d62d656c4fbd8744560ab191786d71b732fe6c21
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083313"
---
# <a name="mediacontentratingunitedstates-resource-type"></a><span data-ttu-id="4263f-103">Tipo de recurso mediaContentRatingUnitedStates</span><span class="sxs-lookup"><span data-stu-id="4263f-103">mediaContentRatingUnitedStates resource type</span></span>

> <span data-ttu-id="4263f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4263f-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4263f-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4263f-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4263f-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4263f-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4263f-107">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4263f-107">Not yet documented</span></span>
## <a name="properties"></a><span data-ttu-id="4263f-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4263f-108">Properties</span></span>
|<span data-ttu-id="4263f-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4263f-109">Property</span></span>|<span data-ttu-id="4263f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="4263f-110">Type</span></span>|<span data-ttu-id="4263f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4263f-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4263f-112">movieRating</span><span class="sxs-lookup"><span data-stu-id="4263f-112">movieRating</span></span>|[<span data-ttu-id="4263f-113">ratingUnitedStatesMoviesType</span><span class="sxs-lookup"><span data-stu-id="4263f-113">ratingUnitedStatesMoviesType</span></span>](../resources/intune-deviceconfig-ratingunitedstatesmoviestype.md)|<span data-ttu-id="4263f-114">Películas de clasificación seleccionado para Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="4263f-114">Movies rating selected for United States.</span></span> <span data-ttu-id="4263f-115">Los valores posibles son: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `parentalGuidance13`, `restricted` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="4263f-115">Possible values are: `allAllowed`, `allBlocked`, `general`, `parentalGuidance`, `parentalGuidance13`, `restricted`, `adults`.</span></span>|
|<span data-ttu-id="4263f-116">tvRating</span><span class="sxs-lookup"><span data-stu-id="4263f-116">tvRating</span></span>|[<span data-ttu-id="4263f-117">ratingUnitedStatesTelevisionType</span><span class="sxs-lookup"><span data-stu-id="4263f-117">ratingUnitedStatesTelevisionType</span></span>](../resources/intune-deviceconfig-ratingunitedstatestelevisiontype.md)|<span data-ttu-id="4263f-118">Clasificación de TV seleccionada para Estados Unidos.</span><span class="sxs-lookup"><span data-stu-id="4263f-118">TV rating selected for United States.</span></span> <span data-ttu-id="4263f-119">Los valores posibles son: `allAllowed`, `allBlocked`, `childrenAll`, `childrenAbove7`, `general`, `parentalGuidance`, `childrenAbove14` y `adults`.</span><span class="sxs-lookup"><span data-stu-id="4263f-119">Possible values are: `allAllowed`, `allBlocked`, `childrenAll`, `childrenAbove7`, `general`, `parentalGuidance`, `childrenAbove14`, `adults`.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4263f-120">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4263f-120">Relationships</span></span>
<span data-ttu-id="4263f-121">Ninguna</span><span class="sxs-lookup"><span data-stu-id="4263f-121">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="4263f-122">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4263f-122">JSON Representation</span></span>
<span data-ttu-id="4263f-123">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4263f-123">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mediaContentRatingUnitedStates",
  "movieRating": "String",
  "tvRating": "String"
}
```





