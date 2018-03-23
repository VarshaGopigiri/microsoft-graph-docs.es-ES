# <a name="update-windows10enterprisemodernappmanagementconfiguration"></a><span data-ttu-id="e6d2c-101">Actualizar windows10EnterpriseModernAppManagementConfiguration</span><span class="sxs-lookup"><span data-stu-id="e6d2c-101">Update windows10EnterpriseModernAppManagementConfiguration</span></span>

> <span data-ttu-id="e6d2c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e6d2c-103">Actualice las propiedades de un objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune_deviceconfig_windows10enterprisemodernappmanagementconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e6d2c-103">Update the properties of a [calendar](../resources/intune_deviceconfig_windows10enterprisemodernappmanagementconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e6d2c-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e6d2c-104">Prerequisites</span></span>
<span data-ttu-id="e6d2c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e6d2c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e6d2c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e6d2c-107">Permission type</span></span>|<span data-ttu-id="e6d2c-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e6d2c-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e6d2c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e6d2c-109">Delegated (work or school account)</span></span>|<span data-ttu-id="e6d2c-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e6d2c-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="e6d2c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e6d2c-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e6d2c-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-112">Not supported.</span></span>|
|<span data-ttu-id="e6d2c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e6d2c-113">Application</span></span>|<span data-ttu-id="e6d2c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e6d2c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e6d2c-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="e6d2c-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e6d2c-116">Request headers</span></span>
|<span data-ttu-id="e6d2c-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e6d2c-117">Header</span></span>|<span data-ttu-id="e6d2c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e6d2c-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e6d2c-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="e6d2c-119">Authorization</span></span>|<span data-ttu-id="e6d2c-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="e6d2c-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="e6d2c-121">Accept</span></span>|<span data-ttu-id="e6d2c-122">application/json</span><span class="sxs-lookup"><span data-stu-id="e6d2c-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e6d2c-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e6d2c-123">Request body</span></span>
<span data-ttu-id="e6d2c-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune_deviceconfig_windows10enterprisemodernappmanagementconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e6d2c-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_windows10enterprisemodernappmanagementconfiguration.md) object.</span></span>

<span data-ttu-id="e6d2c-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune_deviceconfig_windows10enterprisemodernappmanagementconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="e6d2c-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="e6d2c-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e6d2c-126">Property</span></span>|<span data-ttu-id="e6d2c-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="e6d2c-127">Type</span></span>|<span data-ttu-id="e6d2c-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e6d2c-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="e6d2c-129">id</span><span class="sxs-lookup"><span data-stu-id="e6d2c-129">id</span></span>|<span data-ttu-id="e6d2c-130">String</span><span class="sxs-lookup"><span data-stu-id="e6d2c-130">String</span></span>|<span data-ttu-id="e6d2c-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-131">Key of the setting.</span></span> <span data-ttu-id="e6d2c-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e6d2c-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e6d2c-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="e6d2c-133">lastModifiedDateTime</span></span>|<span data-ttu-id="e6d2c-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e6d2c-134">DateTimeOffset</span></span>|<span data-ttu-id="e6d2c-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-135">Indicates the date the object was last modified.</span></span> <span data-ttu-id="e6d2c-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e6d2c-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e6d2c-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="e6d2c-137">createdDateTime</span></span>|<span data-ttu-id="e6d2c-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="e6d2c-138">DateTimeOffset</span></span>|<span data-ttu-id="e6d2c-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-139">DateTime the object was created.</span></span> <span data-ttu-id="e6d2c-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e6d2c-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e6d2c-141">description</span><span class="sxs-lookup"><span data-stu-id="e6d2c-141">description</span></span>|<span data-ttu-id="e6d2c-142">String</span><span class="sxs-lookup"><span data-stu-id="e6d2c-142">String</span></span>|<span data-ttu-id="e6d2c-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="e6d2c-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e6d2c-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e6d2c-145">displayName</span><span class="sxs-lookup"><span data-stu-id="e6d2c-145">displayName</span></span>|<span data-ttu-id="e6d2c-146">String</span><span class="sxs-lookup"><span data-stu-id="e6d2c-146">String</span></span>|<span data-ttu-id="e6d2c-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="e6d2c-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e6d2c-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e6d2c-149">version</span><span class="sxs-lookup"><span data-stu-id="e6d2c-149">version</span></span>|<span data-ttu-id="e6d2c-150">Int32</span><span class="sxs-lookup"><span data-stu-id="e6d2c-150">Int32</span></span>|<span data-ttu-id="e6d2c-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-151">Version of the device configuration.</span></span> <span data-ttu-id="e6d2c-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="e6d2c-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="e6d2c-153">uninstallBuiltInApps</span><span class="sxs-lookup"><span data-stu-id="e6d2c-153">uninstallBuiltInApps</span></span>|<span data-ttu-id="e6d2c-154">Boolean</span><span class="sxs-lookup"><span data-stu-id="e6d2c-154">Boolean</span></span>|<span data-ttu-id="e6d2c-155">Indica si se desinstalará o no una lista fija de aplicaciones integradas de Windows.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-155">Indicates whether or not to uninstall a fixed list of built-in Windows apps.</span></span>|



## <a name="response"></a><span data-ttu-id="e6d2c-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6d2c-156">Response</span></span>
<span data-ttu-id="e6d2c-157">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10EnterpriseModernAppManagementConfiguration](../resources/intune_deviceconfig_windows10enterprisemodernappmanagementconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-157">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_windows10enterprisemodernappmanagementconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e6d2c-158">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e6d2c-158">Example</span></span>
### <a name="request"></a><span data-ttu-id="e6d2c-159">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e6d2c-159">Request</span></span>
<span data-ttu-id="e6d2c-160">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-160">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 196

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "uninstallBuiltInApps": true
}
```

### <a name="response"></a><span data-ttu-id="e6d2c-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e6d2c-161">Response</span></span>
<span data-ttu-id="e6d2c-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e6d2c-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 394

{
  "@odata.type": "#microsoft.graph.windows10EnterpriseModernAppManagementConfiguration",
  "id": "d6577687-7687-d657-8776-57d6877657d6",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "uninstallBuiltInApps": true
}
```



