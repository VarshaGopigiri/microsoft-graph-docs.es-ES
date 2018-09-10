# <a name="update-iosdevicefeaturesconfiguration"></a><span data-ttu-id="ea84f-101">Actualizar iosDeviceFeaturesConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea84f-101">Update iosDeviceFeaturesConfiguration</span></span>

> <span data-ttu-id="ea84f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ea84f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ea84f-103">Actualice las propiedades de un objeto [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ea84f-103">Update the properties of a [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ea84f-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea84f-104">Prerequisites</span></span>
<span data-ttu-id="ea84f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ea84f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ea84f-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea84f-107">Permission type</span></span>|<span data-ttu-id="ea84f-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea84f-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ea84f-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea84f-109">Delegated (work or school account)</span></span>|<span data-ttu-id="ea84f-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea84f-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ea84f-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea84f-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ea84f-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea84f-112">Not supported.</span></span>|
|<span data-ttu-id="ea84f-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea84f-113">Application</span></span>|<span data-ttu-id="ea84f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea84f-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ea84f-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea84f-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="ea84f-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea84f-116">Request headers</span></span>
|<span data-ttu-id="ea84f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea84f-117">Header</span></span>|<span data-ttu-id="ea84f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ea84f-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ea84f-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea84f-119">Authorization</span></span>|<span data-ttu-id="ea84f-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ea84f-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ea84f-121">Accept</span><span class="sxs-lookup"><span data-stu-id="ea84f-121">Accept</span></span>|<span data-ttu-id="ea84f-122">application/json</span><span class="sxs-lookup"><span data-stu-id="ea84f-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ea84f-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea84f-123">Request body</span></span>
<span data-ttu-id="ea84f-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ea84f-124">In the request body, supply a JSON representation for the [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) object.</span></span>

<span data-ttu-id="ea84f-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="ea84f-125">The following table shows the properties that are required when you create the [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md).</span></span>

|<span data-ttu-id="ea84f-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea84f-126">Property</span></span>|<span data-ttu-id="ea84f-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea84f-127">Type</span></span>|<span data-ttu-id="ea84f-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea84f-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ea84f-129">id</span><span class="sxs-lookup"><span data-stu-id="ea84f-129">id</span></span>|<span data-ttu-id="ea84f-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea84f-130">String</span></span>|<span data-ttu-id="ea84f-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ea84f-131">Key of the entity.</span></span> <span data-ttu-id="ea84f-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea84f-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea84f-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ea84f-133">lastModifiedDateTime</span></span>|<span data-ttu-id="ea84f-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea84f-134">DateTimeOffset</span></span>|<span data-ttu-id="ea84f-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="ea84f-135">DateTime the object was last modified.</span></span> <span data-ttu-id="ea84f-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea84f-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea84f-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ea84f-137">createdDateTime</span></span>|<span data-ttu-id="ea84f-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea84f-138">DateTimeOffset</span></span>|<span data-ttu-id="ea84f-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="ea84f-139">DateTime the object was created.</span></span> <span data-ttu-id="ea84f-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea84f-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea84f-141">description</span><span class="sxs-lookup"><span data-stu-id="ea84f-141">description</span></span>|<span data-ttu-id="ea84f-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea84f-142">String</span></span>|<span data-ttu-id="ea84f-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea84f-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="ea84f-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea84f-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea84f-145">displayName</span><span class="sxs-lookup"><span data-stu-id="ea84f-145">displayName</span></span>|<span data-ttu-id="ea84f-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="ea84f-146">String</span></span>|<span data-ttu-id="ea84f-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea84f-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="ea84f-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea84f-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea84f-149">version</span><span class="sxs-lookup"><span data-stu-id="ea84f-149">version</span></span>|<span data-ttu-id="ea84f-150">Int32</span><span class="sxs-lookup"><span data-stu-id="ea84f-150">Int32</span></span>|<span data-ttu-id="ea84f-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ea84f-151">Version of the device configuration.</span></span> <span data-ttu-id="ea84f-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="ea84f-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="ea84f-153">assetTagTemplate</span><span class="sxs-lookup"><span data-stu-id="ea84f-153">assetTagTemplate</span></span>|<span data-ttu-id="ea84f-154">String</span><span class="sxs-lookup"><span data-stu-id="ea84f-154">String</span></span>|<span data-ttu-id="ea84f-155">Información de la etiqueta de activo del dispositivo, se muestra en la ventana de inicio de sesión y en la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="ea84f-155">Asset tag information for the device, displayed on the login window and lock screen.</span></span>|
|<span data-ttu-id="ea84f-156">lockScreenFootnote</span><span class="sxs-lookup"><span data-stu-id="ea84f-156">lockScreenFootnote</span></span>|<span data-ttu-id="ea84f-157">String</span><span class="sxs-lookup"><span data-stu-id="ea84f-157">String</span></span>|<span data-ttu-id="ea84f-158">Nota al pie que se muestra en la ventana de inicio de sesión y la pantalla de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="ea84f-158">A footnote displayed on the login window and lock screen.</span></span> <span data-ttu-id="ea84f-159">Disponible en iOS 9.3.1 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="ea84f-159">Available in iOS 9.3.1 and later.</span></span>|
|<span data-ttu-id="ea84f-160">homeScreenDockIcons</span><span class="sxs-lookup"><span data-stu-id="ea84f-160">homeScreenDockIcons</span></span>|<span data-ttu-id="ea84f-161">Colección [iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md)</span><span class="sxs-lookup"><span data-stu-id="ea84f-161">[iosHomeScreenItem](../resources/intune_deviceconfig_ioshomescreenitem.md) collection</span></span>|<span data-ttu-id="ea84f-162">Lista de las aplicaciones y carpetas que aparecen en el Dock de la pantalla de inicio.</span><span class="sxs-lookup"><span data-stu-id="ea84f-162">A list of app and folders to appear on the Home Screen Dock.</span></span> <span data-ttu-id="ea84f-163">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="ea84f-163">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="ea84f-164">homeScreenPages</span><span class="sxs-lookup"><span data-stu-id="ea84f-164">homeScreenPages</span></span>|<span data-ttu-id="ea84f-165">Colección [iosHomeScreenPage](../resources/intune_deviceconfig_ioshomescreenpage.md)</span><span class="sxs-lookup"><span data-stu-id="ea84f-165">[iosHomeScreenPage](../resources/intune_deviceconfig_ioshomescreenpage.md) collection</span></span>|<span data-ttu-id="ea84f-166">Lista de páginas en la pantalla de inicio.</span><span class="sxs-lookup"><span data-stu-id="ea84f-166">A list of pages on the Home Screen.</span></span> <span data-ttu-id="ea84f-167">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="ea84f-167">This collection can contain a maximum of 500 elements.</span></span>|
|<span data-ttu-id="ea84f-168">notificationSettings</span><span class="sxs-lookup"><span data-stu-id="ea84f-168">notificationSettings</span></span>|<span data-ttu-id="ea84f-169">Colección [iosNotificationSettings](../resources/intune_deviceconfig_iosnotificationsettings.md)</span><span class="sxs-lookup"><span data-stu-id="ea84f-169">[iosNotificationSettings](../resources/intune_deviceconfig_iosnotificationsettings.md) collection</span></span>|<span data-ttu-id="ea84f-170">Configuración de notificaciones de cada identificador de agrupación. Solo se aplica a los dispositivos en modo supervisado (iOS 9.3 y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="ea84f-170">Notification settings for each bundle id. Applicable to devices in supervised mode only (iOS 9.3 and later).</span></span> <span data-ttu-id="ea84f-171">Esta colección puede contener un máximo de 500 elementos.</span><span class="sxs-lookup"><span data-stu-id="ea84f-171">This collection can contain a maximum of 500 elements.</span></span>|



## <a name="response"></a><span data-ttu-id="ea84f-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea84f-172">Response</span></span>
<span data-ttu-id="ea84f-173">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea84f-173">If successful, this method returns a `200 OK` response code and an updated [iosDeviceFeaturesConfiguration](../resources/intune_deviceconfig_iosdevicefeaturesconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea84f-174">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea84f-174">Example</span></span>
### <a name="request"></a><span data-ttu-id="ea84f-175">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea84f-175">Request</span></span>
<span data-ttu-id="ea84f-176">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea84f-176">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 1983

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "assetTagTemplate": "Asset Tag Template value",
  "lockScreenFootnote": "Lock Screen Footnote value",
  "homeScreenDockIcons": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenFolder",
      "displayName": "Display Name value",
      "pages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
          "displayName": "Display Name value",
          "apps": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenApp",
              "displayName": "Display Name value",
              "bundleID": "Bundle ID value"
            }
          ]
        }
      ]
    }
  ],
  "homeScreenPages": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenPage",
      "displayName": "Display Name value",
      "icons": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolder",
          "displayName": "Display Name value",
          "pages": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
              "displayName": "Display Name value",
              "apps": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenApp",
                  "displayName": "Display Name value",
                  "bundleID": "Bundle ID value"
                }
              ]
            }
          ]
        }
      ]
    }
  ],
  "notificationSettings": [
    {
      "@odata.type": "microsoft.graph.iosNotificationSettings",
      "bundleID": "Bundle ID value",
      "appName": "App Name value",
      "publisher": "Publisher value",
      "enabled": true,
      "showInNotificationCenter": true,
      "showOnLockScreen": true,
      "alertType": "banner",
      "badgesEnabled": true,
      "soundsEnabled": true
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="ea84f-177">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea84f-177">Response</span></span>
<span data-ttu-id="ea84f-p112">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea84f-p112">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2160

{
  "@odata.type": "#microsoft.graph.iosDeviceFeaturesConfiguration",
  "id": "651e0ab3-0ab3-651e-b30a-1e65b30a1e65",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "assetTagTemplate": "Asset Tag Template value",
  "lockScreenFootnote": "Lock Screen Footnote value",
  "homeScreenDockIcons": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenFolder",
      "displayName": "Display Name value",
      "pages": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
          "displayName": "Display Name value",
          "apps": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenApp",
              "displayName": "Display Name value",
              "bundleID": "Bundle ID value"
            }
          ]
        }
      ]
    }
  ],
  "homeScreenPages": [
    {
      "@odata.type": "microsoft.graph.iosHomeScreenPage",
      "displayName": "Display Name value",
      "icons": [
        {
          "@odata.type": "microsoft.graph.iosHomeScreenFolder",
          "displayName": "Display Name value",
          "pages": [
            {
              "@odata.type": "microsoft.graph.iosHomeScreenFolderPage",
              "displayName": "Display Name value",
              "apps": [
                {
                  "@odata.type": "microsoft.graph.iosHomeScreenApp",
                  "displayName": "Display Name value",
                  "bundleID": "Bundle ID value"
                }
              ]
            }
          ]
        }
      ]
    }
  ],
  "notificationSettings": [
    {
      "@odata.type": "microsoft.graph.iosNotificationSettings",
      "bundleID": "Bundle ID value",
      "appName": "App Name value",
      "publisher": "Publisher value",
      "enabled": true,
      "showInNotificationCenter": true,
      "showOnLockScreen": true,
      "alertType": "banner",
      "badgesEnabled": true,
      "soundsEnabled": true
    }
  ]
}
```








