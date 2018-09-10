# <a name="update-importedwindowsautopilotdeviceidentity"></a><span data-ttu-id="6c426-101">Actualizar importedWindowsAutopilotDeviceIdentity</span><span class="sxs-lookup"><span data-stu-id="6c426-101">Update importedWindowsAutopilotDeviceIdentity</span></span>

> <span data-ttu-id="6c426-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6c426-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6c426-103">Actualiza las propiedades de un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="6c426-103">Update the properties of a [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6c426-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6c426-104">Prerequisites</span></span>
<span data-ttu-id="6c426-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6c426-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6c426-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6c426-107">Permission type</span></span>|<span data-ttu-id="6c426-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6c426-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6c426-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6c426-109">Delegated (work or school account)</span></span>|<span data-ttu-id="6c426-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6c426-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="6c426-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6c426-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6c426-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c426-112">Not supported.</span></span>|
|<span data-ttu-id="6c426-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6c426-113">Application</span></span>|<span data-ttu-id="6c426-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6c426-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6c426-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6c426-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/importedWindowsAutopilotDeviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
PATCH /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads/{importedWindowsAutopilotDeviceIdentityUploadId}/deviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
```

## <a name="request-headers"></a><span data-ttu-id="6c426-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6c426-116">Request headers</span></span>
|<span data-ttu-id="6c426-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c426-117">Header</span></span>|<span data-ttu-id="6c426-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6c426-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6c426-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="6c426-119">Authorization</span></span>|<span data-ttu-id="6c426-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6c426-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6c426-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6c426-121">Accept</span></span>|<span data-ttu-id="6c426-122">application/json</span><span class="sxs-lookup"><span data-stu-id="6c426-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6c426-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6c426-123">Request body</span></span>
<span data-ttu-id="6c426-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="6c426-124">In the request body, supply a JSON representation for the [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md) object.</span></span>

<span data-ttu-id="6c426-125">En la tabla siguiente se muestran las propiedades necesarias para crear [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md).</span><span class="sxs-lookup"><span data-stu-id="6c426-125">The following table shows the properties that are required when you create the [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md).</span></span>

|<span data-ttu-id="6c426-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6c426-126">Property</span></span>|<span data-ttu-id="6c426-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="6c426-127">Type</span></span>|<span data-ttu-id="6c426-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="6c426-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6c426-129">id</span><span class="sxs-lookup"><span data-stu-id="6c426-129">id</span></span>|<span data-ttu-id="6c426-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c426-130">String</span></span>|<span data-ttu-id="6c426-131">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="6c426-131">The GUID for the object</span></span>|
|<span data-ttu-id="6c426-132">orderIdentifier</span><span class="sxs-lookup"><span data-stu-id="6c426-132">orderIdentifier</span></span>|<span data-ttu-id="6c426-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c426-133">String</span></span>|<span data-ttu-id="6c426-134">Id. de pedido del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="6c426-134">Order Id of the Windows autopilot device.</span></span>|
|<span data-ttu-id="6c426-135">serialNumber</span><span class="sxs-lookup"><span data-stu-id="6c426-135">serialNumber</span></span>|<span data-ttu-id="6c426-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c426-136">String</span></span>|<span data-ttu-id="6c426-137">Número de serie del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="6c426-137">Serial number of the Windows autopilot device.</span></span>|
|<span data-ttu-id="6c426-138">productKey</span><span class="sxs-lookup"><span data-stu-id="6c426-138">productKey</span></span>|<span data-ttu-id="6c426-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="6c426-139">String</span></span>|<span data-ttu-id="6c426-140">Clave de producto del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="6c426-140">Product Key of the Windows autopilot device.</span></span>|
|<span data-ttu-id="6c426-141">hardwareIdentifier</span><span class="sxs-lookup"><span data-stu-id="6c426-141">hardwareIdentifier</span></span>|<span data-ttu-id="6c426-142">Binario</span><span class="sxs-lookup"><span data-stu-id="6c426-142">Binary</span></span>|<span data-ttu-id="6c426-143">Blob de hardware del dispositivo Windows Autopilot.</span><span class="sxs-lookup"><span data-stu-id="6c426-143">Hardware Blob of the Windows autopilot device.</span></span>|
|<span data-ttu-id="6c426-144">estado</span><span class="sxs-lookup"><span data-stu-id="6c426-144">state</span></span>|[<span data-ttu-id="6c426-145">importedWindowsAutopilotDeviceIdentityState</span><span class="sxs-lookup"><span data-stu-id="6c426-145">importedWindowsAutopilotDeviceIdentityState</span></span>](../resources/intune_enrollment_importedwindowsautopilotdeviceidentitystate.md)|<span data-ttu-id="6c426-146">Estado actual del dispositivo importado.</span><span class="sxs-lookup"><span data-stu-id="6c426-146">Current state of the imported device.</span></span>|



## <a name="response"></a><span data-ttu-id="6c426-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c426-147">Response</span></span>
<span data-ttu-id="6c426-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6c426-148">If successful, this method returns a `200 OK` response code and an updated [importedWindowsAutopilotDeviceIdentity](../resources/intune_enrollment_importedwindowsautopilotdeviceidentity.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6c426-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6c426-149">Example</span></span>
### <a name="request"></a><span data-ttu-id="6c426-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6c426-150">Request</span></span>
<span data-ttu-id="6c426-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6c426-151">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentities/{importedWindowsAutopilotDeviceIdentityId}
Content-type: application/json
Content-length: 464

{
  "orderIdentifier": "Order Identifier value",
  "serialNumber": "Serial Number value",
  "productKey": "Product Key value",
  "hardwareIdentifier": "aGFyZHdhcmVJZGVudGlmaWVy",
  "state": {
    "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentityState",
    "deviceImportStatus": "pending",
    "deviceRegistrationId": "Device Registration Id value",
    "deviceErrorCode": 15,
    "deviceErrorName": "Device Error Name value"
  }
}
```

### <a name="response"></a><span data-ttu-id="6c426-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6c426-152">Response</span></span>
<span data-ttu-id="6c426-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6c426-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 590

{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentity",
  "id": "985b4f49-4f49-985b-494f-5b98494f5b98",
  "orderIdentifier": "Order Identifier value",
  "serialNumber": "Serial Number value",
  "productKey": "Product Key value",
  "hardwareIdentifier": "aGFyZHdhcmVJZGVudGlmaWVy",
  "state": {
    "@odata.type": "microsoft.graph.importedWindowsAutopilotDeviceIdentityState",
    "deviceImportStatus": "pending",
    "deviceRegistrationId": "Device Registration Id value",
    "deviceErrorCode": 15,
    "deviceErrorName": "Device Error Name value"
  }
}
```








