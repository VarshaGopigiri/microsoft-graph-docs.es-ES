---
title: Tipo de recurso deviceExchangeAccessStateSummary
description: Resumen del estado de acceso del dispositivo a Exchange
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 10eb3738e14e8239f92f8578d01b9d4888b06b24
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27829823"
---
# <a name="deviceexchangeaccessstatesummary-resource-type"></a><span data-ttu-id="efd92-103">Tipo de recurso deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="efd92-103">deviceExchangeAccessStateSummary resource type</span></span>

> <span data-ttu-id="efd92-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="efd92-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="efd92-105">Resumen del estado de acceso del dispositivo a Exchange</span><span class="sxs-lookup"><span data-stu-id="efd92-105">Device Exchange Access State summary</span></span>
## <a name="properties"></a><span data-ttu-id="efd92-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="efd92-106">Properties</span></span>
|<span data-ttu-id="efd92-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="efd92-107">Property</span></span>|<span data-ttu-id="efd92-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="efd92-108">Type</span></span>|<span data-ttu-id="efd92-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="efd92-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="efd92-110">allowedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="efd92-110">allowedDeviceCount</span></span>|<span data-ttu-id="efd92-111">Int32</span><span class="sxs-lookup"><span data-stu-id="efd92-111">Int32</span></span>|<span data-ttu-id="efd92-112">Número total de dispositivos con el estado de acceso de Exchange: Permitido.</span><span class="sxs-lookup"><span data-stu-id="efd92-112">Total count of devices with Exchange Access State: Allowed.</span></span>|
|<span data-ttu-id="efd92-113">blockedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="efd92-113">blockedDeviceCount</span></span>|<span data-ttu-id="efd92-114">Int32</span><span class="sxs-lookup"><span data-stu-id="efd92-114">Int32</span></span>|<span data-ttu-id="efd92-115">Número total de dispositivos con el estado de acceso de Exchange: Bloqueado.</span><span class="sxs-lookup"><span data-stu-id="efd92-115">Total count of devices with Exchange Access State: Blocked.</span></span>|
|<span data-ttu-id="efd92-116">quarantinedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="efd92-116">quarantinedDeviceCount</span></span>|<span data-ttu-id="efd92-117">Int32</span><span class="sxs-lookup"><span data-stu-id="efd92-117">Int32</span></span>|<span data-ttu-id="efd92-118">Número total de dispositivos con el estado de acceso de Exchange: En cuarentena.</span><span class="sxs-lookup"><span data-stu-id="efd92-118">Total count of devices with Exchange Access State: Quarantined.</span></span>|
|<span data-ttu-id="efd92-119">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="efd92-119">unknownDeviceCount</span></span>|<span data-ttu-id="efd92-120">Int32</span><span class="sxs-lookup"><span data-stu-id="efd92-120">Int32</span></span>|<span data-ttu-id="efd92-121">Número total de dispositivos con el estado de acceso de Exchange: Desconocido.</span><span class="sxs-lookup"><span data-stu-id="efd92-121">Total count of devices with Exchange Access State: Unknown.</span></span>|
|<span data-ttu-id="efd92-122">unavailableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="efd92-122">unavailableDeviceCount</span></span>|<span data-ttu-id="efd92-123">Int32</span><span class="sxs-lookup"><span data-stu-id="efd92-123">Int32</span></span>|<span data-ttu-id="efd92-124">Número total de dispositivos para los que no se puede encontrar el estado de acceso de Exchange.</span><span class="sxs-lookup"><span data-stu-id="efd92-124">Total count of devices for which no Exchange Access State could be found.</span></span>|

## <a name="relationships"></a><span data-ttu-id="efd92-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="efd92-125">Relationships</span></span>
<span data-ttu-id="efd92-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="efd92-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="efd92-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="efd92-127">JSON Representation</span></span>
<span data-ttu-id="efd92-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="efd92-128">Here is a JSON representation of the resource.</span></span>
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



