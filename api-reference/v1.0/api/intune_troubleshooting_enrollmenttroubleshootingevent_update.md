# <a name="update-enrollmenttroubleshootingevent"></a><span data-ttu-id="a516a-101">Actualizar enrollmentTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="a516a-101">Update enrollmentTroubleshootingEvent</span></span>

> <span data-ttu-id="a516a-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a516a-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a516a-103">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a516a-103">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a516a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a516a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a516a-105">Actualice las propiedades de un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="a516a-105">Update the properties of a [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a516a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a516a-106">Prerequisites</span></span>
<span data-ttu-id="a516a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a516a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a516a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a516a-109">Permission type</span></span>|<span data-ttu-id="a516a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a516a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a516a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a516a-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a516a-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a516a-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="a516a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a516a-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a516a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a516a-114">Not supported.</span></span>|
|<span data-ttu-id="a516a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a516a-115">Application</span></span>|<span data-ttu-id="a516a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a516a-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a516a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a516a-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

## <a name="request-headers"></a><span data-ttu-id="a516a-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a516a-118">Request headers</span></span>
|<span data-ttu-id="a516a-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a516a-119">Header</span></span>|<span data-ttu-id="a516a-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a516a-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a516a-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a516a-121">Authorization</span></span>|<span data-ttu-id="a516a-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a516a-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a516a-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a516a-123">Accept</span></span>|<span data-ttu-id="a516a-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a516a-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a516a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a516a-125">Request body</span></span>
<span data-ttu-id="a516a-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="a516a-126">In the request body, supply a JSON representation for the [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object.</span></span>

<span data-ttu-id="a516a-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="a516a-127">The following table shows the properties that are required when you create the [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span></span>

|<span data-ttu-id="a516a-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a516a-128">Property</span></span>|<span data-ttu-id="a516a-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a516a-129">Type</span></span>|<span data-ttu-id="a516a-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a516a-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a516a-131">id</span><span class="sxs-lookup"><span data-stu-id="a516a-131">id</span></span>|<span data-ttu-id="a516a-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="a516a-132">String</span></span>|<span data-ttu-id="a516a-133">UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="a516a-133">UUID for the object Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="a516a-134">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="a516a-134">eventDateTime</span></span>|<span data-ttu-id="a516a-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a516a-135">DateTimeOffset</span></span>|<span data-ttu-id="a516a-136">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="a516a-136">Time when the event occurred .</span></span> <span data-ttu-id="a516a-137">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="a516a-137">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="a516a-138">correlationId</span><span class="sxs-lookup"><span data-stu-id="a516a-138">correlationId</span></span>|<span data-ttu-id="a516a-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="a516a-139">String</span></span>|<span data-ttu-id="a516a-140">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="a516a-140">Id used for tracing the failure in the service.</span></span> <span data-ttu-id="a516a-141">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="a516a-141">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="a516a-142">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="a516a-142">managedDeviceIdentifier</span></span>|<span data-ttu-id="a516a-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="a516a-143">String</span></span>|<span data-ttu-id="a516a-144">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="a516a-144">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="a516a-145">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="a516a-145">operatingSystem</span></span>|<span data-ttu-id="a516a-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="a516a-146">String</span></span>|<span data-ttu-id="a516a-147">Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a516a-147">Operating System.</span></span>|
|<span data-ttu-id="a516a-148">osVersion</span><span class="sxs-lookup"><span data-stu-id="a516a-148">osVersion</span></span>|<span data-ttu-id="a516a-149">Cadena</span><span class="sxs-lookup"><span data-stu-id="a516a-149">String</span></span>|<span data-ttu-id="a516a-150">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a516a-150">OS Version.</span></span>|
|<span data-ttu-id="a516a-151">userId</span><span class="sxs-lookup"><span data-stu-id="a516a-151">userId</span></span>|<span data-ttu-id="a516a-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="a516a-152">String</span></span>|<span data-ttu-id="a516a-153">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a516a-153">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="a516a-154">deviceId</span><span class="sxs-lookup"><span data-stu-id="a516a-154">deviceId</span></span>|<span data-ttu-id="a516a-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="a516a-155">String</span></span>|<span data-ttu-id="a516a-156">Identificador de dispositivo de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a516a-156">Azure AD device identifier.</span></span>|
|<span data-ttu-id="a516a-157">enrollmentType</span><span class="sxs-lookup"><span data-stu-id="a516a-157">enrollmentType</span></span>|[<span data-ttu-id="a516a-158">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="a516a-158">deviceEnrollmentType</span></span>](../resources/intune_shared_deviceenrollmenttype.md)|<span data-ttu-id="a516a-159">Tipo de la inscripción.</span><span class="sxs-lookup"><span data-stu-id="a516a-159">Type of the enrollment.</span></span> <span data-ttu-id="a516a-160">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="a516a-160">The possible values are `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`, , or .</span></span>|
|<span data-ttu-id="a516a-161">failureCategory</span><span class="sxs-lookup"><span data-stu-id="a516a-161">failureCategory</span></span>|[<span data-ttu-id="a516a-162">deviceEnrollmentFailureReason</span><span class="sxs-lookup"><span data-stu-id="a516a-162">deviceEnrollmentFailureReason values</span></span>](../resources/intune_troubleshooting_deviceenrollmentfailurereason.md)|<span data-ttu-id="a516a-163">Categoría de error de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="a516a-163">Highlevel failure category.</span></span> <span data-ttu-id="a516a-164">Los valores posibles son: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced` y `clientDisconnected`.</span><span class="sxs-lookup"><span data-stu-id="a516a-164">The possible values are `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected`, or .</span></span>|
|<span data-ttu-id="a516a-165">failureReason</span><span class="sxs-lookup"><span data-stu-id="a516a-165">failureReason</span></span>|<span data-ttu-id="a516a-166">Cadena</span><span class="sxs-lookup"><span data-stu-id="a516a-166">String</span></span>|<span data-ttu-id="a516a-167">Motivo del error detallado.</span><span class="sxs-lookup"><span data-stu-id="a516a-167">Detailed failure reason.</span></span>|



## <a name="response"></a><span data-ttu-id="a516a-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a516a-168">Response</span></span>
<span data-ttu-id="a516a-169">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a516a-169">If successful, this method returns a `200 OK` response code and an updated [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a516a-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a516a-170">Example</span></span>
### <a name="request"></a><span data-ttu-id="a516a-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a516a-171">Request</span></span>
<span data-ttu-id="a516a-172">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a516a-172">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
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

### <a name="response"></a><span data-ttu-id="a516a-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a516a-173">Response</span></span>
<span data-ttu-id="a516a-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a516a-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



