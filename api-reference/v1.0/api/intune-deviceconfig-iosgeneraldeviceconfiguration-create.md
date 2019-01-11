---
title: Crear iosGeneralDeviceConfiguration
description: Cree un objeto iosGeneralDeviceConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b0cbbc293b549b1276a5ac600ddb276049c7f229
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27838475"
---
# <a name="create-iosgeneraldeviceconfiguration"></a><span data-ttu-id="29e83-103">Crear iosGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="29e83-103">Create iosGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="29e83-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="29e83-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="29e83-105">Crear un objeto [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="29e83-105">Create a new [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="29e83-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="29e83-106">Prerequisites</span></span>
<span data-ttu-id="29e83-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="29e83-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="29e83-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="29e83-109">Permission type</span></span>|<span data-ttu-id="29e83-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="29e83-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="29e83-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="29e83-111">Delegated (work or school account)</span></span>|<span data-ttu-id="29e83-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="29e83-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="29e83-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="29e83-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="29e83-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="29e83-114">Not supported.</span></span>|
|<span data-ttu-id="29e83-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="29e83-115">Application</span></span>|<span data-ttu-id="29e83-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="29e83-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="29e83-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="29e83-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="29e83-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="29e83-118">Request headers</span></span>
|<span data-ttu-id="29e83-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29e83-119">Header</span></span>|<span data-ttu-id="29e83-120">Valor</span><span class="sxs-lookup"><span data-stu-id="29e83-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="29e83-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="29e83-121">Authorization</span></span>|<span data-ttu-id="29e83-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="29e83-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="29e83-123">Accept</span><span class="sxs-lookup"><span data-stu-id="29e83-123">Accept</span></span>|<span data-ttu-id="29e83-124">application/json</span><span class="sxs-lookup"><span data-stu-id="29e83-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="29e83-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="29e83-125">Request body</span></span>
<span data-ttu-id="29e83-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="29e83-126">In the request body, supply a JSON representation for the iosGeneralDeviceConfiguration object.</span></span>

<span data-ttu-id="29e83-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="29e83-127">The following table shows the properties that are required when you create the iosGeneralDeviceConfiguration.</span></span>

