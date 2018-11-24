# <a name="update-detectedapp"></a><span data-ttu-id="c65e2-101">Actualizar detectedApp</span><span class="sxs-lookup"><span data-stu-id="c65e2-101">Update detectedApp</span></span>

> <span data-ttu-id="c65e2-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c65e2-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c65e2-103">Actualice las propiedades de un objeto [detectedApp](../resources/intune_devices_detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="c65e2-103">Update the properties of a [detectedApp](../resources/intune_devices_detectedapp.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c65e2-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c65e2-104">Prerequisites</span></span>
<span data-ttu-id="c65e2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c65e2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c65e2-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c65e2-107">Permission type</span></span>|<span data-ttu-id="c65e2-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c65e2-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c65e2-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c65e2-109">Delegated (work or school account)</span></span>|<span data-ttu-id="c65e2-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c65e2-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="c65e2-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c65e2-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c65e2-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c65e2-112">Not supported.</span></span>|
|<span data-ttu-id="c65e2-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c65e2-113">Application</span></span>|<span data-ttu-id="c65e2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c65e2-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c65e2-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c65e2-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/detectedApps/{detectedAppId}
```

## <a name="request-headers"></a><span data-ttu-id="c65e2-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c65e2-116">Request headers</span></span>
|<span data-ttu-id="c65e2-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c65e2-117">Header</span></span>|<span data-ttu-id="c65e2-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c65e2-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c65e2-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="c65e2-119">Authorization</span></span>|<span data-ttu-id="c65e2-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c65e2-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c65e2-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c65e2-121">Accept</span></span>|<span data-ttu-id="c65e2-122">application/json</span><span class="sxs-lookup"><span data-stu-id="c65e2-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c65e2-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c65e2-123">Request body</span></span>
<span data-ttu-id="c65e2-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [detectedApp](../resources/intune_devices_detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="c65e2-124">In the request body, supply a JSON representation for the [detectedApp](../resources/intune_devices_detectedapp.md) object.</span></span>

<span data-ttu-id="c65e2-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [detectedApp](../resources/intune_devices_detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="c65e2-125">The following table shows the properties that are required when you create the [detectedApp](../resources/intune_devices_detectedapp.md).</span></span>

|<span data-ttu-id="c65e2-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c65e2-126">Property</span></span>|<span data-ttu-id="c65e2-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="c65e2-127">Type</span></span>|<span data-ttu-id="c65e2-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c65e2-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c65e2-129">id</span><span class="sxs-lookup"><span data-stu-id="c65e2-129">id</span></span>|<span data-ttu-id="c65e2-130">String</span><span class="sxs-lookup"><span data-stu-id="c65e2-130">String</span></span>|<span data-ttu-id="c65e2-131">El identificador único de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="c65e2-131">The unique Identifier for the detected application.</span></span> <span data-ttu-id="c65e2-132">Intune lo genera automáticamente en el momento en que se crea la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c65e2-132">This is automatically generated by Intune at the time the application is created.</span></span> <span data-ttu-id="c65e2-133">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c65e2-133">Read-only.</span></span>|
|<span data-ttu-id="c65e2-134">displayName</span><span class="sxs-lookup"><span data-stu-id="c65e2-134">displayName</span></span>|<span data-ttu-id="c65e2-135">String</span><span class="sxs-lookup"><span data-stu-id="c65e2-135">String</span></span>|<span data-ttu-id="c65e2-136">Nombre de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="c65e2-136">Name of the discovered application.</span></span> <span data-ttu-id="c65e2-137">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c65e2-137">Read-only</span></span>|
|<span data-ttu-id="c65e2-138">version</span><span class="sxs-lookup"><span data-stu-id="c65e2-138">version</span></span>|<span data-ttu-id="c65e2-139">String</span><span class="sxs-lookup"><span data-stu-id="c65e2-139">String</span></span>|<span data-ttu-id="c65e2-140">Versión de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="c65e2-140">Version of the discovered application.</span></span> <span data-ttu-id="c65e2-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c65e2-141">Read-only</span></span>|
|<span data-ttu-id="c65e2-142">sizeInByte</span><span class="sxs-lookup"><span data-stu-id="c65e2-142">sizeInByte</span></span>|<span data-ttu-id="c65e2-143">Int64</span><span class="sxs-lookup"><span data-stu-id="c65e2-143">Int64</span></span>|<span data-ttu-id="c65e2-144">Tamaño en bytes de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="c65e2-144">Discovered application size in bytes.</span></span> <span data-ttu-id="c65e2-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="c65e2-145">Read-only</span></span>|
|<span data-ttu-id="c65e2-146">deviceCount</span><span class="sxs-lookup"><span data-stu-id="c65e2-146">deviceCount</span></span>|<span data-ttu-id="c65e2-147">Int32</span><span class="sxs-lookup"><span data-stu-id="c65e2-147">Int32</span></span>|<span data-ttu-id="c65e2-148">El número de dispositivos que han instalado esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="c65e2-148">The number of devices that have installed this application</span></span>|



## <a name="response"></a><span data-ttu-id="c65e2-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c65e2-149">Response</span></span>
<span data-ttu-id="c65e2-150">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [detectedApp](../resources/intune_devices_detectedapp.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c65e2-150">If successful, this method returns a `200 OK` response code and an updated [detectedApp](../resources/intune_devices_detectedapp.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c65e2-151">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c65e2-151">Example</span></span>
### <a name="request"></a><span data-ttu-id="c65e2-152">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c65e2-152">Request</span></span>
<span data-ttu-id="c65e2-153">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c65e2-153">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/detectedApps/{detectedAppId}
Content-type: application/json
Content-length: 167

{
  "@odata.type": "#microsoft.graph.detectedApp",
  "displayName": "Display Name value",
  "version": "Version value",
  "sizeInByte": 10,
  "deviceCount": 11
}
```

### <a name="response"></a><span data-ttu-id="c65e2-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c65e2-154">Response</span></span>
<span data-ttu-id="c65e2-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c65e2-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 216

{
  "@odata.type": "#microsoft.graph.detectedApp",
  "id": "caf60db6-0db6-caf6-b60d-f6cab60df6ca",
  "displayName": "Display Name value",
  "version": "Version value",
  "sizeInByte": 10,
  "deviceCount": 11
}
```



