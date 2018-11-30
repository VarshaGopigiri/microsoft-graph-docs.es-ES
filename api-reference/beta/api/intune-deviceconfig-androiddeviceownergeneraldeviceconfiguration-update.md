---
title: Actualizar androidDeviceOwnerGeneralDeviceConfiguration
description: Actualizar las propiedades de un objeto androidDeviceOwnerGeneralDeviceConfiguration.
ms.openlocfilehash: 463d40f24bb4240eed4fc60078b0fb576a8928b9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087736"
---
# <a name="update-androiddeviceownergeneraldeviceconfiguration"></a><span data-ttu-id="95db0-103">Actualizar androidDeviceOwnerGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="95db0-103">Update androidDeviceOwnerGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="95db0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="95db0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="95db0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="95db0-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="95db0-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="95db0-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="95db0-107">Actualizar las propiedades de un objeto [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="95db0-107">Update the properties of a [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="95db0-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="95db0-108">Prerequisites</span></span>
<span data-ttu-id="95db0-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="95db0-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="95db0-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="95db0-111">Permission type</span></span>|<span data-ttu-id="95db0-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="95db0-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="95db0-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="95db0-113">Delegated (work or school account)</span></span>|<span data-ttu-id="95db0-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="95db0-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="95db0-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="95db0-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="95db0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="95db0-116">Not supported.</span></span>|
|<span data-ttu-id="95db0-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="95db0-117">Application</span></span>|<span data-ttu-id="95db0-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="95db0-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="95db0-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="95db0-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="95db0-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="95db0-120">Request headers</span></span>
|<span data-ttu-id="95db0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="95db0-121">Header</span></span>|<span data-ttu-id="95db0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="95db0-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="95db0-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="95db0-123">Authorization</span></span>|<span data-ttu-id="95db0-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="95db0-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="95db0-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="95db0-125">Accept</span></span>|<span data-ttu-id="95db0-126">application/json</span><span class="sxs-lookup"><span data-stu-id="95db0-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="95db0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="95db0-127">Request body</span></span>
<span data-ttu-id="95db0-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="95db0-128">In the request body, supply a JSON representation for the [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) object.</span></span>

<span data-ttu-id="95db0-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="95db0-129">The following table shows the properties that are required when you create the [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md).</span></span>

