# <a name="update-devicecategory"></a><span data-ttu-id="0ca9d-101">Actualizar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="0ca9d-101">Update deviceCategory</span></span>

> <span data-ttu-id="0ca9d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0ca9d-103">Actualice las propiedades de un objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="0ca9d-103">Update the properties of a [deviceCategory](../resources/intune_shared_devicecategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0ca9d-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0ca9d-104">Prerequisites</span></span>
<span data-ttu-id="0ca9d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0ca9d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0ca9d-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0ca9d-107">Permission type</span></span>|<span data-ttu-id="0ca9d-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0ca9d-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0ca9d-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0ca9d-109">Delegated (work or school account)</span></span>|<span data-ttu-id="0ca9d-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0ca9d-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="0ca9d-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0ca9d-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0ca9d-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-112">Not supported.</span></span>|
|<span data-ttu-id="0ca9d-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0ca9d-113">Application</span></span>|<span data-ttu-id="0ca9d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0ca9d-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0ca9d-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCategories/{deviceCategoryId}
PATCH /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deviceCategory
```

## <a name="request-headers"></a><span data-ttu-id="0ca9d-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0ca9d-116">Request headers</span></span>
|<span data-ttu-id="0ca9d-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0ca9d-117">Header</span></span>|<span data-ttu-id="0ca9d-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0ca9d-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0ca9d-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="0ca9d-119">Authorization</span></span>|<span data-ttu-id="0ca9d-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0ca9d-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0ca9d-121">Accept</span></span>|<span data-ttu-id="0ca9d-122">application/json</span><span class="sxs-lookup"><span data-stu-id="0ca9d-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0ca9d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0ca9d-123">Request body</span></span>
<span data-ttu-id="0ca9d-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="0ca9d-124">In the request body, supply a JSON representation for the [deviceCategory](../resources/intune_shared_devicecategory.md) object.</span></span>

<span data-ttu-id="0ca9d-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="0ca9d-125">The following table shows the properties that are required when you create the [deviceCategory](../resources/intune_shared_devicecategory.md).</span></span>

|<span data-ttu-id="0ca9d-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0ca9d-126">Property</span></span>|<span data-ttu-id="0ca9d-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0ca9d-127">Type</span></span>|<span data-ttu-id="0ca9d-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0ca9d-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0ca9d-129">id.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-129">id</span></span>|<span data-ttu-id="0ca9d-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="0ca9d-130">String</span></span>|<span data-ttu-id="0ca9d-131">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-131">Unique identifier for the device category.</span></span> <span data-ttu-id="0ca9d-132">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-132">Read-only.</span></span>|
|<span data-ttu-id="0ca9d-133">**Incorporación**</span><span class="sxs-lookup"><span data-stu-id="0ca9d-133">**On-boarding**</span></span>|
|<span data-ttu-id="0ca9d-134">displayName</span><span class="sxs-lookup"><span data-stu-id="0ca9d-134">displayName</span></span>|<span data-ttu-id="0ca9d-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="0ca9d-135">String</span></span>|<span data-ttu-id="0ca9d-136">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-136">Display name for the device category.</span></span>|
|<span data-ttu-id="0ca9d-137">descripción</span><span class="sxs-lookup"><span data-stu-id="0ca9d-137">description</span></span>|<span data-ttu-id="0ca9d-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="0ca9d-138">String</span></span>|<span data-ttu-id="0ca9d-139">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-139">Optional description for the device category.</span></span>|



## <a name="response"></a><span data-ttu-id="0ca9d-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0ca9d-140">Response</span></span>
<span data-ttu-id="0ca9d-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCategory](../resources/intune_shared_devicecategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-141">If successful, this method returns a `200 OK` response code and an updated [deviceCategory](../resources/intune_shared_devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0ca9d-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0ca9d-142">Example</span></span>
### <a name="request"></a><span data-ttu-id="0ca9d-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0ca9d-143">Request</span></span>
<span data-ttu-id="0ca9d-144">Aquí tiene ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-144">Here are a couple of examples of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCategories/{deviceCategoryId}
Content-type: application/json
Content-length: 82

{
  "displayName": "Display Name value",
  "description": "Description value"
}

PATCH /deviceManagement/deviceManagementScripts/{deviceManagementScriptId}/deviceRunStates/{deviceManagementScriptDeviceStateId}/managedDevice/deviceCategory
```

### <a name="response"></a><span data-ttu-id="0ca9d-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0ca9d-145">Response</span></span>
<span data-ttu-id="0ca9d-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-146">Here is an example of the response.</span></span> <span data-ttu-id="0ca9d-147">Nota: Es posible que el objeto de respuesta que se muestra aquí se trunque para abreviar.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-147">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="0ca9d-148">Las propiedades de la respuesta variarán según el contexto.</span><span class="sxs-lookup"><span data-stu-id="0ca9d-148">Response properties will vary according to context.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 184

{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "f881b841-b841-f881-41b8-81f841b881f8",
  "displayName": "Display Name value",
  "description": "Description value"
}
```



