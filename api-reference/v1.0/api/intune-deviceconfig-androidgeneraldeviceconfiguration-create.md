---
title: Crear androidGeneralDeviceConfiguration
description: Crear un objeto androidGeneralDeviceConfiguration.
ms.openlocfilehash: e28312afe09e150cb123e10767b373b9014f4f1a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031583"
---
# <a name="create-androidgeneraldeviceconfiguration"></a><span data-ttu-id="8d9d2-103">Crear androidGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8d9d2-103">Create androidGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="8d9d2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d9d2-105">Crear un objeto [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="8d9d2-105">Create a new [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8d9d2-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8d9d2-106">Prerequisites</span></span>
<span data-ttu-id="8d9d2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8d9d2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8d9d2-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8d9d2-109">Permission type</span></span>|<span data-ttu-id="8d9d2-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8d9d2-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-111">Delegated (work or school account)</span></span>|<span data-ttu-id="8d9d2-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8d9d2-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8d9d2-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8d9d2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-114">Not supported.</span></span>|
|<span data-ttu-id="8d9d2-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8d9d2-115">Application</span></span>|<span data-ttu-id="8d9d2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8d9d2-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8d9d2-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="8d9d2-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8d9d2-118">Request headers</span></span>
|<span data-ttu-id="8d9d2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d9d2-119">Header</span></span>|<span data-ttu-id="8d9d2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="8d9d2-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8d9d2-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="8d9d2-121">Authorization</span></span>|<span data-ttu-id="8d9d2-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8d9d2-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8d9d2-123">Accept</span></span>|<span data-ttu-id="8d9d2-124">application/json</span><span class="sxs-lookup"><span data-stu-id="8d9d2-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8d9d2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8d9d2-125">Request body</span></span>
<span data-ttu-id="8d9d2-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-126">In the request body, supply a JSON representation for the androidGeneralDeviceConfiguration object.</span></span>

<span data-ttu-id="8d9d2-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-127">The following table shows the properties that are required when you create the androidGeneralDeviceConfiguration.</span></span>

