# <a name="update-macosdevicefeaturesconfiguration"></a><span data-ttu-id="8ac2f-101">Actualizar macOSDeviceFeaturesConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ac2f-101">Update macOSDeviceFeaturesConfiguration</span></span>

> <span data-ttu-id="8ac2f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8ac2f-103">Actualice las propiedades de un objeto [macOSDeviceFeaturesConfiguration](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="8ac2f-103">Update the properties of a [macOSDeviceFeaturesConfiguration](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8ac2f-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8ac2f-104">Prerequisites</span></span>
<span data-ttu-id="8ac2f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8ac2f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8ac2f-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8ac2f-107">Permission type</span></span>|<span data-ttu-id="8ac2f-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8ac2f-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8ac2f-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8ac2f-109">Delegated (work or school account)</span></span>|<span data-ttu-id="8ac2f-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8ac2f-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8ac2f-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8ac2f-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8ac2f-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-112">Not supported.</span></span>|
|<span data-ttu-id="8ac2f-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8ac2f-113">Application</span></span>|<span data-ttu-id="8ac2f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8ac2f-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8ac2f-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="8ac2f-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8ac2f-116">Request headers</span></span>
|<span data-ttu-id="8ac2f-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8ac2f-117">Header</span></span>|<span data-ttu-id="8ac2f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8ac2f-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8ac2f-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="8ac2f-119">Authorization</span></span>|<span data-ttu-id="8ac2f-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8ac2f-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8ac2f-121">Accept</span></span>|<span data-ttu-id="8ac2f-122">application/json</span><span class="sxs-lookup"><span data-stu-id="8ac2f-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8ac2f-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8ac2f-123">Request body</span></span>
<span data-ttu-id="8ac2f-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSDeviceFeaturesConfiguration](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="8ac2f-124">In the request body, supply a JSON representation for the [macOSDeviceFeaturesConfiguration](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md) object.</span></span>

<span data-ttu-id="8ac2f-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSDeviceFeaturesConfiguration](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="8ac2f-125">The following table shows the properties that are required when you create the [macOSDeviceFeaturesConfiguration](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md).</span></span>

|<span data-ttu-id="8ac2f-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8ac2f-126">Property</span></span>|<span data-ttu-id="8ac2f-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ac2f-127">Type</span></span>|<span data-ttu-id="8ac2f-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ac2f-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8ac2f-129">id</span><span class="sxs-lookup"><span data-stu-id="8ac2f-129">id</span></span>|<span data-ttu-id="8ac2f-130">String</span><span class="sxs-lookup"><span data-stu-id="8ac2f-130">String</span></span>|<span data-ttu-id="8ac2f-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-131">Key of the entity.</span></span> <span data-ttu-id="8ac2f-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ac2f-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ac2f-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8ac2f-133">lastModifiedDateTime</span></span>|<span data-ttu-id="8ac2f-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8ac2f-134">DateTimeOffset</span></span>|<span data-ttu-id="8ac2f-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-135">DateTime the object was last modified.</span></span> <span data-ttu-id="8ac2f-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ac2f-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ac2f-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8ac2f-137">createdDateTime</span></span>|<span data-ttu-id="8ac2f-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8ac2f-138">DateTimeOffset</span></span>|<span data-ttu-id="8ac2f-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-139">DateTime the object was created.</span></span> <span data-ttu-id="8ac2f-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ac2f-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ac2f-141">description</span><span class="sxs-lookup"><span data-stu-id="8ac2f-141">description</span></span>|<span data-ttu-id="8ac2f-142">String</span><span class="sxs-lookup"><span data-stu-id="8ac2f-142">String</span></span>|<span data-ttu-id="8ac2f-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="8ac2f-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ac2f-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ac2f-145">displayName</span><span class="sxs-lookup"><span data-stu-id="8ac2f-145">displayName</span></span>|<span data-ttu-id="8ac2f-146">String</span><span class="sxs-lookup"><span data-stu-id="8ac2f-146">String</span></span>|<span data-ttu-id="8ac2f-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="8ac2f-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ac2f-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="8ac2f-149">version</span><span class="sxs-lookup"><span data-stu-id="8ac2f-149">version</span></span>|<span data-ttu-id="8ac2f-150">Int32</span><span class="sxs-lookup"><span data-stu-id="8ac2f-150">Int32</span></span>|<span data-ttu-id="8ac2f-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-151">Version of the device configuration.</span></span> <span data-ttu-id="8ac2f-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="8ac2f-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|



## <a name="response"></a><span data-ttu-id="8ac2f-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ac2f-153">Response</span></span>
<span data-ttu-id="8ac2f-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSDeviceFeaturesConfiguration](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-154">If successful, this method returns a `200 OK` response code and an updated [macOSDeviceFeaturesConfiguration](../resources/intune_deviceconfig_macosdevicefeaturesconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8ac2f-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8ac2f-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="8ac2f-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8ac2f-156">Request</span></span>
<span data-ttu-id="8ac2f-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-157">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 170

{
  "@odata.type": "#microsoft.graph.macOSDeviceFeaturesConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7
}
```

### <a name="response"></a><span data-ttu-id="8ac2f-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8ac2f-158">Response</span></span>
<span data-ttu-id="8ac2f-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8ac2f-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 342

{
  "@odata.type": "#microsoft.graph.macOSDeviceFeaturesConfiguration",
  "id": "49fa957d-957d-49fa-7d95-fa497d95fa49",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7
}
```



