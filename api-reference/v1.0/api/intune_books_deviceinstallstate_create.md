# <a name="create-deviceinstallstate"></a><span data-ttu-id="61450-101">Crear deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="61450-101">Create deviceInstallState</span></span>

> <span data-ttu-id="61450-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="61450-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="61450-103">Cree un objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="61450-103">Create a new [deviceInstallState](../resources/intune_books_deviceinstallstate.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="61450-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="61450-104">Prerequisites</span></span>
<span data-ttu-id="61450-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="61450-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="61450-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="61450-107">Permission type</span></span>|<span data-ttu-id="61450-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="61450-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="61450-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="61450-109">Delegated (work or school account)</span></span>|<span data-ttu-id="61450-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="61450-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="61450-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="61450-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="61450-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="61450-112">Not supported.</span></span>|
|<span data-ttu-id="61450-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="61450-113">Application</span></span>|<span data-ttu-id="61450-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="61450-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="61450-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="61450-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
POST /deviceAppManagement/managedEBooks/{managedEBookId}/userStateSummary/{userInstallStateSummaryId}/deviceStates
```

## <a name="request-headers"></a><span data-ttu-id="61450-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="61450-116">Request headers</span></span>
|<span data-ttu-id="61450-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61450-117">Header</span></span>|<span data-ttu-id="61450-118">Valor</span><span class="sxs-lookup"><span data-stu-id="61450-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="61450-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="61450-119">Authorization</span></span>|<span data-ttu-id="61450-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="61450-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="61450-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="61450-121">Accept</span></span>|<span data-ttu-id="61450-122">application/json</span><span class="sxs-lookup"><span data-stu-id="61450-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="61450-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="61450-123">Request body</span></span>
<span data-ttu-id="61450-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceInstallState.</span><span class="sxs-lookup"><span data-stu-id="61450-124">In the request body, supply a JSON representation for the deviceInstallState object.</span></span>

<span data-ttu-id="61450-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceInstallState.</span><span class="sxs-lookup"><span data-stu-id="61450-125">The following table shows the properties that are required when you create the deviceInstallState.</span></span>

|<span data-ttu-id="61450-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="61450-126">Property</span></span>|<span data-ttu-id="61450-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="61450-127">Type</span></span>|<span data-ttu-id="61450-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="61450-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="61450-129">id</span><span class="sxs-lookup"><span data-stu-id="61450-129">id</span></span>|<span data-ttu-id="61450-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="61450-130">String</span></span>|<span data-ttu-id="61450-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="61450-131">Key of the entity.</span></span>|
|<span data-ttu-id="61450-132">deviceName</span><span class="sxs-lookup"><span data-stu-id="61450-132">deviceName</span></span>|<span data-ttu-id="61450-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="61450-133">String</span></span>|<span data-ttu-id="61450-134">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61450-134">Device name.</span></span>|
|<span data-ttu-id="61450-135">deviceId</span><span class="sxs-lookup"><span data-stu-id="61450-135">deviceId</span></span>|<span data-ttu-id="61450-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="61450-136">String</span></span>|<span data-ttu-id="61450-137">Id. del dispositivo</span><span class="sxs-lookup"><span data-stu-id="61450-137">Device Id.</span></span>|
|<span data-ttu-id="61450-138">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="61450-138">lastSyncDateTime</span></span>|<span data-ttu-id="61450-139">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="61450-139">DateTimeOffset</span></span>|<span data-ttu-id="61450-140">Fecha y hora de la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="61450-140">Last sync date and time.</span></span>|
|<span data-ttu-id="61450-141">installState</span><span class="sxs-lookup"><span data-stu-id="61450-141">installState</span></span>|[<span data-ttu-id="61450-142">installState</span><span class="sxs-lookup"><span data-stu-id="61450-142">installState</span></span>](../resources/intune_books_installstate.md)|<span data-ttu-id="61450-p102">El estado de instalación del libro electrónico. Los valores posibles son: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="61450-p102">The install state of the eBook. The possible values are: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed`, `unknown`.</span></span>|
|<span data-ttu-id="61450-145">errorCode</span><span class="sxs-lookup"><span data-stu-id="61450-145">errorCode</span></span>|<span data-ttu-id="61450-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="61450-146">String</span></span>|<span data-ttu-id="61450-147">El código de error si hay errores de instalación.</span><span class="sxs-lookup"><span data-stu-id="61450-147">The error code for install failures.</span></span>|
|<span data-ttu-id="61450-148">osVersion</span><span class="sxs-lookup"><span data-stu-id="61450-148">osVersion</span></span>|<span data-ttu-id="61450-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="61450-149">String</span></span>|<span data-ttu-id="61450-150">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="61450-150">OS Version.</span></span>|
|<span data-ttu-id="61450-151">osDescription</span><span class="sxs-lookup"><span data-stu-id="61450-151">osDescription</span></span>|<span data-ttu-id="61450-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="61450-152">String</span></span>|<span data-ttu-id="61450-153">Descripción del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="61450-153">OS Description.</span></span>|
|<span data-ttu-id="61450-154">userName</span><span class="sxs-lookup"><span data-stu-id="61450-154">userName</span></span>|<span data-ttu-id="61450-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="61450-155">String</span></span>|<span data-ttu-id="61450-156">Nombre de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="61450-156">Device User Name.</span></span>|



## <a name="response"></a><span data-ttu-id="61450-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61450-157">Response</span></span>
<span data-ttu-id="61450-158">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceInstallState](../resources/intune_books_deviceinstallstate.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="61450-158">If successful, this method returns a `201 Created` response code and a [deviceInstallState](../resources/intune_books_deviceinstallstate.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="61450-159">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="61450-159">Example</span></span>
### <a name="request"></a><span data-ttu-id="61450-160">Solicitud</span><span class="sxs-lookup"><span data-stu-id="61450-160">Request</span></span>
<span data-ttu-id="61450-161">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="61450-161">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/managedEBooks/{managedEBookId}/deviceStates
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

### <a name="response"></a><span data-ttu-id="61450-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="61450-162">Response</span></span>
<span data-ttu-id="61450-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="61450-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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








