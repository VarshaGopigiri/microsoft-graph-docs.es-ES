# <a name="update-devicecategory"></a><span data-ttu-id="60585-101">Actualizar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="60585-101">Update deviceCategory</span></span>

> <span data-ttu-id="60585-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="60585-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="60585-103">Actualice las propiedades de un objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="60585-103">Update the properties of a [deviceCategory](../resources/intune_shared_devicecategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="60585-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="60585-104">Prerequisites</span></span>
<span data-ttu-id="60585-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="60585-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="60585-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="60585-107">Permission type</span></span>|<span data-ttu-id="60585-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="60585-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="60585-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="60585-109">Delegated (work or school account)</span></span>||
| <span data-ttu-id="60585-110">&nbsp;&nbsp; **Incorporación** y</span><span class="sxs-lookup"><span data-stu-id="60585-110">&nbsp; &nbsp; **Onboarding** and</span></span> <br> <span data-ttu-id="60585-111">&nbsp;&nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="60585-111">&nbsp; &nbsp; **Device Management**</span></span>| <span data-ttu-id="60585-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="60585-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="60585-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="60585-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="60585-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="60585-114">Not supported.</span></span>|
|<span data-ttu-id="60585-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="60585-115">Application</span></span>|<span data-ttu-id="60585-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="60585-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="60585-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="60585-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCategories/{deviceCategoryId}
PATCH /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deviceCategory
```

## <a name="request-headers"></a><span data-ttu-id="60585-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="60585-118">Request headers</span></span>
|<span data-ttu-id="60585-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60585-119">Header</span></span>|<span data-ttu-id="60585-120">Valor</span><span class="sxs-lookup"><span data-stu-id="60585-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="60585-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="60585-121">Authorization</span></span>|<span data-ttu-id="60585-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="60585-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="60585-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="60585-123">Accept</span></span>|<span data-ttu-id="60585-124">application/json</span><span class="sxs-lookup"><span data-stu-id="60585-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="60585-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="60585-125">Request body</span></span>
<span data-ttu-id="60585-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="60585-126">In the request body, supply a JSON representation for the [deviceCategory](../resources/intune_shared_devicecategory.md) object.</span></span>

<span data-ttu-id="60585-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="60585-127">The following table shows the properties that are required when you create the [deviceCategory](../resources/intune_shared_devicecategory.md).</span></span>

|<span data-ttu-id="60585-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="60585-128">Property</span></span>|<span data-ttu-id="60585-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="60585-129">Type</span></span>|<span data-ttu-id="60585-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="60585-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="60585-131">id</span><span class="sxs-lookup"><span data-stu-id="60585-131">id</span></span>|<span data-ttu-id="60585-132">String</span><span class="sxs-lookup"><span data-stu-id="60585-132">String</span></span>|<span data-ttu-id="60585-133">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60585-133">Unique identifier for the device category.</span></span> <span data-ttu-id="60585-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="60585-134">Read-only.</span></span>|
|<span data-ttu-id="60585-135">**Incorporación de redes**</span><span class="sxs-lookup"><span data-stu-id="60585-135">**Onboarding**</span></span>|
|<span data-ttu-id="60585-136">displayName</span><span class="sxs-lookup"><span data-stu-id="60585-136">displayName</span></span>|<span data-ttu-id="60585-137">String</span><span class="sxs-lookup"><span data-stu-id="60585-137">String</span></span>|<span data-ttu-id="60585-138">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60585-138">Display name for the device category.</span></span>|
|<span data-ttu-id="60585-139">descripción</span><span class="sxs-lookup"><span data-stu-id="60585-139">description</span></span>|<span data-ttu-id="60585-140">String</span><span class="sxs-lookup"><span data-stu-id="60585-140">String</span></span>|<span data-ttu-id="60585-141">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="60585-141">Optional description for the device category.</span></span>|



## <a name="response"></a><span data-ttu-id="60585-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60585-142">Response</span></span>
<span data-ttu-id="60585-143">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCategory](../resources/intune_shared_devicecategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60585-143">If successful, this method returns a `200 OK` response code and an updated [deviceCategory](../resources/intune_shared_devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="60585-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="60585-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="60585-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="60585-145">Request</span></span>
<span data-ttu-id="60585-146">Estos son ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="60585-146">Here are examples of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="60585-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="60585-147">Response</span></span>
<span data-ttu-id="60585-148">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="60585-148">Here is an example of the response.</span></span> <span data-ttu-id="60585-149">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="60585-149">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="60585-150">Propiedades de la respuesta variará según el contexto.</span><span class="sxs-lookup"><span data-stu-id="60585-150">Response properties will vary according to context.</span></span>
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



