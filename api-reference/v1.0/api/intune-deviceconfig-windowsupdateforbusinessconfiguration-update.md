---
title: Actualizar windowsUpdateForBusinessConfiguration
description: Actualice las propiedades de un objeto windowsUpdateForBusinessConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d02bbb949e25d587e267130d5f3ebd110a626534
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27931282"
---
# <a name="update-windowsupdateforbusinessconfiguration"></a><span data-ttu-id="1505c-103">Actualizar windowsUpdateForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="1505c-103">Update windowsUpdateForBusinessConfiguration</span></span>

> <span data-ttu-id="1505c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1505c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1505c-105">Actualice las propiedades de un objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1505c-105">Update the properties of a [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1505c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1505c-106">Prerequisites</span></span>
<span data-ttu-id="1505c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="1505c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="1505c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1505c-109">Permission type</span></span>|<span data-ttu-id="1505c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1505c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1505c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1505c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1505c-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1505c-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="1505c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1505c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1505c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1505c-114">Not supported.</span></span>|
|<span data-ttu-id="1505c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1505c-115">Application</span></span>|<span data-ttu-id="1505c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1505c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1505c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1505c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="1505c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1505c-118">Request headers</span></span>
|<span data-ttu-id="1505c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1505c-119">Header</span></span>|<span data-ttu-id="1505c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1505c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1505c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="1505c-121">Authorization</span></span>|<span data-ttu-id="1505c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1505c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1505c-123">Accept</span><span class="sxs-lookup"><span data-stu-id="1505c-123">Accept</span></span>|<span data-ttu-id="1505c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1505c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1505c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1505c-125">Request body</span></span>
<span data-ttu-id="1505c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1505c-126">In the request body, supply a JSON representation for the [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object.</span></span>

<span data-ttu-id="1505c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1505c-127">The following table shows the properties that are required when you create the [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span></span>

|<span data-ttu-id="1505c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1505c-128">Property</span></span>|<span data-ttu-id="1505c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="1505c-129">Type</span></span>|<span data-ttu-id="1505c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="1505c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1505c-131">id</span><span class="sxs-lookup"><span data-stu-id="1505c-131">id</span></span>|<span data-ttu-id="1505c-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="1505c-132">String</span></span>|<span data-ttu-id="1505c-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1505c-133">Key of the entity.</span></span> <span data-ttu-id="1505c-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1505c-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1505c-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1505c-135">lastModifiedDateTime</span></span>|<span data-ttu-id="1505c-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1505c-136">DateTimeOffset</span></span>|<span data-ttu-id="1505c-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="1505c-137">DateTime the object was last modified.</span></span> <span data-ttu-id="1505c-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1505c-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1505c-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1505c-139">createdDateTime</span></span>|<span data-ttu-id="1505c-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1505c-140">DateTimeOffset</span></span>|<span data-ttu-id="1505c-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="1505c-141">DateTime the object was created.</span></span> <span data-ttu-id="1505c-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1505c-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1505c-143">descripción</span><span class="sxs-lookup"><span data-stu-id="1505c-143">description</span></span>|<span data-ttu-id="1505c-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="1505c-144">String</span></span>|<span data-ttu-id="1505c-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1505c-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="1505c-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1505c-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1505c-147">displayName</span><span class="sxs-lookup"><span data-stu-id="1505c-147">displayName</span></span>|<span data-ttu-id="1505c-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="1505c-148">String</span></span>|<span data-ttu-id="1505c-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1505c-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="1505c-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1505c-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1505c-151">version</span><span class="sxs-lookup"><span data-stu-id="1505c-151">version</span></span>|<span data-ttu-id="1505c-152">Int32</span><span class="sxs-lookup"><span data-stu-id="1505c-152">Int32</span></span>|<span data-ttu-id="1505c-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1505c-153">Version of the device configuration.</span></span> <span data-ttu-id="1505c-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1505c-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1505c-155">deliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="1505c-155">deliveryOptimizationMode</span></span>|[<span data-ttu-id="1505c-156">windowsDeliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="1505c-156">windowsDeliveryOptimizationMode</span></span>](../resources/intune-deviceconfig-windowsdeliveryoptimizationmode.md)|<span data-ttu-id="1505c-157">Modo de optimización de la entrega.</span><span class="sxs-lookup"><span data-stu-id="1505c-157">Delivery Optimization Mode.</span></span> <span data-ttu-id="1505c-158">Los valores posibles son: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload` y `bypassMode`.</span><span class="sxs-lookup"><span data-stu-id="1505c-158">Possible values are: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload`, `bypassMode`.</span></span>|
|<span data-ttu-id="1505c-159">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="1505c-159">prereleaseFeatures</span></span>|[<span data-ttu-id="1505c-160">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="1505c-160">prereleaseFeatures</span></span>](../resources/intune-deviceconfig-prereleasefeatures.md)|<span data-ttu-id="1505c-161">Características de la versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="1505c-161">The pre-release features.</span></span> <span data-ttu-id="1505c-162">Los valores posibles son: `userDefined`, `settingsOnly`, `settingsAndExperimentations` y `notAllowed`.</span><span class="sxs-lookup"><span data-stu-id="1505c-162">Possible values are: `userDefined`, `settingsOnly`, `settingsAndExperimentations`, `notAllowed`.</span></span>|
|<span data-ttu-id="1505c-163">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="1505c-163">automaticUpdateMode</span></span>|[<span data-ttu-id="1505c-164">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="1505c-164">automaticUpdateMode</span></span>](../resources/intune-deviceconfig-automaticupdatemode.md)|<span data-ttu-id="1505c-165">Modo de actualización automático.</span><span class="sxs-lookup"><span data-stu-id="1505c-165">Automatic update mode.</span></span> <span data-ttu-id="1505c-166">Los valores posibles son: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime` y `autoInstallAndRebootWithoutEndUserControl`.</span><span class="sxs-lookup"><span data-stu-id="1505c-166">Possible values are: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime`, `autoInstallAndRebootWithoutEndUserControl`.</span></span>|
|<span data-ttu-id="1505c-167">microsoftUpdateServiceAllowed</span><span class="sxs-lookup"><span data-stu-id="1505c-167">microsoftUpdateServiceAllowed</span></span>|<span data-ttu-id="1505c-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="1505c-168">Boolean</span></span>|<span data-ttu-id="1505c-169">Permitir el servicio de Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="1505c-169">Allow Microsoft Update Service</span></span>|
|<span data-ttu-id="1505c-170">driversExcluded</span><span class="sxs-lookup"><span data-stu-id="1505c-170">driversExcluded</span></span>|<span data-ttu-id="1505c-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="1505c-171">Boolean</span></span>|<span data-ttu-id="1505c-172">Excluir controladores de Windows Update</span><span class="sxs-lookup"><span data-stu-id="1505c-172">Exclude Windows update Drivers</span></span>|
|<span data-ttu-id="1505c-173">installationSchedule</span><span class="sxs-lookup"><span data-stu-id="1505c-173">installationSchedule</span></span>|[<span data-ttu-id="1505c-174">windowsUpdateInstallScheduleType</span><span class="sxs-lookup"><span data-stu-id="1505c-174">windowsUpdateInstallScheduleType</span></span>](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)|<span data-ttu-id="1505c-175">Programación de instalación</span><span class="sxs-lookup"><span data-stu-id="1505c-175">Installation schedule</span></span>|
|<span data-ttu-id="1505c-176">qualityUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1505c-176">qualityUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="1505c-177">Int32</span><span class="sxs-lookup"><span data-stu-id="1505c-177">Int32</span></span>|<span data-ttu-id="1505c-178">Aplazar actualizaciones de calidad el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="1505c-178">Defer Quality Updates by these many days</span></span>|
|<span data-ttu-id="1505c-179">featureUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1505c-179">featureUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="1505c-180">Int32</span><span class="sxs-lookup"><span data-stu-id="1505c-180">Int32</span></span>|<span data-ttu-id="1505c-181">Aplazar actualizaciones de características el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="1505c-181">Defer Feature Updates by these many days</span></span>|
|<span data-ttu-id="1505c-182">qualityUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="1505c-182">qualityUpdatesPaused</span></span>|<span data-ttu-id="1505c-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="1505c-183">Boolean</span></span>|<span data-ttu-id="1505c-184">Pausar las actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="1505c-184">Pause Quality Updates</span></span>|
|<span data-ttu-id="1505c-185">featureUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="1505c-185">featureUpdatesPaused</span></span>|<span data-ttu-id="1505c-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="1505c-186">Boolean</span></span>|<span data-ttu-id="1505c-187">Pausar las actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="1505c-187">Pause Feature Updates</span></span>|
|<span data-ttu-id="1505c-188">qualityUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="1505c-188">qualityUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="1505c-189">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1505c-189">DateTimeOffset</span></span>|<span data-ttu-id="1505c-190">Quality Updates Pause Expiry datetime</span><span class="sxs-lookup"><span data-stu-id="1505c-190">Quality Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="1505c-191">featureUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="1505c-191">featureUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="1505c-192">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1505c-192">DateTimeOffset</span></span>|<span data-ttu-id="1505c-193">Fecha y hora de expiración del pausado de actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="1505c-193">Feature Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="1505c-194">businessReadyUpdatesOnly</span><span class="sxs-lookup"><span data-stu-id="1505c-194">businessReadyUpdatesOnly</span></span>|[<span data-ttu-id="1505c-195">windowsUpdateType</span><span class="sxs-lookup"><span data-stu-id="1505c-195">windowsUpdateType</span></span>](../resources/intune-deviceconfig-windowsupdatetype.md)|<span data-ttu-id="1505c-196">Determina qué dispositivos de sucursal recibirá sus actualizaciones desde.</span><span class="sxs-lookup"><span data-stu-id="1505c-196">Determines which branch devices will receive their updates from.</span></span> <span data-ttu-id="1505c-197">Los valores posibles son: `userDefined`, `all`, `businessReadyOnly`, `windowsInsiderBuildFast`, `windowsInsiderBuildSlow`, `windowsInsiderBuildRelease`.</span><span class="sxs-lookup"><span data-stu-id="1505c-197">Possible values are: `userDefined`, `all`, `businessReadyOnly`, `windowsInsiderBuildFast`, `windowsInsiderBuildSlow`, `windowsInsiderBuildRelease`.</span></span>|



## <a name="response"></a><span data-ttu-id="1505c-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1505c-198">Response</span></span>
<span data-ttu-id="1505c-199">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1505c-199">If successful, this method returns a `200 OK` response code and an updated [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1505c-200">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1505c-200">Example</span></span>
### <a name="request"></a><span data-ttu-id="1505c-201">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1505c-201">Request</span></span>
<span data-ttu-id="1505c-202">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1505c-202">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="1505c-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1505c-203">Response</span></span>
<span data-ttu-id="1505c-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1505c-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



