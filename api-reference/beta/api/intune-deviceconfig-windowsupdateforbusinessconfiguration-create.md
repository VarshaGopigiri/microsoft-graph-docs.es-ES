---
title: Crear windowsUpdateForBusinessConfiguration
description: Crear un objeto windowsUpdateForBusinessConfiguration.
ms.openlocfilehash: 83213279b959b927be5a6e4b99f92036c83a99b0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086104"
---
# <a name="create-windowsupdateforbusinessconfiguration"></a><span data-ttu-id="06059-103">Crear windowsUpdateForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="06059-103">Create windowsUpdateForBusinessConfiguration</span></span>

> <span data-ttu-id="06059-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="06059-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="06059-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="06059-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="06059-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="06059-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="06059-107">Crear un objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="06059-107">Create a new [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="06059-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="06059-108">Prerequisites</span></span>
<span data-ttu-id="06059-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="06059-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="06059-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="06059-111">Permission type</span></span>|<span data-ttu-id="06059-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="06059-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="06059-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="06059-113">Delegated (work or school account)</span></span>|<span data-ttu-id="06059-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="06059-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="06059-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="06059-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="06059-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06059-116">Not supported.</span></span>|
|<span data-ttu-id="06059-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="06059-117">Application</span></span>|<span data-ttu-id="06059-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="06059-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="06059-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="06059-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="06059-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="06059-120">Request headers</span></span>
|<span data-ttu-id="06059-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06059-121">Header</span></span>|<span data-ttu-id="06059-122">Valor</span><span class="sxs-lookup"><span data-stu-id="06059-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="06059-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="06059-123">Authorization</span></span>|<span data-ttu-id="06059-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="06059-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="06059-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="06059-125">Accept</span></span>|<span data-ttu-id="06059-126">application/json</span><span class="sxs-lookup"><span data-stu-id="06059-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="06059-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="06059-127">Request body</span></span>
<span data-ttu-id="06059-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto windowsUpdateForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="06059-128">In the request body, supply a JSON representation for the windowsUpdateForBusinessConfiguration object.</span></span>

<span data-ttu-id="06059-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto windowsUpdateForBusinessConfiguration.</span><span class="sxs-lookup"><span data-stu-id="06059-129">The following table shows the properties that are required when you create the windowsUpdateForBusinessConfiguration.</span></span>

|<span data-ttu-id="06059-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="06059-130">Property</span></span>|<span data-ttu-id="06059-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="06059-131">Type</span></span>|<span data-ttu-id="06059-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="06059-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="06059-133">id</span><span class="sxs-lookup"><span data-stu-id="06059-133">id</span></span>|<span data-ttu-id="06059-134">String</span><span class="sxs-lookup"><span data-stu-id="06059-134">String</span></span>|<span data-ttu-id="06059-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="06059-135">Key of the entity.</span></span> <span data-ttu-id="06059-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06059-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06059-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="06059-137">lastModifiedDateTime</span></span>|<span data-ttu-id="06059-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="06059-138">DateTimeOffset</span></span>|<span data-ttu-id="06059-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="06059-139">DateTime the object was last modified.</span></span> <span data-ttu-id="06059-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06059-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06059-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="06059-141">roleScopeTagIds</span></span>|<span data-ttu-id="06059-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="06059-142">String collection</span></span>|<span data-ttu-id="06059-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="06059-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="06059-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06059-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06059-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="06059-145">supportsScopeTags</span></span>|<span data-ttu-id="06059-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="06059-146">Boolean</span></span>|<span data-ttu-id="06059-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="06059-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="06059-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="06059-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="06059-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="06059-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="06059-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="06059-150">This property is read-only.</span></span> <span data-ttu-id="06059-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06059-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06059-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="06059-152">createdDateTime</span></span>|<span data-ttu-id="06059-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="06059-153">DateTimeOffset</span></span>|<span data-ttu-id="06059-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="06059-154">DateTime the object was created.</span></span> <span data-ttu-id="06059-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06059-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06059-156">descripción</span><span class="sxs-lookup"><span data-stu-id="06059-156">description</span></span>|<span data-ttu-id="06059-157">String</span><span class="sxs-lookup"><span data-stu-id="06059-157">String</span></span>|<span data-ttu-id="06059-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06059-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="06059-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06059-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06059-160">displayName</span><span class="sxs-lookup"><span data-stu-id="06059-160">displayName</span></span>|<span data-ttu-id="06059-161">String</span><span class="sxs-lookup"><span data-stu-id="06059-161">String</span></span>|<span data-ttu-id="06059-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06059-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="06059-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06059-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06059-164">version</span><span class="sxs-lookup"><span data-stu-id="06059-164">version</span></span>|<span data-ttu-id="06059-165">Int32</span><span class="sxs-lookup"><span data-stu-id="06059-165">Int32</span></span>|<span data-ttu-id="06059-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06059-166">Version of the device configuration.</span></span> <span data-ttu-id="06059-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="06059-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="06059-168">deliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="06059-168">deliveryOptimizationMode</span></span>|[<span data-ttu-id="06059-169">windowsDeliveryOptimizationMode</span><span class="sxs-lookup"><span data-stu-id="06059-169">windowsDeliveryOptimizationMode</span></span>](../resources/intune-deviceconfig-windowsdeliveryoptimizationmode.md)|<span data-ttu-id="06059-170">Modo de optimización de la entrega.</span><span class="sxs-lookup"><span data-stu-id="06059-170">Delivery Optimization Mode.</span></span> <span data-ttu-id="06059-171">Los valores posibles son: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload` y `bypassMode`.</span><span class="sxs-lookup"><span data-stu-id="06059-171">Possible values are: `userDefined`, `httpOnly`, `httpWithPeeringNat`, `httpWithPeeringPrivateGroup`, `httpWithInternetPeering`, `simpleDownload`, `bypassMode`.</span></span>|
|<span data-ttu-id="06059-172">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="06059-172">prereleaseFeatures</span></span>|[<span data-ttu-id="06059-173">prereleaseFeatures</span><span class="sxs-lookup"><span data-stu-id="06059-173">prereleaseFeatures</span></span>](../resources/intune-deviceconfig-prereleasefeatures.md)|<span data-ttu-id="06059-174">Características de la versión preliminar.</span><span class="sxs-lookup"><span data-stu-id="06059-174">The pre-release features.</span></span> <span data-ttu-id="06059-175">Los valores posibles son: `userDefined`, `settingsOnly`, `settingsAndExperimentations` y `notAllowed`.</span><span class="sxs-lookup"><span data-stu-id="06059-175">Possible values are: `userDefined`, `settingsOnly`, `settingsAndExperimentations`, `notAllowed`.</span></span>|
|<span data-ttu-id="06059-176">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="06059-176">automaticUpdateMode</span></span>|[<span data-ttu-id="06059-177">automaticUpdateMode</span><span class="sxs-lookup"><span data-stu-id="06059-177">automaticUpdateMode</span></span>](../resources/intune-deviceconfig-automaticupdatemode.md)|<span data-ttu-id="06059-178">Modo de actualización automático.</span><span class="sxs-lookup"><span data-stu-id="06059-178">Automatic update mode.</span></span> <span data-ttu-id="06059-179">Los valores posibles son: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime` y `autoInstallAndRebootWithoutEndUserControl`.</span><span class="sxs-lookup"><span data-stu-id="06059-179">Possible values are: `userDefined`, `notifyDownload`, `autoInstallAtMaintenanceTime`, `autoInstallAndRebootAtMaintenanceTime`, `autoInstallAndRebootAtScheduledTime`, `autoInstallAndRebootWithoutEndUserControl`.</span></span>|
|<span data-ttu-id="06059-180">microsoftUpdateServiceAllowed</span><span class="sxs-lookup"><span data-stu-id="06059-180">microsoftUpdateServiceAllowed</span></span>|<span data-ttu-id="06059-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="06059-181">Boolean</span></span>|<span data-ttu-id="06059-182">Permitir el servicio de Microsoft Update</span><span class="sxs-lookup"><span data-stu-id="06059-182">Allow Microsoft Update Service</span></span>|
|<span data-ttu-id="06059-183">driversExcluded</span><span class="sxs-lookup"><span data-stu-id="06059-183">driversExcluded</span></span>|<span data-ttu-id="06059-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="06059-184">Boolean</span></span>|<span data-ttu-id="06059-185">Excluir controladores de Windows Update</span><span class="sxs-lookup"><span data-stu-id="06059-185">Exclude Windows update Drivers</span></span>|
|<span data-ttu-id="06059-186">installationSchedule</span><span class="sxs-lookup"><span data-stu-id="06059-186">installationSchedule</span></span>|[<span data-ttu-id="06059-187">windowsUpdateInstallScheduleType</span><span class="sxs-lookup"><span data-stu-id="06059-187">windowsUpdateInstallScheduleType</span></span>](../resources/intune-deviceconfig-windowsupdateinstallscheduletype.md)|<span data-ttu-id="06059-188">Programación de instalación</span><span class="sxs-lookup"><span data-stu-id="06059-188">Installation schedule</span></span>|
|<span data-ttu-id="06059-189">qualityUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="06059-189">qualityUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="06059-190">Int32</span><span class="sxs-lookup"><span data-stu-id="06059-190">Int32</span></span>|<span data-ttu-id="06059-191">Aplazar actualizaciones de calidad el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="06059-191">Defer Quality Updates by these many days</span></span>|
|<span data-ttu-id="06059-192">featureUpdatesDeferralPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="06059-192">featureUpdatesDeferralPeriodInDays</span></span>|<span data-ttu-id="06059-193">Int32</span><span class="sxs-lookup"><span data-stu-id="06059-193">Int32</span></span>|<span data-ttu-id="06059-194">Aplazar actualizaciones de características el siguiente número de días</span><span class="sxs-lookup"><span data-stu-id="06059-194">Defer Feature Updates by these many days</span></span>|
|<span data-ttu-id="06059-195">qualityUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="06059-195">qualityUpdatesPaused</span></span>|<span data-ttu-id="06059-196">Booleano</span><span class="sxs-lookup"><span data-stu-id="06059-196">Boolean</span></span>|<span data-ttu-id="06059-197">Pausar las actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="06059-197">Pause Quality Updates</span></span>|
|<span data-ttu-id="06059-198">featureUpdatesPaused</span><span class="sxs-lookup"><span data-stu-id="06059-198">featureUpdatesPaused</span></span>|<span data-ttu-id="06059-199">Booleano</span><span class="sxs-lookup"><span data-stu-id="06059-199">Boolean</span></span>|<span data-ttu-id="06059-200">Pausar las actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="06059-200">Pause Feature Updates</span></span>|
|<span data-ttu-id="06059-201">qualityUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="06059-201">qualityUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="06059-202">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="06059-202">DateTimeOffset</span></span>|<span data-ttu-id="06059-203">Quality Updates Pause Expiry datetime</span><span class="sxs-lookup"><span data-stu-id="06059-203">Quality Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="06059-204">featureUpdatesPauseExpiryDateTime</span><span class="sxs-lookup"><span data-stu-id="06059-204">featureUpdatesPauseExpiryDateTime</span></span>|<span data-ttu-id="06059-205">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="06059-205">DateTimeOffset</span></span>|<span data-ttu-id="06059-206">Fecha y hora de expiración del pausado de actualizaciones de características</span><span class="sxs-lookup"><span data-stu-id="06059-206">Feature Updates Pause Expiry datetime</span></span>|
|<span data-ttu-id="06059-207">businessReadyUpdatesOnly</span><span class="sxs-lookup"><span data-stu-id="06059-207">businessReadyUpdatesOnly</span></span>|[<span data-ttu-id="06059-208">windowsUpdateType</span><span class="sxs-lookup"><span data-stu-id="06059-208">windowsUpdateType</span></span>](../resources/intune-deviceconfig-windowsupdatetype.md)|<span data-ttu-id="06059-209">Determina qué dispositivos de sucursal recibirá sus actualizaciones desde.</span><span class="sxs-lookup"><span data-stu-id="06059-209">Determines which branch devices will receive their updates from.</span></span> <span data-ttu-id="06059-210">Los valores posibles son: `userDefined`, `all`, `businessReadyOnly`, `windowsInsiderBuildFast`, `windowsInsiderBuildSlow`, `windowsInsiderBuildRelease`.</span><span class="sxs-lookup"><span data-stu-id="06059-210">Possible values are: `userDefined`, `all`, `businessReadyOnly`, `windowsInsiderBuildFast`, `windowsInsiderBuildSlow`, `windowsInsiderBuildRelease`.</span></span>|
|<span data-ttu-id="06059-211">skipChecksBeforeRestart</span><span class="sxs-lookup"><span data-stu-id="06059-211">skipChecksBeforeRestart</span></span>|<span data-ttu-id="06059-212">Booleano</span><span class="sxs-lookup"><span data-stu-id="06059-212">Boolean</span></span>|<span data-ttu-id="06059-213">Establecer omitir la comprobación de todos los antes de reiniciar: nivel de la batería = 40%, la presencia de usuario, es necesario para mostrar, modo de presentación, el modo de pantalla completa, el estado de llamada de teléfono, modo de juego etcetera.</span><span class="sxs-lookup"><span data-stu-id="06059-213">Set to skip all check before restart: Battery level = 40%, User presence, Display Needed, Presentation mode, Full screen mode, phone call state, game mode etc.</span></span> |
|<span data-ttu-id="06059-214">updateWeeks</span><span class="sxs-lookup"><span data-stu-id="06059-214">updateWeeks</span></span>|[<span data-ttu-id="06059-215">windowsUpdateForBusinessUpdateWeeks</span><span class="sxs-lookup"><span data-stu-id="06059-215">windowsUpdateForBusinessUpdateWeeks</span></span>](../resources/intune-deviceconfig-windowsupdateforbusinessupdateweeks.md)|<span data-ttu-id="06059-216">Programar la instalación de la actualización en las semanas del mes.</span><span class="sxs-lookup"><span data-stu-id="06059-216">Scheduled the update installation on the weeks of the month.</span></span> <span data-ttu-id="06059-217">Los valores posibles son: `userDefined`, `firstWeek`, `secondWeek`, `thirdWeek`, `fourthWeek`, `everyWeek`.</span><span class="sxs-lookup"><span data-stu-id="06059-217">Possible values are: `userDefined`, `firstWeek`, `secondWeek`, `thirdWeek`, `fourthWeek`, `everyWeek`.</span></span>|
|<span data-ttu-id="06059-218">qualityUpdatesPauseStartDateTime</span><span class="sxs-lookup"><span data-stu-id="06059-218">qualityUpdatesPauseStartDateTime</span></span>|<span data-ttu-id="06059-219">String</span><span class="sxs-lookup"><span data-stu-id="06059-219">String</span></span>|<span data-ttu-id="06059-220">Datetime de inicio de pausa de actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="06059-220">Quality Updates Pause Start datetime</span></span>|
|<span data-ttu-id="06059-221">featureUpdatesPauseStartDateTime</span><span class="sxs-lookup"><span data-stu-id="06059-221">featureUpdatesPauseStartDateTime</span></span>|<span data-ttu-id="06059-222">String</span><span class="sxs-lookup"><span data-stu-id="06059-222">String</span></span>|<span data-ttu-id="06059-223">Característica Actualizaciones pausar iniciar datetime</span><span class="sxs-lookup"><span data-stu-id="06059-223">Feature Updates Pause Start datetime</span></span>|
|<span data-ttu-id="06059-224">featureUpdatesRollbackWindowInDays</span><span class="sxs-lookup"><span data-stu-id="06059-224">featureUpdatesRollbackWindowInDays</span></span>|<span data-ttu-id="06059-225">Int32</span><span class="sxs-lookup"><span data-stu-id="06059-225">Int32</span></span>|<span data-ttu-id="06059-226">El número de días después de una actualización de la función para la que es válida una reversión</span><span class="sxs-lookup"><span data-stu-id="06059-226">The number of days after a Feature Update for which a rollback is valid</span></span>|
|<span data-ttu-id="06059-227">qualityUpdatesWillBeRolledBack</span><span class="sxs-lookup"><span data-stu-id="06059-227">qualityUpdatesWillBeRolledBack</span></span>|<span data-ttu-id="06059-228">Booleano</span><span class="sxs-lookup"><span data-stu-id="06059-228">Boolean</span></span>|<span data-ttu-id="06059-229">Especifica si para deshacer actualizaciones de calidad en el dispositivo siguiente proteger</span><span class="sxs-lookup"><span data-stu-id="06059-229">Specifies whether to rollback Quality Updates on the next device check in</span></span>|
|<span data-ttu-id="06059-230">featureUpdatesWillBeRolledBack</span><span class="sxs-lookup"><span data-stu-id="06059-230">featureUpdatesWillBeRolledBack</span></span>|<span data-ttu-id="06059-231">Booleano</span><span class="sxs-lookup"><span data-stu-id="06059-231">Boolean</span></span>|<span data-ttu-id="06059-232">Especifica si a rollback comprobar las actualizaciones de la característica en el dispositivo siguiente</span><span class="sxs-lookup"><span data-stu-id="06059-232">Specifies whether to rollback Feature Updates on the next device check in</span></span>|
|<span data-ttu-id="06059-233">qualityUpdatesRollbackStartDateTime</span><span class="sxs-lookup"><span data-stu-id="06059-233">qualityUpdatesRollbackStartDateTime</span></span>|<span data-ttu-id="06059-234">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="06059-234">DateTimeOffset</span></span>|<span data-ttu-id="06059-235">Datetime de inicio de reversión de actualizaciones de calidad</span><span class="sxs-lookup"><span data-stu-id="06059-235">Quality Updates Rollback Start datetime</span></span>|
|<span data-ttu-id="06059-236">featureUpdatesRollbackStartDateTime</span><span class="sxs-lookup"><span data-stu-id="06059-236">featureUpdatesRollbackStartDateTime</span></span>|<span data-ttu-id="06059-237">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="06059-237">DateTimeOffset</span></span>|<span data-ttu-id="06059-238">Datetime de inicio de reversión de actualizaciones de característica</span><span class="sxs-lookup"><span data-stu-id="06059-238">Feature Updates Rollback Start datetime</span></span>|
|<span data-ttu-id="06059-239">engagedRestartDeadlineInDays</span><span class="sxs-lookup"><span data-stu-id="06059-239">engagedRestartDeadlineInDays</span></span>|<span data-ttu-id="06059-240">Int32</span><span class="sxs-lookup"><span data-stu-id="06059-240">Int32</span></span>|<span data-ttu-id="06059-241">Fecha límite en días antes de ejecutar un reinicio pendiente fuera de horas activas, con válido comprendido entre 2 y 30 días y programación automáticamente</span><span class="sxs-lookup"><span data-stu-id="06059-241">Deadline in days before automatically scheduling and executing a pending restart outside of active hours, with valid range from 2 to 30 days</span></span>|
|<span data-ttu-id="06059-242">engagedRestartSnoozeScheduleInDays</span><span class="sxs-lookup"><span data-stu-id="06059-242">engagedRestartSnoozeScheduleInDays</span></span>|<span data-ttu-id="06059-243">Int32</span><span class="sxs-lookup"><span data-stu-id="06059-243">Int32</span></span>|<span data-ttu-id="06059-244">Número de días que un usuario puede posponer notificaciones de aviso reiniciar comprometida con válido comprendido entre 1 y 3 días</span><span class="sxs-lookup"><span data-stu-id="06059-244">Number of days a user can snooze Engaged Restart reminder notifications with valid range from 1 to 3 days</span></span>|
|<span data-ttu-id="06059-245">engagedRestartTransitionScheduleInDays</span><span class="sxs-lookup"><span data-stu-id="06059-245">engagedRestartTransitionScheduleInDays</span></span>|<span data-ttu-id="06059-246">Int32</span><span class="sxs-lookup"><span data-stu-id="06059-246">Int32</span></span>|<span data-ttu-id="06059-247">Número de días antes de realizar la transición de automático se reinicia programada fuera de horas activas para reiniciar comprometida, que requiere que el usuario programar con válido comprendido entre 0 y 30 días</span><span class="sxs-lookup"><span data-stu-id="06059-247">Number of days before transitioning from Auto Restarts scheduled outside of active hours to Engaged Restart, which requires the user to schedule, with valid range from 0 to 30 days</span></span>|
|<span data-ttu-id="06059-248">autoRestartNotificationDismissal</span><span class="sxs-lookup"><span data-stu-id="06059-248">autoRestartNotificationDismissal</span></span>|[<span data-ttu-id="06059-249">autoRestartNotificationDismissalMethod</span><span class="sxs-lookup"><span data-stu-id="06059-249">autoRestartNotificationDismissalMethod</span></span>](../resources/intune-deviceconfig-autorestartnotificationdismissalmethod.md)|<span data-ttu-id="06059-250">Especificar el método mediante el cual se requiere el reinicio automático se descarta la notificación.</span><span class="sxs-lookup"><span data-stu-id="06059-250">Specify the method by which the auto-restart required notification is dismissed.</span></span> <span data-ttu-id="06059-251">Los valores posibles son: `notConfigured`, `automatic` y `user`.</span><span class="sxs-lookup"><span data-stu-id="06059-251">Possible values are: `notConfigured`, `automatic`, `user`.</span></span>|
|<span data-ttu-id="06059-252">scheduleRestartWarningInHours</span><span class="sxs-lookup"><span data-stu-id="06059-252">scheduleRestartWarningInHours</span></span>|<span data-ttu-id="06059-253">Int32</span><span class="sxs-lookup"><span data-stu-id="06059-253">Int32</span></span>|<span data-ttu-id="06059-254">Especifique el período para las notificaciones de aviso de advertencia de reinicio automático.</span><span class="sxs-lookup"><span data-stu-id="06059-254">Specify the period for auto-restart warning reminder notifications.</span></span> <span data-ttu-id="06059-255">Valores admitidos: 2, 4, 8, 12 o 24 (horas).</span><span class="sxs-lookup"><span data-stu-id="06059-255">Supported values: 2, 4, 8, 12 or 24 (hours).</span></span>|
|<span data-ttu-id="06059-256">scheduleImminentRestartWarningInMinutes</span><span class="sxs-lookup"><span data-stu-id="06059-256">scheduleImminentRestartWarningInMinutes</span></span>|<span data-ttu-id="06059-257">Int32</span><span class="sxs-lookup"><span data-stu-id="06059-257">Int32</span></span>|<span data-ttu-id="06059-258">Especifique el período para las notificaciones de advertencia inminente reinicio automático.</span><span class="sxs-lookup"><span data-stu-id="06059-258">Specify the period for auto-restart imminent warning notifications.</span></span> <span data-ttu-id="06059-259">Valores admitidos: 15, 30 o 60 (minutos).</span><span class="sxs-lookup"><span data-stu-id="06059-259">Supported values: 15, 30 or 60 (minutes).</span></span>|



## <a name="response"></a><span data-ttu-id="06059-260">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06059-260">Response</span></span>
<span data-ttu-id="06059-261">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="06059-261">If successful, this method returns a `201 Created` response code and a [windowsUpdateForBusinessConfiguration](../resources/intune-deviceconfig-windowsupdateforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="06059-262">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="06059-262">Example</span></span>
### <a name="request"></a><span data-ttu-id="06059-263">Solicitud</span><span class="sxs-lookup"><span data-stu-id="06059-263">Request</span></span>
<span data-ttu-id="06059-264">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="06059-264">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 1863

{
  "@odata.type": "#microsoft.graph.windowsUpdateForBusinessConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
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
  "businessReadyUpdatesOnly": "all",
  "skipChecksBeforeRestart": true,
  "updateWeeks": "firstWeek",
  "qualityUpdatesPauseStartDateTime": "Quality Updates Pause Start Date Time value",
  "featureUpdatesPauseStartDateTime": "Feature Updates Pause Start Date Time value",
  "featureUpdatesRollbackWindowInDays": 2,
  "qualityUpdatesWillBeRolledBack": true,
  "featureUpdatesWillBeRolledBack": true,
  "qualityUpdatesRollbackStartDateTime": "2016-12-31T23:57:01.05526-08:00",
  "featureUpdatesRollbackStartDateTime": "2017-01-01T00:03:21.6080517-08:00",
  "engagedRestartDeadlineInDays": 12,
  "engagedRestartSnoozeScheduleInDays": 2,
  "engagedRestartTransitionScheduleInDays": 6,
  "autoRestartNotificationDismissal": "automatic",
  "scheduleRestartWarningInHours": 13,
  "scheduleImminentRestartWarningInMinutes": 7
}
```

### <a name="response"></a><span data-ttu-id="06059-265">Respuesta</span><span class="sxs-lookup"><span data-stu-id="06059-265">Response</span></span>
<span data-ttu-id="06059-p119">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="06059-p119">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 1971

{
  "@odata.type": "#microsoft.graph.windowsUpdateForBusinessConfiguration",
  "id": "4928dd6a-dd6a-4928-6add-28496add2849",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
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
  "businessReadyUpdatesOnly": "all",
  "skipChecksBeforeRestart": true,
  "updateWeeks": "firstWeek",
  "qualityUpdatesPauseStartDateTime": "Quality Updates Pause Start Date Time value",
  "featureUpdatesPauseStartDateTime": "Feature Updates Pause Start Date Time value",
  "featureUpdatesRollbackWindowInDays": 2,
  "qualityUpdatesWillBeRolledBack": true,
  "featureUpdatesWillBeRolledBack": true,
  "qualityUpdatesRollbackStartDateTime": "2016-12-31T23:57:01.05526-08:00",
  "featureUpdatesRollbackStartDateTime": "2017-01-01T00:03:21.6080517-08:00",
  "engagedRestartDeadlineInDays": 12,
  "engagedRestartSnoozeScheduleInDays": 2,
  "engagedRestartTransitionScheduleInDays": 6,
  "autoRestartNotificationDismissal": "automatic",
  "scheduleRestartWarningInHours": 13,
  "scheduleImminentRestartWarningInMinutes": 7
}
```




