# <a name="create-iosgeneraldeviceconfiguration"></a><span data-ttu-id="aa592-101">Crear iosGeneralDeviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="aa592-101">Create iosGeneralDeviceConfiguration</span></span>

> <span data-ttu-id="aa592-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="aa592-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="aa592-103">Crear un objeto [iosGeneralDeviceConfiguration](../resources/intune_deviceconfig_iosgeneraldeviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="aa592-103">Create a new [iosGeneralDeviceConfiguration](../resources/intune_deviceconfig_iosgeneraldeviceconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="aa592-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="aa592-104">Prerequisites</span></span>
<span data-ttu-id="aa592-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="aa592-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="aa592-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="aa592-107">Permission type</span></span>|<span data-ttu-id="aa592-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="aa592-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="aa592-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="aa592-109">Delegated (work or school account)</span></span>|<span data-ttu-id="aa592-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="aa592-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="aa592-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="aa592-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="aa592-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa592-112">Not supported.</span></span>|
|<span data-ttu-id="aa592-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="aa592-113">Application</span></span>|<span data-ttu-id="aa592-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="aa592-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="aa592-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="aa592-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="aa592-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="aa592-116">Request headers</span></span>
|<span data-ttu-id="aa592-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aa592-117">Header</span></span>|<span data-ttu-id="aa592-118">Valor</span><span class="sxs-lookup"><span data-stu-id="aa592-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="aa592-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="aa592-119">Authorization</span></span>|<span data-ttu-id="aa592-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="aa592-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="aa592-121">Accept</span><span class="sxs-lookup"><span data-stu-id="aa592-121">Accept</span></span>|<span data-ttu-id="aa592-122">application/json</span><span class="sxs-lookup"><span data-stu-id="aa592-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="aa592-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="aa592-123">Request body</span></span>
<span data-ttu-id="aa592-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="aa592-124">In the request body, supply a JSON representation for the iosGeneralDeviceConfiguration object.</span></span>

<span data-ttu-id="aa592-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosGeneralDeviceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="aa592-125">The following table shows the properties that are required when you create the iosGeneralDeviceConfiguration.</span></span>

|<span data-ttu-id="aa592-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aa592-126">Property</span></span>|<span data-ttu-id="aa592-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="aa592-127">Type</span></span>|<span data-ttu-id="aa592-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa592-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="aa592-129">id</span><span class="sxs-lookup"><span data-stu-id="aa592-129">id</span></span>|<span data-ttu-id="aa592-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="aa592-130">String</span></span>|<span data-ttu-id="aa592-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="aa592-131">Key of the entity.</span></span> <span data-ttu-id="aa592-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa592-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa592-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="aa592-133">lastModifiedDateTime</span></span>|<span data-ttu-id="aa592-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aa592-134">DateTimeOffset</span></span>|<span data-ttu-id="aa592-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="aa592-135">DateTime the object was last modified.</span></span> <span data-ttu-id="aa592-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa592-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa592-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="aa592-137">createdDateTime</span></span>|<span data-ttu-id="aa592-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="aa592-138">DateTimeOffset</span></span>|<span data-ttu-id="aa592-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="aa592-139">DateTime the object was created.</span></span> <span data-ttu-id="aa592-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa592-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa592-141">description</span><span class="sxs-lookup"><span data-stu-id="aa592-141">description</span></span>|<span data-ttu-id="aa592-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="aa592-142">String</span></span>|<span data-ttu-id="aa592-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa592-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="aa592-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa592-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa592-145">displayName</span><span class="sxs-lookup"><span data-stu-id="aa592-145">displayName</span></span>|<span data-ttu-id="aa592-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="aa592-146">String</span></span>|<span data-ttu-id="aa592-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa592-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="aa592-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa592-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa592-149">version</span><span class="sxs-lookup"><span data-stu-id="aa592-149">version</span></span>|<span data-ttu-id="aa592-150">Int32</span><span class="sxs-lookup"><span data-stu-id="aa592-150">Int32</span></span>|<span data-ttu-id="aa592-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa592-151">Version of the device configuration.</span></span> <span data-ttu-id="aa592-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="aa592-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="aa592-153">accountBlockModification</span><span class="sxs-lookup"><span data-stu-id="aa592-153">accountBlockModification</span></span>|<span data-ttu-id="aa592-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-154">Boolean</span></span>|<span data-ttu-id="aa592-155">Indica si se va a permitir la modificación de cuentas cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-155">Indicates whether or not to allow account modification when the device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-156">activationLockAllowWhenSupervised</span><span class="sxs-lookup"><span data-stu-id="aa592-156">activationLockAllowWhenSupervised</span></span>|<span data-ttu-id="aa592-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-157">Boolean</span></span>|<span data-ttu-id="aa592-158">Indica si se va a permitir el bloqueo de activación cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-158">Indicates whether or not to allow activation lock when the device is in the supervised mode.</span></span>|
|<span data-ttu-id="aa592-159">airDropBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-159">airDropBlocked</span></span>|<span data-ttu-id="aa592-160">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-160">Boolean</span></span>|<span data-ttu-id="aa592-161">Indica si se va a permitir AirDrop cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-161">Indicates whether or not to allow AirDrop when the device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-162">airDropForceUnmanagedDropTarget</span><span class="sxs-lookup"><span data-stu-id="aa592-162">airDropForceUnmanagedDropTarget</span></span>|<span data-ttu-id="aa592-163">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-163">Boolean</span></span>|<span data-ttu-id="aa592-164">Indica si se va a hacer que AirDrop se considere un destino de colocación no administrado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-164">Indicates whether or not to cause AirDrop to be considered an unmanaged drop target (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="aa592-165">airPlayForcePairingPasswordForOutgoingRequests</span><span class="sxs-lookup"><span data-stu-id="aa592-165">airPlayForcePairingPasswordForOutgoingRequests</span></span>|<span data-ttu-id="aa592-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-166">Boolean</span></span>|<span data-ttu-id="aa592-167">Indica si se va a forzar que todos los dispositivos que reciban solicitudes de AirPlay de este dispositivo usen una contraseña de emparejamiento.</span><span class="sxs-lookup"><span data-stu-id="aa592-167">Indicates whether or not to enforce all devices receiving AirPlay requests from this device to use a pairing password.</span></span>|
|<span data-ttu-id="aa592-168">appleWatchBlockPairing</span><span class="sxs-lookup"><span data-stu-id="aa592-168">appleWatchBlockPairing</span></span>|<span data-ttu-id="aa592-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-169">Boolean</span></span>|<span data-ttu-id="aa592-170">Indica si se va a permitir el emparejamiento con Apple Watch cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-170">Indicates whether or not to allow Apple Watch pairing when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="aa592-171">appleWatchForceWristDetection</span><span class="sxs-lookup"><span data-stu-id="aa592-171">appleWatchForceWristDetection</span></span>|<span data-ttu-id="aa592-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-172">Boolean</span></span>|<span data-ttu-id="aa592-173">Indica si se va a forzar que un Apple Watch emparejado use la detección de muñeca (iOS 8.2 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="aa592-173">Indicates whether or not to force a paired Apple Watch to use Wrist Detection (iOS 8.2 and later).</span></span>|
|<span data-ttu-id="aa592-174">appleNewsBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-174">appleNewsBlocked</span></span>|<span data-ttu-id="aa592-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-175">Boolean</span></span>|<span data-ttu-id="aa592-176">Indica si se va a impedir que el usuario use Noticias cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-176">Indicates whether or not to block the user from using News when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="aa592-177">appsSingleAppModeList</span><span class="sxs-lookup"><span data-stu-id="aa592-177">appsSingleAppModeList</span></span>|<span data-ttu-id="aa592-178">Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="aa592-178">[appListItem](../resources/intune_deviceconfig_applistitem.md) collection</span></span>|<span data-ttu-id="aa592-179">Obtiene o establece la lista de aplicaciones permitidas de iOS que pueden entrar de forma autónoma en el Modo de aplicación única.</span><span class="sxs-lookup"><span data-stu-id="aa592-179">Gets or sets the list of iOS apps allowed to autonomously enter Single App Mode.</span></span> <span data-ttu-id="aa592-180">Solo bajo supervisión.</span><span class="sxs-lookup"><span data-stu-id="aa592-180">Supervised only.</span></span> <span data-ttu-id="aa592-181">iOS 7.0 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="aa592-181">iOS 7.0 and later.</span></span> <span data-ttu-id="aa592-182">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="aa592-182">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="aa592-183">appsVisibilityList</span><span class="sxs-lookup"><span data-stu-id="aa592-183">appsVisibilityList</span></span>|<span data-ttu-id="aa592-184">Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="aa592-184">[appListItem](../resources/intune_deviceconfig_applistitem.md) collection</span></span>|<span data-ttu-id="aa592-185">Lista de aplicaciones en la lista de visibilidad (sea la lista de aplicaciones visibles o que se pueden iniciar o la lista de aplicaciones ocultas o que no se pueden iniciar, controlada por AppsVisibilityListType) (iOS 9.3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="aa592-185">List of apps in the visibility list (either visible/launchable apps list or hidden/unlaunchable apps list, controlled by AppsVisibilityListType) (iOS 9.3 and later).</span></span> <span data-ttu-id="aa592-186">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="aa592-186">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="aa592-187">appsVisibilityListType</span><span class="sxs-lookup"><span data-stu-id="aa592-187">appsVisibilityListType</span></span>|[<span data-ttu-id="aa592-188">appListType</span><span class="sxs-lookup"><span data-stu-id="aa592-188">appListType</span></span>](../resources/intune_deviceconfig_applisttype.md)|<span data-ttu-id="aa592-p110">Tipo de lista que se encuentra en la CompliantAppsList. Los valores posibles son: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="aa592-p110">Type of list that is in the AppsVisibilityList. The possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="aa592-191">appStoreBlockAutomaticDownloads</span><span class="sxs-lookup"><span data-stu-id="aa592-191">appStoreBlockAutomaticDownloads</span></span>|<span data-ttu-id="aa592-192">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-192">Boolean</span></span>|<span data-ttu-id="aa592-193">Indica si se va a bloquear la descarga automática de aplicaciones compradas en otros dispositivos cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-193">Indicates whether or not to block the automatic downloading of apps purchased on other devices when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="aa592-194">appStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-194">appStoreBlocked</span></span>|<span data-ttu-id="aa592-195">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-195">Boolean</span></span>|<span data-ttu-id="aa592-196">Indica si se va a impedir que el usuario use el App Store.</span><span class="sxs-lookup"><span data-stu-id="aa592-196">Indicates whether or not to block the user from using the App Store.</span></span>|
|<span data-ttu-id="aa592-197">appStoreBlockInAppPurchases</span><span class="sxs-lookup"><span data-stu-id="aa592-197">appStoreBlockInAppPurchases</span></span>|<span data-ttu-id="aa592-198">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-198">Boolean</span></span>|<span data-ttu-id="aa592-199">Indica si se va a impedir que el usuario haga compras en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="aa592-199">Indicates whether or not to block the user from making in app purchases.</span></span>|
|<span data-ttu-id="aa592-200">appStoreBlockUIAppInstallation</span><span class="sxs-lookup"><span data-stu-id="aa592-200">appStoreBlockUIAppInstallation</span></span>|<span data-ttu-id="aa592-201">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-201">Boolean</span></span>|<span data-ttu-id="aa592-202">Indica si se va a bloquear la aplicación App Store, sin restringir la instalación mediante aplicaciones host.</span><span class="sxs-lookup"><span data-stu-id="aa592-202">Indicates whether or not to block the App Store app, not restricting installation through Host apps.</span></span> <span data-ttu-id="aa592-203">Se aplica solo al modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-203">Applies to supervised mode only (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="aa592-204">appStoreRequirePassword</span><span class="sxs-lookup"><span data-stu-id="aa592-204">appStoreRequirePassword</span></span>|<span data-ttu-id="aa592-205">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-205">Boolean</span></span>|<span data-ttu-id="aa592-206">Indica si se va a requerir una contraseña cuando se use la tienda de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="aa592-206">Indicates whether or not to require a password when using the app store.</span></span>|
|<span data-ttu-id="aa592-207">bluetoothBlockModification</span><span class="sxs-lookup"><span data-stu-id="aa592-207">bluetoothBlockModification</span></span>|<span data-ttu-id="aa592-208">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-208">Boolean</span></span>|<span data-ttu-id="aa592-209">Indica si se va a permitir la modificación de la configuración Bluetooth cuando el dispositivo está en modo supervisado (iOS 10.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-209">Indicates whether or not to allow modification of Bluetooth settings when the device is in supervised mode (iOS 10.0 and later).</span></span>|
|<span data-ttu-id="aa592-210">cameraBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-210">cameraBlocked</span></span>|<span data-ttu-id="aa592-211">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-211">Boolean</span></span>|<span data-ttu-id="aa592-212">Indica si se va a impedir que el usuario obtenga acceso a la cámara del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa592-212">Indicates whether or not to block the user from accessing the camera of the device.</span></span>|
|<span data-ttu-id="aa592-213">cellularBlockDataRoaming</span><span class="sxs-lookup"><span data-stu-id="aa592-213">cellularBlockDataRoaming</span></span>|<span data-ttu-id="aa592-214">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-214">Boolean</span></span>|<span data-ttu-id="aa592-215">Indica si se va a bloquear la itinerancia de datos.</span><span class="sxs-lookup"><span data-stu-id="aa592-215">Indicates whether or not to block data roaming.</span></span>|
|<span data-ttu-id="aa592-216">cellularBlockGlobalBackgroundFetchWhileRoaming</span><span class="sxs-lookup"><span data-stu-id="aa592-216">cellularBlockGlobalBackgroundFetchWhileRoaming</span></span>|<span data-ttu-id="aa592-217">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-217">Boolean</span></span>|<span data-ttu-id="aa592-218">Indica si se va a impedir la captura de fondo global mientras se está en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="aa592-218">Indicates whether or not to block global background fetch while roaming.</span></span>|
|<span data-ttu-id="aa592-219">cellularBlockPerAppDataModification</span><span class="sxs-lookup"><span data-stu-id="aa592-219">cellularBlockPerAppDataModification</span></span>|<span data-ttu-id="aa592-220">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-220">Boolean</span></span>|<span data-ttu-id="aa592-221">Indica si se van a permitir los cambios en la configuración de uso de datos de aplicaciones de telefonía móvil cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-221">Indicates whether or not to allow changes to cellular app data usage settings when the device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-222">cellularBlockPersonalHotspot</span><span class="sxs-lookup"><span data-stu-id="aa592-222">cellularBlockPersonalHotspot</span></span>|<span data-ttu-id="aa592-223">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-223">Boolean</span></span>|<span data-ttu-id="aa592-224">Indica si se va a bloquear el punto de acceso personal.</span><span class="sxs-lookup"><span data-stu-id="aa592-224">Indicates whether or not to block Personal Hotspot.</span></span>|
|<span data-ttu-id="aa592-225">cellularBlockVoiceRoaming</span><span class="sxs-lookup"><span data-stu-id="aa592-225">cellularBlockVoiceRoaming</span></span>|<span data-ttu-id="aa592-226">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-226">Boolean</span></span>|<span data-ttu-id="aa592-227">Indica si se va a bloquear la itinerancia de voz.</span><span class="sxs-lookup"><span data-stu-id="aa592-227">Indicates whether or not to block voice roaming.</span></span>|
|<span data-ttu-id="aa592-228">certificatesBlockUntrustedTlsCertificates</span><span class="sxs-lookup"><span data-stu-id="aa592-228">certificatesBlockUntrustedTlsCertificates</span></span>|<span data-ttu-id="aa592-229">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-229">Boolean</span></span>|<span data-ttu-id="aa592-230">Indica si se van a bloquear los certificados TLS que no son de confianza.</span><span class="sxs-lookup"><span data-stu-id="aa592-230">Indicates whether or not to block untrusted TLS certificates.</span></span>|
|<span data-ttu-id="aa592-231">classroomAppBlockRemoteScreenObservation</span><span class="sxs-lookup"><span data-stu-id="aa592-231">classroomAppBlockRemoteScreenObservation</span></span>|<span data-ttu-id="aa592-232">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-232">Boolean</span></span>|<span data-ttu-id="aa592-233">Indica si se va a permitir la observación de pantalla remota de la aplicación Classroom cuando el dispositivo está en modo supervisado (iOS 9.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-233">Indicates whether or not to allow remote screen observation by Classroom app when the device is in supervised mode (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="aa592-234">classroomAppForceUnpromptedScreenObservation</span><span class="sxs-lookup"><span data-stu-id="aa592-234">classroomAppForceUnpromptedScreenObservation</span></span>|<span data-ttu-id="aa592-235">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-235">Boolean</span></span>|<span data-ttu-id="aa592-236">Indica si se va a autorizar de forma automática al profesor de un curso administrado en la aplicación Classroom para que vea la pantalla de un alumno sin preguntarle cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-236">Indicates whether or not to automatically give permission to the teacher of a managed course on the Classroom app to view a student's screen without prompting when the device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-237">compliantAppsList</span><span class="sxs-lookup"><span data-stu-id="aa592-237">compliantAppsList</span></span>|<span data-ttu-id="aa592-238">Colección [appListItem](../resources/intune_deviceconfig_applistitem.md)</span><span class="sxs-lookup"><span data-stu-id="aa592-238">[appListItem](../resources/intune_deviceconfig_applistitem.md) collection</span></span>|<span data-ttu-id="aa592-239">Lista de aplicaciones en el cumplimiento (sea lista de permitidos o de bloqueados, controlado por CompliantAppListType).</span><span class="sxs-lookup"><span data-stu-id="aa592-239">List of apps in the compliance (either allow list or block list, controlled by CompliantAppListType).</span></span> <span data-ttu-id="aa592-240">Esta colección puede contener un máximo de 10 000 elementos.</span><span class="sxs-lookup"><span data-stu-id="aa592-240">This collection can contain a maximum of 10000 elements.</span></span>|
|<span data-ttu-id="aa592-241">compliantAppListType</span><span class="sxs-lookup"><span data-stu-id="aa592-241">compliantAppListType</span></span>|[<span data-ttu-id="aa592-242">appListType</span><span class="sxs-lookup"><span data-stu-id="aa592-242">appListType</span></span>](../resources/intune_deviceconfig_applisttype.md)|<span data-ttu-id="aa592-p113">Lista que se encuentra en la AppComplianceList. Los valores posibles son: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span><span class="sxs-lookup"><span data-stu-id="aa592-p113">List that is in the AppComplianceList. The possible values are: `none`, `appsInListCompliant`, `appsNotInListCompliant`.</span></span>|
|<span data-ttu-id="aa592-245">configurationProfileBlockChanges</span><span class="sxs-lookup"><span data-stu-id="aa592-245">configurationProfileBlockChanges</span></span>|<span data-ttu-id="aa592-246">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-246">Boolean</span></span>|<span data-ttu-id="aa592-247">Indica si se va a impedir que el usuario instale perfiles de configuración y certificados de forma interactiva cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-247">Indicates whether or not to block the user from installing configuration profiles and certificates interactively when the device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-248">definitionLookupBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-248">definitionLookupBlocked</span></span>|<span data-ttu-id="aa592-249">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-249">Boolean</span></span>|<span data-ttu-id="aa592-250">Indica si se va a bloquear la búsqueda de definiciones cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-250">Indicates whether or not to block definition lookup when the device is in supervised mode (iOS 8.1.3 and later ).</span></span>|
|<span data-ttu-id="aa592-251">deviceBlockEnableRestrictions</span><span class="sxs-lookup"><span data-stu-id="aa592-251">deviceBlockEnableRestrictions</span></span>|<span data-ttu-id="aa592-252">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-252">Boolean</span></span>|<span data-ttu-id="aa592-253">Indica si se va a permitir que el usuario active las restricciones en los ajustes del dispositivo cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-253">Indicates whether or not to allow the user to enables restrictions in the device settings when the device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-254">deviceBlockEraseContentAndSettings</span><span class="sxs-lookup"><span data-stu-id="aa592-254">deviceBlockEraseContentAndSettings</span></span>|<span data-ttu-id="aa592-255">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-255">Boolean</span></span>|<span data-ttu-id="aa592-256">Indica si se va a permitir el uso de la opción "Borrar todo el contenido y la configuración" en el dispositivo cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-256">Indicates whether or not to allow the use of the 'Erase all content and settings' option on the device when the device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-257">deviceBlockNameModification</span><span class="sxs-lookup"><span data-stu-id="aa592-257">deviceBlockNameModification</span></span>|<span data-ttu-id="aa592-258">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-258">Boolean</span></span>|<span data-ttu-id="aa592-259">Indica si se va a permitir modificar el nombre del dispositivo cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-259">Indicates whether or not to allow device name modification when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="aa592-260">diagnosticDataBlockSubmission</span><span class="sxs-lookup"><span data-stu-id="aa592-260">diagnosticDataBlockSubmission</span></span>|<span data-ttu-id="aa592-261">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-261">Boolean</span></span>|<span data-ttu-id="aa592-262">Indica si se va a bloquear el envío de datos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="aa592-262">Indicates whether or not to block diagnostic data submission.</span></span>|
|<span data-ttu-id="aa592-263">diagnosticDataBlockSubmissionModification</span><span class="sxs-lookup"><span data-stu-id="aa592-263">diagnosticDataBlockSubmissionModification</span></span>|<span data-ttu-id="aa592-264">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-264">Boolean</span></span>|<span data-ttu-id="aa592-265">Indica si se va a permitir modificar los ajustes del envío de diagnósticos cuando el dispositivo está en modo supervisado (iOS 9.3.2 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-265">Indicates whether or not to allow diagnostics submission settings modification when the device is in supervised mode (iOS 9.3.2 and later).</span></span>|
|<span data-ttu-id="aa592-266">documentsBlockManagedDocumentsInUnmanagedApps</span><span class="sxs-lookup"><span data-stu-id="aa592-266">documentsBlockManagedDocumentsInUnmanagedApps</span></span>|<span data-ttu-id="aa592-267">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-267">Boolean</span></span>|<span data-ttu-id="aa592-268">Indica si se va a impedir que el usuario visualice documentos administrados en las aplicaciones no administradas.</span><span class="sxs-lookup"><span data-stu-id="aa592-268">Indicates whether or not to block the user from viewing managed documents in unmanaged apps.</span></span>|
|<span data-ttu-id="aa592-269">documentsBlockUnmanagedDocumentsInManagedApps</span><span class="sxs-lookup"><span data-stu-id="aa592-269">documentsBlockUnmanagedDocumentsInManagedApps</span></span>|<span data-ttu-id="aa592-270">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-270">Boolean</span></span>|<span data-ttu-id="aa592-271">Indica si se va a impedir que el usuario visualice documentos no administrados en las aplicaciones administradas.</span><span class="sxs-lookup"><span data-stu-id="aa592-271">Indicates whether or not to block the user from viewing unmanaged documents in managed apps.</span></span>|
|<span data-ttu-id="aa592-272">emailInDomainSuffixes</span><span class="sxs-lookup"><span data-stu-id="aa592-272">emailInDomainSuffixes</span></span>|<span data-ttu-id="aa592-273">Colección String</span><span class="sxs-lookup"><span data-stu-id="aa592-273">String collection</span></span>|<span data-ttu-id="aa592-274">Una dirección de correo electrónico que carezca de un sufijo que coincida con cualquiera de estas cadenas se considerará fuera de dominio.</span><span class="sxs-lookup"><span data-stu-id="aa592-274">An email address lacking a suffix that matches any of these strings will be considered out-of-domain.</span></span>|
|<span data-ttu-id="aa592-275">enterpriseAppBlockTrust</span><span class="sxs-lookup"><span data-stu-id="aa592-275">enterpriseAppBlockTrust</span></span>|<span data-ttu-id="aa592-276">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-276">Boolean</span></span>|<span data-ttu-id="aa592-277">Indica si se va a impedir que el usuario confíe en una aplicación empresarial.</span><span class="sxs-lookup"><span data-stu-id="aa592-277">Indicates whether or not to block the user from trusting an enterprise app.</span></span>|
|<span data-ttu-id="aa592-278">enterpriseAppBlockTrustModification</span><span class="sxs-lookup"><span data-stu-id="aa592-278">enterpriseAppBlockTrustModification</span></span>|<span data-ttu-id="aa592-279">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-279">Boolean</span></span>|<span data-ttu-id="aa592-280">Indica si se va a impedir que el usuario modifique la configuración de confianza de una aplicación empresarial.</span><span class="sxs-lookup"><span data-stu-id="aa592-280">Indicates whether or not to block the user from modifying the enterprise app trust settings.</span></span>|
|<span data-ttu-id="aa592-281">faceTimeBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-281">faceTimeBlocked</span></span>|<span data-ttu-id="aa592-282">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-282">Boolean</span></span>|<span data-ttu-id="aa592-283">Indica si se va a impedir que el usuario use FaceTime.</span><span class="sxs-lookup"><span data-stu-id="aa592-283">Indicates whether or not to block the user from using FaceTime.</span></span>|
|<span data-ttu-id="aa592-284">findMyFriendsBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-284">findMyFriendsBlocked</span></span>|<span data-ttu-id="aa592-285">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-285">Boolean</span></span>|<span data-ttu-id="aa592-286">Indica si se va a bloquear Buscar a mis amigos cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-286">Indicates whether or not to block Find My Friends when the device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-287">gamingBlockGameCenterFriends</span><span class="sxs-lookup"><span data-stu-id="aa592-287">gamingBlockGameCenterFriends</span></span>|<span data-ttu-id="aa592-288">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-288">Boolean</span></span>|<span data-ttu-id="aa592-289">Indica si se va a impedir que el usuario tenga amigos en el Game Center.</span><span class="sxs-lookup"><span data-stu-id="aa592-289">Indicates whether or not to block the user from having friends in Game Center.</span></span>|
|<span data-ttu-id="aa592-290">gamingBlockMultiplayer</span><span class="sxs-lookup"><span data-stu-id="aa592-290">gamingBlockMultiplayer</span></span>|<span data-ttu-id="aa592-291">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-291">Boolean</span></span>|<span data-ttu-id="aa592-292">Indica si se va a impedir que el usuario use los juegos multijugador.</span><span class="sxs-lookup"><span data-stu-id="aa592-292">Indicates whether or not to block the user from using multiplayer gaming.</span></span>|
|<span data-ttu-id="aa592-293">gameCenterBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-293">gameCenterBlocked</span></span>|<span data-ttu-id="aa592-294">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-294">Boolean</span></span>|<span data-ttu-id="aa592-295">Indica si se va a impedir que el usuario use el Game Center cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-295">Indicates whether or not to block the user from using Game Center when the device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-296">hostPairingBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-296">hostPairingBlocked</span></span>|<span data-ttu-id="aa592-297">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-297">Boolean</span></span>|<span data-ttu-id="aa592-298">Indica si se va a permitir el emparejamiento de host para controlar los dispositivos con los que se puede emparejar un dispositivo iOS cuando el dispositivo iOS está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-298">indicates whether or not to allow host pairing to control the devices an iOS device can pair with when the iOS device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-299">iBooksStoreBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-299">iBooksStoreBlocked</span></span>|<span data-ttu-id="aa592-300">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-300">Boolean</span></span>|<span data-ttu-id="aa592-301">Indica si se va a impedir que el usuario use iBooks Store cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-301">Indicates whether or not to block the user from using the iBooks Store when the device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-302">iBooksStoreBlockErotica</span><span class="sxs-lookup"><span data-stu-id="aa592-302">iBooksStoreBlockErotica</span></span>|<span data-ttu-id="aa592-303">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-303">Boolean</span></span>|<span data-ttu-id="aa592-304">Indica si se va a impedir que el usuario descargue archivos multimedia desde el iBook Store que se han etiquetado como eróticos.</span><span class="sxs-lookup"><span data-stu-id="aa592-304">Indicates whether or not to block the user from downloading media from the iBookstore that has been tagged as erotica.</span></span>|
|<span data-ttu-id="aa592-305">iCloudBlockActivityContinuation</span><span class="sxs-lookup"><span data-stu-id="aa592-305">iCloudBlockActivityContinuation</span></span>|<span data-ttu-id="aa592-306">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-306">Boolean</span></span>|<span data-ttu-id="aa592-307">Indica si se va a impedir que el usuario continúe con el trabajo que empezó en el dispositivo iOS en otro dispositivo macOS o iOS.</span><span class="sxs-lookup"><span data-stu-id="aa592-307">Indicates whether or not to block  the the user from continuing work they started on iOS device to another iOS or macOS device.</span></span>|
|<span data-ttu-id="aa592-308">iCloudBlockBackup</span><span class="sxs-lookup"><span data-stu-id="aa592-308">iCloudBlockBackup</span></span>|<span data-ttu-id="aa592-309">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-309">Boolean</span></span>|<span data-ttu-id="aa592-310">Indica si se va a impedir la copia de seguridad de iCloud.</span><span class="sxs-lookup"><span data-stu-id="aa592-310">Indicates whether or not to block iCloud backup.</span></span>|
|<span data-ttu-id="aa592-311">iCloudBlockDocumentSync</span><span class="sxs-lookup"><span data-stu-id="aa592-311">iCloudBlockDocumentSync</span></span>|<span data-ttu-id="aa592-312">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-312">Boolean</span></span>|<span data-ttu-id="aa592-313">Indica si se va a impedir la sincronización de documentos de iCloud.</span><span class="sxs-lookup"><span data-stu-id="aa592-313">Indicates whether or not to block iCloud document sync.</span></span>|
|<span data-ttu-id="aa592-314">iCloudBlockManagedAppsSync</span><span class="sxs-lookup"><span data-stu-id="aa592-314">iCloudBlockManagedAppsSync</span></span>|<span data-ttu-id="aa592-315">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-315">Boolean</span></span>|<span data-ttu-id="aa592-316">Indica si se va a impedir la sincronización en la nube de aplicaciones administradas.</span><span class="sxs-lookup"><span data-stu-id="aa592-316">Indicates whether or not to block Managed Apps Cloud Sync.</span></span>|
|<span data-ttu-id="aa592-317">iCloudBlockPhotoLibrary</span><span class="sxs-lookup"><span data-stu-id="aa592-317">iCloudBlockPhotoLibrary</span></span>|<span data-ttu-id="aa592-318">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-318">Boolean</span></span>|<span data-ttu-id="aa592-319">Indica si se va a bloquear la Fototeca de iCloud.</span><span class="sxs-lookup"><span data-stu-id="aa592-319">Indicates whether or not to block iCloud Photo Library.</span></span>|
|<span data-ttu-id="aa592-320">iCloudBlockPhotoStreamSync</span><span class="sxs-lookup"><span data-stu-id="aa592-320">iCloudBlockPhotoStreamSync</span></span>|<span data-ttu-id="aa592-321">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-321">Boolean</span></span>|<span data-ttu-id="aa592-322">Indica si se va a bloquear la sincronización de fotos en streaming de iCloud.</span><span class="sxs-lookup"><span data-stu-id="aa592-322">Indicates whether or not to block iCloud Photo Stream Sync.</span></span>|
|<span data-ttu-id="aa592-323">iCloudBlockSharedPhotoStream</span><span class="sxs-lookup"><span data-stu-id="aa592-323">iCloudBlockSharedPhotoStream</span></span>|<span data-ttu-id="aa592-324">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-324">Boolean</span></span>|<span data-ttu-id="aa592-325">Indica si se va a bloquear la sincronización de fotos en streaming compartidas.</span><span class="sxs-lookup"><span data-stu-id="aa592-325">Indicates whether or not to block Shared Photo Stream.</span></span>|
|<span data-ttu-id="aa592-326">iCloudRequireEncryptedBackup</span><span class="sxs-lookup"><span data-stu-id="aa592-326">iCloudRequireEncryptedBackup</span></span>|<span data-ttu-id="aa592-327">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-327">Boolean</span></span>|<span data-ttu-id="aa592-328">Indica si se va a requerir que las copias de seguridad de iCloud estén cifradas.</span><span class="sxs-lookup"><span data-stu-id="aa592-328">Indicates whether or not to require backups to iCloud be encrypted.</span></span>|
|<span data-ttu-id="aa592-329">iTunesBlockExplicitContent</span><span class="sxs-lookup"><span data-stu-id="aa592-329">iTunesBlockExplicitContent</span></span>|<span data-ttu-id="aa592-330">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-330">Boolean</span></span>|<span data-ttu-id="aa592-331">Indica si se va a impedir que el usuario obtenga acceso a contenido explícito en iTunes y el App Store.</span><span class="sxs-lookup"><span data-stu-id="aa592-331">Indicates whether or not to block the user from accessing explicit content in iTunes and the App Store.</span></span>|
|<span data-ttu-id="aa592-332">iTunesBlockMusicService</span><span class="sxs-lookup"><span data-stu-id="aa592-332">iTunesBlockMusicService</span></span>|<span data-ttu-id="aa592-333">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-333">Boolean</span></span>|<span data-ttu-id="aa592-334">Indica si se va a bloquear el servicio Música y revertir la aplicación Música al modo clásico cuando el dispositivo está en modo supervisado (iOS 9.3 y versiones posteriores, y macOS 10.12 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="aa592-334">Indicates whether or not to block Music service and revert Music app to classic mode when the device is in supervised mode (iOS 9.3 and later and macOS 10.12 and later).</span></span>|
|<span data-ttu-id="aa592-335">iTunesBlockRadio</span><span class="sxs-lookup"><span data-stu-id="aa592-335">iTunesBlockRadio</span></span>|<span data-ttu-id="aa592-336">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-336">Boolean</span></span>|<span data-ttu-id="aa592-337">Indica si se va a impedir que el usuario use iTunes Radio cuando el dispositivo está en modo supervisado (iOS 9.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-337">Indicates whether or not to block the user from using iTunes Radio when the device is in supervised mode (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="aa592-338">keyboardBlockAutoCorrect</span><span class="sxs-lookup"><span data-stu-id="aa592-338">keyboardBlockAutoCorrect</span></span>|<span data-ttu-id="aa592-339">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-339">Boolean</span></span>|<span data-ttu-id="aa592-340">Indica si se va a bloquear el autocorrector cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-340">Indicates whether or not to block keyboard auto-correction when the device is in supervised mode (iOS 8.1.3 and later).</span></span>|
|<span data-ttu-id="aa592-341">keyboardBlockDictation</span><span class="sxs-lookup"><span data-stu-id="aa592-341">keyboardBlockDictation</span></span>|<span data-ttu-id="aa592-342">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-342">Boolean</span></span>|<span data-ttu-id="aa592-343">Indica si se va a impedir que el usuario use la entrada dictada cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-343">Indicates whether or not to block the user from using dictation input when the device is in supervised mode.</span></span>|
|<span data-ttu-id="aa592-344">keyboardBlockPredictive</span><span class="sxs-lookup"><span data-stu-id="aa592-344">keyboardBlockPredictive</span></span>|<span data-ttu-id="aa592-345">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-345">Boolean</span></span>|<span data-ttu-id="aa592-346">Indica si se van a bloquear los teclados predictivos cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-346">Indicates whether or not to block predictive keyboards when device is in supervised mode (iOS 8.1.3 and later).</span></span>|
|<span data-ttu-id="aa592-347">keyboardBlockShortcuts</span><span class="sxs-lookup"><span data-stu-id="aa592-347">keyboardBlockShortcuts</span></span>|<span data-ttu-id="aa592-348">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-348">Boolean</span></span>|<span data-ttu-id="aa592-349">Indica si se van a bloquear los atajos del teclado cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-349">Indicates whether or not to block keyboard shortcuts when the device is in supervised mode (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="aa592-350">keyboardBlockSpellCheck</span><span class="sxs-lookup"><span data-stu-id="aa592-350">keyboardBlockSpellCheck</span></span>|<span data-ttu-id="aa592-351">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-351">Boolean</span></span>|<span data-ttu-id="aa592-352">Indica si se va a bloquear la revisión ortográfica cuando el dispositivo está en modo supervisado (iOS 8.1.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-352">Indicates whether or not to block keyboard spell-checking when the device is in supervised mode (iOS 8.1.3 and later).</span></span>|
|<span data-ttu-id="aa592-353">kioskModeAllowAssistiveSpeak</span><span class="sxs-lookup"><span data-stu-id="aa592-353">kioskModeAllowAssistiveSpeak</span></span>|<span data-ttu-id="aa592-354">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-354">Boolean</span></span>|<span data-ttu-id="aa592-355">Indica si se va a permitir la lectura de asistencia en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-355">Indicates whether or not to allow assistive speak while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-356">kioskModeAllowAssistiveTouchSettings</span><span class="sxs-lookup"><span data-stu-id="aa592-356">kioskModeAllowAssistiveTouchSettings</span></span>|<span data-ttu-id="aa592-357">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-357">Boolean</span></span>|<span data-ttu-id="aa592-358">Indica si se va a permitir el acceso a la configuración de AssistiveTouch en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-358">Indicates whether or not to allow access to the Assistive Touch Settings while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-359">kioskModeAllowAutoLock</span><span class="sxs-lookup"><span data-stu-id="aa592-359">kioskModeAllowAutoLock</span></span>|<span data-ttu-id="aa592-360">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-360">Boolean</span></span>|<span data-ttu-id="aa592-361">Indica si se va a permitir el bloqueo automático del dispositivo en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-361">Indicates whether or not to allow device auto lock while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-362">kioskModeAllowColorInversionSettings</span><span class="sxs-lookup"><span data-stu-id="aa592-362">kioskModeAllowColorInversionSettings</span></span>|<span data-ttu-id="aa592-363">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-363">Boolean</span></span>|<span data-ttu-id="aa592-364">Indica si se va a permitir el acceso a la configuración de la inversión del color en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-364">Indicates whether or not to allow access to the Color Inversion Settings while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-365">kioskModeAllowRingerSwitch</span><span class="sxs-lookup"><span data-stu-id="aa592-365">kioskModeAllowRingerSwitch</span></span>|<span data-ttu-id="aa592-366">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-366">Boolean</span></span>|<span data-ttu-id="aa592-367">Indica si se va a permitir el uso del cambio de tono en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-367">Indicates whether or not to allow use of the ringer switch while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-368">kioskModeAllowScreenRotation</span><span class="sxs-lookup"><span data-stu-id="aa592-368">kioskModeAllowScreenRotation</span></span>|<span data-ttu-id="aa592-369">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-369">Boolean</span></span>|<span data-ttu-id="aa592-370">Indica si se va a permitir la rotación de pantalla en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-370">Indicates whether or not to allow screen rotation while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-371">kioskModeAllowSleepButton</span><span class="sxs-lookup"><span data-stu-id="aa592-371">kioskModeAllowSleepButton</span></span>|<span data-ttu-id="aa592-372">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-372">Boolean</span></span>|<span data-ttu-id="aa592-373">Indica si se va a permitir el uso del botón de suspensión en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-373">Indicates whether or not to allow use of the sleep button while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-374">kioskModeAllowTouchscreen</span><span class="sxs-lookup"><span data-stu-id="aa592-374">kioskModeAllowTouchscreen</span></span>|<span data-ttu-id="aa592-375">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-375">Boolean</span></span>|<span data-ttu-id="aa592-376">Indica si se va a permitir el uso de la pantalla táctil en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-376">Indicates whether or not to allow use of the touchscreen while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-377">kioskModeAllowVoiceOverSettings</span><span class="sxs-lookup"><span data-stu-id="aa592-377">kioskModeAllowVoiceOverSettings</span></span>|<span data-ttu-id="aa592-378">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-378">Boolean</span></span>|<span data-ttu-id="aa592-379">Indica si se va a permitir el acceso a la configuración de voz en off en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-379">Indicates whether or not to allow access to the voice over settings while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-380">kioskModeAllowVolumeButtons</span><span class="sxs-lookup"><span data-stu-id="aa592-380">kioskModeAllowVolumeButtons</span></span>|<span data-ttu-id="aa592-381">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-381">Boolean</span></span>|<span data-ttu-id="aa592-382">Indica si se va a permitir el uso de los botones de volumen en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-382">Indicates whether or not to allow use of the volume buttons while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-383">kioskModeAllowZoomSettings</span><span class="sxs-lookup"><span data-stu-id="aa592-383">kioskModeAllowZoomSettings</span></span>|<span data-ttu-id="aa592-384">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-384">Boolean</span></span>|<span data-ttu-id="aa592-385">Indica si se va a permitir el acceso a la configuración de zoom en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-385">Indicates whether or not to allow access to the zoom settings while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-386">kioskModeAppStoreUrl</span><span class="sxs-lookup"><span data-stu-id="aa592-386">kioskModeAppStoreUrl</span></span>|<span data-ttu-id="aa592-387">Cadena</span><span class="sxs-lookup"><span data-stu-id="aa592-387">String</span></span>|<span data-ttu-id="aa592-388">Dirección URL en la tienda de aplicaciones a la aplicación que se usará para el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-388">URL in the app store to the app to use for kiosk mode.</span></span> <span data-ttu-id="aa592-389">Úsela si KioskModeManagedAppId es desconocido.</span><span class="sxs-lookup"><span data-stu-id="aa592-389">Use if KioskModeManagedAppId is not known.</span></span>|
|<span data-ttu-id="aa592-390">kioskModeBuiltInAppId</span><span class="sxs-lookup"><span data-stu-id="aa592-390">kioskModeBuiltInAppId</span></span>|<span data-ttu-id="aa592-391">Cadena</span><span class="sxs-lookup"><span data-stu-id="aa592-391">String</span></span>|<span data-ttu-id="aa592-392">Identificador de aplicaciones integradas que se usará para el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-392">ID for built-in apps to use for kiosk mode.</span></span> <span data-ttu-id="aa592-393">Se usa cuando no se establecen KioskModeManagedAppId y KioskModeAppStoreUrl.</span><span class="sxs-lookup"><span data-stu-id="aa592-393">Used when KioskModeManagedAppId and KioskModeAppStoreUrl are not set.</span></span>|
|<span data-ttu-id="aa592-394">kioskModeRequireAssistiveTouch</span><span class="sxs-lookup"><span data-stu-id="aa592-394">kioskModeRequireAssistiveTouch</span></span>|<span data-ttu-id="aa592-395">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-395">Boolean</span></span>|<span data-ttu-id="aa592-396">Indica si se va a requerir la AssistiveTouch en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-396">Indicates whether or not to require assistive touch while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-397">kioskModeRequireColorInversion</span><span class="sxs-lookup"><span data-stu-id="aa592-397">kioskModeRequireColorInversion</span></span>|<span data-ttu-id="aa592-398">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-398">Boolean</span></span>|<span data-ttu-id="aa592-399">Indica si se va a requerir la inversión de color en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-399">Indicates whether or not to require color inversion while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-400">kioskModeRequireMonoAudio</span><span class="sxs-lookup"><span data-stu-id="aa592-400">kioskModeRequireMonoAudio</span></span>|<span data-ttu-id="aa592-401">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-401">Boolean</span></span>|<span data-ttu-id="aa592-402">Indica si se va a requerir el audio mono en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-402">Indicates whether or not to require mono audio while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-403">kioskModeRequireVoiceOver</span><span class="sxs-lookup"><span data-stu-id="aa592-403">kioskModeRequireVoiceOver</span></span>|<span data-ttu-id="aa592-404">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-404">Boolean</span></span>|<span data-ttu-id="aa592-405">Indica si se va a requerir la voz en off en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-405">Indicates whether or not to require voice over while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-406">kioskModeRequireZoom</span><span class="sxs-lookup"><span data-stu-id="aa592-406">kioskModeRequireZoom</span></span>|<span data-ttu-id="aa592-407">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-407">Boolean</span></span>|<span data-ttu-id="aa592-408">Indica si se va a requerir el zoom en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-408">Indicates whether or not to require zoom while in kiosk mode.</span></span>|
|<span data-ttu-id="aa592-409">kioskModeManagedAppId</span><span class="sxs-lookup"><span data-stu-id="aa592-409">kioskModeManagedAppId</span></span>|<span data-ttu-id="aa592-410">Cadena</span><span class="sxs-lookup"><span data-stu-id="aa592-410">String</span></span>|<span data-ttu-id="aa592-411">identificador de la aplicación administrada de la aplicación que se usará para el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="aa592-411">Managed app id of the app to use for kiosk mode.</span></span> <span data-ttu-id="aa592-412">Si se especifica KioskModeManagedAppId, entonces se omitirá KioskModeAppStoreUrl.</span><span class="sxs-lookup"><span data-stu-id="aa592-412">If KioskModeManagedAppId is specified then KioskModeAppStoreUrl will be ignored.</span></span>|
|<span data-ttu-id="aa592-413">lockScreenBlockControlCenter</span><span class="sxs-lookup"><span data-stu-id="aa592-413">lockScreenBlockControlCenter</span></span>|<span data-ttu-id="aa592-414">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-414">Boolean</span></span>|<span data-ttu-id="aa592-415">Indica si se va a impedir que el usuario use el centro de control en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="aa592-415">Indicates whether or not to block the user from using control center on the lock screen.</span></span>|
|<span data-ttu-id="aa592-416">lockScreenBlockNotificationView</span><span class="sxs-lookup"><span data-stu-id="aa592-416">lockScreenBlockNotificationView</span></span>|<span data-ttu-id="aa592-417">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-417">Boolean</span></span>|<span data-ttu-id="aa592-418">Indica si se va a impedir que el usuario use la visualización de notificaciones en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="aa592-418">Indicates whether or not to block the user from using the notification view on the lock screen.</span></span>|
|<span data-ttu-id="aa592-419">lockScreenBlockPassbook</span><span class="sxs-lookup"><span data-stu-id="aa592-419">lockScreenBlockPassbook</span></span>|<span data-ttu-id="aa592-420">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-420">Boolean</span></span>|<span data-ttu-id="aa592-421">Indica si se va a impedir que el usuario use Passbook cuando el dispositivo está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="aa592-421">Indicates whether or not to block the user from using passbook when the device is locked.</span></span>|
|<span data-ttu-id="aa592-422">lockScreenBlockTodayView</span><span class="sxs-lookup"><span data-stu-id="aa592-422">lockScreenBlockTodayView</span></span>|<span data-ttu-id="aa592-423">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-423">Boolean</span></span>|<span data-ttu-id="aa592-424">Indica si se va a impedir que el usuario use la vista Hoy en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="aa592-424">Indicates whether or not to block the user from using the Today View on the lock screen.</span></span>|
|<span data-ttu-id="aa592-425">mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="aa592-425">mediaContentRatingAustralia</span></span>|[<span data-ttu-id="aa592-426">mediaContentRatingAustralia</span><span class="sxs-lookup"><span data-stu-id="aa592-426">mediaContentRatingAustralia</span></span>](../resources/intune_deviceconfig_mediacontentratingaustralia.md)|<span data-ttu-id="aa592-427">Clasificación de contenido multimedia para Australia</span><span class="sxs-lookup"><span data-stu-id="aa592-427">Media content rating settings for Australia</span></span>|
|<span data-ttu-id="aa592-428">mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="aa592-428">mediaContentRatingCanada</span></span>|[<span data-ttu-id="aa592-429">mediaContentRatingCanada</span><span class="sxs-lookup"><span data-stu-id="aa592-429">mediaContentRatingCanada</span></span>](../resources/intune_deviceconfig_mediacontentratingcanada.md)|<span data-ttu-id="aa592-430">Clasificación de contenido multimedia para Canadá</span><span class="sxs-lookup"><span data-stu-id="aa592-430">Media content rating settings for Canada</span></span>|
|<span data-ttu-id="aa592-431">mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="aa592-431">mediaContentRatingFrance</span></span>|[<span data-ttu-id="aa592-432">mediaContentRatingFrance</span><span class="sxs-lookup"><span data-stu-id="aa592-432">mediaContentRatingFrance</span></span>](../resources/intune_deviceconfig_mediacontentratingfrance.md)|<span data-ttu-id="aa592-433">Clasificación de contenido multimedia para Francia</span><span class="sxs-lookup"><span data-stu-id="aa592-433">Media content rating settings for France</span></span>|
|<span data-ttu-id="aa592-434">mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="aa592-434">mediaContentRatingGermany</span></span>|[<span data-ttu-id="aa592-435">mediaContentRatingGermany</span><span class="sxs-lookup"><span data-stu-id="aa592-435">mediaContentRatingGermany</span></span>](../resources/intune_deviceconfig_mediacontentratinggermany.md)|<span data-ttu-id="aa592-436">Clasificación de contenido multimedia para Alemania</span><span class="sxs-lookup"><span data-stu-id="aa592-436">Media content rating settings for Germany</span></span>|
|<span data-ttu-id="aa592-437">mediaContentRatingIreland</span><span class="sxs-lookup"><span data-stu-id="aa592-437">mediaContentRatingIreland</span></span>|[<span data-ttu-id="aa592-438">mediaContentRatingIreland</span><span class="sxs-lookup"><span data-stu-id="aa592-438">mediaContentRatingIreland</span></span>](../resources/intune_deviceconfig_mediacontentratingireland.md)|<span data-ttu-id="aa592-439">Clasificación de contenido multimedia para Irlanda</span><span class="sxs-lookup"><span data-stu-id="aa592-439">Media content rating settings for Ireland</span></span>|
|<span data-ttu-id="aa592-440">mediaContentRatingJapan</span><span class="sxs-lookup"><span data-stu-id="aa592-440">mediaContentRatingJapan</span></span>|[<span data-ttu-id="aa592-441">mediaContentRatingJapan</span><span class="sxs-lookup"><span data-stu-id="aa592-441">mediaContentRatingJapan</span></span>](../resources/intune_deviceconfig_mediacontentratingjapan.md)|<span data-ttu-id="aa592-442">Clasificación de contenido multimedia para Japón</span><span class="sxs-lookup"><span data-stu-id="aa592-442">Media content rating settings for Japan</span></span>|
|<span data-ttu-id="aa592-443">mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="aa592-443">mediaContentRatingNewZealand</span></span>|[<span data-ttu-id="aa592-444">mediaContentRatingNewZealand</span><span class="sxs-lookup"><span data-stu-id="aa592-444">mediaContentRatingNewZealand</span></span>](../resources/intune_deviceconfig_mediacontentratingnewzealand.md)|<span data-ttu-id="aa592-445">Clasificación de contenido multimedia para Nueva Zelanda</span><span class="sxs-lookup"><span data-stu-id="aa592-445">Media content rating settings for New Zealand</span></span>|
|<span data-ttu-id="aa592-446">mediaContentRatingUnitedKingdom</span><span class="sxs-lookup"><span data-stu-id="aa592-446">mediaContentRatingUnitedKingdom</span></span>|[<span data-ttu-id="aa592-447">mediaContentRatingUnitedKingdom</span><span class="sxs-lookup"><span data-stu-id="aa592-447">mediaContentRatingUnitedKingdom</span></span>](../resources/intune_deviceconfig_mediacontentratingunitedkingdom.md)|<span data-ttu-id="aa592-448">Clasificación de contenido multimedia para el Reino Unido</span><span class="sxs-lookup"><span data-stu-id="aa592-448">Media content rating settings for United Kingdom</span></span>|
|<span data-ttu-id="aa592-449">mediaContentRatingUnitedStates</span><span class="sxs-lookup"><span data-stu-id="aa592-449">mediaContentRatingUnitedStates</span></span>|[<span data-ttu-id="aa592-450">mediaContentRatingUnitedStates</span><span class="sxs-lookup"><span data-stu-id="aa592-450">mediaContentRatingUnitedStates</span></span>](../resources/intune_deviceconfig_mediacontentratingunitedstates.md)|<span data-ttu-id="aa592-451">Clasificación de contenido multimedia para Estados Unidos</span><span class="sxs-lookup"><span data-stu-id="aa592-451">Media content rating settings for United States</span></span>|
|<span data-ttu-id="aa592-452">networkUsageRules</span><span class="sxs-lookup"><span data-stu-id="aa592-452">networkUsageRules</span></span>|<span data-ttu-id="aa592-453">Colección [iosNetworkUsageRule](../resources/intune_deviceconfig_iosnetworkusagerule.md)</span><span class="sxs-lookup"><span data-stu-id="aa592-453">[iosNetworkUsageRule](../resources/intune_deviceconfig_iosnetworkusagerule.md) collection</span></span>|<span data-ttu-id="aa592-454">Lista de aplicaciones administradas y las reglas de red que se les aplican.</span><span class="sxs-lookup"><span data-stu-id="aa592-454">List of managed apps and the network rules that applies to them.</span></span> <span data-ttu-id="aa592-455">Esta colección puede contener un máximo de 1000 elementos.</span><span class="sxs-lookup"><span data-stu-id="aa592-455">This collection can contain a maximum of 1000 elements.</span></span>|
|<span data-ttu-id="aa592-456">mediaContentRatingApps</span><span class="sxs-lookup"><span data-stu-id="aa592-456">mediaContentRatingApps</span></span>|[<span data-ttu-id="aa592-457">ratingAppsType</span><span class="sxs-lookup"><span data-stu-id="aa592-457">ratingAppsType</span></span>](../resources/intune_deviceconfig_ratingappstype.md)|<span data-ttu-id="aa592-458">Configuración de la calificación de los contenidos de elementos multimedia para aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="aa592-458">Media content rating settings for Canada</span></span> <span data-ttu-id="aa592-459">Los valores posibles son: `allAllowed`, `allBlocked`, `agesAbove4`, `agesAbove9`, `agesAbove12`, `agesAbove17`.</span><span class="sxs-lookup"><span data-stu-id="aa592-459">Possible values are: `allAllowed`, `allBlocked`, `agesAbove4`, `agesAbove9`, `agesAbove12`, `agesAbove17`.</span></span>|
|<span data-ttu-id="aa592-460">messagesBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-460">messagesBlocked</span></span>|<span data-ttu-id="aa592-461">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-461">Boolean</span></span>|<span data-ttu-id="aa592-462">Indica si se va a impedir que el usuario use la aplicación Mensajes en el dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-462">Indicates whether or not to block the user from using the Messages app on the supervised device.</span></span>|
|<span data-ttu-id="aa592-463">notificationsBlockSettingsModification</span><span class="sxs-lookup"><span data-stu-id="aa592-463">notificationsBlockSettingsModification</span></span>|<span data-ttu-id="aa592-464">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-464">Boolean</span></span>|<span data-ttu-id="aa592-465">Indica si se van a permitir modificar la configuración de las notificaciones (iOS 9,3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="aa592-465">Indicates whether or not to allow notifications settings modification (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="aa592-466">passcodeBlockFingerprintUnlock</span><span class="sxs-lookup"><span data-stu-id="aa592-466">passcodeBlockFingerprintUnlock</span></span>|<span data-ttu-id="aa592-467">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-467">Boolean</span></span>|<span data-ttu-id="aa592-468">Indica si se va a impedir el desbloqueo por huella dactilar.</span><span class="sxs-lookup"><span data-stu-id="aa592-468">Indicates whether or not to block fingerprint unlock.</span></span>|
|<span data-ttu-id="aa592-469">passcodeBlockFingerprintModification</span><span class="sxs-lookup"><span data-stu-id="aa592-469">passcodeBlockFingerprintModification</span></span>|<span data-ttu-id="aa592-470">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-470">Boolean</span></span>|<span data-ttu-id="aa592-471">Impide la modificación de huellas digitales registradas de Touch ID en el modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-471">Block modification of registered Touch ID fingerprints when in supervised mode.</span></span>|
|<span data-ttu-id="aa592-472">passcodeBlockModification</span><span class="sxs-lookup"><span data-stu-id="aa592-472">passcodeBlockModification</span></span>|<span data-ttu-id="aa592-473">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-473">Boolean</span></span>|<span data-ttu-id="aa592-474">Indica si se va a permitir modificar los códigos de acceso cuando el dispositivo está en modo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-474">Indicates whether or not to allow passcode modification on the supervised device (iOS 9.0 and later).</span></span>|
|<span data-ttu-id="aa592-475">passcodeBlockSimple</span><span class="sxs-lookup"><span data-stu-id="aa592-475">passcodeBlockSimple</span></span>|<span data-ttu-id="aa592-476">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-476">Boolean</span></span>|<span data-ttu-id="aa592-477">Indica si se van a bloquear los códigos de acceso simples.</span><span class="sxs-lookup"><span data-stu-id="aa592-477">Indicates whether or not to block simple passcodes.</span></span>|
|<span data-ttu-id="aa592-478">passcodeExpirationDays</span><span class="sxs-lookup"><span data-stu-id="aa592-478">passcodeExpirationDays</span></span>|<span data-ttu-id="aa592-479">Int32</span><span class="sxs-lookup"><span data-stu-id="aa592-479">Int32</span></span>|<span data-ttu-id="aa592-480">Número de días antes de que expire el código de acceso.</span><span class="sxs-lookup"><span data-stu-id="aa592-480">Number of days before the passcode expires.</span></span> <span data-ttu-id="aa592-481">Valores válidos de 1 a 65535</span><span class="sxs-lookup"><span data-stu-id="aa592-481">Valid values 1 to 65535</span></span>|
|<span data-ttu-id="aa592-482">passcodeMinimumLength</span><span class="sxs-lookup"><span data-stu-id="aa592-482">passcodeMinimumLength</span></span>|<span data-ttu-id="aa592-483">Int32</span><span class="sxs-lookup"><span data-stu-id="aa592-483">Int32</span></span>|<span data-ttu-id="aa592-484">Longitud mínima de los códigos de acceso.</span><span class="sxs-lookup"><span data-stu-id="aa592-484">Minimum length of passcode.</span></span> <span data-ttu-id="aa592-485">Valores válidos de 4 a 14</span><span class="sxs-lookup"><span data-stu-id="aa592-485">Valid values 4 to 14</span></span>|
|<span data-ttu-id="aa592-486">passcodeMinutesOfInactivityBeforeLock</span><span class="sxs-lookup"><span data-stu-id="aa592-486">passcodeMinutesOfInactivityBeforeLock</span></span>|<span data-ttu-id="aa592-487">Int32</span><span class="sxs-lookup"><span data-stu-id="aa592-487">Int32</span></span>|<span data-ttu-id="aa592-488">Minutos de inactividad antes de que sea necesario un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="aa592-488">Minutes of inactivity before a passcode is required.</span></span>|
|<span data-ttu-id="aa592-489">passcodeMinutesOfInactivityBeforeScreenTimeout</span><span class="sxs-lookup"><span data-stu-id="aa592-489">passcodeMinutesOfInactivityBeforeScreenTimeout</span></span>|<span data-ttu-id="aa592-490">Int32</span><span class="sxs-lookup"><span data-stu-id="aa592-490">Int32</span></span>|<span data-ttu-id="aa592-491">Minutos de inactividad antes de que se agote el tiempo de espera de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="aa592-491">Minutes of inactivity before the screen times out.</span></span>|
|<span data-ttu-id="aa592-492">passcodeMinimumCharacterSetCount</span><span class="sxs-lookup"><span data-stu-id="aa592-492">passcodeMinimumCharacterSetCount</span></span>|<span data-ttu-id="aa592-493">Int32</span><span class="sxs-lookup"><span data-stu-id="aa592-493">Int32</span></span>|<span data-ttu-id="aa592-494">Número de juegos de caracteres que debe contener un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="aa592-494">Number of character sets a passcode must contain.</span></span> <span data-ttu-id="aa592-495">Valores válidos de 0 a 4.</span><span class="sxs-lookup"><span data-stu-id="aa592-495">Valid values 0 to 4</span></span>|
|<span data-ttu-id="aa592-496">passcodePreviousPasscodeBlockCount</span><span class="sxs-lookup"><span data-stu-id="aa592-496">passcodePreviousPasscodeBlockCount</span></span>|<span data-ttu-id="aa592-497">Int32</span><span class="sxs-lookup"><span data-stu-id="aa592-497">Int32</span></span>|<span data-ttu-id="aa592-498">Número de códigos de acceso anteriores que bloquear.</span><span class="sxs-lookup"><span data-stu-id="aa592-498">Number of previous passcodes to block.</span></span> <span data-ttu-id="aa592-499">Valores válidos de 1 a 24.</span><span class="sxs-lookup"><span data-stu-id="aa592-499">Valid values 1 to 24</span></span>|
|<span data-ttu-id="aa592-500">passcodeSignInFailureCountBeforeWipe</span><span class="sxs-lookup"><span data-stu-id="aa592-500">passcodeSignInFailureCountBeforeWipe</span></span>|<span data-ttu-id="aa592-501">Int32</span><span class="sxs-lookup"><span data-stu-id="aa592-501">Int32</span></span>|<span data-ttu-id="aa592-502">Número de errores de inicio de sesión permitidos antes de borrar los datos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa592-502">Number of sign in failures allowed before wiping the device.</span></span> <span data-ttu-id="aa592-503">Valores válidos de 4 a 11</span><span class="sxs-lookup"><span data-stu-id="aa592-503">Valid values 4 to 11</span></span>|
|<span data-ttu-id="aa592-504">passcodeRequiredType</span><span class="sxs-lookup"><span data-stu-id="aa592-504">passcodeRequiredType</span></span>|[<span data-ttu-id="aa592-505">requiredPasswordType</span><span class="sxs-lookup"><span data-stu-id="aa592-505">requiredPasswordType</span></span>](../resources/intune_deviceconfig_requiredpasswordtype.md)|<span data-ttu-id="aa592-506">Tipo de código de acceso necesario.</span><span class="sxs-lookup"><span data-stu-id="aa592-506">Type of passcode that is required.</span></span> <span data-ttu-id="aa592-507">Los valores posibles son: `deviceDefault`, `alphanumeric` y `numeric`.</span><span class="sxs-lookup"><span data-stu-id="aa592-507">Possible values are: `deviceDefault`, `alphanumeric`, `numeric`.</span></span>|
|<span data-ttu-id="aa592-508">passcodeRequired</span><span class="sxs-lookup"><span data-stu-id="aa592-508">passcodeRequired</span></span>|<span data-ttu-id="aa592-509">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-509">Boolean</span></span>|<span data-ttu-id="aa592-510">Indica si se va a requerir un código de acceso.</span><span class="sxs-lookup"><span data-stu-id="aa592-510">Indicates whether or not to require a passcode.</span></span>|
|<span data-ttu-id="aa592-511">podcastsBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-511">podcastsBlocked</span></span>|<span data-ttu-id="aa592-512">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-512">Boolean</span></span>|<span data-ttu-id="aa592-513">Indica si se va a impedir que el usuario use Podcasts cuando el dispositivo está en modo supervisado (iOS 8.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-513">Indicates whether or not to block the user from using podcasts on the supervised device (iOS 8.0 and later).</span></span>|
|<span data-ttu-id="aa592-514">safariBlockAutofill</span><span class="sxs-lookup"><span data-stu-id="aa592-514">safariBlockAutofill</span></span>|<span data-ttu-id="aa592-515">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-515">Boolean</span></span>|<span data-ttu-id="aa592-516">Indica si se va a impedir que el usuario use la opción de autorrellenado en Safari.</span><span class="sxs-lookup"><span data-stu-id="aa592-516">Indicates whether or not to block the user from using Auto fill in Safari.</span></span>|
|<span data-ttu-id="aa592-517">safariBlockJavaScript</span><span class="sxs-lookup"><span data-stu-id="aa592-517">safariBlockJavaScript</span></span>|<span data-ttu-id="aa592-518">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-518">Boolean</span></span>|<span data-ttu-id="aa592-519">Indica si se va a bloquear JavaScript en Safari.</span><span class="sxs-lookup"><span data-stu-id="aa592-519">Indicates whether or not to block JavaScript in Safari.</span></span>|
|<span data-ttu-id="aa592-520">safariBlockPopups</span><span class="sxs-lookup"><span data-stu-id="aa592-520">safariBlockPopups</span></span>|<span data-ttu-id="aa592-521">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-521">Boolean</span></span>|<span data-ttu-id="aa592-522">Indica si se van a bloquear los elementos emergentes en Safari.</span><span class="sxs-lookup"><span data-stu-id="aa592-522">Indicates whether or not to block popups in Safari.</span></span>|
|<span data-ttu-id="aa592-523">safariBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-523">safariBlocked</span></span>|<span data-ttu-id="aa592-524">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-524">Boolean</span></span>|<span data-ttu-id="aa592-525">Indica si se va a impedir que el usuario use Safari.</span><span class="sxs-lookup"><span data-stu-id="aa592-525">Indicates whether or not to block the user from using Safari.</span></span>|
|<span data-ttu-id="aa592-526">safariCookieSettings</span><span class="sxs-lookup"><span data-stu-id="aa592-526">safariCookieSettings</span></span>|[<span data-ttu-id="aa592-527">webBrowserCookieSettings</span><span class="sxs-lookup"><span data-stu-id="aa592-527">webBrowserCookieSettings</span></span>](../resources/intune_deviceconfig_webbrowsercookiesettings.md)|<span data-ttu-id="aa592-528">Configuración de cookies para Safari.</span><span class="sxs-lookup"><span data-stu-id="aa592-528">Cookie settings for Safari.</span></span> <span data-ttu-id="aa592-529">Los valores posibles son: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited` y `allowAlways`.</span><span class="sxs-lookup"><span data-stu-id="aa592-529">Possible values are: `browserDefault`, `blockAlways`, `allowCurrentWebSite`, `allowFromWebsitesVisited`, `allowAlways`.</span></span>|
|<span data-ttu-id="aa592-530">safariManagedDomains</span><span class="sxs-lookup"><span data-stu-id="aa592-530">safariManagedDomains</span></span>|<span data-ttu-id="aa592-531">Colección String</span><span class="sxs-lookup"><span data-stu-id="aa592-531">String collection</span></span>|<span data-ttu-id="aa592-532">Las direcciones URL que coinciden con los patrones que se enumeran aquí se considerarán administradas.</span><span class="sxs-lookup"><span data-stu-id="aa592-532">URLs matching the patterns listed here will be considered managed.</span></span>|
|<span data-ttu-id="aa592-533">safariPasswordAutoFillDomains</span><span class="sxs-lookup"><span data-stu-id="aa592-533">safariPasswordAutoFillDomains</span></span>|<span data-ttu-id="aa592-534">Colección String</span><span class="sxs-lookup"><span data-stu-id="aa592-534">String collection</span></span>|<span data-ttu-id="aa592-535">Los usuarios pueden guardar las contraseñas en Safari únicamente de las direcciones URL que coinciden con los patrones que se enumeran aquí.</span><span class="sxs-lookup"><span data-stu-id="aa592-535">Users can save passwords in Safari only from URLs matching the patterns listed here.</span></span> <span data-ttu-id="aa592-536">Se aplica solo a dispositivos en modo supervisado (iOS 9.3 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-536">Applies to devices in supervised mode (iOS 9.3 and later).</span></span>|
|<span data-ttu-id="aa592-537">safariRequireFraudWarning</span><span class="sxs-lookup"><span data-stu-id="aa592-537">safariRequireFraudWarning</span></span>|<span data-ttu-id="aa592-538">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-538">Boolean</span></span>|<span data-ttu-id="aa592-539">Indica si se va a requerir una advertencia de fraude en Safari.</span><span class="sxs-lookup"><span data-stu-id="aa592-539">Indicates whether or not to require fraud warning in Safari.</span></span>|
|<span data-ttu-id="aa592-540">screenCaptureBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-540">screenCaptureBlocked</span></span>|<span data-ttu-id="aa592-541">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-541">Boolean</span></span>|<span data-ttu-id="aa592-542">Indica si se impide o no que el usuario tome capturas de pantalla.</span><span class="sxs-lookup"><span data-stu-id="aa592-542">Indicates whether or not to block the user from taking Screenshots.</span></span>|
|<span data-ttu-id="aa592-543">siriBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-543">siriBlocked</span></span>|<span data-ttu-id="aa592-544">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-544">Boolean</span></span>|<span data-ttu-id="aa592-545">Indica si se va a impedir que el usuario use Siri.</span><span class="sxs-lookup"><span data-stu-id="aa592-545">Indicates whether or not to block the user from using Siri.</span></span>|
|<span data-ttu-id="aa592-546">siriBlockedWhenLocked</span><span class="sxs-lookup"><span data-stu-id="aa592-546">siriBlockedWhenLocked</span></span>|<span data-ttu-id="aa592-547">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-547">Boolean</span></span>|<span data-ttu-id="aa592-548">Indica si se va a impedir que el usuario use Siri cuando está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="aa592-548">Indicates whether or not to block the user from using Siri when locked.</span></span>|
|<span data-ttu-id="aa592-549">siriBlockUserGeneratedContent</span><span class="sxs-lookup"><span data-stu-id="aa592-549">siriBlockUserGeneratedContent</span></span>|<span data-ttu-id="aa592-550">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-550">Boolean</span></span>|<span data-ttu-id="aa592-551">Indica si se va a impedir que Siri haga consultas de contenido generado por el usuario cuando se usa en un dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-551">Indicates whether or not to block Siri from querying user-generated content when used on a supervised device.</span></span>|
|<span data-ttu-id="aa592-552">siriRequireProfanityFilter</span><span class="sxs-lookup"><span data-stu-id="aa592-552">siriRequireProfanityFilter</span></span>|<span data-ttu-id="aa592-553">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-553">Boolean</span></span>|<span data-ttu-id="aa592-554">Indica si se va a evitar que Siri dicte o hable con lenguaje irreverente en un dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-554">Indicates whether or not to prevent Siri from dictating, or speaking profane language on supervised device.</span></span>|
|<span data-ttu-id="aa592-555">spotlightBlockInternetResults</span><span class="sxs-lookup"><span data-stu-id="aa592-555">spotlightBlockInternetResults</span></span>|<span data-ttu-id="aa592-556">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-556">Boolean</span></span>|<span data-ttu-id="aa592-557">Indica si se va a impedir que la búsqueda Spotlight devuelva resultados de Internet en un dispositivo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-557">Indicates whether or not to block Spotlight search from returning internet results on supervised device.</span></span>|
|<span data-ttu-id="aa592-558">voiceDialingBlocked</span><span class="sxs-lookup"><span data-stu-id="aa592-558">voiceDialingBlocked</span></span>|<span data-ttu-id="aa592-559">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-559">Boolean</span></span>|<span data-ttu-id="aa592-560">Indica si se va a bloquear la marcación por voz.</span><span class="sxs-lookup"><span data-stu-id="aa592-560">Indicates whether or not to block voice dialing.</span></span>|
|<span data-ttu-id="aa592-561">wallpaperBlockModification</span><span class="sxs-lookup"><span data-stu-id="aa592-561">wallpaperBlockModification</span></span>|<span data-ttu-id="aa592-562">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-562">Boolean</span></span>|<span data-ttu-id="aa592-563">Indica si se va permitir modificar el fondo de pantalla en un dispositivo supervisado (iOS 9.0 o posterior).</span><span class="sxs-lookup"><span data-stu-id="aa592-563">Indicates whether or not to allow wallpaper modification on supervised device (iOS 9.0 and later) .</span></span>|
|<span data-ttu-id="aa592-564">wiFiConnectOnlyToConfiguredNetworks</span><span class="sxs-lookup"><span data-stu-id="aa592-564">wiFiConnectOnlyToConfiguredNetworks</span></span>|<span data-ttu-id="aa592-565">Booleano</span><span class="sxs-lookup"><span data-stu-id="aa592-565">Boolean</span></span>|<span data-ttu-id="aa592-566">Indica si se va a forzar al dispositivo para que use solo redes Wi-Fi de perfiles de configuración cuando el dispositivo está en modo supervisado.</span><span class="sxs-lookup"><span data-stu-id="aa592-566">Indicates whether or not to force the device to use only Wi-Fi networks from configuration profiles when the device is in supervised mode.</span></span>|



## <a name="response"></a><span data-ttu-id="aa592-567">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa592-567">Response</span></span>
<span data-ttu-id="aa592-568">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosGeneralDeviceConfiguration](../resources/intune_deviceconfig_iosgeneraldeviceconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="aa592-568">If successful, this method returns a `201 Created` response code and a [iosGeneralDeviceConfiguration](../resources/intune_deviceconfig_iosgeneraldeviceconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="aa592-569">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="aa592-569">Example</span></span>
### <a name="request"></a><span data-ttu-id="aa592-570">Solicitud</span><span class="sxs-lookup"><span data-stu-id="aa592-570">Request</span></span>
<span data-ttu-id="aa592-571">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="aa592-571">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 7905

{
  "@odata.type": "#microsoft.graph.iosGeneralDeviceConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
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

### <a name="response"></a><span data-ttu-id="aa592-572">Respuesta</span><span class="sxs-lookup"><span data-stu-id="aa592-572">Response</span></span>
<span data-ttu-id="aa592-p127">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="aa592-p127">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








