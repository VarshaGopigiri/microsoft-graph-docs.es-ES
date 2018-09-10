# <a name="update-ioscustomconfiguration"></a><span data-ttu-id="1de74-101">Actualizar iosCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="1de74-101">Update iosCustomConfiguration</span></span>

> <span data-ttu-id="1de74-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1de74-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1de74-103">Actualice las propiedades de un objeto [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1de74-103">Update the properties of a [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1de74-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1de74-104">Prerequisites</span></span>
<span data-ttu-id="1de74-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1de74-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1de74-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1de74-107">Permission type</span></span>|<span data-ttu-id="1de74-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1de74-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1de74-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1de74-109">Delegated (work or school account)</span></span>|<span data-ttu-id="1de74-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1de74-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="1de74-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1de74-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1de74-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1de74-112">Not supported.</span></span>|
|<span data-ttu-id="1de74-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1de74-113">Application</span></span>|<span data-ttu-id="1de74-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1de74-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1de74-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1de74-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="1de74-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1de74-116">Request headers</span></span>
|<span data-ttu-id="1de74-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1de74-117">Header</span></span>|<span data-ttu-id="1de74-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1de74-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1de74-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="1de74-119">Authorization</span></span>|<span data-ttu-id="1de74-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1de74-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1de74-121">Accept</span><span class="sxs-lookup"><span data-stu-id="1de74-121">Accept</span></span>|<span data-ttu-id="1de74-122">application/json</span><span class="sxs-lookup"><span data-stu-id="1de74-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1de74-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1de74-123">Request body</span></span>
<span data-ttu-id="1de74-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1de74-124">In the request body, supply a JSON representation for the [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md) object.</span></span>

<span data-ttu-id="1de74-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1de74-125">The following table shows the properties that are required when you create the [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md).</span></span>

|<span data-ttu-id="1de74-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1de74-126">Property</span></span>|<span data-ttu-id="1de74-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="1de74-127">Type</span></span>|<span data-ttu-id="1de74-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="1de74-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1de74-129">id</span><span class="sxs-lookup"><span data-stu-id="1de74-129">id</span></span>|<span data-ttu-id="1de74-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="1de74-130">String</span></span>|<span data-ttu-id="1de74-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="1de74-131">Key of the entity.</span></span> <span data-ttu-id="1de74-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1de74-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1de74-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1de74-133">lastModifiedDateTime</span></span>|<span data-ttu-id="1de74-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1de74-134">DateTimeOffset</span></span>|<span data-ttu-id="1de74-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="1de74-135">DateTime the object was last modified.</span></span> <span data-ttu-id="1de74-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1de74-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1de74-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1de74-137">createdDateTime</span></span>|<span data-ttu-id="1de74-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1de74-138">DateTimeOffset</span></span>|<span data-ttu-id="1de74-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="1de74-139">DateTime the object was created.</span></span> <span data-ttu-id="1de74-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1de74-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1de74-141">description</span><span class="sxs-lookup"><span data-stu-id="1de74-141">description</span></span>|<span data-ttu-id="1de74-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="1de74-142">String</span></span>|<span data-ttu-id="1de74-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1de74-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="1de74-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1de74-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1de74-145">displayName</span><span class="sxs-lookup"><span data-stu-id="1de74-145">displayName</span></span>|<span data-ttu-id="1de74-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="1de74-146">String</span></span>|<span data-ttu-id="1de74-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1de74-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="1de74-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1de74-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1de74-149">version</span><span class="sxs-lookup"><span data-stu-id="1de74-149">version</span></span>|<span data-ttu-id="1de74-150">Int32</span><span class="sxs-lookup"><span data-stu-id="1de74-150">Int32</span></span>|<span data-ttu-id="1de74-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1de74-151">Version of the device configuration.</span></span> <span data-ttu-id="1de74-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="1de74-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="1de74-153">payloadName</span><span class="sxs-lookup"><span data-stu-id="1de74-153">payloadName</span></span>|<span data-ttu-id="1de74-154">Cadena</span><span class="sxs-lookup"><span data-stu-id="1de74-154">String</span></span>|<span data-ttu-id="1de74-155">Nombre que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="1de74-155">Name that is displayed to the user.</span></span>|
|<span data-ttu-id="1de74-156">payloadFileName</span><span class="sxs-lookup"><span data-stu-id="1de74-156">payloadFileName</span></span>|<span data-ttu-id="1de74-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="1de74-157">String</span></span>|<span data-ttu-id="1de74-158">Nombre de archivo de carga útil (\*.mobileconfig</span><span class="sxs-lookup"><span data-stu-id="1de74-158">Payload file name (\*.mobileconfig</span></span> | <span data-ttu-id="1de74-159">\*.xml).</span><span class="sxs-lookup"><span data-stu-id="1de74-159">\*.xml).</span></span>|
|<span data-ttu-id="1de74-160">carga útil</span><span class="sxs-lookup"><span data-stu-id="1de74-160">payload</span></span>|<span data-ttu-id="1de74-161">Binario</span><span class="sxs-lookup"><span data-stu-id="1de74-161">Binary</span></span>|<span data-ttu-id="1de74-162">Carga útil.</span><span class="sxs-lookup"><span data-stu-id="1de74-162">Payload.</span></span> <span data-ttu-id="1de74-163">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="1de74-163">(UTF8 encoded byte array)</span></span>|



## <a name="response"></a><span data-ttu-id="1de74-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1de74-164">Response</span></span>
<span data-ttu-id="1de74-165">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1de74-165">If successful, this method returns a `200 OK` response code and an updated [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1de74-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1de74-166">Example</span></span>
### <a name="request"></a><span data-ttu-id="1de74-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1de74-167">Request</span></span>
<span data-ttu-id="1de74-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1de74-168">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 282

{
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "payloadName": "Payload Name value",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA=="
}
```

### <a name="response"></a><span data-ttu-id="1de74-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1de74-169">Response</span></span>
<span data-ttu-id="1de74-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1de74-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 451

{
  "@odata.type": "#microsoft.graph.iosCustomConfiguration",
  "id": "f34428e3-28e3-f344-e328-44f3e32844f3",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "payloadName": "Payload Name value",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA=="
}
```








