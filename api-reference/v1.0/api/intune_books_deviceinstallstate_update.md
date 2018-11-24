# <a name="update-deviceinstallstate"></a><span data-ttu-id="f4563-101">Actualizar deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="f4563-101">Update deviceInstallState</span></span>

> <span data-ttu-id="f4563-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f4563-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f4563-103">Actualice las propiedades de un objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="f4563-103">Update the properties of a [deviceInstallState](../resources/intune_books_deviceinstallstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f4563-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f4563-104">Prerequisites</span></span>
<span data-ttu-id="f4563-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f4563-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f4563-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f4563-107">Permission type</span></span>|<span data-ttu-id="f4563-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f4563-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f4563-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f4563-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f4563-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f4563-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="f4563-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f4563-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f4563-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4563-112">Not supported.</span></span>|
|<span data-ttu-id="f4563-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f4563-113">Application</span></span>|<span data-ttu-id="f4563-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f4563-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f4563-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f4563-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates/{deviceInstallStateId}
PATCH /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}/deviceStates/{deviceInstallStateId}
```

## <a name="request-headers"></a><span data-ttu-id="f4563-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f4563-116">Request headers</span></span>
|<span data-ttu-id="f4563-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f4563-117">Header</span></span>|<span data-ttu-id="f4563-118">Valor</span><span class="sxs-lookup"><span data-stu-id="f4563-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f4563-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="f4563-119">Authorization</span></span>|<span data-ttu-id="f4563-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f4563-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f4563-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f4563-121">Accept</span></span>|<span data-ttu-id="f4563-122">application/json</span><span class="sxs-lookup"><span data-stu-id="f4563-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f4563-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f4563-123">Request body</span></span>
<span data-ttu-id="f4563-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="f4563-124">In the request body, supply a JSON representation for the [deviceInstallState](../resources/intune_books_deviceinstallstate.md) object.</span></span>

<span data-ttu-id="f4563-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="f4563-125">The following table shows the properties that are required when you create the [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span></span>

|<span data-ttu-id="f4563-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f4563-126">Property</span></span>|<span data-ttu-id="f4563-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4563-127">Type</span></span>|<span data-ttu-id="f4563-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="f4563-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f4563-129">id</span><span class="sxs-lookup"><span data-stu-id="f4563-129">id</span></span>|<span data-ttu-id="f4563-130">String</span><span class="sxs-lookup"><span data-stu-id="f4563-130">String</span></span>|<span data-ttu-id="f4563-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f4563-131">Key of the entity.</span></span>|
|<span data-ttu-id="f4563-132">deviceName</span><span class="sxs-lookup"><span data-stu-id="f4563-132">deviceName</span></span>|<span data-ttu-id="f4563-133">String</span><span class="sxs-lookup"><span data-stu-id="f4563-133">String</span></span>|<span data-ttu-id="f4563-134">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4563-134">Device name.</span></span>|
|<span data-ttu-id="f4563-135">deviceId</span><span class="sxs-lookup"><span data-stu-id="f4563-135">deviceId</span></span>|<span data-ttu-id="f4563-136">String</span><span class="sxs-lookup"><span data-stu-id="f4563-136">String</span></span>|<span data-ttu-id="f4563-137">Id. del dispositivo</span><span class="sxs-lookup"><span data-stu-id="f4563-137">Device Id.</span></span>|
|<span data-ttu-id="f4563-138">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="f4563-138">lastSyncDateTime</span></span>|<span data-ttu-id="f4563-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f4563-139">DateTimeOffset</span></span>|<span data-ttu-id="f4563-140">Fecha y hora de la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="f4563-140">Last sync date and time.</span></span>|
|<span data-ttu-id="f4563-141">installState</span><span class="sxs-lookup"><span data-stu-id="f4563-141">installState</span></span>|[<span data-ttu-id="f4563-142">installState</span><span class="sxs-lookup"><span data-stu-id="f4563-142">installState</span></span>](../resources/intune_books_installstate.md)|<span data-ttu-id="f4563-143">El estado de instalación del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="f4563-143">The install state of the eBook.</span></span> <span data-ttu-id="f4563-144">Los valores posibles son: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="f4563-144">Possible values are: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed`, `unknown`.</span></span>|
|<span data-ttu-id="f4563-145">errorCode</span><span class="sxs-lookup"><span data-stu-id="f4563-145">errorCode</span></span>|<span data-ttu-id="f4563-146">String</span><span class="sxs-lookup"><span data-stu-id="f4563-146">String</span></span>|<span data-ttu-id="f4563-147">El código de error si hay errores de instalación.</span><span class="sxs-lookup"><span data-stu-id="f4563-147">The error code for install failures.</span></span>|
|<span data-ttu-id="f4563-148">osVersion</span><span class="sxs-lookup"><span data-stu-id="f4563-148">osVersion</span></span>|<span data-ttu-id="f4563-149">String</span><span class="sxs-lookup"><span data-stu-id="f4563-149">String</span></span>|<span data-ttu-id="f4563-150">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f4563-150">OS Version.</span></span>|
|<span data-ttu-id="f4563-151">osDescription</span><span class="sxs-lookup"><span data-stu-id="f4563-151">osDescription</span></span>|<span data-ttu-id="f4563-152">String</span><span class="sxs-lookup"><span data-stu-id="f4563-152">String</span></span>|<span data-ttu-id="f4563-153">Descripción del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f4563-153">OS Description.</span></span>|
|<span data-ttu-id="f4563-154">userName</span><span class="sxs-lookup"><span data-stu-id="f4563-154">userName</span></span>|<span data-ttu-id="f4563-155">String</span><span class="sxs-lookup"><span data-stu-id="f4563-155">String</span></span>|<span data-ttu-id="f4563-156">Nombre de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4563-156">Device User Name.</span></span>|



## <a name="response"></a><span data-ttu-id="f4563-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4563-157">Response</span></span>
<span data-ttu-id="f4563-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f4563-158">If successful, this method returns a `200 OK` response code and an updated [deviceInstallState](../resources/intune_books_deviceinstallstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f4563-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f4563-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="f4563-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f4563-160">Request</span></span>
<span data-ttu-id="f4563-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f4563-161">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates/{deviceInstallStateId}
Content-type: application/json
Content-length: 374

{
  "@odata.type": "#microsoft.graph.deviceInstallState",
  "deviceName": "Device Name value",
  "deviceId": "Device Id value",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "installState": "installed",
  "errorCode": "Error Code value",
  "osVersion": "Os Version value",
  "osDescription": "Os Description value",
  "userName": "User Name value"
}
```

### <a name="response"></a><span data-ttu-id="f4563-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f4563-162">Response</span></span>
<span data-ttu-id="f4563-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f4563-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 423

{
  "@odata.type": "#microsoft.graph.deviceInstallState",
  "id": "b9feb68f-b68f-b9fe-8fb6-feb98fb6feb9",
  "deviceName": "Device Name value",
  "deviceId": "Device Id value",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "installState": "installed",
  "errorCode": "Error Code value",
  "osVersion": "Os Version value",
  "osDescription": "Os Description value",
  "userName": "User Name value"
}
```



