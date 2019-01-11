---
title: Crear windowsManagedDevice
description: Crear un nuevo objeto windowsManagedDevice.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e23b24365d30954c4da1597ca9d7c14c554a73ae
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27842661"
---
# <a name="create-windowsmanageddevice"></a><span data-ttu-id="dbf7e-103">Crear windowsManagedDevice</span><span class="sxs-lookup"><span data-stu-id="dbf7e-103">Create windowsManagedDevice</span></span>

> <span data-ttu-id="dbf7e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dbf7e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="dbf7e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="dbf7e-107">Crear un nuevo objeto [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) .</span><span class="sxs-lookup"><span data-stu-id="dbf7e-107">Create a new [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="dbf7e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="dbf7e-108">Prerequisites</span></span>
<span data-ttu-id="dbf7e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dbf7e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dbf7e-111">Permission type</span></span>|<span data-ttu-id="dbf7e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="dbf7e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="dbf7e-114">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dbf7e-114">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="dbf7e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="dbf7e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-116">Not supported.</span></span>|
|<span data-ttu-id="dbf7e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dbf7e-117">Application</span></span>|<span data-ttu-id="dbf7e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="dbf7e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dbf7e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /users/{usersId}/managedDevices
POST /deviceManagement/managedDevices
POST /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/detectedApps/{detectedAppId}/managedDevices
```

## <a name="request-headers"></a><span data-ttu-id="dbf7e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dbf7e-120">Request headers</span></span>
|<span data-ttu-id="dbf7e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dbf7e-121">Header</span></span>|<span data-ttu-id="dbf7e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="dbf7e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="dbf7e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="dbf7e-123">Authorization</span></span>|<span data-ttu-id="dbf7e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="dbf7e-125">Accept</span><span class="sxs-lookup"><span data-stu-id="dbf7e-125">Accept</span></span>|<span data-ttu-id="dbf7e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="dbf7e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="dbf7e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dbf7e-127">Request body</span></span>
<span data-ttu-id="dbf7e-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto windowsManagedDevice.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-128">In the request body, supply a JSON representation for the windowsManagedDevice object.</span></span>

<span data-ttu-id="dbf7e-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el windowsManagedDevice.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-129">The following table shows the properties that are required when you create the windowsManagedDevice.</span></span>

|<span data-ttu-id="dbf7e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dbf7e-130">Property</span></span>|<span data-ttu-id="dbf7e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="dbf7e-131">Type</span></span>|<span data-ttu-id="dbf7e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbf7e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="dbf7e-133">id</span><span class="sxs-lookup"><span data-stu-id="dbf7e-133">id</span></span>|<span data-ttu-id="dbf7e-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-134">String</span></span>|<span data-ttu-id="dbf7e-135">Identificador único para el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-135">Unique Identifier for the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-136">userId</span><span class="sxs-lookup"><span data-stu-id="dbf7e-136">userId</span></span>|<span data-ttu-id="dbf7e-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-137">String</span></span>|<span data-ttu-id="dbf7e-138">Identificador único para el usuario asociado con el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-138">Unique Identifier for the user associated with the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-139">deviceName</span><span class="sxs-lookup"><span data-stu-id="dbf7e-139">deviceName</span></span>|<span data-ttu-id="dbf7e-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-140">String</span></span>|<span data-ttu-id="dbf7e-141">Nombre del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-141">Name of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-142">hardwareInformation</span><span class="sxs-lookup"><span data-stu-id="dbf7e-142">hardwareInformation</span></span>|[<span data-ttu-id="dbf7e-143">hardwareInformation</span><span class="sxs-lookup"><span data-stu-id="dbf7e-143">hardwareInformation</span></span>](../resources/intune-devices-hardwareinformation.md)|<span data-ttu-id="dbf7e-144">Los detalles de hardward para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-144">The hardward details for the device.</span></span>  <span data-ttu-id="dbf7e-145">Incluye información como el espacio de almacenamiento, el fabricante, el número de serie, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-145">Includes information such as storage space, manufacturer, serial number, etc. Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-146">ownerType</span><span class="sxs-lookup"><span data-stu-id="dbf7e-146">ownerType</span></span>|[<span data-ttu-id="dbf7e-147">ownerType</span><span class="sxs-lookup"><span data-stu-id="dbf7e-147">ownerType</span></span>](../resources/intune-devices-ownertype.md)|<span data-ttu-id="dbf7e-148">Propietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-148">Ownership of the device.</span></span> <span data-ttu-id="dbf7e-149">Puede ser 'compañía' o 'personal' heredado de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-149">Can be 'company' or 'personal' Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-150">Los valores posibles son: `unknown`, `company` y `personal`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-150">Possible values are: `unknown`, `company`, `personal`.</span></span>|
|<span data-ttu-id="dbf7e-151">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="dbf7e-151">managedDeviceOwnerType</span></span>|[<span data-ttu-id="dbf7e-152">managedDeviceOwnerType</span><span class="sxs-lookup"><span data-stu-id="dbf7e-152">managedDeviceOwnerType</span></span>](../resources/intune-devices-manageddeviceownertype.md)|<span data-ttu-id="dbf7e-153">Propietario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-153">Ownership of the device.</span></span> <span data-ttu-id="dbf7e-154">Puede ser 'compañía' o 'personal' heredado de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-154">Can be 'company' or 'personal' Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-155">Los valores posibles son: `unknown`, `company` y `personal`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-155">Possible values are: `unknown`, `company`, `personal`.</span></span>|
|<span data-ttu-id="dbf7e-156">deviceActionResults</span><span class="sxs-lookup"><span data-stu-id="dbf7e-156">deviceActionResults</span></span>|<span data-ttu-id="dbf7e-157">Colección [deviceActionResult](../resources/intune-devices-deviceactionresult.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-157">[deviceActionResult](../resources/intune-devices-deviceactionresult.md) collection</span></span>|<span data-ttu-id="dbf7e-158">Lista de objetos deviceActionResult ComplexType.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-158">List of ComplexType deviceActionResult objects.</span></span> <span data-ttu-id="dbf7e-159">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-159">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-160">managementState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-160">managementState</span></span>|[<span data-ttu-id="dbf7e-161">managementState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-161">managementState</span></span>](../resources/intune-devices-managementstate.md)|<span data-ttu-id="dbf7e-162">Estado de administración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-162">Management state of the device.</span></span> <span data-ttu-id="dbf7e-163">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-163">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-164">Los valores posibles son: `managed`, `retirePending`, `retireFailed`, `wipePending`, `wipeFailed`, `unhealthy`, `deletePending`, `retireIssued`, `wipeIssued`, `wipeCanceled`, `retireCanceled` y `discovered`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-164">Possible values are: `managed`, `retirePending`, `retireFailed`, `wipePending`, `wipeFailed`, `unhealthy`, `deletePending`, `retireIssued`, `wipeIssued`, `wipeCanceled`, `retireCanceled`, `discovered`.</span></span>|
|<span data-ttu-id="dbf7e-165">enrolledDateTime</span><span class="sxs-lookup"><span data-stu-id="dbf7e-165">enrolledDateTime</span></span>|<span data-ttu-id="dbf7e-166">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dbf7e-166">DateTimeOffset</span></span>|<span data-ttu-id="dbf7e-167">Hora de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-167">Enrollment time of the device.</span></span> <span data-ttu-id="dbf7e-168">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-168">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-169">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="dbf7e-169">lastSyncDateTime</span></span>|<span data-ttu-id="dbf7e-170">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dbf7e-170">DateTimeOffset</span></span>|<span data-ttu-id="dbf7e-171">Fecha y hora en que el dispositivo completó por última vez una sincronización correcta con Intune.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-171">The date and time that the device last completed a successful sync with Intune.</span></span> <span data-ttu-id="dbf7e-172">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-172">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-173">chassisType</span><span class="sxs-lookup"><span data-stu-id="dbf7e-173">chassisType</span></span>|[<span data-ttu-id="dbf7e-174">chassisType</span><span class="sxs-lookup"><span data-stu-id="dbf7e-174">chassisType</span></span>](../resources/intune-devices-chassistype.md)|<span data-ttu-id="dbf7e-175">Tipo de chasis del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-175">Chassis type of the device.</span></span> <span data-ttu-id="dbf7e-176">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-176">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-177">Los valores posibles son: `unknown`, `desktop`, `laptop`, `worksWorkstation`, `enterpriseServer`, `phone`, `tablet`, `mobileOther` y `mobileUnknown`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-177">Possible values are: `unknown`, `desktop`, `laptop`, `worksWorkstation`, `enterpriseServer`, `phone`, `tablet`, `mobileOther`, `mobileUnknown`.</span></span>|
|<span data-ttu-id="dbf7e-178">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="dbf7e-178">operatingSystem</span></span>|<span data-ttu-id="dbf7e-179">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-179">String</span></span>|<span data-ttu-id="dbf7e-180">Sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-180">Operating system of the device.</span></span> <span data-ttu-id="dbf7e-181">Windows, iOS, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-181">Windows, iOS, etc. Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-182">deviceType</span><span class="sxs-lookup"><span data-stu-id="dbf7e-182">deviceType</span></span>|[<span data-ttu-id="dbf7e-183">deviceType</span><span class="sxs-lookup"><span data-stu-id="dbf7e-183">deviceType</span></span>](../resources/intune-shared-devicetype.md)|<span data-ttu-id="dbf7e-184">Plataforma del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-184">Platform of the device.</span></span> <span data-ttu-id="dbf7e-185">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-185">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-186">Los valores posibles son: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise` , `blackberry`, `palm`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-186">Possible values are: `desktop`, `windowsRT`, `winMO6`, `nokia`, `windowsPhone`, `mac`, `winCE`, `winEmbedded`, `iPhone`, `iPad`, `iPod`, `android`, `iSocConsumer`, `unix`, `macMDM`, `holoLens`, `surfaceHub`, `androidForWork`, `androidEnterprise`, `blackberry`, `palm`, `unknown`.</span></span>|
|<span data-ttu-id="dbf7e-187">complianceState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-187">complianceState</span></span>|[<span data-ttu-id="dbf7e-188">complianceState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-188">complianceState</span></span>](../resources/intune-devices-compliancestate.md)|<span data-ttu-id="dbf7e-189">Estado de cumplimiento del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-189">Compliance state of the device.</span></span> <span data-ttu-id="dbf7e-190">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-190">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-191">Los valores posibles son: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod` y `configManager`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-191">Possible values are: `unknown`, `compliant`, `noncompliant`, `conflict`, `error`, `inGracePeriod`, `configManager`.</span></span>|
|<span data-ttu-id="dbf7e-192">jailBroken</span><span class="sxs-lookup"><span data-stu-id="dbf7e-192">jailBroken</span></span>|<span data-ttu-id="dbf7e-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-193">String</span></span>|<span data-ttu-id="dbf7e-194">Indica si se trata de un dispositivo liberado o con permisos elevados.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-194">whether the device is jail broken or rooted.</span></span> <span data-ttu-id="dbf7e-195">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-195">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-196">managementAgent</span><span class="sxs-lookup"><span data-stu-id="dbf7e-196">managementAgent</span></span>|[<span data-ttu-id="dbf7e-197">managementAgentType</span><span class="sxs-lookup"><span data-stu-id="dbf7e-197">managementAgentType</span></span>](../resources/intune-devices-managementagenttype.md)|<span data-ttu-id="dbf7e-198">Canal de administración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-198">Management channel of the device.</span></span> <span data-ttu-id="dbf7e-199">Intune, EAS, etcetera. Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-199">Intune, EAS, etc. Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-200">Los valores posibles son: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController` y `microsoft365ManagedMdm`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-200">Possible values are: `eas`, `mdm`, `easMdm`, `intuneClient`, `easIntuneClient`, `configurationManagerClient`, `configurationManagerClientMdm`, `configurationManagerClientMdmEas`, `unknown`, `jamf`, `googleCloudDevicePolicyController`, `microsoft365ManagedMdm`.</span></span>|
|<span data-ttu-id="dbf7e-201">osVersion</span><span class="sxs-lookup"><span data-stu-id="dbf7e-201">osVersion</span></span>|<span data-ttu-id="dbf7e-202">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-202">String</span></span>|<span data-ttu-id="dbf7e-203">Versión del sistema operativo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-203">Operating system version of the device.</span></span> <span data-ttu-id="dbf7e-204">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-204">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-205">easActivated</span><span class="sxs-lookup"><span data-stu-id="dbf7e-205">easActivated</span></span>|<span data-ttu-id="dbf7e-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="dbf7e-206">Boolean</span></span>|<span data-ttu-id="dbf7e-207">Indica si el dispositivo tiene Exchange ActiveSync activado.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-207">Whether the device is Exchange ActiveSync activated.</span></span> <span data-ttu-id="dbf7e-208">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-208">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-209">easDeviceId</span><span class="sxs-lookup"><span data-stu-id="dbf7e-209">easDeviceId</span></span>|<span data-ttu-id="dbf7e-210">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-210">String</span></span>|<span data-ttu-id="dbf7e-211">Identificador de Exchange ActiveSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-211">Exchange ActiveSync Id of the device.</span></span> <span data-ttu-id="dbf7e-212">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-212">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-213">easActivationDateTime</span><span class="sxs-lookup"><span data-stu-id="dbf7e-213">easActivationDateTime</span></span>|<span data-ttu-id="dbf7e-214">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dbf7e-214">DateTimeOffset</span></span>|<span data-ttu-id="dbf7e-215">Hora de activación de Exchange ActivationSync del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-215">Exchange ActivationSync activation time of the device.</span></span> <span data-ttu-id="dbf7e-216">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-216">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-217">aadRegistered</span><span class="sxs-lookup"><span data-stu-id="dbf7e-217">aadRegistered</span></span>|<span data-ttu-id="dbf7e-218">Booleano</span><span class="sxs-lookup"><span data-stu-id="dbf7e-218">Boolean</span></span>|<span data-ttu-id="dbf7e-219">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-219">Whether the device is Azure Active Directory registered.</span></span> <span data-ttu-id="dbf7e-220">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-220">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-221">azureADRegistered</span><span class="sxs-lookup"><span data-stu-id="dbf7e-221">azureADRegistered</span></span>|<span data-ttu-id="dbf7e-222">Booleano</span><span class="sxs-lookup"><span data-stu-id="dbf7e-222">Boolean</span></span>|<span data-ttu-id="dbf7e-223">Indica si el dispositivo está registrado en Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-223">Whether the device is Azure Active Directory registered.</span></span> <span data-ttu-id="dbf7e-224">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-224">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-225">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="dbf7e-225">deviceEnrollmentType</span></span>|[<span data-ttu-id="dbf7e-226">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="dbf7e-226">deviceEnrollmentType</span></span>](../resources/intune-shared-deviceenrollmenttype.md)|<span data-ttu-id="dbf7e-227">Tipo de inscripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-227">Enrollment type of the device.</span></span> <span data-ttu-id="dbf7e-228">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-228">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-229">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-229">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="dbf7e-230">lostModeState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-230">lostModeState</span></span>|[<span data-ttu-id="dbf7e-231">lostModeState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-231">lostModeState</span></span>](../resources/intune-devices-lostmodestate.md)|<span data-ttu-id="dbf7e-232">Indica si el modo pierden está habilitado o deshabilitado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-232">Indicates if Lost mode is enabled or disabled Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-233">Los valores posibles son: `disabled` y `enabled`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-233">Possible values are: `disabled`, `enabled`.</span></span>|
|<span data-ttu-id="dbf7e-234">activationLockBypassCode</span><span class="sxs-lookup"><span data-stu-id="dbf7e-234">activationLockBypassCode</span></span>|<span data-ttu-id="dbf7e-235">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-235">String</span></span>|<span data-ttu-id="dbf7e-236">Código que permite que se omita el bloqueo de activación en un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-236">Code that allows the Activation Lock on a device to be bypassed.</span></span> <span data-ttu-id="dbf7e-237">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-237">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-238">emailAddress</span><span class="sxs-lookup"><span data-stu-id="dbf7e-238">emailAddress</span></span>|<span data-ttu-id="dbf7e-239">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-239">String</span></span>|<span data-ttu-id="dbf7e-240">Email(s) para el usuario asociado con el dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-240">Email(s) for the user associated with the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-241">azureActiveDirectoryDeviceId</span><span class="sxs-lookup"><span data-stu-id="dbf7e-241">azureActiveDirectoryDeviceId</span></span>|<span data-ttu-id="dbf7e-242">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-242">String</span></span>|<span data-ttu-id="dbf7e-243">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-243">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="dbf7e-244">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-244">Read only.</span></span> <span data-ttu-id="dbf7e-245">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-245">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-246">azureADDeviceId</span><span class="sxs-lookup"><span data-stu-id="dbf7e-246">azureADDeviceId</span></span>|<span data-ttu-id="dbf7e-247">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-247">String</span></span>|<span data-ttu-id="dbf7e-248">Identificador único del dispositivo de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-248">The unique identifier for the Azure Active Directory device.</span></span> <span data-ttu-id="dbf7e-249">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-249">Read only.</span></span> <span data-ttu-id="dbf7e-250">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-250">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-251">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-251">deviceRegistrationState</span></span>|[<span data-ttu-id="dbf7e-252">deviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-252">deviceRegistrationState</span></span>](../resources/intune-devices-deviceregistrationstate.md)|<span data-ttu-id="dbf7e-253">Estado de registro del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-253">Device registration state.</span></span> <span data-ttu-id="dbf7e-254">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-254">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-255">Los valores posibles son: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-255">Possible values are: `notRegistered`, `registered`, `revoked`, `keyConflict`, `approvalPending`, `certificateReset`, `notRegisteredPendingEnrollment`, `unknown`.</span></span>|
|<span data-ttu-id="dbf7e-256">deviceCategoryDisplayName</span><span class="sxs-lookup"><span data-stu-id="dbf7e-256">deviceCategoryDisplayName</span></span>|<span data-ttu-id="dbf7e-257">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-257">String</span></span>|<span data-ttu-id="dbf7e-258">Nombre para mostrar categoría dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-258">Device category display name Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-259">isSupervised</span><span class="sxs-lookup"><span data-stu-id="dbf7e-259">isSupervised</span></span>|<span data-ttu-id="dbf7e-260">Booleano</span><span class="sxs-lookup"><span data-stu-id="dbf7e-260">Boolean</span></span>|<span data-ttu-id="dbf7e-261">Estado del dispositivo supervisado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-261">Device supervised status Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-262">exchangeLastSuccessfulSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="dbf7e-262">exchangeLastSuccessfulSyncDateTime</span></span>|<span data-ttu-id="dbf7e-263">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dbf7e-263">DateTimeOffset</span></span>|<span data-ttu-id="dbf7e-264">Última vez que el dispositivo estableció contacto con Exchange.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-264">Last time the device contacted Exchange.</span></span> <span data-ttu-id="dbf7e-265">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-265">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-266">exchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-266">exchangeAccessState</span></span>|[<span data-ttu-id="dbf7e-267">deviceManagementExchangeAccessState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-267">deviceManagementExchangeAccessState</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstate.md)|<span data-ttu-id="dbf7e-268">Estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-268">The Access State of the device in Exchange.</span></span> <span data-ttu-id="dbf7e-269">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-269">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-270">Los valores posibles son: `none`, `unknown`, `allowed`, `blocked` y `quarantined`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-270">Possible values are: `none`, `unknown`, `allowed`, `blocked`, `quarantined`.</span></span>|
|<span data-ttu-id="dbf7e-271">exchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="dbf7e-271">exchangeAccessStateReason</span></span>|[<span data-ttu-id="dbf7e-272">deviceManagementExchangeAccessStateReason</span><span class="sxs-lookup"><span data-stu-id="dbf7e-272">deviceManagementExchangeAccessStateReason</span></span>](../resources/intune-devices-devicemanagementexchangeaccessstatereason.md)|<span data-ttu-id="dbf7e-273">Motivo del estado de acceso del dispositivo en Exchange.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-273">The reason for the device's access state in Exchange.</span></span> <span data-ttu-id="dbf7e-274">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-274">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-275">Los valores posibles son: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword` y `deviceNotKnownWithManagedApp`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-275">Possible values are: `none`, `unknown`, `exchangeGlobalRule`, `exchangeIndividualRule`, `exchangeDeviceRule`, `exchangeUpgrade`, `exchangeMailboxPolicy`, `other`, `compliant`, `notCompliant`, `notEnrolled`, `unknownLocation`, `mfaRequired`, `azureADBlockDueToAccessPolicy`, `compromisedPassword`, `deviceNotKnownWithManagedApp`.</span></span>|
|<span data-ttu-id="dbf7e-276">remoteAssistanceSessionUrl</span><span class="sxs-lookup"><span data-stu-id="dbf7e-276">remoteAssistanceSessionUrl</span></span>|<span data-ttu-id="dbf7e-277">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-277">String</span></span>|<span data-ttu-id="dbf7e-278">Dirección URL que permite que se establezca una sesión remota con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-278">Url that allows a Remote Assistance session to be established with the device.</span></span> <span data-ttu-id="dbf7e-279">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-279">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-280">remoteAssistanceSessionErrorDetails</span><span class="sxs-lookup"><span data-stu-id="dbf7e-280">remoteAssistanceSessionErrorDetails</span></span>|<span data-ttu-id="dbf7e-281">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-281">String</span></span>|<span data-ttu-id="dbf7e-282">Cadena de error que identifica los problemas al crear objetos de la sesión de asistencia remota.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-282">An error string that identifies issues when creating Remote Assistance session objects.</span></span> <span data-ttu-id="dbf7e-283">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-283">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-284">isEncrypted</span><span class="sxs-lookup"><span data-stu-id="dbf7e-284">isEncrypted</span></span>|<span data-ttu-id="dbf7e-285">Booleano</span><span class="sxs-lookup"><span data-stu-id="dbf7e-285">Boolean</span></span>|<span data-ttu-id="dbf7e-286">Estado del dispositivo cifrado Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-286">Device encryption status Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-287">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="dbf7e-287">userPrincipalName</span></span>|<span data-ttu-id="dbf7e-288">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-288">String</span></span>|<span data-ttu-id="dbf7e-289">Dispositivo nombre principal de usuario Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-289">Device user principal name Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-290">model</span><span class="sxs-lookup"><span data-stu-id="dbf7e-290">model</span></span>|<span data-ttu-id="dbf7e-291">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-291">String</span></span>|<span data-ttu-id="dbf7e-292">Modelo del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-292">Model of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-293">manufacturer</span><span class="sxs-lookup"><span data-stu-id="dbf7e-293">manufacturer</span></span>|<span data-ttu-id="dbf7e-294">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-294">String</span></span>|<span data-ttu-id="dbf7e-295">Fabricante del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-295">Manufacturer of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-296">imei</span><span class="sxs-lookup"><span data-stu-id="dbf7e-296">imei</span></span>|<span data-ttu-id="dbf7e-297">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-297">String</span></span>|<span data-ttu-id="dbf7e-298">IMEI se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-298">IMEI Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-299">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="dbf7e-299">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="dbf7e-300">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dbf7e-300">DateTimeOffset</span></span>|<span data-ttu-id="dbf7e-301">La fecha y hora en período de gracia de cumplimiento de normas de dispositivo expira Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-301">The DateTime when device compliance grace period expires Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-302">serialNumber</span><span class="sxs-lookup"><span data-stu-id="dbf7e-302">serialNumber</span></span>|<span data-ttu-id="dbf7e-303">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-303">String</span></span>|<span data-ttu-id="dbf7e-304">SerialNumber heredado de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-304">SerialNumber Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-305">phoneNumber</span><span class="sxs-lookup"><span data-stu-id="dbf7e-305">phoneNumber</span></span>|<span data-ttu-id="dbf7e-306">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-306">String</span></span>|<span data-ttu-id="dbf7e-307">Número de teléfono del dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-307">Phone number of the device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-308">androidSecurityPatchLevel</span><span class="sxs-lookup"><span data-stu-id="dbf7e-308">androidSecurityPatchLevel</span></span>|<span data-ttu-id="dbf7e-309">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-309">String</span></span>|<span data-ttu-id="dbf7e-310">Nivel de revisión de seguridad para Android Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-310">Android security patch level Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-311">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="dbf7e-311">userDisplayName</span></span>|<span data-ttu-id="dbf7e-312">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-312">String</span></span>|<span data-ttu-id="dbf7e-313">Nombre de usuario para mostrar Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-313">User display name Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-314">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="dbf7e-314">configurationManagerClientEnabledFeatures</span></span>|[<span data-ttu-id="dbf7e-315">configurationManagerClientEnabledFeatures</span><span class="sxs-lookup"><span data-stu-id="dbf7e-315">configurationManagerClientEnabledFeatures</span></span>](../resources/intune-devices-configurationmanagerclientenabledfeatures.md)|<span data-ttu-id="dbf7e-316">ConfigrMgr cliente habilitado para las características Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-316">ConfigrMgr client enabled features Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-317">wiFiMacAddress</span><span class="sxs-lookup"><span data-stu-id="dbf7e-317">wiFiMacAddress</span></span>|<span data-ttu-id="dbf7e-318">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-318">String</span></span>|<span data-ttu-id="dbf7e-319">Wi-Fi MAC se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-319">Wi-Fi MAC Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-320">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-320">deviceHealthAttestationState</span></span>|[<span data-ttu-id="dbf7e-321">deviceHealthAttestationState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-321">deviceHealthAttestationState</span></span>](../resources/intune-devices-devicehealthattestationstate.md)|<span data-ttu-id="dbf7e-322">Estado de la atestación de estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-322">The device health attestation state.</span></span> <span data-ttu-id="dbf7e-323">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-323">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-324">subscriberCarrier</span><span class="sxs-lookup"><span data-stu-id="dbf7e-324">subscriberCarrier</span></span>|<span data-ttu-id="dbf7e-325">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-325">String</span></span>|<span data-ttu-id="dbf7e-326">Operador de suscriptor se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-326">Subscriber Carrier Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-327">meid</span><span class="sxs-lookup"><span data-stu-id="dbf7e-327">meid</span></span>|<span data-ttu-id="dbf7e-328">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-328">String</span></span>|<span data-ttu-id="dbf7e-329">MEID se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-329">MEID Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-330">totalStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="dbf7e-330">totalStorageSpaceInBytes</span></span>|<span data-ttu-id="dbf7e-331">Int64</span><span class="sxs-lookup"><span data-stu-id="dbf7e-331">Int64</span></span>|<span data-ttu-id="dbf7e-332">Almacenamiento total en Bytes se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-332">Total Storage in Bytes Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-333">freeStorageSpaceInBytes</span><span class="sxs-lookup"><span data-stu-id="dbf7e-333">freeStorageSpaceInBytes</span></span>|<span data-ttu-id="dbf7e-334">Int64</span><span class="sxs-lookup"><span data-stu-id="dbf7e-334">Int64</span></span>|<span data-ttu-id="dbf7e-335">Espacio de almacenamiento en Bytes se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-335">Free Storage in Bytes Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-336">managedDeviceName</span><span class="sxs-lookup"><span data-stu-id="dbf7e-336">managedDeviceName</span></span>|<span data-ttu-id="dbf7e-337">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-337">String</span></span>|<span data-ttu-id="dbf7e-338">Nombre generado automáticamente para identificar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-338">Automatically generated name to identify a device.</span></span> <span data-ttu-id="dbf7e-339">Se puede sobrescribir con un nombre descriptivo del usuario.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-339">Can be overwritten to a user friendly name.</span></span> <span data-ttu-id="dbf7e-340">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-340">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-341">partnerReportedThreatState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-341">partnerReportedThreatState</span></span>|[<span data-ttu-id="dbf7e-342">managedDevicePartnerReportedHealthState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-342">managedDevicePartnerReportedHealthState</span></span>](../resources/intune-devices-manageddevicepartnerreportedhealthstate.md)|<span data-ttu-id="dbf7e-343">Indica el estado de amenazas de un dispositivo cuando la cuenta y el dispositivo usan un partner de Mobile Threat Defense.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-343">Indicates the threat state of a device when a Mobile Threat Defense partner is in use by the account and device.</span></span> <span data-ttu-id="dbf7e-344">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-344">Read Only.</span></span> <span data-ttu-id="dbf7e-345">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md).</span><span class="sxs-lookup"><span data-stu-id="dbf7e-345">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md).</span></span> <span data-ttu-id="dbf7e-346">Los valores posibles son: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised` y `misconfigured`.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-346">Possible values are: `unknown`, `activated`, `deactivated`, `secured`, `lowSeverity`, `mediumSeverity`, `highSeverity`, `unresponsive`, `compromised`, `misconfigured`.</span></span>|
|<span data-ttu-id="dbf7e-347">usersLoggedOn</span><span class="sxs-lookup"><span data-stu-id="dbf7e-347">usersLoggedOn</span></span>|<span data-ttu-id="dbf7e-348">colección de [loggedOnUser](../resources/intune-devices-loggedonuser.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-348">[loggedOnUser](../resources/intune-devices-loggedonuser.md) collection</span></span>|<span data-ttu-id="dbf7e-349">Indica la última sesión a los usuarios de un dispositivo Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-349">Indicates the last logged on users of a device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-350">preferMdmOverGroupPolicyAppliedDateTime</span><span class="sxs-lookup"><span data-stu-id="dbf7e-350">preferMdmOverGroupPolicyAppliedDateTime</span></span>|<span data-ttu-id="dbf7e-351">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dbf7e-351">DateTimeOffset</span></span>|<span data-ttu-id="dbf7e-352">Informes la fecha y hora de que la configuración de preferMdmOverGroupPolicy se estableció.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-352">Reports the DateTime the preferMdmOverGroupPolicy setting was set.</span></span>  <span data-ttu-id="dbf7e-353">Cuando se establece, la configuración MDM Intune invalidará la configuración de directiva de grupo si hay un conflicto.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-353">When set, the Intune MDM settings will override Group Policy settings if there is a conflict.</span></span> <span data-ttu-id="dbf7e-354">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-354">Read Only.</span></span> <span data-ttu-id="dbf7e-355">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-355">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-356">autopilotEnrolled</span><span class="sxs-lookup"><span data-stu-id="dbf7e-356">autopilotEnrolled</span></span>|<span data-ttu-id="dbf7e-357">Booleano</span><span class="sxs-lookup"><span data-stu-id="dbf7e-357">Boolean</span></span>|<span data-ttu-id="dbf7e-358">Informa de si el dispositivo administrado está inscrito a través de piloto automático.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-358">Reports if the managed device is enrolled via auto-pilot.</span></span> <span data-ttu-id="dbf7e-359">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-359">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-360">requireUserEnrollmentApproval</span><span class="sxs-lookup"><span data-stu-id="dbf7e-360">requireUserEnrollmentApproval</span></span>|<span data-ttu-id="dbf7e-361">Booleano</span><span class="sxs-lookup"><span data-stu-id="dbf7e-361">Boolean</span></span>|<span data-ttu-id="dbf7e-362">Informa de si el dispositivo iOS administrada es inscripción de aprobación del usuario.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-362">Reports if the managed iOS device is user approval enrollment.</span></span> <span data-ttu-id="dbf7e-363">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-363">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-364">managementCertificateExpirationDate</span><span class="sxs-lookup"><span data-stu-id="dbf7e-364">managementCertificateExpirationDate</span></span>|<span data-ttu-id="dbf7e-365">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dbf7e-365">DateTimeOffset</span></span>|<span data-ttu-id="dbf7e-366">Informes de dispositivo administración certificado fecha de caducidad Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-366">Reports device management certificate expiration date Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-367">iccid</span><span class="sxs-lookup"><span data-stu-id="dbf7e-367">iccid</span></span>|<span data-ttu-id="dbf7e-368">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-368">String</span></span>|<span data-ttu-id="dbf7e-369">Identificador de la tarjeta de circuitos integrados, es número de identificación único de la tarjeta SIM A.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-369">Integrated Circuit Card Identifier, it is A SIM card's unique identification number.</span></span> <span data-ttu-id="dbf7e-370">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-370">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-371">UDID</span><span class="sxs-lookup"><span data-stu-id="dbf7e-371">udid</span></span>|<span data-ttu-id="dbf7e-372">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-372">String</span></span>|<span data-ttu-id="dbf7e-373">Identificador único de dispositivo para dispositivos iOS y Mac OS.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-373">Unique Device Identifier for iOS and macOS devices.</span></span> <span data-ttu-id="dbf7e-374">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-374">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-375">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="dbf7e-375">roleScopeTagIds</span></span>|<span data-ttu-id="dbf7e-376">Colección String</span><span class="sxs-lookup"><span data-stu-id="dbf7e-376">String collection</span></span>|<span data-ttu-id="dbf7e-377">Lista de identificadores de etiqueta de ámbito para esta instancia de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-377">List of Scope Tag IDs for this Device instance.</span></span> <span data-ttu-id="dbf7e-378">Se hereda de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-378">Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-379">windowsActiveMalwareCount</span><span class="sxs-lookup"><span data-stu-id="dbf7e-379">windowsActiveMalwareCount</span></span>|<span data-ttu-id="dbf7e-380">Int32</span><span class="sxs-lookup"><span data-stu-id="dbf7e-380">Int32</span></span>|<span data-ttu-id="dbf7e-381">Recuento de malware para este dispositivo windows Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-381">Count of active malware for this windows device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-382">windowsRemediatedMalwareCount</span><span class="sxs-lookup"><span data-stu-id="dbf7e-382">windowsRemediatedMalwareCount</span></span>|<span data-ttu-id="dbf7e-383">Int32</span><span class="sxs-lookup"><span data-stu-id="dbf7e-383">Int32</span></span>|<span data-ttu-id="dbf7e-384">Recuento de malware corregidos con pruebas para este dispositivo windows Inherited desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-384">Count of remediated malware for this windows device Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-385">notas</span><span class="sxs-lookup"><span data-stu-id="dbf7e-385">notes</span></span>|<span data-ttu-id="dbf7e-386">Cadena</span><span class="sxs-lookup"><span data-stu-id="dbf7e-386">String</span></span>|<span data-ttu-id="dbf7e-387">Notas en el dispositivo creado mediante la administración de TI se hereda desde [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-387">Notes on the device created by IT Admin Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|
|<span data-ttu-id="dbf7e-388">configurationManagerClientHealthState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-388">configurationManagerClientHealthState</span></span>|[<span data-ttu-id="dbf7e-389">configurationManagerClientHealthState</span><span class="sxs-lookup"><span data-stu-id="dbf7e-389">configurationManagerClientHealthState</span></span>](../resources/intune-devices-configurationmanagerclienthealthstate.md)|<span data-ttu-id="dbf7e-390">Configuración Administrador cliente estado de mantenimiento, válido sólo para los dispositivos administrados por MDM/ConfigMgr heredado de agente de [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="dbf7e-390">Configuration manager client health state, valid only for devices managed by MDM/ConfigMgr Agent Inherited from [managedDevice](../resources/intune-devices-manageddevice.md)</span></span>|



## <a name="response"></a><span data-ttu-id="dbf7e-391">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbf7e-391">Response</span></span>
<span data-ttu-id="dbf7e-392">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-392">If successful, this method returns a `201 Created` response code and a [windowsManagedDevice](../resources/intune-devices-windowsmanageddevice.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dbf7e-393">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dbf7e-393">Example</span></span>
### <a name="request"></a><span data-ttu-id="dbf7e-394">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dbf7e-394">Request</span></span>
<span data-ttu-id="dbf7e-395">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-395">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="dbf7e-396">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dbf7e-396">Response</span></span>
<span data-ttu-id="dbf7e-p142">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="dbf7e-p142">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





