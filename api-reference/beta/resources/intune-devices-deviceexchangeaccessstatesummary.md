---
title: Tipo de recurso deviceExchangeAccessStateSummary
description: Resumen del estado de acceso del dispositivo a Exchange
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b8ca08b026b8e1cdbac4bd0dc73331a9d5df80fc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889988"
---
# <a name="deviceexchangeaccessstatesummary-resource-type"></a><span data-ttu-id="59381-103">Tipo de recurso deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="59381-103">deviceExchangeAccessStateSummary resource type</span></span>

> <span data-ttu-id="59381-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="59381-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="59381-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="59381-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="59381-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="59381-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="59381-107">Resumen del estado de acceso del dispositivo a Exchange</span><span class="sxs-lookup"><span data-stu-id="59381-107">Device Exchange Access State summary</span></span>
## <a name="properties"></a><span data-ttu-id="59381-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="59381-108">Properties</span></span>
|<span data-ttu-id="59381-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59381-109">Property</span></span>|<span data-ttu-id="59381-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="59381-110">Type</span></span>|<span data-ttu-id="59381-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="59381-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="59381-112">allowedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="59381-112">allowedDeviceCount</span></span>|<span data-ttu-id="59381-113">Int32</span><span class="sxs-lookup"><span data-stu-id="59381-113">Int32</span></span>|<span data-ttu-id="59381-114">Número total de dispositivos con el estado de acceso de Exchange: Permitido.</span><span class="sxs-lookup"><span data-stu-id="59381-114">Total count of devices with Exchange Access State: Allowed.</span></span>|
|<span data-ttu-id="59381-115">blockedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="59381-115">blockedDeviceCount</span></span>|<span data-ttu-id="59381-116">Int32</span><span class="sxs-lookup"><span data-stu-id="59381-116">Int32</span></span>|<span data-ttu-id="59381-117">Número total de dispositivos con el estado de acceso de Exchange: Bloqueado.</span><span class="sxs-lookup"><span data-stu-id="59381-117">Total count of devices with Exchange Access State: Blocked.</span></span>|
|<span data-ttu-id="59381-118">quarantinedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="59381-118">quarantinedDeviceCount</span></span>|<span data-ttu-id="59381-119">Int32</span><span class="sxs-lookup"><span data-stu-id="59381-119">Int32</span></span>|<span data-ttu-id="59381-120">Número total de dispositivos con el estado de acceso de Exchange: En cuarentena.</span><span class="sxs-lookup"><span data-stu-id="59381-120">Total count of devices with Exchange Access State: Quarantined.</span></span>|
|<span data-ttu-id="59381-121">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="59381-121">unknownDeviceCount</span></span>|<span data-ttu-id="59381-122">Int32</span><span class="sxs-lookup"><span data-stu-id="59381-122">Int32</span></span>|<span data-ttu-id="59381-123">Número total de dispositivos con el estado de acceso de Exchange: Desconocido.</span><span class="sxs-lookup"><span data-stu-id="59381-123">Total count of devices with Exchange Access State: Unknown.</span></span>|
|<span data-ttu-id="59381-124">unavailableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="59381-124">unavailableDeviceCount</span></span>|<span data-ttu-id="59381-125">Int32</span><span class="sxs-lookup"><span data-stu-id="59381-125">Int32</span></span>|<span data-ttu-id="59381-126">Número total de dispositivos para los que no se puede encontrar el estado de acceso de Exchange.</span><span class="sxs-lookup"><span data-stu-id="59381-126">Total count of devices for which no Exchange Access State could be found.</span></span>|

## <a name="relationships"></a><span data-ttu-id="59381-127">Relaciones</span><span class="sxs-lookup"><span data-stu-id="59381-127">Relationships</span></span>
<span data-ttu-id="59381-128">Ninguna</span><span class="sxs-lookup"><span data-stu-id="59381-128">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="59381-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="59381-129">JSON Representation</span></span>
<span data-ttu-id="59381-130">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="59381-130">Here is a JSON representation of the resource.</span></span>
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





