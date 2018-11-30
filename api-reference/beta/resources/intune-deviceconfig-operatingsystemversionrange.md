---
title: tipo de recurso operatingSystemVersionRange
description: Intervalo de versión del sistema operativo.
ms.openlocfilehash: af140bf2a5d889b66d45460465e47c466bb2160b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085201"
---
# <a name="operatingsystemversionrange-resource-type"></a><span data-ttu-id="d3921-103">tipo de recurso operatingSystemVersionRange</span><span class="sxs-lookup"><span data-stu-id="d3921-103">operatingSystemVersionRange resource type</span></span>

> <span data-ttu-id="d3921-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d3921-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d3921-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d3921-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d3921-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d3921-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d3921-107">Intervalo de versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d3921-107">Operating System version range.</span></span>
## <a name="properties"></a><span data-ttu-id="d3921-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d3921-108">Properties</span></span>
|<span data-ttu-id="d3921-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d3921-109">Property</span></span>|<span data-ttu-id="d3921-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d3921-110">Type</span></span>|<span data-ttu-id="d3921-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d3921-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d3921-112">description</span><span class="sxs-lookup"><span data-stu-id="d3921-112">description</span></span>|<span data-ttu-id="d3921-113">String</span><span class="sxs-lookup"><span data-stu-id="d3921-113">String</span></span>|<span data-ttu-id="d3921-114">La descripción de este intervalo (por ejemplo, válido 1702 compilaciones)</span><span class="sxs-lookup"><span data-stu-id="d3921-114">The description of this range (e.g. Valid 1702 builds)</span></span>|
|<span data-ttu-id="d3921-115">lowestVersion</span><span class="sxs-lookup"><span data-stu-id="d3921-115">lowestVersion</span></span>|<span data-ttu-id="d3921-116">String</span><span class="sxs-lookup"><span data-stu-id="d3921-116">String</span></span>|<span data-ttu-id="d3921-117">La más baja inclusive versión que contiene este intervalo.</span><span class="sxs-lookup"><span data-stu-id="d3921-117">The lowest inclusive version that this range contains.</span></span>|
|<span data-ttu-id="d3921-118">highestVersion</span><span class="sxs-lookup"><span data-stu-id="d3921-118">highestVersion</span></span>|<span data-ttu-id="d3921-119">String</span><span class="sxs-lookup"><span data-stu-id="d3921-119">String</span></span>|<span data-ttu-id="d3921-120">La versión inclusive más alta que contiene este intervalo.</span><span class="sxs-lookup"><span data-stu-id="d3921-120">The highest inclusive version that this range contains.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d3921-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d3921-121">Relationships</span></span>
<span data-ttu-id="d3921-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d3921-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d3921-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d3921-123">JSON Representation</span></span>
<span data-ttu-id="d3921-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d3921-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.operatingSystemVersionRange"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.operatingSystemVersionRange",
  "description": "String",
  "lowestVersion": "String",
  "highestVersion": "String"
}
```





