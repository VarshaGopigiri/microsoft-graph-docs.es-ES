# <a name="create-importedwindowsautopilotdeviceidentityupload"></a><span data-ttu-id="f6790-101">Crear importedWindowsAutopilotDeviceIdentityUpload</span><span class="sxs-lookup"><span data-stu-id="f6790-101">Create importedWindowsAutopilotDeviceIdentityUpload</span></span>

> <span data-ttu-id="f6790-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f6790-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f6790-103">Crear un nuevo objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune_enrollment_importedwindowsautopilotdeviceidentityupload.md) .</span><span class="sxs-lookup"><span data-stu-id="f6790-103">Create a new [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune_enrollment_importedwindowsautopilotdeviceidentityupload.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f6790-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f6790-104">Prerequisites</span></span>
<span data-ttu-id="f6790-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f6790-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f6790-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f6790-107">Permission type</span></span>|<span data-ttu-id="f6790-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f6790-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f6790-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f6790-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f6790-110">DeviceManagementServiceConfig.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f6790-110">DeviceManagementServiceConfig.ReadWrite.All</span></span>|
|<span data-ttu-id="f6790-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f6790-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f6790-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6790-112">Not supported.</span></span>|
|<span data-ttu-id="f6790-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f6790-113">Application</span></span>|<span data-ttu-id="f6790-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6790-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f6790-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f6790-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
```

## <a name="request-headers"></a><span data-ttu-id="f6790-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f6790-116">Request headers</span></span>
|<span data-ttu-id="f6790-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6790-117">Header</span></span>|<span data-ttu-id="f6790-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f6790-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f6790-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f6790-119">Authorization</span></span>|<span data-ttu-id="f6790-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f6790-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f6790-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f6790-121">Accept</span></span>|<span data-ttu-id="f6790-122">application/json</span><span class="sxs-lookup"><span data-stu-id="f6790-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f6790-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f6790-123">Request body</span></span>
<span data-ttu-id="f6790-124">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto importedWindowsAutopilotDeviceIdentityUpload.</span><span class="sxs-lookup"><span data-stu-id="f6790-124">In the request body, supply a JSON representation for the importedWindowsAutopilotDeviceIdentityUpload object.</span></span>

<span data-ttu-id="f6790-125">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el importedWindowsAutopilotDeviceIdentityUpload.</span><span class="sxs-lookup"><span data-stu-id="f6790-125">The following table shows the properties that are required when you create the importedWindowsAutopilotDeviceIdentityUpload.</span></span>

|<span data-ttu-id="f6790-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f6790-126">Property</span></span>|<span data-ttu-id="f6790-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6790-127">Type</span></span>|<span data-ttu-id="f6790-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6790-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f6790-129">id</span><span class="sxs-lookup"><span data-stu-id="f6790-129">id</span></span>|<span data-ttu-id="f6790-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="f6790-130">String</span></span>|<span data-ttu-id="f6790-131">El GUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="f6790-131">The GUID for the object</span></span>|
|<span data-ttu-id="f6790-132">createdDateTimeUtc</span><span class="sxs-lookup"><span data-stu-id="f6790-132">createdDateTimeUtc</span></span>|<span data-ttu-id="f6790-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f6790-133">DateTimeOffset</span></span>|<span data-ttu-id="f6790-134">Fecha y hora cuando se crea la entidad.</span><span class="sxs-lookup"><span data-stu-id="f6790-134">DateTime when the entity is created.</span></span>|
|<span data-ttu-id="f6790-135">status</span><span class="sxs-lookup"><span data-stu-id="f6790-135">status</span></span>|[<span data-ttu-id="f6790-136">importedWindowsAutopilotDeviceIdentityUploadStatus</span><span class="sxs-lookup"><span data-stu-id="f6790-136">importedWindowsAutopilotDeviceIdentityUploadStatus</span></span>](../resources/intune_enrollment_importedwindowsautopilotdeviceidentityuploadstatus.md)|<span data-ttu-id="f6790-137">Estado de la carga.</span><span class="sxs-lookup"><span data-stu-id="f6790-137">Upload status.</span></span> <span data-ttu-id="f6790-138">Los valores posibles son: `noUpload`, `pending`, `complete` y `error`.</span><span class="sxs-lookup"><span data-stu-id="f6790-138">Possible values are: `noUpload`, `pending`, `complete`, `error`.</span></span>|



## <a name="response"></a><span data-ttu-id="f6790-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6790-139">Response</span></span>
<span data-ttu-id="f6790-140">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune_enrollment_importedwindowsautopilotdeviceidentityupload.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6790-140">If successful, this method returns a `201 Created` response code and a [importedWindowsAutopilotDeviceIdentityUpload](../resources/intune_enrollment_importedwindowsautopilotdeviceidentityupload.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f6790-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6790-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="f6790-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f6790-142">Request</span></span>
<span data-ttu-id="f6790-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f6790-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/importedWindowsAutopilotDeviceIdentityUploads
Content-type: application/json
Content-length: 172

{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityUpload",
  "createdDateTimeUtc": "2016-12-31T23:59:45.8788427-08:00",
  "status": "pending"
}
```

### <a name="response"></a><span data-ttu-id="f6790-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6790-144">Response</span></span>
<span data-ttu-id="f6790-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f6790-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 221

{
  "@odata.type": "#microsoft.graph.importedWindowsAutopilotDeviceIdentityUpload",
  "id": "8d639524-9524-8d63-2495-638d2495638d",
  "createdDateTimeUtc": "2016-12-31T23:59:45.8788427-08:00",
  "status": "pending"
}
```



