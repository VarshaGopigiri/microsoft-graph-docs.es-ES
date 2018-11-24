# <a name="update-manageddevicemobileappconfigurationuserstatus"></a><span data-ttu-id="bf950-101">Actualizar managedDeviceMobileAppConfigurationUserStatus</span><span class="sxs-lookup"><span data-stu-id="bf950-101">Update managedDeviceMobileAppConfigurationUserStatus</span></span>

> <span data-ttu-id="bf950-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bf950-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bf950-103">Actualice las propiedades de un objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="bf950-103">Update the properties of a [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bf950-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bf950-104">Prerequisites</span></span>
<span data-ttu-id="bf950-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bf950-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bf950-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bf950-107">Permission type</span></span>|<span data-ttu-id="bf950-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bf950-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bf950-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bf950-109">Delegated (work or school account)</span></span>|<span data-ttu-id="bf950-110">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bf950-110">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="bf950-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bf950-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bf950-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf950-112">Not supported.</span></span>|
|<span data-ttu-id="bf950-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bf950-113">Application</span></span>|<span data-ttu-id="bf950-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bf950-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bf950-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bf950-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/userStatuses/{managedDeviceMobileAppConfigurationUserStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="bf950-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bf950-116">Request headers</span></span>
|<span data-ttu-id="bf950-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bf950-117">Header</span></span>|<span data-ttu-id="bf950-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bf950-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bf950-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="bf950-119">Authorization</span></span>|<span data-ttu-id="bf950-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bf950-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bf950-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bf950-121">Accept</span></span>|<span data-ttu-id="bf950-122">application/json</span><span class="sxs-lookup"><span data-stu-id="bf950-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bf950-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bf950-123">Request body</span></span>
<span data-ttu-id="bf950-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="bf950-124">In the request body, supply a JSON representation for the [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md) object.</span></span>

<span data-ttu-id="bf950-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="bf950-125">The following table shows the properties that are required when you create the [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md).</span></span>

|<span data-ttu-id="bf950-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bf950-126">Property</span></span>|<span data-ttu-id="bf950-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf950-127">Type</span></span>|<span data-ttu-id="bf950-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf950-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bf950-129">id</span><span class="sxs-lookup"><span data-stu-id="bf950-129">id</span></span>|<span data-ttu-id="bf950-130">String</span><span class="sxs-lookup"><span data-stu-id="bf950-130">String</span></span>|<span data-ttu-id="bf950-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bf950-131">Key of the entity.</span></span>|
|<span data-ttu-id="bf950-132">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="bf950-132">userDisplayName</span></span>|<span data-ttu-id="bf950-133">String</span><span class="sxs-lookup"><span data-stu-id="bf950-133">String</span></span>|<span data-ttu-id="bf950-134">Nombre de usuario de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="bf950-134">User name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="bf950-135">devicesCount</span><span class="sxs-lookup"><span data-stu-id="bf950-135">devicesCount</span></span>|<span data-ttu-id="bf950-136">Int32</span><span class="sxs-lookup"><span data-stu-id="bf950-136">Int32</span></span>|<span data-ttu-id="bf950-137">Número de dispositivos para dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="bf950-137">Devices count for that user.</span></span>|
|<span data-ttu-id="bf950-138">status</span><span class="sxs-lookup"><span data-stu-id="bf950-138">status</span></span>|[<span data-ttu-id="bf950-139">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="bf950-139">complianceStatus</span></span>](../resources/intune_shared_compliancestatus.md)|<span data-ttu-id="bf950-140">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="bf950-140">Compliance status of the policy report.</span></span> <span data-ttu-id="bf950-141">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="bf950-141">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="bf950-142">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="bf950-142">lastReportedDateTime</span></span>|<span data-ttu-id="bf950-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bf950-143">DateTimeOffset</span></span>|<span data-ttu-id="bf950-144">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="bf950-144">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="bf950-145">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="bf950-145">userPrincipalName</span></span>|<span data-ttu-id="bf950-146">String</span><span class="sxs-lookup"><span data-stu-id="bf950-146">String</span></span>|<span data-ttu-id="bf950-147">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="bf950-147">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="bf950-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf950-148">Response</span></span>
<span data-ttu-id="bf950-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bf950-149">If successful, this method returns a `200 OK` response code and an updated [managedDeviceMobileAppConfigurationUserStatus](../resources/intune_apps_manageddevicemobileappconfigurationuserstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bf950-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bf950-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="bf950-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bf950-151">Request</span></span>
<span data-ttu-id="bf950-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bf950-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/userStatuses/{managedDeviceMobileAppConfigurationUserStatusId}
Content-type: application/json
Content-length: 306

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationUserStatus",
  "userDisplayName": "User Display Name value",
  "devicesCount": 12,
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="bf950-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bf950-153">Response</span></span>
<span data-ttu-id="bf950-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bf950-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 355

{
  "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationUserStatus",
  "id": "44960944-0944-4496-4409-964444099644",
  "userDisplayName": "User Display Name value",
  "devicesCount": 12,
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```



