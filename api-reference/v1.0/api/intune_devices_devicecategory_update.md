# <a name="update-devicecategory"></a><span data-ttu-id="68d61-101">Actualizar deviceCategory</span><span class="sxs-lookup"><span data-stu-id="68d61-101">Update deviceCategory</span></span>

> <span data-ttu-id="68d61-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="68d61-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="68d61-103">Actualice las propiedades de un objeto [deviceCategory](../resources/intune_devices_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="68d61-103">Update the properties of a [calendar](../resources/intune_devices_devicecategory.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="68d61-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="68d61-104">Prerequisites</span></span>
<span data-ttu-id="68d61-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="68d61-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="68d61-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="68d61-107">Permission type</span></span>|<span data-ttu-id="68d61-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="68d61-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="68d61-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="68d61-109">Delegated (work or school account)</span></span>|<span data-ttu-id="68d61-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="68d61-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="68d61-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="68d61-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="68d61-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68d61-112">Not supported.</span></span>|
|<span data-ttu-id="68d61-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="68d61-113">Application</span></span>|<span data-ttu-id="68d61-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="68d61-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="68d61-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="68d61-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deviceCategory
```

## <a name="request-headers"></a><span data-ttu-id="68d61-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="68d61-116">Request headers</span></span>
|<span data-ttu-id="68d61-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68d61-117">Header</span></span>|<span data-ttu-id="68d61-118">Valor</span><span class="sxs-lookup"><span data-stu-id="68d61-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="68d61-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="68d61-119">Authorization</span></span>|<span data-ttu-id="68d61-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="68d61-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="68d61-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="68d61-121">Accept</span></span>|<span data-ttu-id="68d61-122">application/json</span><span class="sxs-lookup"><span data-stu-id="68d61-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="68d61-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="68d61-123">Request body</span></span>
<span data-ttu-id="68d61-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCategory](../resources/intune_devices_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="68d61-124">In the request body, supply a JSON representation of [directoryObject](../resources/intune_devices_devicecategory.md) object.</span></span>

<span data-ttu-id="68d61-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCategory](../resources/intune_devices_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="68d61-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="68d61-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="68d61-126">Property</span></span>|<span data-ttu-id="68d61-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="68d61-127">Type</span></span>|<span data-ttu-id="68d61-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="68d61-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="68d61-129">id</span><span class="sxs-lookup"><span data-stu-id="68d61-129">id</span></span>|<span data-ttu-id="68d61-130">String</span><span class="sxs-lookup"><span data-stu-id="68d61-130">String</span></span>|<span data-ttu-id="68d61-131">El identificador único de la categoría de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="68d61-131">Unique identifier for the device category.</span></span> <span data-ttu-id="68d61-132">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="68d61-132">Read-only.</span></span>|



## <a name="response"></a><span data-ttu-id="68d61-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68d61-133">Response</span></span>
<span data-ttu-id="68d61-134">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCategory](../resources/intune_devices_devicecategory.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="68d61-134">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_devices_devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="68d61-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="68d61-135">Example</span></span>
### <a name="request"></a><span data-ttu-id="68d61-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="68d61-136">Request</span></span>
<span data-ttu-id="68d61-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="68d61-137">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deviceCategory
Content-type: application/json
Content-length: 2

{}
```

### <a name="response"></a><span data-ttu-id="68d61-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="68d61-138">Response</span></span>
<span data-ttu-id="68d61-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="68d61-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 105

{
  "@odata.type": "#microsoft.graph.deviceCategory",
  "id": "f881b841-b841-f881-41b8-81f841b881f8"
}
```



