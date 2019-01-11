---
title: Actualizar managedDevice
description: Actualiza las propiedades de un objeto managedDevice.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 242b9416b94072348fb1bfa1adc07d93274e45d8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27835703"
---
# <a name="update-manageddevice"></a><span data-ttu-id="7da02-103">Actualizar managedDevice</span><span class="sxs-lookup"><span data-stu-id="7da02-103">Update managedDevice</span></span>

> <span data-ttu-id="7da02-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7da02-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7da02-105">Actualiza las propiedades de un objeto [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="7da02-105">Update the properties of a [managedDevice](../resources/intune-devices-manageddevice.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7da02-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7da02-106">Prerequisites</span></span>
<span data-ttu-id="7da02-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7da02-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7da02-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7da02-109">Permission type</span></span>|<span data-ttu-id="7da02-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7da02-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7da02-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7da02-111">Delegated (work or school account)</span></span>|<span data-ttu-id="7da02-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7da02-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="7da02-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7da02-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7da02-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7da02-114">Not supported.</span></span>|
|<span data-ttu-id="7da02-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7da02-115">Application</span></span>|<span data-ttu-id="7da02-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7da02-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7da02-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7da02-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /users/{usersId}/managedDevices/{managedDeviceId}
PATCH /deviceManagement/managedDevices/{managedDeviceId}
PATCH /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}
```

## <a name="request-headers"></a><span data-ttu-id="7da02-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7da02-118">Request headers</span></span>
|<span data-ttu-id="7da02-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7da02-119">Header</span></span>|<span data-ttu-id="7da02-120">Valor</span><span class="sxs-lookup"><span data-stu-id="7da02-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7da02-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="7da02-121">Authorization</span></span>|<span data-ttu-id="7da02-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7da02-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7da02-123">Accept</span><span class="sxs-lookup"><span data-stu-id="7da02-123">Accept</span></span>|<span data-ttu-id="7da02-124">application/json</span><span class="sxs-lookup"><span data-stu-id="7da02-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7da02-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7da02-125">Request body</span></span>
<span data-ttu-id="7da02-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="7da02-126">In the request body, supply a JSON representation for the [managedDevice](../resources/intune-devices-manageddevice.md) object.</span></span>

<span data-ttu-id="7da02-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="7da02-127">The following table shows the properties that are required when you create the [managedDevice](../resources/intune-devices-manageddevice.md).</span></span>

|<span data-ttu-id="7da02-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7da02-128">Property</span></span>|<span data-ttu-id="7da02-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7da02-129">Type</span></span>|<span data-ttu-id="7da02-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7da02-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7da02-131">id</span><span class="sxs-lookup"><span data-stu-id="7da02-131">id</span></span>|<span data-ttu-id="7da02-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-132">String</span></span>|<span data-ttu-id="7da02-133">Identificador único del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-133">Unique Identifier for the device</span></span>|
|<span data-ttu-id="7da02-134">userId</span><span class="sxs-lookup"><span data-stu-id="7da02-134">userId</span></span>|<span data-ttu-id="7da02-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-135">String</span></span>|<span data-ttu-id="7da02-136">Identificador único del usuario asociado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-136">Unique Identifier for the user associated with the device</span></span>|
|<span data-ttu-id="7da02-137">deviceName</span><span class="sxs-lookup"><span data-stu-id="7da02-137">deviceName</span></span>|<span data-ttu-id="7da02-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-138">String</span></span>|<span data-ttu-id="7da02-139">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-139">Name of the device</span></span>|
|<span data-ttu-id="7da02-140">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="7da02-140">managedDeviceOwnerType</span></span>|[<span data-ttu-id="7da02-141">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="7da02-141">managedDeviceOwnerType</span></span>](../resources/intune-devices-manageddeviceownertype.md)|<span data-ttu-id="7da02-142">Propietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-142">Ownership of the device.</span></span> <span data-ttu-id="7da02-143">Puede ser 'compañía' o 'personal'.</span><span class="sxs-lookup"><span data-stu-id="7da02-143">Can be 'company' or 'personal'.</span></span> <span data-ttu-id="7da02-144">Los valores posibles son: `unknown`, `company` y `personal`.</span><span class="sxs-lookup"><span data-stu-id="7da02-144">Possible values are: `unknown`, `company`, `personal`.</span></span>|
|<span data-ttu-id="7da02-145">deviceActionResults</span><span class="sxs-lookup"><span data-stu-id="7da02-145">deviceActionResults</span></span>|<span data-ttu-id="7da02-146">Colección [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="7da02-146">[deviceActionResult](../resources/intune-devices-deviceactionresult.md) collection</span></span>|<span data-ttu-id="7da02-147">Lista de objetos deviceActionResult ComplexType.</span><span class="sxs-lookup"><span data-stu-id="7da02-147">List of ComplexType deviceActionResult objects.</span></span>|
|<span data-ttu-id="7da02-148">enrolledDateTime</span><span class="sxs-lookup"><span data-stu-id="7da02-148">enrolledDateTime</span></span>|<span data-ttu-id="7da02-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7da02-149">DateTimeOffset</span></span>|<span data-ttu-id="7da02-150">Hora de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-150">Enrollment time of the device.</span></span>|
|<span data-ttu-id="7da02-151">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="7da02-151">lastSyncDateTime</span></span>|<span data-ttu-id="7da02-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7da02-152">DateTimeOffset</span></span>|<span data-ttu-id="7da02-153">Fecha y hora en que el dispositivo completó por última vez una sincronización correcta con Intune.</span><span class="sxs-lookup"><span data-stu-id="7da02-153">The date and time that the device last completed a successful sync with Intune.</span></span>|
|<span data-ttu-id="7da02-154">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="7da02-154">operatingSystem</span></span>|<span data-ttu-id="7da02-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-155">String</span></span>|<span data-ttu-id="7da02-156">Sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-156">Operating system of the device.</span></span> <span data-ttu-id="7da02-157">Windows, iOS, etc.</span><span class="sxs-lookup"><span data-stu-id="7da02-157">Windows, iOS, etc.</span></span>|
|<span data-ttu-id="7da02-158">complianceState</span><span class="sxs-lookup"><span data-stu-id="7da02-158">complianceState</span></span>|[<span data-ttu-id="7da02-159">complianceState</span><span class="sxs-lookup"><span data-stu-id="7da02-159">complianceState</span></span>](../resources/intune-devices-compliancestate.md)|<span data-ttu-id="7da02-160">Estado de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-160">Compliance state of the device.</span></span> <span data-ttu-id="7da02-161">Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod` y `configManager`.</span><span class="sxs-lookup"><span data-stu-id="7da02-161">Possible values are: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod`, `configManager`.</span></span>|
|<span data-ttu-id="7da02-162">jailBroken</span><span class="sxs-lookup"><span data-stu-id="7da02-162">jailBroken</span></span>|<span data-ttu-id="7da02-163">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-163">String</span></span>|<span data-ttu-id="7da02-164">Indica si se trata de un dispositivo liberado o con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="7da02-164">whether the device is jail broken or rooted.</span></span>|
|<span data-ttu-id="7da02-165">managementAgent</span><span class="sxs-lookup"><span data-stu-id="7da02-165">managementAgent</span></span>|[<span data-ttu-id="7da02-166">managementAgentType</span><span class="sxs-lookup"><span data-stu-id="7da02-166">managementAgentType</span></span>](../resources/intune-devices-managementagenttype.md)|<span data-ttu-id="7da02-167">Canal de administración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-167">Management channel of the device.</span></span> <span data-ttu-id="7da02-168">Intune, EAS, etc. Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf` y `googleCloudDevicePolicyController`.</span><span class="sxs-lookup"><span data-stu-id="7da02-168">Intune, EAS, etc. Possible values are: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`.</span></span>|
|<span data-ttu-id="7da02-169">osVersion</span><span class="sxs-lookup"><span data-stu-id="7da02-169">osVersion</span></span>|<span data-ttu-id="7da02-170">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-170">String</span></span>|<span data-ttu-id="7da02-171">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-171">Operating system version of the device.</span></span>|
|<span data-ttu-id="7da02-172">easActivated</span><span class="sxs-lookup"><span data-stu-id="7da02-172">easActivated</span></span>|<span data-ttu-id="7da02-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="7da02-173">Boolean</span></span>|<span data-ttu-id="7da02-174">Indica si el dispositivo tiene Exchange ActiveSync activado.</span><span class="sxs-lookup"><span data-stu-id="7da02-174">Whether the device is Exchange ActiveSync activated.</span></span>|
|<span data-ttu-id="7da02-175">easDeviceId</span><span class="sxs-lookup"><span data-stu-id="7da02-175">easDeviceId</span></span>|<span data-ttu-id="7da02-176">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-176">String</span></span>|<span data-ttu-id="7da02-177">Identificador de Exchange ActiveSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-177">Exchange ActiveSync Id of the device.</span></span>|
|<span data-ttu-id="7da02-178">easActivationDateTime</span><span class="sxs-lookup"><span data-stu-id="7da02-178">easActivationDateTime</span></span>|<span data-ttu-id="7da02-179">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7da02-179">DateTimeOffset</span></span>|<span data-ttu-id="7da02-180">Hora de activación de Exchange ActivationSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-180">Exchange ActivationSync activation time of the device.</span></span>|
|<span data-ttu-id="7da02-181">azureADRegistered</span><span class="sxs-lookup"><span data-stu-id="7da02-181">azureADRegistered</span></span>|<span data-ttu-id="7da02-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="7da02-182">Boolean</span></span>|<span data-ttu-id="7da02-183">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7da02-183">Whether the device is Azure Active Directory registered.</span></span>|
|<span data-ttu-id="7da02-184">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="7da02-184">deviceEnrollmentType</span></span>|[<span data-ttu-id="7da02-185">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="7da02-185">deviceEnrollmentType</span></span>](../resources/intune-devices-deviceenrollmenttype.md)|<span data-ttu-id="7da02-186">Tipo de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-186">Enrollment type of the device.</span></span> <span data-ttu-id="7da02-187">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="7da02-187">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="7da02-188">activationLockBypassCode</span><span class="sxs-lookup"><span data-stu-id="7da02-188">activationLockBypassCode</span></span>|<span data-ttu-id="7da02-189">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-189">String</span></span>|<span data-ttu-id="7da02-190">Código que permite que se omita el bloqueo de activación en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-190">Code that allows the Activation Lock on a device to be bypassed.</span></span>|
|<span data-ttu-id="7da02-191">emailAddress</span><span class="sxs-lookup"><span data-stu-id="7da02-191">emailAddress</span></span>|<span data-ttu-id="7da02-192">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-192">String</span></span>|<span data-ttu-id="7da02-193">Direcciones de correo electrónico del usuario asociado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-193">Email(s) for the user associated with the device</span></span>|
|<span data-ttu-id="7da02-194">azureADDeviceId</span><span class="sxs-lookup"><span data-stu-id="7da02-194">azureADDeviceId</span></span>|<span data-ttu-id="7da02-195">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-195">String</span></span>|<span data-ttu-id="7da02-196">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7da02-196">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="7da02-197">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7da02-197">Read only.</span></span>|
|<span data-ttu-id="7da02-198">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="7da02-198">deviceRegistrationState</span></span>|[<span data-ttu-id="7da02-199">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="7da02-199">deviceRegistrationState</span></span>](../resources/intune-devices-deviceregistrationstate.md)|<span data-ttu-id="7da02-200">Estado de registro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-200">Device registration state.</span></span> <span data-ttu-id="7da02-201">Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="7da02-201">Possible values are: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment`, `unknown`.</span></span>|
|<span data-ttu-id="7da02-202">deviceCategoryDisplayName</span><span class="sxs-lookup"><span data-stu-id="7da02-202">deviceCategoryDisplayName</span></span>|<span data-ttu-id="7da02-203">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-203">String</span></span>|<span data-ttu-id="7da02-204">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-204">Device category display name</span></span>|
|<span data-ttu-id="7da02-205">isSupervised</span><span class="sxs-lookup"><span data-stu-id="7da02-205">isSupervised</span></span>|<span data-ttu-id="7da02-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="7da02-206">Boolean</span></span>|<span data-ttu-id="7da02-207">Estado supervisado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-207">Device supervised status</span></span>|
|<span data-ttu-id="7da02-208">exchangeLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="7da02-208">exchangeLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="7da02-209">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7da02-209">DateTimeOffset</span></span>|<span data-ttu-id="7da02-210">Última vez que el dispositivo estableció contacto con Exchange.</span><span class="sxs-lookup"><span data-stu-id="7da02-210">Last time the device contacted Exchange.</span></span>|
|<span data-ttu-id="7da02-211">exchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="7da02-211">exchangeAccessState</span></span>|[<span data-ttu-id="7da02-212">deviceManagementExchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="7da02-212">deviceManagementExchangeAccessState</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstate.md)|<span data-ttu-id="7da02-213">Estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="7da02-213">The Access State of the device in Exchange.</span></span> <span data-ttu-id="7da02-214">Los valores posibles son: `none`, `unknown`, `allowed`, `blocked` y `quarantined`.</span><span class="sxs-lookup"><span data-stu-id="7da02-214">Possible values are: `none`, `unknown`, `allowed`, `blocked`, `quarantined`.</span></span>|
|<span data-ttu-id="7da02-215">exchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="7da02-215">exchangeAccessStateReason</span></span>|[<span data-ttu-id="7da02-216">deviceManagementExchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="7da02-216">deviceManagementExchangeAccessStateReason</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstatereason.md)|<span data-ttu-id="7da02-217">Motivo del estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="7da02-217">The reason for the device's access state in Exchange.</span></span> <span data-ttu-id="7da02-218">Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword` y `deviceNotKnownWithManagedApp`.</span><span class="sxs-lookup"><span data-stu-id="7da02-218">Possible values are: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword`, `deviceNotKnownWithManagedApp`.</span></span>|
|<span data-ttu-id="7da02-219">remoteAssistanceSessionUrl</span><span class="sxs-lookup"><span data-stu-id="7da02-219">remoteAssistanceSessionUrl</span></span>|<span data-ttu-id="7da02-220">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-220">String</span></span>|<span data-ttu-id="7da02-221">Dirección URL que permite que se establezca una sesión remota con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-221">Url that allows a Remote Assistance session to be established with the device.</span></span>|
|<span data-ttu-id="7da02-222">remoteAssistanceSessionErrorDetails</span><span class="sxs-lookup"><span data-stu-id="7da02-222">remoteAssistanceSessionErrorDetails</span></span>|<span data-ttu-id="7da02-223">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-223">String</span></span>|<span data-ttu-id="7da02-224">Cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="7da02-224">An error string that identifies issues when creating Remote Assistance session objects.</span></span>|
|<span data-ttu-id="7da02-225">isEncrypted</span><span class="sxs-lookup"><span data-stu-id="7da02-225">isEncrypted</span></span>|<span data-ttu-id="7da02-226">Booleano</span><span class="sxs-lookup"><span data-stu-id="7da02-226">Boolean</span></span>|<span data-ttu-id="7da02-227">Estado del cifrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-227">Device encryption status</span></span>|
|<span data-ttu-id="7da02-228">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7da02-228">userPrincipalName</span></span>|<span data-ttu-id="7da02-229">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-229">String</span></span>|<span data-ttu-id="7da02-230">Nombre principal de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-230">Device user principal name</span></span>|
|<span data-ttu-id="7da02-231">model</span><span class="sxs-lookup"><span data-stu-id="7da02-231">model</span></span>|<span data-ttu-id="7da02-232">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-232">String</span></span>|<span data-ttu-id="7da02-233">Modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-233">Model of the device</span></span>|
|<span data-ttu-id="7da02-234">manufacturer</span><span class="sxs-lookup"><span data-stu-id="7da02-234">manufacturer</span></span>|<span data-ttu-id="7da02-235">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-235">String</span></span>|<span data-ttu-id="7da02-236">Fabricante del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-236">Manufacturer of the device</span></span>|
|<span data-ttu-id="7da02-237">imei</span><span class="sxs-lookup"><span data-stu-id="7da02-237">imei</span></span>|<span data-ttu-id="7da02-238">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-238">String</span></span>|<span data-ttu-id="7da02-239">IMEI</span><span class="sxs-lookup"><span data-stu-id="7da02-239">IMEI</span></span>|
|<span data-ttu-id="7da02-240">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="7da02-240">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="7da02-241">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7da02-241">DateTimeOffset</span></span>|<span data-ttu-id="7da02-242">Fecha y hora en que expira el período de gracia de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-242">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="7da02-243">serialNumber</span><span class="sxs-lookup"><span data-stu-id="7da02-243">serialNumber</span></span>|<span data-ttu-id="7da02-244">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-244">String</span></span>|<span data-ttu-id="7da02-245">Número de serie.</span><span class="sxs-lookup"><span data-stu-id="7da02-245">SerialNumber</span></span>|
|<span data-ttu-id="7da02-246">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="7da02-246">phoneNumber</span></span>|<span data-ttu-id="7da02-247">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-247">String</span></span>|<span data-ttu-id="7da02-248">Número de teléfono del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-248">Phone number of the device</span></span>|
|<span data-ttu-id="7da02-249">androidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="7da02-249">androidSecurityPatchLevel</span></span>|<span data-ttu-id="7da02-250">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-250">String</span></span>|<span data-ttu-id="7da02-251">Nivel de revisión de seguridad de Android.</span><span class="sxs-lookup"><span data-stu-id="7da02-251">Android security patch level</span></span>|
|<span data-ttu-id="7da02-252">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="7da02-252">userDisplayName</span></span>|<span data-ttu-id="7da02-253">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-253">String</span></span>|<span data-ttu-id="7da02-254">Nombre para mostrar del usuario.</span><span class="sxs-lookup"><span data-stu-id="7da02-254">User display name</span></span>|
|<span data-ttu-id="7da02-255">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="7da02-255">configurationManagerClientEnabledFeatures</span></span>|[<span data-ttu-id="7da02-256">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="7da02-256">configurationManagerClientEnabledFeatures</span></span>](../resources/intune-devices-configurationmanagerclientenabledfeatures.md)|<span data-ttu-id="7da02-257">Características activadas del cliente ConfigrMgr.</span><span class="sxs-lookup"><span data-stu-id="7da02-257">ConfigrMgr client enabled features</span></span>|
|<span data-ttu-id="7da02-258">wiFiMacAddress</span><span class="sxs-lookup"><span data-stu-id="7da02-258">wiFiMacAddress</span></span>|<span data-ttu-id="7da02-259">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-259">String</span></span>|<span data-ttu-id="7da02-260">MAC de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="7da02-260">Wi-Fi MAC</span></span>|
|<span data-ttu-id="7da02-261">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="7da02-261">deviceHealthAttestationState</span></span>|[<span data-ttu-id="7da02-262">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="7da02-262">deviceHealthAttestationState</span></span>](../resources/intune-devices-devicehealthattestationstate.md)|<span data-ttu-id="7da02-263">Estado de la atestación de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-263">The device health attestation state.</span></span>|
|<span data-ttu-id="7da02-264">subscriberCarrier</span><span class="sxs-lookup"><span data-stu-id="7da02-264">subscriberCarrier</span></span>|<span data-ttu-id="7da02-265">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-265">String</span></span>|<span data-ttu-id="7da02-266">Operador del suscriptor.</span><span class="sxs-lookup"><span data-stu-id="7da02-266">Subscriber Carrier</span></span>|
|<span data-ttu-id="7da02-267">meid</span><span class="sxs-lookup"><span data-stu-id="7da02-267">meid</span></span>|<span data-ttu-id="7da02-268">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-268">String</span></span>|<span data-ttu-id="7da02-269">MEID</span><span class="sxs-lookup"><span data-stu-id="7da02-269">MEID</span></span>|
|<span data-ttu-id="7da02-270">totalStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="7da02-270">totalStorageSpaceInBytes</span></span>|<span data-ttu-id="7da02-271">Int64</span><span class="sxs-lookup"><span data-stu-id="7da02-271">Int64</span></span>|<span data-ttu-id="7da02-272">Almacenamiento total en bytes.</span><span class="sxs-lookup"><span data-stu-id="7da02-272">Total Storage in Bytes</span></span>|
|<span data-ttu-id="7da02-273">freeStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="7da02-273">freeStorageSpaceInBytes</span></span>|<span data-ttu-id="7da02-274">Int64</span><span class="sxs-lookup"><span data-stu-id="7da02-274">Int64</span></span>|<span data-ttu-id="7da02-275">Almacenamiento disponible en bytes.</span><span class="sxs-lookup"><span data-stu-id="7da02-275">Free Storage in Bytes</span></span>|
|<span data-ttu-id="7da02-276">managedDeviceName</span><span class="sxs-lookup"><span data-stu-id="7da02-276">managedDeviceName</span></span>|<span data-ttu-id="7da02-277">Cadena</span><span class="sxs-lookup"><span data-stu-id="7da02-277">String</span></span>|<span data-ttu-id="7da02-278">Nombre generado automáticamente para identificar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7da02-278">Automatically generated name to identify a device.</span></span> <span data-ttu-id="7da02-279">Se puede sobrescribir con un nombre descriptivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="7da02-279">Can be overwritten to a user friendly name.</span></span>|
|<span data-ttu-id="7da02-280">partnerReportedThreatState</span><span class="sxs-lookup"><span data-stu-id="7da02-280">partnerReportedThreatState</span></span>|[<span data-ttu-id="7da02-281">managedDevicePartnerReportedHealthState</span><span class="sxs-lookup"><span data-stu-id="7da02-281">managedDevicePartnerReportedHealthState</span></span>](../resources/intune-devices-manageddevicepartnerreportedhealthstate.md)|<span data-ttu-id="7da02-282">Indica el estado de amenazas de un dispositivo cuando la cuenta y el dispositivo usan un partner de Mobile Threat Defense.</span><span class="sxs-lookup"><span data-stu-id="7da02-282">Indicates the threat state of a device when a Mobile Threat Defense partner is in use by the account and device.</span></span> <span data-ttu-id="7da02-283">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="7da02-283">Read Only.</span></span> <span data-ttu-id="7da02-284">Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised` y `misconfigured`.</span><span class="sxs-lookup"><span data-stu-id="7da02-284">Possible values are: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised`, `misconfigured`.</span></span>|



## <a name="response"></a><span data-ttu-id="7da02-285">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7da02-285">Response</span></span>
<span data-ttu-id="7da02-286">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDevice](../resources/intune-devices-manageddevice.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7da02-286">If successful, this method returns a `200 OK` response code and an updated [managedDevice](../resources/intune-devices-manageddevice.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7da02-287">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7da02-287">Example</span></span>
### <a name="request"></a><span data-ttu-id="7da02-288">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7da02-288">Request</span></span>
<span data-ttu-id="7da02-289">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7da02-289">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/users/{usersId}/managedDevices/{managedDeviceId}
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

### <a name="response"></a><span data-ttu-id="7da02-290">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7da02-290">Response</span></span>
<span data-ttu-id="7da02-p113">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7da02-p113">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



