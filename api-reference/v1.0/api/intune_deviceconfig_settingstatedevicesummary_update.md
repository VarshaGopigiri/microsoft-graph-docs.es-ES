# <a name="update-settingstatedevicesummary"></a><span data-ttu-id="c4ce6-101">Actualizar settingStateDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="c4ce6-101">Update settingStateDeviceSummary</span></span>

> <span data-ttu-id="c4ce6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c4ce6-103">Actualice las propiedades de un objeto [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="c4ce6-103">Update the properties of a [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c4ce6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c4ce6-104">Prerequisites</span></span>
<span data-ttu-id="c4ce6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c4ce6-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c4ce6-107">Permission type</span></span>|<span data-ttu-id="c4ce6-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c4ce6-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c4ce6-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c4ce6-109">Delegated (work or school account)</span></span>|<span data-ttu-id="c4ce6-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c4ce6-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="c4ce6-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c4ce6-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c4ce6-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-112">Not supported.</span></span>|
|<span data-ttu-id="c4ce6-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c4ce6-113">Application</span></span>|<span data-ttu-id="c4ce6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c4ce6-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c4ce6-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="c4ce6-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c4ce6-116">Request headers</span></span>
|<span data-ttu-id="c4ce6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4ce6-117">Header</span></span>|<span data-ttu-id="c4ce6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c4ce6-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c4ce6-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="c4ce6-119">Authorization</span></span>|<span data-ttu-id="c4ce6-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c4ce6-121">Accept</span><span class="sxs-lookup"><span data-stu-id="c4ce6-121">Accept</span></span>|<span data-ttu-id="c4ce6-122">application/json</span><span class="sxs-lookup"><span data-stu-id="c4ce6-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c4ce6-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c4ce6-123">Request body</span></span>
<span data-ttu-id="c4ce6-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="c4ce6-124">In the request body, supply a JSON representation for the [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md) object.</span></span>

<span data-ttu-id="c4ce6-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="c4ce6-125">The following table shows the properties that are required when you create the [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md).</span></span>

|<span data-ttu-id="c4ce6-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c4ce6-126">Property</span></span>|<span data-ttu-id="c4ce6-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="c4ce6-127">Type</span></span>|<span data-ttu-id="c4ce6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="c4ce6-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c4ce6-129">id</span><span class="sxs-lookup"><span data-stu-id="c4ce6-129">id</span></span>|<span data-ttu-id="c4ce6-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="c4ce6-130">String</span></span>|<span data-ttu-id="c4ce6-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-131">Key of the entity.</span></span>|
|<span data-ttu-id="c4ce6-132">settingName</span><span class="sxs-lookup"><span data-stu-id="c4ce6-132">settingName</span></span>|<span data-ttu-id="c4ce6-133">String</span><span class="sxs-lookup"><span data-stu-id="c4ce6-133">String</span></span>|<span data-ttu-id="c4ce6-134">Nombre de la configuración</span><span class="sxs-lookup"><span data-stu-id="c4ce6-134">Name of the setting</span></span>|
|<span data-ttu-id="c4ce6-135">instancePath</span><span class="sxs-lookup"><span data-stu-id="c4ce6-135">instancePath</span></span>|<span data-ttu-id="c4ce6-136">String</span><span class="sxs-lookup"><span data-stu-id="c4ce6-136">String</span></span>|<span data-ttu-id="c4ce6-137">Nombre de InstancePath para la configuración</span><span class="sxs-lookup"><span data-stu-id="c4ce6-137">Name of the InstancePath for the setting</span></span>|
|<span data-ttu-id="c4ce6-138">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="c4ce6-138">unknownDeviceCount</span></span>|<span data-ttu-id="c4ce6-139">Int32</span><span class="sxs-lookup"><span data-stu-id="c4ce6-139">Int32</span></span>|<span data-ttu-id="c4ce6-140">Número de dispositivos desconocido para la configuración</span><span class="sxs-lookup"><span data-stu-id="c4ce6-140">Device Unkown count for the setting</span></span>|
|<span data-ttu-id="c4ce6-141">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="c4ce6-141">notApplicableDeviceCount</span></span>|<span data-ttu-id="c4ce6-142">Int32</span><span class="sxs-lookup"><span data-stu-id="c4ce6-142">Int32</span></span>|<span data-ttu-id="c4ce6-143">Número de dispositivos no aplicables para la configuración</span><span class="sxs-lookup"><span data-stu-id="c4ce6-143">Device Not Applicable count for the setting</span></span>|
|<span data-ttu-id="c4ce6-144">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="c4ce6-144">compliantDeviceCount</span></span>|<span data-ttu-id="c4ce6-145">Int32</span><span class="sxs-lookup"><span data-stu-id="c4ce6-145">Int32</span></span>|<span data-ttu-id="c4ce6-146">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="c4ce6-146">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="c4ce6-147">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="c4ce6-147">remediatedDeviceCount</span></span>|<span data-ttu-id="c4ce6-148">Int32</span><span class="sxs-lookup"><span data-stu-id="c4ce6-148">Int32</span></span>|<span data-ttu-id="c4ce6-149">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="c4ce6-149">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="c4ce6-150">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="c4ce6-150">nonCompliantDeviceCount</span></span>|<span data-ttu-id="c4ce6-151">Int32</span><span class="sxs-lookup"><span data-stu-id="c4ce6-151">Int32</span></span>|<span data-ttu-id="c4ce6-152">Número de dispositivos no compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="c4ce6-152">Device NonCompliant count for the setting</span></span>|
|<span data-ttu-id="c4ce6-153">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="c4ce6-153">errorDeviceCount</span></span>|<span data-ttu-id="c4ce6-154">Int32</span><span class="sxs-lookup"><span data-stu-id="c4ce6-154">Int32</span></span>|<span data-ttu-id="c4ce6-155">Número de errores de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="c4ce6-155">Device error count for the setting</span></span>|
|<span data-ttu-id="c4ce6-156">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="c4ce6-156">conflictDeviceCount</span></span>|<span data-ttu-id="c4ce6-157">Int32</span><span class="sxs-lookup"><span data-stu-id="c4ce6-157">Int32</span></span>|<span data-ttu-id="c4ce6-158">Número de errores de conflictos de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="c4ce6-158">Device conflict error count for the setting</span></span>|



## <a name="response"></a><span data-ttu-id="c4ce6-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4ce6-159">Response</span></span>
<span data-ttu-id="c4ce6-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-160">If successful, this method returns a `200 OK` response code and an updated [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c4ce6-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c4ce6-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="c4ce6-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c4ce6-162">Request</span></span>
<span data-ttu-id="c4ce6-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-163">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="c4ce6-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4ce6-164">Response</span></span>
<span data-ttu-id="c4ce6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c4ce6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








