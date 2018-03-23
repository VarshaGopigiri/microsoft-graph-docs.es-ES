# <a name="update-settingstatedevicesummary"></a><span data-ttu-id="82024-101">Actualizar settingStateDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="82024-101">Update settingStateDeviceSummary</span></span>

> <span data-ttu-id="82024-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="82024-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="82024-103">Actualice las propiedades de un objeto [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="82024-103">Update the properties of a [calendar](../resources/intune_deviceconfig_settingstatedevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="82024-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="82024-104">Prerequisites</span></span>
<span data-ttu-id="82024-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="82024-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="82024-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="82024-107">Permission type</span></span>|<span data-ttu-id="82024-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="82024-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="82024-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="82024-109">Delegated (work or school account)</span></span>|<span data-ttu-id="82024-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="82024-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="82024-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="82024-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="82024-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82024-112">Not supported.</span></span>|
|<span data-ttu-id="82024-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="82024-113">Application</span></span>|<span data-ttu-id="82024-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82024-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="82024-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="82024-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="82024-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="82024-116">Request headers</span></span>
|<span data-ttu-id="82024-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82024-117">Header</span></span>|<span data-ttu-id="82024-118">Valor</span><span class="sxs-lookup"><span data-stu-id="82024-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="82024-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="82024-119">Authorization</span></span>|<span data-ttu-id="82024-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="82024-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="82024-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="82024-121">Accept</span></span>|<span data-ttu-id="82024-122">application/json</span><span class="sxs-lookup"><span data-stu-id="82024-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="82024-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="82024-123">Request body</span></span>
<span data-ttu-id="82024-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="82024-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_settingstatedevicesummary.md) object.</span></span>

<span data-ttu-id="82024-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="82024-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="82024-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82024-126">Property</span></span>|<span data-ttu-id="82024-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="82024-127">Type</span></span>|<span data-ttu-id="82024-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="82024-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="82024-129">id</span><span class="sxs-lookup"><span data-stu-id="82024-129">id</span></span>|<span data-ttu-id="82024-130">String</span><span class="sxs-lookup"><span data-stu-id="82024-130">String</span></span>|<span data-ttu-id="82024-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="82024-131">Key of the setting.</span></span>|
|<span data-ttu-id="82024-132">settingName</span><span class="sxs-lookup"><span data-stu-id="82024-132">settingName</span></span>|<span data-ttu-id="82024-133">String</span><span class="sxs-lookup"><span data-stu-id="82024-133">String</span></span>|<span data-ttu-id="82024-134">Nombre de la configuración</span><span class="sxs-lookup"><span data-stu-id="82024-134">Name of the setting.</span></span>|
|<span data-ttu-id="82024-135">instancePath</span><span class="sxs-lookup"><span data-stu-id="82024-135">instancePath</span></span>|<span data-ttu-id="82024-136">String</span><span class="sxs-lookup"><span data-stu-id="82024-136">String</span></span>|<span data-ttu-id="82024-137">Nombre de InstancePath para la configuración</span><span class="sxs-lookup"><span data-stu-id="82024-137">Name of the InstancePath for the setting</span></span>|
|<span data-ttu-id="82024-138">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="82024-138">unknownDeviceCount</span></span>|<span data-ttu-id="82024-139">Int32</span><span class="sxs-lookup"><span data-stu-id="82024-139">Int32</span></span>|<span data-ttu-id="82024-140">Número de dispositivos desconocido para la configuración</span><span class="sxs-lookup"><span data-stu-id="82024-140">Device Unkown count for the setting</span></span>|
|<span data-ttu-id="82024-141">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="82024-141">notApplicableDeviceCount</span></span>|<span data-ttu-id="82024-142">Int32</span><span class="sxs-lookup"><span data-stu-id="82024-142">Int32</span></span>|<span data-ttu-id="82024-143">Número de dispositivos no aplicables para la configuración</span><span class="sxs-lookup"><span data-stu-id="82024-143">Device Not Applicable count for the setting</span></span>|
|<span data-ttu-id="82024-144">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="82024-144">compliantDeviceCount</span></span>|<span data-ttu-id="82024-145">Int32</span><span class="sxs-lookup"><span data-stu-id="82024-145">Int32</span></span>|<span data-ttu-id="82024-146">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="82024-146">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="82024-147">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="82024-147">remediatedDeviceCount</span></span>|<span data-ttu-id="82024-148">Int32</span><span class="sxs-lookup"><span data-stu-id="82024-148">Int32</span></span>|<span data-ttu-id="82024-149">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="82024-149">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="82024-150">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="82024-150">nonCompliantDeviceCount</span></span>|<span data-ttu-id="82024-151">Int32</span><span class="sxs-lookup"><span data-stu-id="82024-151">Int32</span></span>|<span data-ttu-id="82024-152">Número de dispositivos no compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="82024-152">Device NonCompliant count for the setting</span></span>|
|<span data-ttu-id="82024-153">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="82024-153">errorDeviceCount</span></span>|<span data-ttu-id="82024-154">Int32</span><span class="sxs-lookup"><span data-stu-id="82024-154">Int32</span></span>|<span data-ttu-id="82024-155">Número de errores de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="82024-155">Device error count for the setting</span></span>|
|<span data-ttu-id="82024-156">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="82024-156">conflictDeviceCount</span></span>|<span data-ttu-id="82024-157">Int32</span><span class="sxs-lookup"><span data-stu-id="82024-157">Int32</span></span>|<span data-ttu-id="82024-158">Número de errores de conflictos de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="82024-158">Device conflict error count for the setting</span></span>|



## <a name="response"></a><span data-ttu-id="82024-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82024-159">Response</span></span>
<span data-ttu-id="82024-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="82024-160">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_settingstatedevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="82024-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="82024-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="82024-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="82024-162">Request</span></span>
<span data-ttu-id="82024-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="82024-163">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
Content-type: application/json
Content-length: 296

{
  "settingName": "Setting Name value",
  "instancePath": "Instance Path value",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```

### <a name="response"></a><span data-ttu-id="82024-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82024-164">Response</span></span>
<span data-ttu-id="82024-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="82024-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 409

{
  "@odata.type": "#microsoft.graph.settingStateDeviceSummary",
  "id": "3e2d4526-4526-3e2d-2645-2d3e26452d3e",
  "settingName": "Setting Name value",
  "instancePath": "Instance Path value",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```



