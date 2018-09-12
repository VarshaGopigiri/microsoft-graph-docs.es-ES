# <a name="update-enrollmenttroubleshootingevent"></a><span data-ttu-id="8f8a0-101">Actualizar enrollmentTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="8f8a0-101">Update enrollmentTroubleshootingEvent</span></span>

> <span data-ttu-id="8f8a0-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8f8a0-103">Actualice las propiedades de un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="8f8a0-103">Update the properties of a [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8f8a0-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8f8a0-104">Prerequisites</span></span>
<span data-ttu-id="8f8a0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8f8a0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8f8a0-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8f8a0-107">Permission type</span></span>|<span data-ttu-id="8f8a0-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8f8a0-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8f8a0-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8f8a0-109">Delegated (work or school account)</span></span>|<span data-ttu-id="8f8a0-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8f8a0-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="8f8a0-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8f8a0-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8f8a0-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-112">Not supported.</span></span>|
|<span data-ttu-id="8f8a0-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8f8a0-113">Application</span></span>|<span data-ttu-id="8f8a0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8f8a0-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8f8a0-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

## <a name="request-headers"></a><span data-ttu-id="8f8a0-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8f8a0-116">Request headers</span></span>
|<span data-ttu-id="8f8a0-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8f8a0-117">Header</span></span>|<span data-ttu-id="8f8a0-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8f8a0-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8f8a0-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="8f8a0-119">Authorization</span></span>|<span data-ttu-id="8f8a0-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8f8a0-121">Accept</span><span class="sxs-lookup"><span data-stu-id="8f8a0-121">Accept</span></span>|<span data-ttu-id="8f8a0-122">application/json</span><span class="sxs-lookup"><span data-stu-id="8f8a0-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8f8a0-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8f8a0-123">Request body</span></span>
<span data-ttu-id="8f8a0-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="8f8a0-124">In the request body, supply a JSON representation for the [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object.</span></span>

<span data-ttu-id="8f8a0-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="8f8a0-125">The following table shows the properties that are required when you create the [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span></span>

|<span data-ttu-id="8f8a0-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8f8a0-126">Property</span></span>|<span data-ttu-id="8f8a0-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="8f8a0-127">Type</span></span>|<span data-ttu-id="8f8a0-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="8f8a0-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8f8a0-129">id</span><span class="sxs-lookup"><span data-stu-id="8f8a0-129">id</span></span>|<span data-ttu-id="8f8a0-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f8a0-130">String</span></span>|<span data-ttu-id="8f8a0-131">UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="8f8a0-131">UUID for the object Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="8f8a0-132">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="8f8a0-132">eventDateTime</span></span>|<span data-ttu-id="8f8a0-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8f8a0-133">DateTimeOffset</span></span>|<span data-ttu-id="8f8a0-134">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-134">Time when the event occurred .</span></span> <span data-ttu-id="8f8a0-135">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="8f8a0-135">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="8f8a0-136">correlationId</span><span class="sxs-lookup"><span data-stu-id="8f8a0-136">correlationId</span></span>|<span data-ttu-id="8f8a0-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f8a0-137">String</span></span>|<span data-ttu-id="8f8a0-138">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-138">Id used for tracing the failure in the service.</span></span> <span data-ttu-id="8f8a0-139">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="8f8a0-139">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="8f8a0-140">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="8f8a0-140">managedDeviceIdentifier</span></span>|<span data-ttu-id="8f8a0-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f8a0-141">String</span></span>|<span data-ttu-id="8f8a0-142">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-142">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="8f8a0-143">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="8f8a0-143">operatingSystem</span></span>|<span data-ttu-id="8f8a0-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f8a0-144">String</span></span>|<span data-ttu-id="8f8a0-145">Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-145">Operating System.</span></span>|
|<span data-ttu-id="8f8a0-146">osVersion</span><span class="sxs-lookup"><span data-stu-id="8f8a0-146">osVersion</span></span>|<span data-ttu-id="8f8a0-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f8a0-147">String</span></span>|<span data-ttu-id="8f8a0-148">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-148">OS Version.</span></span>|
|<span data-ttu-id="8f8a0-149">userId</span><span class="sxs-lookup"><span data-stu-id="8f8a0-149">userId</span></span>|<span data-ttu-id="8f8a0-150">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f8a0-150">String</span></span>|<span data-ttu-id="8f8a0-151">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-151">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="8f8a0-152">deviceId</span><span class="sxs-lookup"><span data-stu-id="8f8a0-152">deviceId</span></span>|<span data-ttu-id="8f8a0-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f8a0-153">String</span></span>|<span data-ttu-id="8f8a0-154">Identificador de dispositivo de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-154">Azure AD device identifier.</span></span>|
|<span data-ttu-id="8f8a0-155">enrollmentType</span><span class="sxs-lookup"><span data-stu-id="8f8a0-155">enrollmentType</span></span>|[<span data-ttu-id="8f8a0-156">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="8f8a0-156">deviceEnrollmentType</span></span>](../resources/intune_shared_deviceenrollmenttype.md)|<span data-ttu-id="8f8a0-157">Tipo de la inscripción.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-157">Type of the enrollment.</span></span> <span data-ttu-id="8f8a0-158">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-158">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="8f8a0-159">failureCategory</span><span class="sxs-lookup"><span data-stu-id="8f8a0-159">failureCategory</span></span>|[<span data-ttu-id="8f8a0-160">deviceEnrollmentFailureReason</span><span class="sxs-lookup"><span data-stu-id="8f8a0-160">deviceEnrollmentFailureReason values</span></span>](../resources/intune_troubleshooting_deviceenrollmentfailurereason.md)|<span data-ttu-id="8f8a0-161">Categoría general del error.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-161">Highlevel failure category.</span></span> <span data-ttu-id="8f8a0-162">Los valores posibles son: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected` y `userAbandonment`.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-162">Possible values are: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected`, `userAbandonment`.</span></span>|
|<span data-ttu-id="8f8a0-163">failureReason</span><span class="sxs-lookup"><span data-stu-id="8f8a0-163">failureReason</span></span>|<span data-ttu-id="8f8a0-164">Cadena</span><span class="sxs-lookup"><span data-stu-id="8f8a0-164">String</span></span>|<span data-ttu-id="8f8a0-165">Motivo del error detallado.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-165">Detailed failure reason.</span></span>|



## <a name="response"></a><span data-ttu-id="8f8a0-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f8a0-166">Response</span></span>
<span data-ttu-id="8f8a0-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-167">If successful, this method returns a `200 OK` response code and an updated [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8f8a0-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f8a0-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="8f8a0-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8f8a0-169">Request</span></span>
<span data-ttu-id="8f8a0-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1/deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
Content-type: application/json
Content-length: 440

{
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

### <a name="response"></a><span data-ttu-id="8f8a0-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8f8a0-171">Response</span></span>
<span data-ttu-id="8f8a0-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8f8a0-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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




