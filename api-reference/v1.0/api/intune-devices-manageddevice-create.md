---
title: Crear managedDevice
description: Crear un objeto managedDevice.
ms.openlocfilehash: 9fa8efe9a4dd1a4ec753c25382f95f383bf0fe8f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029076"
---
# <a name="create-manageddevice"></a><span data-ttu-id="e3193-103">Crear managedDevice</span><span class="sxs-lookup"><span data-stu-id="e3193-103">Create managedDevice</span></span>

> <span data-ttu-id="e3193-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e3193-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e3193-105">Crear un objeto [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="e3193-105">Create a new [managedDevice](../resources/intune-devices-manageddevice.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e3193-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e3193-106">Prerequisites</span></span>
<span data-ttu-id="e3193-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e3193-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e3193-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e3193-109">Permission type</span></span>|<span data-ttu-id="e3193-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e3193-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e3193-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e3193-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e3193-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e3193-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="e3193-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e3193-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e3193-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e3193-114">Not supported.</span></span>|
|<span data-ttu-id="e3193-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e3193-115">Application</span></span>|<span data-ttu-id="e3193-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e3193-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e3193-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e3193-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices
POST /deviceManagement/managedDevices
POST /deviceManagement/detectedApps/{detectedAppId}/managedDevices
```

## <a name="request-headers"></a><span data-ttu-id="e3193-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e3193-118">Request headers</span></span>
|<span data-ttu-id="e3193-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e3193-119">Header</span></span>|<span data-ttu-id="e3193-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e3193-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e3193-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="e3193-121">Authorization</span></span>|<span data-ttu-id="e3193-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e3193-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e3193-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e3193-123">Accept</span></span>|<span data-ttu-id="e3193-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e3193-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e3193-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e3193-125">Request body</span></span>
<span data-ttu-id="e3193-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto managedDevice.</span><span class="sxs-lookup"><span data-stu-id="e3193-126">In the request body, supply a JSON representation for the managedDevice object.</span></span>

<span data-ttu-id="e3193-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto managedDevice.</span><span class="sxs-lookup"><span data-stu-id="e3193-127">The following table shows the properties that are required when you create the managedDevice.</span></span>

|<span data-ttu-id="e3193-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3193-128">Property</span></span>|<span data-ttu-id="e3193-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3193-129">Type</span></span>|<span data-ttu-id="e3193-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3193-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e3193-131">id</span><span class="sxs-lookup"><span data-stu-id="e3193-131">id</span></span>|<span data-ttu-id="e3193-132">String</span><span class="sxs-lookup"><span data-stu-id="e3193-132">String</span></span>|<span data-ttu-id="e3193-133">Identificador único del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-133">Unique Identifier for the device</span></span>|
|<span data-ttu-id="e3193-134">userId</span><span class="sxs-lookup"><span data-stu-id="e3193-134">userId</span></span>|<span data-ttu-id="e3193-135">String</span><span class="sxs-lookup"><span data-stu-id="e3193-135">String</span></span>|<span data-ttu-id="e3193-136">Identificador único del usuario asociado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-136">Unique Identifier for the user associated with the device</span></span>|
|<span data-ttu-id="e3193-137">deviceName</span><span class="sxs-lookup"><span data-stu-id="e3193-137">deviceName</span></span>|<span data-ttu-id="e3193-138">String</span><span class="sxs-lookup"><span data-stu-id="e3193-138">String</span></span>|<span data-ttu-id="e3193-139">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-139">Name of the device</span></span>|
|<span data-ttu-id="e3193-140">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="e3193-140">managedDeviceOwnerType</span></span>|[<span data-ttu-id="e3193-141">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="e3193-141">managedDeviceOwnerType</span></span>](../resources/intune-devices-manageddeviceownertype.md)|<span data-ttu-id="e3193-142">Propietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-142">Ownership of the device.</span></span> <span data-ttu-id="e3193-143">Puede ser 'compañía' o 'personal'.</span><span class="sxs-lookup"><span data-stu-id="e3193-143">Can be 'company' or 'personal'.</span></span> <span data-ttu-id="e3193-144">Los valores posibles son: `unknown`, `company` y `personal`.</span><span class="sxs-lookup"><span data-stu-id="e3193-144">Possible values are: `unknown`, `company`, `personal`.</span></span>|
|<span data-ttu-id="e3193-145">deviceActionResults</span><span class="sxs-lookup"><span data-stu-id="e3193-145">deviceActionResults</span></span>|<span data-ttu-id="e3193-146">Colección [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="e3193-146">[deviceActionResult](../resources/intune-devices-deviceactionresult.md) collection</span></span>|<span data-ttu-id="e3193-147">Lista de objetos deviceActionResult ComplexType.</span><span class="sxs-lookup"><span data-stu-id="e3193-147">List of ComplexType deviceActionResult objects.</span></span>|
|<span data-ttu-id="e3193-148">enrolledDateTime</span><span class="sxs-lookup"><span data-stu-id="e3193-148">enrolledDateTime</span></span>|<span data-ttu-id="e3193-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e3193-149">DateTimeOffset</span></span>|<span data-ttu-id="e3193-150">Hora de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-150">Enrollment time of the device.</span></span>|
|<span data-ttu-id="e3193-151">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="e3193-151">lastSyncDateTime</span></span>|<span data-ttu-id="e3193-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e3193-152">DateTimeOffset</span></span>|<span data-ttu-id="e3193-153">Fecha y hora en que el dispositivo completó por última vez una sincronización correcta con Intune.</span><span class="sxs-lookup"><span data-stu-id="e3193-153">The date and time that the device last completed a successful sync with Intune.</span></span>|
|<span data-ttu-id="e3193-154">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="e3193-154">operatingSystem</span></span>|<span data-ttu-id="e3193-155">String</span><span class="sxs-lookup"><span data-stu-id="e3193-155">String</span></span>|<span data-ttu-id="e3193-156">Sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-156">Operating system of the device.</span></span> <span data-ttu-id="e3193-157">Windows, iOS, etc.</span><span class="sxs-lookup"><span data-stu-id="e3193-157">Windows, iOS, etc.</span></span>|
|<span data-ttu-id="e3193-158">complianceState</span><span class="sxs-lookup"><span data-stu-id="e3193-158">complianceState</span></span>|[<span data-ttu-id="e3193-159">complianceState</span><span class="sxs-lookup"><span data-stu-id="e3193-159">complianceState</span></span>](../resources/intune-devices-compliancestate.md)|<span data-ttu-id="e3193-160">Estado de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-160">Compliance state of the device.</span></span> <span data-ttu-id="e3193-161">Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod` y `configManager`.</span><span class="sxs-lookup"><span data-stu-id="e3193-161">Possible values are: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod`, `configManager`.</span></span>|
|<span data-ttu-id="e3193-162">jailBroken</span><span class="sxs-lookup"><span data-stu-id="e3193-162">jailBroken</span></span>|<span data-ttu-id="e3193-163">String</span><span class="sxs-lookup"><span data-stu-id="e3193-163">String</span></span>|<span data-ttu-id="e3193-164">Indica si se trata de un dispositivo liberado o con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="e3193-164">whether the device is jail broken or rooted.</span></span>|
|<span data-ttu-id="e3193-165">managementAgent</span><span class="sxs-lookup"><span data-stu-id="e3193-165">managementAgent</span></span>|[<span data-ttu-id="e3193-166">managementAgentType</span><span class="sxs-lookup"><span data-stu-id="e3193-166">managementAgentType</span></span>](../resources/intune-devices-managementagenttype.md)|<span data-ttu-id="e3193-167">Canal de administración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-167">Management channel of the device.</span></span> <span data-ttu-id="e3193-168">Intune, EAS, etc. Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf` y `googleCloudDevicePolicyController`.</span><span class="sxs-lookup"><span data-stu-id="e3193-168">Intune, EAS, etc. Possible values are: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`.</span></span>|
|<span data-ttu-id="e3193-169">osVersion</span><span class="sxs-lookup"><span data-stu-id="e3193-169">osVersion</span></span>|<span data-ttu-id="e3193-170">String</span><span class="sxs-lookup"><span data-stu-id="e3193-170">String</span></span>|<span data-ttu-id="e3193-171">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-171">Operating system version of the device.</span></span>|
|<span data-ttu-id="e3193-172">easActivated</span><span class="sxs-lookup"><span data-stu-id="e3193-172">easActivated</span></span>|<span data-ttu-id="e3193-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="e3193-173">Boolean</span></span>|<span data-ttu-id="e3193-174">Indica si el dispositivo tiene Exchange ActiveSync activado.</span><span class="sxs-lookup"><span data-stu-id="e3193-174">Whether the device is Exchange ActiveSync activated.</span></span>|
|<span data-ttu-id="e3193-175">easDeviceId</span><span class="sxs-lookup"><span data-stu-id="e3193-175">easDeviceId</span></span>|<span data-ttu-id="e3193-176">String</span><span class="sxs-lookup"><span data-stu-id="e3193-176">String</span></span>|<span data-ttu-id="e3193-177">Identificador de Exchange ActiveSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-177">Exchange ActiveSync Id of the device.</span></span>|
|<span data-ttu-id="e3193-178">easActivationDateTime</span><span class="sxs-lookup"><span data-stu-id="e3193-178">easActivationDateTime</span></span>|<span data-ttu-id="e3193-179">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e3193-179">DateTimeOffset</span></span>|<span data-ttu-id="e3193-180">Hora de activación de Exchange ActivationSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-180">Exchange ActivationSync activation time of the device.</span></span>|
|<span data-ttu-id="e3193-181">azureADRegistered</span><span class="sxs-lookup"><span data-stu-id="e3193-181">azureADRegistered</span></span>|<span data-ttu-id="e3193-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="e3193-182">Boolean</span></span>|<span data-ttu-id="e3193-183">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e3193-183">Whether the device is Azure Active Directory registered.</span></span>|
|<span data-ttu-id="e3193-184">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="e3193-184">deviceEnrollmentType</span></span>|[<span data-ttu-id="e3193-185">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="e3193-185">deviceEnrollmentType</span></span>](../resources/intune-devices-deviceenrollmenttype.md)|<span data-ttu-id="e3193-186">Tipo de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-186">Enrollment type of the device.</span></span> <span data-ttu-id="e3193-187">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="e3193-187">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="e3193-188">activationLockBypassCode</span><span class="sxs-lookup"><span data-stu-id="e3193-188">activationLockBypassCode</span></span>|<span data-ttu-id="e3193-189">String</span><span class="sxs-lookup"><span data-stu-id="e3193-189">String</span></span>|<span data-ttu-id="e3193-190">Código que permite que se omita el bloqueo de activación en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-190">Code that allows the Activation Lock on a device to be bypassed.</span></span>|
|<span data-ttu-id="e3193-191">emailAddress</span><span class="sxs-lookup"><span data-stu-id="e3193-191">emailAddress</span></span>|<span data-ttu-id="e3193-192">String</span><span class="sxs-lookup"><span data-stu-id="e3193-192">String</span></span>|<span data-ttu-id="e3193-193">Direcciones de correo electrónico del usuario asociado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-193">Email(s) for the user associated with the device</span></span>|
|<span data-ttu-id="e3193-194">azureADDeviceId</span><span class="sxs-lookup"><span data-stu-id="e3193-194">azureADDeviceId</span></span>|<span data-ttu-id="e3193-195">String</span><span class="sxs-lookup"><span data-stu-id="e3193-195">String</span></span>|<span data-ttu-id="e3193-196">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e3193-196">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="e3193-197">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3193-197">Read only.</span></span>|
|<span data-ttu-id="e3193-198">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="e3193-198">deviceRegistrationState</span></span>|[<span data-ttu-id="e3193-199">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="e3193-199">deviceRegistrationState</span></span>](../resources/intune-devices-deviceregistrationstate.md)|<span data-ttu-id="e3193-200">Estado de registro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-200">Device registration state.</span></span> <span data-ttu-id="e3193-201">Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="e3193-201">Possible values are: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment`, `unknown`.</span></span>|
|<span data-ttu-id="e3193-202">deviceCategoryDisplayName</span><span class="sxs-lookup"><span data-stu-id="e3193-202">deviceCategoryDisplayName</span></span>|<span data-ttu-id="e3193-203">String</span><span class="sxs-lookup"><span data-stu-id="e3193-203">String</span></span>|<span data-ttu-id="e3193-204">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-204">Device category display name</span></span>|
|<span data-ttu-id="e3193-205">isSupervised</span><span class="sxs-lookup"><span data-stu-id="e3193-205">isSupervised</span></span>|<span data-ttu-id="e3193-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="e3193-206">Boolean</span></span>|<span data-ttu-id="e3193-207">Estado supervisado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-207">Device supervised status</span></span>|
|<span data-ttu-id="e3193-208">exchangeLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="e3193-208">exchangeLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="e3193-209">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e3193-209">DateTimeOffset</span></span>|<span data-ttu-id="e3193-210">Última vez que el dispositivo estableció contacto con Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3193-210">Last time the device contacted Exchange.</span></span>|
|<span data-ttu-id="e3193-211">exchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="e3193-211">exchangeAccessState</span></span>|[<span data-ttu-id="e3193-212">deviceManagementExchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="e3193-212">deviceManagementExchangeAccessState</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstate.md)|<span data-ttu-id="e3193-213">Estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3193-213">The Access State of the device in Exchange.</span></span> <span data-ttu-id="e3193-214">Los valores posibles son: `none`, `unknown`, `allowed`, `blocked` y `quarantined`.</span><span class="sxs-lookup"><span data-stu-id="e3193-214">Possible values are: `none`, `unknown`, `allowed`, `blocked`, `quarantined`.</span></span>|
|<span data-ttu-id="e3193-215">exchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="e3193-215">exchangeAccessStateReason</span></span>|[<span data-ttu-id="e3193-216">deviceManagementExchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="e3193-216">deviceManagementExchangeAccessStateReason</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstatereason.md)|<span data-ttu-id="e3193-217">Motivo del estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3193-217">The reason for the device's access state in Exchange.</span></span> <span data-ttu-id="e3193-218">Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword` y `deviceNotKnownWithManagedApp`.</span><span class="sxs-lookup"><span data-stu-id="e3193-218">Possible values are: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword`, `deviceNotKnownWithManagedApp`.</span></span>|
|<span data-ttu-id="e3193-219">remoteAssistanceSessionUrl</span><span class="sxs-lookup"><span data-stu-id="e3193-219">remoteAssistanceSessionUrl</span></span>|<span data-ttu-id="e3193-220">String</span><span class="sxs-lookup"><span data-stu-id="e3193-220">String</span></span>|<span data-ttu-id="e3193-221">Dirección URL que permite que se establezca una sesión remota con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-221">Url that allows a Remote Assistance session to be established with the device.</span></span>|
|<span data-ttu-id="e3193-222">remoteAssistanceSessionErrorDetails</span><span class="sxs-lookup"><span data-stu-id="e3193-222">remoteAssistanceSessionErrorDetails</span></span>|<span data-ttu-id="e3193-223">String</span><span class="sxs-lookup"><span data-stu-id="e3193-223">String</span></span>|<span data-ttu-id="e3193-224">Cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="e3193-224">An error string that identifies issues when creating Remote Assistance session objects.</span></span>|
|<span data-ttu-id="e3193-225">isEncrypted</span><span class="sxs-lookup"><span data-stu-id="e3193-225">isEncrypted</span></span>|<span data-ttu-id="e3193-226">Booleano</span><span class="sxs-lookup"><span data-stu-id="e3193-226">Boolean</span></span>|<span data-ttu-id="e3193-227">Estado del cifrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-227">Device encryption status</span></span>|
|<span data-ttu-id="e3193-228">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e3193-228">userPrincipalName</span></span>|<span data-ttu-id="e3193-229">String</span><span class="sxs-lookup"><span data-stu-id="e3193-229">String</span></span>|<span data-ttu-id="e3193-230">Nombre principal de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-230">Device user principal name</span></span>|
|<span data-ttu-id="e3193-231">model</span><span class="sxs-lookup"><span data-stu-id="e3193-231">model</span></span>|<span data-ttu-id="e3193-232">String</span><span class="sxs-lookup"><span data-stu-id="e3193-232">String</span></span>|<span data-ttu-id="e3193-233">Modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-233">Model of the device</span></span>|
|<span data-ttu-id="e3193-234">manufacturer</span><span class="sxs-lookup"><span data-stu-id="e3193-234">manufacturer</span></span>|<span data-ttu-id="e3193-235">String</span><span class="sxs-lookup"><span data-stu-id="e3193-235">String</span></span>|<span data-ttu-id="e3193-236">Fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-236">Manufacturer of the device</span></span>|
|<span data-ttu-id="e3193-237">imei</span><span class="sxs-lookup"><span data-stu-id="e3193-237">imei</span></span>|<span data-ttu-id="e3193-238">String</span><span class="sxs-lookup"><span data-stu-id="e3193-238">String</span></span>|<span data-ttu-id="e3193-239">IMEI</span><span class="sxs-lookup"><span data-stu-id="e3193-239">IMEI</span></span>|
|<span data-ttu-id="e3193-240">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="e3193-240">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="e3193-241">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e3193-241">DateTimeOffset</span></span>|<span data-ttu-id="e3193-242">Fecha y hora en que expira el período de gracia de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-242">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="e3193-243">serialNumber</span><span class="sxs-lookup"><span data-stu-id="e3193-243">serialNumber</span></span>|<span data-ttu-id="e3193-244">String</span><span class="sxs-lookup"><span data-stu-id="e3193-244">String</span></span>|<span data-ttu-id="e3193-245">Número de serie.</span><span class="sxs-lookup"><span data-stu-id="e3193-245">SerialNumber</span></span>|
|<span data-ttu-id="e3193-246">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="e3193-246">phoneNumber</span></span>|<span data-ttu-id="e3193-247">String</span><span class="sxs-lookup"><span data-stu-id="e3193-247">String</span></span>|<span data-ttu-id="e3193-248">Número de teléfono del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-248">Phone number of the device</span></span>|
|<span data-ttu-id="e3193-249">androidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="e3193-249">androidSecurityPatchLevel</span></span>|<span data-ttu-id="e3193-250">String</span><span class="sxs-lookup"><span data-stu-id="e3193-250">String</span></span>|<span data-ttu-id="e3193-251">Nivel de revisión de seguridad de Android.</span><span class="sxs-lookup"><span data-stu-id="e3193-251">Android security patch level</span></span>|
|<span data-ttu-id="e3193-252">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="e3193-252">userDisplayName</span></span>|<span data-ttu-id="e3193-253">String</span><span class="sxs-lookup"><span data-stu-id="e3193-253">String</span></span>|<span data-ttu-id="e3193-254">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="e3193-254">User display name</span></span>|
|<span data-ttu-id="e3193-255">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="e3193-255">configurationManagerClientEnabledFeatures</span></span>|[<span data-ttu-id="e3193-256">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="e3193-256">configurationManagerClientEnabledFeatures</span></span>](../resources/intune-devices-configurationmanagerclientenabledfeatures.md)|<span data-ttu-id="e3193-257">Características activadas del cliente ConfigrMgr.</span><span class="sxs-lookup"><span data-stu-id="e3193-257">ConfigrMgr client enabled features</span></span>|
|<span data-ttu-id="e3193-258">wiFiMacAddress</span><span class="sxs-lookup"><span data-stu-id="e3193-258">wiFiMacAddress</span></span>|<span data-ttu-id="e3193-259">String</span><span class="sxs-lookup"><span data-stu-id="e3193-259">String</span></span>|<span data-ttu-id="e3193-260">MAC de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="e3193-260">Wi-Fi MAC</span></span>|
|<span data-ttu-id="e3193-261">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="e3193-261">deviceHealthAttestationState</span></span>|[<span data-ttu-id="e3193-262">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="e3193-262">deviceHealthAttestationState</span></span>](../resources/intune-devices-devicehealthattestationstate.md)|<span data-ttu-id="e3193-263">Estado de la atestación de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-263">The device health attestation state.</span></span>|
|<span data-ttu-id="e3193-264">subscriberCarrier</span><span class="sxs-lookup"><span data-stu-id="e3193-264">subscriberCarrier</span></span>|<span data-ttu-id="e3193-265">String</span><span class="sxs-lookup"><span data-stu-id="e3193-265">String</span></span>|<span data-ttu-id="e3193-266">Operador del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="e3193-266">Subscriber Carrier</span></span>|
|<span data-ttu-id="e3193-267">meid</span><span class="sxs-lookup"><span data-stu-id="e3193-267">meid</span></span>|<span data-ttu-id="e3193-268">String</span><span class="sxs-lookup"><span data-stu-id="e3193-268">String</span></span>|<span data-ttu-id="e3193-269">MEID</span><span class="sxs-lookup"><span data-stu-id="e3193-269">MEID</span></span>|
|<span data-ttu-id="e3193-270">totalStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="e3193-270">totalStorageSpaceInBytes</span></span>|<span data-ttu-id="e3193-271">Int64</span><span class="sxs-lookup"><span data-stu-id="e3193-271">Int64</span></span>|<span data-ttu-id="e3193-272">Almacenamiento total en bytes.</span><span class="sxs-lookup"><span data-stu-id="e3193-272">Total Storage in Bytes</span></span>|
|<span data-ttu-id="e3193-273">freeStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="e3193-273">freeStorageSpaceInBytes</span></span>|<span data-ttu-id="e3193-274">Int64</span><span class="sxs-lookup"><span data-stu-id="e3193-274">Int64</span></span>|<span data-ttu-id="e3193-275">Almacenamiento disponible en bytes.</span><span class="sxs-lookup"><span data-stu-id="e3193-275">Free Storage in Bytes</span></span>|
|<span data-ttu-id="e3193-276">managedDeviceName</span><span class="sxs-lookup"><span data-stu-id="e3193-276">managedDeviceName</span></span>|<span data-ttu-id="e3193-277">String</span><span class="sxs-lookup"><span data-stu-id="e3193-277">String</span></span>|<span data-ttu-id="e3193-278">Nombre generado automáticamente para identificar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e3193-278">Automatically generated name to identify a device.</span></span> <span data-ttu-id="e3193-279">Se puede sobrescribir con un nombre descriptivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="e3193-279">Can be overwritten to a user friendly name.</span></span>|
|<span data-ttu-id="e3193-280">partnerReportedThreatState</span><span class="sxs-lookup"><span data-stu-id="e3193-280">partnerReportedThreatState</span></span>|[<span data-ttu-id="e3193-281">managedDevicePartnerReportedHealthState</span><span class="sxs-lookup"><span data-stu-id="e3193-281">managedDevicePartnerReportedHealthState</span></span>](../resources/intune-devices-manageddevicepartnerreportedhealthstate.md)|<span data-ttu-id="e3193-282">Indica el estado de amenazas de un dispositivo cuando la cuenta y el dispositivo usan un partner de Mobile Threat Defense.</span><span class="sxs-lookup"><span data-stu-id="e3193-282">Indicates the threat state of a device when a Mobile Threat Defense partner is in use by the account and device.</span></span> <span data-ttu-id="e3193-283">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e3193-283">Read Only.</span></span> <span data-ttu-id="e3193-284">Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised` y `misconfigured`.</span><span class="sxs-lookup"><span data-stu-id="e3193-284">Possible values are: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised`, `misconfigured`.</span></span>|



## <a name="response"></a><span data-ttu-id="e3193-285">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3193-285">Response</span></span>
<span data-ttu-id="e3193-286">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [managedDevice](../resources/intune-devices-manageddevice.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e3193-286">If successful, this method returns a `201 Created` response code and a [managedDevice](../resources/intune-devices-manageddevice.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e3193-287">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e3193-287">Example</span></span>
### <a name="request"></a><span data-ttu-id="e3193-288">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e3193-288">Request</span></span>
<span data-ttu-id="e3193-289">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e3193-289">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices
Content-type: application/json
Content-length: 4656

{
  "@odata.type": "#microsoft.graph.managedDevice",
  "userId": "User Id value",
  "deviceName": "Device Name value",
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
  "enrolledDateTime": "2016-12-31T23:59:43.797191-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "operatingSystem": "Operating System value",
  "complianceState": "compliant",
  "jailBroken": "Jail Broken value",
  "managementAgent": "mdm",
  "osVersion": "Os Version value",
  "easActivated": true,
  "easDeviceId": "Eas Device Id value",
  "easActivationDateTime": "2016-12-31T23:59:43.4878784-08:00",
  "azureADRegistered": true,
  "deviceEnrollmentType": "userEnrollment",
  "activationLockBypassCode": "Activation Lock Bypass Code value",
  "emailAddress": "Email Address value",
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
  "partnerReportedThreatState": "activated"
}
```

### <a name="response"></a><span data-ttu-id="e3193-290">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e3193-290">Response</span></span>
<span data-ttu-id="e3193-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e3193-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 4705

{
  "@odata.type": "#microsoft.graph.managedDevice",
  "id": "705c034c-034c-705c-4c03-5c704c035c70",
  "userId": "User Id value",
  "deviceName": "Device Name value",
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
  "enrolledDateTime": "2016-12-31T23:59:43.797191-08:00",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "operatingSystem": "Operating System value",
  "complianceState": "compliant",
  "jailBroken": "Jail Broken value",
  "managementAgent": "mdm",
  "osVersion": "Os Version value",
  "easActivated": true,
  "easDeviceId": "Eas Device Id value",
  "easActivationDateTime": "2016-12-31T23:59:43.4878784-08:00",
  "azureADRegistered": true,
  "deviceEnrollmentType": "userEnrollment",
  "activationLockBypassCode": "Activation Lock Bypass Code value",
  "emailAddress": "Email Address value",
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
  "partnerReportedThreatState": "activated"
}
```