|<span data-ttu-id="95db0-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="95db0-130">Property</span></span>|<span data-ttu-id="95db0-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="95db0-131">Type</span></span>|<span data-ttu-id="95db0-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="95db0-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="95db0-133">id</span><span class="sxs-lookup"><span data-stu-id="95db0-133">id</span></span>|<span data-ttu-id="95db0-134">String</span><span class="sxs-lookup"><span data-stu-id="95db0-134">String</span></span>|<span data-ttu-id="95db0-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="95db0-135">Key of the entity.</span></span> <span data-ttu-id="95db0-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="95db0-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="95db0-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="95db0-137">lastModifiedDateTime</span></span>|<span data-ttu-id="95db0-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="95db0-138">DateTimeOffset</span></span>|<span data-ttu-id="95db0-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="95db0-139">DateTime the object was last modified.</span></span> <span data-ttu-id="95db0-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="95db0-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="95db0-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="95db0-141">roleScopeTagIds</span></span>|<span data-ttu-id="95db0-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="95db0-142">String collection</span></span>|<span data-ttu-id="95db0-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="95db0-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="95db0-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="95db0-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="95db0-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="95db0-145">supportsScopeTags</span></span>|<span data-ttu-id="95db0-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-146">Boolean</span></span>|<span data-ttu-id="95db0-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="95db0-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="95db0-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="95db0-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="95db0-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="95db0-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="95db0-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="95db0-150">This property is read-only.</span></span> <span data-ttu-id="95db0-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="95db0-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="95db0-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="95db0-152">createdDateTime</span></span>|<span data-ttu-id="95db0-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="95db0-153">DateTimeOffset</span></span>|<span data-ttu-id="95db0-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="95db0-154">DateTime the object was created.</span></span> <span data-ttu-id="95db0-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="95db0-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="95db0-156">descripción</span><span class="sxs-lookup"><span data-stu-id="95db0-156">description</span></span>|<span data-ttu-id="95db0-157">String</span><span class="sxs-lookup"><span data-stu-id="95db0-157">String</span></span>|<span data-ttu-id="95db0-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95db0-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="95db0-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="95db0-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="95db0-160">displayName</span><span class="sxs-lookup"><span data-stu-id="95db0-160">displayName</span></span>|<span data-ttu-id="95db0-161">String</span><span class="sxs-lookup"><span data-stu-id="95db0-161">String</span></span>|<span data-ttu-id="95db0-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95db0-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="95db0-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="95db0-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="95db0-164">version</span><span class="sxs-lookup"><span data-stu-id="95db0-164">version</span></span>|<span data-ttu-id="95db0-165">Int32</span><span class="sxs-lookup"><span data-stu-id="95db0-165">Int32</span></span>|<span data-ttu-id="95db0-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95db0-166">Version of the device configuration.</span></span> <span data-ttu-id="95db0-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="95db0-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="95db0-168">accountsBlockModification</span><span class="sxs-lookup"><span data-stu-id="95db0-168">accountsBlockModification</span></span>|<span data-ttu-id="95db0-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-169">Boolean</span></span>|<span data-ttu-id="95db0-170">Indica si está deshabilitada la opción Agregar o quitar cuentas de.</span><span class="sxs-lookup"><span data-stu-id="95db0-170">Indicates whether or not adding or removing accounts is disabled.</span></span>|
|<span data-ttu-id="95db0-171">appsAllowInstallFromUnknownSources</span><span class="sxs-lookup"><span data-stu-id="95db0-171">appsAllowInstallFromUnknownSources</span></span>|<span data-ttu-id="95db0-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-172">Boolean</span></span>|<span data-ttu-id="95db0-173">Indica si se permite al usuario para habilitar la configuración de orígenes desconocidos.</span><span class="sxs-lookup"><span data-stu-id="95db0-173">Indicates whether or not the user is allowed to enable to unknown sources setting.</span></span>|
|<span data-ttu-id="95db0-174">appsAutoUpdatePolicy</span><span class="sxs-lookup"><span data-stu-id="95db0-174">appsAutoUpdatePolicy</span></span>|[<span data-ttu-id="95db0-175">androidDeviceOwnerAppAutoUpdatePolicyType</span><span class="sxs-lookup"><span data-stu-id="95db0-175">androidDeviceOwnerAppAutoUpdatePolicyType</span></span>](../resources/intune-deviceconfig-androiddeviceownerappautoupdatepolicytype.md)|<span data-ttu-id="95db0-176">Indica el valor de la directiva de actualización automática de aplicación.</span><span class="sxs-lookup"><span data-stu-id="95db0-176">Indicates the value of the app auto update policy.</span></span> <span data-ttu-id="95db0-177">Los valores posibles son: `notConfigured`, `userChoice`, `never`, `wiFiOnly` y `always`.</span><span class="sxs-lookup"><span data-stu-id="95db0-177">Possible values are: `notConfigured`, `userChoice`, `never`, `wiFiOnly`, `always`.</span></span>|
|<span data-ttu-id="95db0-178">appsDefaultPermissionPolicy</span><span class="sxs-lookup"><span data-stu-id="95db0-178">appsDefaultPermissionPolicy</span></span>|[<span data-ttu-id="95db0-179">androidDeviceOwnerDefaultAppPermissionPolicyType</span><span class="sxs-lookup"><span data-stu-id="95db0-179">androidDeviceOwnerDefaultAppPermissionPolicyType</span></span>](../resources/intune-deviceconfig-androiddeviceownerdefaultapppermissionpolicytype.md)|<span data-ttu-id="95db0-180">Indica la directiva de permisos para las solicitudes de permisos en tiempo de ejecución si uno no se ha definido para la aplicación en concreto.</span><span class="sxs-lookup"><span data-stu-id="95db0-180">Indicates the permission policy for requests for runtime permissions if one is not defined for the app specifically.</span></span> <span data-ttu-id="95db0-181">Los valores posibles son: `deviceDefault`, `prompt`, `autoGrant` y `autoDeny`.</span><span class="sxs-lookup"><span data-stu-id="95db0-181">Possible values are: `deviceDefault`, `prompt`, `autoGrant`, `autoDeny`.</span></span>|
|<span data-ttu-id="95db0-182">bluetoothBlockConfiguration</span><span class="sxs-lookup"><span data-stu-id="95db0-182">bluetoothBlockConfiguration</span></span>|<span data-ttu-id="95db0-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-183">Boolean</span></span>|<span data-ttu-id="95db0-184">Indica si se deben bloquear un usuario desde la configuración de bluetooth.</span><span class="sxs-lookup"><span data-stu-id="95db0-184">Indicates whether or not to block a user from configuring bluetooth.</span></span>|
|<span data-ttu-id="95db0-185">bluetoothBlockContactSharing</span><span class="sxs-lookup"><span data-stu-id="95db0-185">bluetoothBlockContactSharing</span></span>|<span data-ttu-id="95db0-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-186">Boolean</span></span>|<span data-ttu-id="95db0-187">Indica si se va a bloquear un usuario de uso compartido de contactos a través de bluetooth o no.</span><span class="sxs-lookup"><span data-stu-id="95db0-187">Indicates whether or not to block a user from sharing contacts via bluetooth.</span></span>|
|<span data-ttu-id="95db0-188">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="95db0-188">cameraBlocked</span></span>|<span data-ttu-id="95db0-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-189">Boolean</span></span>|<span data-ttu-id="95db0-190">Indica si se va a deshabilitar el uso de la cámara o no.</span><span class="sxs-lookup"><span data-stu-id="95db0-190">Indicates whether or not to disable the use of the camera.</span></span>|
|<span data-ttu-id="95db0-191">cellularBlockWiFiTethering</span><span class="sxs-lookup"><span data-stu-id="95db0-191">cellularBlockWiFiTethering</span></span>|<span data-ttu-id="95db0-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-192">Boolean</span></span>|<span data-ttu-id="95db0-193">Indica si se va a bloquear el tethering Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="95db0-193">Indicates whether or not to block Wi-Fi tethering.</span></span>|
|<span data-ttu-id="95db0-194">dataRoamingBlocked</span><span class="sxs-lookup"><span data-stu-id="95db0-194">dataRoamingBlocked</span></span>|<span data-ttu-id="95db0-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-195">Boolean</span></span>|<span data-ttu-id="95db0-196">Indica si se deben bloquear un usuario de movilidad de datos.</span><span class="sxs-lookup"><span data-stu-id="95db0-196">Indicates whether or not to block a user from data roaming.</span></span>|
|<span data-ttu-id="95db0-197">dateTimeConfigurationBlocked</span><span class="sxs-lookup"><span data-stu-id="95db0-197">dateTimeConfigurationBlocked</span></span>|<span data-ttu-id="95db0-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-198">Boolean</span></span>|<span data-ttu-id="95db0-199">Indica si se deben bloquear el usuario cambie manualmente la fecha o la hora en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="95db0-199">Indicates whether or not to block the user from manually changing the date or time on the device</span></span>|
|<span data-ttu-id="95db0-200">factoryResetDeviceAdministratorEmails</span><span class="sxs-lookup"><span data-stu-id="95db0-200">factoryResetDeviceAdministratorEmails</span></span>|<span data-ttu-id="95db0-201">Colección String</span><span class="sxs-lookup"><span data-stu-id="95db0-201">String collection</span></span>|<span data-ttu-id="95db0-202">Lista de correos electrónicos de la cuenta de Google que serán necesarios para autenticar una vez fábrica restablecer antes de que se puede configurar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95db0-202">List of Google account emails that will be required to authenticate after a device is factory reset before it can be set up.</span></span>|
|<span data-ttu-id="95db0-203">factoryResetBlocked</span><span class="sxs-lookup"><span data-stu-id="95db0-203">factoryResetBlocked</span></span>|<span data-ttu-id="95db0-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-204">Boolean</span></span>|<span data-ttu-id="95db0-205">Indica si está deshabilitada la opción de restablecimiento de fábrica en configuración.</span><span class="sxs-lookup"><span data-stu-id="95db0-205">Indicates whether or not the factory reset option in settings is disabled.</span></span>|
|<span data-ttu-id="95db0-206">kioskModeApps</span><span class="sxs-lookup"><span data-stu-id="95db0-206">kioskModeApps</span></span>|<span data-ttu-id="95db0-207">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="95db0-207">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="95db0-208">Una lista de aplicaciones administradas que se mostrará cuando el dispositivo está en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="95db0-208">A list of managed apps that will be shown when the device is in Kiosk Mode.</span></span> <span data-ttu-id="95db0-209">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="95db0-209">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="95db0-210">microphoneForceMute</span><span class="sxs-lookup"><span data-stu-id="95db0-210">microphoneForceMute</span></span>|<span data-ttu-id="95db0-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-211">Boolean</span></span>|<span data-ttu-id="95db0-212">Indica si se deben bloquear del audio del micrófono en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95db0-212">Indicates whether or not to block unmuting the microphone on the device.</span></span>|
|<span data-ttu-id="95db0-213">networkEscapeHatchAllowed</span><span class="sxs-lookup"><span data-stu-id="95db0-213">networkEscapeHatchAllowed</span></span>|<span data-ttu-id="95db0-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-214">Boolean</span></span>|<span data-ttu-id="95db0-215">Indica si el dispositivo permitirá que se conectan a una conexión de red temporal en tiempo de inicio.</span><span class="sxs-lookup"><span data-stu-id="95db0-215">Indicates whether or not the device will allow connecting to a temporary network connection at boot time.</span></span>|
|<span data-ttu-id="95db0-216">nfcBlockOutgoingBeam</span><span class="sxs-lookup"><span data-stu-id="95db0-216">nfcBlockOutgoingBeam</span></span>|<span data-ttu-id="95db0-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-217">Boolean</span></span>|<span data-ttu-id="95db0-218">Indica si se deben bloquear carretera saliente CNC.</span><span class="sxs-lookup"><span data-stu-id="95db0-218">Indicates whether or not to block NFC outgoing beam.</span></span>|
|<span data-ttu-id="95db0-219">passwordBlockKeyguard</span><span class="sxs-lookup"><span data-stu-id="95db0-219">passwordBlockKeyguard</span></span>|<span data-ttu-id="95db0-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-220">Boolean</span></span>|<span data-ttu-id="95db0-221">Indica si está deshabilitada la keyguard.</span><span class="sxs-lookup"><span data-stu-id="95db0-221">Indicates whether or not the keyguard is disabled.</span></span>|
|<span data-ttu-id="95db0-222">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="95db0-222">passwordExpirationDays</span></span>|<span data-ttu-id="95db0-223">Int32</span><span class="sxs-lookup"><span data-stu-id="95db0-223">Int32</span></span>|<span data-ttu-id="95db0-224">Indica la cantidad de tiempo en segundos que se puede establecer una contraseña para antes de que caduque y se le solicitará una contraseña nueva.</span><span class="sxs-lookup"><span data-stu-id="95db0-224">Indicates the amount of time in seconds that a password can be set for before it expires and a new password will be required.</span></span> <span data-ttu-id="95db0-225">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="95db0-225">Valid values 1 to 365</span></span>|
|<span data-ttu-id="95db0-226">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="95db0-226">passwordMinimumLength</span></span>|<span data-ttu-id="95db0-227">Int32</span><span class="sxs-lookup"><span data-stu-id="95db0-227">Int32</span></span>|<span data-ttu-id="95db0-228">Indica la longitud mínima de la contraseña requerida en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95db0-228">Indicates the minimum length of the password required on the device.</span></span> <span data-ttu-id="95db0-229">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="95db0-229">Valid values 4 to 16</span></span>|
|<span data-ttu-id="95db0-230">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="95db0-230">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="95db0-231">Int32</span><span class="sxs-lookup"><span data-stu-id="95db0-231">Int32</span></span>|<span data-ttu-id="95db0-232">Milisegundos de inactividad antes de agote el tiempo de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="95db0-232">Milliseconds of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="95db0-233">passwordPreviousPasswordCountToBlock</span><span class="sxs-lookup"><span data-stu-id="95db0-233">passwordPreviousPasswordCountToBlock</span></span>|<span data-ttu-id="95db0-234">Int32</span><span class="sxs-lookup"><span data-stu-id="95db0-234">Int32</span></span>|<span data-ttu-id="95db0-235">Indica la longitud del historial de contraseñas, donde el usuario no podrá escribir una nueva contraseña que es el mismo que el de las contraseñas en el historial.</span><span class="sxs-lookup"><span data-stu-id="95db0-235">Indicates the length of password history, where the user will not be able to enter a new password that is the same as any password in the history.</span></span> <span data-ttu-id="95db0-236">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="95db0-236">Valid values 0 to 24</span></span>|
|<span data-ttu-id="95db0-237">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="95db0-237">passwordRequiredType</span></span>|[<span data-ttu-id="95db0-238">androidDeviceOwnerRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="95db0-238">androidDeviceOwnerRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androiddeviceownerrequiredpasswordtype.md)|<span data-ttu-id="95db0-239">Indica la calidad mínima de la contraseña necesaria en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95db0-239">Indicates the minimum password quality required on the device.</span></span> <span data-ttu-id="95db0-240">Los valores posibles son: `deviceDefault`, `required`, `numeric`, `numericComplex`, `alphabetic`, `alphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="95db0-240">Possible values are: `deviceDefault`, `required`, `numeric`, `numericComplex`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="95db0-241">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="95db0-241">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="95db0-242">Int32</span><span class="sxs-lookup"><span data-stu-id="95db0-242">Int32</span></span>|<span data-ttu-id="95db0-243">Indica el número de veces que un usuario puede escribir una contraseña incorrecta antes de que se borre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="95db0-243">Indicates the number of times a user can enter an incorrect password before the device is wiped.</span></span> <span data-ttu-id="95db0-244">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="95db0-244">Valid values 4 to 11</span></span>|
|<span data-ttu-id="95db0-245">safeBootBlocked</span><span class="sxs-lookup"><span data-stu-id="95db0-245">safeBootBlocked</span></span>|<span data-ttu-id="95db0-246">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-246">Boolean</span></span>|<span data-ttu-id="95db0-247">Indica si al reiniciar que el dispositivo en Inicio seguro está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="95db0-247">Indicates whether or not rebooting the device into safe boot is disabled.</span></span>|
|<span data-ttu-id="95db0-248">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="95db0-248">screenCaptureBlocked</span></span>|<span data-ttu-id="95db0-249">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-249">Boolean</span></span>|<span data-ttu-id="95db0-250">Indica si se va a deshabilitar la capacidad de realizar capturas de pantalla o no.</span><span class="sxs-lookup"><span data-stu-id="95db0-250">Indicates whether or not to disable the capability to take screenshots.</span></span>|
|<span data-ttu-id="95db0-251">securityAllowDebuggingFeatures</span><span class="sxs-lookup"><span data-stu-id="95db0-251">securityAllowDebuggingFeatures</span></span>|<span data-ttu-id="95db0-252">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-252">Boolean</span></span>|<span data-ttu-id="95db0-253">Indica si desea impedir que el usuario de habilitación de características de depuración en el dispositivo o no.</span><span class="sxs-lookup"><span data-stu-id="95db0-253">Indicates whether or not to block the user from enabling debugging features on the device.</span></span>|
|<span data-ttu-id="95db0-254">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="95db0-254">securityRequireVerifyApps</span></span>|<span data-ttu-id="95db0-255">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-255">Boolean</span></span>|<span data-ttu-id="95db0-256">Indica si o no comprobar aplicaciones es necesario.</span><span class="sxs-lookup"><span data-stu-id="95db0-256">Indicates whether or not verify apps is required.</span></span>|
|<span data-ttu-id="95db0-257">statusBarBlocked</span><span class="sxs-lookup"><span data-stu-id="95db0-257">statusBarBlocked</span></span>|<span data-ttu-id="95db0-258">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-258">Boolean</span></span>|<span data-ttu-id="95db0-259">Indica si el estado o barra está deshabilitada, incluidas las notificaciones, la configuración rápida y otros superposiciones de pantalla.</span><span class="sxs-lookup"><span data-stu-id="95db0-259">Indicates whether or the status bar is disabled, including notifications, quick settings and other screen overlays.</span></span>|
|<span data-ttu-id="95db0-260">stayOnModes</span><span class="sxs-lookup"><span data-stu-id="95db0-260">stayOnModes</span></span>|<span data-ttu-id="95db0-261">colección de [androidDeviceOwnerBatteryPluggedMode](../resources/intune-deviceconfig-androiddeviceownerbatterypluggedmode.md)</span><span class="sxs-lookup"><span data-stu-id="95db0-261">[androidDeviceOwnerBatteryPluggedMode](../resources/intune-deviceconfig-androiddeviceownerbatterypluggedmode.md) collection</span></span>|<span data-ttu-id="95db0-262">Lista de los modos en que la pantalla del dispositivo permanecerá enciende.</span><span class="sxs-lookup"><span data-stu-id="95db0-262">List of modes in which the device's display will stay powered-on.</span></span> <span data-ttu-id="95db0-263">Esta colección puede contener un máximo de 4 elementos.</span><span class="sxs-lookup"><span data-stu-id="95db0-263">This collection can contain a maximum of 4 elements.</span></span> <span data-ttu-id="95db0-264">Los valores posibles son: `notConfigured`, `ac`, `usb` y `wireless`.</span><span class="sxs-lookup"><span data-stu-id="95db0-264">Possible values are: `notConfigured`, `ac`, `usb`, `wireless`.</span></span>|
|<span data-ttu-id="95db0-265">storageAllowUsb</span><span class="sxs-lookup"><span data-stu-id="95db0-265">storageAllowUsb</span></span>|<span data-ttu-id="95db0-266">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-266">Boolean</span></span>|<span data-ttu-id="95db0-267">Indica si se debe o no permitir el almacenamiento masivo USB.</span><span class="sxs-lookup"><span data-stu-id="95db0-267">Indicates whether or not to allow USB mass storage.</span></span>|
|<span data-ttu-id="95db0-268">storageBlockExternalMedia</span><span class="sxs-lookup"><span data-stu-id="95db0-268">storageBlockExternalMedia</span></span>|<span data-ttu-id="95db0-269">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-269">Boolean</span></span>|<span data-ttu-id="95db0-270">Indica si se deben bloquear medios externos.</span><span class="sxs-lookup"><span data-stu-id="95db0-270">Indicates whether or not to block external media.</span></span>|
|<span data-ttu-id="95db0-271">storageBlockUsbFileTransfer</span><span class="sxs-lookup"><span data-stu-id="95db0-271">storageBlockUsbFileTransfer</span></span>|<span data-ttu-id="95db0-272">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-272">Boolean</span></span>|<span data-ttu-id="95db0-273">Indica si se deben bloquear la transferencia de archivos USB.</span><span class="sxs-lookup"><span data-stu-id="95db0-273">Indicates whether or not to block USB file transfer.</span></span>|
|<span data-ttu-id="95db0-274">systemUpdateWindowStartMinutesAfterMidnight</span><span class="sxs-lookup"><span data-stu-id="95db0-274">systemUpdateWindowStartMinutesAfterMidnight</span></span>|<span data-ttu-id="95db0-275">Int32</span><span class="sxs-lookup"><span data-stu-id="95db0-275">Int32</span></span>|<span data-ttu-id="95db0-276">Indica el número de minutos después de la medianoche que inicia la ventana de actualización del sistema.</span><span class="sxs-lookup"><span data-stu-id="95db0-276">Indicates the number of minutes after midnight that the system update window starts.</span></span> <span data-ttu-id="95db0-277">Valores válidos 0 y 1440.</span><span class="sxs-lookup"><span data-stu-id="95db0-277">Valid values 0 to 1440</span></span>|
|<span data-ttu-id="95db0-278">systemUpdateWindowEndMinutesAfterMidnight</span><span class="sxs-lookup"><span data-stu-id="95db0-278">systemUpdateWindowEndMinutesAfterMidnight</span></span>|<span data-ttu-id="95db0-279">Int32</span><span class="sxs-lookup"><span data-stu-id="95db0-279">Int32</span></span>|<span data-ttu-id="95db0-280">Indica el número de minutos después de la medianoche que termina la ventana de actualización del sistema.</span><span class="sxs-lookup"><span data-stu-id="95db0-280">Indicates the number of minutes after midnight that the system update window ends.</span></span> <span data-ttu-id="95db0-281">Valores válidos 0 y 1440.</span><span class="sxs-lookup"><span data-stu-id="95db0-281">Valid values 0 to 1440</span></span>|
|<span data-ttu-id="95db0-282">systemUpdateInstallType</span><span class="sxs-lookup"><span data-stu-id="95db0-282">systemUpdateInstallType</span></span>|[<span data-ttu-id="95db0-283">androidDeviceOwnerSystemUpdateInstallType</span><span class="sxs-lookup"><span data-stu-id="95db0-283">androidDeviceOwnerSystemUpdateInstallType</span></span>](../resources/intune-deviceconfig-androiddeviceownersystemupdateinstalltype.md)|<span data-ttu-id="95db0-284">El tipo de configuración de la actualización del sistema.</span><span class="sxs-lookup"><span data-stu-id="95db0-284">The type of system update configuration.</span></span> <span data-ttu-id="95db0-285">Los valores posibles son: `deviceDefault`, `postpone`, `windowed` y `automatic`.</span><span class="sxs-lookup"><span data-stu-id="95db0-285">Possible values are: `deviceDefault`, `postpone`, `windowed`, `automatic`.</span></span>|
|<span data-ttu-id="95db0-286">usersBlockAdd</span><span class="sxs-lookup"><span data-stu-id="95db0-286">usersBlockAdd</span></span>|<span data-ttu-id="95db0-287">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-287">Boolean</span></span>|<span data-ttu-id="95db0-288">Indica si está deshabilitada la opción Agregar usuarios y perfiles de.</span><span class="sxs-lookup"><span data-stu-id="95db0-288">Indicates whether or not adding users and profiles is disabled.</span></span>|
|<span data-ttu-id="95db0-289">usersBlockRemove</span><span class="sxs-lookup"><span data-stu-id="95db0-289">usersBlockRemove</span></span>|<span data-ttu-id="95db0-290">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-290">Boolean</span></span>|<span data-ttu-id="95db0-291">Indica si desea deshabilitar la eliminación de otros usuarios desde el dispositivo o no.</span><span class="sxs-lookup"><span data-stu-id="95db0-291">Indicates whether or not to disable removing other users from the device.</span></span>|
|<span data-ttu-id="95db0-292">volumeBlockAdjustment</span><span class="sxs-lookup"><span data-stu-id="95db0-292">volumeBlockAdjustment</span></span>|<span data-ttu-id="95db0-293">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-293">Boolean</span></span>|<span data-ttu-id="95db0-294">Indica si o no ajustar que el volumen principal está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="95db0-294">Indicates whether or not adjusting the master volume is disabled.</span></span>|
|<span data-ttu-id="95db0-295">wifiBlockEditConfigurations</span><span class="sxs-lookup"><span data-stu-id="95db0-295">wifiBlockEditConfigurations</span></span>|<span data-ttu-id="95db0-296">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-296">Boolean</span></span>|<span data-ttu-id="95db0-297">Indica si desea impedir que el usuario de edición de la configuración de conexión wifi o no.</span><span class="sxs-lookup"><span data-stu-id="95db0-297">Indicates whether or not to block the user from editing the wifi connection settings.</span></span>|
|<span data-ttu-id="95db0-298">wifiBlockEditPolicyDefinedConfigurations</span><span class="sxs-lookup"><span data-stu-id="95db0-298">wifiBlockEditPolicyDefinedConfigurations</span></span>|<span data-ttu-id="95db0-299">Booleano</span><span class="sxs-lookup"><span data-stu-id="95db0-299">Boolean</span></span>|<span data-ttu-id="95db0-300">Indica si desea impedir que el usuario acaba las redes definidas por la directiva de edición o no.</span><span class="sxs-lookup"><span data-stu-id="95db0-300">Indicates whether or not to block the user from editing just the networks defined by the policy.</span></span>|



