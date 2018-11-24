# <a name="update-iosupdatedevicestatus"></a><span data-ttu-id="ea4b3-101">Actualizar iosUpdateDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="ea4b3-101">Update iosUpdateDeviceStatus</span></span>

> <span data-ttu-id="ea4b3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ea4b3-103">Actualice las propiedades de un objeto [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="ea4b3-103">Update the properties of a [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ea4b3-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ea4b3-104">Prerequisites</span></span>
<span data-ttu-id="ea4b3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ea4b3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ea4b3-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ea4b3-107">Permission type</span></span>|<span data-ttu-id="ea4b3-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ea4b3-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ea4b3-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ea4b3-109">Delegated (work or school account)</span></span>|<span data-ttu-id="ea4b3-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ea4b3-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ea4b3-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ea4b3-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ea4b3-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-112">Not supported.</span></span>|
|<span data-ttu-id="ea4b3-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ea4b3-113">Application</span></span>|<span data-ttu-id="ea4b3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ea4b3-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ea4b3-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="ea4b3-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ea4b3-116">Request headers</span></span>
|<span data-ttu-id="ea4b3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ea4b3-117">Header</span></span>|<span data-ttu-id="ea4b3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ea4b3-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ea4b3-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="ea4b3-119">Authorization</span></span>|<span data-ttu-id="ea4b3-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ea4b3-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ea4b3-121">Accept</span></span>|<span data-ttu-id="ea4b3-122">application/json</span><span class="sxs-lookup"><span data-stu-id="ea4b3-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ea4b3-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ea4b3-123">Request body</span></span>
<span data-ttu-id="ea4b3-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="ea4b3-124">In the request body, supply a JSON representation for the [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md) object.</span></span>

<span data-ttu-id="ea4b3-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="ea4b3-125">The following table shows the properties that are required when you create the [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).</span></span>

|<span data-ttu-id="ea4b3-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ea4b3-126">Property</span></span>|<span data-ttu-id="ea4b3-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="ea4b3-127">Type</span></span>|<span data-ttu-id="ea4b3-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ea4b3-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ea4b3-129">id</span><span class="sxs-lookup"><span data-stu-id="ea4b3-129">id</span></span>|<span data-ttu-id="ea4b3-130">String</span><span class="sxs-lookup"><span data-stu-id="ea4b3-130">String</span></span>|<span data-ttu-id="ea4b3-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-131">Key of the entity.</span></span>|
|<span data-ttu-id="ea4b3-132">installStatus</span><span class="sxs-lookup"><span data-stu-id="ea4b3-132">installStatus</span></span>|[<span data-ttu-id="ea4b3-133">iosUpdatesInstallStatus</span><span class="sxs-lookup"><span data-stu-id="ea4b3-133">iosUpdatesInstallStatus</span></span>](../resources/intune_deviceconfig_iosupdatesinstallstatus.md)|<span data-ttu-id="ea4b3-134">Estado de la instalación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-134">The installation status of the policy report.</span></span> <span data-ttu-id="ea4b3-135">Los valores posibles son: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-135">Possible values are: `success`, `available`, `idle`, `unknown`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span></span>|
|<span data-ttu-id="ea4b3-136">osVersion</span><span class="sxs-lookup"><span data-stu-id="ea4b3-136">osVersion</span></span>|<span data-ttu-id="ea4b3-137">String</span><span class="sxs-lookup"><span data-stu-id="ea4b3-137">String</span></span>|<span data-ttu-id="ea4b3-138">La versión del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-138">The device version that is being reported.</span></span>|
|<span data-ttu-id="ea4b3-139">deviceId</span><span class="sxs-lookup"><span data-stu-id="ea4b3-139">deviceId</span></span>|<span data-ttu-id="ea4b3-140">String</span><span class="sxs-lookup"><span data-stu-id="ea4b3-140">String</span></span>|<span data-ttu-id="ea4b3-141">El identificador del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-141">The device id that is being reported.</span></span>|
|<span data-ttu-id="ea4b3-142">userId</span><span class="sxs-lookup"><span data-stu-id="ea4b3-142">userId</span></span>|<span data-ttu-id="ea4b3-143">String</span><span class="sxs-lookup"><span data-stu-id="ea4b3-143">String</span></span>|<span data-ttu-id="ea4b3-144">El identificador del usuario que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-144">The User id that is being reported.</span></span>|
|<span data-ttu-id="ea4b3-145">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="ea4b3-145">deviceDisplayName</span></span>|<span data-ttu-id="ea4b3-146">String</span><span class="sxs-lookup"><span data-stu-id="ea4b3-146">String</span></span>|<span data-ttu-id="ea4b3-147">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-147">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="ea4b3-148">userName</span><span class="sxs-lookup"><span data-stu-id="ea4b3-148">userName</span></span>|<span data-ttu-id="ea4b3-149">String</span><span class="sxs-lookup"><span data-stu-id="ea4b3-149">String</span></span>|<span data-ttu-id="ea4b3-150">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="ea4b3-150">The User Name that is being reported</span></span>|
|<span data-ttu-id="ea4b3-151">deviceModel</span><span class="sxs-lookup"><span data-stu-id="ea4b3-151">deviceModel</span></span>|<span data-ttu-id="ea4b3-152">String</span><span class="sxs-lookup"><span data-stu-id="ea4b3-152">String</span></span>|<span data-ttu-id="ea4b3-153">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="ea4b3-153">The device model that is being reported</span></span>|
|<span data-ttu-id="ea4b3-154">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="ea4b3-154">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="ea4b3-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea4b3-155">DateTimeOffset</span></span>|<span data-ttu-id="ea4b3-156">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ea4b3-156">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="ea4b3-157">status</span><span class="sxs-lookup"><span data-stu-id="ea4b3-157">status</span></span>|[<span data-ttu-id="ea4b3-158">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="ea4b3-158">complianceStatus</span></span>](../resources/intune_shared_compliancestatus.md)|<span data-ttu-id="ea4b3-159">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-159">Compliance status of the policy report.</span></span> <span data-ttu-id="ea4b3-160">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-160">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="ea4b3-161">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="ea4b3-161">lastReportedDateTime</span></span>|<span data-ttu-id="ea4b3-162">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ea4b3-162">DateTimeOffset</span></span>|<span data-ttu-id="ea4b3-163">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-163">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="ea4b3-164">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ea4b3-164">userPrincipalName</span></span>|<span data-ttu-id="ea4b3-165">String</span><span class="sxs-lookup"><span data-stu-id="ea4b3-165">String</span></span>|<span data-ttu-id="ea4b3-166">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-166">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="ea4b3-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea4b3-167">Response</span></span>
<span data-ttu-id="ea4b3-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-168">If successful, this method returns a `200 OK` response code and an updated [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ea4b3-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ea4b3-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="ea4b3-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ea4b3-170">Request</span></span>
<span data-ttu-id="ea4b3-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-171">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
Content-type: application/json
Content-length: 552

{
  "@odata.type": "#microsoft.graph.iosUpdateDeviceStatus",
  "installStatus": "available",
  "osVersion": "Os Version value",
  "deviceId": "Device Id value",
  "userId": "User Id value",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="ea4b3-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ea4b3-172">Response</span></span>
<span data-ttu-id="ea4b3-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ea4b3-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 601

{
  "@odata.type": "#microsoft.graph.iosUpdateDeviceStatus",
  "id": "63a79499-9499-63a7-9994-a7639994a763",
  "installStatus": "available",
  "osVersion": "Os Version value",
  "deviceId": "Device Id value",
  "userId": "User Id value",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```



