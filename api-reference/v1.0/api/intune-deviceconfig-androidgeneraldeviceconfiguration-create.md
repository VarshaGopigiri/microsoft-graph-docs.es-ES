---
title: Crear androidGeneralDeviceConfiguration
description: Crear un objeto androidGeneralDeviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: dcf27402456ab0e37d71ef82ff5e559a54df0b89
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972519"
---
# <a name="create-androidgeneraldeviceconfiguration"></a><span data-ttu-id="cc42c-103">Crear androidGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="cc42c-103">Create androidGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="cc42c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cc42c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cc42c-105">Crear un objeto [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cc42c-105">Create a new [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cc42c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cc42c-106">Prerequisites</span></span>
<span data-ttu-id="cc42c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cc42c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cc42c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cc42c-109">Permission type</span></span>|<span data-ttu-id="cc42c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cc42c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cc42c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cc42c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="cc42c-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cc42c-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="cc42c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cc42c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cc42c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc42c-114">Not supported.</span></span>|
|<span data-ttu-id="cc42c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cc42c-115">Application</span></span>|<span data-ttu-id="cc42c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc42c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cc42c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc42c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="cc42c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cc42c-118">Request headers</span></span>
|<span data-ttu-id="cc42c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cc42c-119">Header</span></span>|<span data-ttu-id="cc42c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cc42c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cc42c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="cc42c-121">Authorization</span></span>|<span data-ttu-id="cc42c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cc42c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cc42c-123">Accept</span><span class="sxs-lookup"><span data-stu-id="cc42c-123">Accept</span></span>|<span data-ttu-id="cc42c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cc42c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cc42c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc42c-125">Request body</span></span>
<span data-ttu-id="cc42c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto androidGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cc42c-126">In the request body, supply a JSON representation for the androidGeneralDeviceConfiguration object.</span></span>

<span data-ttu-id="cc42c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto androidGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cc42c-127">The following table shows the properties that are required when you create the androidGeneralDeviceConfiguration.</span></span>

