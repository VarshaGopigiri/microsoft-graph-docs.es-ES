# <a name="create-devicecategory"></a><span data-ttu-id="fb6cb-101">Crear deviceCategory</span><span class="sxs-lookup"><span data-stu-id="fb6cb-101">Create deviceCategory</span></span>

> <span data-ttu-id="fb6cb-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fb6cb-103">Cree un objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="fb6cb-103">Create a new [deviceCategory](../resources/intune_shared_devicecategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fb6cb-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fb6cb-104">Prerequisites</span></span>
<span data-ttu-id="fb6cb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fb6cb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fb6cb-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fb6cb-107">Permission type</span></span>|<span data-ttu-id="fb6cb-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fb6cb-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fb6cb-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fb6cb-109">Delegated (work or school account)</span></span>|<span data-ttu-id="fb6cb-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fb6cb-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="fb6cb-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fb6cb-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fb6cb-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-112">Not supported.</span></span>|
|<span data-ttu-id="fb6cb-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fb6cb-113">Application</span></span>|<span data-ttu-id="fb6cb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fb6cb-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fb6cb-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCategories
```

## <a name="request-headers"></a><span data-ttu-id="fb6cb-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb6cb-116">Request headers</span></span>
|<span data-ttu-id="fb6cb-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb6cb-117">Header</span></span>|<span data-ttu-id="fb6cb-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fb6cb-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fb6cb-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="fb6cb-119">Authorization</span></span>|<span data-ttu-id="fb6cb-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fb6cb-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fb6cb-121">Accept</span></span>|<span data-ttu-id="fb6cb-122">application/json</span><span class="sxs-lookup"><span data-stu-id="fb6cb-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fb6cb-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fb6cb-123">Request body</span></span>
<span data-ttu-id="fb6cb-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceCategory.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-124">In the request body, supply a JSON representation for the deviceCategory object.</span></span>

<span data-ttu-id="fb6cb-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceCategory.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-125">The following table shows the properties that are required when you create the deviceCategory.</span></span>

|<span data-ttu-id="fb6cb-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb6cb-126">Property</span></span>|<span data-ttu-id="fb6cb-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb6cb-127">Type</span></span>|<span data-ttu-id="fb6cb-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb6cb-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fb6cb-129">id</span><span class="sxs-lookup"><span data-stu-id="fb6cb-129">id</span></span>|<span data-ttu-id="fb6cb-130">String</span><span class="sxs-lookup"><span data-stu-id="fb6cb-130">String</span></span>|<span data-ttu-id="fb6cb-131">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-131">Unique identifier for the device category.</span></span> <span data-ttu-id="fb6cb-132">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-132">Read-only.</span></span>|
|<span data-ttu-id="fb6cb-133">displayName</span><span class="sxs-lookup"><span data-stu-id="fb6cb-133">displayName</span></span>|<span data-ttu-id="fb6cb-134">String</span><span class="sxs-lookup"><span data-stu-id="fb6cb-134">String</span></span>|<span data-ttu-id="fb6cb-135">Nombre para mostrar de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-135">Display name for the device category.</span></span>|
|<span data-ttu-id="fb6cb-136">descripción</span><span class="sxs-lookup"><span data-stu-id="fb6cb-136">description</span></span>|<span data-ttu-id="fb6cb-137">String</span><span class="sxs-lookup"><span data-stu-id="fb6cb-137">String</span></span>|<span data-ttu-id="fb6cb-138">Descripción opcional de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-138">Optional description for the device category.</span></span>|



## <a name="response"></a><span data-ttu-id="fb6cb-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb6cb-139">Response</span></span>
<span data-ttu-id="fb6cb-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceCategory](../resources/intune_shared_devicecategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-140">If successful, this method returns a `201 Created` response code and a [deviceCategory](../resources/intune_shared_devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fb6cb-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb6cb-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="fb6cb-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fb6cb-142">Request</span></span>
<span data-ttu-id="fb6cb-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCategories
Content-type: application/json
Content-length: 135

{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "displayName": "Display Name value",
  "description": "Description value"
}
```

### <a name="response"></a><span data-ttu-id="fb6cb-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb6cb-144">Response</span></span>
<span data-ttu-id="fb6cb-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fb6cb-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 184

{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "f881b841-b841-f881-41b8-81f841b881f8",
  "displayName": "Display Name value",
  "description": "Description value"
}
```



