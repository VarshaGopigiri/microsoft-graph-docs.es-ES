# <a name="update-enrollmenttroubleshootingevent"></a><span data-ttu-id="fc567-101">Actualizar enrollmentTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="fc567-101">Update enrollmentTroubleshootingEvent</span></span>

> <span data-ttu-id="fc567-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fc567-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fc567-103">Actualice las propiedades de un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="fc567-103">Update the properties of a [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fc567-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fc567-104">Prerequisites</span></span>
<span data-ttu-id="fc567-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fc567-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fc567-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fc567-107">Permission type</span></span>|<span data-ttu-id="fc567-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fc567-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fc567-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fc567-109">Delegated (work or school account)</span></span>|<span data-ttu-id="fc567-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fc567-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="fc567-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fc567-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fc567-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc567-112">Not supported.</span></span>|
|<span data-ttu-id="fc567-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fc567-113">Application</span></span>|<span data-ttu-id="fc567-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fc567-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fc567-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fc567-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

## <a name="request-headers"></a><span data-ttu-id="fc567-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fc567-116">Request headers</span></span>
|<span data-ttu-id="fc567-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fc567-117">Header</span></span>|<span data-ttu-id="fc567-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fc567-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fc567-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="fc567-119">Authorization</span></span>|<span data-ttu-id="fc567-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fc567-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="fc567-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fc567-121">Accept</span></span>|<span data-ttu-id="fc567-122">application/json</span><span class="sxs-lookup"><span data-stu-id="fc567-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fc567-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fc567-123">Request body</span></span>
<span data-ttu-id="fc567-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="fc567-124">In the request body, supply a JSON representation for the [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object.</span></span>

<span data-ttu-id="fc567-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="fc567-125">The following table shows the properties that are required when you create the [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span></span>

|<span data-ttu-id="fc567-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fc567-126">Property</span></span>|<span data-ttu-id="fc567-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="fc567-127">Type</span></span>|<span data-ttu-id="fc567-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="fc567-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fc567-129">id</span><span class="sxs-lookup"><span data-stu-id="fc567-129">id</span></span>|<span data-ttu-id="fc567-130">String</span><span class="sxs-lookup"><span data-stu-id="fc567-130">String</span></span>|<span data-ttu-id="fc567-131">UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="fc567-131">UUID for the object Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="fc567-132">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="fc567-132">eventDateTime</span></span>|<span data-ttu-id="fc567-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="fc567-133">DateTimeOffset</span></span>|<span data-ttu-id="fc567-134">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="fc567-134">Time when the event occurred .</span></span> <span data-ttu-id="fc567-135">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="fc567-135">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="fc567-136">correlationId</span><span class="sxs-lookup"><span data-stu-id="fc567-136">correlationId</span></span>|<span data-ttu-id="fc567-137">String</span><span class="sxs-lookup"><span data-stu-id="fc567-137">String</span></span>|<span data-ttu-id="fc567-138">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="fc567-138">Id used for tracing the failure in the service.</span></span> <span data-ttu-id="fc567-139">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="fc567-139">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="fc567-140">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="fc567-140">managedDeviceIdentifier</span></span>|<span data-ttu-id="fc567-141">String</span><span class="sxs-lookup"><span data-stu-id="fc567-141">String</span></span>|<span data-ttu-id="fc567-142">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="fc567-142">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="fc567-143">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="fc567-143">operatingSystem</span></span>|<span data-ttu-id="fc567-144">String</span><span class="sxs-lookup"><span data-stu-id="fc567-144">String</span></span>|<span data-ttu-id="fc567-145">Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fc567-145">Operating System.</span></span>|
|<span data-ttu-id="fc567-146">osVersion</span><span class="sxs-lookup"><span data-stu-id="fc567-146">osVersion</span></span>|<span data-ttu-id="fc567-147">String</span><span class="sxs-lookup"><span data-stu-id="fc567-147">String</span></span>|<span data-ttu-id="fc567-148">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="fc567-148">OS Version.</span></span>|
|<span data-ttu-id="fc567-149">userId</span><span class="sxs-lookup"><span data-stu-id="fc567-149">userId</span></span>|<span data-ttu-id="fc567-150">String</span><span class="sxs-lookup"><span data-stu-id="fc567-150">String</span></span>|<span data-ttu-id="fc567-151">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc567-151">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="fc567-152">deviceId</span><span class="sxs-lookup"><span data-stu-id="fc567-152">deviceId</span></span>|<span data-ttu-id="fc567-153">String</span><span class="sxs-lookup"><span data-stu-id="fc567-153">String</span></span>|<span data-ttu-id="fc567-154">Identificador de dispositivo de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="fc567-154">Azure AD device identifier.</span></span>|
|<span data-ttu-id="fc567-155">enrollmentType</span><span class="sxs-lookup"><span data-stu-id="fc567-155">enrollmentType</span></span>|[<span data-ttu-id="fc567-156">deviceEnrollmentType</span><span class="sxs-lookup"><span data-stu-id="fc567-156">deviceEnrollmentType</span></span>](../resources/intune_shared_deviceenrollmenttype.md)|<span data-ttu-id="fc567-157">Tipo de la inscripción.</span><span class="sxs-lookup"><span data-stu-id="fc567-157">Type of the enrollment.</span></span> <span data-ttu-id="fc567-158">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="fc567-158">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="fc567-159">failureCategory</span><span class="sxs-lookup"><span data-stu-id="fc567-159">failureCategory</span></span>|[<span data-ttu-id="fc567-160">deviceEnrollmentFailureReason</span><span class="sxs-lookup"><span data-stu-id="fc567-160">deviceEnrollmentFailureReason</span></span>](../resources/intune_troubleshooting_deviceenrollmentfailurereason.md)|<span data-ttu-id="fc567-161">Categoría general del error.</span><span class="sxs-lookup"><span data-stu-id="fc567-161">Highlevel failure category.</span></span> <span data-ttu-id="fc567-162">Los valores posibles son: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected` y `userAbandonment`.</span><span class="sxs-lookup"><span data-stu-id="fc567-162">Possible values are: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected`, `userAbandonment`.</span></span>|
|<span data-ttu-id="fc567-163">failureReason</span><span class="sxs-lookup"><span data-stu-id="fc567-163">failureReason</span></span>|<span data-ttu-id="fc567-164">String</span><span class="sxs-lookup"><span data-stu-id="fc567-164">String</span></span>|<span data-ttu-id="fc567-165">Motivo del error detallado.</span><span class="sxs-lookup"><span data-stu-id="fc567-165">Detailed failure reason.</span></span>|



## <a name="response"></a><span data-ttu-id="fc567-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc567-166">Response</span></span>
<span data-ttu-id="fc567-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fc567-167">If successful, this method returns a `200 OK` response code and an updated [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fc567-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fc567-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="fc567-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fc567-169">Request</span></span>
<span data-ttu-id="fc567-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fc567-170">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
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

### <a name="response"></a><span data-ttu-id="fc567-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fc567-171">Response</span></span>
<span data-ttu-id="fc567-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fc567-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