|<span data-ttu-id="29e83-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="29e83-128">Property</span></span>|<span data-ttu-id="29e83-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="29e83-129">Type</span></span>|<span data-ttu-id="29e83-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="29e83-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="29e83-131">id</span><span class="sxs-lookup"><span data-stu-id="29e83-131">id</span></span>|<span data-ttu-id="29e83-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="29e83-132">String</span></span>|<span data-ttu-id="29e83-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="29e83-133">Key of the entity.</span></span> <span data-ttu-id="29e83-134">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29e83-134">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29e83-135">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="29e83-135">lastModifiedDateTime</span></span>|<span data-ttu-id="29e83-136">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="29e83-136">DateTimeOffset</span></span>|<span data-ttu-id="29e83-137">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="29e83-137">DateTime the object was last modified.</span></span> <span data-ttu-id="29e83-138">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29e83-138">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29e83-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="29e83-139">createdDateTime</span></span>|<span data-ttu-id="29e83-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="29e83-140">DateTimeOffset</span></span>|<span data-ttu-id="29e83-141">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="29e83-141">DateTime the object was created.</span></span> <span data-ttu-id="29e83-142">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29e83-142">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29e83-143">descripción</span><span class="sxs-lookup"><span data-stu-id="29e83-143">description</span></span>|<span data-ttu-id="29e83-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="29e83-144">String</span></span>|<span data-ttu-id="29e83-145">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29e83-145">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="29e83-146">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29e83-146">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29e83-147">displayName</span><span class="sxs-lookup"><span data-stu-id="29e83-147">displayName</span></span>|<span data-ttu-id="29e83-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="29e83-148">String</span></span>|<span data-ttu-id="29e83-149">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29e83-149">Admin provided name of the device configuration.</span></span> <span data-ttu-id="29e83-150">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29e83-150">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29e83-151">version</span><span class="sxs-lookup"><span data-stu-id="29e83-151">version</span></span>|<span data-ttu-id="29e83-152">Int32</span><span class="sxs-lookup"><span data-stu-id="29e83-152">Int32</span></span>|<span data-ttu-id="29e83-153">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29e83-153">Version of the device configuration.</span></span> <span data-ttu-id="29e83-154">Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="29e83-154">Inherited from [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span></span>|
|<span data-ttu-id="29e83-155">accountBlockModification</span><span class="sxs-lookup"><span data-stu-id="29e83-155">accountBlockModification</span></span>|<span data-ttu-id="29e83-156">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-156">Boolean</span></span>|<span data-ttu-id="29e83-157">Indica si se va a permitir la modificación de cuentas cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-157">Indicates whether or not to allow account modification when the device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-158">activationLockAllowWhenSupervised</span><span class="sxs-lookup"><span data-stu-id="29e83-158">activationLockAllowWhenSupervised</span></span>|<span data-ttu-id="29e83-159">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-159">Boolean</span></span>|<span data-ttu-id="29e83-160">Indica si se va a permitir el bloqueo de activación cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-160">Indicates whether or not to allow activation lock when the device is in the supervised mode.</span></span>|
|<span data-ttu-id="29e83-161">airDropBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-161">airDropBlocked</span></span>|<span data-ttu-id="29e83-162">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-162">Boolean</span></span>|<span data-ttu-id="29e83-163">Indica si se va a permitir AirDrop cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-163">Indicates whether or not to allow AirDrop when the device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-164">airDropForceUnmanagedDropTarget</span><span class="sxs-lookup"><span data-stu-id="29e83-164">airDropForceUnmanagedDropTarget</span></span>|<span data-ttu-id="29e83-165">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-165">Boolean</span></span>|<span data-ttu-id="29e83-166">Indica si se va a hacer que AirDrop se considere un destino de colocación no administrado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-166">Indicates whether or not to cause AirDrop to be considered an unmanaged drop target (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="29e83-167">airPlayForcePairingPasswordForOutgoingRequests</span><span class="sxs-lookup"><span data-stu-id="29e83-167">airPlayForcePairingPasswordForOutgoingRequests</span></span>|<span data-ttu-id="29e83-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-168">Boolean</span></span>|<span data-ttu-id="29e83-169">Indica si se va a forzar que todos los dispositivos que reciban solicitudes de AirPlay de este dispositivo usen una contraseña de emparejamiento.</span><span class="sxs-lookup"><span data-stu-id="29e83-169">Indicates whether or not to enforce all devices receiving AirPlay requests from this device to use a pairing password.</span></span>|
|<span data-ttu-id="29e83-170">appleWatchBlockPairing</span><span class="sxs-lookup"><span data-stu-id="29e83-170">appleWatchBlockPairing</span></span>|<span data-ttu-id="29e83-171">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-171">Boolean</span></span>|<span data-ttu-id="29e83-172">Indica si se va a permitir el emparejamiento con Apple Watch cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-172">Indicates whether or not to allow Apple Watch pairing when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="29e83-173">appleWatchForceWristDetection</span><span class="sxs-lookup"><span data-stu-id="29e83-173">appleWatchForceWristDetection</span></span>|<span data-ttu-id="29e83-174">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-174">Boolean</span></span>|<span data-ttu-id="29e83-175">Indica si se va a forzar que un Apple Watch emparejado use la detección de muñeca (iOS 8.2 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="29e83-175">Indicates whether or not to force a paired Apple Watch to use Wrist Detection (iOS 8.2 and later).</span></span>|
|<span data-ttu-id="29e83-176">appleNewsBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-176">appleNewsBlocked</span></span>|<span data-ttu-id="29e83-177">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-177">Boolean</span></span>|<span data-ttu-id="29e83-178">Indica si se va a impedir que el usuario use Noticias cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-178">Indicates whether or not to block the user from using News when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="29e83-179">appsSingleAppModeList</span><span class="sxs-lookup"><span data-stu-id="29e83-179">appsSingleAppModeList</span></span>|<span data-ttu-id="29e83-180">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="29e83-180">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="29e83-181">Obtiene o establece la lista de aplicaciones permitidas de iOS que pueden entrar de forma autónoma en el Modo de aplicación única.</span><span class="sxs-lookup"><span data-stu-id="29e83-181">Gets or sets the list of iOS apps allowed to autonomously enter Single App Mode.</span></span> <span data-ttu-id="29e83-182">Solo bajo supervisión.</span><span class="sxs-lookup"><span data-stu-id="29e83-182">Supervised only.</span></span> <span data-ttu-id="29e83-183">iOS 7.0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="29e83-183">iOS 7.0 and later.</span></span> <span data-ttu-id="29e83-184">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="29e83-184">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="29e83-185">appsVisibilityList</span><span class="sxs-lookup"><span data-stu-id="29e83-185">appsVisibilityList</span></span>|<span data-ttu-id="29e83-186">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="29e83-186">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="29e83-187">Lista de aplicaciones en la lista de visibilidad (sea la lista de aplicaciones visibles o que se pueden iniciar o la lista de aplicaciones ocultas o que no se pueden iniciar, controlada por AppsVisibilityListType) (iOS 9.3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="29e83-187">List of apps in the visibility list (either visible/launchable apps list or hidden/unlaunchable apps list, controlled by AppsVisibilityListType) (iOS 9.3 and later).</span></span> <span data-ttu-id="29e83-188">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="29e83-188">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="29e83-189">appsVisibilityListType</span><span class="sxs-lookup"><span data-stu-id="29e83-189">appsVisibilityListType</span></span>|[<span data-ttu-id="29e83-190">appListType</span><span class="sxs-lookup"><span data-stu-id="29e83-190">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="29e83-191">Tipo de lista que se encuentra en la AppsVisibilityList.</span><span class="sxs-lookup"><span data-stu-id="29e83-191">Type of list that is in the AppsVisibilityList.</span></span> <span data-ttu-id="29e83-192">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="29e83-192">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="29e83-193">appStoreBlockAutomaticDownloads</span><span class="sxs-lookup"><span data-stu-id="29e83-193">appStoreBlockAutomaticDownloads</span></span>|<span data-ttu-id="29e83-194">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-194">Boolean</span></span>|<span data-ttu-id="29e83-195">Indica si se va a bloquear la descarga automática de aplicaciones compradas en otros dispositivos cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-195">Indicates whether or not to block the automatic downloading of apps purchased on other devices when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="29e83-196">appStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-196">appStoreBlocked</span></span>|<span data-ttu-id="29e83-197">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-197">Boolean</span></span>|<span data-ttu-id="29e83-198">Indica si se va a impedir que el usuario use el App Store.</span><span class="sxs-lookup"><span data-stu-id="29e83-198">Indicates whether or not to block the user from using the App Store.</span></span>|
|<span data-ttu-id="29e83-199">appStoreBlockInAppPurchases</span><span class="sxs-lookup"><span data-stu-id="29e83-199">appStoreBlockInAppPurchases</span></span>|<span data-ttu-id="29e83-200">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-200">Boolean</span></span>|<span data-ttu-id="29e83-201">Indica si se va a impedir que el usuario haga compras en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="29e83-201">Indicates whether or not to block the user from making in app purchases.</span></span>|
|<span data-ttu-id="29e83-202">appStoreBlockUIAppInstallation</span><span class="sxs-lookup"><span data-stu-id="29e83-202">appStoreBlockUIAppInstallation</span></span>|<span data-ttu-id="29e83-203">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-203">Boolean</span></span>|<span data-ttu-id="29e83-204">Indica si se va a bloquear la aplicación App Store, sin restringir la instalación mediante aplicaciones host.</span><span class="sxs-lookup"><span data-stu-id="29e83-204">Indicates whether or not to block the App Store app, not restricting installation through Host apps.</span></span> <span data-ttu-id="29e83-205">Se aplica solo al modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-205">Applies to supervised mode only (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="29e83-206">appStoreRequirePassword</span><span class="sxs-lookup"><span data-stu-id="29e83-206">appStoreRequirePassword</span></span>|<span data-ttu-id="29e83-207">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-207">Boolean</span></span>|<span data-ttu-id="29e83-208">Indica si se va a requerir una contraseña cuando se use la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="29e83-208">Indicates whether or not to require a password when using the app store.</span></span>|
|<span data-ttu-id="29e83-209">bluetoothBlockModification</span><span class="sxs-lookup"><span data-stu-id="29e83-209">bluetoothBlockModification</span></span>|<span data-ttu-id="29e83-210">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-210">Boolean</span></span>|<span data-ttu-id="29e83-211">Indica si se va a permitir la modificación de la configuración Bluetooth cuando el dispositivo está en modo supervisado (iOS 10.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-211">Indicates whether or not to allow modification of Bluetooth settings when the device is in supervised mode (iOS 10.0 and later).</span></span>|
|<span data-ttu-id="29e83-212">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-212">cameraBlocked</span></span>|<span data-ttu-id="29e83-213">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-213">Boolean</span></span>|<span data-ttu-id="29e83-214">Indica si se va a impedir que el usuario obtenga acceso a la cámara del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29e83-214">Indicates whether or not to block the user from accessing the camera of the device.</span></span>|
|<span data-ttu-id="29e83-215">cellularBlockDataRoaming</span><span class="sxs-lookup"><span data-stu-id="29e83-215">cellularBlockDataRoaming</span></span>|<span data-ttu-id="29e83-216">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-216">Boolean</span></span>|<span data-ttu-id="29e83-217">Indica si se va a bloquear la itinerancia de datos.</span><span class="sxs-lookup"><span data-stu-id="29e83-217">Indicates whether or not to block data roaming.</span></span>|
|<span data-ttu-id="29e83-218">cellularBlockGlobalBackgroundFetchWhileRoaming</span><span class="sxs-lookup"><span data-stu-id="29e83-218">cellularBlockGlobalBackgroundFetchWhileRoaming</span></span>|<span data-ttu-id="29e83-219">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-219">Boolean</span></span>|<span data-ttu-id="29e83-220">Indica si se va a impedir la captura de fondo global mientras se está en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="29e83-220">Indicates whether or not to block global background fetch while roaming.</span></span>|
|<span data-ttu-id="29e83-221">cellularBlockPerAppDataModification</span><span class="sxs-lookup"><span data-stu-id="29e83-221">cellularBlockPerAppDataModification</span></span>|<span data-ttu-id="29e83-222">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-222">Boolean</span></span>|<span data-ttu-id="29e83-223">Indica si se van a permitir los cambios en la configuración de uso de datos de aplicaciones de telefonía móvil cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-223">Indicates whether or not to allow changes to cellular app data usage settings when the device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-224">cellularBlockPersonalHotspot</span><span class="sxs-lookup"><span data-stu-id="29e83-224">cellularBlockPersonalHotspot</span></span>|<span data-ttu-id="29e83-225">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-225">Boolean</span></span>|<span data-ttu-id="29e83-226">Indica si se va a bloquear el punto de acceso personal.</span><span class="sxs-lookup"><span data-stu-id="29e83-226">Indicates whether or not to block Personal Hotspot.</span></span>|
|<span data-ttu-id="29e83-227">cellularBlockVoiceRoaming</span><span class="sxs-lookup"><span data-stu-id="29e83-227">cellularBlockVoiceRoaming</span></span>|<span data-ttu-id="29e83-228">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-228">Boolean</span></span>|<span data-ttu-id="29e83-229">Indica si se va a bloquear la itinerancia de voz.</span><span class="sxs-lookup"><span data-stu-id="29e83-229">Indicates whether or not to block voice roaming.</span></span>|
|<span data-ttu-id="29e83-230">certificatesBlockUntrustedTlsCertificates</span><span class="sxs-lookup"><span data-stu-id="29e83-230">certificatesBlockUntrustedTlsCertificates</span></span>|<span data-ttu-id="29e83-231">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-231">Boolean</span></span>|<span data-ttu-id="29e83-232">Indica si se van a bloquear los certificados TLS que no son de confianza.</span><span class="sxs-lookup"><span data-stu-id="29e83-232">Indicates whether or not to block untrusted TLS certificates.</span></span>|
|<span data-ttu-id="29e83-233">classroomAppBlockRemoteScreenObservation</span><span class="sxs-lookup"><span data-stu-id="29e83-233">classroomAppBlockRemoteScreenObservation</span></span>|<span data-ttu-id="29e83-234">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-234">Boolean</span></span>|<span data-ttu-id="29e83-235">Indica si se va a permitir la observación de pantalla remota de la aplicación Classroom cuando el dispositivo está en modo supervisado (iOS 9.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-235">Indicates whether or not to allow remote screen observation by Classroom app when the device is in supervised mode (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="29e83-236">classroomAppForceUnpromptedScreenObservation</span><span class="sxs-lookup"><span data-stu-id="29e83-236">classroomAppForceUnpromptedScreenObservation</span></span>|<span data-ttu-id="29e83-237">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-237">Boolean</span></span>|<span data-ttu-id="29e83-238">Indica si se va a autorizar de forma automática al profesor de un curso administrado en la aplicación Classroom para que vea la pantalla de un alumno sin preguntarle cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-238">Indicates whether or not to automatically give permission to the teacher of a managed course on the Classroom app to view a student's screen without prompting when the device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-239">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="29e83-239">compliantAppsList</span></span>|<span data-ttu-id="29e83-240">Colección [appListItem](../resources/intune-deviceconfig-applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="29e83-240">[appListItem](../resources/intune-deviceconfig-applistitem.md) collection</span></span>|<span data-ttu-id="29e83-241">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="29e83-241">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="29e83-242">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="29e83-242">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="29e83-243">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="29e83-243">compliantAppListType</span></span>|[<span data-ttu-id="29e83-244">appListType</span><span class="sxs-lookup"><span data-stu-id="29e83-244">appListType</span></span>](../resources/intune-deviceconfig-applisttype.md)|<span data-ttu-id="29e83-245">Lista que se encuentra en la AppComplianceList.</span><span class="sxs-lookup"><span data-stu-id="29e83-245">List that is in the AppComplianceList.</span></span> <span data-ttu-id="29e83-246">Los valores posibles son: `none`, `appsInListCompliant` y `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="29e83-246">Possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="29e83-247">configurationProfileBlockChanges</span><span class="sxs-lookup"><span data-stu-id="29e83-247">configurationProfileBlockChanges</span></span>|<span data-ttu-id="29e83-248">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-248">Boolean</span></span>|<span data-ttu-id="29e83-249">Indica si se va a impedir que el usuario instale perfiles de configuración y certificados de forma interactiva cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-249">Indicates whether or not to block the user from installing configuration profiles and certificates interactively when the device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-250">definitionLookupBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-250">definitionLookupBlocked</span></span>|<span data-ttu-id="29e83-251">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-251">Boolean</span></span>|<span data-ttu-id="29e83-252">Indica si se va a bloquear la búsqueda de definiciones cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-252">Indicates whether or not to block definition lookup when the device is in supervised mode (iOS 8.1.3 and later ).</span></span>|
|<span data-ttu-id="29e83-253">deviceBlockEnableRestrictions</span><span class="sxs-lookup"><span data-stu-id="29e83-253">deviceBlockEnableRestrictions</span></span>|<span data-ttu-id="29e83-254">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-254">Boolean</span></span>|<span data-ttu-id="29e83-255">Indica si se va a permitir que el usuario active las restricciones en los ajustes del dispositivo cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-255">Indicates whether or not to allow the user to enables restrictions in the device settings when the device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-256">deviceBlockEraseContentAndSettings</span><span class="sxs-lookup"><span data-stu-id="29e83-256">deviceBlockEraseContentAndSettings</span></span>|<span data-ttu-id="29e83-257">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-257">Boolean</span></span>|<span data-ttu-id="29e83-258">Indica si se va a permitir el uso de la opción "Borrar todo el contenido y la configuración" en el dispositivo cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-258">Indicates whether or not to allow the use of the 'Erase all content and settings' option on the device when the device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-259">deviceBlockNameModification</span><span class="sxs-lookup"><span data-stu-id="29e83-259">deviceBlockNameModification</span></span>|<span data-ttu-id="29e83-260">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-260">Boolean</span></span>|<span data-ttu-id="29e83-261">Indica si se va a permitir modificar el nombre del dispositivo cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-261">Indicates whether or not to allow device name modification when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="29e83-262">diagnosticDataBlockSubmission</span><span class="sxs-lookup"><span data-stu-id="29e83-262">diagnosticDataBlockSubmission</span></span>|<span data-ttu-id="29e83-263">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-263">Boolean</span></span>|<span data-ttu-id="29e83-264">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="29e83-264">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="29e83-265">diagnosticDataBlockSubmissionModification</span><span class="sxs-lookup"><span data-stu-id="29e83-265">diagnosticDataBlockSubmissionModification</span></span>|<span data-ttu-id="29e83-266">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-266">Boolean</span></span>|<span data-ttu-id="29e83-267">Indica si se va a permitir modificar los ajustes del envío de diagnósticos cuando el dispositivo está en modo supervisado (iOS 9.3.2 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-267">Indicates whether or not to allow diagnostics submission settings modification when the device is in supervised mode (iOS 9.3.2 and later).</span></span>|
|<span data-ttu-id="29e83-268">documentsBlockManagedDocumentsInUnmanagedApps</span><span class="sxs-lookup"><span data-stu-id="29e83-268">documentsBlockManagedDocumentsInUnmanagedApps</span></span>|<span data-ttu-id="29e83-269">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-269">Boolean</span></span>|<span data-ttu-id="29e83-270">Indica si se va a impedir que el usuario visualice documentos administrados en las aplicaciones no administradas.</span><span class="sxs-lookup"><span data-stu-id="29e83-270">Indicates whether or not to block the user from viewing managed documents in unmanaged apps.</span></span>|
|<span data-ttu-id="29e83-271">documentsBlockUnmanagedDocumentsInManagedApps</span><span class="sxs-lookup"><span data-stu-id="29e83-271">documentsBlockUnmanagedDocumentsInManagedApps</span></span>|<span data-ttu-id="29e83-272">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-272">Boolean</span></span>|<span data-ttu-id="29e83-273">Indica si se va a impedir que el usuario visualice documentos no administrados en las aplicaciones administradas.</span><span class="sxs-lookup"><span data-stu-id="29e83-273">Indicates whether or not to block the user from viewing unmanaged documents in managed apps.</span></span>|
|<span data-ttu-id="29e83-274">emailInDomainSuffixes</span><span class="sxs-lookup"><span data-stu-id="29e83-274">emailInDomainSuffixes</span></span>|<span data-ttu-id="29e83-275">Colección String</span><span class="sxs-lookup"><span data-stu-id="29e83-275">String collection</span></span>|<span data-ttu-id="29e83-276">Una dirección de correo electrónico que carezca de un sufijo que coincida con cualquiera de estas cadenas se considerará fuera de dominio.</span><span class="sxs-lookup"><span data-stu-id="29e83-276">An email address lacking a suffix that matches any of these strings will be considered out-of-domain.</span></span>|
|<span data-ttu-id="29e83-277">enterpriseAppBlockTrust</span><span class="sxs-lookup"><span data-stu-id="29e83-277">enterpriseAppBlockTrust</span></span>|<span data-ttu-id="29e83-278">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-278">Boolean</span></span>|<span data-ttu-id="29e83-279">Indica si se va a impedir que el usuario confíe en una aplicación empresarial.</span><span class="sxs-lookup"><span data-stu-id="29e83-279">Indicates whether or not to block the user from trusting an enterprise app.</span></span>|
|<span data-ttu-id="29e83-280">enterpriseAppBlockTrustModification</span><span class="sxs-lookup"><span data-stu-id="29e83-280">enterpriseAppBlockTrustModification</span></span>|<span data-ttu-id="29e83-281">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-281">Boolean</span></span>|<span data-ttu-id="29e83-282">Indica si se va a impedir que el usuario modifique la configuración de confianza de una aplicación empresarial.</span><span class="sxs-lookup"><span data-stu-id="29e83-282">Indicates whether or not to block the user from modifying the enterprise app trust settings.</span></span>|
|<span data-ttu-id="29e83-283">faceTimeBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-283">faceTimeBlocked</span></span>|<span data-ttu-id="29e83-284">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-284">Boolean</span></span>|<span data-ttu-id="29e83-285">Indica si se va a impedir que el usuario use FaceTime.</span><span class="sxs-lookup"><span data-stu-id="29e83-285">Indicates whether or not to block the user from using FaceTime.</span></span>|
|<span data-ttu-id="29e83-286">findMyFriendsBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-286">findMyFriendsBlocked</span></span>|<span data-ttu-id="29e83-287">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-287">Boolean</span></span>|<span data-ttu-id="29e83-288">Indica si se va a bloquear Buscar a mis amigos cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-288">Indicates whether or not to block Find My Friends when the device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-289">gamingBlockGameCenterFriends</span><span class="sxs-lookup"><span data-stu-id="29e83-289">gamingBlockGameCenterFriends</span></span>|<span data-ttu-id="29e83-290">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-290">Boolean</span></span>|<span data-ttu-id="29e83-291">Indica si se va a impedir que el usuario tenga amigos en el Game Center.</span><span class="sxs-lookup"><span data-stu-id="29e83-291">Indicates whether or not to block the user from having friends in Game Center.</span></span>|
|<span data-ttu-id="29e83-292">gamingBlockMultiplayer</span><span class="sxs-lookup"><span data-stu-id="29e83-292">gamingBlockMultiplayer</span></span>|<span data-ttu-id="29e83-293">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-293">Boolean</span></span>|<span data-ttu-id="29e83-294">Indica si se va a impedir que el usuario use los juegos multijugador.</span><span class="sxs-lookup"><span data-stu-id="29e83-294">Indicates whether or not to block the user from using multiplayer gaming.</span></span>|
|<span data-ttu-id="29e83-295">gameCenterBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-295">gameCenterBlocked</span></span>|<span data-ttu-id="29e83-296">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-296">Boolean</span></span>|<span data-ttu-id="29e83-297">Indica si se va a impedir que el usuario use el Game Center cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-297">Indicates whether or not to block the user from using Game Center when the device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-298">hostPairingBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-298">hostPairingBlocked</span></span>|<span data-ttu-id="29e83-299">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-299">Boolean</span></span>|<span data-ttu-id="29e83-300">Indica si se va a permitir el emparejamiento de host para controlar los dispositivos con los que se puede emparejar un dispositivo iOS cuando el dispositivo iOS está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-300">indicates whether or not to allow host pairing to control the devices an iOS device can pair with when the iOS device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-301">iBooksStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-301">iBooksStoreBlocked</span></span>|<span data-ttu-id="29e83-302">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-302">Boolean</span></span>|<span data-ttu-id="29e83-303">Indica si se va a impedir que el usuario use iBooks Store cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-303">Indicates whether or not to block the user from using the iBooks Store when the device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-304">iBooksStoreBlockErotica</span><span class="sxs-lookup"><span data-stu-id="29e83-304">iBooksStoreBlockErotica</span></span>|<span data-ttu-id="29e83-305">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-305">Boolean</span></span>|<span data-ttu-id="29e83-306">Indica si se va a impedir que el usuario descargue archivos multimedia desde el iBook Store que se han etiquetado como eróticos.</span><span class="sxs-lookup"><span data-stu-id="29e83-306">Indicates whether or not to block the user from downloading media from the iBookstore that has been tagged as erotica.</span></span>|
|<span data-ttu-id="29e83-307">iCloudBlockActivityContinuation</span><span class="sxs-lookup"><span data-stu-id="29e83-307">iCloudBlockActivityContinuation</span></span>|<span data-ttu-id="29e83-308">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-308">Boolean</span></span>|<span data-ttu-id="29e83-309">Indica si se va a impedir que el usuario continúe con el trabajo que empezó en el dispositivo iOS en otro dispositivo macOS o iOS.</span><span class="sxs-lookup"><span data-stu-id="29e83-309">Indicates whether or not to block  the the user from continuing work they started on iOS device to another iOS or macOS device.</span></span>|
|<span data-ttu-id="29e83-310">iCloudBlockBackup</span><span class="sxs-lookup"><span data-stu-id="29e83-310">iCloudBlockBackup</span></span>|<span data-ttu-id="29e83-311">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-311">Boolean</span></span>|<span data-ttu-id="29e83-312">Indica si se va a impedir la copia de seguridad de iCloud.</span><span class="sxs-lookup"><span data-stu-id="29e83-312">Indicates whether or not to block iCloud backup.</span></span>|
|<span data-ttu-id="29e83-313">iCloudBlockDocumentSync</span><span class="sxs-lookup"><span data-stu-id="29e83-313">iCloudBlockDocumentSync</span></span>|<span data-ttu-id="29e83-314">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-314">Boolean</span></span>|<span data-ttu-id="29e83-315">Indica si se va a impedir la sincronización de documentos de iCloud.</span><span class="sxs-lookup"><span data-stu-id="29e83-315">Indicates whether or not to block iCloud document sync.</span></span>|
|<span data-ttu-id="29e83-316">iCloudBlockManagedAppsSync</span><span class="sxs-lookup"><span data-stu-id="29e83-316">iCloudBlockManagedAppsSync</span></span>|<span data-ttu-id="29e83-317">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-317">Boolean</span></span>|<span data-ttu-id="29e83-318">Indica si se va a impedir la sincronización en la nube de aplicaciones administradas.</span><span class="sxs-lookup"><span data-stu-id="29e83-318">Indicates whether or not to block Managed Apps Cloud Sync.</span></span>|
|<span data-ttu-id="29e83-319">iCloudBlockPhotoLibrary</span><span class="sxs-lookup"><span data-stu-id="29e83-319">iCloudBlockPhotoLibrary</span></span>|<span data-ttu-id="29e83-320">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-320">Boolean</span></span>|<span data-ttu-id="29e83-321">Indica si se va a bloquear la Fototeca de iCloud.</span><span class="sxs-lookup"><span data-stu-id="29e83-321">Indicates whether or not to block iCloud Photo Library.</span></span>|
|<span data-ttu-id="29e83-322">iCloudBlockPhotoStreamSync</span><span class="sxs-lookup"><span data-stu-id="29e83-322">iCloudBlockPhotoStreamSync</span></span>|<span data-ttu-id="29e83-323">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-323">Boolean</span></span>|<span data-ttu-id="29e83-324">Indica si se va a bloquear la sincronización de fotos en streaming de iCloud.</span><span class="sxs-lookup"><span data-stu-id="29e83-324">Indicates whether or not to block iCloud Photo Stream Sync.</span></span>|
|<span data-ttu-id="29e83-325">iCloudBlockSharedPhotoStream</span><span class="sxs-lookup"><span data-stu-id="29e83-325">iCloudBlockSharedPhotoStream</span></span>|<span data-ttu-id="29e83-326">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-326">Boolean</span></span>|<span data-ttu-id="29e83-327">Indica si se va a bloquear la sincronización de fotos en streaming compartidas.</span><span class="sxs-lookup"><span data-stu-id="29e83-327">Indicates whether or not to block Shared Photo Stream.</span></span>|
|<span data-ttu-id="29e83-328">iCloudRequireEncryptedBackup</span><span class="sxs-lookup"><span data-stu-id="29e83-328">iCloudRequireEncryptedBackup</span></span>|<span data-ttu-id="29e83-329">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-329">Boolean</span></span>|<span data-ttu-id="29e83-330">Indica si se va a requerir que las copias de seguridad de iCloud estén cifradas.</span><span class="sxs-lookup"><span data-stu-id="29e83-330">Indicates whether or not to require backups to iCloud be encrypted.</span></span>|
|<span data-ttu-id="29e83-331">iTunesBlockExplicitContent</span><span class="sxs-lookup"><span data-stu-id="29e83-331">iTunesBlockExplicitContent</span></span>|<span data-ttu-id="29e83-332">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-332">Boolean</span></span>|<span data-ttu-id="29e83-333">Indica si se va a impedir que el usuario obtenga acceso a contenido explícito en iTunes y el App Store.</span><span class="sxs-lookup"><span data-stu-id="29e83-333">Indicates whether or not to block the user from accessing explicit content in iTunes and the App Store.</span></span>|
|<span data-ttu-id="29e83-334">iTunesBlockMusicService</span><span class="sxs-lookup"><span data-stu-id="29e83-334">iTunesBlockMusicService</span></span>|<span data-ttu-id="29e83-335">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-335">Boolean</span></span>|<span data-ttu-id="29e83-336">Indica si se va a bloquear el servicio Música y revertir la aplicación Música al modo clásico cuando el dispositivo está en modo supervisado (iOS 9.3 y versiones posteriores, y macOS 10.12 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="29e83-336">Indicates whether or not to block Music service and revert Music app to classic mode when the device is in supervised mode (iOS 9.3 and later and macOS 10.12 and later).</span></span>|
|<span data-ttu-id="29e83-337">iTunesBlockRadio</span><span class="sxs-lookup"><span data-stu-id="29e83-337">iTunesBlockRadio</span></span>|<span data-ttu-id="29e83-338">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-338">Boolean</span></span>|<span data-ttu-id="29e83-339">Indica si se va a impedir que el usuario use iTunes Radio cuando el dispositivo está en modo supervisado (iOS 9.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-339">Indicates whether or not to block the user from using iTunes Radio when the device is in supervised mode (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="29e83-340">keyboardBlockAutoCorrect</span><span class="sxs-lookup"><span data-stu-id="29e83-340">keyboardBlockAutoCorrect</span></span>|<span data-ttu-id="29e83-341">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-341">Boolean</span></span>|<span data-ttu-id="29e83-342">Indica si se va a bloquear el autocorrector cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-342">Indicates whether or not to block keyboard auto-correction when the device is in supervised mode (iOS 8.1.3 and later).</span></span>|
|<span data-ttu-id="29e83-343">keyboardBlockDictation</span><span class="sxs-lookup"><span data-stu-id="29e83-343">keyboardBlockDictation</span></span>|<span data-ttu-id="29e83-344">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-344">Boolean</span></span>|<span data-ttu-id="29e83-345">Indica si se va a impedir que el usuario use la entrada dictada cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-345">Indicates whether or not to block the user from using dictation input when the device is in supervised mode.</span></span>|
|<span data-ttu-id="29e83-346">keyboardBlockPredictive</span><span class="sxs-lookup"><span data-stu-id="29e83-346">keyboardBlockPredictive</span></span>|<span data-ttu-id="29e83-347">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-347">Boolean</span></span>|<span data-ttu-id="29e83-348">Indica si se van a bloquear los teclados predictivos cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-348">Indicates whether or not to block predictive keyboards when device is in supervised mode (iOS 8.1.3 and later).</span></span>|
|<span data-ttu-id="29e83-349">keyboardBlockShortcuts</span><span class="sxs-lookup"><span data-stu-id="29e83-349">keyboardBlockShortcuts</span></span>|<span data-ttu-id="29e83-350">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-350">Boolean</span></span>|<span data-ttu-id="29e83-351">Indica si se van a bloquear los atajos del teclado cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-351">Indicates whether or not to block keyboard shortcuts when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="29e83-352">keyboardBlockSpellCheck</span><span class="sxs-lookup"><span data-stu-id="29e83-352">keyboardBlockSpellCheck</span></span>|<span data-ttu-id="29e83-353">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-353">Boolean</span></span>|<span data-ttu-id="29e83-354">Indica si se va a bloquear la revisión ortográfica cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-354">Indicates whether or not to block keyboard spell-checking when the device is in supervised mode (iOS 8.1.3 and later).</span></span>|
|<span data-ttu-id="29e83-355">kioskModeAllowAssistiveSpeak</span><span class="sxs-lookup"><span data-stu-id="29e83-355">kioskModeAllowAssistiveSpeak</span></span>|<span data-ttu-id="29e83-356">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-356">Boolean</span></span>|<span data-ttu-id="29e83-357">Indica si se va a permitir la lectura de asistencia en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-357">Indicates whether or not to allow assistive speak while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-358">kioskModeAllowAssistiveTouchSettings</span><span class="sxs-lookup"><span data-stu-id="29e83-358">kioskModeAllowAssistiveTouchSettings</span></span>|<span data-ttu-id="29e83-359">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-359">Boolean</span></span>|<span data-ttu-id="29e83-360">Indica si se va a permitir el acceso a la configuración de AssistiveTouch en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-360">Indicates whether or not to allow access to the Assistive Touch Settings while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-361">kioskModeAllowAutoLock</span><span class="sxs-lookup"><span data-stu-id="29e83-361">kioskModeAllowAutoLock</span></span>|<span data-ttu-id="29e83-362">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-362">Boolean</span></span>|<span data-ttu-id="29e83-363">Indica si se va a permitir el bloqueo automático del dispositivo en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-363">Indicates whether or not to allow device auto lock while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-364">kioskModeAllowColorInversionSettings</span><span class="sxs-lookup"><span data-stu-id="29e83-364">kioskModeAllowColorInversionSettings</span></span>|<span data-ttu-id="29e83-365">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-365">Boolean</span></span>|<span data-ttu-id="29e83-366">Indica si se va a permitir el acceso a la configuración de la inversión del color en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-366">Indicates whether or not to allow access to the Color Inversion Settings while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-367">kioskModeAllowRingerSwitch</span><span class="sxs-lookup"><span data-stu-id="29e83-367">kioskModeAllowRingerSwitch</span></span>|<span data-ttu-id="29e83-368">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-368">Boolean</span></span>|<span data-ttu-id="29e83-369">Indica si se va a permitir el uso del cambio de tono en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-369">Indicates whether or not to allow use of the ringer switch while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-370">kioskModeAllowScreenRotation</span><span class="sxs-lookup"><span data-stu-id="29e83-370">kioskModeAllowScreenRotation</span></span>|<span data-ttu-id="29e83-371">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-371">Boolean</span></span>|<span data-ttu-id="29e83-372">Indica si se va a permitir la rotación de pantalla en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-372">Indicates whether or not to allow screen rotation while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-373">kioskModeAllowSleepButton</span><span class="sxs-lookup"><span data-stu-id="29e83-373">kioskModeAllowSleepButton</span></span>|<span data-ttu-id="29e83-374">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-374">Boolean</span></span>|<span data-ttu-id="29e83-375">Indica si se va a permitir el uso del botón de suspensión en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-375">Indicates whether or not to allow use of the sleep button while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-376">kioskModeAllowTouchscreen</span><span class="sxs-lookup"><span data-stu-id="29e83-376">kioskModeAllowTouchscreen</span></span>|<span data-ttu-id="29e83-377">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-377">Boolean</span></span>|<span data-ttu-id="29e83-378">Indica si se va a permitir el uso de la pantalla táctil en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-378">Indicates whether or not to allow use of the touchscreen while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-379">kioskModeAllowVoiceOverSettings</span><span class="sxs-lookup"><span data-stu-id="29e83-379">kioskModeAllowVoiceOverSettings</span></span>|<span data-ttu-id="29e83-380">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-380">Boolean</span></span>|<span data-ttu-id="29e83-381">Indica si se va a permitir el acceso a la configuración de voz en off en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-381">Indicates whether or not to allow access to the voice over settings while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-382">kioskModeAllowVolumeButtons</span><span class="sxs-lookup"><span data-stu-id="29e83-382">kioskModeAllowVolumeButtons</span></span>|<span data-ttu-id="29e83-383">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-383">Boolean</span></span>|<span data-ttu-id="29e83-384">Indica si se va a permitir el uso de los botones de volumen en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-384">Indicates whether or not to allow use of the volume buttons while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-385">kioskModeAllowZoomSettings</span><span class="sxs-lookup"><span data-stu-id="29e83-385">kioskModeAllowZoomSettings</span></span>|<span data-ttu-id="29e83-386">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-386">Boolean</span></span>|<span data-ttu-id="29e83-387">Indica si se va a permitir el acceso a la configuración de zoom en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-387">Indicates whether or not to allow access to the zoom settings while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-388">kioskModeAppStoreUrl</span><span class="sxs-lookup"><span data-stu-id="29e83-388">kioskModeAppStoreUrl</span></span>|<span data-ttu-id="29e83-389">Cadena</span><span class="sxs-lookup"><span data-stu-id="29e83-389">String</span></span>|<span data-ttu-id="29e83-390">Dirección URL en la tienda de aplicaciones a la aplicación que se usará para el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-390">URL in the app store to the app to use for kiosk mode.</span></span> <span data-ttu-id="29e83-391">Úsela si KioskModeManagedAppId es desconocido.</span><span class="sxs-lookup"><span data-stu-id="29e83-391">Use if KioskModeManagedAppId is not known.</span></span>|
|<span data-ttu-id="29e83-392">kioskModeBuiltInAppId</span><span class="sxs-lookup"><span data-stu-id="29e83-392">kioskModeBuiltInAppId</span></span>|<span data-ttu-id="29e83-393">Cadena</span><span class="sxs-lookup"><span data-stu-id="29e83-393">String</span></span>|<span data-ttu-id="29e83-394">Identificador de aplicaciones integradas que se usará para el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-394">ID for built-in apps to use for kiosk mode.</span></span> <span data-ttu-id="29e83-395">Se usa cuando no se establecen KioskModeManagedAppId y KioskModeAppStoreUrl.</span><span class="sxs-lookup"><span data-stu-id="29e83-395">Used when KioskModeManagedAppId and KioskModeAppStoreUrl are not set.</span></span>|
|<span data-ttu-id="29e83-396">kioskModeRequireAssistiveTouch</span><span class="sxs-lookup"><span data-stu-id="29e83-396">kioskModeRequireAssistiveTouch</span></span>|<span data-ttu-id="29e83-397">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-397">Boolean</span></span>|<span data-ttu-id="29e83-398">Indica si se va a requerir la AssistiveTouch en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-398">Indicates whether or not to require assistive touch while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-399">kioskModeRequireColorInversion</span><span class="sxs-lookup"><span data-stu-id="29e83-399">kioskModeRequireColorInversion</span></span>|<span data-ttu-id="29e83-400">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-400">Boolean</span></span>|<span data-ttu-id="29e83-401">Indica si se va a requerir la inversión de color en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-401">Indicates whether or not to require color inversion while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-402">kioskModeRequireMonoAudio</span><span class="sxs-lookup"><span data-stu-id="29e83-402">kioskModeRequireMonoAudio</span></span>|<span data-ttu-id="29e83-403">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-403">Boolean</span></span>|<span data-ttu-id="29e83-404">Indica si se va a requerir el audio mono en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-404">Indicates whether or not to require mono audio while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-405">kioskModeRequireVoiceOver</span><span class="sxs-lookup"><span data-stu-id="29e83-405">kioskModeRequireVoiceOver</span></span>|<span data-ttu-id="29e83-406">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-406">Boolean</span></span>|<span data-ttu-id="29e83-407">Indica si se va a requerir la voz en off en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-407">Indicates whether or not to require voice over while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-408">kioskModeRequireZoom</span><span class="sxs-lookup"><span data-stu-id="29e83-408">kioskModeRequireZoom</span></span>|<span data-ttu-id="29e83-409">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-409">Boolean</span></span>|<span data-ttu-id="29e83-410">Indica si se va a requerir el zoom en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-410">Indicates whether or not to require zoom while in kiosk mode.</span></span>|
|<span data-ttu-id="29e83-411">kioskModeManagedAppId</span><span class="sxs-lookup"><span data-stu-id="29e83-411">kioskModeManagedAppId</span></span>|<span data-ttu-id="29e83-412">Cadena</span><span class="sxs-lookup"><span data-stu-id="29e83-412">String</span></span>|<span data-ttu-id="29e83-413">identificador de la aplicación administrada de la aplicación que se usará para el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29e83-413">Managed app id of the app to use for kiosk mode.</span></span> <span data-ttu-id="29e83-414">Si se especifica KioskModeManagedAppId, entonces se omitirá KioskModeAppStoreUrl.</span><span class="sxs-lookup"><span data-stu-id="29e83-414">If KioskModeManagedAppId is specified then KioskModeAppStoreUrl will be ignored.</span></span>|
|<span data-ttu-id="29e83-415">lockScreenBlockControlCenter</span><span class="sxs-lookup"><span data-stu-id="29e83-415">lockScreenBlockControlCenter</span></span>|<span data-ttu-id="29e83-416">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-416">Boolean</span></span>|<span data-ttu-id="29e83-417">Indica si se va a impedir que el usuario use el centro de control en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="29e83-417">Indicates whether or not to block the user from using control center on the lock screen.</span></span>|
|<span data-ttu-id="29e83-418">lockScreenBlockNotificationView</span><span class="sxs-lookup"><span data-stu-id="29e83-418">lockScreenBlockNotificationView</span></span>|<span data-ttu-id="29e83-419">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-419">Boolean</span></span>|<span data-ttu-id="29e83-420">Indica si se va a impedir que el usuario use la visualización de notificaciones en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="29e83-420">Indicates whether or not to block the user from using the notification view on the lock screen.</span></span>|
|<span data-ttu-id="29e83-421">lockScreenBlockPassbook</span><span class="sxs-lookup"><span data-stu-id="29e83-421">lockScreenBlockPassbook</span></span>|<span data-ttu-id="29e83-422">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-422">Boolean</span></span>|<span data-ttu-id="29e83-423">Indica si se va a impedir que el usuario use Passbook cuando el dispositivo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="29e83-423">Indicates whether or not to block the user from using passbook when the device is locked.</span></span>|
|<span data-ttu-id="29e83-424">lockScreenBlockTodayView</span><span class="sxs-lookup"><span data-stu-id="29e83-424">lockScreenBlockTodayView</span></span>|<span data-ttu-id="29e83-425">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-425">Boolean</span></span>|<span data-ttu-id="29e83-426">Indica si se va a impedir que el usuario use la vista Hoy en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="29e83-426">Indicates whether or not to block the user from using the Today View on the lock screen.</span></span>|
|<span data-ttu-id="29e83-427">mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="29e83-427">mediaContentRatingAustralia</span></span>|[<span data-ttu-id="29e83-428">mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="29e83-428">mediaContentRatingAustralia</span></span>](../resources/intune-deviceconfig-mediacontentratingaustralia.md)|<span data-ttu-id="29e83-429">Clasificación de contenido multimedia para Australia</span><span class="sxs-lookup"><span data-stu-id="29e83-429">Media content rating settings for Australia</span></span>|
|<span data-ttu-id="29e83-430">mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="29e83-430">mediaContentRatingCanada</span></span>|[<span data-ttu-id="29e83-431">mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="29e83-431">mediaContentRatingCanada</span></span>](../resources/intune-deviceconfig-mediacontentratingcanada.md)|<span data-ttu-id="29e83-432">Clasificación de contenido multimedia para Canadá</span><span class="sxs-lookup"><span data-stu-id="29e83-432">Media content rating settings for Canada</span></span>|
|<span data-ttu-id="29e83-433">mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="29e83-433">mediaContentRatingFrance</span></span>|[<span data-ttu-id="29e83-434">mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="29e83-434">mediaContentRatingFrance</span></span>](../resources/intune-deviceconfig-mediacontentratingfrance.md)|<span data-ttu-id="29e83-435">Clasificación de contenido multimedia para Francia</span><span class="sxs-lookup"><span data-stu-id="29e83-435">Media content rating settings for France</span></span>|
|<span data-ttu-id="29e83-436">mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="29e83-436">mediaContentRatingGermany</span></span>|[<span data-ttu-id="29e83-437">mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="29e83-437">mediaContentRatingGermany</span></span>](../resources/intune-deviceconfig-mediacontentratinggermany.md)|<span data-ttu-id="29e83-438">Clasificación de contenido multimedia para Alemania</span><span class="sxs-lookup"><span data-stu-id="29e83-438">Media content rating settings for Germany</span></span>|
|<span data-ttu-id="29e83-439">mediaContentRatingIreland</span><span class="sxs-lookup"><span data-stu-id="29e83-439">mediaContentRatingIreland</span></span>|[<span data-ttu-id="29e83-440">mediaContentRatingIreland</span><span class="sxs-lookup"><span data-stu-id="29e83-440">mediaContentRatingIreland</span></span>](../resources/intune-deviceconfig-mediacontentratingireland.md)|<span data-ttu-id="29e83-441">Clasificación de contenido multimedia para Irlanda</span><span class="sxs-lookup"><span data-stu-id="29e83-441">Media content rating settings for Ireland</span></span>|
|<span data-ttu-id="29e83-442">mediaContentRatingJapan</span><span class="sxs-lookup"><span data-stu-id="29e83-442">mediaContentRatingJapan</span></span>|[<span data-ttu-id="29e83-443">mediaContentRatingJapan</span><span class="sxs-lookup"><span data-stu-id="29e83-443">mediaContentRatingJapan</span></span>](../resources/intune-deviceconfig-mediacontentratingjapan.md)|<span data-ttu-id="29e83-444">Clasificación de contenido multimedia para Japón</span><span class="sxs-lookup"><span data-stu-id="29e83-444">Media content rating settings for Japan</span></span>|
|<span data-ttu-id="29e83-445">mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="29e83-445">mediaContentRatingNewZealand</span></span>|[<span data-ttu-id="29e83-446">mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="29e83-446">mediaContentRatingNewZealand</span></span>](../resources/intune-deviceconfig-mediacontentratingnewzealand.md)|<span data-ttu-id="29e83-447">Clasificación de contenido multimedia para Nueva Zelanda</span><span class="sxs-lookup"><span data-stu-id="29e83-447">Media content rating settings for New Zealand</span></span>|
|<span data-ttu-id="29e83-448">mediaContentRatingUnitedKingdom</span><span class="sxs-lookup"><span data-stu-id="29e83-448">mediaContentRatingUnitedKingdom</span></span>|[<span data-ttu-id="29e83-449">mediaContentRatingUnitedKingdom</span><span class="sxs-lookup"><span data-stu-id="29e83-449">mediaContentRatingUnitedKingdom</span></span>](../resources/intune-deviceconfig-mediacontentratingunitedkingdom.md)|<span data-ttu-id="29e83-450">Clasificación de contenido multimedia para el Reino Unido</span><span class="sxs-lookup"><span data-stu-id="29e83-450">Media content rating settings for United Kingdom</span></span>|
|<span data-ttu-id="29e83-451">mediaContentRatingUnitedStates</span><span class="sxs-lookup"><span data-stu-id="29e83-451">mediaContentRatingUnitedStates</span></span>|[<span data-ttu-id="29e83-452">mediaContentRatingUnitedStates</span><span class="sxs-lookup"><span data-stu-id="29e83-452">mediaContentRatingUnitedStates</span></span>](../resources/intune-deviceconfig-mediacontentratingunitedstates.md)|<span data-ttu-id="29e83-453">Clasificación de contenido multimedia para Estados Unidos</span><span class="sxs-lookup"><span data-stu-id="29e83-453">Media content rating settings for United States</span></span>|
|<span data-ttu-id="29e83-454">networkUsageRules</span><span class="sxs-lookup"><span data-stu-id="29e83-454">networkUsageRules</span></span>|<span data-ttu-id="29e83-455">Colección [iosNetworkUsageRule](../resources/intune-deviceconfig-iosnetworkusagerule.md)</span><span class="sxs-lookup"><span data-stu-id="29e83-455">[iosNetworkUsageRule](../resources/intune-deviceconfig-iosnetworkusagerule.md) collection</span></span>|<span data-ttu-id="29e83-456">Lista de aplicaciones administradas y las reglas de red que se les aplican.</span><span class="sxs-lookup"><span data-stu-id="29e83-456">List of managed apps and the network rules that applies to them.</span></span> <span data-ttu-id="29e83-457">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="29e83-457">This collection can contain a maximum of 1000 elements.</span></span>|
|<span data-ttu-id="29e83-458">mediaContentRatingApps</span><span class="sxs-lookup"><span data-stu-id="29e83-458">mediaContentRatingApps</span></span>|[<span data-ttu-id="29e83-459">ratingAppsType</span><span class="sxs-lookup"><span data-stu-id="29e83-459">ratingAppsType</span></span>](../resources/intune-deviceconfig-ratingappstype.md)|<span data-ttu-id="29e83-460">Configuración de clasificación para las aplicaciones de contenido de medios.</span><span class="sxs-lookup"><span data-stu-id="29e83-460">Media content rating settings for Apps.</span></span> <span data-ttu-id="29e83-461">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove4`, `agesAbove9`, `agesAbove12`, `agesAbove17`.</span><span class="sxs-lookup"><span data-stu-id="29e83-461">Possible values are: `allAllowed`, `allBlocked`, `agesAbove4`, `agesAbove9`, `agesAbove12`, `agesAbove17`.</span></span>|
|<span data-ttu-id="29e83-462">messagesBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-462">messagesBlocked</span></span>|<span data-ttu-id="29e83-463">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-463">Boolean</span></span>|<span data-ttu-id="29e83-464">Indica si se va a impedir que el usuario use la aplicación Mensajes en el dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-464">Indicates whether or not to block the user from using the Messages app on the supervised device.</span></span>|
|<span data-ttu-id="29e83-465">notificationsBlockSettingsModification</span><span class="sxs-lookup"><span data-stu-id="29e83-465">notificationsBlockSettingsModification</span></span>|<span data-ttu-id="29e83-466">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-466">Boolean</span></span>|<span data-ttu-id="29e83-467">Indica si se van a permitir modificar la configuración de las notificaciones (iOS 9,3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="29e83-467">Indicates whether or not to allow notifications settings modification (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="29e83-468">passcodeBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="29e83-468">passcodeBlockFingerprintUnlock</span></span>|<span data-ttu-id="29e83-469">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-469">Boolean</span></span>|<span data-ttu-id="29e83-470">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="29e83-470">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="29e83-471">passcodeBlockFingerprintModification</span><span class="sxs-lookup"><span data-stu-id="29e83-471">passcodeBlockFingerprintModification</span></span>|<span data-ttu-id="29e83-472">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-472">Boolean</span></span>|<span data-ttu-id="29e83-473">Impide la modificación de huellas digitales registradas de Touch ID en el modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-473">Block modification of registered Touch ID fingerprints when in supervised mode.</span></span>|
|<span data-ttu-id="29e83-474">passcodeBlockModification</span><span class="sxs-lookup"><span data-stu-id="29e83-474">passcodeBlockModification</span></span>|<span data-ttu-id="29e83-475">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-475">Boolean</span></span>|<span data-ttu-id="29e83-476">Indica si se va a permitir modificar los códigos de acceso cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-476">Indicates whether or not to allow passcode modification on the supervised device (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="29e83-477">passcodeBlockSimple</span><span class="sxs-lookup"><span data-stu-id="29e83-477">passcodeBlockSimple</span></span>|<span data-ttu-id="29e83-478">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-478">Boolean</span></span>|<span data-ttu-id="29e83-479">Indica si se van a bloquear los códigos de acceso simples.</span><span class="sxs-lookup"><span data-stu-id="29e83-479">Indicates whether or not to block simple passcodes.</span></span>|
|<span data-ttu-id="29e83-480">passcodeExpirationDays</span><span class="sxs-lookup"><span data-stu-id="29e83-480">passcodeExpirationDays</span></span>|<span data-ttu-id="29e83-481">Int32</span><span class="sxs-lookup"><span data-stu-id="29e83-481">Int32</span></span>|<span data-ttu-id="29e83-482">Número de días antes de que expire el código de acceso.</span><span class="sxs-lookup"><span data-stu-id="29e83-482">Number of days before the passcode expires.</span></span> <span data-ttu-id="29e83-483">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="29e83-483">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="29e83-484">passcodeMinimumLength</span><span class="sxs-lookup"><span data-stu-id="29e83-484">passcodeMinimumLength</span></span>|<span data-ttu-id="29e83-485">Int32</span><span class="sxs-lookup"><span data-stu-id="29e83-485">Int32</span></span>|<span data-ttu-id="29e83-486">Longitud mínima de los códigos de acceso.</span><span class="sxs-lookup"><span data-stu-id="29e83-486">Minimum length of passcode.</span></span> <span data-ttu-id="29e83-487">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="29e83-487">Valid values 4 to 14</span></span>|
|<span data-ttu-id="29e83-488">passcodeMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="29e83-488">passcodeMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="29e83-489">Int32</span><span class="sxs-lookup"><span data-stu-id="29e83-489">Int32</span></span>|<span data-ttu-id="29e83-490">Minutos de inactividad antes de que sea necesario un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="29e83-490">Minutes of inactivity before a passcode is required.</span></span>|
|<span data-ttu-id="29e83-491">passcodeMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="29e83-491">passcodeMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="29e83-492">Int32</span><span class="sxs-lookup"><span data-stu-id="29e83-492">Int32</span></span>|<span data-ttu-id="29e83-493">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="29e83-493">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="29e83-494">passcodeMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="29e83-494">passcodeMinimumCharacterSetCount</span></span>|<span data-ttu-id="29e83-495">Int32</span><span class="sxs-lookup"><span data-stu-id="29e83-495">Int32</span></span>|<span data-ttu-id="29e83-496">Número de juegos de caracteres que debe contener un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="29e83-496">Number of character sets a passcode must contain.</span></span> <span data-ttu-id="29e83-497">Valores válidos de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="29e83-497">Valid values 0 to 4</span></span>|
|<span data-ttu-id="29e83-498">passcodePreviousPasscodeBlockCount</span><span class="sxs-lookup"><span data-stu-id="29e83-498">passcodePreviousPasscodeBlockCount</span></span>|<span data-ttu-id="29e83-499">Int32</span><span class="sxs-lookup"><span data-stu-id="29e83-499">Int32</span></span>|<span data-ttu-id="29e83-500">Número de códigos de acceso anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="29e83-500">Number of previous passcodes to block.</span></span> <span data-ttu-id="29e83-501">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="29e83-501">Valid values 1 to 24</span></span>|
|<span data-ttu-id="29e83-502">passcodeSignInFailureCountBeforeWipe</span><span class="sxs-lookup"><span data-stu-id="29e83-502">passcodeSignInFailureCountBeforeWipe</span></span>|<span data-ttu-id="29e83-503">Int32</span><span class="sxs-lookup"><span data-stu-id="29e83-503">Int32</span></span>|<span data-ttu-id="29e83-504">Número de errores de inicio de sesión permitidos antes de borrar los datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29e83-504">Number of sign in failures allowed before wiping the device.</span></span> <span data-ttu-id="29e83-505">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="29e83-505">Valid values 4 to 11</span></span>|
|<span data-ttu-id="29e83-506">passcodeRequiredType</span><span class="sxs-lookup"><span data-stu-id="29e83-506">passcodeRequiredType</span></span>|[<span data-ttu-id="29e83-507">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="29e83-507">requiredPasswordType</span></span>](../resources/intune-deviceconfig-requiredpasswordtype.md)|<span data-ttu-id="29e83-508">Tipo de código de acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="29e83-508">Type of passcode that is required.</span></span> <span data-ttu-id="29e83-509">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="29e83-509">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="29e83-510">passcodeRequired</span><span class="sxs-lookup"><span data-stu-id="29e83-510">passcodeRequired</span></span>|<span data-ttu-id="29e83-511">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-511">Boolean</span></span>|<span data-ttu-id="29e83-512">Indica si se va a requerir un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="29e83-512">Indicates whether or not to require a passcode.</span></span>|
|<span data-ttu-id="29e83-513">podcastsBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-513">podcastsBlocked</span></span>|<span data-ttu-id="29e83-514">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-514">Boolean</span></span>|<span data-ttu-id="29e83-515">Indica si se va a impedir que el usuario use Podcasts cuando el dispositivo está en modo supervisado (iOS 8.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-515">Indicates whether or not to block the user from using podcasts on the supervised device (iOS 8.0 and later).</span></span>|
|<span data-ttu-id="29e83-516">safariBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="29e83-516">safariBlockAutofill</span></span>|<span data-ttu-id="29e83-517">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-517">Boolean</span></span>|<span data-ttu-id="29e83-518">Indica si se va a impedir que el usuario use la opción de autorrellenado en Safari.</span><span class="sxs-lookup"><span data-stu-id="29e83-518">Indicates whether or not to block the user from using Auto fill in Safari.</span></span>|
|<span data-ttu-id="29e83-519">safariBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="29e83-519">safariBlockJavaScript</span></span>|<span data-ttu-id="29e83-520">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-520">Boolean</span></span>|<span data-ttu-id="29e83-521">Indica si se va a bloquear JavaScript en Safari.</span><span class="sxs-lookup"><span data-stu-id="29e83-521">Indicates whether or not to block JavaScript in Safari.</span></span>|
|<span data-ttu-id="29e83-522">safariBlockPopups</span><span class="sxs-lookup"><span data-stu-id="29e83-522">safariBlockPopups</span></span>|<span data-ttu-id="29e83-523">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-523">Boolean</span></span>|<span data-ttu-id="29e83-524">Indica si se van a bloquear los elementos emergentes en Safari.</span><span class="sxs-lookup"><span data-stu-id="29e83-524">Indicates whether or not to block popups in Safari.</span></span>|
|<span data-ttu-id="29e83-525">safariBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-525">safariBlocked</span></span>|<span data-ttu-id="29e83-526">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-526">Boolean</span></span>|<span data-ttu-id="29e83-527">Indica si se va a impedir que el usuario use Safari.</span><span class="sxs-lookup"><span data-stu-id="29e83-527">Indicates whether or not to block the user from using Safari.</span></span>|
|<span data-ttu-id="29e83-528">safariCookieSettings</span><span class="sxs-lookup"><span data-stu-id="29e83-528">safariCookieSettings</span></span>|[<span data-ttu-id="29e83-529">webBrowserCookieSettings</span><span class="sxs-lookup"><span data-stu-id="29e83-529">webBrowserCookieSettings</span></span>](../resources/intune-deviceconfig-webbrowsercookiesettings.md)|<span data-ttu-id="29e83-530">Configuración de cookies para Safari.</span><span class="sxs-lookup"><span data-stu-id="29e83-530">Cookie settings for Safari.</span></span> <span data-ttu-id="29e83-531">Los valores posibles son: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited` y `allowAlways`.</span><span class="sxs-lookup"><span data-stu-id="29e83-531">Possible values are: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited`, `allowAlways`.</span></span>|
|<span data-ttu-id="29e83-532">safariManagedDomains</span><span class="sxs-lookup"><span data-stu-id="29e83-532">safariManagedDomains</span></span>|<span data-ttu-id="29e83-533">Colección String</span><span class="sxs-lookup"><span data-stu-id="29e83-533">String collection</span></span>|<span data-ttu-id="29e83-534">Las direcciones URL que coinciden con los patrones que se enumeran aquí se considerarán administradas.</span><span class="sxs-lookup"><span data-stu-id="29e83-534">URLs matching the patterns listed here will be considered managed.</span></span>|
|<span data-ttu-id="29e83-535">safariPasswordAutoFillDomains</span><span class="sxs-lookup"><span data-stu-id="29e83-535">safariPasswordAutoFillDomains</span></span>|<span data-ttu-id="29e83-536">Colección String</span><span class="sxs-lookup"><span data-stu-id="29e83-536">String collection</span></span>|<span data-ttu-id="29e83-537">Los usuarios pueden guardar las contraseñas en Safari únicamente de las direcciones URL que coinciden con los patrones que se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="29e83-537">Users can save passwords in Safari only from URLs matching the patterns listed here.</span></span> <span data-ttu-id="29e83-538">Se aplica solo a dispositivos en modo supervisado (iOS 9.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-538">Applies to devices in supervised mode (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="29e83-539">safariRequireFraudWarning</span><span class="sxs-lookup"><span data-stu-id="29e83-539">safariRequireFraudWarning</span></span>|<span data-ttu-id="29e83-540">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-540">Boolean</span></span>|<span data-ttu-id="29e83-541">Indica si se va a requerir una advertencia de fraude en Safari.</span><span class="sxs-lookup"><span data-stu-id="29e83-541">Indicates whether or not to require fraud warning in Safari.</span></span>|
|<span data-ttu-id="29e83-542">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-542">screenCaptureBlocked</span></span>|<span data-ttu-id="29e83-543">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-543">Boolean</span></span>|<span data-ttu-id="29e83-544">Indica si se impide o no que el usuario tome capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="29e83-544">Indicates whether or not to block the user from taking Screenshots.</span></span>|
|<span data-ttu-id="29e83-545">siriBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-545">siriBlocked</span></span>|<span data-ttu-id="29e83-546">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-546">Boolean</span></span>|<span data-ttu-id="29e83-547">Indica si se va a impedir que el usuario use Siri.</span><span class="sxs-lookup"><span data-stu-id="29e83-547">Indicates whether or not to block the user from using Siri.</span></span>|
|<span data-ttu-id="29e83-548">siriBlockedWhenLocked</span><span class="sxs-lookup"><span data-stu-id="29e83-548">siriBlockedWhenLocked</span></span>|<span data-ttu-id="29e83-549">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-549">Boolean</span></span>|<span data-ttu-id="29e83-550">Indica si se va a impedir que el usuario use Siri cuando está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="29e83-550">Indicates whether or not to block the user from using Siri when locked.</span></span>|
|<span data-ttu-id="29e83-551">siriBlockUserGeneratedContent</span><span class="sxs-lookup"><span data-stu-id="29e83-551">siriBlockUserGeneratedContent</span></span>|<span data-ttu-id="29e83-552">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-552">Boolean</span></span>|<span data-ttu-id="29e83-553">Indica si se va a impedir que Siri haga consultas de contenido generado por el usuario cuando se usa en un dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-553">Indicates whether or not to block Siri from querying user-generated content when used on a supervised device.</span></span>|
|<span data-ttu-id="29e83-554">siriRequireProfanityFilter</span><span class="sxs-lookup"><span data-stu-id="29e83-554">siriRequireProfanityFilter</span></span>|<span data-ttu-id="29e83-555">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-555">Boolean</span></span>|<span data-ttu-id="29e83-556">Indica si se va a evitar que Siri dicte o hable con lenguaje irreverente en un dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-556">Indicates whether or not to prevent Siri from dictating, or speaking profane language on supervised device.</span></span>|
|<span data-ttu-id="29e83-557">spotlightBlockInternetResults</span><span class="sxs-lookup"><span data-stu-id="29e83-557">spotlightBlockInternetResults</span></span>|<span data-ttu-id="29e83-558">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-558">Boolean</span></span>|<span data-ttu-id="29e83-559">Indica si se va a impedir que la búsqueda Spotlight devuelva resultados de Internet en un dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-559">Indicates whether or not to block Spotlight search from returning internet results on supervised device.</span></span>|
|<span data-ttu-id="29e83-560">voiceDialingBlocked</span><span class="sxs-lookup"><span data-stu-id="29e83-560">voiceDialingBlocked</span></span>|<span data-ttu-id="29e83-561">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-561">Boolean</span></span>|<span data-ttu-id="29e83-562">Indica si se va a bloquear la marcación por voz.</span><span class="sxs-lookup"><span data-stu-id="29e83-562">Indicates whether or not to block voice dialing.</span></span>|
|<span data-ttu-id="29e83-563">wallpaperBlockModification</span><span class="sxs-lookup"><span data-stu-id="29e83-563">wallpaperBlockModification</span></span>|<span data-ttu-id="29e83-564">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-564">Boolean</span></span>|<span data-ttu-id="29e83-565">Indica si se va permitir modificar el fondo de pantalla en un dispositivo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="29e83-565">Indicates whether or not to allow wallpaper modification on supervised device (iOS 9.0 and later) .</span></span>|
|<span data-ttu-id="29e83-566">wiFiConnectOnlyToConfiguredNetworks</span><span class="sxs-lookup"><span data-stu-id="29e83-566">wiFiConnectOnlyToConfiguredNetworks</span></span>|<span data-ttu-id="29e83-567">Booleano</span><span class="sxs-lookup"><span data-stu-id="29e83-567">Boolean</span></span>|<span data-ttu-id="29e83-568">Indica si se va a forzar al dispositivo para que use solo redes Wi-Fi de perfiles de configuración cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="29e83-568">Indicates whether or not to force the device to use only Wi-Fi networks from configuration profiles when the device is in supervised mode.</span></span>|



## <a name="response"></a><span data-ttu-id="29e83-569">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29e83-569">Response</span></span>
<span data-ttu-id="29e83-570">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="29e83-570">If successful, this method returns a `201 Created` response code and a [iosGeneralDeviceConfiguration](../resources/intune-deviceconfig-iosgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="29e83-571">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="29e83-571">Example</span></span>
### <a name="request"></a><span data-ttu-id="29e83-572">Solicitud</span><span class="sxs-lookup"><span data-stu-id="29e83-572">Request</span></span>
<span data-ttu-id="29e83-573">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="29e83-573">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 7841

{
  "@odata.type": "#microsoft.graph.iosGeneralDeviceConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountBlockModification": true,
  "activationLockAllowWhenSupervised": true,
  "airDropBlocked": true,
  "airDropForceUnmanagedDropTarget": true,
  "airPlayForcePairingPasswordForOutgoingRequests": true,
  "appleWatchBlockPairing": true,
  "appleWatchForceWristDetection": true,
  "appleNewsBlocked": true,
  "appsSingleAppModeList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityListType": "appsInListCompliant",
  "appStoreBlockAutomaticDownloads": true,
  "appStoreBlocked": true,
  "appStoreBlockInAppPurchases": true,
  "appStoreBlockUIAppInstallation": true,
  "appStoreRequirePassword": true,
  "bluetoothBlockModification": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockGlobalBackgroundFetchWhileRoaming": true,
  "cellularBlockPerAppDataModification": true,
  "cellularBlockPersonalHotspot": true,
  "cellularBlockVoiceRoaming": true,
  "certificatesBlockUntrustedTlsCertificates": true,
  "classroomAppBlockRemoteScreenObservation": true,
  "classroomAppForceUnpromptedScreenObservation": true,
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
  "configurationProfileBlockChanges": true,
  "definitionLookupBlocked": true,
  "deviceBlockEnableRestrictions": true,
  "deviceBlockEraseContentAndSettings": true,
  "deviceBlockNameModification": true,
  "diagnosticDataBlockSubmission": true,
  "diagnosticDataBlockSubmissionModification": true,
  "documentsBlockManagedDocumentsInUnmanagedApps": true,
  "documentsBlockUnmanagedDocumentsInManagedApps": true,
  "emailInDomainSuffixes": [
    "Email In Domain Suffixes value"
  ],
  "enterpriseAppBlockTrust": true,
  "enterpriseAppBlockTrustModification": true,
  "faceTimeBlocked": true,
  "findMyFriendsBlocked": true,
  "gamingBlockGameCenterFriends": true,
  "gamingBlockMultiplayer": true,
  "gameCenterBlocked": true,
  "hostPairingBlocked": true,
  "iBooksStoreBlocked": true,
  "iBooksStoreBlockErotica": true,
  "iCloudBlockActivityContinuation": true,
  "iCloudBlockBackup": true,
  "iCloudBlockDocumentSync": true,
  "iCloudBlockManagedAppsSync": true,
  "iCloudBlockPhotoLibrary": true,
  "iCloudBlockPhotoStreamSync": true,
  "iCloudBlockSharedPhotoStream": true,
  "iCloudRequireEncryptedBackup": true,
  "iTunesBlockExplicitContent": true,
  "iTunesBlockMusicService": true,
  "iTunesBlockRadio": true,
  "keyboardBlockAutoCorrect": true,
  "keyboardBlockDictation": true,
  "keyboardBlockPredictive": true,
  "keyboardBlockShortcuts": true,
  "keyboardBlockSpellCheck": true,
  "kioskModeAllowAssistiveSpeak": true,
  "kioskModeAllowAssistiveTouchSettings": true,
  "kioskModeAllowAutoLock": true,
  "kioskModeAllowColorInversionSettings": true,
  "kioskModeAllowRingerSwitch": true,
  "kioskModeAllowScreenRotation": true,
  "kioskModeAllowSleepButton": true,
  "kioskModeAllowTouchscreen": true,
  "kioskModeAllowVoiceOverSettings": true,
  "kioskModeAllowVolumeButtons": true,
  "kioskModeAllowZoomSettings": true,
  "kioskModeAppStoreUrl": "https://example.com/kioskModeAppStoreUrl/",
  "kioskModeBuiltInAppId": "Kiosk Mode Built In App Id value",
  "kioskModeRequireAssistiveTouch": true,
  "kioskModeRequireColorInversion": true,
  "kioskModeRequireMonoAudio": true,
  "kioskModeRequireVoiceOver": true,
  "kioskModeRequireZoom": true,
  "kioskModeManagedAppId": "Kiosk Mode Managed App Id value",
  "lockScreenBlockControlCenter": true,
  "lockScreenBlockNotificationView": true,
  "lockScreenBlockPassbook": true,
  "lockScreenBlockTodayView": true,
  "mediaContentRatingAustralia": {
    "@odata.type": "microsoft.graph.mediaContentRatingAustralia",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingCanada": {
    "@odata.type": "microsoft.graph.mediaContentRatingCanada",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingFrance": {
    "@odata.type": "microsoft.graph.mediaContentRatingFrance",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingGermany": {
    "@odata.type": "microsoft.graph.mediaContentRatingGermany",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingIreland": {
    "@odata.type": "microsoft.graph.mediaContentRatingIreland",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingJapan": {
    "@odata.type": "microsoft.graph.mediaContentRatingJapan",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingNewZealand": {
    "@odata.type": "microsoft.graph.mediaContentRatingNewZealand",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedKingdom": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedStates": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "networkUsageRules": [
    {
      "@odata.type": "microsoft.graph.iosNetworkUsageRule",
      "managedApps": [
        {
          "@odata.type": "microsoft.graph.appListItem",
          "name": "Name value",
          "publisher": "Publisher value",
          "appStoreUrl": "https://example.com/appStoreUrl/",
          "appId": "App Id value"
        }
      ],
      "cellularDataBlockWhenRoaming": true,
      "cellularDataBlocked": true
    }
  ],
  "mediaContentRatingApps": "allBlocked",
  "messagesBlocked": true,
  "notificationsBlockSettingsModification": true,
  "passcodeBlockFingerprintUnlock": true,
  "passcodeBlockFingerprintModification": true,
  "passcodeBlockModification": true,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 6,
  "passcodeMinimumLength": 5,
  "passcodeMinutesOfInactivityBeforeLock": 5,
  "passcodeMinutesOfInactivityBeforeScreenTimeout": 14,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeSignInFailureCountBeforeWipe": 4,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "podcastsBlocked": true,
  "safariBlockAutofill": true,
  "safariBlockJavaScript": true,
  "safariBlockPopups": true,
  "safariBlocked": true,
  "safariCookieSettings": "blockAlways",
  "safariManagedDomains": [
    "Safari Managed Domains value"
  ],
  "safariPasswordAutoFillDomains": [
    "Safari Password Auto Fill Domains value"
  ],
  "safariRequireFraudWarning": true,
  "screenCaptureBlocked": true,
  "siriBlocked": true,
  "siriBlockedWhenLocked": true,
  "siriBlockUserGeneratedContent": true,
  "siriRequireProfanityFilter": true,
  "spotlightBlockInternetResults": true,
  "voiceDialingBlocked": true,
  "wallpaperBlockModification": true,
  "wiFiConnectOnlyToConfiguredNetworks": true
}
```

### <a name="response"></a><span data-ttu-id="29e83-574">Respuesta</span><span class="sxs-lookup"><span data-stu-id="29e83-574">Response</span></span>
<span data-ttu-id="29e83-p127">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="29e83-p127">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 8013

{
  "@odata.type": "#microsoft.graph.iosGeneralDeviceConfiguration",
  "id": "ebba5202-5202-ebba-0252-baeb0252baeb",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "accountBlockModification": true,
  "activationLockAllowWhenSupervised": true,
  "airDropBlocked": true,
  "airDropForceUnmanagedDropTarget": true,
  "airPlayForcePairingPasswordForOutgoingRequests": true,
  "appleWatchBlockPairing": true,
  "appleWatchForceWristDetection": true,
  "appleNewsBlocked": true,
  "appsSingleAppModeList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityList": [
    {
      "@odata.type": "microsoft.graph.appListItem",
      "name": "Name value",
      "publisher": "Publisher value",
      "appStoreUrl": "https://example.com/appStoreUrl/",
      "appId": "App Id value"
    }
  ],
  "appsVisibilityListType": "appsInListCompliant",
  "appStoreBlockAutomaticDownloads": true,
  "appStoreBlocked": true,
  "appStoreBlockInAppPurchases": true,
  "appStoreBlockUIAppInstallation": true,
  "appStoreRequirePassword": true,
  "bluetoothBlockModification": true,
  "cameraBlocked": true,
  "cellularBlockDataRoaming": true,
  "cellularBlockGlobalBackgroundFetchWhileRoaming": true,
  "cellularBlockPerAppDataModification": true,
  "cellularBlockPersonalHotspot": true,
  "cellularBlockVoiceRoaming": true,
  "certificatesBlockUntrustedTlsCertificates": true,
  "classroomAppBlockRemoteScreenObservation": true,
  "classroomAppForceUnpromptedScreenObservation": true,
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
  "configurationProfileBlockChanges": true,
  "definitionLookupBlocked": true,
  "deviceBlockEnableRestrictions": true,
  "deviceBlockEraseContentAndSettings": true,
  "deviceBlockNameModification": true,
  "diagnosticDataBlockSubmission": true,
  "diagnosticDataBlockSubmissionModification": true,
  "documentsBlockManagedDocumentsInUnmanagedApps": true,
  "documentsBlockUnmanagedDocumentsInManagedApps": true,
  "emailInDomainSuffixes": [
    "Email In Domain Suffixes value"
  ],
  "enterpriseAppBlockTrust": true,
  "enterpriseAppBlockTrustModification": true,
  "faceTimeBlocked": true,
  "findMyFriendsBlocked": true,
  "gamingBlockGameCenterFriends": true,
  "gamingBlockMultiplayer": true,
  "gameCenterBlocked": true,
  "hostPairingBlocked": true,
  "iBooksStoreBlocked": true,
  "iBooksStoreBlockErotica": true,
  "iCloudBlockActivityContinuation": true,
  "iCloudBlockBackup": true,
  "iCloudBlockDocumentSync": true,
  "iCloudBlockManagedAppsSync": true,
  "iCloudBlockPhotoLibrary": true,
  "iCloudBlockPhotoStreamSync": true,
  "iCloudBlockSharedPhotoStream": true,
  "iCloudRequireEncryptedBackup": true,
  "iTunesBlockExplicitContent": true,
  "iTunesBlockMusicService": true,
  "iTunesBlockRadio": true,
  "keyboardBlockAutoCorrect": true,
  "keyboardBlockDictation": true,
  "keyboardBlockPredictive": true,
  "keyboardBlockShortcuts": true,
  "keyboardBlockSpellCheck": true,
  "kioskModeAllowAssistiveSpeak": true,
  "kioskModeAllowAssistiveTouchSettings": true,
  "kioskModeAllowAutoLock": true,
  "kioskModeAllowColorInversionSettings": true,
  "kioskModeAllowRingerSwitch": true,
  "kioskModeAllowScreenRotation": true,
  "kioskModeAllowSleepButton": true,
  "kioskModeAllowTouchscreen": true,
  "kioskModeAllowVoiceOverSettings": true,
  "kioskModeAllowVolumeButtons": true,
  "kioskModeAllowZoomSettings": true,
  "kioskModeAppStoreUrl": "https://example.com/kioskModeAppStoreUrl/",
  "kioskModeBuiltInAppId": "Kiosk Mode Built In App Id value",
  "kioskModeRequireAssistiveTouch": true,
  "kioskModeRequireColorInversion": true,
  "kioskModeRequireMonoAudio": true,
  "kioskModeRequireVoiceOver": true,
  "kioskModeRequireZoom": true,
  "kioskModeManagedAppId": "Kiosk Mode Managed App Id value",
  "lockScreenBlockControlCenter": true,
  "lockScreenBlockNotificationView": true,
  "lockScreenBlockPassbook": true,
  "lockScreenBlockTodayView": true,
  "mediaContentRatingAustralia": {
    "@odata.type": "microsoft.graph.mediaContentRatingAustralia",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingCanada": {
    "@odata.type": "microsoft.graph.mediaContentRatingCanada",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingFrance": {
    "@odata.type": "microsoft.graph.mediaContentRatingFrance",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingGermany": {
    "@odata.type": "microsoft.graph.mediaContentRatingGermany",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingIreland": {
    "@odata.type": "microsoft.graph.mediaContentRatingIreland",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingJapan": {
    "@odata.type": "microsoft.graph.mediaContentRatingJapan",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingNewZealand": {
    "@odata.type": "microsoft.graph.mediaContentRatingNewZealand",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedKingdom": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedKingdom",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "mediaContentRatingUnitedStates": {
    "@odata.type": "microsoft.graph.mediaContentRatingUnitedStates",
    "movieRating": "allBlocked",
    "tvRating": "allBlocked"
  },
  "networkUsageRules": [
    {
      "@odata.type": "microsoft.graph.iosNetworkUsageRule",
      "managedApps": [
        {
          "@odata.type": "microsoft.graph.appListItem",
          "name": "Name value",
          "publisher": "Publisher value",
          "appStoreUrl": "https://example.com/appStoreUrl/",
          "appId": "App Id value"
        }
      ],
      "cellularDataBlockWhenRoaming": true,
      "cellularDataBlocked": true
    }
  ],
  "mediaContentRatingApps": "allBlocked",
  "messagesBlocked": true,
  "notificationsBlockSettingsModification": true,
  "passcodeBlockFingerprintUnlock": true,
  "passcodeBlockFingerprintModification": true,
  "passcodeBlockModification": true,
  "passcodeBlockSimple": true,
  "passcodeExpirationDays": 6,
  "passcodeMinimumLength": 5,
  "passcodeMinutesOfInactivityBeforeLock": 5,
  "passcodeMinutesOfInactivityBeforeScreenTimeout": 14,
  "passcodeMinimumCharacterSetCount": 0,
  "passcodePreviousPasscodeBlockCount": 2,
  "passcodeSignInFailureCountBeforeWipe": 4,
  "passcodeRequiredType": "alphanumeric",
  "passcodeRequired": true,
  "podcastsBlocked": true,
  "safariBlockAutofill": true,
  "safariBlockJavaScript": true,
  "safariBlockPopups": true,
  "safariBlocked": true,
  "safariCookieSettings": "blockAlways",
  "safariManagedDomains": [
    "Safari Managed Domains value"
  ],
  "safariPasswordAutoFillDomains": [
    "Safari Password Auto Fill Domains value"
  ],
  "safariRequireFraudWarning": true,
  "screenCaptureBlocked": true,
  "siriBlocked": true,
  "siriBlockedWhenLocked": true,
  "siriBlockUserGeneratedContent": true,
  "siriRequireProfanityFilter": true,
  "spotlightBlockInternetResults": true,
  "voiceDialingBlocked": true,
  "wallpaperBlockModification": true,
  "wiFiConnectOnlyToConfiguredNetworks": true
}
```



