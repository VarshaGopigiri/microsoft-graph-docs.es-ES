---
title: Actualizar androidGeneralDeviceConfiguration
description: Actualice las propiedades de un objeto androidGeneralDeviceConfiguration.
author: tfitzmac
ms.openlocfilehash: a495a071577798597685d1ff15e1705968c32d31
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27326883"
---
# <a name="update-androidgeneraldeviceconfiguration"></a><span data-ttu-id="25e0e-103">Actualizar androidGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="25e0e-103">Update androidGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="25e0e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="25e0e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="25e0e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="25e0e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="25e0e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="25e0e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="25e0e-107">Actualice las propiedades de un objeto [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="25e0e-107">Update the properties of a [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="25e0e-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="25e0e-108">Prerequisites</span></span>
<span data-ttu-id="25e0e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="25e0e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="25e0e-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="25e0e-111">Permission type</span></span>|<span data-ttu-id="25e0e-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="25e0e-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="25e0e-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="25e0e-113">Delegated (work or school account)</span></span>|<span data-ttu-id="25e0e-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="25e0e-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="25e0e-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="25e0e-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="25e0e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25e0e-116">Not supported.</span></span>|
|<span data-ttu-id="25e0e-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="25e0e-117">Application</span></span>|<span data-ttu-id="25e0e-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25e0e-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="25e0e-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="25e0e-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="25e0e-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="25e0e-120">Request headers</span></span>
|<span data-ttu-id="25e0e-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="25e0e-121">Header</span></span>|<span data-ttu-id="25e0e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="25e0e-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="25e0e-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="25e0e-123">Authorization</span></span>|<span data-ttu-id="25e0e-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="25e0e-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="25e0e-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="25e0e-125">Accept</span></span>|<span data-ttu-id="25e0e-126">application/json</span><span class="sxs-lookup"><span data-stu-id="25e0e-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="25e0e-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="25e0e-127">Request body</span></span>
<span data-ttu-id="25e0e-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="25e0e-128">In the request body, supply a JSON representation for the [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md) object.</span></span>

<span data-ttu-id="25e0e-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="25e0e-129">The following table shows the properties that are required when you create the [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md).</span></span>

