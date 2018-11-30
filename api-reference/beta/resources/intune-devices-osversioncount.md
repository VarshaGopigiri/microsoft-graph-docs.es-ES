---
title: tipo de recurso osVersionCount
description: Recuento de dispositivos con malware para cada versión del sistema operativo
ms.openlocfilehash: 7892761bd0dc20f09ab2deb47549aeb157e25644
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089234"
---
# <a name="osversioncount-resource-type"></a><span data-ttu-id="41134-103">tipo de recurso osVersionCount</span><span class="sxs-lookup"><span data-stu-id="41134-103">osVersionCount resource type</span></span>

> <span data-ttu-id="41134-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="41134-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="41134-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="41134-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="41134-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="41134-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="41134-107">Recuento de dispositivos con malware para cada versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="41134-107">Count of devices with malware for each OS version</span></span>
## <a name="properties"></a><span data-ttu-id="41134-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41134-108">Properties</span></span>
|<span data-ttu-id="41134-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41134-109">Property</span></span>|<span data-ttu-id="41134-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="41134-110">Type</span></span>|<span data-ttu-id="41134-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="41134-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="41134-112">osVersion</span><span class="sxs-lookup"><span data-stu-id="41134-112">osVersion</span></span>|<span data-ttu-id="41134-113">String</span><span class="sxs-lookup"><span data-stu-id="41134-113">String</span></span>|<span data-ttu-id="41134-114">Versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="41134-114">OS version</span></span>|
|<span data-ttu-id="41134-115">deviceCount</span><span class="sxs-lookup"><span data-stu-id="41134-115">deviceCount</span></span>|<span data-ttu-id="41134-116">Int32</span><span class="sxs-lookup"><span data-stu-id="41134-116">Int32</span></span>|<span data-ttu-id="41134-117">Recuento de dispositivos con malware para la versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="41134-117">Count of devices with malware for the OS version</span></span>|
|<span data-ttu-id="41134-118">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="41134-118">lastUpdateDateTime</span></span>|<span data-ttu-id="41134-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="41134-119">DateTimeOffset</span></span>|<span data-ttu-id="41134-120">Recuento de la marca de hora de la última actualización del dispositivo en UTC</span><span class="sxs-lookup"><span data-stu-id="41134-120">The Timestamp of the last update for the device count in UTC</span></span>|

## <a name="relationships"></a><span data-ttu-id="41134-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="41134-121">Relationships</span></span>
<span data-ttu-id="41134-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="41134-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="41134-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="41134-123">JSON Representation</span></span>
<span data-ttu-id="41134-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="41134-124">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.osVersionCount"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.osVersionCount",
  "osVersion": "String",
  "deviceCount": 1024,
  "lastUpdateDateTime": "String (timestamp)"
}
```





