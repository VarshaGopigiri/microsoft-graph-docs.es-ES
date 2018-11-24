# <a name="create-manageddevicemobileappconfigurationdevicestatus"></a><span data-ttu-id="afb41-101">Crear managedDeviceMobileAppConfigurationDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="afb41-101">Create managedDeviceMobileAppConfigurationDeviceStatus</span></span>

> <span data-ttu-id="afb41-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="afb41-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="afb41-103">Crear un nuevo objeto [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="afb41-103">Create a new [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="afb41-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="afb41-104">Prerequisites</span></span>
<span data-ttu-id="afb41-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="afb41-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="afb41-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="afb41-107">Permission type</span></span>|<span data-ttu-id="afb41-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="afb41-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="afb41-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="afb41-109">Delegated (work or school account)</span></span>|<span data-ttu-id="afb41-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="afb41-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="afb41-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="afb41-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="afb41-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="afb41-112">Not supported.</span></span>|
|<span data-ttu-id="afb41-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="afb41-113">Application</span></span>|<span data-ttu-id="afb41-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="afb41-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="afb41-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="afb41-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="afb41-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="afb41-116">Request headers</span></span>
|<span data-ttu-id="afb41-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="afb41-117">Header</span></span>|<span data-ttu-id="afb41-118">Valor</span><span class="sxs-lookup"><span data-stu-id="afb41-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="afb41-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="afb41-119">Authorization</span></span>|<span data-ttu-id="afb41-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="afb41-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="afb41-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="afb41-121">Accept</span></span>|<span data-ttu-id="afb41-122">application/json</span><span class="sxs-lookup"><span data-stu-id="afb41-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="afb41-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="afb41-123">Request body</span></span>
<span data-ttu-id="afb41-124">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto managedDeviceMobileAppConfigurationDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="afb41-124">In the request body, supply a JSON representation for the managedDeviceMobileAppConfigurationDeviceStatus object.</span></span>

<span data-ttu-id="afb41-125">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el managedDeviceMobileAppConfigurationDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="afb41-125">The following table shows the properties that are required when you create the managedDeviceMobileAppConfigurationDeviceStatus.</span></span>

|<span data-ttu-id="afb41-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="afb41-126">Property</span></span>|<span data-ttu-id="afb41-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="afb41-127">Type</span></span>|<span data-ttu-id="afb41-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="afb41-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="afb41-129">id</span><span class="sxs-lookup"><span data-stu-id="afb41-129">id</span></span>|<span data-ttu-id="afb41-130">String</span><span class="sxs-lookup"><span data-stu-id="afb41-130">String</span></span>|<span data-ttu-id="afb41-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="afb41-131">Key of the entity.</span></span>|
|<span data-ttu-id="afb41-132">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="afb41-132">deviceDisplayName</span></span>|<span data-ttu-id="afb41-133">String</span><span class="sxs-lookup"><span data-stu-id="afb41-133">String</span></span>|<span data-ttu-id="afb41-134">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="afb41-134">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="afb41-135">userName</span><span class="sxs-lookup"><span data-stu-id="afb41-135">userName</span></span>|<span data-ttu-id="afb41-136">String</span><span class="sxs-lookup"><span data-stu-id="afb41-136">String</span></span>|<span data-ttu-id="afb41-137">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="afb41-137">The User Name that is being reported</span></span>|
|<span data-ttu-id="afb41-138">deviceModel</span><span class="sxs-lookup"><span data-stu-id="afb41-138">deviceModel</span></span>|<span data-ttu-id="afb41-139">String</span><span class="sxs-lookup"><span data-stu-id="afb41-139">String</span></span>|<span data-ttu-id="afb41-140">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="afb41-140">The device model that is being reported</span></span>|
|<span data-ttu-id="afb41-141">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="afb41-141">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="afb41-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="afb41-142">DateTimeOffset</span></span>|<span data-ttu-id="afb41-143">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="afb41-143">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="afb41-144">status</span><span class="sxs-lookup"><span data-stu-id="afb41-144">status</span></span>|[<span data-ttu-id="afb41-145">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="afb41-145">complianceStatus</span></span>](../resources/intune_shared_compliancestatus.md)|<span data-ttu-id="afb41-146">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="afb41-146">Compliance status of the policy report.</span></span> <span data-ttu-id="afb41-147">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="afb41-147">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="afb41-148">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="afb41-148">lastReportedDateTime</span></span>|<span data-ttu-id="afb41-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="afb41-149">DateTimeOffset</span></span>|<span data-ttu-id="afb41-150">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="afb41-150">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="afb41-151">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="afb41-151">userPrincipalName</span></span>|<span data-ttu-id="afb41-152">String</span><span class="sxs-lookup"><span data-stu-id="afb41-152">String</span></span>|<span data-ttu-id="afb41-153">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="afb41-153">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="afb41-154">Respuesta</span><span class="sxs-lookup"><span data-stu-id="afb41-154">Response</span></span>
<span data-ttu-id="afb41-155">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="afb41-155">If successful, this method returns a `201 Created` response code and a [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="afb41-156">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="afb41-156">Example</span></span>
### <a name="request"></a><span data-ttu-id="afb41-157">Solicitud</span><span class="sxs-lookup"><span data-stu-id="afb41-157">Request</span></span>
<span data-ttu-id="afb41-158">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="afb41-158">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses
Content-type: application/json
Content-length: 445

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceStatus",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="afb41-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="afb41-159">Response</span></span>
<span data-ttu-id="afb41-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="afb41-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 494

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceStatus",
  "id": "477d3651-3651-477d-5136-7d4751367d47",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```