|<span data-ttu-id="cc42c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cc42c-128">Property</span></span>|<span data-ttu-id="cc42c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc42c-129">Type</span></span>|<span data-ttu-id="cc42c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc42c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cc42c-131">id</span><span class="sxs-lookup"><span data-stu-id="cc42c-131">id</span></span>|<span data-ttu-id="cc42c-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="cc42c-132">String</span></span>|<span data-ttu-id="cc42c-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="cc42c-133">Key of the entity.</span></span> <span data-ttu-id="cc42c-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc42c-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc42c-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="cc42c-135">lastModifiedDateTime</span></span>|<span data-ttu-id="cc42c-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cc42c-136">DateTimeOffset</span></span>|<span data-ttu-id="cc42c-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="cc42c-137">DateTime the object was last modified.</span></span> <span data-ttu-id="cc42c-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc42c-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc42c-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="cc42c-139">createdDateTime</span></span>|<span data-ttu-id="cc42c-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="cc42c-140">DateTimeOffset</span></span>|<span data-ttu-id="cc42c-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="cc42c-141">DateTime the object was created.</span></span> <span data-ttu-id="cc42c-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc42c-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc42c-143">descripción</span><span class="sxs-lookup"><span data-stu-id="cc42c-143">description</span></span>|<span data-ttu-id="cc42c-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="cc42c-144">String</span></span>|<span data-ttu-id="cc42c-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc42c-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="cc42c-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc42c-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc42c-147">displayName</span><span class="sxs-lookup"><span data-stu-id="cc42c-147">displayName</span></span>|<span data-ttu-id="cc42c-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="cc42c-148">String</span></span>|<span data-ttu-id="cc42c-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc42c-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="cc42c-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc42c-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc42c-151">version</span><span class="sxs-lookup"><span data-stu-id="cc42c-151">version</span></span>|<span data-ttu-id="cc42c-152">Int32</span><span class="sxs-lookup"><span data-stu-id="cc42c-152">Int32</span></span>|<span data-ttu-id="cc42c-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc42c-153">Version of the device configuration.</span></span> <span data-ttu-id="cc42c-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="cc42c-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="cc42c-155">appsBlockClipboardSharing</span><span class="sxs-lookup"><span data-stu-id="cc42c-155">appsBlockClipboardSharing</span></span>|<span data-ttu-id="cc42c-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-156">Boolean</span></span>|<span data-ttu-id="cc42c-157">Indica si se va a bloquear el uso compartido del Portapapeles para copiar y pegar entre aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="cc42c-157">Indicates whether or not to block clipboard sharing to copy and paste between applications.</span></span>|
|<span data-ttu-id="cc42c-158">appsBlockCopyPaste</span><span class="sxs-lookup"><span data-stu-id="cc42c-158">appsBlockCopyPaste</span></span>|<span data-ttu-id="cc42c-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-159">Boolean</span></span>|<span data-ttu-id="cc42c-160">Indica si se va a impedir copiar y pegar en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="cc42c-160">Indicates whether or not to block copy and paste within applications.</span></span>|
|<span data-ttu-id="cc42c-161">appsBlockYouTube</span><span class="sxs-lookup"><span data-stu-id="cc42c-161">appsBlockYouTube</span></span>|<span data-ttu-id="cc42c-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-162">Boolean</span></span>|<span data-ttu-id="cc42c-163">Indica si se va a bloquear la aplicación YouTube.</span><span class="sxs-lookup"><span data-stu-id="cc42c-163">Indicates whether or not to block the YouTube app.</span></span>|
|<span data-ttu-id="cc42c-164">bluetoothBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-164">bluetoothBlocked</span></span>|<span data-ttu-id="cc42c-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-165">Boolean</span></span>|<span data-ttu-id="cc42c-166">Indica si se va a bloquear Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="cc42c-166">Indicates whether or not to block Bluetooth.</span></span>|
|<span data-ttu-id="cc42c-167">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-167">cameraBlocked</span></span>|<span data-ttu-id="cc42c-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-168">Boolean</span></span>|<span data-ttu-id="cc42c-169">Indica si se va a bloquear el uso de la cámara.</span><span class="sxs-lookup"><span data-stu-id="cc42c-169">Indicates whether or not to block the use of the camera.</span></span>|
|<span data-ttu-id="cc42c-170">cellularBlockDataRoaming</span><span class="sxs-lookup"><span data-stu-id="cc42c-170">cellularBlockDataRoaming</span></span>|<span data-ttu-id="cc42c-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-171">Boolean</span></span>|<span data-ttu-id="cc42c-172">Indica si se va a bloquear la itinerancia de datos.</span><span class="sxs-lookup"><span data-stu-id="cc42c-172">Indicates whether or not to block data roaming.</span></span>|
|<span data-ttu-id="cc42c-173">cellularBlockMessaging</span><span class="sxs-lookup"><span data-stu-id="cc42c-173">cellularBlockMessaging</span></span>|<span data-ttu-id="cc42c-174">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-174">Boolean</span></span>|<span data-ttu-id="cc42c-175">Indica si se va a bloquear la mensajería SMS/MMS.</span><span class="sxs-lookup"><span data-stu-id="cc42c-175">Indicates whether or not to block SMS/MMS messaging.</span></span>|
|<span data-ttu-id="cc42c-176">cellularBlockVoiceRoaming</span><span class="sxs-lookup"><span data-stu-id="cc42c-176">cellularBlockVoiceRoaming</span></span>|<span data-ttu-id="cc42c-177">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-177">Boolean</span></span>|<span data-ttu-id="cc42c-178">Indica si se va a bloquear la itinerancia de voz.</span><span class="sxs-lookup"><span data-stu-id="cc42c-178">Indicates whether or not to block voice roaming.</span></span>|
|<span data-ttu-id="cc42c-179">cellularBlockWiFiTethering</span><span class="sxs-lookup"><span data-stu-id="cc42c-179">cellularBlockWiFiTethering</span></span>|<span data-ttu-id="cc42c-180">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-180">Boolean</span></span>|<span data-ttu-id="cc42c-181">Indica si se va a bloquear la sincronización de tethering Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="cc42c-181">Indicates whether or not to block syncing Wi-Fi tethering.</span></span>|
|<span data-ttu-id="cc42c-182">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="cc42c-182">compliantAppsList</span></span>|<span data-ttu-id="cc42c-183">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="cc42c-183">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="cc42c-184">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="cc42c-184">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="cc42c-185">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="cc42c-185">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="cc42c-186">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="cc42c-186">compliantAppListType</span></span>|[<span data-ttu-id="cc42c-187">appListType</span><span class="sxs-lookup"><span data-stu-id="cc42c-187">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="cc42c-188">Tipo de lista que se encuentra en la CompliantAppsList.</span><span class="sxs-lookup"><span data-stu-id="cc42c-188">Type of list that is in the CompliantAppsList.</span></span> <span data-ttu-id="cc42c-189">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="cc42c-189">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="cc42c-190">diagnosticDataBlockSubmission</span><span class="sxs-lookup"><span data-stu-id="cc42c-190">diagnosticDataBlockSubmission</span></span>|<span data-ttu-id="cc42c-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-191">Boolean</span></span>|<span data-ttu-id="cc42c-192">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="cc42c-192">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="cc42c-193">locationServicesBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-193">locationServicesBlocked</span></span>|<span data-ttu-id="cc42c-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-194">Boolean</span></span>|<span data-ttu-id="cc42c-195">Indica si se van a bloquear los servicios de ubicación.</span><span class="sxs-lookup"><span data-stu-id="cc42c-195">Indicates whether or not to block location services.</span></span>|
|<span data-ttu-id="cc42c-196">googleAccountBlockAutoSync</span><span class="sxs-lookup"><span data-stu-id="cc42c-196">googleAccountBlockAutoSync</span></span>|<span data-ttu-id="cc42c-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-197">Boolean</span></span>|<span data-ttu-id="cc42c-198">Indica si se va a bloquear la sincronización automática de cuentas de Google.</span><span class="sxs-lookup"><span data-stu-id="cc42c-198">Indicates whether or not to block Google account auto sync.</span></span>|
|<span data-ttu-id="cc42c-199">googlePlayStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-199">googlePlayStoreBlocked</span></span>|<span data-ttu-id="cc42c-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-200">Boolean</span></span>|<span data-ttu-id="cc42c-201">Indica si se va a bloquear la aplicación Google Play Store.</span><span class="sxs-lookup"><span data-stu-id="cc42c-201">Indicates whether or not to block the Google Play store.</span></span>|
|<span data-ttu-id="cc42c-202">kioskModeBlockSleepButton</span><span class="sxs-lookup"><span data-stu-id="cc42c-202">kioskModeBlockSleepButton</span></span>|<span data-ttu-id="cc42c-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-203">Boolean</span></span>|<span data-ttu-id="cc42c-204">Indica si se va a bloquear el botón de suspensión de pantalla durante el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="cc42c-204">Indicates whether or not to block the screen sleep button while in Kiosk Mode.</span></span>|
|<span data-ttu-id="cc42c-205">kioskModeBlockVolumeButtons</span><span class="sxs-lookup"><span data-stu-id="cc42c-205">kioskModeBlockVolumeButtons</span></span>|<span data-ttu-id="cc42c-206">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-206">Boolean</span></span>|<span data-ttu-id="cc42c-207">Indica si se van a bloquear los botones de volumen durante el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="cc42c-207">Indicates whether or not to block the volume buttons while in Kiosk Mode.</span></span>|
|<span data-ttu-id="cc42c-208">kioskModeApps</span><span class="sxs-lookup"><span data-stu-id="cc42c-208">kioskModeApps</span></span>|<span data-ttu-id="cc42c-209">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="cc42c-209">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="cc42c-210">Lista de aplicaciones que se podrán ejecutar cuando el dispositivo esté en modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="cc42c-210">A list of apps that will be allowed to run when the device is in Kiosk Mode.</span></span> <span data-ttu-id="cc42c-211">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="cc42c-211">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="cc42c-212">nfcBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-212">nfcBlocked</span></span>|<span data-ttu-id="cc42c-213">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-213">Boolean</span></span>|<span data-ttu-id="cc42c-214">Indica si se va a bloquear la transmisión de datos en proximidad.</span><span class="sxs-lookup"><span data-stu-id="cc42c-214">Indicates whether or not to block Near-Field Communication.</span></span>|
|<span data-ttu-id="cc42c-215">passwordBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="cc42c-215">passwordBlockFingerprintUnlock</span></span>|<span data-ttu-id="cc42c-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-216">Boolean</span></span>|<span data-ttu-id="cc42c-217">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="cc42c-217">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="cc42c-218">passwordBlockTrustAgents</span><span class="sxs-lookup"><span data-stu-id="cc42c-218">passwordBlockTrustAgents</span></span>|<span data-ttu-id="cc42c-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-219">Boolean</span></span>|<span data-ttu-id="cc42c-220">Indica si se van a bloquear Smart Lock y otros agentes de confianza.</span><span class="sxs-lookup"><span data-stu-id="cc42c-220">Indicates whether or not to block Smart Lock and other trust agents.</span></span>|
|<span data-ttu-id="cc42c-221">passwordExpirationDays</span><span class="sxs-lookup"><span data-stu-id="cc42c-221">passwordExpirationDays</span></span>|<span data-ttu-id="cc42c-222">Int32</span><span class="sxs-lookup"><span data-stu-id="cc42c-222">Int32</span></span>|<span data-ttu-id="cc42c-223">Número de días antes de que expire la contraseña.</span><span class="sxs-lookup"><span data-stu-id="cc42c-223">Number of days before the password expires.</span></span> <span data-ttu-id="cc42c-224">Valores válidos de 1 a 365</span><span class="sxs-lookup"><span data-stu-id="cc42c-224">Valid values 1 to 365</span></span>|
|<span data-ttu-id="cc42c-225">passwordMinimumLength</span><span class="sxs-lookup"><span data-stu-id="cc42c-225">passwordMinimumLength</span></span>|<span data-ttu-id="cc42c-226">Int32</span><span class="sxs-lookup"><span data-stu-id="cc42c-226">Int32</span></span>|<span data-ttu-id="cc42c-227">Longitud mínima de las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="cc42c-227">Minimum length of passwords.</span></span> <span data-ttu-id="cc42c-228">Valores válidos de 4 a 16</span><span class="sxs-lookup"><span data-stu-id="cc42c-228">Valid values 4 to 16</span></span>|
|<span data-ttu-id="cc42c-229">passwordMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="cc42c-229">passwordMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="cc42c-230">Int32</span><span class="sxs-lookup"><span data-stu-id="cc42c-230">Int32</span></span>|<span data-ttu-id="cc42c-231">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="cc42c-231">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="cc42c-232">passwordPreviousPasswordBlockCount</span><span class="sxs-lookup"><span data-stu-id="cc42c-232">passwordPreviousPasswordBlockCount</span></span>|<span data-ttu-id="cc42c-233">Int32</span><span class="sxs-lookup"><span data-stu-id="cc42c-233">Int32</span></span>|<span data-ttu-id="cc42c-234">Número de contraseñas anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="cc42c-234">Number of previous passwords to block.</span></span> <span data-ttu-id="cc42c-235">Valores válidos de 0 a 24</span><span class="sxs-lookup"><span data-stu-id="cc42c-235">Valid values 0 to 24</span></span>|
|<span data-ttu-id="cc42c-236">passwordSignInFailureCountBeforeFactoryReset</span><span class="sxs-lookup"><span data-stu-id="cc42c-236">passwordSignInFailureCountBeforeFactoryReset</span></span>|<span data-ttu-id="cc42c-237">Int32</span><span class="sxs-lookup"><span data-stu-id="cc42c-237">Int32</span></span>|<span data-ttu-id="cc42c-238">Número de errores de inicio de sesión permitidos antes del restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="cc42c-238">Number of sign in failures allowed before factory reset.</span></span> <span data-ttu-id="cc42c-239">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="cc42c-239">Valid values 4 to 11</span></span>|
|<span data-ttu-id="cc42c-240">passwordRequiredType</span><span class="sxs-lookup"><span data-stu-id="cc42c-240">passwordRequiredType</span></span>|[<span data-ttu-id="cc42c-241">androidRequiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="cc42c-241">androidRequiredPasswordType</span></span>](../resources/intune-deviceconfig-androidrequiredpasswordtype.md)|<span data-ttu-id="cc42c-242">Tipo de contraseña que es necesario.</span><span class="sxs-lookup"><span data-stu-id="cc42c-242">Type of password that is required.</span></span> <span data-ttu-id="cc42c-243">Los valores posibles son: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex` y `any`.</span><span class="sxs-lookup"><span data-stu-id="cc42c-243">Possible values are: `deviceDefault`, `alphabetic`, `alphanumeric`, `alphanumericWithSymbols`, `lowSecurityBiometric`, `numeric`, `numericComplex`, `any`.</span></span>|
|<span data-ttu-id="cc42c-244">passwordRequired</span><span class="sxs-lookup"><span data-stu-id="cc42c-244">passwordRequired</span></span>|<span data-ttu-id="cc42c-245">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-245">Boolean</span></span>|<span data-ttu-id="cc42c-246">Indica si se va a requerir una contraseña.</span><span class="sxs-lookup"><span data-stu-id="cc42c-246">Indicates whether or not to require a password.</span></span>|
|<span data-ttu-id="cc42c-247">powerOffBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-247">powerOffBlocked</span></span>|<span data-ttu-id="cc42c-248">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-248">Boolean</span></span>|<span data-ttu-id="cc42c-249">Indica si se va a bloquear el apagado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc42c-249">Indicates whether or not to block powering off the device.</span></span>|
|<span data-ttu-id="cc42c-250">factoryResetBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-250">factoryResetBlocked</span></span>|<span data-ttu-id="cc42c-251">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-251">Boolean</span></span>|<span data-ttu-id="cc42c-252">Indica si se va a impedir que el usuario realice un restablecimiento de fábrica.</span><span class="sxs-lookup"><span data-stu-id="cc42c-252">Indicates whether or not to block user performing a factory reset.</span></span>|
|<span data-ttu-id="cc42c-253">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-253">screenCaptureBlocked</span></span>|<span data-ttu-id="cc42c-254">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-254">Boolean</span></span>|<span data-ttu-id="cc42c-255">Indica si se van a impedir las capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="cc42c-255">Indicates whether or not to block screenshots.</span></span>|
|<span data-ttu-id="cc42c-256">deviceSharingAllowed</span><span class="sxs-lookup"><span data-stu-id="cc42c-256">deviceSharingAllowed</span></span>|<span data-ttu-id="cc42c-257">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-257">Boolean</span></span>|<span data-ttu-id="cc42c-258">Indica si se va a permitir el modo de uso compartido del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc42c-258">Indicates whether or not to allow device sharing mode.</span></span>|
|<span data-ttu-id="cc42c-259">storageBlockGoogleBackup</span><span class="sxs-lookup"><span data-stu-id="cc42c-259">storageBlockGoogleBackup</span></span>|<span data-ttu-id="cc42c-260">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-260">Boolean</span></span>|<span data-ttu-id="cc42c-261">Indica si se va a bloquear Google Backup.</span><span class="sxs-lookup"><span data-stu-id="cc42c-261">Indicates whether or not to block Google Backup.</span></span>|
|<span data-ttu-id="cc42c-262">storageBlockRemovableStorage</span><span class="sxs-lookup"><span data-stu-id="cc42c-262">storageBlockRemovableStorage</span></span>|<span data-ttu-id="cc42c-263">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-263">Boolean</span></span>|<span data-ttu-id="cc42c-264">Indica si se va a bloquear el uso de almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="cc42c-264">Indicates whether or not to block removable storage usage.</span></span>|
|<span data-ttu-id="cc42c-265">storageRequireDeviceEncryption</span><span class="sxs-lookup"><span data-stu-id="cc42c-265">storageRequireDeviceEncryption</span></span>|<span data-ttu-id="cc42c-266">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-266">Boolean</span></span>|<span data-ttu-id="cc42c-267">Indica si se va a requerir cifrado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc42c-267">Indicates whether or not to require device encryption.</span></span>|
|<span data-ttu-id="cc42c-268">storageRequireRemovableStorageEncryption</span><span class="sxs-lookup"><span data-stu-id="cc42c-268">storageRequireRemovableStorageEncryption</span></span>|<span data-ttu-id="cc42c-269">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-269">Boolean</span></span>|<span data-ttu-id="cc42c-270">Indica si se va a requerir cifrado del almacenamiento extraíble.</span><span class="sxs-lookup"><span data-stu-id="cc42c-270">Indicates whether or not to require removable storage encryption.</span></span>|
|<span data-ttu-id="cc42c-271">voiceAssistantBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-271">voiceAssistantBlocked</span></span>|<span data-ttu-id="cc42c-272">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-272">Boolean</span></span>|<span data-ttu-id="cc42c-273">Indica si se va a bloquear el uso del asistente de voz.</span><span class="sxs-lookup"><span data-stu-id="cc42c-273">Indicates whether or not to block the use of the Voice Assistant.</span></span>|
|<span data-ttu-id="cc42c-274">voiceDialingBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-274">voiceDialingBlocked</span></span>|<span data-ttu-id="cc42c-275">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-275">Boolean</span></span>|<span data-ttu-id="cc42c-276">Indica si se va a bloquear la marcación por voz.</span><span class="sxs-lookup"><span data-stu-id="cc42c-276">Indicates whether or not to block voice dialing.</span></span>|
|<span data-ttu-id="cc42c-277">webBrowserBlockPopups</span><span class="sxs-lookup"><span data-stu-id="cc42c-277">webBrowserBlockPopups</span></span>|<span data-ttu-id="cc42c-278">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-278">Boolean</span></span>|<span data-ttu-id="cc42c-279">Indica si se van a bloquear los elementos emergentes en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="cc42c-279">Indicates whether or not to block popups within the web browser.</span></span>|
|<span data-ttu-id="cc42c-280">webBrowserBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="cc42c-280">webBrowserBlockAutofill</span></span>|<span data-ttu-id="cc42c-281">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-281">Boolean</span></span>|<span data-ttu-id="cc42c-282">Indica si se va a bloquear la característica de autorrellenado del explorador web.</span><span class="sxs-lookup"><span data-stu-id="cc42c-282">Indicates whether or not to block the web browser's auto fill feature.</span></span>|
|<span data-ttu-id="cc42c-283">webBrowserBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="cc42c-283">webBrowserBlockJavaScript</span></span>|<span data-ttu-id="cc42c-284">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-284">Boolean</span></span>|<span data-ttu-id="cc42c-285">Indica si se va a bloquear JavaScript en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="cc42c-285">Indicates whether or not to block JavaScript within the web browser.</span></span>|
|<span data-ttu-id="cc42c-286">webBrowserBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-286">webBrowserBlocked</span></span>|<span data-ttu-id="cc42c-287">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-287">Boolean</span></span>|<span data-ttu-id="cc42c-288">Indica si se va a bloquear el explorador web.</span><span class="sxs-lookup"><span data-stu-id="cc42c-288">Indicates whether or not to block the web browser.</span></span>|
|<span data-ttu-id="cc42c-289">webBrowserCookieSettings</span><span class="sxs-lookup"><span data-stu-id="cc42c-289">webBrowserCookieSettings</span></span>|[<span data-ttu-id="cc42c-290">webBrowserCookieSettings</span><span class="sxs-lookup"><span data-stu-id="cc42c-290">webBrowserCookieSettings</span></span>](../resources/intune-deviceconfig-webbrowsercookiesettings.md)|<span data-ttu-id="cc42c-291">Configuración de cookies en el explorador web.</span><span class="sxs-lookup"><span data-stu-id="cc42c-291">Cookie settings within the web browser.</span></span> <span data-ttu-id="cc42c-292">Los valores posibles son: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited` y `allowAlways`.</span><span class="sxs-lookup"><span data-stu-id="cc42c-292">Possible values are: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited`, `allowAlways`.</span></span>|
|<span data-ttu-id="cc42c-293">wiFiBlocked</span><span class="sxs-lookup"><span data-stu-id="cc42c-293">wiFiBlocked</span></span>|<span data-ttu-id="cc42c-294">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-294">Boolean</span></span>|<span data-ttu-id="cc42c-295">Indica si se va a bloquear la sincronización de Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="cc42c-295">Indicates whether or not to block syncing Wi-Fi.</span></span>|
|<span data-ttu-id="cc42c-296">appsInstallAllowList</span><span class="sxs-lookup"><span data-stu-id="cc42c-296">appsInstallAllowList</span></span>|<span data-ttu-id="cc42c-297">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="cc42c-297">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="cc42c-298">Lista de aplicaciones que se pueden instalar en el dispositivo KNOX.</span><span class="sxs-lookup"><span data-stu-id="cc42c-298">List of apps which can be installed on the KNOX device.</span></span> <span data-ttu-id="cc42c-299">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="cc42c-299">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="cc42c-300">appsLaunchBlockList</span><span class="sxs-lookup"><span data-stu-id="cc42c-300">appsLaunchBlockList</span></span>|<span data-ttu-id="cc42c-301">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="cc42c-301">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="cc42c-302">Lista de aplicaciones cuyo inicio en el dispositivo KNOX está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="cc42c-302">List of apps which are blocked from being launched on the KNOX device.</span></span> <span data-ttu-id="cc42c-303">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="cc42c-303">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="cc42c-304">appsHideList</span><span class="sxs-lookup"><span data-stu-id="cc42c-304">appsHideList</span></span>|<span data-ttu-id="cc42c-305">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="cc42c-305">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="cc42c-306">Lista de aplicaciones que se ocultarán en el dispositivo KNOX.</span><span class="sxs-lookup"><span data-stu-id="cc42c-306">List of apps to be hidden on the KNOX device.</span></span> <span data-ttu-id="cc42c-307">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="cc42c-307">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="cc42c-308">securityRequireVerifyApps</span><span class="sxs-lookup"><span data-stu-id="cc42c-308">securityRequireVerifyApps</span></span>|<span data-ttu-id="cc42c-309">Booleano</span><span class="sxs-lookup"><span data-stu-id="cc42c-309">Boolean</span></span>|<span data-ttu-id="cc42c-310">Requerir que la característica Verificar aplicaciones de Android esté activada.</span><span class="sxs-lookup"><span data-stu-id="cc42c-310">Require the Android Verify apps feature is turned on.</span></span>|



## <a name="response"></a><span data-ttu-id="cc42c-311">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc42c-311">Response</span></span>
<span data-ttu-id="cc42c-312">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc42c-312">If successful, this method returns a `201 Created` response code and a [androidGeneralDeviceConfiguration](../resources/intune-deviceconfig-androidgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cc42c-313">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc42c-313">Example</span></span>
### <a name="request"></a><span data-ttu-id="cc42c-314">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc42c-314">Request</span></span>
<span data-ttu-id="cc42c-315">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc42c-315">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="cc42c-316">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc42c-316">Response</span></span>
<span data-ttu-id="cc42c-p120">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cc42c-p120">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