## <a name="response"></a><span data-ttu-id="95db0-301">Respuesta</span><span class="sxs-lookup"><span data-stu-id="95db0-301">Response</span></span>
<span data-ttu-id="95db0-302">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="95db0-302">If successful, this method returns a `200 OK` response code and an updated [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="95db0-303">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="95db0-303">Example</span></span>
### <a name="request"></a><span data-ttu-id="95db0-304">Solicitud</span><span class="sxs-lookup"><span data-stu-id="95db0-304">Request</span></span>
<span data-ttu-id="95db0-305">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="95db0-305">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 2073

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountsBlockModification": true,
  "appsAllowInstallFromUnknownSources": true,
  "appsAutoUpdatePolicy": "userChoice",
  "appsDefaultPermissionPolicy": "prompt",
  "bluetoothBlockConfiguration": true,
  "bluetoothBlockContactSharing": true,
  "cameraBlocked": true,
  "cellularBlockWiFiTethering": true,
  "dataRoamingBlocked": true,
  "dateTimeConfigurationBlocked": true,
  "factoryResetDeviceAdministratorEmails": [
    "Factory Reset Device Administrator Emails value"
  ],
  "factoryResetBlocked": true,
  "kioskModeApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "microphoneForceMute": true,
  "networkEscapeHatchAllowed": true,
  "nfcBlockOutgoingBeam": true,
  "passwordBlockKeyguard": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordCountToBlock": 4,
  "passwordRequiredType": "required",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "safeBootBlocked": true,
  "screenCaptureBlocked": true,
  "securityAllowDebuggingFeatures": true,
  "securityRequireVerifyApps": true,
  "statusBarBlocked": true,
  "stayOnModes": [
    "ac"
  ],
  "storageAllowUsb": true,
  "storageBlockExternalMedia": true,
  "storageBlockUsbFileTransfer": true,
  "systemUpdateWindowStartMinutesAfterMidnight": 11,
  "systemUpdateWindowEndMinutesAfterMidnight": 9,
  "systemUpdateInstallType": "postpone",
  "usersBlockAdd": true,
  "usersBlockRemove": true,
  "volumeBlockAdjustment": true,
  "wifiBlockEditConfigurations": true,
  "wifiBlockEditPolicyDefinedConfigurations": true
}
```

### <a name="response"></a><span data-ttu-id="95db0-306">Respuesta</span><span class="sxs-lookup"><span data-stu-id="95db0-306">Response</span></span>
<span data-ttu-id="95db0-p123">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="95db0-p123">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2264

{
  "@odata.type": "#microsoft.graph.androidDeviceOwnerGeneralDeviceConfiguration",
  "id": "edad943d-943d-edad-3d94-aded3d94aded",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountsBlockModification": true,
  "appsAllowInstallFromUnknownSources": true,
  "appsAutoUpdatePolicy": "userChoice",
  "appsDefaultPermissionPolicy": "prompt",
  "bluetoothBlockConfiguration": true,
  "bluetoothBlockContactSharing": true,
  "cameraBlocked": true,
  "cellularBlockWiFiTethering": true,
  "dataRoamingBlocked": true,
  "dateTimeConfigurationBlocked": true,
  "factoryResetDeviceAdministratorEmails": [
    "Factory Reset Device Administrator Emails value"
  ],
  "factoryResetBlocked": true,
  "kioskModeApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "microphoneForceMute": true,
  "networkEscapeHatchAllowed": true,
  "nfcBlockOutgoingBeam": true,
  "passwordBlockKeyguard": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordCountToBlock": 4,
  "passwordRequiredType": "required",
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "safeBootBlocked": true,
  "screenCaptureBlocked": true,
  "securityAllowDebuggingFeatures": true,
  "securityRequireVerifyApps": true,
  "statusBarBlocked": true,
  "stayOnModes": [
    "ac"
  ],
  "storageAllowUsb": true,
  "storageBlockExternalMedia": true,
  "storageBlockUsbFileTransfer": true,
  "systemUpdateWindowStartMinutesAfterMidnight": 11,
  "systemUpdateWindowEndMinutesAfterMidnight": 9,
  "systemUpdateInstallType": "postpone",
  "usersBlockAdd": true,
  "usersBlockRemove": true,
  "volumeBlockAdjustment": true,
  "wifiBlockEditConfigurations": true,
  "wifiBlockEditPolicyDefinedConfigurations": true
}
```





