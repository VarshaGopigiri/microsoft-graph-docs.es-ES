# <a name="create-ioscustomconfiguration"></a><span data-ttu-id="c68d7-101">Crear iosCustomConfiguration</span><span class="sxs-lookup"><span data-stu-id="c68d7-101">Create iosCustomConfiguration</span></span>

> <span data-ttu-id="c68d7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c68d7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c68d7-103">Cree un objeto [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="c68d7-103">Create a new [plannerBucket](../resources/intune_deviceconfig_ioscustomconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c68d7-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c68d7-104">Prerequisites</span></span>
<span data-ttu-id="c68d7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c68d7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c68d7-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c68d7-107">Permission type</span></span>|<span data-ttu-id="c68d7-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c68d7-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c68d7-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c68d7-109">Delegated (work or school account)</span></span>|<span data-ttu-id="c68d7-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c68d7-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="c68d7-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c68d7-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c68d7-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c68d7-112">Not supported.</span></span>|
|<span data-ttu-id="c68d7-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c68d7-113">Application</span></span>|<span data-ttu-id="c68d7-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c68d7-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c68d7-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c68d7-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="c68d7-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c68d7-116">Request headers</span></span>
|<span data-ttu-id="c68d7-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c68d7-117">Header</span></span>|<span data-ttu-id="c68d7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c68d7-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c68d7-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="c68d7-119">Authorization</span></span>|<span data-ttu-id="c68d7-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c68d7-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="c68d7-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c68d7-121">Accept</span></span>|<span data-ttu-id="c68d7-122">application/json</span><span class="sxs-lookup"><span data-stu-id="c68d7-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c68d7-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c68d7-123">Request body</span></span>
<span data-ttu-id="c68d7-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto iosCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c68d7-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="c68d7-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto iosCustomConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c68d7-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="c68d7-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c68d7-126">Property</span></span>|<span data-ttu-id="c68d7-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="c68d7-127">Type</span></span>|<span data-ttu-id="c68d7-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c68d7-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c68d7-129">id</span><span class="sxs-lookup"><span data-stu-id="c68d7-129">id</span></span>|<span data-ttu-id="c68d7-130">String</span><span class="sxs-lookup"><span data-stu-id="c68d7-130">String</span></span>|<span data-ttu-id="c68d7-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c68d7-131">Key of the setting.</span></span> <span data-ttu-id="c68d7-132">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c68d7-132">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c68d7-133">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="c68d7-133">lastModifiedDateTime</span></span>|<span data-ttu-id="c68d7-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c68d7-134">DateTimeOffset</span></span>|<span data-ttu-id="c68d7-135">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="c68d7-135">Indicates the date the object was last modified.</span></span> <span data-ttu-id="c68d7-136">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c68d7-136">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c68d7-137">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="c68d7-137">createdDateTime</span></span>|<span data-ttu-id="c68d7-138">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c68d7-138">DateTimeOffset</span></span>|<span data-ttu-id="c68d7-139">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="c68d7-139">DateTime the object was created.</span></span> <span data-ttu-id="c68d7-140">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c68d7-140">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c68d7-141">description</span><span class="sxs-lookup"><span data-stu-id="c68d7-141">description</span></span>|<span data-ttu-id="c68d7-142">String</span><span class="sxs-lookup"><span data-stu-id="c68d7-142">String</span></span>|<span data-ttu-id="c68d7-143">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c68d7-143">Admin provided description of the Device Configuration.</span></span> <span data-ttu-id="c68d7-144">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c68d7-144">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c68d7-145">displayName</span><span class="sxs-lookup"><span data-stu-id="c68d7-145">displayName</span></span>|<span data-ttu-id="c68d7-146">String</span><span class="sxs-lookup"><span data-stu-id="c68d7-146">String</span></span>|<span data-ttu-id="c68d7-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c68d7-147">Admin provided name of the device configuration.</span></span> <span data-ttu-id="c68d7-148">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c68d7-148">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c68d7-149">version</span><span class="sxs-lookup"><span data-stu-id="c68d7-149">version</span></span>|<span data-ttu-id="c68d7-150">Int32</span><span class="sxs-lookup"><span data-stu-id="c68d7-150">Int32</span></span>|<span data-ttu-id="c68d7-151">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c68d7-151">Version of the device configuration.</span></span> <span data-ttu-id="c68d7-152">Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="c68d7-152">Inherited from [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)</span></span>|
|<span data-ttu-id="c68d7-153">payloadName</span><span class="sxs-lookup"><span data-stu-id="c68d7-153">payloadName</span></span>|<span data-ttu-id="c68d7-154">String</span><span class="sxs-lookup"><span data-stu-id="c68d7-154">String</span></span>|<span data-ttu-id="c68d7-155">Nombre que se muestra al usuario.</span><span class="sxs-lookup"><span data-stu-id="c68d7-155">Name that is displayed to the user.</span></span>|
|<span data-ttu-id="c68d7-156">payloadFileName</span><span class="sxs-lookup"><span data-stu-id="c68d7-156">payloadFileName</span></span>|<span data-ttu-id="c68d7-157">String</span><span class="sxs-lookup"><span data-stu-id="c68d7-157">String</span></span>|<span data-ttu-id="c68d7-158">Nombre de archivo de carga útil (\*.mobileconfig</span><span class="sxs-lookup"><span data-stu-id="c68d7-158">Payload file name (\*.mobileconfig</span></span> | <span data-ttu-id="c68d7-159">\*.xml).</span><span class="sxs-lookup"><span data-stu-id="c68d7-159">XML</span></span>|
|<span data-ttu-id="c68d7-160">carga útil</span><span class="sxs-lookup"><span data-stu-id="c68d7-160">Notification payload</span></span>|<span data-ttu-id="c68d7-161">Binario</span><span class="sxs-lookup"><span data-stu-id="c68d7-161">Binary</span></span>|<span data-ttu-id="c68d7-162">Carga útil.</span><span class="sxs-lookup"><span data-stu-id="c68d7-162">Payload.</span></span> <span data-ttu-id="c68d7-163">(Matriz de bytes codificada UTF8)</span><span class="sxs-lookup"><span data-stu-id="c68d7-163">(UTF8 encoded byte array)</span></span>|



## <a name="response"></a><span data-ttu-id="c68d7-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c68d7-164">Response</span></span>
<span data-ttu-id="c68d7-165">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [iosCustomConfiguration](../resources/intune_deviceconfig_ioscustomconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c68d7-165">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_deviceconfig_ioscustomconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c68d7-166">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c68d7-166">Example</span></span>
### <a name="request"></a><span data-ttu-id="c68d7-167">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c68d7-167">Request</span></span>
<span data-ttu-id="c68d7-168">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c68d7-168">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
Content-type: application/json
Content-length: 343

{
  "@odata.type": "#microsoft.graph.iosCustomConfiguration",
  "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
  "description": "Description value",
  "displayName": "Display Name value",
  "version": 7,
  "payloadName": "Payload Name value",
  "payloadFileName": "Payload File Name value",
  "payload": "cGF5bG9hZA=="
}
```

### <a name="response"></a><span data-ttu-id="c68d7-169">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c68d7-169">Response</span></span>
<span data-ttu-id="c68d7-p109">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c68d7-p109">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



