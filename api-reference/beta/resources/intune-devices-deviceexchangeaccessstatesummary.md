---
title: Tipo de recurso deviceExchangeAccessStateSummary
description: Resumen del estado de acceso del dispositivo a Exchange
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 49afbb3383035711bc950a9a7226a354ae78f0e0
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920432"
---
# <a name="deviceexchangeaccessstatesummary-resource-type"></a><span data-ttu-id="b2d76-103">Tipo de recurso deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="b2d76-103">deviceExchangeAccessStateSummary resource type</span></span>

> <span data-ttu-id="b2d76-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b2d76-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b2d76-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b2d76-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b2d76-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b2d76-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b2d76-107">Resumen del estado de acceso del dispositivo a Exchange</span><span class="sxs-lookup"><span data-stu-id="b2d76-107">Device Exchange Access State summary</span></span>
## <a name="properties"></a><span data-ttu-id="b2d76-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2d76-108">Properties</span></span>
|<span data-ttu-id="b2d76-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b2d76-109">Property</span></span>|<span data-ttu-id="b2d76-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="b2d76-110">Type</span></span>|<span data-ttu-id="b2d76-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2d76-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b2d76-112">allowedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b2d76-112">allowedDeviceCount</span></span>|<span data-ttu-id="b2d76-113">Int32</span><span class="sxs-lookup"><span data-stu-id="b2d76-113">Int32</span></span>|<span data-ttu-id="b2d76-114">Número total de dispositivos con el estado de acceso de Exchange: Permitido.</span><span class="sxs-lookup"><span data-stu-id="b2d76-114">Total count of devices with Exchange Access State: Allowed.</span></span>|
|<span data-ttu-id="b2d76-115">blockedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b2d76-115">blockedDeviceCount</span></span>|<span data-ttu-id="b2d76-116">Int32</span><span class="sxs-lookup"><span data-stu-id="b2d76-116">Int32</span></span>|<span data-ttu-id="b2d76-117">Número total de dispositivos con el estado de acceso de Exchange: Bloqueado.</span><span class="sxs-lookup"><span data-stu-id="b2d76-117">Total count of devices with Exchange Access State: Blocked.</span></span>|
|<span data-ttu-id="b2d76-118">quarantinedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b2d76-118">quarantinedDeviceCount</span></span>|<span data-ttu-id="b2d76-119">Int32</span><span class="sxs-lookup"><span data-stu-id="b2d76-119">Int32</span></span>|<span data-ttu-id="b2d76-120">Número total de dispositivos con el estado de acceso de Exchange: En cuarentena.</span><span class="sxs-lookup"><span data-stu-id="b2d76-120">Total count of devices with Exchange Access State: Quarantined.</span></span>|
|<span data-ttu-id="b2d76-121">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b2d76-121">unknownDeviceCount</span></span>|<span data-ttu-id="b2d76-122">Int32</span><span class="sxs-lookup"><span data-stu-id="b2d76-122">Int32</span></span>|<span data-ttu-id="b2d76-123">Número total de dispositivos con el estado de acceso de Exchange: Desconocido.</span><span class="sxs-lookup"><span data-stu-id="b2d76-123">Total count of devices with Exchange Access State: Unknown.</span></span>|
|<span data-ttu-id="b2d76-124">unavailableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b2d76-124">unavailableDeviceCount</span></span>|<span data-ttu-id="b2d76-125">Int32</span><span class="sxs-lookup"><span data-stu-id="b2d76-125">Int32</span></span>|<span data-ttu-id="b2d76-126">Número total de dispositivos para los que no se puede encontrar el estado de acceso de Exchange.</span><span class="sxs-lookup"><span data-stu-id="b2d76-126">Total count of devices for which no Exchange Access State could be found.</span></span>|

## <a name="relationships"></a><span data-ttu-id="b2d76-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b2d76-127">Relationships</span></span>
<span data-ttu-id="b2d76-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="b2d76-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="b2d76-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b2d76-129">JSON Representation</span></span>
<span data-ttu-id="b2d76-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b2d76-130">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceExchangeAccessStateSummary",
  "allowedDeviceCount": 1024,
  "blockedDeviceCount": 1024,
  "quarantinedDeviceCount": 1024,
  "unknownDeviceCount": 1024,
  "unavailableDeviceCount": 1024
}
```





