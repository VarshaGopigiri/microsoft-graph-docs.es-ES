---
title: Tipo de recurso deviceExchangeAccessStateSummary
description: Resumen del estado de acceso del dispositivo a Exchange
ms.openlocfilehash: 0210a01fe522a5f8bab38d473d866aef176df3b4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031626"
---
# <a name="deviceexchangeaccessstatesummary-resource-type"></a><span data-ttu-id="38340-103">Tipo de recurso deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="38340-103">deviceExchangeAccessStateSummary resource type</span></span>

> <span data-ttu-id="38340-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="38340-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="38340-105">Resumen del estado de acceso del dispositivo a Exchange</span><span class="sxs-lookup"><span data-stu-id="38340-105">Device Exchange Access State summary</span></span>
## <a name="properties"></a><span data-ttu-id="38340-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38340-106">Properties</span></span>
|<span data-ttu-id="38340-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38340-107">Property</span></span>|<span data-ttu-id="38340-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="38340-108">Type</span></span>|<span data-ttu-id="38340-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="38340-109">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="38340-110">allowedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38340-110">allowedDeviceCount</span></span>|<span data-ttu-id="38340-111">Int32</span><span class="sxs-lookup"><span data-stu-id="38340-111">Int32</span></span>|<span data-ttu-id="38340-112">Número total de dispositivos con el estado de acceso de Exchange: Permitido.</span><span class="sxs-lookup"><span data-stu-id="38340-112">Total count of devices with Exchange Access State: Allowed.</span></span>|
|<span data-ttu-id="38340-113">blockedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38340-113">blockedDeviceCount</span></span>|<span data-ttu-id="38340-114">Int32</span><span class="sxs-lookup"><span data-stu-id="38340-114">Int32</span></span>|<span data-ttu-id="38340-115">Número total de dispositivos con el estado de acceso de Exchange: Bloqueado.</span><span class="sxs-lookup"><span data-stu-id="38340-115">Total count of devices with Exchange Access State: Blocked.</span></span>|
|<span data-ttu-id="38340-116">quarantinedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38340-116">quarantinedDeviceCount</span></span>|<span data-ttu-id="38340-117">Int32</span><span class="sxs-lookup"><span data-stu-id="38340-117">Int32</span></span>|<span data-ttu-id="38340-118">Número total de dispositivos con el estado de acceso de Exchange: En cuarentena.</span><span class="sxs-lookup"><span data-stu-id="38340-118">Total count of devices with Exchange Access State: Quarantined.</span></span>|
|<span data-ttu-id="38340-119">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38340-119">unknownDeviceCount</span></span>|<span data-ttu-id="38340-120">Int32</span><span class="sxs-lookup"><span data-stu-id="38340-120">Int32</span></span>|<span data-ttu-id="38340-121">Número total de dispositivos con el estado de acceso de Exchange: Desconocido.</span><span class="sxs-lookup"><span data-stu-id="38340-121">Total count of devices with Exchange Access State: Unknown.</span></span>|
|<span data-ttu-id="38340-122">unavailableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38340-122">unavailableDeviceCount</span></span>|<span data-ttu-id="38340-123">Int32</span><span class="sxs-lookup"><span data-stu-id="38340-123">Int32</span></span>|<span data-ttu-id="38340-124">Número total de dispositivos para los que no se puede encontrar el estado de acceso de Exchange.</span><span class="sxs-lookup"><span data-stu-id="38340-124">Total count of devices for which no Exchange Access State could be found.</span></span>|

## <a name="relationships"></a><span data-ttu-id="38340-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="38340-125">Relationships</span></span>
<span data-ttu-id="38340-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="38340-126">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="38340-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="38340-127">JSON Representation</span></span>
<span data-ttu-id="38340-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="38340-128">Here is a JSON representation of the resource.</span></span>
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