|<span data-ttu-id="8d9d2-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d9d2-128">Property</span></span>|<span data-ttu-id="8d9d2-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d9d2-129">Type</span></span>|<span data-ttu-id="8d9d2-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d9d2-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d9d2-131">id</span><span class="sxs-lookup"><span data-stu-id="8d9d2-131">id</span></span>|<span data-ttu-id="8d9d2-132">String</span><span class="sxs-lookup"><span data-stu-id="8d9d2-132">String</span></span>|<span data-ttu-id="8d9d2-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-133">Key of the entity.</span></span> <span data-ttu-id="8d9d2-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8d9d2-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8d9d2-135">lastModifiedDateTime</span></span>|<span data-ttu-id="8d9d2-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8d9d2-136">DateTimeOffset</span></span>|<span data-ttu-id="8d9d2-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-137">DateTime the object was last modified.</span></span> <span data-ttu-id="8d9d2-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8d9d2-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8d9d2-139">createdDateTime</span></span>|<span data-ttu-id="8d9d2-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8d9d2-140">DateTimeOffset</span></span>|<span data-ttu-id="8d9d2-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-141">DateTime the object was created.</span></span> <span data-ttu-id="8d9d2-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8d9d2-143">descripción</span><span class="sxs-lookup"><span data-stu-id="8d9d2-143">description</span></span>|<span data-ttu-id="8d9d2-144">String</span><span class="sxs-lookup"><span data-stu-id="8d9d2-144">String</span></span>|<span data-ttu-id="8d9d2-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="8d9d2-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8d9d2-147">displayName</span><span class="sxs-lookup"><span data-stu-id="8d9d2-147">displayName</span></span>|<span data-ttu-id="8d9d2-148">String</span><span class="sxs-lookup"><span data-stu-id="8d9d2-148">String</span></span>|<span data-ttu-id="8d9d2-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="8d9d2-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8d9d2-151">version</span><span class="sxs-lookup"><span data-stu-id="8d9d2-151">version</span></span>|<span data-ttu-id="8d9d2-152">Int32</span><span class="sxs-lookup"><span data-stu-id="8d9d2-152">Int32</span></span>|<span data-ttu-id="8d9d2-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-153">Version of the device configuration.</span></span> <span data-ttu-id="8d9d2-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8d9d2-155">appsBlockClipboardSharing</span><span class="sxs-lookup"><span data-stu-id="8d9d2-155">appsBlockClipboardSharing</span></span>|<span data-ttu-id="8d9d2-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-156">Boolean</span></span>|<span data-ttu-id="8d9d2-157">Indica si se va a bloquear el uso compartido del Portapapeles para copiar y pegar entre aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-157">Indicates whether or not to block clipboard sharing to copy and paste between applications.</span></span>|
|<span data-ttu-id="8d9d2-158">appsBlockCopyPaste</span><span class="sxs-lookup"><span data-stu-id="8d9d2-158">appsBlockCopyPaste</span></span>|<span data-ttu-id="8d9d2-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-159">Boolean</span></span>|<span data-ttu-id="8d9d2-160">Indica si se va a impedir copiar y pegar en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-160">Indicates whether or not to block copy and paste within applications.</span></span>|
|<span data-ttu-id="8d9d2-161">appsBlockYouTube</span><span class="sxs-lookup"><span data-stu-id="8d9d2-161">appsBlockYouTube</span></span>|<span data-ttu-id="8d9d2-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-162">Boolean</span></span>|<span data-ttu-id="8d9d2-163">Indica si se va a bloquear la aplicación YouTube.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-163">Indicates whether or not to block the YouTube app.</span></span>|
|<span data-ttu-id="8d9d2-164">bluetoothBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-164">bluetoothBlocked</span></span>|<span data-ttu-id="8d9d2-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-165">Boolean</span></span>|<span data-ttu-id="8d9d2-166">Indica si se va a bloquear Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-166">Indicates whether or not to block Bluetooth.</span></span>|
|<span data-ttu-id="8d9d2-167">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-167">cameraBlocked</span></span>|<span data-ttu-id="8d9d2-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-168">Boolean</span></span>|<span data-ttu-id="8d9d2-169">Indica si se va a bloquear el uso de la cámara.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-169">Indicates whether or not to block the use of the camera.</span></span>|
|<span data-ttu-id="8d9d2-170">cellularBlockDataRoaming</span><span class="sxs-lookup"><span data-stu-id="8d9d2-170">cellularBlockDataRoaming</span></span>|<span data-ttu-id="8d9d2-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-171">Boolean</span></span>|<span data-ttu-id="8d9d2-172">Indica si se va a bloquear la itinerancia de datos.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-172">Indicates whether or not to block data roaming.</span></span>|
|<span data-ttu-id="8d9d2-173">cellularBlockMessaging</span><span class="sxs-lookup"><span data-stu-id="8d9d2-173">cellularBlockMessaging</span></span>|<span data-ttu-id="8d9d2-174">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-174">Boolean</span></span>|<span data-ttu-id="8d9d2-175">Indica si se va a bloquear la mensajería SMS/MMS.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-175">Indicates whether or not to block SMS/MMS messaging.</span></span>|
|<span data-ttu-id="8d9d2-176">cellularBlockVoiceRoaming</span><span class="sxs-lookup"><span data-stu-id="8d9d2-176">cellularBlockVoiceRoaming</span></span>|<span data-ttu-id="8d9d2-177">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-177">Boolean</span></span>|<span data-ttu-id="8d9d2-178">Indica si se va a bloquear la itinerancia de voz.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-178">Indicates whether or not to block voice roaming.</span></span>|
|<span data-ttu-id="8d9d2-179">cellularBlockWiFiTethering</span><span class="sxs-lookup"><span data-stu-id="8d9d2-179">cellularBlockWiFiTethering</span></span>|<span data-ttu-id="8d9d2-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-180">Boolean</span></span>|<span data-ttu-id="8d9d2-181">Indica si se va a bloquear la sincronización de tethering Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-181">Indicates whether or not to block syncing Wi-Fi tethering.</span></span>|
|<span data-ttu-id="8d9d2-182">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="8d9d2-182">compliantAppsList</span></span>|<span data-ttu-id="8d9d2-183">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-183">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="8d9d2-184">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="8d9d2-184">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="8d9d2-185">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-185">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="8d9d2-186">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="8d9d2-186">compliantAppListType</span></span>|[<span data-ttu-id="8d9d2-187">appListType</span><span class="sxs-lookup"><span data-stu-id="8d9d2-187">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="8d9d2-188">Tipo de lista que se encuentra en la CompliantAppsList.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-188">Type of list that is in the CompliantAppsList.</span></span> <span data-ttu-id="8d9d2-189">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-189">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="8d9d2-190">diagnosticDataBlockSubmission</span><span class="sxs-lookup"><span data-stu-id="8d9d2-190">diagnosticDataBlockSubmission</span></span>|<span data-ttu-id="8d9d2-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-191">Boolean</span></span>|<span data-ttu-id="8d9d2-192">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-192">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="8d9d2-193">locationServicesBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-193">locationServicesBlocked</span></span>|<span data-ttu-id="8d9d2-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-194">Boolean</span></span>|<span data-ttu-id="8d9d2-195">Indica si se van a bloquear los servicios de ubicación.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-195">Indicates whether or not to block location services.</span></span>|
|<span data-ttu-id="8d9d2-196">googleAccountBlockAutoSync</span><span class="sxs-lookup"><span data-stu-id="8d9d2-196">googleAccountBlockAutoSync</span></span>|<span data-ttu-id="8d9d2-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-197">Boolean</span></span>|<span data-ttu-id="8d9d2-198">Indica si se va a bloquear la sincronización automática de cuentas de Google.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-198">Indicates whether or not to block Google account auto sync.</span></span>|
|<span data-ttu-id="8d9d2-199">googlePlayStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-199">googlePlayStoreBlocked</span></span>|<span data-ttu-id="8d9d2-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-200">Boolean</span></span>|<span data-ttu-id="8d9d2-201">Indica si se va a bloquear la aplicación Google Play Store.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-201">Indicates whether or not to block the Google Play store.</span></span>|
|<span data-ttu-id="8d9d2-202">kioskModeBlockSleepButton</span><span class="sxs-lookup"><span data-stu-id="8d9d2-202">kioskModeBlockSleepButton</span></span>|<span data-ttu-id="8d9d2-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-203">Boolean</span></span>|<span data-ttu-id="8d9d2-204">Indica si se va a bloquear el botón de suspensión de pantalla durante el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-204">Indicates whether or not to block the screen sleep button while in Kiosk Mode.</span></span>|
|<span data-ttu-id="8d9d2-205">kioskModeBlockVolumeButtons</span><span class="sxs-lookup"><span data-stu-id="8d9d2-205">kioskModeBlockVolumeButtons</span></span>|<span data-ttu-id="8d9d2-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-206">Boolean</span></span>|<span data-ttu-id="8d9d2-207">Indica si se van a bloquear los botones de volumen durante el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-207">Indicates whether or not to block the volume buttons while in Kiosk Mode.</span></span>|
|<span data-ttu-id="8d9d2-208">kioskModeApps</span><span class="sxs-lookup"><span data-stu-id="8d9d2-208">kioskModeApps</span></span>|<span data-ttu-id="8d9d2-209">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-209">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="8d9d2-210">Lista de aplicaciones que se podrán ejecutar cuando el dispositivo esté en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-210">A list of apps that will be allowed to run when the device is in Kiosk Mode.</span></span> <span data-ttu-id="8d9d2-211">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-211">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="8d9d2-212">nfcBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-212">nfcBlocked</span></span>|<span data-ttu-id="8d9d2-213">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-213">Boolean</span></span>|<span data-ttu-id="8d9d2-214">Indica si se va a bloquear la transmisión de datos en proximidad.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-214">Indicates whether or not to block Near-Field Communication.</span></span>|
|<span data-ttu-id="8d9d2-215">passwordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="8d9d2-215">passwordBlockFingerprintUnlock</span></span>|<span data-ttu-id="8d9d2-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-216">Boolean</span></span>|<span data-ttu-id="8d9d2-217">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-217">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="8d9d2-218">passwordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="8d9d2-218">passwordBlockTrustAgents</span></span>|<span data-ttu-id="8d9d2-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-219">Boolean</span></span>|<span data-ttu-id="8d9d2-220">Indica si se van a bloquear Smart Lock y otros agentes de confianza.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-220">Indicates whether or not to block Smart Lock and other trust agents.</span></span>|
|<span data-ttu-id="8d9d2-221">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="8d9d2-221">passwordExpirationDays</span></span>|<span data-ttu-id="8d9d2-222">Int32</span><span class="sxs-lookup"><span data-stu-id="8d9d2-222">Int32</span></span>|<span data-ttu-id="8d9d2-223">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-223">Number of days before the password expires.</span></span> <span data-ttu-id="8d9d2-224">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="8d9d2-224">Valid values 1 to 365</span></span>|
|<span data-ttu-id="8d9d2-225">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="8d9d2-225">passwordMinimumLength</span></span>|<span data-ttu-id="8d9d2-226">Int32</span><span class="sxs-lookup"><span data-stu-id="8d9d2-226">Int32</span></span>|<span data-ttu-id="8d9d2-227">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-227">Minimum length of passwords.</span></span> <span data-ttu-id="8d9d2-228">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="8d9d2-228">Valid values 4 to 16</span></span>|
|<span data-ttu-id="8d9d2-229">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="8d9d2-229">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="8d9d2-230">Int32</span><span class="sxs-lookup"><span data-stu-id="8d9d2-230">Int32</span></span>|<span data-ttu-id="8d9d2-231">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-231">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="8d9d2-232">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="8d9d2-232">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="8d9d2-233">Int32</span><span class="sxs-lookup"><span data-stu-id="8d9d2-233">Int32</span></span>|<span data-ttu-id="8d9d2-234">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-234">Number of previous passwords to block.</span></span> <span data-ttu-id="8d9d2-235">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="8d9d2-235">Valid values 0 to 24</span></span>|
|<span data-ttu-id="8d9d2-236">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="8d9d2-236">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="8d9d2-237">Int32</span><span class="sxs-lookup"><span data-stu-id="8d9d2-237">Int32</span></span>|<span data-ttu-id="8d9d2-238">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-238">Number of sign in failures allowed before factory reset.</span></span> <span data-ttu-id="8d9d2-239">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="8d9d2-239">Valid values 4 to 11</span></span>|
|<span data-ttu-id="8d9d2-240">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="8d9d2-240">passwordRequiredType</span></span>|[<span data-ttu-id="8d9d2-241">androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="8d9d2-241">androidRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidrequiredpasswordtype.md)|<span data-ttu-id="8d9d2-242">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-242">Type of password that is required.</span></span> <span data-ttu-id="8d9d2-243">Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-243">Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span></span>|
|<span data-ttu-id="8d9d2-244">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="8d9d2-244">passwordRequired</span></span>|<span data-ttu-id="8d9d2-245">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-245">Boolean</span></span>|<span data-ttu-id="8d9d2-246">Indica si se va a requerir una contraseña.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-246">Indicates whether or not to require a password.</span></span>|
|<span data-ttu-id="8d9d2-247">powerOffBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-247">powerOffBlocked</span></span>|<span data-ttu-id="8d9d2-248">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-248">Boolean</span></span>|<span data-ttu-id="8d9d2-249">Indica si se va a bloquear el apagado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-249">Indicates whether or not to block powering off the device.</span></span>|
|<span data-ttu-id="8d9d2-250">factoryResetBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-250">factoryResetBlocked</span></span>|<span data-ttu-id="8d9d2-251">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-251">Boolean</span></span>|<span data-ttu-id="8d9d2-252">Indica si se va a impedir que el usuario realice un restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-252">Indicates whether or not to block user performing a factory reset.</span></span>|
|<span data-ttu-id="8d9d2-253">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-253">screenCaptureBlocked</span></span>|<span data-ttu-id="8d9d2-254">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-254">Boolean</span></span>|<span data-ttu-id="8d9d2-255">Indica si se van a impedir las capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-255">Indicates whether or not to block screenshots.</span></span>|
|<span data-ttu-id="8d9d2-256">deviceSharingAllowed</span><span class="sxs-lookup"><span data-stu-id="8d9d2-256">deviceSharingAllowed</span></span>|<span data-ttu-id="8d9d2-257">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-257">Boolean</span></span>|<span data-ttu-id="8d9d2-258">Indica si se va a permitir el modo de uso compartido del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-258">Indicates whether or not to allow device sharing mode.</span></span>|
|<span data-ttu-id="8d9d2-259">storageBlockGoogleBackup</span><span class="sxs-lookup"><span data-stu-id="8d9d2-259">storageBlockGoogleBackup</span></span>|<span data-ttu-id="8d9d2-260">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-260">Boolean</span></span>|<span data-ttu-id="8d9d2-261">Indica si se va a bloquear Google Backup.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-261">Indicates whether or not to block Google Backup.</span></span>|
|<span data-ttu-id="8d9d2-262">storageBlockRemovableStorage</span><span class="sxs-lookup"><span data-stu-id="8d9d2-262">storageBlockRemovableStorage</span></span>|<span data-ttu-id="8d9d2-263">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-263">Boolean</span></span>|<span data-ttu-id="8d9d2-264">Indica si se va a bloquear el uso de almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-264">Indicates whether or not to block removable storage usage.</span></span>|
|<span data-ttu-id="8d9d2-265">storageRequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="8d9d2-265">storageRequireDeviceEncryption</span></span>|<span data-ttu-id="8d9d2-266">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-266">Boolean</span></span>|<span data-ttu-id="8d9d2-267">Indica si se va a requerir cifrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-267">Indicates whether or not to require device encryption.</span></span>|
|<span data-ttu-id="8d9d2-268">storageRequireRemovableStorageEncryption</span><span class="sxs-lookup"><span data-stu-id="8d9d2-268">storageRequireRemovableStorageEncryption</span></span>|<span data-ttu-id="8d9d2-269">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-269">Boolean</span></span>|<span data-ttu-id="8d9d2-270">Indica si se va a requerir cifrado del almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-270">Indicates whether or not to require removable storage encryption.</span></span>|
|<span data-ttu-id="8d9d2-271">voiceAssistantBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-271">voiceAssistantBlocked</span></span>|<span data-ttu-id="8d9d2-272">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-272">Boolean</span></span>|<span data-ttu-id="8d9d2-273">Indica si se va a bloquear el uso del asistente de voz.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-273">Indicates whether or not to block the use of the Voice Assistant.</span></span>|
|<span data-ttu-id="8d9d2-274">voiceDialingBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-274">voiceDialingBlocked</span></span>|<span data-ttu-id="8d9d2-275">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-275">Boolean</span></span>|<span data-ttu-id="8d9d2-276">Indica si se va a bloquear la marcación por voz.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-276">Indicates whether or not to block voice dialing.</span></span>|
|<span data-ttu-id="8d9d2-277">webBrowserBlockPopups</span><span class="sxs-lookup"><span data-stu-id="8d9d2-277">webBrowserBlockPopups</span></span>|<span data-ttu-id="8d9d2-278">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-278">Boolean</span></span>|<span data-ttu-id="8d9d2-279">Indica si se van a bloquear los elementos emergentes en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-279">Indicates whether or not to block popups within the web browser.</span></span>|
|<span data-ttu-id="8d9d2-280">webBrowserBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="8d9d2-280">webBrowserBlockAutofill</span></span>|<span data-ttu-id="8d9d2-281">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-281">Boolean</span></span>|<span data-ttu-id="8d9d2-282">Indica si se va a bloquear la característica de autorrellenado del explorador web.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-282">Indicates whether or not to block the web browser's auto fill feature.</span></span>|
|<span data-ttu-id="8d9d2-283">webBrowserBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="8d9d2-283">webBrowserBlockJavaScript</span></span>|<span data-ttu-id="8d9d2-284">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-284">Boolean</span></span>|<span data-ttu-id="8d9d2-285">Indica si se va a bloquear JavaScript en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-285">Indicates whether or not to block JavaScript within the web browser.</span></span>|
|<span data-ttu-id="8d9d2-286">webBrowserBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-286">webBrowserBlocked</span></span>|<span data-ttu-id="8d9d2-287">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-287">Boolean</span></span>|<span data-ttu-id="8d9d2-288">Indica si se va a bloquear el explorador web.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-288">Indicates whether or not to block the web browser.</span></span>|
|<span data-ttu-id="8d9d2-289">webBrowserCookieSettings</span><span class="sxs-lookup"><span data-stu-id="8d9d2-289">webBrowserCookieSettings</span></span>|[<span data-ttu-id="8d9d2-290">webBrowserCookieSettings</span><span class="sxs-lookup"><span data-stu-id="8d9d2-290">webBrowserCookieSettings</span></span>](../resources/intune-deviceconfig-webbrowsercookiesettings.md)|<span data-ttu-id="8d9d2-291">Configuración de cookies en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-291">Cookie settings within the web browser.</span></span> <span data-ttu-id="8d9d2-292">Los valores posibles son: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited` y `allowAlways`.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-292">Possible values are: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited`, `allowAlways`.</span></span>|
|<span data-ttu-id="8d9d2-293">wiFiBlocked</span><span class="sxs-lookup"><span data-stu-id="8d9d2-293">wiFiBlocked</span></span>|<span data-ttu-id="8d9d2-294">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-294">Boolean</span></span>|<span data-ttu-id="8d9d2-295">Indica si se va a bloquear la sincronización de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-295">Indicates whether or not to block syncing Wi-Fi.</span></span>|
|<span data-ttu-id="8d9d2-296">appsInstallAllowList</span><span class="sxs-lookup"><span data-stu-id="8d9d2-296">appsInstallAllowList</span></span>|<span data-ttu-id="8d9d2-297">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-297">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="8d9d2-298">Lista de aplicaciones que se pueden instalar en el dispositivo KNOX.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-298">List of apps which can be installed on the KNOX device.</span></span> <span data-ttu-id="8d9d2-299">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-299">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="8d9d2-300">appsLaunchBlockList</span><span class="sxs-lookup"><span data-stu-id="8d9d2-300">appsLaunchBlockList</span></span>|<span data-ttu-id="8d9d2-301">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-301">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="8d9d2-302">Lista de aplicaciones cuyo inicio en el dispositivo KNOX está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-302">List of apps which are blocked from being launched on the KNOX device.</span></span> <span data-ttu-id="8d9d2-303">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-303">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="8d9d2-304">appsHideList</span><span class="sxs-lookup"><span data-stu-id="8d9d2-304">appsHideList</span></span>|<span data-ttu-id="8d9d2-305">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="8d9d2-305">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="8d9d2-306">Lista de aplicaciones que se ocultarán en el dispositivo KNOX.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-306">List of apps to be hidden on the KNOX device.</span></span> <span data-ttu-id="8d9d2-307">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-307">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="8d9d2-308">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="8d9d2-308">securityRequireVerifyApps</span></span>|<span data-ttu-id="8d9d2-309">Booleano</span><span class="sxs-lookup"><span data-stu-id="8d9d2-309">Boolean</span></span>|<span data-ttu-id="8d9d2-310">Requerir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-310">Require the Android Verify apps feature is turned on.</span></span>|



## <a name="response"></a><span data-ttu-id="8d9d2-311">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d9d2-311">Response</span></span>
<span data-ttu-id="8d9d2-312">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-312">If successful, this method returns a `201 Created` response code and a [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8d9d2-313">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d9d2-313">Example</span></span>
### <a name="request"></a><span data-ttu-id="8d9d2-314">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8d9d2-314">Request</span></span>
<span data-ttu-id="8d9d2-315">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-315">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 3033

{
  "@odata.type": "#microsoft.graph.androidGeneralDeviceConfiguration",
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

### <a name="response"></a><span data-ttu-id="8d9d2-316">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d9d2-316">Response</span></span>
<span data-ttu-id="8d9d2-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8d9d2-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 3205

{
  "@odata.type": "#microsoft.graph.androidGeneralDeviceConfiguration",
  "id": "9e00d534-d534-9e00-34d5-009e34d5009e",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
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



