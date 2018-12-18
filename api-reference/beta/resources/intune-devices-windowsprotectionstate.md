---
title: tipo de recurso windowsProtectionState
description: Entidad de estado de protección de dispositivo.
author: tfitzmac
ms.openlocfilehash: 636b969ddafde5976939df764ae1180e19a181c0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27328080"
---
# <a name="windowsprotectionstate-resource-type"></a><span data-ttu-id="ffc21-103">tipo de recurso windowsProtectionState</span><span class="sxs-lookup"><span data-stu-id="ffc21-103">windowsProtectionState resource type</span></span>

> <span data-ttu-id="ffc21-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ffc21-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ffc21-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ffc21-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ffc21-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ffc21-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ffc21-107">Entidad de estado de protección de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ffc21-107">Device protection status entity.</span></span>
## <a name="methods"></a><span data-ttu-id="ffc21-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="ffc21-108">Methods</span></span>
|<span data-ttu-id="ffc21-109">Método</span><span class="sxs-lookup"><span data-stu-id="ffc21-109">Method</span></span>|<span data-ttu-id="ffc21-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ffc21-110">Return Type</span></span>|<span data-ttu-id="ffc21-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffc21-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="ffc21-112">Obtener windowsProtectionState</span><span class="sxs-lookup"><span data-stu-id="ffc21-112">Get windowsProtectionState</span></span>](../api/intune-devices-windowsprotectionstate-get.md)|[<span data-ttu-id="ffc21-113">windowsProtectionState</span><span class="sxs-lookup"><span data-stu-id="ffc21-113">windowsProtectionState</span></span>](../resources/intune-devices-windowsprotectionstate.md)|<span data-ttu-id="ffc21-114">Leer las propiedades y las relaciones del objeto [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc21-114">Read properties and relationships of the [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) object.</span></span>|
|[<span data-ttu-id="ffc21-115">Actualizar windowsProtectionState</span><span class="sxs-lookup"><span data-stu-id="ffc21-115">Update windowsProtectionState</span></span>](../api/intune-devices-windowsprotectionstate-update.md)|[<span data-ttu-id="ffc21-116">windowsProtectionState</span><span class="sxs-lookup"><span data-stu-id="ffc21-116">windowsProtectionState</span></span>](../resources/intune-devices-windowsprotectionstate.md)|<span data-ttu-id="ffc21-117">Actualizar las propiedades de un objeto [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) .</span><span class="sxs-lookup"><span data-stu-id="ffc21-117">Update the properties of a [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="ffc21-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffc21-118">Properties</span></span>
|<span data-ttu-id="ffc21-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ffc21-119">Property</span></span>|<span data-ttu-id="ffc21-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc21-120">Type</span></span>|<span data-ttu-id="ffc21-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffc21-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ffc21-122">id</span><span class="sxs-lookup"><span data-stu-id="ffc21-122">id</span></span>|<span data-ttu-id="ffc21-123">String</span><span class="sxs-lookup"><span data-stu-id="ffc21-123">String</span></span>|<span data-ttu-id="ffc21-124">El identificador único para el objeto de estado de protección de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ffc21-124">The unique Identifier for the device protection status object.</span></span> <span data-ttu-id="ffc21-125">Esto es el identificador de dispositivo del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ffc21-125">This is device id of the device</span></span>|
|<span data-ttu-id="ffc21-126">malwareProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="ffc21-126">malwareProtectionEnabled</span></span>|<span data-ttu-id="ffc21-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="ffc21-127">Boolean</span></span>|<span data-ttu-id="ffc21-128">Protección contra malware está habilitado o no</span><span class="sxs-lookup"><span data-stu-id="ffc21-128">Anti malware is enabled or not</span></span>|
|<span data-ttu-id="ffc21-129">deviceState</span><span class="sxs-lookup"><span data-stu-id="ffc21-129">deviceState</span></span>|[<span data-ttu-id="ffc21-130">windowsDeviceHealthState</span><span class="sxs-lookup"><span data-stu-id="ffc21-130">windowsDeviceHealthState</span></span>](../resources/intune-devices-windowsdevicehealthstate.md)|<span data-ttu-id="ffc21-131">Estado del equipo (como clean o pendiente de examen completo o pendientes reinicio etcetera).</span><span class="sxs-lookup"><span data-stu-id="ffc21-131">Computer's state (like clean or pending full scan or pending reboot etc).</span></span> <span data-ttu-id="ffc21-132">Los valores posibles son: `clean`, `fullScanPending`, `rebootPending`, `manualStepsPending`, `offlineScanPending`, `critical`.</span><span class="sxs-lookup"><span data-stu-id="ffc21-132">Possible values are: `clean`, `fullScanPending`, `rebootPending`, `manualStepsPending`, `offlineScanPending`, `critical`.</span></span>|
|<span data-ttu-id="ffc21-133">realTimeProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="ffc21-133">realTimeProtectionEnabled</span></span>|<span data-ttu-id="ffc21-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="ffc21-134">Boolean</span></span>|<span data-ttu-id="ffc21-135">¿Protección en tiempo real está habilitada o no?</span><span class="sxs-lookup"><span data-stu-id="ffc21-135">Real time protection is enabled or not?</span></span>|
|<span data-ttu-id="ffc21-136">networkInspectionSystemEnabled</span><span class="sxs-lookup"><span data-stu-id="ffc21-136">networkInspectionSystemEnabled</span></span>|<span data-ttu-id="ffc21-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="ffc21-137">Boolean</span></span>|<span data-ttu-id="ffc21-138">¿Sistema de control de red habilitado o no?</span><span class="sxs-lookup"><span data-stu-id="ffc21-138">Network inspection system enabled or not?</span></span>|
|<span data-ttu-id="ffc21-139">quickScanOverdue</span><span class="sxs-lookup"><span data-stu-id="ffc21-139">quickScanOverdue</span></span>|<span data-ttu-id="ffc21-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="ffc21-140">Boolean</span></span>|<span data-ttu-id="ffc21-141">¿Rápido examinar vencidas o no?</span><span class="sxs-lookup"><span data-stu-id="ffc21-141">Quick scan overdue or not?</span></span>|
|<span data-ttu-id="ffc21-142">fullScanOverdue</span><span class="sxs-lookup"><span data-stu-id="ffc21-142">fullScanOverdue</span></span>|<span data-ttu-id="ffc21-143">Boolean</span><span class="sxs-lookup"><span data-stu-id="ffc21-143">Boolean</span></span>|<span data-ttu-id="ffc21-144">¿Total de examen vencida o no?</span><span class="sxs-lookup"><span data-stu-id="ffc21-144">Full scan overdue or not?</span></span>|
|<span data-ttu-id="ffc21-145">signatureUpdateOverdue</span><span class="sxs-lookup"><span data-stu-id="ffc21-145">signatureUpdateOverdue</span></span>|<span data-ttu-id="ffc21-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="ffc21-146">Boolean</span></span>|<span data-ttu-id="ffc21-147">¿Firma caducada o no?</span><span class="sxs-lookup"><span data-stu-id="ffc21-147">Signature out of date or not?</span></span>|
|<span data-ttu-id="ffc21-148">rebootRequired</span><span class="sxs-lookup"><span data-stu-id="ffc21-148">rebootRequired</span></span>|<span data-ttu-id="ffc21-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="ffc21-149">Boolean</span></span>|<span data-ttu-id="ffc21-150">¿Es necesario reiniciar o no?</span><span class="sxs-lookup"><span data-stu-id="ffc21-150">Reboot required or not?</span></span>|
|<span data-ttu-id="ffc21-151">fullScanRequired</span><span class="sxs-lookup"><span data-stu-id="ffc21-151">fullScanRequired</span></span>|<span data-ttu-id="ffc21-152">Boolean</span><span class="sxs-lookup"><span data-stu-id="ffc21-152">Boolean</span></span>|<span data-ttu-id="ffc21-153">¿Examen completo o no necesario?</span><span class="sxs-lookup"><span data-stu-id="ffc21-153">Full scan required or not?</span></span>|
|<span data-ttu-id="ffc21-154">engineVersion</span><span class="sxs-lookup"><span data-stu-id="ffc21-154">engineVersion</span></span>|<span data-ttu-id="ffc21-155">String</span><span class="sxs-lookup"><span data-stu-id="ffc21-155">String</span></span>|<span data-ttu-id="ffc21-156">Versión del motor de actual extremo protección</span><span class="sxs-lookup"><span data-stu-id="ffc21-156">Current endpoint protection engine's version</span></span>|
|<span data-ttu-id="ffc21-157">signatureVersion</span><span class="sxs-lookup"><span data-stu-id="ffc21-157">signatureVersion</span></span>|<span data-ttu-id="ffc21-158">String</span><span class="sxs-lookup"><span data-stu-id="ffc21-158">String</span></span>|<span data-ttu-id="ffc21-159">Versión actual de las definiciones de malware</span><span class="sxs-lookup"><span data-stu-id="ffc21-159">Current malware definitions version</span></span>|
|<span data-ttu-id="ffc21-160">antiMalwareVersion</span><span class="sxs-lookup"><span data-stu-id="ffc21-160">antiMalwareVersion</span></span>|<span data-ttu-id="ffc21-161">String</span><span class="sxs-lookup"><span data-stu-id="ffc21-161">String</span></span>|<span data-ttu-id="ffc21-162">Actual de protección contra malware versión</span><span class="sxs-lookup"><span data-stu-id="ffc21-162">Current anti malware version</span></span>|
|<span data-ttu-id="ffc21-163">lastQuickScanDateTime</span><span class="sxs-lookup"><span data-stu-id="ffc21-163">lastQuickScanDateTime</span></span>|<span data-ttu-id="ffc21-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ffc21-164">DateTimeOffset</span></span>|<span data-ttu-id="ffc21-165">Fecha y hora último análisis rápido</span><span class="sxs-lookup"><span data-stu-id="ffc21-165">Last quick scan datetime</span></span>|
|<span data-ttu-id="ffc21-166">lastFullScanDateTime</span><span class="sxs-lookup"><span data-stu-id="ffc21-166">lastFullScanDateTime</span></span>|<span data-ttu-id="ffc21-167">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ffc21-167">DateTimeOffset</span></span>|<span data-ttu-id="ffc21-168">Fecha y hora último análisis rápido</span><span class="sxs-lookup"><span data-stu-id="ffc21-168">Last quick scan datetime</span></span>|
|<span data-ttu-id="ffc21-169">lastQuickScanSignatureVersion</span><span class="sxs-lookup"><span data-stu-id="ffc21-169">lastQuickScanSignatureVersion</span></span>|<span data-ttu-id="ffc21-170">String</span><span class="sxs-lookup"><span data-stu-id="ffc21-170">String</span></span>|<span data-ttu-id="ffc21-171">Última versión de firma de análisis rápido</span><span class="sxs-lookup"><span data-stu-id="ffc21-171">Last quick scan signature version</span></span>|
|<span data-ttu-id="ffc21-172">lastFullScanSignatureVersion</span><span class="sxs-lookup"><span data-stu-id="ffc21-172">lastFullScanSignatureVersion</span></span>|<span data-ttu-id="ffc21-173">String</span><span class="sxs-lookup"><span data-stu-id="ffc21-173">String</span></span>|<span data-ttu-id="ffc21-174">Última versión de firma de examen completo</span><span class="sxs-lookup"><span data-stu-id="ffc21-174">Last full scan signature version</span></span>|
|<span data-ttu-id="ffc21-175">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="ffc21-175">lastReportedDateTime</span></span>|<span data-ttu-id="ffc21-176">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ffc21-176">DateTimeOffset</span></span>|<span data-ttu-id="ffc21-177">Último estado de mantenimiento de dispositivo el tiempo notificado</span><span class="sxs-lookup"><span data-stu-id="ffc21-177">Last device health status reported time</span></span>|

## <a name="relationships"></a><span data-ttu-id="ffc21-178">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ffc21-178">Relationships</span></span>
|<span data-ttu-id="ffc21-179">Relación</span><span class="sxs-lookup"><span data-stu-id="ffc21-179">Relationship</span></span>|<span data-ttu-id="ffc21-180">Tipo</span><span class="sxs-lookup"><span data-stu-id="ffc21-180">Type</span></span>|<span data-ttu-id="ffc21-181">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffc21-181">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ffc21-182">detectedMalwareState</span><span class="sxs-lookup"><span data-stu-id="ffc21-182">detectedMalwareState</span></span>|<span data-ttu-id="ffc21-183">colección de [windowsDeviceMalwareState](../resources/intune-devices-windowsdevicemalwarestate.md)</span><span class="sxs-lookup"><span data-stu-id="ffc21-183">[windowsDeviceMalwareState](../resources/intune-devices-windowsdevicemalwarestate.md) collection</span></span>|<span data-ttu-id="ffc21-184">Lista de dispositivos de malware</span><span class="sxs-lookup"><span data-stu-id="ffc21-184">Device malware list</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ffc21-185">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ffc21-185">JSON Representation</span></span>
<span data-ttu-id="ffc21-186">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ffc21-186">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windowsProtectionState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsProtectionState",
  "id": "String (identifier)",
  "malwareProtectionEnabled": true,
  "deviceState": "String",
  "realTimeProtectionEnabled": true,
  "networkInspectionSystemEnabled": true,
  "quickScanOverdue": true,
  "fullScanOverdue": true,
  "signatureUpdateOverdue": true,
  "rebootRequired": true,
  "fullScanRequired": true,
  "engineVersion": "String",
  "signatureVersion": "String",
  "antiMalwareVersion": "String",
  "lastQuickScanDateTime": "String (timestamp)",
  "lastFullScanDateTime": "String (timestamp)",
  "lastQuickScanSignatureVersion": "String",
  "lastFullScanSignatureVersion": "String",
  "lastReportedDateTime": "String (timestamp)"
}
```





