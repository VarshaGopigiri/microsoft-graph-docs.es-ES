# <a name="update-macoscustomconfiguration"></a><span data-ttu-id="71acf-101">Actualizar macOSCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="71acf-101">Update macOSCustomConfiguration</span></span>

> <span data-ttu-id="71acf-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="71acf-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="71acf-103">Actualice las propiedades de un objeto [macOSCustomConfiguration](../resources/intune_deviceconfig_macoscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="71acf-103">Update the properties of a [macOSCustomConfiguration](../resources/intune_deviceconfig_macoscustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="71acf-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="71acf-104">Prerequisites</span></span>
<span data-ttu-id="71acf-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="71acf-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="71acf-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="71acf-107">Permission type</span></span>|<span data-ttu-id="71acf-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="71acf-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="71acf-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="71acf-109">Delegated (work or school account)</span></span>|<span data-ttu-id="71acf-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="71acf-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="71acf-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="71acf-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="71acf-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71acf-112">Not supported.</span></span>|
|<span data-ttu-id="71acf-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="71acf-113">Application</span></span>|<span data-ttu-id="71acf-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="71acf-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="71acf-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="71acf-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="request-headers"></a><span data-ttu-id="71acf-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="71acf-116">Request headers</span></span>
|<span data-ttu-id="71acf-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71acf-117">Header</span></span>|<span data-ttu-id="71acf-118">Valor</span><span class="sxs-lookup"><span data-stu-id="71acf-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="71acf-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="71acf-119">Authorization</span></span>|<span data-ttu-id="71acf-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="71acf-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="71acf-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="71acf-121">Accept</span></span>|<span data-ttu-id="71acf-122">application/json</span><span class="sxs-lookup"><span data-stu-id="71acf-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="71acf-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="71acf-123">Request body</span></span>
<span data-ttu-id="71acf-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [macOSCustomConfiguration](../resources/intune_deviceconfig_macoscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="71acf-124">In the request body, supply a JSON representation for the [macOSCustomConfiguration](../resources/intune_deviceconfig_macoscustomconfiguration.md) object.</span></span>

<span data-ttu-id="71acf-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [macOSCustomConfiguration](../resources/intune_deviceconfig_macoscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="71acf-125">The following table shows the properties that are required when you create the [macOSCustomConfiguration](../resources/intune_deviceconfig_macoscustomconfiguration.md).</span></span>

|<span data-ttu-id="71acf-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="71acf-126">Property</span></span>|<span data-ttu-id="71acf-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="71acf-127">Type</span></span>|<span data-ttu-id="71acf-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="71acf-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="71acf-129">id</span><span class="sxs-lookup"><span data-stu-id="71acf-129">id</span></span>|<span data-ttu-id="71acf-130">String</span><span class="sxs-lookup"><span data-stu-id="71acf-130">String</span></span>|<span data-ttu-id="71acf-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="71acf-131">Key of the entity.</span></span> <span data-ttu-id="71acf-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="71acf-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="71acf-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="71acf-133">lastModifiedDateTime</span></span>|<span data-ttu-id="71acf-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="71acf-134">DateTimeOffset</span></span>|<span data-ttu-id="71acf-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="71acf-135">DateTime the object was last modified.</span></span> <span data-ttu-id="71acf-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="71acf-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="71acf-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="71acf-137">createdDateTime</span></span>|<span data-ttu-id="71acf-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="71acf-138">DateTimeOffset</span></span>|<span data-ttu-id="71acf-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="71acf-139">DateTime the object was created.</span></span> <span data-ttu-id="71acf-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="71acf-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="71acf-141">description</span><span class="sxs-lookup"><span data-stu-id="71acf-141">description</span></span>|<span data-ttu-id="71acf-142">String</span><span class="sxs-lookup"><span data-stu-id="71acf-142">String</span></span>|<span data-ttu-id="71acf-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71acf-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="71acf-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="71acf-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="71acf-145">displayName</span><span class="sxs-lookup"><span data-stu-id="71acf-145">displayName</span></span>|<span data-ttu-id="71acf-146">String</span><span class="sxs-lookup"><span data-stu-id="71acf-146">String</span></span>|<span data-ttu-id="71acf-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71acf-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="71acf-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="71acf-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="71acf-149">version</span><span class="sxs-lookup"><span data-stu-id="71acf-149">version</span></span>|<span data-ttu-id="71acf-150">Int32</span><span class="sxs-lookup"><span data-stu-id="71acf-150">Int32</span></span>|<span data-ttu-id="71acf-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="71acf-151">Version of the device configuration.</span></span> <span data-ttu-id="71acf-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="71acf-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="71acf-153">payloadName</span><span class="sxs-lookup"><span data-stu-id="71acf-153">payloadName</span></span>|<span data-ttu-id="71acf-154">String</span><span class="sxs-lookup"><span data-stu-id="71acf-154">String</span></span>|<span data-ttu-id="71acf-155">Nombre que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="71acf-155">Name that is displayed to the user.</span></span>|
|<span data-ttu-id="71acf-156">payloadFileName</span><span class="sxs-lookup"><span data-stu-id="71acf-156">payloadFileName</span></span>|<span data-ttu-id="71acf-157">String</span><span class="sxs-lookup"><span data-stu-id="71acf-157">String</span></span>|<span data-ttu-id="71acf-158">Nombre de archivo de carga útil (\*.mobileconfig</span><span class="sxs-lookup"><span data-stu-id="71acf-158">Payload file name (\*.mobileconfig</span></span> | <span data-ttu-id="71acf-159">\*.xml).</span><span class="sxs-lookup"><span data-stu-id="71acf-159">\*.xml).</span></span>|
|<span data-ttu-id="71acf-160">carga útil</span><span class="sxs-lookup"><span data-stu-id="71acf-160">payload</span></span>|<span data-ttu-id="71acf-161">Binario</span><span class="sxs-lookup"><span data-stu-id="71acf-161">Binary</span></span>|<span data-ttu-id="71acf-162">Carga útil.</span><span class="sxs-lookup"><span data-stu-id="71acf-162">Payload.</span></span> <span data-ttu-id="71acf-163">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="71acf-163">(UTF8 encoded byte array)</span></span>|



## <a name="response"></a><span data-ttu-id="71acf-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71acf-164">Response</span></span>
<span data-ttu-id="71acf-165">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [macOSCustomConfiguration](../resources/intune_deviceconfig_macoscustomconfiguration.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="71acf-165">If successful, this method returns a `200 OK` response code and an updated [macOSCustomConfiguration](../resources/intune_deviceconfig_macoscustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="71acf-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="71acf-166">Example</span></span>
### <a name="request"></a><span data-ttu-id="71acf-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="71acf-167">Request</span></span>
<span data-ttu-id="71acf-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="71acf-168">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
Content-type: application/json
Content-length: 281

{
  "@odata.type": "#microsoft.graph.macOSCustomConfiguration",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "payloadName": "Payload Name value",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA=="
}
```

### <a name="response"></a><span data-ttu-id="71acf-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="71acf-169">Response</span></span>
<span data-ttu-id="71acf-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="71acf-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 453

{
  "@odata.type": "#microsoft.graph.macOSCustomConfiguration",
  "id": "a253835d-835d-a253-5d83-53a25d8353a2",
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



