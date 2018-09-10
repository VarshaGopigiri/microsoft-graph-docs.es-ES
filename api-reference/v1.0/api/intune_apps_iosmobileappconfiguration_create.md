# <a name="create-iosmobileappconfiguration"></a><span data-ttu-id="92063-101">Crear iosMobileAppConfiguration</span><span class="sxs-lookup"><span data-stu-id="92063-101">Create iosMobileAppConfiguration</span></span>

> <span data-ttu-id="92063-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="92063-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="92063-103">Crear un nuevo objeto [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="92063-103">Create a new [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="92063-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="92063-104">Prerequisites</span></span>
<span data-ttu-id="92063-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="92063-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="92063-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="92063-107">Permission type</span></span>|<span data-ttu-id="92063-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="92063-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="92063-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="92063-109">Delegated (work or school account)</span></span>|<span data-ttu-id="92063-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="92063-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="92063-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="92063-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="92063-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="92063-112">Not supported.</span></span>|
|<span data-ttu-id="92063-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="92063-113">Application</span></span>|<span data-ttu-id="92063-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="92063-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="92063-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="92063-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="92063-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="92063-116">Request headers</span></span>
|<span data-ttu-id="92063-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92063-117">Header</span></span>|<span data-ttu-id="92063-118">Valor</span><span class="sxs-lookup"><span data-stu-id="92063-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="92063-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="92063-119">Authorization</span></span>|<span data-ttu-id="92063-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="92063-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="92063-121">Accept</span><span class="sxs-lookup"><span data-stu-id="92063-121">Accept</span></span>|<span data-ttu-id="92063-122">application/json</span><span class="sxs-lookup"><span data-stu-id="92063-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="92063-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="92063-123">Request body</span></span>
<span data-ttu-id="92063-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="92063-124">In the request body, supply a JSON representation for the iosMobileAppConfiguration object.</span></span>

<span data-ttu-id="92063-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosMobileAppConfiguration.</span><span class="sxs-lookup"><span data-stu-id="92063-125">The following table shows the properties that are required when you create the iosMobileAppConfiguration.</span></span>

|<span data-ttu-id="92063-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="92063-126">Property</span></span>|<span data-ttu-id="92063-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="92063-127">Type</span></span>|<span data-ttu-id="92063-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="92063-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="92063-129">id</span><span class="sxs-lookup"><span data-stu-id="92063-129">id</span></span>|<span data-ttu-id="92063-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="92063-130">String</span></span>|<span data-ttu-id="92063-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="92063-131">Key of the entity.</span></span> <span data-ttu-id="92063-132">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="92063-132">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="92063-133">targetedMobileApps</span><span class="sxs-lookup"><span data-stu-id="92063-133">targetedMobileApps</span></span>|<span data-ttu-id="92063-134">Colección string</span><span class="sxs-lookup"><span data-stu-id="92063-134">String collection</span></span>|<span data-ttu-id="92063-135">La aplicación asociada.</span><span class="sxs-lookup"><span data-stu-id="92063-135">the associated app.</span></span> <span data-ttu-id="92063-136">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="92063-136">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="92063-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="92063-137">createdDateTime</span></span>|<span data-ttu-id="92063-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="92063-138">DateTimeOffset</span></span>|<span data-ttu-id="92063-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="92063-139">DateTime the object was created.</span></span> <span data-ttu-id="92063-140">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="92063-140">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="92063-141">descripción</span><span class="sxs-lookup"><span data-stu-id="92063-141">description</span></span>|<span data-ttu-id="92063-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="92063-142">String</span></span>|<span data-ttu-id="92063-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92063-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="92063-144">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="92063-144">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="92063-145">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="92063-145">lastModifiedDateTime</span></span>|<span data-ttu-id="92063-146">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="92063-146">DateTimeOffset</span></span>|<span data-ttu-id="92063-147">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="92063-147">DateTime the object was last modified.</span></span> <span data-ttu-id="92063-148">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="92063-148">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="92063-149">displayName</span><span class="sxs-lookup"><span data-stu-id="92063-149">displayName</span></span>|<span data-ttu-id="92063-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="92063-150">String</span></span>|<span data-ttu-id="92063-151">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92063-151">Admin provided name of the device configuration.</span></span> <span data-ttu-id="92063-152">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="92063-152">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="92063-153">versión</span><span class="sxs-lookup"><span data-stu-id="92063-153">version</span></span>|<span data-ttu-id="92063-154">Int32</span><span class="sxs-lookup"><span data-stu-id="92063-154">Int32</span></span>|<span data-ttu-id="92063-155">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92063-155">Version of the device configuration.</span></span> <span data-ttu-id="92063-156">Heredado de [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="92063-156">Inherited from [managedDeviceMobileAppConfiguration](../resources/intune_apps_manageddevicemobileappconfiguration.md)</span></span>|
|<span data-ttu-id="92063-157">encodedSettingXml</span><span class="sxs-lookup"><span data-stu-id="92063-157">encodedSettingXml</span></span>|<span data-ttu-id="92063-158">Binario</span><span class="sxs-lookup"><span data-stu-id="92063-158">Binary</span></span>|<span data-ttu-id="92063-159">Binario Base64 de la configuración de la aplicación mdm.</span><span class="sxs-lookup"><span data-stu-id="92063-159">mdm app configuration Base64 binary.</span></span>|
|<span data-ttu-id="92063-160">configuración</span><span class="sxs-lookup"><span data-stu-id="92063-160">settings</span></span>|<span data-ttu-id="92063-161">Colección [appConfigurationSettingItem](../resources/intune_apps_appconfigurationsettingitem.md)</span><span class="sxs-lookup"><span data-stu-id="92063-161">[appConfigurationSettingItem](../resources/intune_apps_appconfigurationsettingitem.md) collection</span></span>|<span data-ttu-id="92063-162">Elementos de configuración de la configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="92063-162">app configuration setting items.</span></span>|



## <a name="response"></a><span data-ttu-id="92063-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="92063-163">Response</span></span>
<span data-ttu-id="92063-164">Si se ejecuta correctamente, este método devuelve un `201 Created` código de respuesta y un objeto [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="92063-164">If successful, this method returns a `201 Created` response code and a [iosMobileAppConfiguration](../resources/intune_apps_iosmobileappconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="92063-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="92063-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="92063-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="92063-166">Request</span></span>
<span data-ttu-id="92063-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="92063-167">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations
Content-type: application/json
Content-length: 598

{
  "@odata.type": "#microsoft.graph.iosMobileAppConfiguration",
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

### <a name="response"></a><span data-ttu-id="92063-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="92063-168">Response</span></span>
<span data-ttu-id="92063-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="92063-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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








