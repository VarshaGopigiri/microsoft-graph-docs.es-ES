---
title: Tipo de recurso deviceExchangeAccessStateSummary
description: Resumen del estado de acceso del dispositivo a Exchange
author: tfitzmac
ms.openlocfilehash: dd2784078e8b44b1a02cb5a0013c1e38804912c0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301746"
---
# <a name="deviceexchangeaccessstatesummary-resource-type"></a><span data-ttu-id="9a3b6-103">Tipo de recurso deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="9a3b6-103">deviceExchangeAccessStateSummary resource type</span></span>

> <span data-ttu-id="9a3b6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9a3b6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9a3b6-105">Resumen del estado de acceso del dispositivo a Exchange</span><span class="sxs-lookup"><span data-stu-id="9a3b6-105">Device Exchange Access State summary</span></span>
## <a name="properties"></a><span data-ttu-id="9a3b6-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a3b6-106">Properties</span></span>
|<span data-ttu-id="9a3b6-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9a3b6-107">Property</span></span>|<span data-ttu-id="9a3b6-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a3b6-108">Type</span></span>|<span data-ttu-id="9a3b6-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a3b6-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9a3b6-110">allowedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9a3b6-110">allowedDeviceCount</span></span>|<span data-ttu-id="9a3b6-111">Int32</span><span class="sxs-lookup"><span data-stu-id="9a3b6-111">Int32</span></span>|<span data-ttu-id="9a3b6-112">Número total de dispositivos con el estado de acceso de Exchange: Permitido.</span><span class="sxs-lookup"><span data-stu-id="9a3b6-112">Total count of devices with Exchange Access State: Allowed.</span></span>|
|<span data-ttu-id="9a3b6-113">blockedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9a3b6-113">blockedDeviceCount</span></span>|<span data-ttu-id="9a3b6-114">Int32</span><span class="sxs-lookup"><span data-stu-id="9a3b6-114">Int32</span></span>|<span data-ttu-id="9a3b6-115">Número total de dispositivos con el estado de acceso de Exchange: Bloqueado.</span><span class="sxs-lookup"><span data-stu-id="9a3b6-115">Total count of devices with Exchange Access State: Blocked.</span></span>|
|<span data-ttu-id="9a3b6-116">quarantinedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9a3b6-116">quarantinedDeviceCount</span></span>|<span data-ttu-id="9a3b6-117">Int32</span><span class="sxs-lookup"><span data-stu-id="9a3b6-117">Int32</span></span>|<span data-ttu-id="9a3b6-118">Número total de dispositivos con el estado de acceso de Exchange: En cuarentena.</span><span class="sxs-lookup"><span data-stu-id="9a3b6-118">Total count of devices with Exchange Access State: Quarantined.</span></span>|
|<span data-ttu-id="9a3b6-119">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9a3b6-119">unknownDeviceCount</span></span>|<span data-ttu-id="9a3b6-120">Int32</span><span class="sxs-lookup"><span data-stu-id="9a3b6-120">Int32</span></span>|<span data-ttu-id="9a3b6-121">Número total de dispositivos con el estado de acceso de Exchange: Desconocido.</span><span class="sxs-lookup"><span data-stu-id="9a3b6-121">Total count of devices with Exchange Access State: Unknown.</span></span>|
|<span data-ttu-id="9a3b6-122">unavailableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9a3b6-122">unavailableDeviceCount</span></span>|<span data-ttu-id="9a3b6-123">Int32</span><span class="sxs-lookup"><span data-stu-id="9a3b6-123">Int32</span></span>|<span data-ttu-id="9a3b6-124">Número total de dispositivos para los que no se puede encontrar el estado de acceso de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9a3b6-124">Total count of devices for which no Exchange Access State could be found.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9a3b6-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9a3b6-125">Relationships</span></span>
<span data-ttu-id="9a3b6-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="9a3b6-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="9a3b6-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9a3b6-127">JSON Representation</span></span>
<span data-ttu-id="9a3b6-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9a3b6-128">Here is a JSON representation of the resource.</span></span>
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



