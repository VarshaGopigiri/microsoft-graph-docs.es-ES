---
title: Actualizar windowsManagedDevice
description: Actualizar las propiedades de un objeto windowsManagedDevice.
author: tfitzmac
ms.openlocfilehash: d1aa637a513d45ad33a1a5990399cf35f4cb21ae
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347638"
---
# <a name="update-windowsmanageddevice"></a><span data-ttu-id="f3c07-103">Actualizar windowsManagedDevice</span><span class="sxs-lookup"><span data-stu-id="f3c07-103">Update windowsManagedDevice</span></span>

> <span data-ttu-id="f3c07-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f3c07-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f3c07-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f3c07-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f3c07-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f3c07-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f3c07-107">Actualizar las propiedades de un objeto [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c07-107">Update the properties of a [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f3c07-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f3c07-108">Prerequisites</span></span>
<span data-ttu-id="f3c07-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f3c07-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f3c07-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f3c07-111">Permission type</span></span>|<span data-ttu-id="f3c07-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f3c07-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f3c07-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f3c07-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f3c07-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f3c07-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="f3c07-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f3c07-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f3c07-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3c07-116">Not supported.</span></span>|
|<span data-ttu-id="f3c07-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f3c07-117">Application</span></span>|<span data-ttu-id="f3c07-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f3c07-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f3c07-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f3c07-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}/managedDevices/{managedDeviceId}
PATCH /deviceManagement/managedDevices/{managedDeviceId}
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice
PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}
```

## <a name="request-headers"></a><span data-ttu-id="f3c07-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f3c07-120">Request headers</span></span>
|<span data-ttu-id="f3c07-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f3c07-121">Header</span></span>|<span data-ttu-id="f3c07-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f3c07-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f3c07-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f3c07-123">Authorization</span></span>|<span data-ttu-id="f3c07-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f3c07-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f3c07-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f3c07-125">Accept</span></span>|<span data-ttu-id="f3c07-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f3c07-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f3c07-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f3c07-127">Request body</span></span>
<span data-ttu-id="f3c07-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) .</span><span class="sxs-lookup"><span data-stu-id="f3c07-128">In the request body, supply a JSON representation for the [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) object.</span></span>

<span data-ttu-id="f3c07-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-129">The following table shows the properties that are required when you create the [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md).</span></span>

|<span data-ttu-id="f3c07-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f3c07-130">Property</span></span>|<span data-ttu-id="f3c07-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f3c07-131">Type</span></span>|<span data-ttu-id="f3c07-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3c07-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f3c07-133">id</span><span class="sxs-lookup"><span data-stu-id="f3c07-133">id</span></span>|<span data-ttu-id="f3c07-134">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-134">String</span></span>|<span data-ttu-id="f3c07-135">Identificador único para el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-135">Unique Identifier for the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-136">userId</span><span class="sxs-lookup"><span data-stu-id="f3c07-136">userId</span></span>|<span data-ttu-id="f3c07-137">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-137">String</span></span>|<span data-ttu-id="f3c07-138">Identificador único para el usuario asociado con el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-138">Unique Identifier for the user associated with the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-139">deviceName</span><span class="sxs-lookup"><span data-stu-id="f3c07-139">deviceName</span></span>|<span data-ttu-id="f3c07-140">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-140">String</span></span>|<span data-ttu-id="f3c07-141">Nombre del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-141">Name of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-142">hardwareInformation</span><span class="sxs-lookup"><span data-stu-id="f3c07-142">hardwareInformation</span></span>|[<span data-ttu-id="f3c07-143">hardwareInformation</span><span class="sxs-lookup"><span data-stu-id="f3c07-143">hardwareInformation</span></span>](../resources/intune-devices-hardwareinformation.md)|<span data-ttu-id="f3c07-144">Los detalles de hardward para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-144">The hardward details for the device.</span></span>  <span data-ttu-id="f3c07-145">Incluye información como el espacio de almacenamiento, el fabricante, el número de serie, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-145">Includes information such as storage space, manufacturer, serial number, etc. Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-146">ownerType</span><span class="sxs-lookup"><span data-stu-id="f3c07-146">ownerType</span></span>|[<span data-ttu-id="f3c07-147">ownerType</span><span class="sxs-lookup"><span data-stu-id="f3c07-147">ownerType</span></span>](../resources/intune-devices-ownertype.md)|<span data-ttu-id="f3c07-148">Propietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-148">Ownership of the device.</span></span> <span data-ttu-id="f3c07-149">Puede ser 'compañía' o 'personal' heredado de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-149">Can be 'company' or 'personal' Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-150">Los valores posibles son: `unknown`, `company` y `personal`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-150">Possible values are: `unknown`, `company`, `personal`.</span></span>|
|<span data-ttu-id="f3c07-151">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="f3c07-151">managedDeviceOwnerType</span></span>|[<span data-ttu-id="f3c07-152">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="f3c07-152">managedDeviceOwnerType</span></span>](../resources/intune-devices-manageddeviceownertype.md)|<span data-ttu-id="f3c07-153">Propietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-153">Ownership of the device.</span></span> <span data-ttu-id="f3c07-154">Puede ser 'compañía' o 'personal' heredado de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-154">Can be 'company' or 'personal' Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-155">Los valores posibles son: `unknown`, `company` y `personal`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-155">Possible values are: `unknown`, `company`, `personal`.</span></span>|
|<span data-ttu-id="f3c07-156">deviceActionResults</span><span class="sxs-lookup"><span data-stu-id="f3c07-156">deviceActionResults</span></span>|<span data-ttu-id="f3c07-157">Colección [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-157">[deviceActionResult](../resources/intune-devices-deviceactionresult.md) collection</span></span>|<span data-ttu-id="f3c07-158">Lista de objetos deviceActionResult ComplexType.</span><span class="sxs-lookup"><span data-stu-id="f3c07-158">List of ComplexType deviceActionResult objects.</span></span> <span data-ttu-id="f3c07-159">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-159">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-160">managementState</span><span class="sxs-lookup"><span data-stu-id="f3c07-160">managementState</span></span>|[<span data-ttu-id="f3c07-161">managementState</span><span class="sxs-lookup"><span data-stu-id="f3c07-161">managementState</span></span>](../resources/intune-devices-managementstate.md)|<span data-ttu-id="f3c07-162">Estado de administración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-162">Management state of the device.</span></span> <span data-ttu-id="f3c07-163">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-163">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-164">Los valores posibles son: `managed`, `retirePending`, `retireFailed`, `wipePending`, `wipeFailed`, `unhealthy`, `deletePending`, `retireIssued`, `wipeIssued`, `wipeCanceled`, `retireCanceled` y `discovered`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-164">Possible values are: `managed`, `retirePending`, `retireFailed`, `wipePending`, `wipeFailed`, `unhealthy`, `deletePending`, `retireIssued`, `wipeIssued`, `wipeCanceled`, `retireCanceled`, `discovered`.</span></span>|
|<span data-ttu-id="f3c07-165">enrolledDateTime</span><span class="sxs-lookup"><span data-stu-id="f3c07-165">enrolledDateTime</span></span>|<span data-ttu-id="f3c07-166">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f3c07-166">DateTimeOffset</span></span>|<span data-ttu-id="f3c07-167">Hora de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-167">Enrollment time of the device.</span></span> <span data-ttu-id="f3c07-168">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-168">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-169">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="f3c07-169">lastSyncDateTime</span></span>|<span data-ttu-id="f3c07-170">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f3c07-170">DateTimeOffset</span></span>|<span data-ttu-id="f3c07-171">Fecha y hora en que el dispositivo completó por última vez una sincronización correcta con Intune.</span><span class="sxs-lookup"><span data-stu-id="f3c07-171">The date and time that the device last completed a successful sync with Intune.</span></span> <span data-ttu-id="f3c07-172">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-172">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-173">chassisType</span><span class="sxs-lookup"><span data-stu-id="f3c07-173">chassisType</span></span>|[<span data-ttu-id="f3c07-174">chassisType</span><span class="sxs-lookup"><span data-stu-id="f3c07-174">chassisType</span></span>](../resources/intune-devices-chassistype.md)|<span data-ttu-id="f3c07-175">Tipo de chasis del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-175">Chassis type of the device.</span></span> <span data-ttu-id="f3c07-176">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-176">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-177">Los valores posibles son: `unknown`, `desktop`, `laptop`, `worksWorkstation`, `enterpriseServer`, `phone`, `tablet`, `mobileOther` y `mobileUnknown`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-177">Possible values are: `unknown`, `desktop`, `laptop`, `worksWorkstation`, `enterpriseServer`, `phone`, `tablet`, `mobileOther`, `mobileUnknown`.</span></span>|
|<span data-ttu-id="f3c07-178">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="f3c07-178">operatingSystem</span></span>|<span data-ttu-id="f3c07-179">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-179">String</span></span>|<span data-ttu-id="f3c07-180">Sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-180">Operating system of the device.</span></span> <span data-ttu-id="f3c07-181">Windows, iOS, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-181">Windows, iOS, etc. Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-182">deviceType</span><span class="sxs-lookup"><span data-stu-id="f3c07-182">deviceType</span></span>|[<span data-ttu-id="f3c07-183">deviceType</span><span class="sxs-lookup"><span data-stu-id="f3c07-183">deviceType</span></span>](../resources/intune-shared-devicetype.md)|<span data-ttu-id="f3c07-184">Plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-184">Platform of the device.</span></span> <span data-ttu-id="f3c07-185">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-185">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-186">Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-186">Possible values are: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise`, `blackberry`, `palm`, `unknown`.</span></span>|
|<span data-ttu-id="f3c07-187">complianceState</span><span class="sxs-lookup"><span data-stu-id="f3c07-187">complianceState</span></span>|[<span data-ttu-id="f3c07-188">complianceState</span><span class="sxs-lookup"><span data-stu-id="f3c07-188">complianceState</span></span>](../resources/intune-devices-compliancestate.md)|<span data-ttu-id="f3c07-189">Estado de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-189">Compliance state of the device.</span></span> <span data-ttu-id="f3c07-190">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-190">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-191">Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod` y `configManager`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-191">Possible values are: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod`, `configManager`.</span></span>|
|<span data-ttu-id="f3c07-192">jailBroken</span><span class="sxs-lookup"><span data-stu-id="f3c07-192">jailBroken</span></span>|<span data-ttu-id="f3c07-193">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-193">String</span></span>|<span data-ttu-id="f3c07-194">Indica si se trata de un dispositivo liberado o con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="f3c07-194">whether the device is jail broken or rooted.</span></span> <span data-ttu-id="f3c07-195">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-195">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-196">managementAgent</span><span class="sxs-lookup"><span data-stu-id="f3c07-196">managementAgent</span></span>|[<span data-ttu-id="f3c07-197">managementAgentType</span><span class="sxs-lookup"><span data-stu-id="f3c07-197">managementAgentType</span></span>](../resources/intune-devices-managementagenttype.md)|<span data-ttu-id="f3c07-198">Canal de administración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-198">Management channel of the device.</span></span> <span data-ttu-id="f3c07-199">Intune, EAS, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-199">Intune, EAS, etc. Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-200">Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController` y `microsoft365ManagedMdm`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-200">Possible values are: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`, `microsoft365ManagedMdm`.</span></span>|
|<span data-ttu-id="f3c07-201">osVersion</span><span class="sxs-lookup"><span data-stu-id="f3c07-201">osVersion</span></span>|<span data-ttu-id="f3c07-202">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-202">String</span></span>|<span data-ttu-id="f3c07-203">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-203">Operating system version of the device.</span></span> <span data-ttu-id="f3c07-204">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-204">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-205">easActivated</span><span class="sxs-lookup"><span data-stu-id="f3c07-205">easActivated</span></span>|<span data-ttu-id="f3c07-206">Boolean</span><span class="sxs-lookup"><span data-stu-id="f3c07-206">Boolean</span></span>|<span data-ttu-id="f3c07-207">Indica si el dispositivo tiene Exchange ActiveSync activado.</span><span class="sxs-lookup"><span data-stu-id="f3c07-207">Whether the device is Exchange ActiveSync activated.</span></span> <span data-ttu-id="f3c07-208">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-208">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-209">easDeviceId</span><span class="sxs-lookup"><span data-stu-id="f3c07-209">easDeviceId</span></span>|<span data-ttu-id="f3c07-210">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-210">String</span></span>|<span data-ttu-id="f3c07-211">Identificador de Exchange ActiveSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-211">Exchange ActiveSync Id of the device.</span></span> <span data-ttu-id="f3c07-212">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-212">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-213">easActivationDateTime</span><span class="sxs-lookup"><span data-stu-id="f3c07-213">easActivationDateTime</span></span>|<span data-ttu-id="f3c07-214">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f3c07-214">DateTimeOffset</span></span>|<span data-ttu-id="f3c07-215">Hora de activación de Exchange ActivationSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-215">Exchange ActivationSync activation time of the device.</span></span> <span data-ttu-id="f3c07-216">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-216">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-217">aadRegistered</span><span class="sxs-lookup"><span data-stu-id="f3c07-217">aadRegistered</span></span>|<span data-ttu-id="f3c07-218">Boolean</span><span class="sxs-lookup"><span data-stu-id="f3c07-218">Boolean</span></span>|<span data-ttu-id="f3c07-219">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3c07-219">Whether the device is Azure Active Directory registered.</span></span> <span data-ttu-id="f3c07-220">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-220">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-221">azureADRegistered</span><span class="sxs-lookup"><span data-stu-id="f3c07-221">azureADRegistered</span></span>|<span data-ttu-id="f3c07-222">Boolean</span><span class="sxs-lookup"><span data-stu-id="f3c07-222">Boolean</span></span>|<span data-ttu-id="f3c07-223">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3c07-223">Whether the device is Azure Active Directory registered.</span></span> <span data-ttu-id="f3c07-224">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-224">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-225">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="f3c07-225">deviceEnrollmentType</span></span>|[<span data-ttu-id="f3c07-226">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="f3c07-226">deviceEnrollmentType</span></span>](../resources/intune-shared-deviceenrollmenttype.md)|<span data-ttu-id="f3c07-227">Tipo de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-227">Enrollment type of the device.</span></span> <span data-ttu-id="f3c07-228">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-228">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-229">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-229">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="f3c07-230">lostModeState</span><span class="sxs-lookup"><span data-stu-id="f3c07-230">lostModeState</span></span>|[<span data-ttu-id="f3c07-231">lostModeState</span><span class="sxs-lookup"><span data-stu-id="f3c07-231">lostModeState</span></span>](../resources/intune-devices-lostmodestate.md)|<span data-ttu-id="f3c07-232">Indica si el modo pierden está habilitado o deshabilitado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-232">Indicates if Lost mode is enabled or disabled Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-233">Los valores posibles son: `disabled` y `enabled`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-233">Possible values are: `disabled`, `enabled`.</span></span>|
|<span data-ttu-id="f3c07-234">activationLockBypassCode</span><span class="sxs-lookup"><span data-stu-id="f3c07-234">activationLockBypassCode</span></span>|<span data-ttu-id="f3c07-235">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-235">String</span></span>|<span data-ttu-id="f3c07-236">Código que permite que se omita el bloqueo de activación en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-236">Code that allows the Activation Lock on a device to be bypassed.</span></span> <span data-ttu-id="f3c07-237">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-237">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-238">emailAddress</span><span class="sxs-lookup"><span data-stu-id="f3c07-238">emailAddress</span></span>|<span data-ttu-id="f3c07-239">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-239">String</span></span>|<span data-ttu-id="f3c07-240">Email(s) para el usuario asociado con el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-240">Email(s) for the user associated with the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-241">azureActiveDirectoryDeviceId</span><span class="sxs-lookup"><span data-stu-id="f3c07-241">azureActiveDirectoryDeviceId</span></span>|<span data-ttu-id="f3c07-242">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-242">String</span></span>|<span data-ttu-id="f3c07-243">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3c07-243">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="f3c07-244">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f3c07-244">Read only.</span></span> <span data-ttu-id="f3c07-245">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-245">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-246">azureADDeviceId</span><span class="sxs-lookup"><span data-stu-id="f3c07-246">azureADDeviceId</span></span>|<span data-ttu-id="f3c07-247">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-247">String</span></span>|<span data-ttu-id="f3c07-248">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f3c07-248">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="f3c07-249">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f3c07-249">Read only.</span></span> <span data-ttu-id="f3c07-250">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-250">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-251">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="f3c07-251">deviceRegistrationState</span></span>|[<span data-ttu-id="f3c07-252">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="f3c07-252">deviceRegistrationState</span></span>](../resources/intune-devices-deviceregistrationstate.md)|<span data-ttu-id="f3c07-253">Estado de registro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-253">Device registration state.</span></span> <span data-ttu-id="f3c07-254">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-254">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-255">Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-255">Possible values are: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment`, `unknown`.</span></span>|
|<span data-ttu-id="f3c07-256">deviceCategoryDisplayName</span><span class="sxs-lookup"><span data-stu-id="f3c07-256">deviceCategoryDisplayName</span></span>|<span data-ttu-id="f3c07-257">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-257">String</span></span>|<span data-ttu-id="f3c07-258">Nombre para mostrar categoría dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-258">Device category display name Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-259">isSupervised</span><span class="sxs-lookup"><span data-stu-id="f3c07-259">isSupervised</span></span>|<span data-ttu-id="f3c07-260">Boolean</span><span class="sxs-lookup"><span data-stu-id="f3c07-260">Boolean</span></span>|<span data-ttu-id="f3c07-261">Estado del dispositivo supervisado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-261">Device supervised status Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-262">exchangeLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="f3c07-262">exchangeLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="f3c07-263">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f3c07-263">DateTimeOffset</span></span>|<span data-ttu-id="f3c07-264">Última vez que el dispositivo estableció contacto con Exchange.</span><span class="sxs-lookup"><span data-stu-id="f3c07-264">Last time the device contacted Exchange.</span></span> <span data-ttu-id="f3c07-265">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-265">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-266">exchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="f3c07-266">exchangeAccessState</span></span>|[<span data-ttu-id="f3c07-267">deviceManagementExchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="f3c07-267">deviceManagementExchangeAccessState</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstate.md)|<span data-ttu-id="f3c07-268">Estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="f3c07-268">The Access State of the device in Exchange.</span></span> <span data-ttu-id="f3c07-269">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-269">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-270">Los valores posibles son: `none`, `unknown`, `allowed`, `blocked` y `quarantined`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-270">Possible values are: `none`, `unknown`, `allowed`, `blocked`, `quarantined`.</span></span>|
|<span data-ttu-id="f3c07-271">exchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="f3c07-271">exchangeAccessStateReason</span></span>|[<span data-ttu-id="f3c07-272">deviceManagementExchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="f3c07-272">deviceManagementExchangeAccessStateReason</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstatereason.md)|<span data-ttu-id="f3c07-273">Motivo del estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="f3c07-273">The reason for the device's access state in Exchange.</span></span> <span data-ttu-id="f3c07-274">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-274">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-275">Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword` y `deviceNotKnownWithManagedApp`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-275">Possible values are: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword`, `deviceNotKnownWithManagedApp`.</span></span>|
|<span data-ttu-id="f3c07-276">remoteAssistanceSessionUrl</span><span class="sxs-lookup"><span data-stu-id="f3c07-276">remoteAssistanceSessionUrl</span></span>|<span data-ttu-id="f3c07-277">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-277">String</span></span>|<span data-ttu-id="f3c07-278">Dirección URL que permite que se establezca una sesión remota con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-278">Url that allows a Remote Assistance session to be established with the device.</span></span> <span data-ttu-id="f3c07-279">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-279">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-280">remoteAssistanceSessionErrorDetails</span><span class="sxs-lookup"><span data-stu-id="f3c07-280">remoteAssistanceSessionErrorDetails</span></span>|<span data-ttu-id="f3c07-281">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-281">String</span></span>|<span data-ttu-id="f3c07-282">Cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="f3c07-282">An error string that identifies issues when creating Remote Assistance session objects.</span></span> <span data-ttu-id="f3c07-283">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-283">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-284">isEncrypted</span><span class="sxs-lookup"><span data-stu-id="f3c07-284">isEncrypted</span></span>|<span data-ttu-id="f3c07-285">Boolean</span><span class="sxs-lookup"><span data-stu-id="f3c07-285">Boolean</span></span>|<span data-ttu-id="f3c07-286">Estado del dispositivo cifrado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-286">Device encryption status Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-287">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f3c07-287">userPrincipalName</span></span>|<span data-ttu-id="f3c07-288">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-288">String</span></span>|<span data-ttu-id="f3c07-289">Dispositivo nombre principal de usuario Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-289">Device user principal name Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-290">model</span><span class="sxs-lookup"><span data-stu-id="f3c07-290">model</span></span>|<span data-ttu-id="f3c07-291">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-291">String</span></span>|<span data-ttu-id="f3c07-292">Modelo del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-292">Model of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-293">manufacturer</span><span class="sxs-lookup"><span data-stu-id="f3c07-293">manufacturer</span></span>|<span data-ttu-id="f3c07-294">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-294">String</span></span>|<span data-ttu-id="f3c07-295">Fabricante del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-295">Manufacturer of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-296">imei</span><span class="sxs-lookup"><span data-stu-id="f3c07-296">imei</span></span>|<span data-ttu-id="f3c07-297">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-297">String</span></span>|<span data-ttu-id="f3c07-298">IMEI se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-298">IMEI Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-299">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="f3c07-299">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="f3c07-300">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f3c07-300">DateTimeOffset</span></span>|<span data-ttu-id="f3c07-301">La fecha y hora en período de gracia de cumplimiento de normas de dispositivo expira Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-301">The DateTime when device compliance grace period expires Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-302">serialNumber</span><span class="sxs-lookup"><span data-stu-id="f3c07-302">serialNumber</span></span>|<span data-ttu-id="f3c07-303">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-303">String</span></span>|<span data-ttu-id="f3c07-304">SerialNumber heredado de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-304">SerialNumber Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-305">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="f3c07-305">phoneNumber</span></span>|<span data-ttu-id="f3c07-306">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-306">String</span></span>|<span data-ttu-id="f3c07-307">Número de teléfono del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-307">Phone number of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-308">androidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="f3c07-308">androidSecurityPatchLevel</span></span>|<span data-ttu-id="f3c07-309">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-309">String</span></span>|<span data-ttu-id="f3c07-310">Nivel de revisión de seguridad para Android Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-310">Android security patch level Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-311">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="f3c07-311">userDisplayName</span></span>|<span data-ttu-id="f3c07-312">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-312">String</span></span>|<span data-ttu-id="f3c07-313">Nombre de usuario para mostrar Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-313">User display name Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-314">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="f3c07-314">configurationManagerClientEnabledFeatures</span></span>|[<span data-ttu-id="f3c07-315">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="f3c07-315">configurationManagerClientEnabledFeatures</span></span>](../resources/intune-devices-configurationmanagerclientenabledfeatures.md)|<span data-ttu-id="f3c07-316">ConfigrMgr cliente habilitado para las características Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-316">ConfigrMgr client enabled features Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-317">wiFiMacAddress</span><span class="sxs-lookup"><span data-stu-id="f3c07-317">wiFiMacAddress</span></span>|<span data-ttu-id="f3c07-318">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-318">String</span></span>|<span data-ttu-id="f3c07-319">Wi-Fi MAC se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-319">Wi-Fi MAC Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-320">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="f3c07-320">deviceHealthAttestationState</span></span>|[<span data-ttu-id="f3c07-321">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="f3c07-321">deviceHealthAttestationState</span></span>](../resources/intune-devices-devicehealthattestationstate.md)|<span data-ttu-id="f3c07-322">Estado de la atestación de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-322">The device health attestation state.</span></span> <span data-ttu-id="f3c07-323">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-323">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-324">subscriberCarrier</span><span class="sxs-lookup"><span data-stu-id="f3c07-324">subscriberCarrier</span></span>|<span data-ttu-id="f3c07-325">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-325">String</span></span>|<span data-ttu-id="f3c07-326">Operador de suscriptor se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-326">Subscriber Carrier Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-327">meid</span><span class="sxs-lookup"><span data-stu-id="f3c07-327">meid</span></span>|<span data-ttu-id="f3c07-328">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-328">String</span></span>|<span data-ttu-id="f3c07-329">MEID se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-329">MEID Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-330">totalStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="f3c07-330">totalStorageSpaceInBytes</span></span>|<span data-ttu-id="f3c07-331">Int64</span><span class="sxs-lookup"><span data-stu-id="f3c07-331">Int64</span></span>|<span data-ttu-id="f3c07-332">Almacenamiento total en Bytes se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-332">Total Storage in Bytes Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-333">freeStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="f3c07-333">freeStorageSpaceInBytes</span></span>|<span data-ttu-id="f3c07-334">Int64</span><span class="sxs-lookup"><span data-stu-id="f3c07-334">Int64</span></span>|<span data-ttu-id="f3c07-335">Espacio de almacenamiento en Bytes se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-335">Free Storage in Bytes Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-336">managedDeviceName</span><span class="sxs-lookup"><span data-stu-id="f3c07-336">managedDeviceName</span></span>|<span data-ttu-id="f3c07-337">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-337">String</span></span>|<span data-ttu-id="f3c07-338">Nombre generado automáticamente para identificar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-338">Automatically generated name to identify a device.</span></span> <span data-ttu-id="f3c07-339">Se puede sobrescribir con un nombre descriptivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="f3c07-339">Can be overwritten to a user friendly name.</span></span> <span data-ttu-id="f3c07-340">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-340">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-341">partnerReportedThreatState</span><span class="sxs-lookup"><span data-stu-id="f3c07-341">partnerReportedThreatState</span></span>|[<span data-ttu-id="f3c07-342">managedDevicePartnerReportedHealthState</span><span class="sxs-lookup"><span data-stu-id="f3c07-342">managedDevicePartnerReportedHealthState</span></span>](../resources/intune-devices-manageddevicepartnerreportedhealthstate.md)|<span data-ttu-id="f3c07-343">Indica el estado de amenazas de un dispositivo cuando la cuenta y el dispositivo usan un partner de Mobile Threat Defense.</span><span class="sxs-lookup"><span data-stu-id="f3c07-343">Indicates the threat state of a device when a Mobile Threat Defense partner is in use by the account and device.</span></span> <span data-ttu-id="f3c07-344">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f3c07-344">Read Only.</span></span> <span data-ttu-id="f3c07-345">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="f3c07-345">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="f3c07-346">Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised` y `misconfigured`.</span><span class="sxs-lookup"><span data-stu-id="f3c07-346">Possible values are: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised`, `misconfigured`.</span></span>|
|<span data-ttu-id="f3c07-347">usersLoggedOn</span><span class="sxs-lookup"><span data-stu-id="f3c07-347">usersLoggedOn</span></span>|<span data-ttu-id="f3c07-348">colección de [loggedOnUser](../resources/intune-devices-loggedonuser.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-348">[loggedOnUser](../resources/intune-devices-loggedonuser.md) collection</span></span>|<span data-ttu-id="f3c07-349">Indica la última sesión a los usuarios de un dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-349">Indicates the last logged on users of a device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-350">preferMdmOverGroupPolicyAppliedDateTime</span><span class="sxs-lookup"><span data-stu-id="f3c07-350">preferMdmOverGroupPolicyAppliedDateTime</span></span>|<span data-ttu-id="f3c07-351">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f3c07-351">DateTimeOffset</span></span>|<span data-ttu-id="f3c07-352">Informes la fecha y hora de que la configuración de preferMdmOverGroupPolicy se estableció.</span><span class="sxs-lookup"><span data-stu-id="f3c07-352">Reports the DateTime the preferMdmOverGroupPolicy setting was set.</span></span>  <span data-ttu-id="f3c07-353">Cuando se establece, la configuración MDM Intune invalidará la configuración de directiva de grupo si hay un conflicto.</span><span class="sxs-lookup"><span data-stu-id="f3c07-353">When set, the Intune MDM settings will override Group Policy settings if there is a conflict.</span></span> <span data-ttu-id="f3c07-354">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f3c07-354">Read Only.</span></span> <span data-ttu-id="f3c07-355">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-355">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-356">autopilotEnrolled</span><span class="sxs-lookup"><span data-stu-id="f3c07-356">autopilotEnrolled</span></span>|<span data-ttu-id="f3c07-357">Boolean</span><span class="sxs-lookup"><span data-stu-id="f3c07-357">Boolean</span></span>|<span data-ttu-id="f3c07-358">Informa de si el dispositivo administrado está inscrito a través de piloto automático.</span><span class="sxs-lookup"><span data-stu-id="f3c07-358">Reports if the managed device is enrolled via auto-pilot.</span></span> <span data-ttu-id="f3c07-359">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-359">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-360">requireUserEnrollmentApproval</span><span class="sxs-lookup"><span data-stu-id="f3c07-360">requireUserEnrollmentApproval</span></span>|<span data-ttu-id="f3c07-361">Boolean</span><span class="sxs-lookup"><span data-stu-id="f3c07-361">Boolean</span></span>|<span data-ttu-id="f3c07-362">Informa de si el dispositivo iOS administrada es inscripción de aprobación del usuario.</span><span class="sxs-lookup"><span data-stu-id="f3c07-362">Reports if the managed iOS device is user approval enrollment.</span></span> <span data-ttu-id="f3c07-363">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-363">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-364">managementCertificateExpirationDate</span><span class="sxs-lookup"><span data-stu-id="f3c07-364">managementCertificateExpirationDate</span></span>|<span data-ttu-id="f3c07-365">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f3c07-365">DateTimeOffset</span></span>|<span data-ttu-id="f3c07-366">Informes de dispositivo administración certificado fecha de caducidad Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-366">Reports device management certificate expiration date Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-367">iccid</span><span class="sxs-lookup"><span data-stu-id="f3c07-367">iccid</span></span>|<span data-ttu-id="f3c07-368">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-368">String</span></span>|<span data-ttu-id="f3c07-369">Identificador de la tarjeta de circuitos integrados, es número de identificación único de la tarjeta SIM A.</span><span class="sxs-lookup"><span data-stu-id="f3c07-369">Integrated Circuit Card Identifier, it is A SIM card's unique identification number.</span></span> <span data-ttu-id="f3c07-370">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-370">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-371">UDID</span><span class="sxs-lookup"><span data-stu-id="f3c07-371">udid</span></span>|<span data-ttu-id="f3c07-372">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-372">String</span></span>|<span data-ttu-id="f3c07-373">Identificador único de dispositivo para dispositivos iOS y Mac OS.</span><span class="sxs-lookup"><span data-stu-id="f3c07-373">Unique Device Identifier for iOS and macOS devices.</span></span> <span data-ttu-id="f3c07-374">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-374">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-375">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="f3c07-375">roleScopeTagIds</span></span>|<span data-ttu-id="f3c07-376">Colección String</span><span class="sxs-lookup"><span data-stu-id="f3c07-376">String collection</span></span>|<span data-ttu-id="f3c07-377">Lista de identificadores de etiqueta de ámbito para esta instancia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f3c07-377">List of Scope Tag IDs for this Device instance.</span></span> <span data-ttu-id="f3c07-378">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-378">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-379">windowsActiveMalwareCount</span><span class="sxs-lookup"><span data-stu-id="f3c07-379">windowsActiveMalwareCount</span></span>|<span data-ttu-id="f3c07-380">Int32</span><span class="sxs-lookup"><span data-stu-id="f3c07-380">Int32</span></span>|<span data-ttu-id="f3c07-381">Recuento de malware para este dispositivo windows Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-381">Count of active malware for this windows device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-382">windowsRemediatedMalwareCount</span><span class="sxs-lookup"><span data-stu-id="f3c07-382">windowsRemediatedMalwareCount</span></span>|<span data-ttu-id="f3c07-383">Int32</span><span class="sxs-lookup"><span data-stu-id="f3c07-383">Int32</span></span>|<span data-ttu-id="f3c07-384">Recuento de malware corregidos con pruebas para este dispositivo windows Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-384">Count of remediated malware for this windows device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-385">notas</span><span class="sxs-lookup"><span data-stu-id="f3c07-385">notes</span></span>|<span data-ttu-id="f3c07-386">String</span><span class="sxs-lookup"><span data-stu-id="f3c07-386">String</span></span>|<span data-ttu-id="f3c07-387">Notas en el dispositivo creado mediante la administración de TI se hereda desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-387">Notes on the device created by IT Admin Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="f3c07-388">configurationManagerClientHealthState</span><span class="sxs-lookup"><span data-stu-id="f3c07-388">configurationManagerClientHealthState</span></span>|[<span data-ttu-id="f3c07-389">configurationManagerClientHealthState</span><span class="sxs-lookup"><span data-stu-id="f3c07-389">configurationManagerClientHealthState</span></span>](../resources/intune-devices-configurationmanagerclienthealthstate.md)|<span data-ttu-id="f3c07-390">Configuración Administrador cliente estado de mantenimiento, válido sólo para los dispositivos administrados por MDM/ConfigMgr heredado de agente de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="f3c07-390">Configuration manager client health state, valid only for devices managed by MDM/ConfigMgr Agent Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|



## <a name="response"></a><span data-ttu-id="f3c07-391">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3c07-391">Response</span></span>
<span data-ttu-id="f3c07-392">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f3c07-392">If successful, this method returns a `200 OK` response code and an updated [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f3c07-393">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f3c07-393">Example</span></span>
### <a name="request"></a><span data-ttu-id="f3c07-394">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f3c07-394">Request</span></span>
<span data-ttu-id="f3c07-395">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f3c07-395">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/users/{usersId}/managedDevices/{managedDeviceId}
Content-type: application/json
Content-length: 7114

{
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

### <a name="response"></a><span data-ttu-id="f3c07-396">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f3c07-396">Response</span></span>
<span data-ttu-id="f3c07-p142">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f3c07-p142">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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





