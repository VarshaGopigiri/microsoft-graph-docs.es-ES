# <a name="update-iosmobileappconfiguration"></a><span data-ttu-id="0f7f1-101">Actualizar iosMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f7f1-101">Update iosMobileAppConfiguration</span></span>

> <span data-ttu-id="0f7f1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0f7f1-103">Actualiza las propiedades de un objeto [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f1-103">Update the properties of a [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0f7f1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0f7f1-104">Prerequisites</span></span>
<span data-ttu-id="0f7f1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0f7f1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0f7f1-107">Permission type</span></span>|<span data-ttu-id="0f7f1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0f7f1-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0f7f1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0f7f1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="0f7f1-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0f7f1-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="0f7f1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0f7f1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0f7f1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-112">Not supported.</span></span>|
|<span data-ttu-id="0f7f1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0f7f1-113">Application</span></span>|<span data-ttu-id="0f7f1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0f7f1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0f7f1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="0f7f1-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0f7f1-116">Request headers</span></span>
|<span data-ttu-id="0f7f1-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f7f1-117">Header</span></span>|<span data-ttu-id="0f7f1-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0f7f1-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0f7f1-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="0f7f1-119">Authorization</span></span>|<span data-ttu-id="0f7f1-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0f7f1-121">Accept</span><span class="sxs-lookup"><span data-stu-id="0f7f1-121">Accept</span></span>|<span data-ttu-id="0f7f1-122">application/json</span><span class="sxs-lookup"><span data-stu-id="0f7f1-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0f7f1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0f7f1-123">Request body</span></span>
<span data-ttu-id="0f7f1-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f1-124">In the request body, supply a JSON representation for the [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md) object.</span></span>

<span data-ttu-id="0f7f1-125">En la tabla siguiente se muestran las propiedades necesarias para crear [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="0f7f1-125">The following table shows the properties that are required when you create the [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md).</span></span>

|<span data-ttu-id="0f7f1-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0f7f1-126">Property</span></span>|<span data-ttu-id="0f7f1-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0f7f1-127">Type</span></span>|<span data-ttu-id="0f7f1-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0f7f1-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0f7f1-129">id</span><span class="sxs-lookup"><span data-stu-id="0f7f1-129">id</span></span>|<span data-ttu-id="0f7f1-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="0f7f1-130">String</span></span>|<span data-ttu-id="0f7f1-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-131">Key of the entity.</span></span> <span data-ttu-id="0f7f1-132">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f1-132">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="0f7f1-133">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="0f7f1-133">targetedMobileApps</span></span>|<span data-ttu-id="0f7f1-134">Colección string</span><span class="sxs-lookup"><span data-stu-id="0f7f1-134">String collection</span></span>|<span data-ttu-id="0f7f1-135">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-135">the associated app.</span></span> <span data-ttu-id="0f7f1-136">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f1-136">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="0f7f1-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="0f7f1-137">createdDateTime</span></span>|<span data-ttu-id="0f7f1-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0f7f1-138">DateTimeOffset</span></span>|<span data-ttu-id="0f7f1-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-139">DateTime the object was created.</span></span> <span data-ttu-id="0f7f1-140">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f1-140">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="0f7f1-141">descripción</span><span class="sxs-lookup"><span data-stu-id="0f7f1-141">description</span></span>|<span data-ttu-id="0f7f1-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="0f7f1-142">String</span></span>|<span data-ttu-id="0f7f1-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="0f7f1-144">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f1-144">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="0f7f1-145">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0f7f1-145">lastModifiedDateTime</span></span>|<span data-ttu-id="0f7f1-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0f7f1-146">DateTimeOffset</span></span>|<span data-ttu-id="0f7f1-147">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-147">DateTime the object was last modified.</span></span> <span data-ttu-id="0f7f1-148">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f1-148">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="0f7f1-149">displayName</span><span class="sxs-lookup"><span data-stu-id="0f7f1-149">displayName</span></span>|<span data-ttu-id="0f7f1-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="0f7f1-150">String</span></span>|<span data-ttu-id="0f7f1-151">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-151">Admin provided name of the device configuration.</span></span> <span data-ttu-id="0f7f1-152">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f1-152">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="0f7f1-153">versión</span><span class="sxs-lookup"><span data-stu-id="0f7f1-153">version</span></span>|<span data-ttu-id="0f7f1-154">Int32</span><span class="sxs-lookup"><span data-stu-id="0f7f1-154">Int32</span></span>|<span data-ttu-id="0f7f1-155">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-155">Version of the device configuration.</span></span> <span data-ttu-id="0f7f1-156">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f1-156">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="0f7f1-157">encodedSettingXml</span><span class="sxs-lookup"><span data-stu-id="0f7f1-157">encodedSettingXml</span></span>|<span data-ttu-id="0f7f1-158">Binario</span><span class="sxs-lookup"><span data-stu-id="0f7f1-158">Binary</span></span>|<span data-ttu-id="0f7f1-159">Binario Base64 de la configuración de la aplicación mdm.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-159">mdm app configuration Base64 binary.</span></span>|
|<span data-ttu-id="0f7f1-160">configuración</span><span class="sxs-lookup"><span data-stu-id="0f7f1-160">settings</span></span>|<span data-ttu-id="0f7f1-161">Colección [appConfigurationSettingItem](../resources/intune_apps_appconfigurationsettingitem.md)</span><span class="sxs-lookup"><span data-stu-id="0f7f1-161">[appConfigurationSettingItem](../resources/intune_apps_appconfigurationsettingitem.md) collection</span></span>|<span data-ttu-id="0f7f1-162">Elementos de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-162">app configuration setting items.</span></span>|



## <a name="response"></a><span data-ttu-id="0f7f1-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f7f1-163">Response</span></span>
<span data-ttu-id="0f7f1-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-164">If successful, this method returns a `200 OK` response code and an updated [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0f7f1-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f7f1-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="0f7f1-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0f7f1-166">Request</span></span>
<span data-ttu-id="0f7f1-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-167">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}
Content-type: application/json
Content-length: 534

{
  "targetedMobileApps": [
    "Targeted Mobile Apps value"
  ],
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "encodedSettingXml": "ZW5jb2RlZFNldHRpbmdYbWw=",
  "settings": [
    {
      "@odata.type": "microsoft.graph.appConfigurationSettingItem",
      "appConfigKey": "App Config Key value",
      "appConfigKeyType": "integerType",
      "appConfigKeyValue": "App Config Key Value value"
    }
  ]
}
```

### <a name="response"></a><span data-ttu-id="0f7f1-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f7f1-168">Response</span></span>
<span data-ttu-id="0f7f1-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0f7f1-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 706

{
  "@odata.type": "#microsoft.graph.iosMobileAppConfiguration",
  "id": "b2c33191-3191-b2c3-9131-c3b29131c3b2",
  "targetedMobileApps": [
    "Targeted Mobile Apps value"
  ],
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "displayName": "Display Name value",
  "version": 7,
  "encodedSettingXml": "ZW5jb2RlZFNldHRpbmdYbWw=",
  "settings": [
    {
      "@odata.type": "microsoft.graph.appConfigurationSettingItem",
      "appConfigKey": "App Config Key value",
      "appConfigKeyType": "integerType",
      "appConfigKeyValue": "App Config Key Value value"
    }
  ]
}
```