|<span data-ttu-id="25e0e-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="25e0e-130">Property</span></span>|<span data-ttu-id="25e0e-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="25e0e-131">Type</span></span>|<span data-ttu-id="25e0e-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="25e0e-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="25e0e-133">id</span><span class="sxs-lookup"><span data-stu-id="25e0e-133">id</span></span>|<span data-ttu-id="25e0e-134">String</span><span class="sxs-lookup"><span data-stu-id="25e0e-134">String</span></span>|<span data-ttu-id="25e0e-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="25e0e-135">Key of the entity.</span></span> <span data-ttu-id="25e0e-136">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-136">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25e0e-137">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="25e0e-137">lastModifiedDateTime</span></span>|<span data-ttu-id="25e0e-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="25e0e-138">DateTimeOffset</span></span>|<span data-ttu-id="25e0e-139">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="25e0e-139">DateTime the object was last modified.</span></span> <span data-ttu-id="25e0e-140">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-140">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25e0e-141">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="25e0e-141">roleScopeTagIds</span></span>|<span data-ttu-id="25e0e-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="25e0e-142">String collection</span></span>|<span data-ttu-id="25e0e-143">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="25e0e-143">List of Scope Tags for this Entity instance.</span></span> <span data-ttu-id="25e0e-144">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-144">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25e0e-145">supportsScopeTags</span><span class="sxs-lookup"><span data-stu-id="25e0e-145">supportsScopeTags</span></span>|<span data-ttu-id="25e0e-146">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-146">Boolean</span></span>|<span data-ttu-id="25e0e-147">Indica si la configuración del dispositivo subyacente admite la asignación de etiquetas de ámbito.</span><span class="sxs-lookup"><span data-stu-id="25e0e-147">Indicates whether or not the underlying Device Configuration supports the assignment of scope tags.</span></span> <span data-ttu-id="25e0e-148">No se permite la asignación a la propiedad ScopeTags cuando este valor es false y entidades no estará visibles para los usuarios con ámbito.</span><span class="sxs-lookup"><span data-stu-id="25e0e-148">Assigning to the ScopeTags property is not allowed when this value is false and entities will not be visible to scoped users.</span></span> <span data-ttu-id="25e0e-149">Esto se produce para las directivas de heredado creadas en Silverlight y se puede resolver por eliminar y volver a crear la directiva en el Portal de Azure.</span><span class="sxs-lookup"><span data-stu-id="25e0e-149">This occurs for Legacy policies created in Silverlight and can be resolved by deleting and recreating the policy in the Azure Portal.</span></span> <span data-ttu-id="25e0e-150">Esta propiedad es de sólo lectura.</span><span class="sxs-lookup"><span data-stu-id="25e0e-150">This property is read-only.</span></span> <span data-ttu-id="25e0e-151">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-151">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25e0e-152">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="25e0e-152">createdDateTime</span></span>|<span data-ttu-id="25e0e-153">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="25e0e-153">DateTimeOffset</span></span>|<span data-ttu-id="25e0e-154">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="25e0e-154">DateTime the object was created.</span></span> <span data-ttu-id="25e0e-155">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-155">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25e0e-156">descripción</span><span class="sxs-lookup"><span data-stu-id="25e0e-156">description</span></span>|<span data-ttu-id="25e0e-157">String</span><span class="sxs-lookup"><span data-stu-id="25e0e-157">String</span></span>|<span data-ttu-id="25e0e-158">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25e0e-158">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="25e0e-159">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-159">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25e0e-160">displayName</span><span class="sxs-lookup"><span data-stu-id="25e0e-160">displayName</span></span>|<span data-ttu-id="25e0e-161">String</span><span class="sxs-lookup"><span data-stu-id="25e0e-161">String</span></span>|<span data-ttu-id="25e0e-162">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25e0e-162">Admin provided name of the device configuration.</span></span> <span data-ttu-id="25e0e-163">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-163">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25e0e-164">version</span><span class="sxs-lookup"><span data-stu-id="25e0e-164">version</span></span>|<span data-ttu-id="25e0e-165">Int32</span><span class="sxs-lookup"><span data-stu-id="25e0e-165">Int32</span></span>|<span data-ttu-id="25e0e-166">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25e0e-166">Version of the device configuration.</span></span> <span data-ttu-id="25e0e-167">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-167">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="25e0e-168">appsBlockClipboardSharing</span><span class="sxs-lookup"><span data-stu-id="25e0e-168">appsBlockClipboardSharing</span></span>|<span data-ttu-id="25e0e-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="25e0e-169">Boolean</span></span>|<span data-ttu-id="25e0e-170">Indica si se va a bloquear el uso compartido del Portapapeles para copiar y pegar entre aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="25e0e-170">Indicates whether or not to block clipboard sharing to copy and paste between applications.</span></span>|
|<span data-ttu-id="25e0e-171">appsBlockCopyPaste</span><span class="sxs-lookup"><span data-stu-id="25e0e-171">appsBlockCopyPaste</span></span>|<span data-ttu-id="25e0e-172">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-172">Boolean</span></span>|<span data-ttu-id="25e0e-173">Indica si se va a impedir copiar y pegar en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="25e0e-173">Indicates whether or not to block copy and paste within applications.</span></span>|
|<span data-ttu-id="25e0e-174">appsBlockYouTube</span><span class="sxs-lookup"><span data-stu-id="25e0e-174">appsBlockYouTube</span></span>|<span data-ttu-id="25e0e-175">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-175">Boolean</span></span>|<span data-ttu-id="25e0e-176">Indica si se va a bloquear la aplicación YouTube.</span><span class="sxs-lookup"><span data-stu-id="25e0e-176">Indicates whether or not to block the YouTube app.</span></span>|
|<span data-ttu-id="25e0e-177">bluetoothBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-177">bluetoothBlocked</span></span>|<span data-ttu-id="25e0e-178">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-178">Boolean</span></span>|<span data-ttu-id="25e0e-179">Indica si se va a bloquear Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="25e0e-179">Indicates whether or not to block Bluetooth.</span></span>|
|<span data-ttu-id="25e0e-180">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-180">cameraBlocked</span></span>|<span data-ttu-id="25e0e-181">Booleano</span><span class="sxs-lookup"><span data-stu-id="25e0e-181">Boolean</span></span>|<span data-ttu-id="25e0e-182">Indica si se va a bloquear el uso de la cámara.</span><span class="sxs-lookup"><span data-stu-id="25e0e-182">Indicates whether or not to block the use of the camera.</span></span>|
|<span data-ttu-id="25e0e-183">cellularBlockDataRoaming</span><span class="sxs-lookup"><span data-stu-id="25e0e-183">cellularBlockDataRoaming</span></span>|<span data-ttu-id="25e0e-184">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-184">Boolean</span></span>|<span data-ttu-id="25e0e-185">Indica si se va a bloquear la itinerancia de datos.</span><span class="sxs-lookup"><span data-stu-id="25e0e-185">Indicates whether or not to block data roaming.</span></span>|
|<span data-ttu-id="25e0e-186">cellularBlockMessaging</span><span class="sxs-lookup"><span data-stu-id="25e0e-186">cellularBlockMessaging</span></span>|<span data-ttu-id="25e0e-187">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-187">Boolean</span></span>|<span data-ttu-id="25e0e-188">Indica si se va a bloquear la mensajería SMS/MMS.</span><span class="sxs-lookup"><span data-stu-id="25e0e-188">Indicates whether or not to block SMS/MMS messaging.</span></span>|
|<span data-ttu-id="25e0e-189">cellularBlockVoiceRoaming</span><span class="sxs-lookup"><span data-stu-id="25e0e-189">cellularBlockVoiceRoaming</span></span>|<span data-ttu-id="25e0e-190">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-190">Boolean</span></span>|<span data-ttu-id="25e0e-191">Indica si se va a bloquear la itinerancia de voz.</span><span class="sxs-lookup"><span data-stu-id="25e0e-191">Indicates whether or not to block voice roaming.</span></span>|
|<span data-ttu-id="25e0e-192">cellularBlockWiFiTethering</span><span class="sxs-lookup"><span data-stu-id="25e0e-192">cellularBlockWiFiTethering</span></span>|<span data-ttu-id="25e0e-193">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-193">Boolean</span></span>|<span data-ttu-id="25e0e-194">Indica si se va a bloquear la sincronización de tethering Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="25e0e-194">Indicates whether or not to block syncing Wi-Fi tethering.</span></span>|
|<span data-ttu-id="25e0e-195">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="25e0e-195">compliantAppsList</span></span>|<span data-ttu-id="25e0e-196">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-196">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="25e0e-197">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="25e0e-197">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="25e0e-198">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="25e0e-198">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="25e0e-199">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="25e0e-199">compliantAppListType</span></span>|[<span data-ttu-id="25e0e-200">appListType</span><span class="sxs-lookup"><span data-stu-id="25e0e-200">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="25e0e-201">Tipo de lista que se encuentra en la CompliantAppsList.</span><span class="sxs-lookup"><span data-stu-id="25e0e-201">Type of list that is in the CompliantAppsList.</span></span> <span data-ttu-id="25e0e-202">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="25e0e-202">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="25e0e-203">diagnosticDataBlockSubmission</span><span class="sxs-lookup"><span data-stu-id="25e0e-203">diagnosticDataBlockSubmission</span></span>|<span data-ttu-id="25e0e-204">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-204">Boolean</span></span>|<span data-ttu-id="25e0e-205">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="25e0e-205">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="25e0e-206">locationServicesBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-206">locationServicesBlocked</span></span>|<span data-ttu-id="25e0e-207">Booleano</span><span class="sxs-lookup"><span data-stu-id="25e0e-207">Boolean</span></span>|<span data-ttu-id="25e0e-208">Indica si se van a bloquear los servicios de ubicación.</span><span class="sxs-lookup"><span data-stu-id="25e0e-208">Indicates whether or not to block location services.</span></span>|
|<span data-ttu-id="25e0e-209">googleAccountBlockAutoSync</span><span class="sxs-lookup"><span data-stu-id="25e0e-209">googleAccountBlockAutoSync</span></span>|<span data-ttu-id="25e0e-210">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-210">Boolean</span></span>|<span data-ttu-id="25e0e-211">Indica si se va a bloquear la sincronización automática de cuentas de Google.</span><span class="sxs-lookup"><span data-stu-id="25e0e-211">Indicates whether or not to block Google account auto sync.</span></span>|
|<span data-ttu-id="25e0e-212">googlePlayStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-212">googlePlayStoreBlocked</span></span>|<span data-ttu-id="25e0e-213">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-213">Boolean</span></span>|<span data-ttu-id="25e0e-214">Indica si se va a bloquear la aplicación Google Play Store.</span><span class="sxs-lookup"><span data-stu-id="25e0e-214">Indicates whether or not to block the Google Play store.</span></span>|
|<span data-ttu-id="25e0e-215">kioskModeBlockSleepButton</span><span class="sxs-lookup"><span data-stu-id="25e0e-215">kioskModeBlockSleepButton</span></span>|<span data-ttu-id="25e0e-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-216">Boolean</span></span>|<span data-ttu-id="25e0e-217">Indica si se va a bloquear el botón de suspensión de pantalla durante el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="25e0e-217">Indicates whether or not to block the screen sleep button while in Kiosk Mode.</span></span>|
|<span data-ttu-id="25e0e-218">kioskModeBlockVolumeButtons</span><span class="sxs-lookup"><span data-stu-id="25e0e-218">kioskModeBlockVolumeButtons</span></span>|<span data-ttu-id="25e0e-219">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-219">Boolean</span></span>|<span data-ttu-id="25e0e-220">Indica si se van a bloquear los botones de volumen durante el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="25e0e-220">Indicates whether or not to block the volume buttons while in Kiosk Mode.</span></span>|
|<span data-ttu-id="25e0e-221">dateAndTimeBlockChanges</span><span class="sxs-lookup"><span data-stu-id="25e0e-221">dateAndTimeBlockChanges</span></span>|<span data-ttu-id="25e0e-222">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-222">Boolean</span></span>|<span data-ttu-id="25e0e-223">Indica si se deben bloquear cambiantes de fecha y hora en el modo de KNOX.</span><span class="sxs-lookup"><span data-stu-id="25e0e-223">Indicates whether or not to block changing date and time while in KNOX Mode.</span></span>|
|<span data-ttu-id="25e0e-224">kioskModeApps</span><span class="sxs-lookup"><span data-stu-id="25e0e-224">kioskModeApps</span></span>|<span data-ttu-id="25e0e-225">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-225">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="25e0e-226">Lista de aplicaciones que se podrán ejecutar cuando el dispositivo esté en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="25e0e-226">A list of apps that will be allowed to run when the device is in Kiosk Mode.</span></span> <span data-ttu-id="25e0e-227">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="25e0e-227">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="25e0e-228">nfcBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-228">nfcBlocked</span></span>|<span data-ttu-id="25e0e-229">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-229">Boolean</span></span>|<span data-ttu-id="25e0e-230">Indica si se va a bloquear la transmisión de datos en proximidad.</span><span class="sxs-lookup"><span data-stu-id="25e0e-230">Indicates whether or not to block Near-Field Communication.</span></span>|
|<span data-ttu-id="25e0e-231">passwordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="25e0e-231">passwordBlockFingerprintUnlock</span></span>|<span data-ttu-id="25e0e-232">Booleano</span><span class="sxs-lookup"><span data-stu-id="25e0e-232">Boolean</span></span>|<span data-ttu-id="25e0e-233">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="25e0e-233">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="25e0e-234">passwordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="25e0e-234">passwordBlockTrustAgents</span></span>|<span data-ttu-id="25e0e-235">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-235">Boolean</span></span>|<span data-ttu-id="25e0e-236">Indica si se van a bloquear Smart Lock y otros agentes de confianza.</span><span class="sxs-lookup"><span data-stu-id="25e0e-236">Indicates whether or not to block Smart Lock and other trust agents.</span></span>|
|<span data-ttu-id="25e0e-237">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="25e0e-237">passwordExpirationDays</span></span>|<span data-ttu-id="25e0e-238">Int32</span><span class="sxs-lookup"><span data-stu-id="25e0e-238">Int32</span></span>|<span data-ttu-id="25e0e-239">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="25e0e-239">Number of days before the password expires.</span></span> <span data-ttu-id="25e0e-240">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="25e0e-240">Valid values 1 to 365</span></span>|
|<span data-ttu-id="25e0e-241">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="25e0e-241">passwordMinimumLength</span></span>|<span data-ttu-id="25e0e-242">Int32</span><span class="sxs-lookup"><span data-stu-id="25e0e-242">Int32</span></span>|<span data-ttu-id="25e0e-243">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="25e0e-243">Minimum length of passwords.</span></span> <span data-ttu-id="25e0e-244">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="25e0e-244">Valid values 4 to 16</span></span>|
|<span data-ttu-id="25e0e-245">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="25e0e-245">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="25e0e-246">Int32</span><span class="sxs-lookup"><span data-stu-id="25e0e-246">Int32</span></span>|<span data-ttu-id="25e0e-247">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="25e0e-247">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="25e0e-248">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="25e0e-248">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="25e0e-249">Int32</span><span class="sxs-lookup"><span data-stu-id="25e0e-249">Int32</span></span>|<span data-ttu-id="25e0e-250">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="25e0e-250">Number of previous passwords to block.</span></span> <span data-ttu-id="25e0e-251">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="25e0e-251">Valid values 0 to 24</span></span>|
|<span data-ttu-id="25e0e-252">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="25e0e-252">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="25e0e-253">Int32</span><span class="sxs-lookup"><span data-stu-id="25e0e-253">Int32</span></span>|<span data-ttu-id="25e0e-254">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="25e0e-254">Number of sign in failures allowed before factory reset.</span></span> <span data-ttu-id="25e0e-255">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="25e0e-255">Valid values 4 to 11</span></span>|
|<span data-ttu-id="25e0e-256">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="25e0e-256">passwordRequiredType</span></span>|[<span data-ttu-id="25e0e-257">androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="25e0e-257">androidRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidrequiredpasswordtype.md)|<span data-ttu-id="25e0e-258">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="25e0e-258">Type of password that is required.</span></span> <span data-ttu-id="25e0e-259">Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.</span><span class="sxs-lookup"><span data-stu-id="25e0e-259">Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span></span>|
|<span data-ttu-id="25e0e-260">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="25e0e-260">passwordRequired</span></span>|<span data-ttu-id="25e0e-261">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-261">Boolean</span></span>|<span data-ttu-id="25e0e-262">Indica si se va a requerir una contraseña.</span><span class="sxs-lookup"><span data-stu-id="25e0e-262">Indicates whether or not to require a password.</span></span>|
|<span data-ttu-id="25e0e-263">powerOffBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-263">powerOffBlocked</span></span>|<span data-ttu-id="25e0e-264">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-264">Boolean</span></span>|<span data-ttu-id="25e0e-265">Indica si se va a bloquear el apagado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25e0e-265">Indicates whether or not to block powering off the device.</span></span>|
|<span data-ttu-id="25e0e-266">factoryResetBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-266">factoryResetBlocked</span></span>|<span data-ttu-id="25e0e-267">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-267">Boolean</span></span>|<span data-ttu-id="25e0e-268">Indica si se va a impedir que el usuario realice un restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="25e0e-268">Indicates whether or not to block user performing a factory reset.</span></span>|
|<span data-ttu-id="25e0e-269">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-269">screenCaptureBlocked</span></span>|<span data-ttu-id="25e0e-270">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-270">Boolean</span></span>|<span data-ttu-id="25e0e-271">Indica si se van a impedir las capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="25e0e-271">Indicates whether or not to block screenshots.</span></span>|
|<span data-ttu-id="25e0e-272">deviceSharingAllowed</span><span class="sxs-lookup"><span data-stu-id="25e0e-272">deviceSharingAllowed</span></span>|<span data-ttu-id="25e0e-273">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-273">Boolean</span></span>|<span data-ttu-id="25e0e-274">Indica si se va a permitir el modo de uso compartido del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25e0e-274">Indicates whether or not to allow device sharing mode.</span></span>|
|<span data-ttu-id="25e0e-275">storageBlockGoogleBackup</span><span class="sxs-lookup"><span data-stu-id="25e0e-275">storageBlockGoogleBackup</span></span>|<span data-ttu-id="25e0e-276">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-276">Boolean</span></span>|<span data-ttu-id="25e0e-277">Indica si se va a bloquear Google Backup.</span><span class="sxs-lookup"><span data-stu-id="25e0e-277">Indicates whether or not to block Google Backup.</span></span>|
|<span data-ttu-id="25e0e-278">storageBlockRemovableStorage</span><span class="sxs-lookup"><span data-stu-id="25e0e-278">storageBlockRemovableStorage</span></span>|<span data-ttu-id="25e0e-279">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-279">Boolean</span></span>|<span data-ttu-id="25e0e-280">Indica si se va a bloquear el uso de almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="25e0e-280">Indicates whether or not to block removable storage usage.</span></span>|
|<span data-ttu-id="25e0e-281">storageRequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="25e0e-281">storageRequireDeviceEncryption</span></span>|<span data-ttu-id="25e0e-282">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-282">Boolean</span></span>|<span data-ttu-id="25e0e-283">Indica si se va a requerir cifrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="25e0e-283">Indicates whether or not to require device encryption.</span></span>|
|<span data-ttu-id="25e0e-284">storageRequireRemovableStorageEncryption</span><span class="sxs-lookup"><span data-stu-id="25e0e-284">storageRequireRemovableStorageEncryption</span></span>|<span data-ttu-id="25e0e-285">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-285">Boolean</span></span>|<span data-ttu-id="25e0e-286">Indica si se va a requerir cifrado del almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="25e0e-286">Indicates whether or not to require removable storage encryption.</span></span>|
|<span data-ttu-id="25e0e-287">voiceAssistantBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-287">voiceAssistantBlocked</span></span>|<span data-ttu-id="25e0e-288">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-288">Boolean</span></span>|<span data-ttu-id="25e0e-289">Indica si se va a bloquear el uso del asistente de voz.</span><span class="sxs-lookup"><span data-stu-id="25e0e-289">Indicates whether or not to block the use of the Voice Assistant.</span></span>|
|<span data-ttu-id="25e0e-290">voiceDialingBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-290">voiceDialingBlocked</span></span>|<span data-ttu-id="25e0e-291">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-291">Boolean</span></span>|<span data-ttu-id="25e0e-292">Indica si se va a bloquear la marcación por voz.</span><span class="sxs-lookup"><span data-stu-id="25e0e-292">Indicates whether or not to block voice dialing.</span></span>|
|<span data-ttu-id="25e0e-293">webBrowserBlockPopups</span><span class="sxs-lookup"><span data-stu-id="25e0e-293">webBrowserBlockPopups</span></span>|<span data-ttu-id="25e0e-294">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-294">Boolean</span></span>|<span data-ttu-id="25e0e-295">Indica si se van a bloquear los elementos emergentes en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="25e0e-295">Indicates whether or not to block popups within the web browser.</span></span>|
|<span data-ttu-id="25e0e-296">webBrowserBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="25e0e-296">webBrowserBlockAutofill</span></span>|<span data-ttu-id="25e0e-297">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-297">Boolean</span></span>|<span data-ttu-id="25e0e-298">Indica si se va a bloquear la característica de autorrellenado del explorador web.</span><span class="sxs-lookup"><span data-stu-id="25e0e-298">Indicates whether or not to block the web browser's auto fill feature.</span></span>|
|<span data-ttu-id="25e0e-299">webBrowserBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="25e0e-299">webBrowserBlockJavaScript</span></span>|<span data-ttu-id="25e0e-300">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-300">Boolean</span></span>|<span data-ttu-id="25e0e-301">Indica si se va a bloquear JavaScript en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="25e0e-301">Indicates whether or not to block JavaScript within the web browser.</span></span>|
|<span data-ttu-id="25e0e-302">webBrowserBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-302">webBrowserBlocked</span></span>|<span data-ttu-id="25e0e-303">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-303">Boolean</span></span>|<span data-ttu-id="25e0e-304">Indica si se va a bloquear el explorador web.</span><span class="sxs-lookup"><span data-stu-id="25e0e-304">Indicates whether or not to block the web browser.</span></span>|
|<span data-ttu-id="25e0e-305">webBrowserCookieSettings</span><span class="sxs-lookup"><span data-stu-id="25e0e-305">webBrowserCookieSettings</span></span>|[<span data-ttu-id="25e0e-306">webBrowserCookieSettings</span><span class="sxs-lookup"><span data-stu-id="25e0e-306">webBrowserCookieSettings</span></span>](../resources/intune-deviceconfig-webbrowsercookiesettings.md)|<span data-ttu-id="25e0e-307">Configuración de cookies en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="25e0e-307">Cookie settings within the web browser.</span></span> <span data-ttu-id="25e0e-308">Los valores posibles son: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited` y `allowAlways`.</span><span class="sxs-lookup"><span data-stu-id="25e0e-308">Possible values are: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited`, `allowAlways`.</span></span>|
|<span data-ttu-id="25e0e-309">wiFiBlocked</span><span class="sxs-lookup"><span data-stu-id="25e0e-309">wiFiBlocked</span></span>|<span data-ttu-id="25e0e-310">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-310">Boolean</span></span>|<span data-ttu-id="25e0e-311">Indica si se va a bloquear la sincronización de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="25e0e-311">Indicates whether or not to block syncing Wi-Fi.</span></span>|
|<span data-ttu-id="25e0e-312">appsInstallAllowList</span><span class="sxs-lookup"><span data-stu-id="25e0e-312">appsInstallAllowList</span></span>|<span data-ttu-id="25e0e-313">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-313">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="25e0e-314">Lista de aplicaciones que se pueden instalar en el dispositivo KNOX.</span><span class="sxs-lookup"><span data-stu-id="25e0e-314">List of apps which can be installed on the KNOX device.</span></span> <span data-ttu-id="25e0e-315">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="25e0e-315">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="25e0e-316">appsLaunchBlockList</span><span class="sxs-lookup"><span data-stu-id="25e0e-316">appsLaunchBlockList</span></span>|<span data-ttu-id="25e0e-317">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-317">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="25e0e-318">Lista de aplicaciones cuyo inicio en el dispositivo KNOX está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="25e0e-318">List of apps which are blocked from being launched on the KNOX device.</span></span> <span data-ttu-id="25e0e-319">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="25e0e-319">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="25e0e-320">appsHideList</span><span class="sxs-lookup"><span data-stu-id="25e0e-320">appsHideList</span></span>|<span data-ttu-id="25e0e-321">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="25e0e-321">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="25e0e-322">Lista de aplicaciones que se ocultarán en el dispositivo KNOX.</span><span class="sxs-lookup"><span data-stu-id="25e0e-322">List of apps to be hidden on the KNOX device.</span></span> <span data-ttu-id="25e0e-323">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="25e0e-323">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="25e0e-324">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="25e0e-324">securityRequireVerifyApps</span></span>|<span data-ttu-id="25e0e-325">Boolean</span><span class="sxs-lookup"><span data-stu-id="25e0e-325">Boolean</span></span>|<span data-ttu-id="25e0e-326">Requerir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="25e0e-326">Require the Android Verify apps feature is turned on.</span></span>|



