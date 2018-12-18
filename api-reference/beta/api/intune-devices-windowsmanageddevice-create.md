---
title: Crear windowsManagedDevice
description: Crear un nuevo objeto windowsManagedDevice.
author: tfitzmac
ms.openlocfilehash: 21626854a52ed305dbf237562e151e168330f170
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324447"
---
# <a name="create-windowsmanageddevice"></a><span data-ttu-id="d8876-103">Crear windowsManagedDevice</span><span class="sxs-lookup"><span data-stu-id="d8876-103">Create windowsManagedDevice</span></span>

> <span data-ttu-id="d8876-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d8876-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d8876-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d8876-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d8876-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d8876-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d8876-107">Crear un nuevo objeto [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) .</span><span class="sxs-lookup"><span data-stu-id="d8876-107">Create a new [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d8876-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d8876-108">Prerequisites</span></span>
<span data-ttu-id="d8876-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="d8876-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="d8876-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d8876-111">Permission type</span></span>|<span data-ttu-id="d8876-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d8876-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d8876-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d8876-113">Delegated (work or school account)</span></span>|<span data-ttu-id="d8876-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d8876-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="d8876-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d8876-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d8876-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d8876-116">Not supported.</span></span>|
|<span data-ttu-id="d8876-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d8876-117">Application</span></span>|<span data-ttu-id="d8876-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d8876-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d8876-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d8876-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices
POST /deviceManagement/managedDevices
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices
```

## <a name="request-headers"></a><span data-ttu-id="d8876-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d8876-120">Request headers</span></span>
|<span data-ttu-id="d8876-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8876-121">Header</span></span>|<span data-ttu-id="d8876-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d8876-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d8876-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="d8876-123">Authorization</span></span>|<span data-ttu-id="d8876-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d8876-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d8876-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d8876-125">Accept</span></span>|<span data-ttu-id="d8876-126">application/json</span><span class="sxs-lookup"><span data-stu-id="d8876-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d8876-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d8876-127">Request body</span></span>
<span data-ttu-id="d8876-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsManagedDevice.</span><span class="sxs-lookup"><span data-stu-id="d8876-128">In the request body, supply a JSON representation for the windowsManagedDevice object.</span></span>

<span data-ttu-id="d8876-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsManagedDevice.</span><span class="sxs-lookup"><span data-stu-id="d8876-129">The following table shows the properties that are required when you create the windowsManagedDevice.</span></span>

|<span data-ttu-id="d8876-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d8876-130">Property</span></span>|<span data-ttu-id="d8876-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="d8876-131">Type</span></span>|<span data-ttu-id="d8876-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8876-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d8876-133">id</span><span class="sxs-lookup"><span data-stu-id="d8876-133">id</span></span>|<span data-ttu-id="d8876-134">String</span><span class="sxs-lookup"><span data-stu-id="d8876-134">String</span></span>|<span data-ttu-id="d8876-135">Identificador único para el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-135">Unique Identifier for the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-136">userId</span><span class="sxs-lookup"><span data-stu-id="d8876-136">userId</span></span>|<span data-ttu-id="d8876-137">String</span><span class="sxs-lookup"><span data-stu-id="d8876-137">String</span></span>|<span data-ttu-id="d8876-138">Identificador único para el usuario asociado con el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-138">Unique Identifier for the user associated with the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-139">deviceName</span><span class="sxs-lookup"><span data-stu-id="d8876-139">deviceName</span></span>|<span data-ttu-id="d8876-140">String</span><span class="sxs-lookup"><span data-stu-id="d8876-140">String</span></span>|<span data-ttu-id="d8876-141">Nombre del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-141">Name of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-142">hardwareInformation</span><span class="sxs-lookup"><span data-stu-id="d8876-142">hardwareInformation</span></span>|[<span data-ttu-id="d8876-143">hardwareInformation</span><span class="sxs-lookup"><span data-stu-id="d8876-143">hardwareInformation</span></span>](../resources/intune-devices-hardwareinformation.md)|<span data-ttu-id="d8876-144">Los detalles de hardward para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-144">The hardward details for the device.</span></span>  <span data-ttu-id="d8876-145">Incluye información como el espacio de almacenamiento, el fabricante, el número de serie, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-145">Includes information such as storage space, manufacturer, serial number, etc. Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-146">ownerType</span><span class="sxs-lookup"><span data-stu-id="d8876-146">ownerType</span></span>|[<span data-ttu-id="d8876-147">ownerType</span><span class="sxs-lookup"><span data-stu-id="d8876-147">ownerType</span></span>](../resources/intune-devices-ownertype.md)|<span data-ttu-id="d8876-148">Propietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-148">Ownership of the device.</span></span> <span data-ttu-id="d8876-149">Puede ser 'compañía' o 'personal' heredado de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-149">Can be 'company' or 'personal' Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-150">Los valores posibles son: `unknown`, `company` y `personal`.</span><span class="sxs-lookup"><span data-stu-id="d8876-150">Possible values are: `unknown`, `company`, `personal`.</span></span>|
|<span data-ttu-id="d8876-151">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="d8876-151">managedDeviceOwnerType</span></span>|[<span data-ttu-id="d8876-152">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="d8876-152">managedDeviceOwnerType</span></span>](../resources/intune-devices-manageddeviceownertype.md)|<span data-ttu-id="d8876-153">Propietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-153">Ownership of the device.</span></span> <span data-ttu-id="d8876-154">Puede ser 'compañía' o 'personal' heredado de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-154">Can be 'company' or 'personal' Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-155">Los valores posibles son: `unknown`, `company` y `personal`.</span><span class="sxs-lookup"><span data-stu-id="d8876-155">Possible values are: `unknown`, `company`, `personal`.</span></span>|
|<span data-ttu-id="d8876-156">deviceActionResults</span><span class="sxs-lookup"><span data-stu-id="d8876-156">deviceActionResults</span></span>|<span data-ttu-id="d8876-157">Colección [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-157">[deviceActionResult](../resources/intune-devices-deviceactionresult.md) collection</span></span>|<span data-ttu-id="d8876-158">Lista de objetos deviceActionResult ComplexType.</span><span class="sxs-lookup"><span data-stu-id="d8876-158">List of ComplexType deviceActionResult objects.</span></span> <span data-ttu-id="d8876-159">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-159">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-160">managementState</span><span class="sxs-lookup"><span data-stu-id="d8876-160">managementState</span></span>|[<span data-ttu-id="d8876-161">managementState</span><span class="sxs-lookup"><span data-stu-id="d8876-161">managementState</span></span>](../resources/intune-devices-managementstate.md)|<span data-ttu-id="d8876-162">Estado de administración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-162">Management state of the device.</span></span> <span data-ttu-id="d8876-163">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-163">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-164">Los valores posibles son: `managed`, `retirePending`, `retireFailed`, `wipePending`, `wipeFailed`, `unhealthy`, `deletePending`, `retireIssued`, `wipeIssued`, `wipeCanceled`, `retireCanceled` y `discovered`.</span><span class="sxs-lookup"><span data-stu-id="d8876-164">Possible values are: `managed`, `retirePending`, `retireFailed`, `wipePending`, `wipeFailed`, `unhealthy`, `deletePending`, `retireIssued`, `wipeIssued`, `wipeCanceled`, `retireCanceled`, `discovered`.</span></span>|
|<span data-ttu-id="d8876-165">enrolledDateTime</span><span class="sxs-lookup"><span data-stu-id="d8876-165">enrolledDateTime</span></span>|<span data-ttu-id="d8876-166">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d8876-166">DateTimeOffset</span></span>|<span data-ttu-id="d8876-167">Hora de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-167">Enrollment time of the device.</span></span> <span data-ttu-id="d8876-168">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-168">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-169">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="d8876-169">lastSyncDateTime</span></span>|<span data-ttu-id="d8876-170">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d8876-170">DateTimeOffset</span></span>|<span data-ttu-id="d8876-171">Fecha y hora en que el dispositivo completó por última vez una sincronización correcta con Intune.</span><span class="sxs-lookup"><span data-stu-id="d8876-171">The date and time that the device last completed a successful sync with Intune.</span></span> <span data-ttu-id="d8876-172">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-172">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-173">chassisType</span><span class="sxs-lookup"><span data-stu-id="d8876-173">chassisType</span></span>|[<span data-ttu-id="d8876-174">chassisType</span><span class="sxs-lookup"><span data-stu-id="d8876-174">chassisType</span></span>](../resources/intune-devices-chassistype.md)|<span data-ttu-id="d8876-175">Tipo de chasis del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-175">Chassis type of the device.</span></span> <span data-ttu-id="d8876-176">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-176">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-177">Los valores posibles son: `unknown`, `desktop`, `laptop`, `worksWorkstation`, `enterpriseServer`, `phone`, `tablet`, `mobileOther` y `mobileUnknown`.</span><span class="sxs-lookup"><span data-stu-id="d8876-177">Possible values are: `unknown`, `desktop`, `laptop`, `worksWorkstation`, `enterpriseServer`, `phone`, `tablet`, `mobileOther`, `mobileUnknown`.</span></span>|
|<span data-ttu-id="d8876-178">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="d8876-178">operatingSystem</span></span>|<span data-ttu-id="d8876-179">String</span><span class="sxs-lookup"><span data-stu-id="d8876-179">String</span></span>|<span data-ttu-id="d8876-180">Sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-180">Operating system of the device.</span></span> <span data-ttu-id="d8876-181">Windows, iOS, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-181">Windows, iOS, etc. Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-182">deviceType</span><span class="sxs-lookup"><span data-stu-id="d8876-182">deviceType</span></span>|[<span data-ttu-id="d8876-183">deviceType</span><span class="sxs-lookup"><span data-stu-id="d8876-183">deviceType</span></span>](../resources/intune-shared-devicetype.md)|<span data-ttu-id="d8876-184">Plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-184">Platform of the device.</span></span> <span data-ttu-id="d8876-185">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-185">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-186">Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="d8876-186">Possible values are: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise`, `blackberry`, `palm`, `unknown`.</span></span>|
|<span data-ttu-id="d8876-187">complianceState</span><span class="sxs-lookup"><span data-stu-id="d8876-187">complianceState</span></span>|[<span data-ttu-id="d8876-188">complianceState</span><span class="sxs-lookup"><span data-stu-id="d8876-188">complianceState</span></span>](../resources/intune-devices-compliancestate.md)|<span data-ttu-id="d8876-189">Estado de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-189">Compliance state of the device.</span></span> <span data-ttu-id="d8876-190">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-190">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-191">Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod` y `configManager`.</span><span class="sxs-lookup"><span data-stu-id="d8876-191">Possible values are: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod`, `configManager`.</span></span>|
|<span data-ttu-id="d8876-192">jailBroken</span><span class="sxs-lookup"><span data-stu-id="d8876-192">jailBroken</span></span>|<span data-ttu-id="d8876-193">String</span><span class="sxs-lookup"><span data-stu-id="d8876-193">String</span></span>|<span data-ttu-id="d8876-194">Indica si se trata de un dispositivo liberado o con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="d8876-194">whether the device is jail broken or rooted.</span></span> <span data-ttu-id="d8876-195">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-195">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-196">managementAgent</span><span class="sxs-lookup"><span data-stu-id="d8876-196">managementAgent</span></span>|[<span data-ttu-id="d8876-197">managementAgentType</span><span class="sxs-lookup"><span data-stu-id="d8876-197">managementAgentType</span></span>](../resources/intune-devices-managementagenttype.md)|<span data-ttu-id="d8876-198">Canal de administración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-198">Management channel of the device.</span></span> <span data-ttu-id="d8876-199">Intune, EAS, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-199">Intune, EAS, etc. Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-200">Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController` y `microsoft365ManagedMdm`.</span><span class="sxs-lookup"><span data-stu-id="d8876-200">Possible values are: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`, `microsoft365ManagedMdm`.</span></span>|
|<span data-ttu-id="d8876-201">osVersion</span><span class="sxs-lookup"><span data-stu-id="d8876-201">osVersion</span></span>|<span data-ttu-id="d8876-202">String</span><span class="sxs-lookup"><span data-stu-id="d8876-202">String</span></span>|<span data-ttu-id="d8876-203">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-203">Operating system version of the device.</span></span> <span data-ttu-id="d8876-204">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-204">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-205">easActivated</span><span class="sxs-lookup"><span data-stu-id="d8876-205">easActivated</span></span>|<span data-ttu-id="d8876-206">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8876-206">Boolean</span></span>|<span data-ttu-id="d8876-207">Indica si el dispositivo tiene Exchange ActiveSync activado.</span><span class="sxs-lookup"><span data-stu-id="d8876-207">Whether the device is Exchange ActiveSync activated.</span></span> <span data-ttu-id="d8876-208">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-208">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-209">easDeviceId</span><span class="sxs-lookup"><span data-stu-id="d8876-209">easDeviceId</span></span>|<span data-ttu-id="d8876-210">String</span><span class="sxs-lookup"><span data-stu-id="d8876-210">String</span></span>|<span data-ttu-id="d8876-211">Identificador de Exchange ActiveSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-211">Exchange ActiveSync Id of the device.</span></span> <span data-ttu-id="d8876-212">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-212">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-213">easActivationDateTime</span><span class="sxs-lookup"><span data-stu-id="d8876-213">easActivationDateTime</span></span>|<span data-ttu-id="d8876-214">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d8876-214">DateTimeOffset</span></span>|<span data-ttu-id="d8876-215">Hora de activación de Exchange ActivationSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-215">Exchange ActivationSync activation time of the device.</span></span> <span data-ttu-id="d8876-216">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-216">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-217">aadRegistered</span><span class="sxs-lookup"><span data-stu-id="d8876-217">aadRegistered</span></span>|<span data-ttu-id="d8876-218">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8876-218">Boolean</span></span>|<span data-ttu-id="d8876-219">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8876-219">Whether the device is Azure Active Directory registered.</span></span> <span data-ttu-id="d8876-220">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-220">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-221">azureADRegistered</span><span class="sxs-lookup"><span data-stu-id="d8876-221">azureADRegistered</span></span>|<span data-ttu-id="d8876-222">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8876-222">Boolean</span></span>|<span data-ttu-id="d8876-223">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8876-223">Whether the device is Azure Active Directory registered.</span></span> <span data-ttu-id="d8876-224">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-224">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-225">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="d8876-225">deviceEnrollmentType</span></span>|[<span data-ttu-id="d8876-226">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="d8876-226">deviceEnrollmentType</span></span>](../resources/intune-shared-deviceenrollmenttype.md)|<span data-ttu-id="d8876-227">Tipo de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-227">Enrollment type of the device.</span></span> <span data-ttu-id="d8876-228">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-228">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-229">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="d8876-229">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="d8876-230">lostModeState</span><span class="sxs-lookup"><span data-stu-id="d8876-230">lostModeState</span></span>|[<span data-ttu-id="d8876-231">lostModeState</span><span class="sxs-lookup"><span data-stu-id="d8876-231">lostModeState</span></span>](../resources/intune-devices-lostmodestate.md)|<span data-ttu-id="d8876-232">Indica si el modo pierden está habilitado o deshabilitado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-232">Indicates if Lost mode is enabled or disabled Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-233">Los valores posibles son: `disabled` y `enabled`.</span><span class="sxs-lookup"><span data-stu-id="d8876-233">Possible values are: `disabled`, `enabled`.</span></span>|
|<span data-ttu-id="d8876-234">activationLockBypassCode</span><span class="sxs-lookup"><span data-stu-id="d8876-234">activationLockBypassCode</span></span>|<span data-ttu-id="d8876-235">String</span><span class="sxs-lookup"><span data-stu-id="d8876-235">String</span></span>|<span data-ttu-id="d8876-236">Código que permite que se omita el bloqueo de activación en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-236">Code that allows the Activation Lock on a device to be bypassed.</span></span> <span data-ttu-id="d8876-237">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-237">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-238">emailAddress</span><span class="sxs-lookup"><span data-stu-id="d8876-238">emailAddress</span></span>|<span data-ttu-id="d8876-239">String</span><span class="sxs-lookup"><span data-stu-id="d8876-239">String</span></span>|<span data-ttu-id="d8876-240">Email(s) para el usuario asociado con el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-240">Email(s) for the user associated with the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-241">azureActiveDirectoryDeviceId</span><span class="sxs-lookup"><span data-stu-id="d8876-241">azureActiveDirectoryDeviceId</span></span>|<span data-ttu-id="d8876-242">String</span><span class="sxs-lookup"><span data-stu-id="d8876-242">String</span></span>|<span data-ttu-id="d8876-243">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8876-243">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="d8876-244">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d8876-244">Read only.</span></span> <span data-ttu-id="d8876-245">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-245">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-246">azureADDeviceId</span><span class="sxs-lookup"><span data-stu-id="d8876-246">azureADDeviceId</span></span>|<span data-ttu-id="d8876-247">String</span><span class="sxs-lookup"><span data-stu-id="d8876-247">String</span></span>|<span data-ttu-id="d8876-248">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d8876-248">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="d8876-249">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d8876-249">Read only.</span></span> <span data-ttu-id="d8876-250">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-250">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-251">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="d8876-251">deviceRegistrationState</span></span>|[<span data-ttu-id="d8876-252">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="d8876-252">deviceRegistrationState</span></span>](../resources/intune-devices-deviceregistrationstate.md)|<span data-ttu-id="d8876-253">Estado de registro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-253">Device registration state.</span></span> <span data-ttu-id="d8876-254">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-254">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-255">Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="d8876-255">Possible values are: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment`, `unknown`.</span></span>|
|<span data-ttu-id="d8876-256">deviceCategoryDisplayName</span><span class="sxs-lookup"><span data-stu-id="d8876-256">deviceCategoryDisplayName</span></span>|<span data-ttu-id="d8876-257">String</span><span class="sxs-lookup"><span data-stu-id="d8876-257">String</span></span>|<span data-ttu-id="d8876-258">Nombre para mostrar categoría dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-258">Device category display name Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-259">isSupervised</span><span class="sxs-lookup"><span data-stu-id="d8876-259">isSupervised</span></span>|<span data-ttu-id="d8876-260">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8876-260">Boolean</span></span>|<span data-ttu-id="d8876-261">Estado del dispositivo supervisado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-261">Device supervised status Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-262">exchangeLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="d8876-262">exchangeLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="d8876-263">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d8876-263">DateTimeOffset</span></span>|<span data-ttu-id="d8876-264">Última vez que el dispositivo estableció contacto con Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8876-264">Last time the device contacted Exchange.</span></span> <span data-ttu-id="d8876-265">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-265">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-266">exchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="d8876-266">exchangeAccessState</span></span>|[<span data-ttu-id="d8876-267">deviceManagementExchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="d8876-267">deviceManagementExchangeAccessState</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstate.md)|<span data-ttu-id="d8876-268">Estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8876-268">The Access State of the device in Exchange.</span></span> <span data-ttu-id="d8876-269">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-269">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-270">Los valores posibles son: `none`, `unknown`, `allowed`, `blocked` y `quarantined`.</span><span class="sxs-lookup"><span data-stu-id="d8876-270">Possible values are: `none`, `unknown`, `allowed`, `blocked`, `quarantined`.</span></span>|
|<span data-ttu-id="d8876-271">exchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="d8876-271">exchangeAccessStateReason</span></span>|[<span data-ttu-id="d8876-272">deviceManagementExchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="d8876-272">deviceManagementExchangeAccessStateReason</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstatereason.md)|<span data-ttu-id="d8876-273">Motivo del estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="d8876-273">The reason for the device's access state in Exchange.</span></span> <span data-ttu-id="d8876-274">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-274">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-275">Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword` y `deviceNotKnownWithManagedApp`.</span><span class="sxs-lookup"><span data-stu-id="d8876-275">Possible values are: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword`, `deviceNotKnownWithManagedApp`.</span></span>|
|<span data-ttu-id="d8876-276">remoteAssistanceSessionUrl</span><span class="sxs-lookup"><span data-stu-id="d8876-276">remoteAssistanceSessionUrl</span></span>|<span data-ttu-id="d8876-277">String</span><span class="sxs-lookup"><span data-stu-id="d8876-277">String</span></span>|<span data-ttu-id="d8876-278">Dirección URL que permite que se establezca una sesión remota con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-278">Url that allows a Remote Assistance session to be established with the device.</span></span> <span data-ttu-id="d8876-279">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-279">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-280">remoteAssistanceSessionErrorDetails</span><span class="sxs-lookup"><span data-stu-id="d8876-280">remoteAssistanceSessionErrorDetails</span></span>|<span data-ttu-id="d8876-281">String</span><span class="sxs-lookup"><span data-stu-id="d8876-281">String</span></span>|<span data-ttu-id="d8876-282">Cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="d8876-282">An error string that identifies issues when creating Remote Assistance session objects.</span></span> <span data-ttu-id="d8876-283">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-283">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-284">isEncrypted</span><span class="sxs-lookup"><span data-stu-id="d8876-284">isEncrypted</span></span>|<span data-ttu-id="d8876-285">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8876-285">Boolean</span></span>|<span data-ttu-id="d8876-286">Estado del dispositivo cifrado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-286">Device encryption status Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-287">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d8876-287">userPrincipalName</span></span>|<span data-ttu-id="d8876-288">String</span><span class="sxs-lookup"><span data-stu-id="d8876-288">String</span></span>|<span data-ttu-id="d8876-289">Dispositivo nombre principal de usuario Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-289">Device user principal name Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-290">model</span><span class="sxs-lookup"><span data-stu-id="d8876-290">model</span></span>|<span data-ttu-id="d8876-291">String</span><span class="sxs-lookup"><span data-stu-id="d8876-291">String</span></span>|<span data-ttu-id="d8876-292">Modelo del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-292">Model of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-293">manufacturer</span><span class="sxs-lookup"><span data-stu-id="d8876-293">manufacturer</span></span>|<span data-ttu-id="d8876-294">String</span><span class="sxs-lookup"><span data-stu-id="d8876-294">String</span></span>|<span data-ttu-id="d8876-295">Fabricante del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-295">Manufacturer of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-296">imei</span><span class="sxs-lookup"><span data-stu-id="d8876-296">imei</span></span>|<span data-ttu-id="d8876-297">String</span><span class="sxs-lookup"><span data-stu-id="d8876-297">String</span></span>|<span data-ttu-id="d8876-298">IMEI se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-298">IMEI Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-299">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="d8876-299">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="d8876-300">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d8876-300">DateTimeOffset</span></span>|<span data-ttu-id="d8876-301">La fecha y hora en período de gracia de cumplimiento de normas de dispositivo expira Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-301">The DateTime when device compliance grace period expires Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-302">serialNumber</span><span class="sxs-lookup"><span data-stu-id="d8876-302">serialNumber</span></span>|<span data-ttu-id="d8876-303">String</span><span class="sxs-lookup"><span data-stu-id="d8876-303">String</span></span>|<span data-ttu-id="d8876-304">SerialNumber heredado de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-304">SerialNumber Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-305">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="d8876-305">phoneNumber</span></span>|<span data-ttu-id="d8876-306">String</span><span class="sxs-lookup"><span data-stu-id="d8876-306">String</span></span>|<span data-ttu-id="d8876-307">Número de teléfono del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-307">Phone number of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-308">androidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="d8876-308">androidSecurityPatchLevel</span></span>|<span data-ttu-id="d8876-309">String</span><span class="sxs-lookup"><span data-stu-id="d8876-309">String</span></span>|<span data-ttu-id="d8876-310">Nivel de revisión de seguridad para Android Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-310">Android security patch level Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-311">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="d8876-311">userDisplayName</span></span>|<span data-ttu-id="d8876-312">String</span><span class="sxs-lookup"><span data-stu-id="d8876-312">String</span></span>|<span data-ttu-id="d8876-313">Nombre de usuario para mostrar Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-313">User display name Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-314">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="d8876-314">configurationManagerClientEnabledFeatures</span></span>|[<span data-ttu-id="d8876-315">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="d8876-315">configurationManagerClientEnabledFeatures</span></span>](../resources/intune-devices-configurationmanagerclientenabledfeatures.md)|<span data-ttu-id="d8876-316">ConfigrMgr cliente habilitado para las características Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-316">ConfigrMgr client enabled features Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-317">wiFiMacAddress</span><span class="sxs-lookup"><span data-stu-id="d8876-317">wiFiMacAddress</span></span>|<span data-ttu-id="d8876-318">String</span><span class="sxs-lookup"><span data-stu-id="d8876-318">String</span></span>|<span data-ttu-id="d8876-319">Wi-Fi MAC se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-319">Wi-Fi MAC Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-320">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="d8876-320">deviceHealthAttestationState</span></span>|[<span data-ttu-id="d8876-321">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="d8876-321">deviceHealthAttestationState</span></span>](../resources/intune-devices-devicehealthattestationstate.md)|<span data-ttu-id="d8876-322">Estado de la atestación de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-322">The device health attestation state.</span></span> <span data-ttu-id="d8876-323">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-323">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-324">subscriberCarrier</span><span class="sxs-lookup"><span data-stu-id="d8876-324">subscriberCarrier</span></span>|<span data-ttu-id="d8876-325">String</span><span class="sxs-lookup"><span data-stu-id="d8876-325">String</span></span>|<span data-ttu-id="d8876-326">Operador de suscriptor se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-326">Subscriber Carrier Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-327">meid</span><span class="sxs-lookup"><span data-stu-id="d8876-327">meid</span></span>|<span data-ttu-id="d8876-328">String</span><span class="sxs-lookup"><span data-stu-id="d8876-328">String</span></span>|<span data-ttu-id="d8876-329">MEID se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-329">MEID Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-330">totalStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="d8876-330">totalStorageSpaceInBytes</span></span>|<span data-ttu-id="d8876-331">Int64</span><span class="sxs-lookup"><span data-stu-id="d8876-331">Int64</span></span>|<span data-ttu-id="d8876-332">Almacenamiento total en Bytes se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-332">Total Storage in Bytes Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-333">freeStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="d8876-333">freeStorageSpaceInBytes</span></span>|<span data-ttu-id="d8876-334">Int64</span><span class="sxs-lookup"><span data-stu-id="d8876-334">Int64</span></span>|<span data-ttu-id="d8876-335">Espacio de almacenamiento en Bytes se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-335">Free Storage in Bytes Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-336">managedDeviceName</span><span class="sxs-lookup"><span data-stu-id="d8876-336">managedDeviceName</span></span>|<span data-ttu-id="d8876-337">String</span><span class="sxs-lookup"><span data-stu-id="d8876-337">String</span></span>|<span data-ttu-id="d8876-338">Nombre generado automáticamente para identificar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-338">Automatically generated name to identify a device.</span></span> <span data-ttu-id="d8876-339">Se puede sobrescribir con un nombre descriptivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="d8876-339">Can be overwritten to a user friendly name.</span></span> <span data-ttu-id="d8876-340">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-340">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-341">partnerReportedThreatState</span><span class="sxs-lookup"><span data-stu-id="d8876-341">partnerReportedThreatState</span></span>|[<span data-ttu-id="d8876-342">managedDevicePartnerReportedHealthState</span><span class="sxs-lookup"><span data-stu-id="d8876-342">managedDevicePartnerReportedHealthState</span></span>](../resources/intune-devices-manageddevicepartnerreportedhealthstate.md)|<span data-ttu-id="d8876-343">Indica el estado de amenazas de un dispositivo cuando la cuenta y el dispositivo usan un partner de Mobile Threat Defense.</span><span class="sxs-lookup"><span data-stu-id="d8876-343">Indicates the threat state of a device when a Mobile Threat Defense partner is in use by the account and device.</span></span> <span data-ttu-id="d8876-344">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d8876-344">Read Only.</span></span> <span data-ttu-id="d8876-345">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="d8876-345">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="d8876-346">Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised` y `misconfigured`.</span><span class="sxs-lookup"><span data-stu-id="d8876-346">Possible values are: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised`, `misconfigured`.</span></span>|
|<span data-ttu-id="d8876-347">usersLoggedOn</span><span class="sxs-lookup"><span data-stu-id="d8876-347">usersLoggedOn</span></span>|<span data-ttu-id="d8876-348">colección de [loggedOnUser](../resources/intune-devices-loggedonuser.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-348">[loggedOnUser](../resources/intune-devices-loggedonuser.md) collection</span></span>|<span data-ttu-id="d8876-349">Indica la última sesión a los usuarios de un dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-349">Indicates the last logged on users of a device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-350">preferMdmOverGroupPolicyAppliedDateTime</span><span class="sxs-lookup"><span data-stu-id="d8876-350">preferMdmOverGroupPolicyAppliedDateTime</span></span>|<span data-ttu-id="d8876-351">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d8876-351">DateTimeOffset</span></span>|<span data-ttu-id="d8876-352">Informes la fecha y hora de que la configuración de preferMdmOverGroupPolicy se estableció.</span><span class="sxs-lookup"><span data-stu-id="d8876-352">Reports the DateTime the preferMdmOverGroupPolicy setting was set.</span></span>  <span data-ttu-id="d8876-353">Cuando se establece, la configuración MDM Intune invalidará la configuración de directiva de grupo si hay un conflicto.</span><span class="sxs-lookup"><span data-stu-id="d8876-353">When set, the Intune MDM settings will override Group Policy settings if there is a conflict.</span></span> <span data-ttu-id="d8876-354">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d8876-354">Read Only.</span></span> <span data-ttu-id="d8876-355">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-355">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-356">autopilotEnrolled</span><span class="sxs-lookup"><span data-stu-id="d8876-356">autopilotEnrolled</span></span>|<span data-ttu-id="d8876-357">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8876-357">Boolean</span></span>|<span data-ttu-id="d8876-358">Informa de si el dispositivo administrado está inscrito a través de piloto automático.</span><span class="sxs-lookup"><span data-stu-id="d8876-358">Reports if the managed device is enrolled via auto-pilot.</span></span> <span data-ttu-id="d8876-359">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-359">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-360">requireUserEnrollmentApproval</span><span class="sxs-lookup"><span data-stu-id="d8876-360">requireUserEnrollmentApproval</span></span>|<span data-ttu-id="d8876-361">Boolean</span><span class="sxs-lookup"><span data-stu-id="d8876-361">Boolean</span></span>|<span data-ttu-id="d8876-362">Informa de si el dispositivo iOS administrada es inscripción de aprobación del usuario.</span><span class="sxs-lookup"><span data-stu-id="d8876-362">Reports if the managed iOS device is user approval enrollment.</span></span> <span data-ttu-id="d8876-363">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-363">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-364">managementCertificateExpirationDate</span><span class="sxs-lookup"><span data-stu-id="d8876-364">managementCertificateExpirationDate</span></span>|<span data-ttu-id="d8876-365">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d8876-365">DateTimeOffset</span></span>|<span data-ttu-id="d8876-366">Informes de dispositivo administración certificado fecha de caducidad Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-366">Reports device management certificate expiration date Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-367">iccid</span><span class="sxs-lookup"><span data-stu-id="d8876-367">iccid</span></span>|<span data-ttu-id="d8876-368">String</span><span class="sxs-lookup"><span data-stu-id="d8876-368">String</span></span>|<span data-ttu-id="d8876-369">Identificador de la tarjeta de circuitos integrados, es número de identificación único de la tarjeta SIM A.</span><span class="sxs-lookup"><span data-stu-id="d8876-369">Integrated Circuit Card Identifier, it is A SIM card's unique identification number.</span></span> <span data-ttu-id="d8876-370">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-370">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-371">UDID</span><span class="sxs-lookup"><span data-stu-id="d8876-371">udid</span></span>|<span data-ttu-id="d8876-372">String</span><span class="sxs-lookup"><span data-stu-id="d8876-372">String</span></span>|<span data-ttu-id="d8876-373">Identificador único de dispositivo para dispositivos iOS y Mac OS.</span><span class="sxs-lookup"><span data-stu-id="d8876-373">Unique Device Identifier for iOS and macOS devices.</span></span> <span data-ttu-id="d8876-374">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-374">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-375">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="d8876-375">roleScopeTagIds</span></span>|<span data-ttu-id="d8876-376">Colección String</span><span class="sxs-lookup"><span data-stu-id="d8876-376">String collection</span></span>|<span data-ttu-id="d8876-377">Lista de identificadores de etiqueta de ámbito para esta instancia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8876-377">List of Scope Tag IDs for this Device instance.</span></span> <span data-ttu-id="d8876-378">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-378">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-379">windowsActiveMalwareCount</span><span class="sxs-lookup"><span data-stu-id="d8876-379">windowsActiveMalwareCount</span></span>|<span data-ttu-id="d8876-380">Int32</span><span class="sxs-lookup"><span data-stu-id="d8876-380">Int32</span></span>|<span data-ttu-id="d8876-381">Recuento de malware para este dispositivo windows Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-381">Count of active malware for this windows device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-382">windowsRemediatedMalwareCount</span><span class="sxs-lookup"><span data-stu-id="d8876-382">windowsRemediatedMalwareCount</span></span>|<span data-ttu-id="d8876-383">Int32</span><span class="sxs-lookup"><span data-stu-id="d8876-383">Int32</span></span>|<span data-ttu-id="d8876-384">Recuento de malware corregidos con pruebas para este dispositivo windows Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-384">Count of remediated malware for this windows device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-385">notas</span><span class="sxs-lookup"><span data-stu-id="d8876-385">notes</span></span>|<span data-ttu-id="d8876-386">String</span><span class="sxs-lookup"><span data-stu-id="d8876-386">String</span></span>|<span data-ttu-id="d8876-387">Notas en el dispositivo creado mediante la administración de TI se hereda desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-387">Notes on the device created by IT Admin Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="d8876-388">configurationManagerClientHealthState</span><span class="sxs-lookup"><span data-stu-id="d8876-388">configurationManagerClientHealthState</span></span>|[<span data-ttu-id="d8876-389">configurationManagerClientHealthState</span><span class="sxs-lookup"><span data-stu-id="d8876-389">configurationManagerClientHealthState</span></span>](../resources/intune-devices-configurationmanagerclienthealthstate.md)|<span data-ttu-id="d8876-390">Configuración Administrador cliente estado de mantenimiento, válido sólo para los dispositivos administrados por MDM/ConfigMgr heredado de agente de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="d8876-390">Configuration manager client health state, valid only for devices managed by MDM/ConfigMgr Agent Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|



## <a name="response"></a><span data-ttu-id="d8876-391">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8876-391">Response</span></span>
<span data-ttu-id="d8876-392">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d8876-392">If successful, this method returns a `201 Created` response code and a [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d8876-393">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d8876-393">Example</span></span>
### <a name="request"></a><span data-ttu-id="d8876-394">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d8876-394">Request</span></span>
<span data-ttu-id="d8876-395">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8876-395">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/users/{usersId}/managedDevices
Content-type: application/json
Content-length: 7173

{
  "@odata.type": "#microsoft.graph.windowsManagedDevice",
  "userId": "User Id value",
  "deviceName": "Device Name value",
  "hardwareInformation": {
    "@odata.type": "microsoft.graph.hardwareInformation",
    "serialNumber": "Serial Number value",
    "totalStorageSpace": 1,
    "freeStorageSpace": 0,
    "imei": "Imei value",
    "meid": "Meid value",
    "manufacturer": "Manufacturer value",
    "model": "Model value",
    "phoneNumber": "Phone Number value",
    "subscriberCarrier": "Subscriber Carrier value",
    "cellularTechnology": "Cellular Technology value",
    "wifiMac": "Wifi Mac value",
    "operatingSystemLanguage": "Operating System Language value",
    "isSupervised": true,
    "isEncrypted": true,
    "isSharedDevice": true,
    "sharedDeviceCachedUsers": [
      {
        "@odata.type": "microsoft.graph.sharedAppleDeviceUser",
        "userPrincipalName": "User Principal Name value",
        "dataToSync": true,
        "dataQuota": 9,
        "dataUsed": 8
      }
    ],
    "tpmSpecificationVersion": "Tpm Specification Version value",
    "operatingSystemEdition": "Operating System Edition value",
    "deviceFullQualifiedDomainName": "Device Full Qualified Domain Name value",
    "deviceGuardVirtualizationBasedSecurityHardwareRequirementState": "secureBootRequired",
    "deviceGuardVirtualizationBasedSecurityState": "rebootRequired",
    "deviceGuardLocalSystemAuthorityCredentialGuardState": "rebootRequired"
  },
  "ownerType": "company",
  "managedDeviceOwnerType": "company",
  "deviceActionResults": [
    {
      "@odata.type": "microsoft.graph.deviceActionResult",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ],
  "managementState": "retirePending",
  "enrolledDateTime": "2016-12-31T23:59:43.797191-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "chassisType": "desktop",
  "operatingSystem": "Operating System value",
  "deviceType": "windowsRT",
  "complianceState": "compliant",
  "jailBroken": "Jail Broken value",
  "managementAgent": "mdm",
  "osVersion": "Os Version value",
  "easActivated": true,
  "easDeviceId": "Eas Device Id value",
  "easActivationDateTime": "2016-12-31T23:59:43.4878784-08:00",
  "aadRegistered": true,
  "azureADRegistered": true,
  "deviceEnrollmentType": "userEnrollment",
  "lostModeState": "enabled",
  "activationLockBypassCode": "Activation Lock Bypass Code value",
  "emailAddress": "Email Address value",
  "azureActiveDirectoryDeviceId": "Azure Active Directory Device Id value",
  "azureADDeviceId": "Azure ADDevice Id value",
  "deviceRegistrationState": "registered",
  "deviceCategoryDisplayName": "Device Category Display Name value",
  "isSupervised": true,
  "exchangeLastSuccessfulSyncDateTime": "2017-01-01T00:00:45.8803083-08:00",
  "exchangeAccessState": "unknown",
  "exchangeAccessStateReason": "unknown",
  "remoteAssistanceSessionUrl": "https://example.com/remoteAssistanceSessionUrl/",
  "remoteAssistanceSessionErrorDetails": "Remote Assistance Session Error Details value",
  "isEncrypted": true,
  "userPrincipalName": "User Principal Name value",
  "model": "Model value",
  "manufacturer": "Manufacturer value",
  "imei": "Imei value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "serialNumber": "Serial Number value",
  "phoneNumber": "Phone Number value",
  "androidSecurityPatchLevel": "Android Security Patch Level value",
  "userDisplayName": "User Display Name value",
  "configurationManagerClientEnabledFeatures": {
    "@odata.type": "microsoft.graph.configurationManagerClientEnabledFeatures",
    "inventory": true,
    "modernApps": true,
    "resourceAccess": true,
    "deviceConfiguration": true,
    "compliancePolicy": true,
    "windowsUpdateForBusiness": true
  },
  "wiFiMacAddress": "Wi Fi Mac Address value",
  "deviceHealthAttestationState": {
    "@odata.type": "microsoft.graph.deviceHealthAttestationState",
    "lastUpdateDateTime": "Last Update Date Time value",
    "contentNamespaceUrl": "https://example.com/contentNamespaceUrl/",
    "deviceHealthAttestationStatus": "Device Health Attestation Status value",
    "contentVersion": "Content Version value",
    "issuedDateTime": "2016-12-31T23:58:22.1231038-08:00",
    "attestationIdentityKey": "Attestation Identity Key value",
    "resetCount": 10,
    "restartCount": 12,
    "dataExcutionPolicy": "Data Excution Policy value",
    "bitLockerStatus": "Bit Locker Status value",
    "bootManagerVersion": "Boot Manager Version value",
    "codeIntegrityCheckVersion": "Code Integrity Check Version value",
    "secureBoot": "Secure Boot value",
    "bootDebugging": "Boot Debugging value",
    "operatingSystemKernelDebugging": "Operating System Kernel Debugging value",
    "codeIntegrity": "Code Integrity value",
    "testSigning": "Test Signing value",
    "safeMode": "Safe Mode value",
    "windowsPE": "Windows PE value",
    "earlyLaunchAntiMalwareDriverProtection": "Early Launch Anti Malware Driver Protection value",
    "virtualSecureMode": "Virtual Secure Mode value",
    "pcrHashAlgorithm": "Pcr Hash Algorithm value",
    "bootAppSecurityVersion": "Boot App Security Version value",
    "bootManagerSecurityVersion": "Boot Manager Security Version value",
    "tpmVersion": "Tpm Version value",
    "pcr0": "Pcr0 value",
    "secureBootConfigurationPolicyFingerPrint": "Secure Boot Configuration Policy Finger Print value",
    "codeIntegrityPolicy": "Code Integrity Policy value",
    "bootRevisionListInfo": "Boot Revision List Info value",
    "operatingSystemRevListInfo": "Operating System Rev List Info value",
    "healthStatusMismatchInfo": "Health Status Mismatch Info value",
    "healthAttestationSupportedStatus": "Health Attestation Supported Status value"
  },
  "subscriberCarrier": "Subscriber Carrier value",
  "meid": "Meid value",
  "totalStorageSpaceInBytes": 8,
  "freeStorageSpaceInBytes": 7,
  "managedDeviceName": "Managed Device Name value",
  "partnerReportedThreatState": "activated",
  "usersLoggedOn": [
    {
      "@odata.type": "microsoft.graph.loggedOnUser",
      "userId": "User Id value",
      "lastLogOnDateTime": "2016-12-31T23:58:37.4262708-08:00"
    }
  ],
  "preferMdmOverGroupPolicyAppliedDateTime": "2016-12-31T23:57:34.4649887-08:00",
  "autopilotEnrolled": true,
  "requireUserEnrollmentApproval": true,
  "managementCertificateExpirationDate": "2016-12-31T23:57:59.9789653-08:00",
  "iccid": "Iccid value",
  "udid": "Udid value",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "windowsActiveMalwareCount": 9,
  "windowsRemediatedMalwareCount": 13,
  "notes": "Notes value",
  "configurationManagerClientHealthState": {
    "@odata.type": "microsoft.graph.configurationManagerClientHealthState",
    "state": "installed",
    "errorCode": 9,
    "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00"
  }
}
```

### <a name="response"></a><span data-ttu-id="d8876-396">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d8876-396">Response</span></span>
<span data-ttu-id="d8876-p142">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d8876-p142">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 7222

{
  "@odata.type": "#microsoft.graph.windowsManagedDevice",
  "id": "97842b67-2b67-9784-672b-8497672b8497",
  "userId": "User Id value",
  "deviceName": "Device Name value",
  "hardwareInformation": {
    "@odata.type": "microsoft.graph.hardwareInformation",
    "serialNumber": "Serial Number value",
    "totalStorageSpace": 1,
    "freeStorageSpace": 0,
    "imei": "Imei value",
    "meid": "Meid value",
    "manufacturer": "Manufacturer value",
    "model": "Model value",
    "phoneNumber": "Phone Number value",
    "subscriberCarrier": "Subscriber Carrier value",
    "cellularTechnology": "Cellular Technology value",
    "wifiMac": "Wifi Mac value",
    "operatingSystemLanguage": "Operating System Language value",
    "isSupervised": true,
    "isEncrypted": true,
    "isSharedDevice": true,
    "sharedDeviceCachedUsers": [
      {
        "@odata.type": "microsoft.graph.sharedAppleDeviceUser",
        "userPrincipalName": "User Principal Name value",
        "dataToSync": true,
        "dataQuota": 9,
        "dataUsed": 8
      }
    ],
    "tpmSpecificationVersion": "Tpm Specification Version value",
    "operatingSystemEdition": "Operating System Edition value",
    "deviceFullQualifiedDomainName": "Device Full Qualified Domain Name value",
    "deviceGuardVirtualizationBasedSecurityHardwareRequirementState": "secureBootRequired",
    "deviceGuardVirtualizationBasedSecurityState": "rebootRequired",
    "deviceGuardLocalSystemAuthorityCredentialGuardState": "rebootRequired"
  },
  "ownerType": "company",
  "managedDeviceOwnerType": "company",
  "deviceActionResults": [
    {
      "@odata.type": "microsoft.graph.deviceActionResult",
      "actionName": "Action Name value",
      "actionState": "pending",
      "startDateTime": "2016-12-31T23:58:46.7156189-08:00",
      "lastUpdatedDateTime": "2017-01-01T00:00:56.8321556-08:00"
    }
  ],
  "managementState": "retirePending",
  "enrolledDateTime": "2016-12-31T23:59:43.797191-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "chassisType": "desktop",
  "operatingSystem": "Operating System value",
  "deviceType": "windowsRT",
  "complianceState": "compliant",
  "jailBroken": "Jail Broken value",
  "managementAgent": "mdm",
  "osVersion": "Os Version value",
  "easActivated": true,
  "easDeviceId": "Eas Device Id value",
  "easActivationDateTime": "2016-12-31T23:59:43.4878784-08:00",
  "aadRegistered": true,
  "azureADRegistered": true,
  "deviceEnrollmentType": "userEnrollment",
  "lostModeState": "enabled",
  "activationLockBypassCode": "Activation Lock Bypass Code value",
  "emailAddress": "Email Address value",
  "azureActiveDirectoryDeviceId": "Azure Active Directory Device Id value",
  "azureADDeviceId": "Azure ADDevice Id value",
  "deviceRegistrationState": "registered",
  "deviceCategoryDisplayName": "Device Category Display Name value",
  "isSupervised": true,
  "exchangeLastSuccessfulSyncDateTime": "2017-01-01T00:00:45.8803083-08:00",
  "exchangeAccessState": "unknown",
  "exchangeAccessStateReason": "unknown",
  "remoteAssistanceSessionUrl": "https://example.com/remoteAssistanceSessionUrl/",
  "remoteAssistanceSessionErrorDetails": "Remote Assistance Session Error Details value",
  "isEncrypted": true,
  "userPrincipalName": "User Principal Name value",
  "model": "Model value",
  "manufacturer": "Manufacturer value",
  "imei": "Imei value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "serialNumber": "Serial Number value",
  "phoneNumber": "Phone Number value",
  "androidSecurityPatchLevel": "Android Security Patch Level value",
  "userDisplayName": "User Display Name value",
  "configurationManagerClientEnabledFeatures": {
    "@odata.type": "microsoft.graph.configurationManagerClientEnabledFeatures",
    "inventory": true,
    "modernApps": true,
    "resourceAccess": true,
    "deviceConfiguration": true,
    "compliancePolicy": true,
    "windowsUpdateForBusiness": true
  },
  "wiFiMacAddress": "Wi Fi Mac Address value",
  "deviceHealthAttestationState": {
    "@odata.type": "microsoft.graph.deviceHealthAttestationState",
    "lastUpdateDateTime": "Last Update Date Time value",
    "contentNamespaceUrl": "https://example.com/contentNamespaceUrl/",
    "deviceHealthAttestationStatus": "Device Health Attestation Status value",
    "contentVersion": "Content Version value",
    "issuedDateTime": "2016-12-31T23:58:22.1231038-08:00",
    "attestationIdentityKey": "Attestation Identity Key value",
    "resetCount": 10,
    "restartCount": 12,
    "dataExcutionPolicy": "Data Excution Policy value",
    "bitLockerStatus": "Bit Locker Status value",
    "bootManagerVersion": "Boot Manager Version value",
    "codeIntegrityCheckVersion": "Code Integrity Check Version value",
    "secureBoot": "Secure Boot value",
    "bootDebugging": "Boot Debugging value",
    "operatingSystemKernelDebugging": "Operating System Kernel Debugging value",
    "codeIntegrity": "Code Integrity value",
    "testSigning": "Test Signing value",
    "safeMode": "Safe Mode value",
    "windowsPE": "Windows PE value",
    "earlyLaunchAntiMalwareDriverProtection": "Early Launch Anti Malware Driver Protection value",
    "virtualSecureMode": "Virtual Secure Mode value",
    "pcrHashAlgorithm": "Pcr Hash Algorithm value",
    "bootAppSecurityVersion": "Boot App Security Version value",
    "bootManagerSecurityVersion": "Boot Manager Security Version value",
    "tpmVersion": "Tpm Version value",
    "pcr0": "Pcr0 value",
    "secureBootConfigurationPolicyFingerPrint": "Secure Boot Configuration Policy Finger Print value",
    "codeIntegrityPolicy": "Code Integrity Policy value",
    "bootRevisionListInfo": "Boot Revision List Info value",
    "operatingSystemRevListInfo": "Operating System Rev List Info value",
    "healthStatusMismatchInfo": "Health Status Mismatch Info value",
    "healthAttestationSupportedStatus": "Health Attestation Supported Status value"
  },
  "subscriberCarrier": "Subscriber Carrier value",
  "meid": "Meid value",
  "totalStorageSpaceInBytes": 8,
  "freeStorageSpaceInBytes": 7,
  "managedDeviceName": "Managed Device Name value",
  "partnerReportedThreatState": "activated",
  "usersLoggedOn": [
    {
      "@odata.type": "microsoft.graph.loggedOnUser",
      "userId": "User Id value",
      "lastLogOnDateTime": "2016-12-31T23:58:37.4262708-08:00"
    }
  ],
  "preferMdmOverGroupPolicyAppliedDateTime": "2016-12-31T23:57:34.4649887-08:00",
  "autopilotEnrolled": true,
  "requireUserEnrollmentApproval": true,
  "managementCertificateExpirationDate": "2016-12-31T23:57:59.9789653-08:00",
  "iccid": "Iccid value",
  "udid": "Udid value",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "windowsActiveMalwareCount": 9,
  "windowsRemediatedMalwareCount": 13,
  "notes": "Notes value",
  "configurationManagerClientHealthState": {
    "@odata.type": "microsoft.graph.configurationManagerClientHealthState",
    "state": "installed",
    "errorCode": 9,
    "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00"
  }
}
```





