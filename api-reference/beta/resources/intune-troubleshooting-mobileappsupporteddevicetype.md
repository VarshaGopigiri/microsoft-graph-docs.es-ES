---
title: tipo de recurso mobileAppSupportedDeviceType
description: Propiedades del dispositivo
ms.openlocfilehash: 7bea84a009d8940608c82bbb551c2d3c8be750ce
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085512"
---
# <a name="mobileappsupporteddevicetype-resource-type"></a><span data-ttu-id="04a5b-103">tipo de recurso mobileAppSupportedDeviceType</span><span class="sxs-lookup"><span data-stu-id="04a5b-103">mobileAppSupportedDeviceType resource type</span></span>

> <span data-ttu-id="04a5b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="04a5b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="04a5b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="04a5b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="04a5b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="04a5b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="04a5b-107">Propiedades del dispositivo</span><span class="sxs-lookup"><span data-stu-id="04a5b-107">Device properties</span></span>
## <a name="properties"></a><span data-ttu-id="04a5b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="04a5b-108">Properties</span></span>
|<span data-ttu-id="04a5b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="04a5b-109">Property</span></span>|<span data-ttu-id="04a5b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="04a5b-110">Type</span></span>|<span data-ttu-id="04a5b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="04a5b-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="04a5b-112">type</span><span class="sxs-lookup"><span data-stu-id="04a5b-112">type</span></span>|[<span data-ttu-id="04a5b-113">deviceType</span><span class="sxs-lookup"><span data-stu-id="04a5b-113">deviceType</span></span>](../resources/intune-shared-devicetype.md)|<span data-ttu-id="04a5b-114">Tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="04a5b-114">Device type.</span></span> <span data-ttu-id="04a5b-115">Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="04a5b-115">Possible values are: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise`, `blackberry`, `palm`, `unknown`.</span></span>|
|<span data-ttu-id="04a5b-116">minimumOperatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="04a5b-116">minimumOperatingSystemVersion</span></span>|<span data-ttu-id="04a5b-117">String</span><span class="sxs-lookup"><span data-stu-id="04a5b-117">String</span></span>|<span data-ttu-id="04a5b-118">Versión del sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="04a5b-118">Minimum OS version</span></span>|
|<span data-ttu-id="04a5b-119">maximumOperatingSystemVersion</span><span class="sxs-lookup"><span data-stu-id="04a5b-119">maximumOperatingSystemVersion</span></span>|<span data-ttu-id="04a5b-120">String</span><span class="sxs-lookup"><span data-stu-id="04a5b-120">String</span></span>|<span data-ttu-id="04a5b-121">Versión de sistema operativo máximo</span><span class="sxs-lookup"><span data-stu-id="04a5b-121">Maximum OS version</span></span>|

## <a name="relationships"></a><span data-ttu-id="04a5b-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="04a5b-122">Relationships</span></span>
<span data-ttu-id="04a5b-123">Ninguna</span><span class="sxs-lookup"><span data-stu-id="04a5b-123">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="04a5b-124">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="04a5b-124">JSON Representation</span></span>
<span data-ttu-id="04a5b-125">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="04a5b-125">Here is a JSON representation of the resource.</span></span>
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





