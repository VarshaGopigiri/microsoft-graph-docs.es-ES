---
title: tipo de recurso mobileAppSupportedDeviceType
description: Propiedades del dispositivo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b1b757e9c621f77d1a26251345ee6751eca2ca7c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27980226"
---
# <a name="mobileappsupporteddevicetype-resource-type"></a><span data-ttu-id="077da-103">tipo de recurso mobileAppSupportedDeviceType</span><span class="sxs-lookup"><span data-stu-id="077da-103">mobileAppSupportedDeviceType resource type</span></span>

> <span data-ttu-id="077da-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="077da-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="077da-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="077da-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="077da-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="077da-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="077da-107">Propiedades del dispositivo</span><span class="sxs-lookup"><span data-stu-id="077da-107">Device properties</span></span>
## <a name="properties"></a><span data-ttu-id="077da-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="077da-108">Properties</span></span>
|<span data-ttu-id="077da-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="077da-109">Property</span></span>|<span data-ttu-id="077da-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="077da-110">Type</span></span>|<span data-ttu-id="077da-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="077da-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="077da-112">type</span><span class="sxs-lookup"><span data-stu-id="077da-112">type</span></span>|[<span data-ttu-id="077da-113">deviceType</span><span class="sxs-lookup"><span data-stu-id="077da-113">deviceType</span></span>](../resources/intune-shared-devicetype.md)|<span data-ttu-id="077da-114">Tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="077da-114">Device type.</span></span> <span data-ttu-id="077da-115">Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="077da-115">Possible values are: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise`, `blackberry`, `palm`, `unknown`.</span></span>|
|<span data-ttu-id="077da-116">minimumOperatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="077da-116">minimumOperatingSystemVersion</span></span>|<span data-ttu-id="077da-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="077da-117">String</span></span>|<span data-ttu-id="077da-118">Versión del sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="077da-118">Minimum OS version</span></span>|
|<span data-ttu-id="077da-119">maximumOperatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="077da-119">maximumOperatingSystemVersion</span></span>|<span data-ttu-id="077da-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="077da-120">String</span></span>|<span data-ttu-id="077da-121">Versión de sistema operativo máximo</span><span class="sxs-lookup"><span data-stu-id="077da-121">Maximum OS version</span></span>|

## <a name="relationships"></a><span data-ttu-id="077da-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="077da-122">Relationships</span></span>
<span data-ttu-id="077da-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="077da-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="077da-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="077da-124">JSON Representation</span></span>
<span data-ttu-id="077da-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="077da-125">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.mobileAppSupportedDeviceType"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppSupportedDeviceType",
  "type": "String",
  "minimumOperatingSystemVersion": "String",
  "maximumOperatingSystemVersion": "String"
}
```





