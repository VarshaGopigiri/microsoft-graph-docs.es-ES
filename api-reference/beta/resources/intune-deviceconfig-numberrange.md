---
title: tipo de recurso numberRange
description: Definición del intervalo de números.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 9dc10caaa125144944cf3e6c52c65e58f9d57975
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977412"
---
# <a name="numberrange-resource-type"></a><span data-ttu-id="924cf-103">tipo de recurso numberRange</span><span class="sxs-lookup"><span data-stu-id="924cf-103">numberRange resource type</span></span>

> <span data-ttu-id="924cf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="924cf-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="924cf-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="924cf-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="924cf-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="924cf-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="924cf-107">Definición del intervalo de números.</span><span class="sxs-lookup"><span data-stu-id="924cf-107">Number Range definition.</span></span>
## <a name="properties"></a><span data-ttu-id="924cf-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="924cf-108">Properties</span></span>
|<span data-ttu-id="924cf-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="924cf-109">Property</span></span>|<span data-ttu-id="924cf-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="924cf-110">Type</span></span>|<span data-ttu-id="924cf-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="924cf-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="924cf-112">lowerNumber</span><span class="sxs-lookup"><span data-stu-id="924cf-112">lowerNumber</span></span>|<span data-ttu-id="924cf-113">Int32</span><span class="sxs-lookup"><span data-stu-id="924cf-113">Int32</span></span>|<span data-ttu-id="924cf-114">Número inferior.</span><span class="sxs-lookup"><span data-stu-id="924cf-114">Lower number.</span></span>|
|<span data-ttu-id="924cf-115">upperNumber</span><span class="sxs-lookup"><span data-stu-id="924cf-115">upperNumber</span></span>|<span data-ttu-id="924cf-116">Int32</span><span class="sxs-lookup"><span data-stu-id="924cf-116">Int32</span></span>|<span data-ttu-id="924cf-117">Número superior.</span><span class="sxs-lookup"><span data-stu-id="924cf-117">Upper number.</span></span>|

## <a name="relationships"></a><span data-ttu-id="924cf-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="924cf-118">Relationships</span></span>
<span data-ttu-id="924cf-119">Ninguna</span><span class="sxs-lookup"><span data-stu-id="924cf-119">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="924cf-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="924cf-120">JSON Representation</span></span>
<span data-ttu-id="924cf-121">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="924cf-121">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.numberRange"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.numberRange",
  "lowerNumber": 1024,
  "upperNumber": 1024
}
```





