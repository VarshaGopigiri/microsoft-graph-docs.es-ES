# <a name="update-iosupdatedevicestatus"></a><span data-ttu-id="63138-101">Actualizar iosUpdateDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="63138-101">Update iosUpdateDeviceStatus</span></span>

> <span data-ttu-id="63138-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="63138-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="63138-103">Actualice las propiedades de un objeto [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="63138-103">Update the properties of a [calendar](../resources/intune_deviceconfig_iosupdatedevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="63138-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="63138-104">Prerequisites</span></span>
<span data-ttu-id="63138-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="63138-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="63138-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="63138-107">Permission type</span></span>|<span data-ttu-id="63138-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="63138-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="63138-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="63138-109">Delegated (work or school account)</span></span>|<span data-ttu-id="63138-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="63138-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="63138-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="63138-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="63138-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63138-112">Not supported.</span></span>|
|<span data-ttu-id="63138-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="63138-113">Application</span></span>|<span data-ttu-id="63138-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="63138-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="63138-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="63138-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="63138-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="63138-116">Request headers</span></span>
|<span data-ttu-id="63138-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63138-117">Header</span></span>|<span data-ttu-id="63138-118">Valor</span><span class="sxs-lookup"><span data-stu-id="63138-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="63138-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="63138-119">Authorization</span></span>|<span data-ttu-id="63138-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="63138-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="63138-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="63138-121">Accept</span></span>|<span data-ttu-id="63138-122">application/json</span><span class="sxs-lookup"><span data-stu-id="63138-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="63138-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="63138-123">Request body</span></span>
<span data-ttu-id="63138-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="63138-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_iosupdatedevicestatus.md) object.</span></span>

<span data-ttu-id="63138-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="63138-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="63138-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="63138-126">Property</span></span>|<span data-ttu-id="63138-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="63138-127">Type</span></span>|<span data-ttu-id="63138-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="63138-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="63138-129">id</span><span class="sxs-lookup"><span data-stu-id="63138-129">id</span></span>|<span data-ttu-id="63138-130">String</span><span class="sxs-lookup"><span data-stu-id="63138-130">String</span></span>|<span data-ttu-id="63138-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="63138-131">Key of the setting.</span></span>|
|<span data-ttu-id="63138-132">installStatus</span><span class="sxs-lookup"><span data-stu-id="63138-132">installStatus</span></span>|<span data-ttu-id="63138-133">String</span><span class="sxs-lookup"><span data-stu-id="63138-133">String</span></span>|<span data-ttu-id="63138-134">Estado de la instalación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="63138-134">The installation status of the policy report.</span></span> <span data-ttu-id="63138-135">Los valores posibles son: `success`, `available`, `idle`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation` y `sharedDeviceUserLoggedInError`.</span><span class="sxs-lookup"><span data-stu-id="63138-135">Possible values are: `success`, `available`, `idle`, `downloading`, `downloadFailed`, `downloadRequiresComputer`, `downloadInsufficientSpace`, `downloadInsufficientPower`, `downloadInsufficientNetwork`, `installing`, `installInsufficientSpace`, `installInsufficientPower`, `installPhoneCallInProgress`, `installFailed`, `notSupportedOperation`, `sharedDeviceUserLoggedInError`.</span></span>|
|<span data-ttu-id="63138-136">osVersion</span><span class="sxs-lookup"><span data-stu-id="63138-136">osVersion</span></span>|<span data-ttu-id="63138-137">String</span><span class="sxs-lookup"><span data-stu-id="63138-137">String</span></span>|<span data-ttu-id="63138-138">La versión del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="63138-138">The device version that is being reported.</span></span>|
|<span data-ttu-id="63138-139">deviceId</span><span class="sxs-lookup"><span data-stu-id="63138-139">deviceId</span></span>|<span data-ttu-id="63138-140">String</span><span class="sxs-lookup"><span data-stu-id="63138-140">String</span></span>|<span data-ttu-id="63138-141">El identificador del dispositivo que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="63138-141">The device id that is being reported.</span></span>|
|<span data-ttu-id="63138-142">userId</span><span class="sxs-lookup"><span data-stu-id="63138-142">userID</span></span>|<span data-ttu-id="63138-143">String</span><span class="sxs-lookup"><span data-stu-id="63138-143">String</span></span>|<span data-ttu-id="63138-144">El identificador del usuario que se está notificando.</span><span class="sxs-lookup"><span data-stu-id="63138-144">The User id that is being reported.</span></span>|
|<span data-ttu-id="63138-145">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="63138-145">deviceDisplayName</span></span>|<span data-ttu-id="63138-146">String</span><span class="sxs-lookup"><span data-stu-id="63138-146">String</span></span>|<span data-ttu-id="63138-147">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="63138-147">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="63138-148">userName</span><span class="sxs-lookup"><span data-stu-id="63138-148">userName</span></span>|<span data-ttu-id="63138-149">String</span><span class="sxs-lookup"><span data-stu-id="63138-149">String</span></span>|<span data-ttu-id="63138-150">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="63138-150">The User Name that is being reported</span></span>|
|<span data-ttu-id="63138-151">deviceModel</span><span class="sxs-lookup"><span data-stu-id="63138-151">deviceModel</span></span>|<span data-ttu-id="63138-152">String</span><span class="sxs-lookup"><span data-stu-id="63138-152">String</span></span>|<span data-ttu-id="63138-153">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="63138-153">The device model that is being reported</span></span>|
|<span data-ttu-id="63138-154">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="63138-154">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="63138-155">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63138-155">DateTimeOffset</span></span>|<span data-ttu-id="63138-156">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="63138-156">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="63138-157">status</span><span class="sxs-lookup"><span data-stu-id="63138-157">status</span></span>|<span data-ttu-id="63138-158">String</span><span class="sxs-lookup"><span data-stu-id="63138-158">String</span></span>|<span data-ttu-id="63138-159">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="63138-159">Compliance status of the policy report.</span></span> <span data-ttu-id="63138-160">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error` y `conflict`.</span><span class="sxs-lookup"><span data-stu-id="63138-160">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`.</span></span>|
|<span data-ttu-id="63138-161">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="63138-161">lastReportedDateTime</span></span>|<span data-ttu-id="63138-162">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="63138-162">DateTimeOffset</span></span>|<span data-ttu-id="63138-163">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="63138-163">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="63138-164">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="63138-164">userPrincipalName</span></span>|<span data-ttu-id="63138-165">String</span><span class="sxs-lookup"><span data-stu-id="63138-165">String</span></span>|<span data-ttu-id="63138-166">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="63138-166">userPrincipalName</span></span>|



## <a name="response"></a><span data-ttu-id="63138-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63138-167">Response</span></span>
<span data-ttu-id="63138-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosUpdateDeviceStatus](../resources/intune_deviceconfig_iosupdatedevicestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="63138-168">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_iosupdatedevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="63138-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="63138-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="63138-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="63138-170">Request</span></span>
<span data-ttu-id="63138-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="63138-171">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
Content-type: application/json
Content-length: 492

{
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

### <a name="response"></a><span data-ttu-id="63138-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="63138-172">Response</span></span>
<span data-ttu-id="63138-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="63138-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



