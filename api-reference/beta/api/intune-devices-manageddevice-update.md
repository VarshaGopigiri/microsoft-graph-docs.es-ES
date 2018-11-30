---
title: Actualizar managedDevice
description: Actualiza las propiedades de un objeto managedDevice.
ms.openlocfilehash: fa831967b7c091e8f698de4acef70cfec7119435
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085818"
---
# <a name="update-manageddevice"></a><span data-ttu-id="763c6-103">Actualizar managedDevice</span><span class="sxs-lookup"><span data-stu-id="763c6-103">Update managedDevice</span></span>

> <span data-ttu-id="763c6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="763c6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="763c6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="763c6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="763c6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="763c6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="763c6-107">Actualiza las propiedades de un objeto [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="763c6-107">Update the properties of a [managedDevice](../resources/intune-devices-manageddevice.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="763c6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="763c6-108">Prerequisites</span></span>
<span data-ttu-id="763c6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="763c6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="763c6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="763c6-111">Permission type</span></span>|<span data-ttu-id="763c6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="763c6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="763c6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="763c6-113">Delegated (work or school account)</span></span>|<span data-ttu-id="763c6-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="763c6-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="763c6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="763c6-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="763c6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="763c6-116">Not supported.</span></span>|
|<span data-ttu-id="763c6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="763c6-117">Application</span></span>|<span data-ttu-id="763c6-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="763c6-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="763c6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="763c6-119">HTTP Request</span></span>
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

## <a name="request-headers"></a><span data-ttu-id="763c6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="763c6-120">Request headers</span></span>
|<span data-ttu-id="763c6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="763c6-121">Header</span></span>|<span data-ttu-id="763c6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="763c6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="763c6-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="763c6-123">Authorization</span></span>|<span data-ttu-id="763c6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="763c6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="763c6-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="763c6-125">Accept</span></span>|<span data-ttu-id="763c6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="763c6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="763c6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="763c6-127">Request body</span></span>
<span data-ttu-id="763c6-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="763c6-128">In the request body, supply a JSON representation for the [managedDevice](../resources/intune-devices-manageddevice.md) object.</span></span>

<span data-ttu-id="763c6-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="763c6-129">The following table shows the properties that are required when you create the [managedDevice](../resources/intune-devices-manageddevice.md).</span></span>

|<span data-ttu-id="763c6-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="763c6-130">Property</span></span>|<span data-ttu-id="763c6-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="763c6-131">Type</span></span>|<span data-ttu-id="763c6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="763c6-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="763c6-133">id</span><span class="sxs-lookup"><span data-stu-id="763c6-133">id</span></span>|<span data-ttu-id="763c6-134">String</span><span class="sxs-lookup"><span data-stu-id="763c6-134">String</span></span>|<span data-ttu-id="763c6-135">Identificador único del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-135">Unique Identifier for the device</span></span>|
|<span data-ttu-id="763c6-136">userId</span><span class="sxs-lookup"><span data-stu-id="763c6-136">userId</span></span>|<span data-ttu-id="763c6-137">String</span><span class="sxs-lookup"><span data-stu-id="763c6-137">String</span></span>|<span data-ttu-id="763c6-138">Identificador único del usuario asociado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-138">Unique Identifier for the user associated with the device</span></span>|
|<span data-ttu-id="763c6-139">deviceName</span><span class="sxs-lookup"><span data-stu-id="763c6-139">deviceName</span></span>|<span data-ttu-id="763c6-140">String</span><span class="sxs-lookup"><span data-stu-id="763c6-140">String</span></span>|<span data-ttu-id="763c6-141">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-141">Name of the device</span></span>|
|<span data-ttu-id="763c6-142">hardwareInformation</span><span class="sxs-lookup"><span data-stu-id="763c6-142">hardwareInformation</span></span>|[<span data-ttu-id="763c6-143">hardwareInformation</span><span class="sxs-lookup"><span data-stu-id="763c6-143">hardwareInformation</span></span>](../resources/intune-devices-hardwareinformation.md)|<span data-ttu-id="763c6-144">Los detalles de hardward para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-144">The hardward details for the device.</span></span>  <span data-ttu-id="763c6-145">Incluye información como el espacio de almacenamiento, el fabricante, el número de serie, etcetera.</span><span class="sxs-lookup"><span data-stu-id="763c6-145">Includes information such as storage space, manufacturer, serial number, etc.</span></span>|
|<span data-ttu-id="763c6-146">ownerType</span><span class="sxs-lookup"><span data-stu-id="763c6-146">ownerType</span></span>|[<span data-ttu-id="763c6-147">ownerType</span><span class="sxs-lookup"><span data-stu-id="763c6-147">ownerType</span></span>](../resources/intune-devices-ownertype.md)|<span data-ttu-id="763c6-148">Propietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-148">Ownership of the device.</span></span> <span data-ttu-id="763c6-149">Puede ser 'compañía' o 'personal'.</span><span class="sxs-lookup"><span data-stu-id="763c6-149">Can be 'company' or 'personal'.</span></span> <span data-ttu-id="763c6-150">Los valores posibles son: `unknown`, `company` y `personal`.</span><span class="sxs-lookup"><span data-stu-id="763c6-150">Possible values are: `unknown`, `company`, `personal`.</span></span>|
|<span data-ttu-id="763c6-151">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="763c6-151">managedDeviceOwnerType</span></span>|[<span data-ttu-id="763c6-152">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="763c6-152">managedDeviceOwnerType</span></span>](../resources/intune-devices-manageddeviceownertype.md)|<span data-ttu-id="763c6-153">Propietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-153">Ownership of the device.</span></span> <span data-ttu-id="763c6-154">Puede ser 'compañía' o 'personal'.</span><span class="sxs-lookup"><span data-stu-id="763c6-154">Can be 'company' or 'personal'.</span></span> <span data-ttu-id="763c6-155">Los valores posibles son: `unknown`, `company` y `personal`.</span><span class="sxs-lookup"><span data-stu-id="763c6-155">Possible values are: `unknown`, `company`, `personal`.</span></span>|
|<span data-ttu-id="763c6-156">deviceActionResults</span><span class="sxs-lookup"><span data-stu-id="763c6-156">deviceActionResults</span></span>|<span data-ttu-id="763c6-157">Colección [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="763c6-157">[deviceActionResult](../resources/intune-devices-deviceactionresult.md) collection</span></span>|<span data-ttu-id="763c6-158">Lista de objetos deviceActionResult ComplexType.</span><span class="sxs-lookup"><span data-stu-id="763c6-158">List of ComplexType deviceActionResult objects.</span></span>|
|<span data-ttu-id="763c6-159">managementState</span><span class="sxs-lookup"><span data-stu-id="763c6-159">managementState</span></span>|[<span data-ttu-id="763c6-160">managementState</span><span class="sxs-lookup"><span data-stu-id="763c6-160">managementState</span></span>](../resources/intune-devices-managementstate.md)|<span data-ttu-id="763c6-161">Estado de administración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-161">Management state of the device.</span></span> <span data-ttu-id="763c6-162">Los valores posibles son: `managed`, `retirePending`, `retireFailed`, `wipePending`, `wipeFailed`, `unhealthy`, `deletePending`, `retireIssued`, `wipeIssued`, `wipeCanceled`, `retireCanceled` y `discovered`.</span><span class="sxs-lookup"><span data-stu-id="763c6-162">Possible values are: `managed`, `retirePending`, `retireFailed`, `wipePending`, `wipeFailed`, `unhealthy`, `deletePending`, `retireIssued`, `wipeIssued`, `wipeCanceled`, `retireCanceled`, `discovered`.</span></span>|
|<span data-ttu-id="763c6-163">enrolledDateTime</span><span class="sxs-lookup"><span data-stu-id="763c6-163">enrolledDateTime</span></span>|<span data-ttu-id="763c6-164">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="763c6-164">DateTimeOffset</span></span>|<span data-ttu-id="763c6-165">Hora de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-165">Enrollment time of the device.</span></span>|
|<span data-ttu-id="763c6-166">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="763c6-166">lastSyncDateTime</span></span>|<span data-ttu-id="763c6-167">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="763c6-167">DateTimeOffset</span></span>|<span data-ttu-id="763c6-168">Fecha y hora en que el dispositivo completó por última vez una sincronización correcta con Intune.</span><span class="sxs-lookup"><span data-stu-id="763c6-168">The date and time that the device last completed a successful sync with Intune.</span></span>|
|<span data-ttu-id="763c6-169">chassisType</span><span class="sxs-lookup"><span data-stu-id="763c6-169">chassisType</span></span>|[<span data-ttu-id="763c6-170">chassisType</span><span class="sxs-lookup"><span data-stu-id="763c6-170">chassisType</span></span>](../resources/intune-devices-chassistype.md)|<span data-ttu-id="763c6-171">Tipo de chasis del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-171">Chassis type of the device.</span></span> <span data-ttu-id="763c6-172">Los valores posibles son: `unknown`, `desktop`, `laptop`, `worksWorkstation`, `enterpriseServer`, `phone`, `tablet`, `mobileOther` y `mobileUnknown`.</span><span class="sxs-lookup"><span data-stu-id="763c6-172">Possible values are: `unknown`, `desktop`, `laptop`, `worksWorkstation`, `enterpriseServer`, `phone`, `tablet`, `mobileOther`, `mobileUnknown`.</span></span>|
|<span data-ttu-id="763c6-173">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="763c6-173">operatingSystem</span></span>|<span data-ttu-id="763c6-174">String</span><span class="sxs-lookup"><span data-stu-id="763c6-174">String</span></span>|<span data-ttu-id="763c6-175">Sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-175">Operating system of the device.</span></span> <span data-ttu-id="763c6-176">Windows, iOS, etc.</span><span class="sxs-lookup"><span data-stu-id="763c6-176">Windows, iOS, etc.</span></span>|
|<span data-ttu-id="763c6-177">deviceType</span><span class="sxs-lookup"><span data-stu-id="763c6-177">deviceType</span></span>|[<span data-ttu-id="763c6-178">deviceType</span><span class="sxs-lookup"><span data-stu-id="763c6-178">deviceType</span></span>](../resources/intune-shared-devicetype.md)|<span data-ttu-id="763c6-179">Plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-179">Platform of the device.</span></span> <span data-ttu-id="763c6-180">Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="763c6-180">Possible values are: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise`, `blackberry`, `palm`, `unknown`.</span></span>|
|<span data-ttu-id="763c6-181">complianceState</span><span class="sxs-lookup"><span data-stu-id="763c6-181">complianceState</span></span>|[<span data-ttu-id="763c6-182">complianceState</span><span class="sxs-lookup"><span data-stu-id="763c6-182">complianceState</span></span>](../resources/intune-devices-compliancestate.md)|<span data-ttu-id="763c6-183">Estado de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-183">Compliance state of the device.</span></span> <span data-ttu-id="763c6-184">Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod` y `configManager`.</span><span class="sxs-lookup"><span data-stu-id="763c6-184">Possible values are: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod`, `configManager`.</span></span>|
|<span data-ttu-id="763c6-185">jailBroken</span><span class="sxs-lookup"><span data-stu-id="763c6-185">jailBroken</span></span>|<span data-ttu-id="763c6-186">String</span><span class="sxs-lookup"><span data-stu-id="763c6-186">String</span></span>|<span data-ttu-id="763c6-187">Indica si se trata de un dispositivo liberado o con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="763c6-187">whether the device is jail broken or rooted.</span></span>|
|<span data-ttu-id="763c6-188">managementAgent</span><span class="sxs-lookup"><span data-stu-id="763c6-188">managementAgent</span></span>|[<span data-ttu-id="763c6-189">managementAgentType</span><span class="sxs-lookup"><span data-stu-id="763c6-189">managementAgentType</span></span>](../resources/intune-devices-managementagenttype.md)|<span data-ttu-id="763c6-190">Canal de administración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-190">Management channel of the device.</span></span> <span data-ttu-id="763c6-191">Intune, EAS, etcetera. Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`, `microsoft365ManagedMdm`.</span><span class="sxs-lookup"><span data-stu-id="763c6-191">Intune, EAS, etc. Possible values are: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`, `microsoft365ManagedMdm`.</span></span>|
|<span data-ttu-id="763c6-192">osVersion</span><span class="sxs-lookup"><span data-stu-id="763c6-192">osVersion</span></span>|<span data-ttu-id="763c6-193">String</span><span class="sxs-lookup"><span data-stu-id="763c6-193">String</span></span>|<span data-ttu-id="763c6-194">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-194">Operating system version of the device.</span></span>|
|<span data-ttu-id="763c6-195">easActivated</span><span class="sxs-lookup"><span data-stu-id="763c6-195">easActivated</span></span>|<span data-ttu-id="763c6-196">Booleano</span><span class="sxs-lookup"><span data-stu-id="763c6-196">Boolean</span></span>|<span data-ttu-id="763c6-197">Indica si el dispositivo tiene Exchange ActiveSync activado.</span><span class="sxs-lookup"><span data-stu-id="763c6-197">Whether the device is Exchange ActiveSync activated.</span></span>|
|<span data-ttu-id="763c6-198">easDeviceId</span><span class="sxs-lookup"><span data-stu-id="763c6-198">easDeviceId</span></span>|<span data-ttu-id="763c6-199">String</span><span class="sxs-lookup"><span data-stu-id="763c6-199">String</span></span>|<span data-ttu-id="763c6-200">Identificador de Exchange ActiveSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-200">Exchange ActiveSync Id of the device.</span></span>|
|<span data-ttu-id="763c6-201">easActivationDateTime</span><span class="sxs-lookup"><span data-stu-id="763c6-201">easActivationDateTime</span></span>|<span data-ttu-id="763c6-202">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="763c6-202">DateTimeOffset</span></span>|<span data-ttu-id="763c6-203">Hora de activación de Exchange ActivationSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-203">Exchange ActivationSync activation time of the device.</span></span>|
|<span data-ttu-id="763c6-204">aadRegistered</span><span class="sxs-lookup"><span data-stu-id="763c6-204">aadRegistered</span></span>|<span data-ttu-id="763c6-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="763c6-205">Boolean</span></span>|<span data-ttu-id="763c6-206">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="763c6-206">Whether the device is Azure Active Directory registered.</span></span>|
|<span data-ttu-id="763c6-207">azureADRegistered</span><span class="sxs-lookup"><span data-stu-id="763c6-207">azureADRegistered</span></span>|<span data-ttu-id="763c6-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="763c6-208">Boolean</span></span>|<span data-ttu-id="763c6-209">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="763c6-209">Whether the device is Azure Active Directory registered.</span></span>|
|<span data-ttu-id="763c6-210">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="763c6-210">deviceEnrollmentType</span></span>|[<span data-ttu-id="763c6-211">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="763c6-211">deviceEnrollmentType</span></span>](../resources/intune-shared-deviceenrollmenttype.md)|<span data-ttu-id="763c6-212">Tipo de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-212">Enrollment type of the device.</span></span> <span data-ttu-id="763c6-213">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="763c6-213">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="763c6-214">lostModeState</span><span class="sxs-lookup"><span data-stu-id="763c6-214">lostModeState</span></span>|[<span data-ttu-id="763c6-215">lostModeState</span><span class="sxs-lookup"><span data-stu-id="763c6-215">lostModeState</span></span>](../resources/intune-devices-lostmodestate.md)|<span data-ttu-id="763c6-216">Indica si el modo pierden está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="763c6-216">Indicates if Lost mode is enabled or disabled.</span></span> <span data-ttu-id="763c6-217">Los valores posibles son: `disabled` y `enabled`.</span><span class="sxs-lookup"><span data-stu-id="763c6-217">Possible values are: `disabled`, `enabled`.</span></span>|
|<span data-ttu-id="763c6-218">activationLockBypassCode</span><span class="sxs-lookup"><span data-stu-id="763c6-218">activationLockBypassCode</span></span>|<span data-ttu-id="763c6-219">String</span><span class="sxs-lookup"><span data-stu-id="763c6-219">String</span></span>|<span data-ttu-id="763c6-220">Código que permite que se omita el bloqueo de activación en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-220">Code that allows the Activation Lock on a device to be bypassed.</span></span>|
|<span data-ttu-id="763c6-221">emailAddress</span><span class="sxs-lookup"><span data-stu-id="763c6-221">emailAddress</span></span>|<span data-ttu-id="763c6-222">String</span><span class="sxs-lookup"><span data-stu-id="763c6-222">String</span></span>|<span data-ttu-id="763c6-223">Direcciones de correo electrónico del usuario asociado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-223">Email(s) for the user associated with the device</span></span>|
|<span data-ttu-id="763c6-224">azureActiveDirectoryDeviceId</span><span class="sxs-lookup"><span data-stu-id="763c6-224">azureActiveDirectoryDeviceId</span></span>|<span data-ttu-id="763c6-225">String</span><span class="sxs-lookup"><span data-stu-id="763c6-225">String</span></span>|<span data-ttu-id="763c6-226">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="763c6-226">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="763c6-227">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="763c6-227">Read only.</span></span>|
|<span data-ttu-id="763c6-228">azureADDeviceId</span><span class="sxs-lookup"><span data-stu-id="763c6-228">azureADDeviceId</span></span>|<span data-ttu-id="763c6-229">String</span><span class="sxs-lookup"><span data-stu-id="763c6-229">String</span></span>|<span data-ttu-id="763c6-230">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="763c6-230">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="763c6-231">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="763c6-231">Read only.</span></span>|
|<span data-ttu-id="763c6-232">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="763c6-232">deviceRegistrationState</span></span>|[<span data-ttu-id="763c6-233">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="763c6-233">deviceRegistrationState</span></span>](../resources/intune-devices-deviceregistrationstate.md)|<span data-ttu-id="763c6-234">Estado de registro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-234">Device registration state.</span></span> <span data-ttu-id="763c6-235">Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="763c6-235">Possible values are: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment`, `unknown`.</span></span>|
|<span data-ttu-id="763c6-236">deviceCategoryDisplayName</span><span class="sxs-lookup"><span data-stu-id="763c6-236">deviceCategoryDisplayName</span></span>|<span data-ttu-id="763c6-237">String</span><span class="sxs-lookup"><span data-stu-id="763c6-237">String</span></span>|<span data-ttu-id="763c6-238">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-238">Device category display name</span></span>|
|<span data-ttu-id="763c6-239">isSupervised</span><span class="sxs-lookup"><span data-stu-id="763c6-239">isSupervised</span></span>|<span data-ttu-id="763c6-240">Booleano</span><span class="sxs-lookup"><span data-stu-id="763c6-240">Boolean</span></span>|<span data-ttu-id="763c6-241">Estado supervisado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-241">Device supervised status</span></span>|
|<span data-ttu-id="763c6-242">exchangeLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="763c6-242">exchangeLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="763c6-243">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="763c6-243">DateTimeOffset</span></span>|<span data-ttu-id="763c6-244">Última vez que el dispositivo estableció contacto con Exchange.</span><span class="sxs-lookup"><span data-stu-id="763c6-244">Last time the device contacted Exchange.</span></span>|
|<span data-ttu-id="763c6-245">exchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="763c6-245">exchangeAccessState</span></span>|[<span data-ttu-id="763c6-246">deviceManagementExchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="763c6-246">deviceManagementExchangeAccessState</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstate.md)|<span data-ttu-id="763c6-247">Estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="763c6-247">The Access State of the device in Exchange.</span></span> <span data-ttu-id="763c6-248">Los valores posibles son: `none`, `unknown`, `allowed`, `blocked` y `quarantined`.</span><span class="sxs-lookup"><span data-stu-id="763c6-248">Possible values are: `none`, `unknown`, `allowed`, `blocked`, `quarantined`.</span></span>|
|<span data-ttu-id="763c6-249">exchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="763c6-249">exchangeAccessStateReason</span></span>|[<span data-ttu-id="763c6-250">deviceManagementExchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="763c6-250">deviceManagementExchangeAccessStateReason</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstatereason.md)|<span data-ttu-id="763c6-251">Motivo del estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="763c6-251">The reason for the device's access state in Exchange.</span></span> <span data-ttu-id="763c6-252">Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword` y `deviceNotKnownWithManagedApp`.</span><span class="sxs-lookup"><span data-stu-id="763c6-252">Possible values are: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword`, `deviceNotKnownWithManagedApp`.</span></span>|
|<span data-ttu-id="763c6-253">remoteAssistanceSessionUrl</span><span class="sxs-lookup"><span data-stu-id="763c6-253">remoteAssistanceSessionUrl</span></span>|<span data-ttu-id="763c6-254">String</span><span class="sxs-lookup"><span data-stu-id="763c6-254">String</span></span>|<span data-ttu-id="763c6-255">Dirección URL que permite que se establezca una sesión remota con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-255">Url that allows a Remote Assistance session to be established with the device.</span></span>|
|<span data-ttu-id="763c6-256">remoteAssistanceSessionErrorDetails</span><span class="sxs-lookup"><span data-stu-id="763c6-256">remoteAssistanceSessionErrorDetails</span></span>|<span data-ttu-id="763c6-257">String</span><span class="sxs-lookup"><span data-stu-id="763c6-257">String</span></span>|<span data-ttu-id="763c6-258">Cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="763c6-258">An error string that identifies issues when creating Remote Assistance session objects.</span></span>|
|<span data-ttu-id="763c6-259">isEncrypted</span><span class="sxs-lookup"><span data-stu-id="763c6-259">isEncrypted</span></span>|<span data-ttu-id="763c6-260">Booleano</span><span class="sxs-lookup"><span data-stu-id="763c6-260">Boolean</span></span>|<span data-ttu-id="763c6-261">Estado del cifrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-261">Device encryption status</span></span>|
|<span data-ttu-id="763c6-262">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="763c6-262">userPrincipalName</span></span>|<span data-ttu-id="763c6-263">String</span><span class="sxs-lookup"><span data-stu-id="763c6-263">String</span></span>|<span data-ttu-id="763c6-264">Nombre principal de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-264">Device user principal name</span></span>|
|<span data-ttu-id="763c6-265">model</span><span class="sxs-lookup"><span data-stu-id="763c6-265">model</span></span>|<span data-ttu-id="763c6-266">String</span><span class="sxs-lookup"><span data-stu-id="763c6-266">String</span></span>|<span data-ttu-id="763c6-267">Modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-267">Model of the device</span></span>|
|<span data-ttu-id="763c6-268">manufacturer</span><span class="sxs-lookup"><span data-stu-id="763c6-268">manufacturer</span></span>|<span data-ttu-id="763c6-269">String</span><span class="sxs-lookup"><span data-stu-id="763c6-269">String</span></span>|<span data-ttu-id="763c6-270">Fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-270">Manufacturer of the device</span></span>|
|<span data-ttu-id="763c6-271">imei</span><span class="sxs-lookup"><span data-stu-id="763c6-271">imei</span></span>|<span data-ttu-id="763c6-272">String</span><span class="sxs-lookup"><span data-stu-id="763c6-272">String</span></span>|<span data-ttu-id="763c6-273">IMEI</span><span class="sxs-lookup"><span data-stu-id="763c6-273">IMEI</span></span>|
|<span data-ttu-id="763c6-274">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="763c6-274">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="763c6-275">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="763c6-275">DateTimeOffset</span></span>|<span data-ttu-id="763c6-276">Fecha y hora en que expira el período de gracia de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-276">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="763c6-277">serialNumber</span><span class="sxs-lookup"><span data-stu-id="763c6-277">serialNumber</span></span>|<span data-ttu-id="763c6-278">String</span><span class="sxs-lookup"><span data-stu-id="763c6-278">String</span></span>|<span data-ttu-id="763c6-279">Número de serie.</span><span class="sxs-lookup"><span data-stu-id="763c6-279">SerialNumber</span></span>|
|<span data-ttu-id="763c6-280">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="763c6-280">phoneNumber</span></span>|<span data-ttu-id="763c6-281">String</span><span class="sxs-lookup"><span data-stu-id="763c6-281">String</span></span>|<span data-ttu-id="763c6-282">Número de teléfono del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-282">Phone number of the device</span></span>|
|<span data-ttu-id="763c6-283">androidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="763c6-283">androidSecurityPatchLevel</span></span>|<span data-ttu-id="763c6-284">String</span><span class="sxs-lookup"><span data-stu-id="763c6-284">String</span></span>|<span data-ttu-id="763c6-285">Nivel de revisión de seguridad de Android.</span><span class="sxs-lookup"><span data-stu-id="763c6-285">Android security patch level</span></span>|
|<span data-ttu-id="763c6-286">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="763c6-286">userDisplayName</span></span>|<span data-ttu-id="763c6-287">String</span><span class="sxs-lookup"><span data-stu-id="763c6-287">String</span></span>|<span data-ttu-id="763c6-288">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="763c6-288">User display name</span></span>|
|<span data-ttu-id="763c6-289">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="763c6-289">configurationManagerClientEnabledFeatures</span></span>|[<span data-ttu-id="763c6-290">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="763c6-290">configurationManagerClientEnabledFeatures</span></span>](../resources/intune-devices-configurationmanagerclientenabledfeatures.md)|<span data-ttu-id="763c6-291">Características activadas del cliente ConfigrMgr.</span><span class="sxs-lookup"><span data-stu-id="763c6-291">ConfigrMgr client enabled features</span></span>|
|<span data-ttu-id="763c6-292">wiFiMacAddress</span><span class="sxs-lookup"><span data-stu-id="763c6-292">wiFiMacAddress</span></span>|<span data-ttu-id="763c6-293">String</span><span class="sxs-lookup"><span data-stu-id="763c6-293">String</span></span>|<span data-ttu-id="763c6-294">MAC de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="763c6-294">Wi-Fi MAC</span></span>|
|<span data-ttu-id="763c6-295">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="763c6-295">deviceHealthAttestationState</span></span>|[<span data-ttu-id="763c6-296">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="763c6-296">deviceHealthAttestationState</span></span>](../resources/intune-devices-devicehealthattestationstate.md)|<span data-ttu-id="763c6-297">Estado de la atestación de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-297">The device health attestation state.</span></span>|
|<span data-ttu-id="763c6-298">subscriberCarrier</span><span class="sxs-lookup"><span data-stu-id="763c6-298">subscriberCarrier</span></span>|<span data-ttu-id="763c6-299">String</span><span class="sxs-lookup"><span data-stu-id="763c6-299">String</span></span>|<span data-ttu-id="763c6-300">Operador del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="763c6-300">Subscriber Carrier</span></span>|
|<span data-ttu-id="763c6-301">meid</span><span class="sxs-lookup"><span data-stu-id="763c6-301">meid</span></span>|<span data-ttu-id="763c6-302">String</span><span class="sxs-lookup"><span data-stu-id="763c6-302">String</span></span>|<span data-ttu-id="763c6-303">MEID</span><span class="sxs-lookup"><span data-stu-id="763c6-303">MEID</span></span>|
|<span data-ttu-id="763c6-304">totalStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="763c6-304">totalStorageSpaceInBytes</span></span>|<span data-ttu-id="763c6-305">Int64</span><span class="sxs-lookup"><span data-stu-id="763c6-305">Int64</span></span>|<span data-ttu-id="763c6-306">Almacenamiento total en bytes.</span><span class="sxs-lookup"><span data-stu-id="763c6-306">Total Storage in Bytes</span></span>|
|<span data-ttu-id="763c6-307">freeStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="763c6-307">freeStorageSpaceInBytes</span></span>|<span data-ttu-id="763c6-308">Int64</span><span class="sxs-lookup"><span data-stu-id="763c6-308">Int64</span></span>|<span data-ttu-id="763c6-309">Almacenamiento disponible en bytes.</span><span class="sxs-lookup"><span data-stu-id="763c6-309">Free Storage in Bytes</span></span>|
|<span data-ttu-id="763c6-310">managedDeviceName</span><span class="sxs-lookup"><span data-stu-id="763c6-310">managedDeviceName</span></span>|<span data-ttu-id="763c6-311">String</span><span class="sxs-lookup"><span data-stu-id="763c6-311">String</span></span>|<span data-ttu-id="763c6-312">Nombre generado automáticamente para identificar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-312">Automatically generated name to identify a device.</span></span> <span data-ttu-id="763c6-313">Se puede sobrescribir con un nombre descriptivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="763c6-313">Can be overwritten to a user friendly name.</span></span>|
|<span data-ttu-id="763c6-314">partnerReportedThreatState</span><span class="sxs-lookup"><span data-stu-id="763c6-314">partnerReportedThreatState</span></span>|[<span data-ttu-id="763c6-315">managedDevicePartnerReportedHealthState</span><span class="sxs-lookup"><span data-stu-id="763c6-315">managedDevicePartnerReportedHealthState</span></span>](../resources/intune-devices-manageddevicepartnerreportedhealthstate.md)|<span data-ttu-id="763c6-316">Indica el estado de amenazas de un dispositivo cuando la cuenta y el dispositivo usan un partner de Mobile Threat Defense.</span><span class="sxs-lookup"><span data-stu-id="763c6-316">Indicates the threat state of a device when a Mobile Threat Defense partner is in use by the account and device.</span></span> <span data-ttu-id="763c6-317">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="763c6-317">Read Only.</span></span> <span data-ttu-id="763c6-318">Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised` y `misconfigured`.</span><span class="sxs-lookup"><span data-stu-id="763c6-318">Possible values are: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised`, `misconfigured`.</span></span>|
|<span data-ttu-id="763c6-319">usersLoggedOn</span><span class="sxs-lookup"><span data-stu-id="763c6-319">usersLoggedOn</span></span>|<span data-ttu-id="763c6-320">colección de [loggedOnUser](../resources/intune-devices-loggedonuser.md)</span><span class="sxs-lookup"><span data-stu-id="763c6-320">[loggedOnUser](../resources/intune-devices-loggedonuser.md) collection</span></span>|<span data-ttu-id="763c6-321">Indica la última sesión de los usuarios de un dispositivo</span><span class="sxs-lookup"><span data-stu-id="763c6-321">Indicates the last logged on users of a device</span></span>|
|<span data-ttu-id="763c6-322">preferMdmOverGroupPolicyAppliedDateTime</span><span class="sxs-lookup"><span data-stu-id="763c6-322">preferMdmOverGroupPolicyAppliedDateTime</span></span>|<span data-ttu-id="763c6-323">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="763c6-323">DateTimeOffset</span></span>|<span data-ttu-id="763c6-324">Informes la fecha y hora de que la configuración de preferMdmOverGroupPolicy se estableció.</span><span class="sxs-lookup"><span data-stu-id="763c6-324">Reports the DateTime the preferMdmOverGroupPolicy setting was set.</span></span>  <span data-ttu-id="763c6-325">Cuando se establece, la configuración MDM Intune invalidará la configuración de directiva de grupo si hay un conflicto.</span><span class="sxs-lookup"><span data-stu-id="763c6-325">When set, the Intune MDM settings will override Group Policy settings if there is a conflict.</span></span> <span data-ttu-id="763c6-326">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="763c6-326">Read Only.</span></span>|
|<span data-ttu-id="763c6-327">autopilotEnrolled</span><span class="sxs-lookup"><span data-stu-id="763c6-327">autopilotEnrolled</span></span>|<span data-ttu-id="763c6-328">Booleano</span><span class="sxs-lookup"><span data-stu-id="763c6-328">Boolean</span></span>|<span data-ttu-id="763c6-329">Informa de si el dispositivo administrado está inscrito a través de piloto automático.</span><span class="sxs-lookup"><span data-stu-id="763c6-329">Reports if the managed device is enrolled via auto-pilot.</span></span>|
|<span data-ttu-id="763c6-330">requireUserEnrollmentApproval</span><span class="sxs-lookup"><span data-stu-id="763c6-330">requireUserEnrollmentApproval</span></span>|<span data-ttu-id="763c6-331">Booleano</span><span class="sxs-lookup"><span data-stu-id="763c6-331">Boolean</span></span>|<span data-ttu-id="763c6-332">Informa de si el dispositivo iOS administrada es inscripción de aprobación del usuario.</span><span class="sxs-lookup"><span data-stu-id="763c6-332">Reports if the managed iOS device is user approval enrollment.</span></span>|
|<span data-ttu-id="763c6-333">managementCertificateExpirationDate</span><span class="sxs-lookup"><span data-stu-id="763c6-333">managementCertificateExpirationDate</span></span>|<span data-ttu-id="763c6-334">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="763c6-334">DateTimeOffset</span></span>|<span data-ttu-id="763c6-335">Fecha de caducidad de certificado de administración de dispositivos de informes</span><span class="sxs-lookup"><span data-stu-id="763c6-335">Reports device management certificate expiration date</span></span>|
|<span data-ttu-id="763c6-336">iccid</span><span class="sxs-lookup"><span data-stu-id="763c6-336">iccid</span></span>|<span data-ttu-id="763c6-337">String</span><span class="sxs-lookup"><span data-stu-id="763c6-337">String</span></span>|<span data-ttu-id="763c6-338">Identificador de la tarjeta de circuitos integrados, es número de identificación único de la tarjeta SIM A.</span><span class="sxs-lookup"><span data-stu-id="763c6-338">Integrated Circuit Card Identifier, it is A SIM card's unique identification number.</span></span>|
|<span data-ttu-id="763c6-339">UDID</span><span class="sxs-lookup"><span data-stu-id="763c6-339">udid</span></span>|<span data-ttu-id="763c6-340">String</span><span class="sxs-lookup"><span data-stu-id="763c6-340">String</span></span>|<span data-ttu-id="763c6-341">Identificador único de dispositivo para dispositivos iOS y Mac OS.</span><span class="sxs-lookup"><span data-stu-id="763c6-341">Unique Device Identifier for iOS and macOS devices.</span></span>|
|<span data-ttu-id="763c6-342">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="763c6-342">roleScopeTagIds</span></span>|<span data-ttu-id="763c6-343">Colección String</span><span class="sxs-lookup"><span data-stu-id="763c6-343">String collection</span></span>|<span data-ttu-id="763c6-344">Lista de identificadores de etiqueta de ámbito para esta instancia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="763c6-344">List of Scope Tag IDs for this Device instance.</span></span>|
|<span data-ttu-id="763c6-345">windowsActiveMalwareCount</span><span class="sxs-lookup"><span data-stu-id="763c6-345">windowsActiveMalwareCount</span></span>|<span data-ttu-id="763c6-346">Int32</span><span class="sxs-lookup"><span data-stu-id="763c6-346">Int32</span></span>|<span data-ttu-id="763c6-347">Recuento de malware para este dispositivo de windows</span><span class="sxs-lookup"><span data-stu-id="763c6-347">Count of active malware for this windows device</span></span>|
|<span data-ttu-id="763c6-348">windowsRemediatedMalwareCount</span><span class="sxs-lookup"><span data-stu-id="763c6-348">windowsRemediatedMalwareCount</span></span>|<span data-ttu-id="763c6-349">Int32</span><span class="sxs-lookup"><span data-stu-id="763c6-349">Int32</span></span>|<span data-ttu-id="763c6-350">Recuento de malware corregidos con pruebas para este dispositivo de windows</span><span class="sxs-lookup"><span data-stu-id="763c6-350">Count of remediated malware for this windows device</span></span>|
|<span data-ttu-id="763c6-351">notas</span><span class="sxs-lookup"><span data-stu-id="763c6-351">notes</span></span>|<span data-ttu-id="763c6-352">String</span><span class="sxs-lookup"><span data-stu-id="763c6-352">String</span></span>|<span data-ttu-id="763c6-353">Notas en el dispositivo creado por el Administrador de TI</span><span class="sxs-lookup"><span data-stu-id="763c6-353">Notes on the device created by IT Admin</span></span>|
|<span data-ttu-id="763c6-354">configurationManagerClientHealthState</span><span class="sxs-lookup"><span data-stu-id="763c6-354">configurationManagerClientHealthState</span></span>|[<span data-ttu-id="763c6-355">configurationManagerClientHealthState</span><span class="sxs-lookup"><span data-stu-id="763c6-355">configurationManagerClientHealthState</span></span>](../resources/intune-devices-configurationmanagerclienthealthstate.md)|<span data-ttu-id="763c6-356">Configuración Administrador cliente estado de mantenimiento, válido sólo para los dispositivos administrados por agente MDM/ConfigMgr</span><span class="sxs-lookup"><span data-stu-id="763c6-356">Configuration manager client health state, valid only for devices managed by MDM/ConfigMgr Agent</span></span>|



## <a name="response"></a><span data-ttu-id="763c6-357">Respuesta</span><span class="sxs-lookup"><span data-stu-id="763c6-357">Response</span></span>
<span data-ttu-id="763c6-358">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDevice](../resources/intune-devices-manageddevice.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="763c6-358">If successful, this method returns a `200 OK` response code and an updated [managedDevice](../resources/intune-devices-manageddevice.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="763c6-359">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="763c6-359">Example</span></span>
### <a name="request"></a><span data-ttu-id="763c6-360">Solicitud</span><span class="sxs-lookup"><span data-stu-id="763c6-360">Request</span></span>
<span data-ttu-id="763c6-361">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="763c6-361">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="763c6-362">Respuesta</span><span class="sxs-lookup"><span data-stu-id="763c6-362">Response</span></span>
<span data-ttu-id="763c6-p122">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="763c6-p122">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 7215

{
  "@odata.type": "#microsoft.graph.managedDevice",
  "id": "705c034c-034c-705c-4c03-5c704c035c70",
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





