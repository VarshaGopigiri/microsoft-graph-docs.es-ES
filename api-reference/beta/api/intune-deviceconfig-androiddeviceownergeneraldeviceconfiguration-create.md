---
title: Crear androidDeviceOwnerGeneralDeviceConfiguration
description: Crear un nuevo objeto androidDeviceOwnerGeneralDeviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ff413da3f1c2d8062527f18efb38d74ecebdfa47
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27973520"
---
# <a name="create-androiddeviceownergeneraldeviceconfiguration"></a><span data-ttu-id="8da74-103">Crear androidDeviceOwnerGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8da74-103">Create androidDeviceOwnerGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="8da74-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8da74-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8da74-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8da74-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8da74-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8da74-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8da74-107">Crear un nuevo objeto [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="8da74-107">Create a new [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8da74-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8da74-108">Prerequisites</span></span>
<span data-ttu-id="8da74-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8da74-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8da74-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8da74-111">Permission type</span></span>|<span data-ttu-id="8da74-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8da74-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8da74-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8da74-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8da74-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8da74-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8da74-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8da74-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8da74-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8da74-116">Not supported.</span></span>|
|<span data-ttu-id="8da74-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8da74-117">Application</span></span>|<span data-ttu-id="8da74-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8da74-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8da74-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8da74-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="8da74-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8da74-120">Request headers</span></span>
|<span data-ttu-id="8da74-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8da74-121">Header</span></span>|<span data-ttu-id="8da74-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8da74-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8da74-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="8da74-123">Authorization</span></span>|<span data-ttu-id="8da74-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8da74-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8da74-125">Accept</span><span class="sxs-lookup"><span data-stu-id="8da74-125">Accept</span></span>|<span data-ttu-id="8da74-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8da74-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8da74-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8da74-127">Request body</span></span>
<span data-ttu-id="8da74-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto androidDeviceOwnerGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8da74-128">In the request body, supply a JSON representation for the androidDeviceOwnerGeneralDeviceConfiguration object.</span></span>

<span data-ttu-id="8da74-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el androidDeviceOwnerGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8da74-129">The following table shows the properties that are required when you create the androidDeviceOwnerGeneralDeviceConfiguration.</span></span>

