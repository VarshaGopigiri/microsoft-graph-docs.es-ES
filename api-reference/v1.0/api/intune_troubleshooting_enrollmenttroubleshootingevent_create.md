# <a name="create-enrollmenttroubleshootingevent"></a><span data-ttu-id="0fa9a-101">Crear enrollmentTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="0fa9a-101">Create enrollmentTroubleshootingEvent</span></span>

> <span data-ttu-id="0fa9a-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0fa9a-103">Cree un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="0fa9a-103">Create a new [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0fa9a-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0fa9a-104">Prerequisites</span></span>
<span data-ttu-id="0fa9a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="0fa9a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="0fa9a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0fa9a-107">Permission type</span></span>|<span data-ttu-id="0fa9a-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0fa9a-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0fa9a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0fa9a-109">Delegated (work or school account)</span></span>|<span data-ttu-id="0fa9a-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0fa9a-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="0fa9a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0fa9a-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0fa9a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-112">Not supported.</span></span>|
|<span data-ttu-id="0fa9a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0fa9a-113">Application</span></span>|<span data-ttu-id="0fa9a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0fa9a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0fa9a-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/troubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="0fa9a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0fa9a-116">Request headers</span></span>
|<span data-ttu-id="0fa9a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0fa9a-117">Header</span></span>|<span data-ttu-id="0fa9a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0fa9a-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0fa9a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="0fa9a-119">Authorization</span></span>|<span data-ttu-id="0fa9a-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0fa9a-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0fa9a-121">Accept</span></span>|<span data-ttu-id="0fa9a-122">application/json</span><span class="sxs-lookup"><span data-stu-id="0fa9a-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0fa9a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0fa9a-123">Request body</span></span>
<span data-ttu-id="0fa9a-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto enrollmentTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-124">In the request body, supply a JSON representation for the enrollmentTroubleshootingEvent object.</span></span>

<span data-ttu-id="0fa9a-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto enrollmentTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-125">The following table shows the properties that are required when you create the enrollmentTroubleshootingEvent.</span></span>

|<span data-ttu-id="0fa9a-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0fa9a-126">Property</span></span>|<span data-ttu-id="0fa9a-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="0fa9a-127">Type</span></span>|<span data-ttu-id="0fa9a-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="0fa9a-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0fa9a-129">id</span><span class="sxs-lookup"><span data-stu-id="0fa9a-129">id</span></span>|<span data-ttu-id="0fa9a-130">String</span><span class="sxs-lookup"><span data-stu-id="0fa9a-130">String</span></span>|<span data-ttu-id="0fa9a-131">UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="0fa9a-131">UUID for the object Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="0fa9a-132">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="0fa9a-132">eventDateTime</span></span>|<span data-ttu-id="0fa9a-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0fa9a-133">DateTimeOffset</span></span>|<span data-ttu-id="0fa9a-134">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-134">Time when the event occurred .</span></span> <span data-ttu-id="0fa9a-135">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="0fa9a-135">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="0fa9a-136">correlationId</span><span class="sxs-lookup"><span data-stu-id="0fa9a-136">correlationId</span></span>|<span data-ttu-id="0fa9a-137">String</span><span class="sxs-lookup"><span data-stu-id="0fa9a-137">String</span></span>|<span data-ttu-id="0fa9a-138">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-138">Id used for tracing the failure in the service.</span></span> <span data-ttu-id="0fa9a-139">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="0fa9a-139">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="0fa9a-140">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="0fa9a-140">managedDeviceIdentifier</span></span>|<span data-ttu-id="0fa9a-141">String</span><span class="sxs-lookup"><span data-stu-id="0fa9a-141">String</span></span>|<span data-ttu-id="0fa9a-142">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-142">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="0fa9a-143">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="0fa9a-143">operatingSystem</span></span>|<span data-ttu-id="0fa9a-144">String</span><span class="sxs-lookup"><span data-stu-id="0fa9a-144">String</span></span>|<span data-ttu-id="0fa9a-145">Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-145">Operating System.</span></span>|
|<span data-ttu-id="0fa9a-146">osVersion</span><span class="sxs-lookup"><span data-stu-id="0fa9a-146">osVersion</span></span>|<span data-ttu-id="0fa9a-147">String</span><span class="sxs-lookup"><span data-stu-id="0fa9a-147">String</span></span>|<span data-ttu-id="0fa9a-148">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-148">OS Version.</span></span>|
|<span data-ttu-id="0fa9a-149">userId</span><span class="sxs-lookup"><span data-stu-id="0fa9a-149">userId</span></span>|<span data-ttu-id="0fa9a-150">String</span><span class="sxs-lookup"><span data-stu-id="0fa9a-150">String</span></span>|<span data-ttu-id="0fa9a-151">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-151">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="0fa9a-152">deviceId</span><span class="sxs-lookup"><span data-stu-id="0fa9a-152">deviceId</span></span>|<span data-ttu-id="0fa9a-153">String</span><span class="sxs-lookup"><span data-stu-id="0fa9a-153">String</span></span>|<span data-ttu-id="0fa9a-154">Identificador de dispositivo de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-154">Azure AD device identifier.</span></span>|
|<span data-ttu-id="0fa9a-155">enrollmentType</span><span class="sxs-lookup"><span data-stu-id="0fa9a-155">enrollmentType</span></span>|[<span data-ttu-id="0fa9a-156">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="0fa9a-156">deviceEnrollmentType</span></span>](../resources/intune_shared_deviceenrollmenttype.md)|<span data-ttu-id="0fa9a-157">Tipo de la inscripción.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-157">Type of the enrollment.</span></span> <span data-ttu-id="0fa9a-158">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-158">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="0fa9a-159">failureCategory</span><span class="sxs-lookup"><span data-stu-id="0fa9a-159">failureCategory</span></span>|[<span data-ttu-id="0fa9a-160">deviceEnrollmentFailureReason</span><span class="sxs-lookup"><span data-stu-id="0fa9a-160">deviceEnrollmentFailureReason</span></span>](../resources/intune_troubleshooting_deviceenrollmentfailurereason.md)|<span data-ttu-id="0fa9a-161">Categoría general del error.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-161">Highlevel failure category.</span></span> <span data-ttu-id="0fa9a-162">Los valores posibles son: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected` y `userAbandonment`.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-162">Possible values are: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected`, `userAbandonment`.</span></span>|
|<span data-ttu-id="0fa9a-163">failureReason</span><span class="sxs-lookup"><span data-stu-id="0fa9a-163">failureReason</span></span>|<span data-ttu-id="0fa9a-164">String</span><span class="sxs-lookup"><span data-stu-id="0fa9a-164">String</span></span>|<span data-ttu-id="0fa9a-165">Motivo del error detallado.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-165">Detailed failure reason.</span></span>|



## <a name="response"></a><span data-ttu-id="0fa9a-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0fa9a-166">Response</span></span>
<span data-ttu-id="0fa9a-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-167">If successful, this method returns a `201 Created` response code and a [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0fa9a-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0fa9a-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="0fa9a-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0fa9a-169">Request</span></span>
<span data-ttu-id="0fa9a-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-170">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/troubleshootingEvents
Content-type: application/json
Content-length: 509

{
  "@odata.type": "#microsoft.graph.enrollmentTroubleshootingEvent",
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value",
  "managedDeviceIdentifier": "Managed Device Identifier value",
  "operatingSystem": "Operating System value",
  "osVersion": "Os Version value",
  "userId": "User Id value",
  "deviceId": "Device Id value",
  "enrollmentType": "userEnrollment",
  "failureCategory": "authentication",
  "failureReason": "Failure Reason value"
}
```

### <a name="response"></a><span data-ttu-id="0fa9a-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0fa9a-171">Response</span></span>
<span data-ttu-id="0fa9a-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0fa9a-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 558

{
  "@odata.type": "#microsoft.graph.enrollmentTroubleshootingEvent",
  "id": "c4a623f5-23f5-c4a6-f523-a6c4f523a6c4",
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value",
  "managedDeviceIdentifier": "Managed Device Identifier value",
  "operatingSystem": "Operating System value",
  "osVersion": "Os Version value",
  "userId": "User Id value",
  "deviceId": "Device Id value",
  "enrollmentType": "userEnrollment",
  "failureCategory": "authentication",
  "failureReason": "Failure Reason value"
}
```



