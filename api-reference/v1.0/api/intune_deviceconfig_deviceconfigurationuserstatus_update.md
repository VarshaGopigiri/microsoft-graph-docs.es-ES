# <a name="update-deviceconfigurationuserstatus"></a><span data-ttu-id="67cb5-101">Actualizar deviceConfigurationUserStatus</span><span class="sxs-lookup"><span data-stu-id="67cb5-101">Update deviceConfigurationUserStatus</span></span>

> <span data-ttu-id="67cb5-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="67cb5-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="67cb5-103">Actualice las propiedades de un objeto [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="67cb5-103">Update the properties of a [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="67cb5-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="67cb5-104">Prerequisites</span></span>
<span data-ttu-id="67cb5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="67cb5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="67cb5-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="67cb5-107">Permission type</span></span>|<span data-ttu-id="67cb5-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="67cb5-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="67cb5-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="67cb5-109">Delegated (work or school account)</span></span>|<span data-ttu-id="67cb5-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="67cb5-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="67cb5-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="67cb5-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="67cb5-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="67cb5-112">Not supported.</span></span>|
|<span data-ttu-id="67cb5-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="67cb5-113">Application</span></span>|<span data-ttu-id="67cb5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="67cb5-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="67cb5-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="67cb5-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatuses/{deviceConfigurationUserStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="67cb5-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="67cb5-116">Request headers</span></span>
|<span data-ttu-id="67cb5-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67cb5-117">Header</span></span>|<span data-ttu-id="67cb5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="67cb5-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="67cb5-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="67cb5-119">Authorization</span></span>|<span data-ttu-id="67cb5-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="67cb5-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="67cb5-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="67cb5-121">Accept</span></span>|<span data-ttu-id="67cb5-122">application/json</span><span class="sxs-lookup"><span data-stu-id="67cb5-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="67cb5-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="67cb5-123">Request body</span></span>
<span data-ttu-id="67cb5-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="67cb5-124">In the request body, supply a JSON representation for the [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md) object.</span></span>

<span data-ttu-id="67cb5-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="67cb5-125">The following table shows the properties that are required when you create the [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md).</span></span>

|<span data-ttu-id="67cb5-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67cb5-126">Property</span></span>|<span data-ttu-id="67cb5-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="67cb5-127">Type</span></span>|<span data-ttu-id="67cb5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="67cb5-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="67cb5-129">id</span><span class="sxs-lookup"><span data-stu-id="67cb5-129">id</span></span>|<span data-ttu-id="67cb5-130">String</span><span class="sxs-lookup"><span data-stu-id="67cb5-130">String</span></span>|<span data-ttu-id="67cb5-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="67cb5-131">Key of the entity.</span></span>|
|<span data-ttu-id="67cb5-132">userDisplayName</span><span class="sxs-lookup"><span data-stu-id="67cb5-132">userDisplayName</span></span>|<span data-ttu-id="67cb5-133">String</span><span class="sxs-lookup"><span data-stu-id="67cb5-133">String</span></span>|<span data-ttu-id="67cb5-134">Nombre de usuario de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="67cb5-134">User name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="67cb5-135">devicesCount</span><span class="sxs-lookup"><span data-stu-id="67cb5-135">devicesCount</span></span>|<span data-ttu-id="67cb5-136">Int32</span><span class="sxs-lookup"><span data-stu-id="67cb5-136">Int32</span></span>|<span data-ttu-id="67cb5-137">Número de dispositivos para dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="67cb5-137">Devices count for that user.</span></span>|
|<span data-ttu-id="67cb5-138">status</span><span class="sxs-lookup"><span data-stu-id="67cb5-138">status</span></span>|[<span data-ttu-id="67cb5-139">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="67cb5-139">complianceStatus</span></span>](../resources/intune_shared_compliancestatus.md)|<span data-ttu-id="67cb5-140">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="67cb5-140">Compliance status of the policy report.</span></span> <span data-ttu-id="67cb5-141">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="67cb5-141">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="67cb5-142">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="67cb5-142">lastReportedDateTime</span></span>|<span data-ttu-id="67cb5-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="67cb5-143">DateTimeOffset</span></span>|<span data-ttu-id="67cb5-144">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="67cb5-144">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="67cb5-145">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="67cb5-145">userPrincipalName</span></span>|<span data-ttu-id="67cb5-146">String</span><span class="sxs-lookup"><span data-stu-id="67cb5-146">String</span></span>|<span data-ttu-id="67cb5-147">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="67cb5-147">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="67cb5-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67cb5-148">Response</span></span>
<span data-ttu-id="67cb5-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="67cb5-149">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="67cb5-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="67cb5-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="67cb5-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="67cb5-151">Request</span></span>
<span data-ttu-id="67cb5-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="67cb5-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatuses/{deviceConfigurationUserStatusId}
Content-type: application/json
Content-length: 290

{
  "@odata.type": "#microsoft.graph.deviceConfigurationUserStatus",
  "userDisplayName": "User Display Name value",
  "devicesCount": 12,
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="67cb5-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67cb5-153">Response</span></span>
<span data-ttu-id="67cb5-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="67cb5-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 339

{
  "@odata.type": "#microsoft.graph.deviceConfigurationUserStatus",
  "id": "7e323db2-3db2-7e32-b23d-327eb23d327e",
  "userDisplayName": "User Display Name value",
  "devicesCount": 12,
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```



