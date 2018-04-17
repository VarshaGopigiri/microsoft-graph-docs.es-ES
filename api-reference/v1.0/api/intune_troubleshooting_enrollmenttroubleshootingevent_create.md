# <a name="create-enrollmenttroubleshootingevent"></a><span data-ttu-id="86ae3-101">Crear enrollmentTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="86ae3-101">Create enrollmentTroubleshootingEvent</span></span>

> <span data-ttu-id="86ae3-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="86ae3-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="86ae3-103">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="86ae3-103">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="86ae3-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="86ae3-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="86ae3-105">Cree un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="86ae3-105">Create a new [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="86ae3-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="86ae3-106">Prerequisites</span></span>
<span data-ttu-id="86ae3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="86ae3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="86ae3-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="86ae3-109">Permission type</span></span>|<span data-ttu-id="86ae3-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="86ae3-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="86ae3-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="86ae3-111">Delegated (work or school account)</span></span>|<span data-ttu-id="86ae3-112">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="86ae3-112">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="86ae3-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="86ae3-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="86ae3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="86ae3-114">Not supported.</span></span>|
|<span data-ttu-id="86ae3-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="86ae3-115">Application</span></span>|<span data-ttu-id="86ae3-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="86ae3-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="86ae3-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="86ae3-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/troubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="86ae3-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="86ae3-118">Request headers</span></span>
|<span data-ttu-id="86ae3-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86ae3-119">Header</span></span>|<span data-ttu-id="86ae3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="86ae3-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="86ae3-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="86ae3-121">Authorization</span></span>|<span data-ttu-id="86ae3-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="86ae3-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="86ae3-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="86ae3-123">Accept</span></span>|<span data-ttu-id="86ae3-124">application/json</span><span class="sxs-lookup"><span data-stu-id="86ae3-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="86ae3-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="86ae3-125">Request body</span></span>
<span data-ttu-id="86ae3-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto enrollmentTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="86ae3-126">In the request body, supply a JSON representation for the enrollmentTroubleshootingEvent object.</span></span>

<span data-ttu-id="86ae3-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto enrollmentTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="86ae3-127">The following table shows the properties that are required when you create the enrollmentTroubleshootingEvent.</span></span>

|<span data-ttu-id="86ae3-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="86ae3-128">Property</span></span>|<span data-ttu-id="86ae3-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="86ae3-129">Type</span></span>|<span data-ttu-id="86ae3-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="86ae3-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="86ae3-131">id</span><span class="sxs-lookup"><span data-stu-id="86ae3-131">id</span></span>|<span data-ttu-id="86ae3-132">String</span><span class="sxs-lookup"><span data-stu-id="86ae3-132">String</span></span>|<span data-ttu-id="86ae3-133">UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="86ae3-133">UUID for the object Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="86ae3-134">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="86ae3-134">eventDateTime</span></span>|<span data-ttu-id="86ae3-135">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="86ae3-135">DateTimeOffset</span></span>|<span data-ttu-id="86ae3-136">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="86ae3-136">Time when the event occurred .</span></span> <span data-ttu-id="86ae3-137">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="86ae3-137">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="86ae3-138">correlationId</span><span class="sxs-lookup"><span data-stu-id="86ae3-138">correlationId</span></span>|<span data-ttu-id="86ae3-139">String</span><span class="sxs-lookup"><span data-stu-id="86ae3-139">String</span></span>|<span data-ttu-id="86ae3-140">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="86ae3-140">Id used for tracing the failure in the service.</span></span> <span data-ttu-id="86ae3-141">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="86ae3-141">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="86ae3-142">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="86ae3-142">managedDeviceIdentifier</span></span>|<span data-ttu-id="86ae3-143">String</span><span class="sxs-lookup"><span data-stu-id="86ae3-143">String</span></span>|<span data-ttu-id="86ae3-144">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="86ae3-144">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="86ae3-145">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="86ae3-145">operatingSystem</span></span>|<span data-ttu-id="86ae3-146">String</span><span class="sxs-lookup"><span data-stu-id="86ae3-146">String</span></span>|<span data-ttu-id="86ae3-147">Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="86ae3-147">Operating System.</span></span>|
|<span data-ttu-id="86ae3-148">osVersion</span><span class="sxs-lookup"><span data-stu-id="86ae3-148">osVersion</span></span>|<span data-ttu-id="86ae3-149">String</span><span class="sxs-lookup"><span data-stu-id="86ae3-149">String</span></span>|<span data-ttu-id="86ae3-150">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="86ae3-150">OS Version.</span></span>|
|<span data-ttu-id="86ae3-151">userId</span><span class="sxs-lookup"><span data-stu-id="86ae3-151">userId</span></span>|<span data-ttu-id="86ae3-152">String</span><span class="sxs-lookup"><span data-stu-id="86ae3-152">String</span></span>|<span data-ttu-id="86ae3-153">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="86ae3-153">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="86ae3-154">deviceId</span><span class="sxs-lookup"><span data-stu-id="86ae3-154">deviceId</span></span>|<span data-ttu-id="86ae3-155">String</span><span class="sxs-lookup"><span data-stu-id="86ae3-155">String</span></span>|<span data-ttu-id="86ae3-156">Identificador de dispositivo de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="86ae3-156">Azure AD device identifier.</span></span>|
|<span data-ttu-id="86ae3-157">enrollmentType</span><span class="sxs-lookup"><span data-stu-id="86ae3-157">enrollmentType</span></span>|<span data-ttu-id="86ae3-158">String</span><span class="sxs-lookup"><span data-stu-id="86ae3-158">String</span></span>|<span data-ttu-id="86ae3-159">Tipo de la inscripción.</span><span class="sxs-lookup"><span data-stu-id="86ae3-159">Type of the enrollment.</span></span> <span data-ttu-id="86ae3-160">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="86ae3-160">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="86ae3-161">failureCategory</span><span class="sxs-lookup"><span data-stu-id="86ae3-161">failureCategory</span></span>|<span data-ttu-id="86ae3-162">String</span><span class="sxs-lookup"><span data-stu-id="86ae3-162">String</span></span>|<span data-ttu-id="86ae3-163">Categoría general del error.</span><span class="sxs-lookup"><span data-stu-id="86ae3-163">Highlevel failure category.</span></span> <span data-ttu-id="86ae3-164">Los valores posibles son: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced` y `clientDisconnected`.</span><span class="sxs-lookup"><span data-stu-id="86ae3-164">Possible values are: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected`.</span></span>|
|<span data-ttu-id="86ae3-165">failureReason</span><span class="sxs-lookup"><span data-stu-id="86ae3-165">failureReason</span></span>|<span data-ttu-id="86ae3-166">String</span><span class="sxs-lookup"><span data-stu-id="86ae3-166">String</span></span>|<span data-ttu-id="86ae3-167">Motivo del error detallado.</span><span class="sxs-lookup"><span data-stu-id="86ae3-167">Detailed failure reason.</span></span>|



## <a name="response"></a><span data-ttu-id="86ae3-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86ae3-168">Response</span></span>
<span data-ttu-id="86ae3-169">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="86ae3-169">If successful, this method returns a `201 Created` response code and a [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="86ae3-170">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="86ae3-170">Example</span></span>
### <a name="request"></a><span data-ttu-id="86ae3-171">Solicitud</span><span class="sxs-lookup"><span data-stu-id="86ae3-171">Request</span></span>
<span data-ttu-id="86ae3-172">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="86ae3-172">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/troubleshootingEvents
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

### <a name="response"></a><span data-ttu-id="86ae3-173">Respuesta</span><span class="sxs-lookup"><span data-stu-id="86ae3-173">Response</span></span>
<span data-ttu-id="86ae3-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="86ae3-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



