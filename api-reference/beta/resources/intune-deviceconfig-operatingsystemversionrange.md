---
title: tipo de recurso operatingSystemVersionRange
description: Intervalo de versión del sistema operativo.
author: tfitzmac
ms.openlocfilehash: b853e71b2d8f66d24122afb51cea97fc6a8f8d7e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27331167"
---
# <a name="operatingsystemversionrange-resource-type"></a><span data-ttu-id="d024d-103">tipo de recurso operatingSystemVersionRange</span><span class="sxs-lookup"><span data-stu-id="d024d-103">operatingSystemVersionRange resource type</span></span>

> <span data-ttu-id="d024d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d024d-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d024d-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d024d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d024d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d024d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d024d-107">Intervalo de versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="d024d-107">Operating System version range.</span></span>
## <a name="properties"></a><span data-ttu-id="d024d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d024d-108">Properties</span></span>
|<span data-ttu-id="d024d-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d024d-109">Property</span></span>|<span data-ttu-id="d024d-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d024d-110">Type</span></span>|<span data-ttu-id="d024d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d024d-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d024d-112">description</span><span class="sxs-lookup"><span data-stu-id="d024d-112">description</span></span>|<span data-ttu-id="d024d-113">String</span><span class="sxs-lookup"><span data-stu-id="d024d-113">String</span></span>|<span data-ttu-id="d024d-114">La descripción de este intervalo (por ejemplo, válido 1702 compilaciones)</span><span class="sxs-lookup"><span data-stu-id="d024d-114">The description of this range (e.g. Valid 1702 builds)</span></span>|
|<span data-ttu-id="d024d-115">lowestVersion</span><span class="sxs-lookup"><span data-stu-id="d024d-115">lowestVersion</span></span>|<span data-ttu-id="d024d-116">String</span><span class="sxs-lookup"><span data-stu-id="d024d-116">String</span></span>|<span data-ttu-id="d024d-117">La más baja inclusive versión que contiene este intervalo.</span><span class="sxs-lookup"><span data-stu-id="d024d-117">The lowest inclusive version that this range contains.</span></span>|
|<span data-ttu-id="d024d-118">highestVersion</span><span class="sxs-lookup"><span data-stu-id="d024d-118">highestVersion</span></span>|<span data-ttu-id="d024d-119">String</span><span class="sxs-lookup"><span data-stu-id="d024d-119">String</span></span>|<span data-ttu-id="d024d-120">La versión inclusive más alta que contiene este intervalo.</span><span class="sxs-lookup"><span data-stu-id="d024d-120">The highest inclusive version that this range contains.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d024d-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d024d-121">Relationships</span></span>
<span data-ttu-id="d024d-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d024d-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d024d-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d024d-123">JSON Representation</span></span>
<span data-ttu-id="d024d-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d024d-124">Here is a JSON representation of the resource.</span></span>
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





