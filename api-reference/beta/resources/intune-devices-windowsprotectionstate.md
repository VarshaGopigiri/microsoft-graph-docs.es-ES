---
title: tipo de recurso windowsProtectionState
description: Entidad de estado de protección de dispositivo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 5a21cc27039f3119836e0027b2558cadadab1b5d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884108"
---
# <a name="windowsprotectionstate-resource-type"></a><span data-ttu-id="8121a-103">tipo de recurso windowsProtectionState</span><span class="sxs-lookup"><span data-stu-id="8121a-103">windowsProtectionState resource type</span></span>

> <span data-ttu-id="8121a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8121a-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8121a-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8121a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8121a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8121a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8121a-107">Entidad de estado de protección de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8121a-107">Device protection status entity.</span></span>
## <a name="methods"></a><span data-ttu-id="8121a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="8121a-108">Methods</span></span>
|<span data-ttu-id="8121a-109">Método</span><span class="sxs-lookup"><span data-stu-id="8121a-109">Method</span></span>|<span data-ttu-id="8121a-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8121a-110">Return Type</span></span>|<span data-ttu-id="8121a-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8121a-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="8121a-112">Obtener windowsProtectionState</span><span class="sxs-lookup"><span data-stu-id="8121a-112">Get windowsProtectionState</span></span>](../api/intune-devices-windowsprotectionstate-get.md)|[<span data-ttu-id="8121a-113">windowsProtectionState</span><span class="sxs-lookup"><span data-stu-id="8121a-113">windowsProtectionState</span></span>](../resources/intune-devices-windowsprotectionstate.md)|<span data-ttu-id="8121a-114">Leer las propiedades y las relaciones del objeto [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) .</span><span class="sxs-lookup"><span data-stu-id="8121a-114">Read properties and relationships of the [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) object.</span></span>|
|[<span data-ttu-id="8121a-115">Actualizar windowsProtectionState</span><span class="sxs-lookup"><span data-stu-id="8121a-115">Update windowsProtectionState</span></span>](../api/intune-devices-windowsprotectionstate-update.md)|[<span data-ttu-id="8121a-116">windowsProtectionState</span><span class="sxs-lookup"><span data-stu-id="8121a-116">windowsProtectionState</span></span>](../resources/intune-devices-windowsprotectionstate.md)|<span data-ttu-id="8121a-117">Actualizar las propiedades de un objeto [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) .</span><span class="sxs-lookup"><span data-stu-id="8121a-117">Update the properties of a [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="8121a-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8121a-118">Properties</span></span>
|<span data-ttu-id="8121a-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8121a-119">Property</span></span>|<span data-ttu-id="8121a-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="8121a-120">Type</span></span>|<span data-ttu-id="8121a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="8121a-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8121a-122">id</span><span class="sxs-lookup"><span data-stu-id="8121a-122">id</span></span>|<span data-ttu-id="8121a-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="8121a-123">String</span></span>|<span data-ttu-id="8121a-124">El identificador único para el objeto de estado de protección de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8121a-124">The unique Identifier for the device protection status object.</span></span> <span data-ttu-id="8121a-125">Esto es el identificador de dispositivo del dispositivo</span><span class="sxs-lookup"><span data-stu-id="8121a-125">This is device id of the device</span></span>|
|<span data-ttu-id="8121a-126">malwareProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="8121a-126">malwareProtectionEnabled</span></span>|<span data-ttu-id="8121a-127">Booleano</span><span class="sxs-lookup"><span data-stu-id="8121a-127">Boolean</span></span>|<span data-ttu-id="8121a-128">Protección contra malware está habilitado o no</span><span class="sxs-lookup"><span data-stu-id="8121a-128">Anti malware is enabled or not</span></span>|
|<span data-ttu-id="8121a-129">deviceState</span><span class="sxs-lookup"><span data-stu-id="8121a-129">deviceState</span></span>|[<span data-ttu-id="8121a-130">windowsDeviceHealthState</span><span class="sxs-lookup"><span data-stu-id="8121a-130">windowsDeviceHealthState</span></span>](../resources/intune-devices-windowsdevicehealthstate.md)|<span data-ttu-id="8121a-131">Estado del equipo (como clean o pendiente de examen completo o pendientes reinicio etcetera).</span><span class="sxs-lookup"><span data-stu-id="8121a-131">Computer's state (like clean or pending full scan or pending reboot etc).</span></span> <span data-ttu-id="8121a-132">Los valores posibles son: `clean`, `fullScanPending`, `rebootPending`, `manualStepsPending`, `offlineScanPending`, `critical`.</span><span class="sxs-lookup"><span data-stu-id="8121a-132">Possible values are: `clean`, `fullScanPending`, `rebootPending`, `manualStepsPending`, `offlineScanPending`, `critical`.</span></span>|
|<span data-ttu-id="8121a-133">realTimeProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="8121a-133">realTimeProtectionEnabled</span></span>|<span data-ttu-id="8121a-134">Booleano</span><span class="sxs-lookup"><span data-stu-id="8121a-134">Boolean</span></span>|<span data-ttu-id="8121a-135">¿Protección en tiempo real está habilitada o no?</span><span class="sxs-lookup"><span data-stu-id="8121a-135">Real time protection is enabled or not?</span></span>|
|<span data-ttu-id="8121a-136">networkInspectionSystemEnabled</span><span class="sxs-lookup"><span data-stu-id="8121a-136">networkInspectionSystemEnabled</span></span>|<span data-ttu-id="8121a-137">Booleano</span><span class="sxs-lookup"><span data-stu-id="8121a-137">Boolean</span></span>|<span data-ttu-id="8121a-138">¿Sistema de control de red habilitado o no?</span><span class="sxs-lookup"><span data-stu-id="8121a-138">Network inspection system enabled or not?</span></span>|
|<span data-ttu-id="8121a-139">quickScanOverdue</span><span class="sxs-lookup"><span data-stu-id="8121a-139">quickScanOverdue</span></span>|<span data-ttu-id="8121a-140">Booleano</span><span class="sxs-lookup"><span data-stu-id="8121a-140">Boolean</span></span>|<span data-ttu-id="8121a-141">¿Rápido examinar vencidas o no?</span><span class="sxs-lookup"><span data-stu-id="8121a-141">Quick scan overdue or not?</span></span>|
|<span data-ttu-id="8121a-142">fullScanOverdue</span><span class="sxs-lookup"><span data-stu-id="8121a-142">fullScanOverdue</span></span>|<span data-ttu-id="8121a-143">Booleano</span><span class="sxs-lookup"><span data-stu-id="8121a-143">Boolean</span></span>|<span data-ttu-id="8121a-144">¿Total de examen vencida o no?</span><span class="sxs-lookup"><span data-stu-id="8121a-144">Full scan overdue or not?</span></span>|
|<span data-ttu-id="8121a-145">signatureUpdateOverdue</span><span class="sxs-lookup"><span data-stu-id="8121a-145">signatureUpdateOverdue</span></span>|<span data-ttu-id="8121a-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="8121a-146">Boolean</span></span>|<span data-ttu-id="8121a-147">¿Firma caducada o no?</span><span class="sxs-lookup"><span data-stu-id="8121a-147">Signature out of date or not?</span></span>|
|<span data-ttu-id="8121a-148">rebootRequired</span><span class="sxs-lookup"><span data-stu-id="8121a-148">rebootRequired</span></span>|<span data-ttu-id="8121a-149">Booleano</span><span class="sxs-lookup"><span data-stu-id="8121a-149">Boolean</span></span>|<span data-ttu-id="8121a-150">¿Es necesario reiniciar o no?</span><span class="sxs-lookup"><span data-stu-id="8121a-150">Reboot required or not?</span></span>|
|<span data-ttu-id="8121a-151">fullScanRequired</span><span class="sxs-lookup"><span data-stu-id="8121a-151">fullScanRequired</span></span>|<span data-ttu-id="8121a-152">Booleano</span><span class="sxs-lookup"><span data-stu-id="8121a-152">Boolean</span></span>|<span data-ttu-id="8121a-153">¿Examen completo o no necesario?</span><span class="sxs-lookup"><span data-stu-id="8121a-153">Full scan required or not?</span></span>|
|<span data-ttu-id="8121a-154">engineVersion</span><span class="sxs-lookup"><span data-stu-id="8121a-154">engineVersion</span></span>|<span data-ttu-id="8121a-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="8121a-155">String</span></span>|<span data-ttu-id="8121a-156">Versión del motor de actual extremo protección</span><span class="sxs-lookup"><span data-stu-id="8121a-156">Current endpoint protection engine's version</span></span>|
|<span data-ttu-id="8121a-157">signatureVersion</span><span class="sxs-lookup"><span data-stu-id="8121a-157">signatureVersion</span></span>|<span data-ttu-id="8121a-158">Cadena</span><span class="sxs-lookup"><span data-stu-id="8121a-158">String</span></span>|<span data-ttu-id="8121a-159">Versión actual de las definiciones de malware</span><span class="sxs-lookup"><span data-stu-id="8121a-159">Current malware definitions version</span></span>|
|<span data-ttu-id="8121a-160">antiMalwareVersion</span><span class="sxs-lookup"><span data-stu-id="8121a-160">antiMalwareVersion</span></span>|<span data-ttu-id="8121a-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="8121a-161">String</span></span>|<span data-ttu-id="8121a-162">Actual de protección contra malware versión</span><span class="sxs-lookup"><span data-stu-id="8121a-162">Current anti malware version</span></span>|
|<span data-ttu-id="8121a-163">lastQuickScanDateTime</span><span class="sxs-lookup"><span data-stu-id="8121a-163">lastQuickScanDateTime</span></span>|<span data-ttu-id="8121a-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8121a-164">DateTimeOffset</span></span>|<span data-ttu-id="8121a-165">Fecha y hora último análisis rápido</span><span class="sxs-lookup"><span data-stu-id="8121a-165">Last quick scan datetime</span></span>|
|<span data-ttu-id="8121a-166">lastFullScanDateTime</span><span class="sxs-lookup"><span data-stu-id="8121a-166">lastFullScanDateTime</span></span>|<span data-ttu-id="8121a-167">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8121a-167">DateTimeOffset</span></span>|<span data-ttu-id="8121a-168">Fecha y hora último análisis rápido</span><span class="sxs-lookup"><span data-stu-id="8121a-168">Last quick scan datetime</span></span>|
|<span data-ttu-id="8121a-169">lastQuickScanSignatureVersion</span><span class="sxs-lookup"><span data-stu-id="8121a-169">lastQuickScanSignatureVersion</span></span>|<span data-ttu-id="8121a-170">Cadena</span><span class="sxs-lookup"><span data-stu-id="8121a-170">String</span></span>|<span data-ttu-id="8121a-171">Última versión de firma de análisis rápido</span><span class="sxs-lookup"><span data-stu-id="8121a-171">Last quick scan signature version</span></span>|
|<span data-ttu-id="8121a-172">lastFullScanSignatureVersion</span><span class="sxs-lookup"><span data-stu-id="8121a-172">lastFullScanSignatureVersion</span></span>|<span data-ttu-id="8121a-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="8121a-173">String</span></span>|<span data-ttu-id="8121a-174">Última versión de firma de examen completo</span><span class="sxs-lookup"><span data-stu-id="8121a-174">Last full scan signature version</span></span>|
|<span data-ttu-id="8121a-175">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="8121a-175">lastReportedDateTime</span></span>|<span data-ttu-id="8121a-176">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8121a-176">DateTimeOffset</span></span>|<span data-ttu-id="8121a-177">Último estado de mantenimiento de dispositivo el tiempo notificado</span><span class="sxs-lookup"><span data-stu-id="8121a-177">Last device health status reported time</span></span>|

## <a name="relationships"></a><span data-ttu-id="8121a-178">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8121a-178">Relationships</span></span>
|<span data-ttu-id="8121a-179">Relación</span><span class="sxs-lookup"><span data-stu-id="8121a-179">Relationship</span></span>|<span data-ttu-id="8121a-180">Tipo</span><span class="sxs-lookup"><span data-stu-id="8121a-180">Type</span></span>|<span data-ttu-id="8121a-181">Description</span><span class="sxs-lookup"><span data-stu-id="8121a-181">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8121a-182">detectedMalwareState</span><span class="sxs-lookup"><span data-stu-id="8121a-182">detectedMalwareState</span></span>|<span data-ttu-id="8121a-183">colección de [windowsDeviceMalwareState](../resources/intune-devices-windowsdevicemalwarestate.md)</span><span class="sxs-lookup"><span data-stu-id="8121a-183">[windowsDeviceMalwareState](../resources/intune-devices-windowsdevicemalwarestate.md) collection</span></span>|<span data-ttu-id="8121a-184">Lista de dispositivos de malware</span><span class="sxs-lookup"><span data-stu-id="8121a-184">Device malware list</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8121a-185">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8121a-185">JSON Representation</span></span>
<span data-ttu-id="8121a-186">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="8121a-186">Here is a JSON representation of the resource.</span></span>
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





