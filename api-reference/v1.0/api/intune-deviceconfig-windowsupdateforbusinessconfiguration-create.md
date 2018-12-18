---
title: Crear windowsUpdateForBusinessConfiguration
description: Crear un objeto windowsUpdateForBusinessConfiguration.
author: tfitzmac
ms.openlocfilehash: 4fa7cc29e439d4c160d752869ef2a877ef0a0e4a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315669"
---
# <a name="create-windowsupdateforbusinessconfiguration"></a><span data-ttu-id="73fd1-103">Crear windowsUpdateForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="73fd1-103">Create windowsUpdateForBusinessConfiguration</span></span>

> <span data-ttu-id="73fd1-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="73fd1-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="73fd1-105">Crear un objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="73fd1-105">Create a new [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="73fd1-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="73fd1-106">Prerequisites</span></span>
<span data-ttu-id="73fd1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="73fd1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="73fd1-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="73fd1-109">Permission type</span></span>|<span data-ttu-id="73fd1-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="73fd1-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="73fd1-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="73fd1-111">Delegated (work or school account)</span></span>|<span data-ttu-id="73fd1-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="73fd1-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="73fd1-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="73fd1-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="73fd1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73fd1-114">Not supported.</span></span>|
|<span data-ttu-id="73fd1-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="73fd1-115">Application</span></span>|<span data-ttu-id="73fd1-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73fd1-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="73fd1-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="73fd1-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="73fd1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="73fd1-118">Request headers</span></span>
|<span data-ttu-id="73fd1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73fd1-119">Header</span></span>|<span data-ttu-id="73fd1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="73fd1-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="73fd1-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="73fd1-121">Authorization</span></span>|<span data-ttu-id="73fd1-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="73fd1-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="73fd1-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="73fd1-123">Accept</span></span>|<span data-ttu-id="73fd1-124">application/json</span><span class="sxs-lookup"><span data-stu-id="73fd1-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="73fd1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="73fd1-125">Request body</span></span>
<span data-ttu-id="73fd1-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsUpdateForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="73fd1-126">In the request body, supply a JSON representation for the windowsUpdateForBusinessConfiguration object.</span></span>

<span data-ttu-id="73fd1-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsUpdateForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="73fd1-127">The following table shows the properties that are required when you create the windowsUpdateForBusinessConfiguration.</span></span>

|<span data-ttu-id="73fd1-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="73fd1-128">Property</span></span>|<span data-ttu-id="73fd1-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="73fd1-129">Type</span></span>|<span data-ttu-id="73fd1-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="73fd1-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="73fd1-131">id</span><span class="sxs-lookup"><span data-stu-id="73fd1-131">id</span></span>|<span data-ttu-id="73fd1-132">String</span><span class="sxs-lookup"><span data-stu-id="73fd1-132">String</span></span>|<span data-ttu-id="73fd1-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="73fd1-133">Key of the entity.</span></span> <span data-ttu-id="73fd1-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="73fd1-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="73fd1-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="73fd1-135">lastModifiedDateTime</span></span>|<span data-ttu-id="73fd1-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="73fd1-136">DateTimeOffset</span></span>|<span data-ttu-id="73fd1-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="73fd1-137">DateTime the object was last modified.</span></span> <span data-ttu-id="73fd1-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="73fd1-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="73fd1-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="73fd1-139">createdDateTime</span></span>|<span data-ttu-id="73fd1-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="73fd1-140">DateTimeOffset</span></span>|<span data-ttu-id="73fd1-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="73fd1-141">DateTime the object was created.</span></span> <span data-ttu-id="73fd1-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="73fd1-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="73fd1-143">descripción</span><span class="sxs-lookup"><span data-stu-id="73fd1-143">description</span></span>|<span data-ttu-id="73fd1-144">String</span><span class="sxs-lookup"><span data-stu-id="73fd1-144">String</span></span>|<span data-ttu-id="73fd1-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73fd1-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="73fd1-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="73fd1-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="73fd1-147">displayName</span><span class="sxs-lookup"><span data-stu-id="73fd1-147">displayName</span></span>|<span data-ttu-id="73fd1-148">String</span><span class="sxs-lookup"><span data-stu-id="73fd1-148">String</span></span>|<span data-ttu-id="73fd1-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73fd1-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="73fd1-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="73fd1-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="73fd1-151">version</span><span class="sxs-lookup"><span data-stu-id="73fd1-151">version</span></span>|<span data-ttu-id="73fd1-152">Int32</span><span class="sxs-lookup"><span data-stu-id="73fd1-152">Int32</span></span>|<span data-ttu-id="73fd1-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="73fd1-153">Version of the device configuration.</span></span> <span data-ttu-id="73fd1-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="73fd1-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="73fd1-155">deliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="73fd1-155">deliveryOptimizationMode</span></span>|[<span data-ttu-id="73fd1-156">windowsDeliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="73fd1-156">windowsDeliveryOptimizationMode</span></span>](../resources/intune-deviceconfig-windowsdeliveryoptimizationmode.md)|<span data-ttu-id="73fd1-157">Modo de optimización de la entrega.</span><span class="sxs-lookup"><span data-stu-id="73fd1-157">Delivery Optimization Mode.</span></span> <span data-ttu-id="73fd1-158">Los valores posibles son: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload` y `bypassMode`.</span><span class="sxs-lookup"><span data-stu-id="73fd1-158">Possible values are: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload`, `bypassMode`.</span></span>|
|<span data-ttu-id="73fd1-159">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="73fd1-159">prereleaseFeatures</span></span>|[<span data-ttu-id="73fd1-160">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="73fd1-160">prereleaseFeatures</span></span>](../resources/intune-deviceconfig-prereleasefeatures.md)|<span data-ttu-id="73fd1-161">Características de la versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="73fd1-161">The pre-release features.</span></span> <span data-ttu-id="73fd1-162">Los valores posibles son: `userDefined`, `settingsOnly`, `settingsAndExperimentations` y `notAllowed`.</span><span class="sxs-lookup"><span data-stu-id="73fd1-162">Possible values are: `userDefined`, `settingsOnly`, `settingsAndExperimentations`, `notAllowed`.</span></span>|
|<span data-ttu-id="73fd1-163">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="73fd1-163">automaticUpdateMode</span></span>|[<span data-ttu-id="73fd1-164">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="73fd1-164">automaticUpdateMode</span></span>](../resources/intune-deviceconfig-automaticupdatemode.md)|<span data-ttu-id="73fd1-165">Modo de actualización automático.</span><span class="sxs-lookup"><span data-stu-id="73fd1-165">Automatic update mode.</span></span> <span data-ttu-id="73fd1-166">Los valores posibles son: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime` y `autoInstallAndRebootWithoutEndUserControl`.</span><span class="sxs-lookup"><span data-stu-id="73fd1-166">Possible values are: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime`, `autoInstallAndRebootWithoutEndUserControl`.</span></span>|
|<span data-ttu-id="73fd1-167">microsoftUpdateServiceAllowed</span><span class="sxs-lookup"><span data-stu-id="73fd1-167">microsoftUpdateServiceAllowed</span></span>|<span data-ttu-id="73fd1-168">Boolean</span><span class="sxs-lookup"><span data-stu-id="73fd1-168">Boolean</span></span>|<span data-ttu-id="73fd1-169">Permitir el servicio de Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="73fd1-169">Allow Microsoft Update Service</span></span>|
|<span data-ttu-id="73fd1-170">driversExcluded</span><span class="sxs-lookup"><span data-stu-id="73fd1-170">driversExcluded</span></span>|<span data-ttu-id="73fd1-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="73fd1-171">Boolean</span></span>|<span data-ttu-id="73fd1-172">Excluir controladores de Windows Update</span><span class="sxs-lookup"><span data-stu-id="73fd1-172">Exclude Windows update Drivers</span></span>|
|<span data-ttu-id="73fd1-173">installationSchedule</span><span class="sxs-lookup"><span data-stu-id="73fd1-173">installationSchedule</span></span>|[<span data-ttu-id="73fd1-174">windowsUpdateInstallScheduleType</span><span class="sxs-lookup"><span data-stu-id="73fd1-174">windowsUpdateInstallScheduleType</span></span>](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)|<span data-ttu-id="73fd1-175">Programación de instalación</span><span class="sxs-lookup"><span data-stu-id="73fd1-175">Installation schedule</span></span>|
|<span data-ttu-id="73fd1-176">qualityUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="73fd1-176">qualityUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="73fd1-177">Int32</span><span class="sxs-lookup"><span data-stu-id="73fd1-177">Int32</span></span>|<span data-ttu-id="73fd1-178">Aplazar actualizaciones de calidad el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="73fd1-178">Defer Quality Updates by these many days</span></span>|
|<span data-ttu-id="73fd1-179">featureUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="73fd1-179">featureUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="73fd1-180">Int32</span><span class="sxs-lookup"><span data-stu-id="73fd1-180">Int32</span></span>|<span data-ttu-id="73fd1-181">Aplazar actualizaciones de características el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="73fd1-181">Defer Feature Updates by these many days</span></span>|
|<span data-ttu-id="73fd1-182">qualityUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="73fd1-182">qualityUpdatesPaused</span></span>|<span data-ttu-id="73fd1-183">Boolean</span><span class="sxs-lookup"><span data-stu-id="73fd1-183">Boolean</span></span>|<span data-ttu-id="73fd1-184">Pausar las actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="73fd1-184">Pause Quality Updates</span></span>|
|<span data-ttu-id="73fd1-185">featureUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="73fd1-185">featureUpdatesPaused</span></span>|<span data-ttu-id="73fd1-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="73fd1-186">Boolean</span></span>|<span data-ttu-id="73fd1-187">Pausar las actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="73fd1-187">Pause Feature Updates</span></span>|
|<span data-ttu-id="73fd1-188">qualityUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="73fd1-188">qualityUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="73fd1-189">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="73fd1-189">DateTimeOffset</span></span>|<span data-ttu-id="73fd1-190">Quality Updates Pause Expiry datetime</span><span class="sxs-lookup"><span data-stu-id="73fd1-190">Quality Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="73fd1-191">featureUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="73fd1-191">featureUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="73fd1-192">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="73fd1-192">DateTimeOffset</span></span>|<span data-ttu-id="73fd1-193">Fecha y hora de expiración del pausado de actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="73fd1-193">Feature Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="73fd1-194">businessReadyUpdatesOnly</span><span class="sxs-lookup"><span data-stu-id="73fd1-194">businessReadyUpdatesOnly</span></span>|[<span data-ttu-id="73fd1-195">windowsUpdateType</span><span class="sxs-lookup"><span data-stu-id="73fd1-195">windowsUpdateType</span></span>](../resources/intune-deviceconfig-windowsupdatetype.md)|<span data-ttu-id="73fd1-196">Determina qué dispositivos de sucursal recibirá sus actualizaciones desde.</span><span class="sxs-lookup"><span data-stu-id="73fd1-196">Determines which branch devices will receive their updates from.</span></span> <span data-ttu-id="73fd1-197">Los valores posibles son: `userDefined`, `all`, `businessReadyOnly`, `windowsInsiderBuildFast`, `windowsInsiderBuildSlow`, `windowsInsiderBuildRelease`.</span><span class="sxs-lookup"><span data-stu-id="73fd1-197">Possible values are: `userDefined`, `all`, `businessReadyOnly`, `windowsInsiderBuildFast`, `windowsInsiderBuildSlow`, `windowsInsiderBuildRelease`.</span></span>|



## <a name="response"></a><span data-ttu-id="73fd1-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73fd1-198">Response</span></span>
<span data-ttu-id="73fd1-199">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73fd1-199">If successful, this method returns a `201 Created` response code and a [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="73fd1-200">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="73fd1-200">Example</span></span>
### <a name="request"></a><span data-ttu-id="73fd1-201">Solicitud</span><span class="sxs-lookup"><span data-stu-id="73fd1-201">Request</span></span>
<span data-ttu-id="73fd1-202">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="73fd1-202">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
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

### <a name="response"></a><span data-ttu-id="73fd1-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73fd1-203">Response</span></span>
<span data-ttu-id="73fd1-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="73fd1-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



