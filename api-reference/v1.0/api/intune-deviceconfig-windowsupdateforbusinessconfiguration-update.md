---
title: Actualizar windowsUpdateForBusinessConfiguration
description: Actualice las propiedades de un objeto windowsUpdateForBusinessConfiguration.
ms.openlocfilehash: 17538d2fb06af92e8b8f5ec63a023d6fe2c0bdbd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032322"
---
# <a name="update-windowsupdateforbusinessconfiguration"></a><span data-ttu-id="9dba3-103">Actualizar windowsUpdateForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="9dba3-103">Update windowsUpdateForBusinessConfiguration</span></span>

> <span data-ttu-id="9dba3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9dba3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9dba3-105">Actualice las propiedades de un objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="9dba3-105">Update the properties of a [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9dba3-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9dba3-106">Prerequisites</span></span>
<span data-ttu-id="9dba3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9dba3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9dba3-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9dba3-109">Permission type</span></span>|<span data-ttu-id="9dba3-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9dba3-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9dba3-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9dba3-111">Delegated (work or school account)</span></span>|<span data-ttu-id="9dba3-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9dba3-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9dba3-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9dba3-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9dba3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9dba3-114">Not supported.</span></span>|
|<span data-ttu-id="9dba3-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9dba3-115">Application</span></span>|<span data-ttu-id="9dba3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9dba3-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9dba3-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9dba3-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="9dba3-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9dba3-118">Request headers</span></span>
|<span data-ttu-id="9dba3-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9dba3-119">Header</span></span>|<span data-ttu-id="9dba3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9dba3-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9dba3-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="9dba3-121">Authorization</span></span>|<span data-ttu-id="9dba3-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9dba3-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9dba3-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9dba3-123">Accept</span></span>|<span data-ttu-id="9dba3-124">application/json</span><span class="sxs-lookup"><span data-stu-id="9dba3-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9dba3-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9dba3-125">Request body</span></span>
<span data-ttu-id="9dba3-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="9dba3-126">In the request body, supply a JSON representation for the [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object.</span></span>

<span data-ttu-id="9dba3-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="9dba3-127">The following table shows the properties that are required when you create the [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span></span>

|<span data-ttu-id="9dba3-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9dba3-128">Property</span></span>|<span data-ttu-id="9dba3-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="9dba3-129">Type</span></span>|<span data-ttu-id="9dba3-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9dba3-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9dba3-131">id</span><span class="sxs-lookup"><span data-stu-id="9dba3-131">id</span></span>|<span data-ttu-id="9dba3-132">String</span><span class="sxs-lookup"><span data-stu-id="9dba3-132">String</span></span>|<span data-ttu-id="9dba3-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9dba3-133">Key of the entity.</span></span> <span data-ttu-id="9dba3-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9dba3-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9dba3-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9dba3-135">lastModifiedDateTime</span></span>|<span data-ttu-id="9dba3-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9dba3-136">DateTimeOffset</span></span>|<span data-ttu-id="9dba3-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="9dba3-137">DateTime the object was last modified.</span></span> <span data-ttu-id="9dba3-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9dba3-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9dba3-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="9dba3-139">createdDateTime</span></span>|<span data-ttu-id="9dba3-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9dba3-140">DateTimeOffset</span></span>|<span data-ttu-id="9dba3-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="9dba3-141">DateTime the object was created.</span></span> <span data-ttu-id="9dba3-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9dba3-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9dba3-143">descripción</span><span class="sxs-lookup"><span data-stu-id="9dba3-143">description</span></span>|<span data-ttu-id="9dba3-144">String</span><span class="sxs-lookup"><span data-stu-id="9dba3-144">String</span></span>|<span data-ttu-id="9dba3-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9dba3-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="9dba3-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9dba3-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9dba3-147">displayName</span><span class="sxs-lookup"><span data-stu-id="9dba3-147">displayName</span></span>|<span data-ttu-id="9dba3-148">String</span><span class="sxs-lookup"><span data-stu-id="9dba3-148">String</span></span>|<span data-ttu-id="9dba3-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9dba3-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="9dba3-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9dba3-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9dba3-151">version</span><span class="sxs-lookup"><span data-stu-id="9dba3-151">version</span></span>|<span data-ttu-id="9dba3-152">Int32</span><span class="sxs-lookup"><span data-stu-id="9dba3-152">Int32</span></span>|<span data-ttu-id="9dba3-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9dba3-153">Version of the device configuration.</span></span> <span data-ttu-id="9dba3-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="9dba3-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="9dba3-155">deliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="9dba3-155">deliveryOptimizationMode</span></span>|[<span data-ttu-id="9dba3-156">windowsDeliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="9dba3-156">windowsDeliveryOptimizationMode</span></span>](../resources/intune-deviceconfig-windowsdeliveryoptimizationmode.md)|<span data-ttu-id="9dba3-157">Modo de optimización de la entrega.</span><span class="sxs-lookup"><span data-stu-id="9dba3-157">Delivery Optimization Mode.</span></span> <span data-ttu-id="9dba3-158">Los valores posibles son: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload` y `bypassMode`.</span><span class="sxs-lookup"><span data-stu-id="9dba3-158">Possible values are: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload`, `bypassMode`.</span></span>|
|<span data-ttu-id="9dba3-159">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="9dba3-159">prereleaseFeatures</span></span>|[<span data-ttu-id="9dba3-160">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="9dba3-160">prereleaseFeatures</span></span>](../resources/intune-deviceconfig-prereleasefeatures.md)|<span data-ttu-id="9dba3-161">Características de la versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="9dba3-161">The pre-release features.</span></span> <span data-ttu-id="9dba3-162">Los valores posibles son: `userDefined`, `settingsOnly`, `settingsAndExperimentations` y `notAllowed`.</span><span class="sxs-lookup"><span data-stu-id="9dba3-162">Possible values are: `userDefined`, `settingsOnly`, `settingsAndExperimentations`, `notAllowed`.</span></span>|
|<span data-ttu-id="9dba3-163">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="9dba3-163">automaticUpdateMode</span></span>|[<span data-ttu-id="9dba3-164">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="9dba3-164">automaticUpdateMode</span></span>](../resources/intune-deviceconfig-automaticupdatemode.md)|<span data-ttu-id="9dba3-165">Modo de actualización automático.</span><span class="sxs-lookup"><span data-stu-id="9dba3-165">Automatic update mode.</span></span> <span data-ttu-id="9dba3-166">Los valores posibles son: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime` y `autoInstallAndRebootWithoutEndUserControl`.</span><span class="sxs-lookup"><span data-stu-id="9dba3-166">Possible values are: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime`, `autoInstallAndRebootWithoutEndUserControl`.</span></span>|
|<span data-ttu-id="9dba3-167">microsoftUpdateServiceAllowed</span><span class="sxs-lookup"><span data-stu-id="9dba3-167">microsoftUpdateServiceAllowed</span></span>|<span data-ttu-id="9dba3-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="9dba3-168">Boolean</span></span>|<span data-ttu-id="9dba3-169">Permitir el servicio de Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="9dba3-169">Allow Microsoft Update Service</span></span>|
|<span data-ttu-id="9dba3-170">driversExcluded</span><span class="sxs-lookup"><span data-stu-id="9dba3-170">driversExcluded</span></span>|<span data-ttu-id="9dba3-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="9dba3-171">Boolean</span></span>|<span data-ttu-id="9dba3-172">Excluir controladores de Windows Update</span><span class="sxs-lookup"><span data-stu-id="9dba3-172">Exclude Windows update Drivers</span></span>|
|<span data-ttu-id="9dba3-173">installationSchedule</span><span class="sxs-lookup"><span data-stu-id="9dba3-173">installationSchedule</span></span>|[<span data-ttu-id="9dba3-174">windowsUpdateInstallScheduleType</span><span class="sxs-lookup"><span data-stu-id="9dba3-174">windowsUpdateInstallScheduleType</span></span>](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)|<span data-ttu-id="9dba3-175">Programación de instalación</span><span class="sxs-lookup"><span data-stu-id="9dba3-175">Installation schedule</span></span>|
|<span data-ttu-id="9dba3-176">qualityUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="9dba3-176">qualityUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="9dba3-177">Int32</span><span class="sxs-lookup"><span data-stu-id="9dba3-177">Int32</span></span>|<span data-ttu-id="9dba3-178">Aplazar actualizaciones de calidad el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="9dba3-178">Defer Quality Updates by these many days</span></span>|
|<span data-ttu-id="9dba3-179">featureUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="9dba3-179">featureUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="9dba3-180">Int32</span><span class="sxs-lookup"><span data-stu-id="9dba3-180">Int32</span></span>|<span data-ttu-id="9dba3-181">Aplazar actualizaciones de características el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="9dba3-181">Defer Feature Updates by these many days</span></span>|
|<span data-ttu-id="9dba3-182">qualityUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="9dba3-182">qualityUpdatesPaused</span></span>|<span data-ttu-id="9dba3-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="9dba3-183">Boolean</span></span>|<span data-ttu-id="9dba3-184">Pausar las actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="9dba3-184">Pause Quality Updates</span></span>|
|<span data-ttu-id="9dba3-185">featureUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="9dba3-185">featureUpdatesPaused</span></span>|<span data-ttu-id="9dba3-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="9dba3-186">Boolean</span></span>|<span data-ttu-id="9dba3-187">Pausar las actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="9dba3-187">Pause Feature Updates</span></span>|
|<span data-ttu-id="9dba3-188">qualityUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="9dba3-188">qualityUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="9dba3-189">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9dba3-189">DateTimeOffset</span></span>|<span data-ttu-id="9dba3-190">Quality Updates Pause Expiry datetime</span><span class="sxs-lookup"><span data-stu-id="9dba3-190">Quality Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="9dba3-191">featureUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="9dba3-191">featureUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="9dba3-192">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9dba3-192">DateTimeOffset</span></span>|<span data-ttu-id="9dba3-193">Fecha y hora de expiración del pausado de actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="9dba3-193">Feature Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="9dba3-194">businessReadyUpdatesOnly</span><span class="sxs-lookup"><span data-stu-id="9dba3-194">businessReadyUpdatesOnly</span></span>|[<span data-ttu-id="9dba3-195">windowsUpdateType</span><span class="sxs-lookup"><span data-stu-id="9dba3-195">windowsUpdateType</span></span>](../resources/intune-deviceconfig-windowsupdatetype.md)|<span data-ttu-id="9dba3-196">Determina qué dispositivos de sucursal recibirá sus actualizaciones desde.</span><span class="sxs-lookup"><span data-stu-id="9dba3-196">Determines which branch devices will receive their updates from.</span></span> <span data-ttu-id="9dba3-197">Los valores posibles son: `userDefined`, `all`, `businessReadyOnly`, `windowsInsiderBuildFast`, `windowsInsiderBuildSlow`, `windowsInsiderBuildRelease`.</span><span class="sxs-lookup"><span data-stu-id="9dba3-197">Possible values are: `userDefined`, `all`, `businessReadyOnly`, `windowsInsiderBuildFast`, `windowsInsiderBuildSlow`, `windowsInsiderBuildRelease`.</span></span>|



## <a name="response"></a><span data-ttu-id="9dba3-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9dba3-198">Response</span></span>
<span data-ttu-id="9dba3-199">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9dba3-199">If successful, this method returns a `200 OK` response code and an updated [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9dba3-200">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9dba3-200">Example</span></span>
### <a name="request"></a><span data-ttu-id="9dba3-201">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9dba3-201">Request</span></span>
<span data-ttu-id="9dba3-202">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9dba3-202">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 910

{
  "@odata.type": "#microsoft.graph.windowsUpdateForBusinessConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "deliveryOptimizationMode": "httpOnly",
  "prereleaseFeatures": "settingsOnly",
  "automaticUpdateMode": "notifyDownload",
  "microsoftUpdateServiceAllowed": true,
  "driversExcluded": true,
  "installationSchedule": {
    "@odata.type": "microsoft.graph.windowsUpdateScheduledInstall",
    "scheduledInstallDay": "everyday",
    "scheduledInstallTime": "11:59:31.3170000"
  },
  "qualityUpdatesDeferralPeriodInDays": 2,
  "featureUpdatesDeferralPeriodInDays": 2,
  "qualityUpdatesPaused": true,
  "featureUpdatesPaused": true,
  "qualityUpdatesPauseExpiryDateTime": "2017-01-01T00:00:22.9594683-08:00",
  "featureUpdatesPauseExpiryDateTime": "2016-12-31T23:58:08.068669-08:00",
  "businessReadyUpdatesOnly": "all"
}
```

### <a name="response"></a><span data-ttu-id="9dba3-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9dba3-203">Response</span></span>
<span data-ttu-id="9dba3-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9dba3-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1082

{
  "@odata.type": "#microsoft.graph.windowsUpdateForBusinessConfiguration",
  "id": "4928dd6a-dd6a-4928-6add-28496add2849",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "deliveryOptimizationMode": "httpOnly",
  "prereleaseFeatures": "settingsOnly",
  "automaticUpdateMode": "notifyDownload",
  "microsoftUpdateServiceAllowed": true,
  "driversExcluded": true,
  "installationSchedule": {
    "@odata.type": "microsoft.graph.windowsUpdateScheduledInstall",
    "scheduledInstallDay": "everyday",
    "scheduledInstallTime": "11:59:31.3170000"
  },
  "qualityUpdatesDeferralPeriodInDays": 2,
  "featureUpdatesDeferralPeriodInDays": 2,
  "qualityUpdatesPaused": true,
  "featureUpdatesPaused": true,
  "qualityUpdatesPauseExpiryDateTime": "2017-01-01T00:00:22.9594683-08:00",
  "featureUpdatesPauseExpiryDateTime": "2016-12-31T23:58:08.068669-08:00",
  "businessReadyUpdatesOnly": "all"
}
```



