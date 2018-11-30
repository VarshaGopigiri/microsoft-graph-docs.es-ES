---
title: Actualizar windowsProtectionState
description: Actualizar las propiedades de un objeto windowsProtectionState.
ms.openlocfilehash: f1323baa9a6611e5f6057456fbbefbaddefa626e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088556"
---
# <a name="update-windowsprotectionstate"></a><span data-ttu-id="9216e-103">Actualizar windowsProtectionState</span><span class="sxs-lookup"><span data-stu-id="9216e-103">Update windowsProtectionState</span></span>

> <span data-ttu-id="9216e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9216e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9216e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9216e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9216e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9216e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9216e-107">Actualizar las propiedades de un objeto [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) .</span><span class="sxs-lookup"><span data-stu-id="9216e-107">Update the properties of a [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9216e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9216e-108">Prerequisites</span></span>
<span data-ttu-id="9216e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9216e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9216e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9216e-111">Permission type</span></span>|<span data-ttu-id="9216e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9216e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9216e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9216e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9216e-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9216e-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="9216e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9216e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9216e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9216e-116">Not supported.</span></span>|
|<span data-ttu-id="9216e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9216e-117">Application</span></span>|<span data-ttu-id="9216e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9216e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9216e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9216e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/windowsMalwareInformation/{windowsMalwareInformationId}/windowsDevicesProtectionState/{windowsProtectionStateId}
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/windowsProtectionState
```

## <a name="request-headers"></a><span data-ttu-id="9216e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9216e-120">Request headers</span></span>
|<span data-ttu-id="9216e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9216e-121">Header</span></span>|<span data-ttu-id="9216e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9216e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9216e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9216e-123">Authorization</span></span>|<span data-ttu-id="9216e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9216e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9216e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9216e-125">Accept</span></span>|<span data-ttu-id="9216e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9216e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9216e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9216e-127">Request body</span></span>
<span data-ttu-id="9216e-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) .</span><span class="sxs-lookup"><span data-stu-id="9216e-128">In the request body, supply a JSON representation for the [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) object.</span></span>

<span data-ttu-id="9216e-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md).</span><span class="sxs-lookup"><span data-stu-id="9216e-129">The following table shows the properties that are required when you create the [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md).</span></span>

|<span data-ttu-id="9216e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9216e-130">Property</span></span>|<span data-ttu-id="9216e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9216e-131">Type</span></span>|<span data-ttu-id="9216e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9216e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9216e-133">id</span><span class="sxs-lookup"><span data-stu-id="9216e-133">id</span></span>|<span data-ttu-id="9216e-134">String</span><span class="sxs-lookup"><span data-stu-id="9216e-134">String</span></span>|<span data-ttu-id="9216e-135">El identificador único para el objeto de estado de protección de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9216e-135">The unique Identifier for the device protection status object.</span></span> <span data-ttu-id="9216e-136">Esto es el identificador de dispositivo del dispositivo</span><span class="sxs-lookup"><span data-stu-id="9216e-136">This is device id of the device</span></span>|
|<span data-ttu-id="9216e-137">malwareProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="9216e-137">malwareProtectionEnabled</span></span>|<span data-ttu-id="9216e-138">Booleano</span><span class="sxs-lookup"><span data-stu-id="9216e-138">Boolean</span></span>|<span data-ttu-id="9216e-139">Protección contra malware está habilitado o no</span><span class="sxs-lookup"><span data-stu-id="9216e-139">Anti malware is enabled or not</span></span>|
|<span data-ttu-id="9216e-140">deviceState</span><span class="sxs-lookup"><span data-stu-id="9216e-140">deviceState</span></span>|[<span data-ttu-id="9216e-141">windowsDeviceHealthState</span><span class="sxs-lookup"><span data-stu-id="9216e-141">windowsDeviceHealthState</span></span>](../resources/intune-devices-windowsdevicehealthstate.md)|<span data-ttu-id="9216e-142">Estado del equipo (como clean o pendiente de examen completo o pendientes reinicio etcetera).</span><span class="sxs-lookup"><span data-stu-id="9216e-142">Computer's state (like clean or pending full scan or pending reboot etc).</span></span> <span data-ttu-id="9216e-143">Los valores posibles son: `clean`, `fullScanPending`, `rebootPending`, `manualStepsPending`, `offlineScanPending`, `critical`.</span><span class="sxs-lookup"><span data-stu-id="9216e-143">Possible values are: `clean`, `fullScanPending`, `rebootPending`, `manualStepsPending`, `offlineScanPending`, `critical`.</span></span>|
|<span data-ttu-id="9216e-144">realTimeProtectionEnabled</span><span class="sxs-lookup"><span data-stu-id="9216e-144">realTimeProtectionEnabled</span></span>|<span data-ttu-id="9216e-145">Booleano</span><span class="sxs-lookup"><span data-stu-id="9216e-145">Boolean</span></span>|<span data-ttu-id="9216e-146">¿Protección en tiempo real está habilitada o no?</span><span class="sxs-lookup"><span data-stu-id="9216e-146">Real time protection is enabled or not?</span></span>|
|<span data-ttu-id="9216e-147">networkInspectionSystemEnabled</span><span class="sxs-lookup"><span data-stu-id="9216e-147">networkInspectionSystemEnabled</span></span>|<span data-ttu-id="9216e-148">Booleano</span><span class="sxs-lookup"><span data-stu-id="9216e-148">Boolean</span></span>|<span data-ttu-id="9216e-149">¿Sistema de control de red habilitado o no?</span><span class="sxs-lookup"><span data-stu-id="9216e-149">Network inspection system enabled or not?</span></span>|
|<span data-ttu-id="9216e-150">quickScanOverdue</span><span class="sxs-lookup"><span data-stu-id="9216e-150">quickScanOverdue</span></span>|<span data-ttu-id="9216e-151">Booleano</span><span class="sxs-lookup"><span data-stu-id="9216e-151">Boolean</span></span>|<span data-ttu-id="9216e-152">¿Rápido examinar vencidas o no?</span><span class="sxs-lookup"><span data-stu-id="9216e-152">Quick scan overdue or not?</span></span>|
|<span data-ttu-id="9216e-153">fullScanOverdue</span><span class="sxs-lookup"><span data-stu-id="9216e-153">fullScanOverdue</span></span>|<span data-ttu-id="9216e-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="9216e-154">Boolean</span></span>|<span data-ttu-id="9216e-155">¿Total de examen vencida o no?</span><span class="sxs-lookup"><span data-stu-id="9216e-155">Full scan overdue or not?</span></span>|
|<span data-ttu-id="9216e-156">signatureUpdateOverdue</span><span class="sxs-lookup"><span data-stu-id="9216e-156">signatureUpdateOverdue</span></span>|<span data-ttu-id="9216e-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="9216e-157">Boolean</span></span>|<span data-ttu-id="9216e-158">¿Firma caducada o no?</span><span class="sxs-lookup"><span data-stu-id="9216e-158">Signature out of date or not?</span></span>|
|<span data-ttu-id="9216e-159">rebootRequired</span><span class="sxs-lookup"><span data-stu-id="9216e-159">rebootRequired</span></span>|<span data-ttu-id="9216e-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="9216e-160">Boolean</span></span>|<span data-ttu-id="9216e-161">¿Es necesario reiniciar o no?</span><span class="sxs-lookup"><span data-stu-id="9216e-161">Reboot required or not?</span></span>|
|<span data-ttu-id="9216e-162">fullScanRequired</span><span class="sxs-lookup"><span data-stu-id="9216e-162">fullScanRequired</span></span>|<span data-ttu-id="9216e-163">Booleano</span><span class="sxs-lookup"><span data-stu-id="9216e-163">Boolean</span></span>|<span data-ttu-id="9216e-164">¿Examen completo o no necesario?</span><span class="sxs-lookup"><span data-stu-id="9216e-164">Full scan required or not?</span></span>|
|<span data-ttu-id="9216e-165">engineVersion</span><span class="sxs-lookup"><span data-stu-id="9216e-165">engineVersion</span></span>|<span data-ttu-id="9216e-166">String</span><span class="sxs-lookup"><span data-stu-id="9216e-166">String</span></span>|<span data-ttu-id="9216e-167">Versión del motor de actual extremo protección</span><span class="sxs-lookup"><span data-stu-id="9216e-167">Current endpoint protection engine's version</span></span>|
|<span data-ttu-id="9216e-168">signatureVersion</span><span class="sxs-lookup"><span data-stu-id="9216e-168">signatureVersion</span></span>|<span data-ttu-id="9216e-169">String</span><span class="sxs-lookup"><span data-stu-id="9216e-169">String</span></span>|<span data-ttu-id="9216e-170">Versión actual de las definiciones de malware</span><span class="sxs-lookup"><span data-stu-id="9216e-170">Current malware definitions version</span></span>|
|<span data-ttu-id="9216e-171">antiMalwareVersion</span><span class="sxs-lookup"><span data-stu-id="9216e-171">antiMalwareVersion</span></span>|<span data-ttu-id="9216e-172">String</span><span class="sxs-lookup"><span data-stu-id="9216e-172">String</span></span>|<span data-ttu-id="9216e-173">Actual de protección contra malware versión</span><span class="sxs-lookup"><span data-stu-id="9216e-173">Current anti malware version</span></span>|
|<span data-ttu-id="9216e-174">lastQuickScanDateTime</span><span class="sxs-lookup"><span data-stu-id="9216e-174">lastQuickScanDateTime</span></span>|<span data-ttu-id="9216e-175">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9216e-175">DateTimeOffset</span></span>|<span data-ttu-id="9216e-176">Fecha y hora último análisis rápido</span><span class="sxs-lookup"><span data-stu-id="9216e-176">Last quick scan datetime</span></span>|
|<span data-ttu-id="9216e-177">lastFullScanDateTime</span><span class="sxs-lookup"><span data-stu-id="9216e-177">lastFullScanDateTime</span></span>|<span data-ttu-id="9216e-178">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9216e-178">DateTimeOffset</span></span>|<span data-ttu-id="9216e-179">Fecha y hora último análisis rápido</span><span class="sxs-lookup"><span data-stu-id="9216e-179">Last quick scan datetime</span></span>|
|<span data-ttu-id="9216e-180">lastQuickScanSignatureVersion</span><span class="sxs-lookup"><span data-stu-id="9216e-180">lastQuickScanSignatureVersion</span></span>|<span data-ttu-id="9216e-181">String</span><span class="sxs-lookup"><span data-stu-id="9216e-181">String</span></span>|<span data-ttu-id="9216e-182">Última versión de firma de análisis rápido</span><span class="sxs-lookup"><span data-stu-id="9216e-182">Last quick scan signature version</span></span>|
|<span data-ttu-id="9216e-183">lastFullScanSignatureVersion</span><span class="sxs-lookup"><span data-stu-id="9216e-183">lastFullScanSignatureVersion</span></span>|<span data-ttu-id="9216e-184">String</span><span class="sxs-lookup"><span data-stu-id="9216e-184">String</span></span>|<span data-ttu-id="9216e-185">Última versión de firma de examen completo</span><span class="sxs-lookup"><span data-stu-id="9216e-185">Last full scan signature version</span></span>|
|<span data-ttu-id="9216e-186">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="9216e-186">lastReportedDateTime</span></span>|<span data-ttu-id="9216e-187">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9216e-187">DateTimeOffset</span></span>|<span data-ttu-id="9216e-188">Último estado de mantenimiento de dispositivo el tiempo notificado</span><span class="sxs-lookup"><span data-stu-id="9216e-188">Last device health status reported time</span></span>|



## <a name="response"></a><span data-ttu-id="9216e-189">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9216e-189">Response</span></span>
<span data-ttu-id="9216e-190">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9216e-190">If successful, this method returns a `200 OK` response code and an updated [windowsProtectionState](../resources/intune-devices-windowsprotectionstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9216e-191">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9216e-191">Example</span></span>
### <a name="request"></a><span data-ttu-id="9216e-192">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9216e-192">Request</span></span>
<span data-ttu-id="9216e-193">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9216e-193">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/windowsMalwareInformation/{windowsMalwareInformationId}/windowsDevicesProtectionState/{windowsProtectionStateId}
Content-type: application/json
Content-length: 804

{
  "malwareProtectionEnabled": true,
  "deviceState": "fullScanPending",
  "realTimeProtectionEnabled": true,
  "networkInspectionSystemEnabled": true,
  "quickScanOverdue": true,
  "fullScanOverdue": true,
  "signatureUpdateOverdue": true,
  "rebootRequired": true,
  "fullScanRequired": true,
  "engineVersion": "Engine Version value",
  "signatureVersion": "Signature Version value",
  "antiMalwareVersion": "Anti Malware Version value",
  "lastQuickScanDateTime": "2016-12-31T23:58:27.5900669-08:00",
  "lastFullScanDateTime": "2017-01-01T00:01:44.9405639-08:00",
  "lastQuickScanSignatureVersion": "Last Quick Scan Signature Version value",
  "lastFullScanSignatureVersion": "Last Full Scan Signature Version value",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00"
}
```

### <a name="response"></a><span data-ttu-id="9216e-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9216e-194">Response</span></span>
<span data-ttu-id="9216e-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9216e-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 914

{
  "@odata.type": "#microsoft.graph.windowsProtectionState",
  "id": "1ac6ea5a-ea5a-1ac6-5aea-c61a5aeac61a",
  "malwareProtectionEnabled": true,
  "deviceState": "fullScanPending",
  "realTimeProtectionEnabled": true,
  "networkInspectionSystemEnabled": true,
  "quickScanOverdue": true,
  "fullScanOverdue": true,
  "signatureUpdateOverdue": true,
  "rebootRequired": true,
  "fullScanRequired": true,
  "engineVersion": "Engine Version value",
  "signatureVersion": "Signature Version value",
  "antiMalwareVersion": "Anti Malware Version value",
  "lastQuickScanDateTime": "2016-12-31T23:58:27.5900669-08:00",
  "lastFullScanDateTime": "2017-01-01T00:01:44.9405639-08:00",
  "lastQuickScanSignatureVersion": "Last Quick Scan Signature Version value",
  "lastFullScanSignatureVersion": "Last Full Scan Signature Version value",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00"
}
```





