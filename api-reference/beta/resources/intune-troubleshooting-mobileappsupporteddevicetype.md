---
title: tipo de recurso mobileAppSupportedDeviceType
description: Propiedades del dispositivo
author: tfitzmac
ms.openlocfilehash: 5ec7d2b1e8340b73ea184dda15d842973f0fab2c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27314423"
---
# <a name="mobileappsupporteddevicetype-resource-type"></a><span data-ttu-id="d20ed-103">tipo de recurso mobileAppSupportedDeviceType</span><span class="sxs-lookup"><span data-stu-id="d20ed-103">mobileAppSupportedDeviceType resource type</span></span>

> <span data-ttu-id="d20ed-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d20ed-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d20ed-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d20ed-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d20ed-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d20ed-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d20ed-107">Propiedades del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d20ed-107">Device properties</span></span>
## <a name="properties"></a><span data-ttu-id="d20ed-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d20ed-108">Properties</span></span>
|<span data-ttu-id="d20ed-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d20ed-109">Property</span></span>|<span data-ttu-id="d20ed-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d20ed-110">Type</span></span>|<span data-ttu-id="d20ed-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d20ed-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d20ed-112">type</span><span class="sxs-lookup"><span data-stu-id="d20ed-112">type</span></span>|[<span data-ttu-id="d20ed-113">deviceType</span><span class="sxs-lookup"><span data-stu-id="d20ed-113">deviceType</span></span>](../resources/intune-shared-devicetype.md)|<span data-ttu-id="d20ed-114">Tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d20ed-114">Device type.</span></span> <span data-ttu-id="d20ed-115">Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="d20ed-115">Possible values are: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise`, `blackberry`, `palm`, `unknown`.</span></span>|
|<span data-ttu-id="d20ed-116">minimumOperatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="d20ed-116">minimumOperatingSystemVersion</span></span>|<span data-ttu-id="d20ed-117">String</span><span class="sxs-lookup"><span data-stu-id="d20ed-117">String</span></span>|<span data-ttu-id="d20ed-118">Versión del sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="d20ed-118">Minimum OS version</span></span>|
|<span data-ttu-id="d20ed-119">maximumOperatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="d20ed-119">maximumOperatingSystemVersion</span></span>|<span data-ttu-id="d20ed-120">String</span><span class="sxs-lookup"><span data-stu-id="d20ed-120">String</span></span>|<span data-ttu-id="d20ed-121">Versión de sistema operativo máximo</span><span class="sxs-lookup"><span data-stu-id="d20ed-121">Maximum OS version</span></span>|

## <a name="relationships"></a><span data-ttu-id="d20ed-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d20ed-122">Relationships</span></span>
<span data-ttu-id="d20ed-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d20ed-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d20ed-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d20ed-124">JSON Representation</span></span>
<span data-ttu-id="d20ed-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d20ed-125">Here is a JSON representation of the resource.</span></span>
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





