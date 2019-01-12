---
title: tipo de recurso osVersionCount
description: Recuento de dispositivos con malware para cada versión del sistema operativo
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: de841e679ede22492d26f2a1587e775179c45761
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911843"
---
# <a name="osversioncount-resource-type"></a><span data-ttu-id="53a14-103">tipo de recurso osVersionCount</span><span class="sxs-lookup"><span data-stu-id="53a14-103">osVersionCount resource type</span></span>

> <span data-ttu-id="53a14-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="53a14-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="53a14-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="53a14-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="53a14-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="53a14-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="53a14-107">Recuento de dispositivos con malware para cada versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="53a14-107">Count of devices with malware for each OS version</span></span>
## <a name="properties"></a><span data-ttu-id="53a14-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="53a14-108">Properties</span></span>
|<span data-ttu-id="53a14-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="53a14-109">Property</span></span>|<span data-ttu-id="53a14-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="53a14-110">Type</span></span>|<span data-ttu-id="53a14-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="53a14-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="53a14-112">osVersion</span><span class="sxs-lookup"><span data-stu-id="53a14-112">osVersion</span></span>|<span data-ttu-id="53a14-113">Cadena</span><span class="sxs-lookup"><span data-stu-id="53a14-113">String</span></span>|<span data-ttu-id="53a14-114">Versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="53a14-114">OS version</span></span>|
|<span data-ttu-id="53a14-115">deviceCount</span><span class="sxs-lookup"><span data-stu-id="53a14-115">deviceCount</span></span>|<span data-ttu-id="53a14-116">Int32</span><span class="sxs-lookup"><span data-stu-id="53a14-116">Int32</span></span>|<span data-ttu-id="53a14-117">Recuento de dispositivos con malware para la versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="53a14-117">Count of devices with malware for the OS version</span></span>|
|<span data-ttu-id="53a14-118">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="53a14-118">lastUpdateDateTime</span></span>|<span data-ttu-id="53a14-119">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="53a14-119">DateTimeOffset</span></span>|<span data-ttu-id="53a14-120">Recuento de la marca de hora de la última actualización del dispositivo en UTC</span><span class="sxs-lookup"><span data-stu-id="53a14-120">The Timestamp of the last update for the device count in UTC</span></span>|

## <a name="relationships"></a><span data-ttu-id="53a14-121">Relaciones</span><span class="sxs-lookup"><span data-stu-id="53a14-121">Relationships</span></span>
<span data-ttu-id="53a14-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="53a14-122">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="53a14-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="53a14-123">JSON Representation</span></span>
<span data-ttu-id="53a14-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="53a14-124">Here is a JSON representation of the resource.</span></span>
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





