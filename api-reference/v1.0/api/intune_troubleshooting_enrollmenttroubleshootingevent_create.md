# <a name="create-enrollmenttroubleshootingevent"></a><span data-ttu-id="20128-101">Crear enrollmentTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="20128-101">Create enrollmentTroubleshootingEvent</span></span>

> <span data-ttu-id="20128-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="20128-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="20128-103">Cree un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="20128-103">Create a new [plannerBucket](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="20128-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="20128-104">Prerequisites</span></span>
<span data-ttu-id="20128-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="20128-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="20128-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="20128-107">Permission type</span></span>|<span data-ttu-id="20128-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="20128-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="20128-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="20128-109">Delegated (work or school account)</span></span>|<span data-ttu-id="20128-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="20128-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="20128-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="20128-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="20128-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="20128-112">Not supported.</span></span>|
|<span data-ttu-id="20128-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="20128-113">Application</span></span>|<span data-ttu-id="20128-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="20128-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="20128-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="20128-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/troubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="20128-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="20128-116">Request headers</span></span>
|<span data-ttu-id="20128-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="20128-117">Header</span></span>|<span data-ttu-id="20128-118">Valor</span><span class="sxs-lookup"><span data-stu-id="20128-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="20128-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="20128-119">Authorization</span></span>|<span data-ttu-id="20128-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="20128-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="20128-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="20128-121">Accept</span></span>|<span data-ttu-id="20128-122">application/json</span><span class="sxs-lookup"><span data-stu-id="20128-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="20128-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="20128-123">Request body</span></span>
<span data-ttu-id="20128-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto enrollmentTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="20128-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="20128-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto enrollmentTroubleshootingEvent.</span><span class="sxs-lookup"><span data-stu-id="20128-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="20128-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="20128-126">Property</span></span>|<span data-ttu-id="20128-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="20128-127">Type</span></span>|<span data-ttu-id="20128-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="20128-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="20128-129">id</span><span class="sxs-lookup"><span data-stu-id="20128-129">id</span></span>|<span data-ttu-id="20128-130">String</span><span class="sxs-lookup"><span data-stu-id="20128-130">String</span></span>|<span data-ttu-id="20128-131">UUID del objeto. Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="20128-131">UUID for the object Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="20128-132">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="20128-132">eventDateTime</span></span>|<span data-ttu-id="20128-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="20128-133">DateTimeOffset</span></span>|<span data-ttu-id="20128-134">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="20128-134">Time when the event occurred .</span></span> <span data-ttu-id="20128-135">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="20128-135">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="20128-136">correlationId</span><span class="sxs-lookup"><span data-stu-id="20128-136">correlationId</span></span>|<span data-ttu-id="20128-137">String</span><span class="sxs-lookup"><span data-stu-id="20128-137">String</span></span>|<span data-ttu-id="20128-138">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="20128-138">Id used for tracing the failure in the service.</span></span> <span data-ttu-id="20128-139">Heredado de [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span><span class="sxs-lookup"><span data-stu-id="20128-139">Inherited from [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md)</span></span>|
|<span data-ttu-id="20128-140">managedDeviceIdentifier</span><span class="sxs-lookup"><span data-stu-id="20128-140">managedDeviceIdentifier</span></span>|<span data-ttu-id="20128-141">String</span><span class="sxs-lookup"><span data-stu-id="20128-141">String</span></span>|<span data-ttu-id="20128-142">Identificador del dispositivo creado o recopilado por Intune.</span><span class="sxs-lookup"><span data-stu-id="20128-142">Device identifier created or collected by Intune.</span></span>|
|<span data-ttu-id="20128-143">operatingSystem</span><span class="sxs-lookup"><span data-stu-id="20128-143">operatingSystem</span></span>|<span data-ttu-id="20128-144">String</span><span class="sxs-lookup"><span data-stu-id="20128-144">String</span></span>|<span data-ttu-id="20128-145">Sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="20128-145">Operating system</span></span>|
|<span data-ttu-id="20128-146">osVersion</span><span class="sxs-lookup"><span data-stu-id="20128-146">osVersion</span></span>|<span data-ttu-id="20128-147">String</span><span class="sxs-lookup"><span data-stu-id="20128-147">String</span></span>|<span data-ttu-id="20128-148">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="20128-148">OS Version.</span></span>|
|<span data-ttu-id="20128-149">userId</span><span class="sxs-lookup"><span data-stu-id="20128-149">userID</span></span>|<span data-ttu-id="20128-150">String</span><span class="sxs-lookup"><span data-stu-id="20128-150">String</span></span>|<span data-ttu-id="20128-151">Identificador del usuario que intentó inscribir el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20128-151">Identifier for the user that tried to enroll the device.</span></span>|
|<span data-ttu-id="20128-152">deviceId</span><span class="sxs-lookup"><span data-stu-id="20128-152">deviceId</span></span>|<span data-ttu-id="20128-153">String</span><span class="sxs-lookup"><span data-stu-id="20128-153">String</span></span>|<span data-ttu-id="20128-154">Identificador de dispositivo de Azure AD.</span><span class="sxs-lookup"><span data-stu-id="20128-154">Azure AD device identifier.</span></span>|
|<span data-ttu-id="20128-155">enrollmentType</span><span class="sxs-lookup"><span data-stu-id="20128-155">enrollmentType</span></span>|<span data-ttu-id="20128-156">String</span><span class="sxs-lookup"><span data-stu-id="20128-156">String</span></span>|<span data-ttu-id="20128-157">Tipo de la inscripción.</span><span class="sxs-lookup"><span data-stu-id="20128-157">Type of the enrollment.</span></span> <span data-ttu-id="20128-158">Los valores posibles son: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin` y `windowsCoManagement`.</span><span class="sxs-lookup"><span data-stu-id="20128-158">Possible values are: `unknown`, `userEnrollment`, `deviceEnrollmentManager`, `appleBulkWithUser`, `appleBulkWithoutUser`, `windowsAzureADJoin`, `windowsBulkUserless`, `windowsAutoEnrollment`, `windowsBulkAzureDomainJoin`, `windowsCoManagement`.</span></span>|
|<span data-ttu-id="20128-159">failureCategory</span><span class="sxs-lookup"><span data-stu-id="20128-159">failureCategory</span></span>|<span data-ttu-id="20128-160">String</span><span class="sxs-lookup"><span data-stu-id="20128-160">String</span></span>|<span data-ttu-id="20128-161">Categoría general del error.</span><span class="sxs-lookup"><span data-stu-id="20128-161">Highlevel failure category.</span></span> <span data-ttu-id="20128-162">Los valores posibles son: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced` y `clientDisconnected`.</span><span class="sxs-lookup"><span data-stu-id="20128-162">Possible values are: `unknown`, `authentication`, `authorization`, `accountValidation`, `userValidation`, `deviceNotSupported`, `inMaintenance`, `badRequest`, `featureNotSupported`, `enrollmentRestrictionsEnforced`, `clientDisconnected`.</span></span>|
|<span data-ttu-id="20128-163">failureReason</span><span class="sxs-lookup"><span data-stu-id="20128-163">failureReason</span></span>|<span data-ttu-id="20128-164">String</span><span class="sxs-lookup"><span data-stu-id="20128-164">String</span></span>|<span data-ttu-id="20128-165">Motivo del error detallado.</span><span class="sxs-lookup"><span data-stu-id="20128-165">Detailed failure reason.</span></span>|



## <a name="response"></a><span data-ttu-id="20128-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="20128-166">Response</span></span>
<span data-ttu-id="20128-167">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="20128-167">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="20128-168">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="20128-168">Example</span></span>
### <a name="request"></a><span data-ttu-id="20128-169">Solicitud</span><span class="sxs-lookup"><span data-stu-id="20128-169">Request</span></span>
<span data-ttu-id="20128-170">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="20128-170">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="20128-171">Respuesta</span><span class="sxs-lookup"><span data-stu-id="20128-171">Response</span></span>
<span data-ttu-id="20128-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="20128-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