|<span data-ttu-id="8da74-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8da74-130">Property</span></span>|<span data-ttu-id="8da74-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8da74-131">Type</span></span>|<span data-ttu-id="8da74-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8da74-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8da74-133">id</span><span class="sxs-lookup"><span data-stu-id="8da74-133">id</span></span>|<span data-ttu-id="8da74-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="8da74-134">String</span></span>|<span data-ttu-id="8da74-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8da74-135">Key of the entity.</span></span> <span data-ttu-id="8da74-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8da74-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8da74-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8da74-137">lastModifiedDateTime</span></span>|<span data-ttu-id="8da74-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8da74-138">DateTimeOffset</span></span>|<span data-ttu-id="8da74-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="8da74-139">DateTime the object was last modified.</span></span> <span data-ttu-id="8da74-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8da74-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8da74-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="8da74-141">roleScopeTagIds</span></span>|<span data-ttu-id="8da74-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="8da74-142">String collection</span></span>|<span data-ttu-id="8da74-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="8da74-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="8da74-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8da74-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8da74-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="8da74-145">supportsScopeTags</span></span>|<span data-ttu-id="8da74-146">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-146">Boolean</span></span>|<span data-ttu-id="8da74-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="8da74-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="8da74-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="8da74-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="8da74-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="8da74-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="8da74-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="8da74-150">This property is read-only.</span></span> <span data-ttu-id="8da74-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8da74-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8da74-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8da74-152">createdDateTime</span></span>|<span data-ttu-id="8da74-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8da74-153">DateTimeOffset</span></span>|<span data-ttu-id="8da74-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="8da74-154">DateTime the object was created.</span></span> <span data-ttu-id="8da74-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8da74-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8da74-156">descripción</span><span class="sxs-lookup"><span data-stu-id="8da74-156">description</span></span>|<span data-ttu-id="8da74-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="8da74-157">String</span></span>|<span data-ttu-id="8da74-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8da74-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="8da74-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8da74-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8da74-160">displayName</span><span class="sxs-lookup"><span data-stu-id="8da74-160">displayName</span></span>|<span data-ttu-id="8da74-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="8da74-161">String</span></span>|<span data-ttu-id="8da74-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8da74-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="8da74-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8da74-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8da74-164">version</span><span class="sxs-lookup"><span data-stu-id="8da74-164">version</span></span>|<span data-ttu-id="8da74-165">Int32</span><span class="sxs-lookup"><span data-stu-id="8da74-165">Int32</span></span>|<span data-ttu-id="8da74-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8da74-166">Version of the device configuration.</span></span> <span data-ttu-id="8da74-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8da74-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8da74-168">accountsBlockModification</span><span class="sxs-lookup"><span data-stu-id="8da74-168">accountsBlockModification</span></span>|<span data-ttu-id="8da74-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-169">Boolean</span></span>|<span data-ttu-id="8da74-170">Indica si está deshabilitada la opción Agregar o quitar cuentas de.</span><span class="sxs-lookup"><span data-stu-id="8da74-170">Indicates whether or not adding or removing accounts is disabled.</span></span>|
|<span data-ttu-id="8da74-171">appsAllowInstallFromUnknownSources</span><span class="sxs-lookup"><span data-stu-id="8da74-171">appsAllowInstallFromUnknownSources</span></span>|<span data-ttu-id="8da74-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-172">Boolean</span></span>|<span data-ttu-id="8da74-173">Indica si se permite al usuario para habilitar la configuración de orígenes desconocidos.</span><span class="sxs-lookup"><span data-stu-id="8da74-173">Indicates whether or not the user is allowed to enable to unknown sources setting.</span></span>|
|<span data-ttu-id="8da74-174">appsAutoUpdatePolicy</span><span class="sxs-lookup"><span data-stu-id="8da74-174">appsAutoUpdatePolicy</span></span>|[<span data-ttu-id="8da74-175">androidDeviceOwnerAppAutoUpdatePolicyType</span><span class="sxs-lookup"><span data-stu-id="8da74-175">androidDeviceOwnerAppAutoUpdatePolicyType</span></span>](../resources/intune-deviceconfig-androiddeviceownerappautoupdatepolicytype.md)|<span data-ttu-id="8da74-176">Indica el valor de la directiva de actualización automática de aplicación.</span><span class="sxs-lookup"><span data-stu-id="8da74-176">Indicates the value of the app auto update policy.</span></span> <span data-ttu-id="8da74-177">Los valores posibles son: `notConfigured`, `userChoice`, `never`, `wiFiOnly` y `always`.</span><span class="sxs-lookup"><span data-stu-id="8da74-177">Possible values are: `notConfigured`, `userChoice`, `never`, `wiFiOnly`, `always`.</span></span>|
|<span data-ttu-id="8da74-178">appsDefaultPermissionPolicy</span><span class="sxs-lookup"><span data-stu-id="8da74-178">appsDefaultPermissionPolicy</span></span>|[<span data-ttu-id="8da74-179">androidDeviceOwnerDefaultAppPermissionPolicyType</span><span class="sxs-lookup"><span data-stu-id="8da74-179">androidDeviceOwnerDefaultAppPermissionPolicyType</span></span>](../resources/intune-deviceconfig-androiddeviceownerdefaultapppermissionpolicytype.md)|<span data-ttu-id="8da74-180">Indica la directiva de permisos para las solicitudes de permisos en tiempo de ejecución si uno no se ha definido para la aplicación en concreto.</span><span class="sxs-lookup"><span data-stu-id="8da74-180">Indicates the permission policy for requests for runtime permissions if one is not defined for the app specifically.</span></span> <span data-ttu-id="8da74-181">Los valores posibles son: `deviceDefault`, `prompt`, `autoGrant` y `autoDeny`.</span><span class="sxs-lookup"><span data-stu-id="8da74-181">Possible values are: `deviceDefault`, `prompt`, `autoGrant`, `autoDeny`.</span></span>|
|<span data-ttu-id="8da74-182">bluetoothBlockConfiguration</span><span class="sxs-lookup"><span data-stu-id="8da74-182">bluetoothBlockConfiguration</span></span>|<span data-ttu-id="8da74-183">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-183">Boolean</span></span>|<span data-ttu-id="8da74-184">Indica si se deben bloquear un usuario desde la configuración de bluetooth.</span><span class="sxs-lookup"><span data-stu-id="8da74-184">Indicates whether or not to block a user from configuring bluetooth.</span></span>|
|<span data-ttu-id="8da74-185">bluetoothBlockContactSharing</span><span class="sxs-lookup"><span data-stu-id="8da74-185">bluetoothBlockContactSharing</span></span>|<span data-ttu-id="8da74-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-186">Boolean</span></span>|<span data-ttu-id="8da74-187">Indica si se va a bloquear un usuario de uso compartido de contactos a través de bluetooth o no.</span><span class="sxs-lookup"><span data-stu-id="8da74-187">Indicates whether or not to block a user from sharing contacts via bluetooth.</span></span>|
|<span data-ttu-id="8da74-188">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="8da74-188">cameraBlocked</span></span>|<span data-ttu-id="8da74-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-189">Boolean</span></span>|<span data-ttu-id="8da74-190">Indica si se va a deshabilitar el uso de la cámara o no.</span><span class="sxs-lookup"><span data-stu-id="8da74-190">Indicates whether or not to disable the use of the camera.</span></span>|
|<span data-ttu-id="8da74-191">cellularBlockWiFiTethering</span><span class="sxs-lookup"><span data-stu-id="8da74-191">cellularBlockWiFiTethering</span></span>|<span data-ttu-id="8da74-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-192">Boolean</span></span>|<span data-ttu-id="8da74-193">Indica si se va a bloquear el tethering Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="8da74-193">Indicates whether or not to block Wi-Fi tethering.</span></span>|
|<span data-ttu-id="8da74-194">dataRoamingBlocked</span><span class="sxs-lookup"><span data-stu-id="8da74-194">dataRoamingBlocked</span></span>|<span data-ttu-id="8da74-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-195">Boolean</span></span>|<span data-ttu-id="8da74-196">Indica si se deben bloquear un usuario de movilidad de datos.</span><span class="sxs-lookup"><span data-stu-id="8da74-196">Indicates whether or not to block a user from data roaming.</span></span>|
|<span data-ttu-id="8da74-197">dateTimeConfigurationBlocked</span><span class="sxs-lookup"><span data-stu-id="8da74-197">dateTimeConfigurationBlocked</span></span>|<span data-ttu-id="8da74-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-198">Boolean</span></span>|<span data-ttu-id="8da74-199">Indica si se deben bloquear el usuario cambie manualmente la fecha o la hora en el dispositivo</span><span class="sxs-lookup"><span data-stu-id="8da74-199">Indicates whether or not to block the user from manually changing the date or time on the device</span></span>|
|<span data-ttu-id="8da74-200">factoryResetDeviceAdministratorEmails</span><span class="sxs-lookup"><span data-stu-id="8da74-200">factoryResetDeviceAdministratorEmails</span></span>|<span data-ttu-id="8da74-201">Colección String</span><span class="sxs-lookup"><span data-stu-id="8da74-201">String collection</span></span>|<span data-ttu-id="8da74-202">Lista de correos electrónicos de la cuenta de Google que serán necesarios para autenticar una vez fábrica restablecer antes de que se puede configurar un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8da74-202">List of Google account emails that will be required to authenticate after a device is factory reset before it can be set up.</span></span>|
|<span data-ttu-id="8da74-203">factoryResetBlocked</span><span class="sxs-lookup"><span data-stu-id="8da74-203">factoryResetBlocked</span></span>|<span data-ttu-id="8da74-204">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-204">Boolean</span></span>|<span data-ttu-id="8da74-205">Indica si está deshabilitada la opción de restablecimiento de fábrica en configuración.</span><span class="sxs-lookup"><span data-stu-id="8da74-205">Indicates whether or not the factory reset option in settings is disabled.</span></span>|
|<span data-ttu-id="8da74-206">kioskModeApps</span><span class="sxs-lookup"><span data-stu-id="8da74-206">kioskModeApps</span></span>|<span data-ttu-id="8da74-207">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="8da74-207">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="8da74-208">Una lista de aplicaciones administradas que se mostrará cuando el dispositivo está en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="8da74-208">A list of managed apps that will be shown when the device is in Kiosk Mode.</span></span> <span data-ttu-id="8da74-209">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="8da74-209">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="8da74-210">microphoneForceMute</span><span class="sxs-lookup"><span data-stu-id="8da74-210">microphoneForceMute</span></span>|<span data-ttu-id="8da74-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-211">Boolean</span></span>|<span data-ttu-id="8da74-212">Indica si se deben bloquear del audio del micrófono en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8da74-212">Indicates whether or not to block unmuting the microphone on the device.</span></span>|
|<span data-ttu-id="8da74-213">networkEscapeHatchAllowed</span><span class="sxs-lookup"><span data-stu-id="8da74-213">networkEscapeHatchAllowed</span></span>|<span data-ttu-id="8da74-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-214">Boolean</span></span>|<span data-ttu-id="8da74-215">Indica si el dispositivo permitirá que se conectan a una conexión de red temporal en tiempo de inicio.</span><span class="sxs-lookup"><span data-stu-id="8da74-215">Indicates whether or not the device will allow connecting to a temporary network connection at boot time.</span></span>|
|<span data-ttu-id="8da74-216">nfcBlockOutgoingBeam</span><span class="sxs-lookup"><span data-stu-id="8da74-216">nfcBlockOutgoingBeam</span></span>|<span data-ttu-id="8da74-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-217">Boolean</span></span>|<span data-ttu-id="8da74-218">Indica si se deben bloquear carretera saliente CNC.</span><span class="sxs-lookup"><span data-stu-id="8da74-218">Indicates whether or not to block NFC outgoing beam.</span></span>|
|<span data-ttu-id="8da74-219">passwordBlockKeyguard</span><span class="sxs-lookup"><span data-stu-id="8da74-219">passwordBlockKeyguard</span></span>|<span data-ttu-id="8da74-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-220">Boolean</span></span>|<span data-ttu-id="8da74-221">Indica si está deshabilitada la keyguard.</span><span class="sxs-lookup"><span data-stu-id="8da74-221">Indicates whether or not the keyguard is disabled.</span></span>|
|<span data-ttu-id="8da74-222">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="8da74-222">passwordExpirationDays</span></span>|<span data-ttu-id="8da74-223">Int32</span><span class="sxs-lookup"><span data-stu-id="8da74-223">Int32</span></span>|<span data-ttu-id="8da74-224">Indica la cantidad de tiempo en segundos que se puede establecer una contraseña para antes de que caduque y se le solicitará una contraseña nueva.</span><span class="sxs-lookup"><span data-stu-id="8da74-224">Indicates the amount of time in seconds that a password can be set for before it expires and a new password will be required.</span></span> <span data-ttu-id="8da74-225">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="8da74-225">Valid values 1 to 365</span></span>|
|<span data-ttu-id="8da74-226">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="8da74-226">passwordMinimumLength</span></span>|<span data-ttu-id="8da74-227">Int32</span><span class="sxs-lookup"><span data-stu-id="8da74-227">Int32</span></span>|<span data-ttu-id="8da74-228">Indica la longitud mínima de la contraseña requerida en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8da74-228">Indicates the minimum length of the password required on the device.</span></span> <span data-ttu-id="8da74-229">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="8da74-229">Valid values 4 to 16</span></span>|
|<span data-ttu-id="8da74-230">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="8da74-230">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="8da74-231">Int32</span><span class="sxs-lookup"><span data-stu-id="8da74-231">Int32</span></span>|<span data-ttu-id="8da74-232">Milisegundos de inactividad antes de agote el tiempo de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="8da74-232">Milliseconds of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="8da74-233">passwordPreviousPasswordCountToBlock</span><span class="sxs-lookup"><span data-stu-id="8da74-233">passwordPreviousPasswordCountToBlock</span></span>|<span data-ttu-id="8da74-234">Int32</span><span class="sxs-lookup"><span data-stu-id="8da74-234">Int32</span></span>|<span data-ttu-id="8da74-235">Indica la longitud del historial de contraseñas, donde el usuario no podrá escribir una nueva contraseña que es el mismo que el de las contraseñas en el historial.</span><span class="sxs-lookup"><span data-stu-id="8da74-235">Indicates the length of password history, where the user will not be able to enter a new password that is the same as any password in the history.</span></span> <span data-ttu-id="8da74-236">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="8da74-236">Valid values 0 to 24</span></span>|
|<span data-ttu-id="8da74-237">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="8da74-237">passwordRequiredType</span></span>|[<span data-ttu-id="8da74-238">androidDeviceOwnerRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="8da74-238">androidDeviceOwnerRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androiddeviceownerrequiredpasswordtype.md)|<span data-ttu-id="8da74-239">Indica la calidad mínima de la contraseña necesaria en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8da74-239">Indicates the minimum password quality required on the device.</span></span> <span data-ttu-id="8da74-240">Los valores posibles son: `deviceDefault`, `required`, `numeric`, `numericComplex`, `alphabetic`, `alphanumeric` y `alphanumericWithSymbols`.</span><span class="sxs-lookup"><span data-stu-id="8da74-240">Possible values are: `deviceDefault`, `required`, `numeric`, `numericComplex`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`.</span></span>|
|<span data-ttu-id="8da74-241">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="8da74-241">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="8da74-242">Int32</span><span class="sxs-lookup"><span data-stu-id="8da74-242">Int32</span></span>|<span data-ttu-id="8da74-243">Indica el número de veces que un usuario puede escribir una contraseña incorrecta antes de que se borre el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8da74-243">Indicates the number of times a user can enter an incorrect password before the device is wiped.</span></span> <span data-ttu-id="8da74-244">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="8da74-244">Valid values 4 to 11</span></span>|
|<span data-ttu-id="8da74-245">safeBootBlocked</span><span class="sxs-lookup"><span data-stu-id="8da74-245">safeBootBlocked</span></span>|<span data-ttu-id="8da74-246">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-246">Boolean</span></span>|<span data-ttu-id="8da74-247">Indica si al reiniciar que el dispositivo en Inicio seguro está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8da74-247">Indicates whether or not rebooting the device into safe boot is disabled.</span></span>|
|<span data-ttu-id="8da74-248">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="8da74-248">screenCaptureBlocked</span></span>|<span data-ttu-id="8da74-249">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-249">Boolean</span></span>|<span data-ttu-id="8da74-250">Indica si se va a deshabilitar la capacidad de realizar capturas de pantalla o no.</span><span class="sxs-lookup"><span data-stu-id="8da74-250">Indicates whether or not to disable the capability to take screenshots.</span></span>|
|<span data-ttu-id="8da74-251">securityAllowDebuggingFeatures</span><span class="sxs-lookup"><span data-stu-id="8da74-251">securityAllowDebuggingFeatures</span></span>|<span data-ttu-id="8da74-252">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-252">Boolean</span></span>|<span data-ttu-id="8da74-253">Indica si desea impedir que el usuario de habilitación de características de depuración en el dispositivo o no.</span><span class="sxs-lookup"><span data-stu-id="8da74-253">Indicates whether or not to block the user from enabling debugging features on the device.</span></span>|
|<span data-ttu-id="8da74-254">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="8da74-254">securityRequireVerifyApps</span></span>|<span data-ttu-id="8da74-255">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-255">Boolean</span></span>|<span data-ttu-id="8da74-256">Indica si o no comprobar aplicaciones es necesario.</span><span class="sxs-lookup"><span data-stu-id="8da74-256">Indicates whether or not verify apps is required.</span></span>|
|<span data-ttu-id="8da74-257">statusBarBlocked</span><span class="sxs-lookup"><span data-stu-id="8da74-257">statusBarBlocked</span></span>|<span data-ttu-id="8da74-258">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-258">Boolean</span></span>|<span data-ttu-id="8da74-259">Indica si el estado o barra está deshabilitada, incluidas las notificaciones, la configuración rápida y otros superposiciones de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8da74-259">Indicates whether or the status bar is disabled, including notifications, quick settings and other screen overlays.</span></span>|
|<span data-ttu-id="8da74-260">stayOnModes</span><span class="sxs-lookup"><span data-stu-id="8da74-260">stayOnModes</span></span>|<span data-ttu-id="8da74-261">colección de [androidDeviceOwnerBatteryPluggedMode](../resources/intune-deviceconfig-androiddeviceownerbatterypluggedmode.md)</span><span class="sxs-lookup"><span data-stu-id="8da74-261">[androidDeviceOwnerBatteryPluggedMode](../resources/intune-deviceconfig-androiddeviceownerbatterypluggedmode.md) collection</span></span>|<span data-ttu-id="8da74-262">Lista de los modos en que la pantalla del dispositivo permanecerá enciende.</span><span class="sxs-lookup"><span data-stu-id="8da74-262">List of modes in which the device's display will stay powered-on.</span></span> <span data-ttu-id="8da74-263">Esta colección puede contener un máximo de 4 elementos.</span><span class="sxs-lookup"><span data-stu-id="8da74-263">This collection can contain a maximum of 4 elements.</span></span> <span data-ttu-id="8da74-264">Los valores posibles son: `notConfigured`, `ac`, `usb` y `wireless`.</span><span class="sxs-lookup"><span data-stu-id="8da74-264">Possible values are: `notConfigured`, `ac`, `usb`, `wireless`.</span></span>|
|<span data-ttu-id="8da74-265">storageAllowUsb</span><span class="sxs-lookup"><span data-stu-id="8da74-265">storageAllowUsb</span></span>|<span data-ttu-id="8da74-266">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-266">Boolean</span></span>|<span data-ttu-id="8da74-267">Indica si se debe o no permitir el almacenamiento masivo USB.</span><span class="sxs-lookup"><span data-stu-id="8da74-267">Indicates whether or not to allow USB mass storage.</span></span>|
|<span data-ttu-id="8da74-268">storageBlockExternalMedia</span><span class="sxs-lookup"><span data-stu-id="8da74-268">storageBlockExternalMedia</span></span>|<span data-ttu-id="8da74-269">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-269">Boolean</span></span>|<span data-ttu-id="8da74-270">Indica si se deben bloquear medios externos.</span><span class="sxs-lookup"><span data-stu-id="8da74-270">Indicates whether or not to block external media.</span></span>|
|<span data-ttu-id="8da74-271">storageBlockUsbFileTransfer</span><span class="sxs-lookup"><span data-stu-id="8da74-271">storageBlockUsbFileTransfer</span></span>|<span data-ttu-id="8da74-272">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-272">Boolean</span></span>|<span data-ttu-id="8da74-273">Indica si se deben bloquear la transferencia de archivos USB.</span><span class="sxs-lookup"><span data-stu-id="8da74-273">Indicates whether or not to block USB file transfer.</span></span>|
|<span data-ttu-id="8da74-274">systemUpdateWindowStartMinutesAfterMidnight</span><span class="sxs-lookup"><span data-stu-id="8da74-274">systemUpdateWindowStartMinutesAfterMidnight</span></span>|<span data-ttu-id="8da74-275">Int32</span><span class="sxs-lookup"><span data-stu-id="8da74-275">Int32</span></span>|<span data-ttu-id="8da74-276">Indica el número de minutos después de la medianoche que inicia la ventana de actualización del sistema.</span><span class="sxs-lookup"><span data-stu-id="8da74-276">Indicates the number of minutes after midnight that the system update window starts.</span></span> <span data-ttu-id="8da74-277">Valores válidos 0 y 1440.</span><span class="sxs-lookup"><span data-stu-id="8da74-277">Valid values 0 to 1440</span></span>|
|<span data-ttu-id="8da74-278">systemUpdateWindowEndMinutesAfterMidnight</span><span class="sxs-lookup"><span data-stu-id="8da74-278">systemUpdateWindowEndMinutesAfterMidnight</span></span>|<span data-ttu-id="8da74-279">Int32</span><span class="sxs-lookup"><span data-stu-id="8da74-279">Int32</span></span>|<span data-ttu-id="8da74-280">Indica el número de minutos después de la medianoche que termina la ventana de actualización del sistema.</span><span class="sxs-lookup"><span data-stu-id="8da74-280">Indicates the number of minutes after midnight that the system update window ends.</span></span> <span data-ttu-id="8da74-281">Valores válidos 0 y 1440.</span><span class="sxs-lookup"><span data-stu-id="8da74-281">Valid values 0 to 1440</span></span>|
|<span data-ttu-id="8da74-282">systemUpdateInstallType</span><span class="sxs-lookup"><span data-stu-id="8da74-282">systemUpdateInstallType</span></span>|[<span data-ttu-id="8da74-283">androidDeviceOwnerSystemUpdateInstallType</span><span class="sxs-lookup"><span data-stu-id="8da74-283">androidDeviceOwnerSystemUpdateInstallType</span></span>](../resources/intune-deviceconfig-androiddeviceownersystemupdateinstalltype.md)|<span data-ttu-id="8da74-284">El tipo de configuración de la actualización del sistema.</span><span class="sxs-lookup"><span data-stu-id="8da74-284">The type of system update configuration.</span></span> <span data-ttu-id="8da74-285">Los valores posibles son: `deviceDefault`, `postpone`, `windowed` y `automatic`.</span><span class="sxs-lookup"><span data-stu-id="8da74-285">Possible values are: `deviceDefault`, `postpone`, `windowed`, `automatic`.</span></span>|
|<span data-ttu-id="8da74-286">usersBlockAdd</span><span class="sxs-lookup"><span data-stu-id="8da74-286">usersBlockAdd</span></span>|<span data-ttu-id="8da74-287">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-287">Boolean</span></span>|<span data-ttu-id="8da74-288">Indica si está deshabilitada la opción Agregar usuarios y perfiles de.</span><span class="sxs-lookup"><span data-stu-id="8da74-288">Indicates whether or not adding users and profiles is disabled.</span></span>|
|<span data-ttu-id="8da74-289">usersBlockRemove</span><span class="sxs-lookup"><span data-stu-id="8da74-289">usersBlockRemove</span></span>|<span data-ttu-id="8da74-290">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-290">Boolean</span></span>|<span data-ttu-id="8da74-291">Indica si desea deshabilitar la eliminación de otros usuarios desde el dispositivo o no.</span><span class="sxs-lookup"><span data-stu-id="8da74-291">Indicates whether or not to disable removing other users from the device.</span></span>|
|<span data-ttu-id="8da74-292">volumeBlockAdjustment</span><span class="sxs-lookup"><span data-stu-id="8da74-292">volumeBlockAdjustment</span></span>|<span data-ttu-id="8da74-293">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-293">Boolean</span></span>|<span data-ttu-id="8da74-294">Indica si o no ajustar que el volumen principal está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="8da74-294">Indicates whether or not adjusting the master volume is disabled.</span></span>|
|<span data-ttu-id="8da74-295">wifiBlockEditConfigurations</span><span class="sxs-lookup"><span data-stu-id="8da74-295">wifiBlockEditConfigurations</span></span>|<span data-ttu-id="8da74-296">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-296">Boolean</span></span>|<span data-ttu-id="8da74-297">Indica si desea impedir que el usuario de edición de la configuración de conexión wifi o no.</span><span class="sxs-lookup"><span data-stu-id="8da74-297">Indicates whether or not to block the user from editing the wifi connection settings.</span></span>|
|<span data-ttu-id="8da74-298">wifiBlockEditPolicyDefinedConfigurations</span><span class="sxs-lookup"><span data-stu-id="8da74-298">wifiBlockEditPolicyDefinedConfigurations</span></span>|<span data-ttu-id="8da74-299">Booleano</span><span class="sxs-lookup"><span data-stu-id="8da74-299">Boolean</span></span>|<span data-ttu-id="8da74-300">Indica si desea impedir que el usuario acaba las redes definidas por la directiva de edición o no.</span><span class="sxs-lookup"><span data-stu-id="8da74-300">Indicates whether or not to block the user from editing just the networks defined by the policy.</span></span>|



## <a name="response"></a><span data-ttu-id="8da74-301">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8da74-301">Response</span></span>
<span data-ttu-id="8da74-302">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8da74-302">If successful, this method returns a `201 Created` response code and a [androidDeviceOwnerGeneralDeviceConfiguration](../resources/intune-deviceconfig-androiddeviceownergeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8da74-303">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8da74-303">Example</span></span>
### <a name="request"></a><span data-ttu-id="8da74-304">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8da74-304">Request</span></span>
<span data-ttu-id="8da74-305">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8da74-305">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 2156

{
  "@odata.type": "#microsoft.graph.androidDeviceOwnerGeneralDeviceConfiguration",
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

### <a name="response"></a><span data-ttu-id="8da74-306">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8da74-306">Response</span></span>
<span data-ttu-id="8da74-p123">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8da74-p123">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





