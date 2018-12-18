---
title: tipo de recurso deviceProtectionOverview
description: Información de hardware de un dispositivo determinado.
author: tfitzmac
ms.openlocfilehash: e705324bfc611117657ec629f8770e76c69be28d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27317055"
---
# <a name="deviceprotectionoverview-resource-type"></a><span data-ttu-id="66903-103">tipo de recurso deviceProtectionOverview</span><span class="sxs-lookup"><span data-stu-id="66903-103">deviceProtectionOverview resource type</span></span>

> <span data-ttu-id="66903-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="66903-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="66903-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="66903-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="66903-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="66903-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="66903-107">Información de hardware de un dispositivo determinado.</span><span class="sxs-lookup"><span data-stu-id="66903-107">Hardware information of a given device.</span></span>
## <a name="properties"></a><span data-ttu-id="66903-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="66903-108">Properties</span></span>
|<span data-ttu-id="66903-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="66903-109">Property</span></span>|<span data-ttu-id="66903-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="66903-110">Type</span></span>|<span data-ttu-id="66903-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="66903-111">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="66903-112">totalReportedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="66903-112">totalReportedDeviceCount</span></span>|<span data-ttu-id="66903-113">Int32</span><span class="sxs-lookup"><span data-stu-id="66903-113">Int32</span></span>|<span data-ttu-id="66903-114">Recuento total del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66903-114">Total device count.</span></span>|
|<span data-ttu-id="66903-115">inactiveThreatAgentDeviceCount</span><span class="sxs-lookup"><span data-stu-id="66903-115">inactiveThreatAgentDeviceCount</span></span>|<span data-ttu-id="66903-116">Int32</span><span class="sxs-lookup"><span data-stu-id="66903-116">Int32</span></span>|<span data-ttu-id="66903-117">Dispositivo con recuento de agente de amenaza inactivos</span><span class="sxs-lookup"><span data-stu-id="66903-117">Device with inactive threat agent count</span></span>|
|<span data-ttu-id="66903-118">unknownStateThreatAgentDeviceCount</span><span class="sxs-lookup"><span data-stu-id="66903-118">unknownStateThreatAgentDeviceCount</span></span>|<span data-ttu-id="66903-119">Int32</span><span class="sxs-lookup"><span data-stu-id="66903-119">Int32</span></span>|<span data-ttu-id="66903-120">Dispositivo con el estado del agente de amenaza como count desconocido.</span><span class="sxs-lookup"><span data-stu-id="66903-120">Device with threat agent state as unknown count.</span></span>|
|<span data-ttu-id="66903-121">pendingSignatureUpdateDeviceCount</span><span class="sxs-lookup"><span data-stu-id="66903-121">pendingSignatureUpdateDeviceCount</span></span>|<span data-ttu-id="66903-122">Int32</span><span class="sxs-lookup"><span data-stu-id="66903-122">Int32</span></span>|<span data-ttu-id="66903-123">Dispositivo con recuento de firma anterior.</span><span class="sxs-lookup"><span data-stu-id="66903-123">Device with old signature count.</span></span>|
|<span data-ttu-id="66903-124">cleanDeviceCount</span><span class="sxs-lookup"><span data-stu-id="66903-124">cleanDeviceCount</span></span>|<span data-ttu-id="66903-125">Int32</span><span class="sxs-lookup"><span data-stu-id="66903-125">Int32</span></span>|<span data-ttu-id="66903-126">Limpieza de recuento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66903-126">Clean device count.</span></span>|
|<span data-ttu-id="66903-127">pendingFullScanDeviceCount</span><span class="sxs-lookup"><span data-stu-id="66903-127">pendingFullScanDeviceCount</span></span>|<span data-ttu-id="66903-128">Int32</span><span class="sxs-lookup"><span data-stu-id="66903-128">Int32</span></span>|<span data-ttu-id="66903-129">Recuento de dispositivo pendiente examen completo.</span><span class="sxs-lookup"><span data-stu-id="66903-129">Pending full scan device count.</span></span>|
|<span data-ttu-id="66903-130">pendingRestartDeviceCount</span><span class="sxs-lookup"><span data-stu-id="66903-130">pendingRestartDeviceCount</span></span>|<span data-ttu-id="66903-131">Int32</span><span class="sxs-lookup"><span data-stu-id="66903-131">Int32</span></span>|<span data-ttu-id="66903-132">Recuento de reinicio pendiente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66903-132">Pending restart device count.</span></span>|
|<span data-ttu-id="66903-133">pendingManualStepsDeviceCount</span><span class="sxs-lookup"><span data-stu-id="66903-133">pendingManualStepsDeviceCount</span></span>|<span data-ttu-id="66903-134">Int32</span><span class="sxs-lookup"><span data-stu-id="66903-134">Int32</span></span>|<span data-ttu-id="66903-135">Recuento de pasos manuales pendiente de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66903-135">Pending manual steps device count.</span></span>|
|<span data-ttu-id="66903-136">pendingOfflineScanDeviceCount</span><span class="sxs-lookup"><span data-stu-id="66903-136">pendingOfflineScanDeviceCount</span></span>|<span data-ttu-id="66903-137">Int32</span><span class="sxs-lookup"><span data-stu-id="66903-137">Int32</span></span>|<span data-ttu-id="66903-138">Recuento de dispositivo de análisis sin conexión pendiente.</span><span class="sxs-lookup"><span data-stu-id="66903-138">Pending offline scan device count.</span></span>|
|<span data-ttu-id="66903-139">criticalFailuresDeviceCount</span><span class="sxs-lookup"><span data-stu-id="66903-139">criticalFailuresDeviceCount</span></span>|<span data-ttu-id="66903-140">Int32</span><span class="sxs-lookup"><span data-stu-id="66903-140">Int32</span></span>|<span data-ttu-id="66903-141">Recuento de errores críticos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="66903-141">Critical failures device count.</span></span>|

## <a name="relationships"></a><span data-ttu-id="66903-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="66903-142">Relationships</span></span>
<span data-ttu-id="66903-143">Ninguna</span><span class="sxs-lookup"><span data-stu-id="66903-143">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="66903-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="66903-144">JSON Representation</span></span>
<span data-ttu-id="66903-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="66903-145">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.deviceProtectionOverview"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceProtectionOverview",
  "totalReportedDeviceCount": 1024,
  "inactiveThreatAgentDeviceCount": 1024,
  "unknownStateThreatAgentDeviceCount": 1024,
  "pendingSignatureUpdateDeviceCount": 1024,
  "cleanDeviceCount": 1024,
  "pendingFullScanDeviceCount": 1024,
  "pendingRestartDeviceCount": 1024,
  "pendingManualStepsDeviceCount": 1024,
  "pendingOfflineScanDeviceCount": 1024,
  "criticalFailuresDeviceCount": 1024
}
```