## <a name="response"></a><span data-ttu-id="25e0e-327">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25e0e-327">Response</span></span>
<span data-ttu-id="25e0e-328">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25e0e-328">If successful, this method returns a `200 OK` response code and an updated [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="25e0e-329">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25e0e-329">Example</span></span>
### <a name="request"></a><span data-ttu-id="25e0e-330">Solicitud</span><span class="sxs-lookup"><span data-stu-id="25e0e-330">Request</span></span>
<span data-ttu-id="25e0e-331">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="25e0e-331">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 3153

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "appsBlockClipboardSharing": true,
  "appsBlockCopyPaste": true,
  "appsBlockYouTube": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockMessaging": true,
  "cellularBlockVoiceRoaming": true,
  "cellularBlockWiFiTethering": true,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "diagnosticDataBlockSubmission": true,
  "locationServicesBlocked": true,
  "googleAccountBlockAutoSync": true,
  "googlePlayStoreBlocked": true,
  "kioskModeBlockSleepButton": true,
  "kioskModeBlockVolumeButtons": true,
  "dateAndTimeBlockChanges": true,
  "kioskModeApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "nfcBlocked": true,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "alphabetic",
  "passwordRequired": true,
  "powerOffBlocked": true,
  "factoryResetBlocked": true,
  "screenCaptureBlocked": true,
  "deviceSharingAllowed": true,
  "storageBlockGoogleBackup": true,
  "storageBlockRemovableStorage": true,
  "storageRequireDeviceEncryption": true,
  "storageRequireRemovableStorageEncryption": true,
  "voiceAssistantBlocked": true,
  "voiceDialingBlocked": true,
  "webBrowserBlockPopups": true,
  "webBrowserBlockAutofill": true,
  "webBrowserBlockJavaScript": true,
  "webBrowserBlocked": true,
  "webBrowserCookieSettings": "blockAlways",
  "wiFiBlocked": true,
  "appsInstallAllowList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsLaunchBlockList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsHideList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "securityRequireVerifyApps": true
}
```

### <a name="response"></a><span data-ttu-id="25e0e-332">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25e0e-332">Response</span></span>
<span data-ttu-id="25e0e-p123">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="25e0e-p123">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 3333

{
  "@odata.type": "#microsoft.graph.androidGeneralDeviceConfiguration",
  "id": "9e00d534-d534-9e00-34d5-009e34d5009e",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "roleScopeTagIds": [
    "Role Scope Tag Ids value"
  ],
  "supportsScopeTags": true,
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "appsBlockClipboardSharing": true,
  "appsBlockCopyPaste": true,
  "appsBlockYouTube": true,
  "bluetoothBlocked": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockMessaging": true,
  "cellularBlockVoiceRoaming": true,
  "cellularBlockWiFiTethering": true,
  "compliantAppsList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "compliantAppListType": "appsInListCompliant",
  "diagnosticDataBlockSubmission": true,
  "locationServicesBlocked": true,
  "googleAccountBlockAutoSync": true,
  "googlePlayStoreBlocked": true,
  "kioskModeBlockSleepButton": true,
  "kioskModeBlockVolumeButtons": true,
  "dateAndTimeBlockChanges": true,
  "kioskModeApps": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "nfcBlocked": true,
  "passwordBlockFingerprintUnlock": true,
  "passwordBlockTrustAgents": true,
  "passwordExpirationDays": 6,
  "passwordMinimumLength": 5,
  "passwordMinutesOfInactivityBeforeScreenTimeout": 14,
  "passwordPreviousPasswordBlockCount": 2,
  "passwordSignInFailureCountBeforeFactoryReset": 12,
  "passwordRequiredType": "alphabetic",
  "passwordRequired": true,
  "powerOffBlocked": true,
  "factoryResetBlocked": true,
  "screenCaptureBlocked": true,
  "deviceSharingAllowed": true,
  "storageBlockGoogleBackup": true,
  "storageBlockRemovableStorage": true,
  "storageRequireDeviceEncryption": true,
  "storageRequireRemovableStorageEncryption": true,
  "voiceAssistantBlocked": true,
  "voiceDialingBlocked": true,
  "webBrowserBlockPopups": true,
  "webBrowserBlockAutofill": true,
  "webBrowserBlockJavaScript": true,
  "webBrowserBlocked": true,
  "webBrowserCookieSettings": "blockAlways",
  "wiFiBlocked": true,
  "appsInstallAllowList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsLaunchBlockList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsHideList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "securityRequireVerifyApps": true
}
```





