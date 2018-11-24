# <a name="update-devicecompliancepolicysettingstatesummary"></a><span data-ttu-id="319f4-101">Actualizar deviceCompliancePolicySettingStateSummary</span><span class="sxs-lookup"><span data-stu-id="319f4-101">Update deviceCompliancePolicySettingStateSummary</span></span>

> <span data-ttu-id="319f4-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="319f4-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="319f4-103">Actualice las propiedades de un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="319f4-103">Update the properties of a [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="319f4-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="319f4-104">Prerequisites</span></span>
<span data-ttu-id="319f4-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="319f4-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="319f4-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="319f4-107">Permission type</span></span>|<span data-ttu-id="319f4-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="319f4-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="319f4-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="319f4-109">Delegated (work or school account)</span></span>|<span data-ttu-id="319f4-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="319f4-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="319f4-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="319f4-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="319f4-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="319f4-112">Not supported.</span></span>|
|<span data-ttu-id="319f4-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="319f4-113">Application</span></span>|<span data-ttu-id="319f4-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="319f4-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="319f4-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="319f4-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="319f4-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="319f4-116">Request headers</span></span>
|<span data-ttu-id="319f4-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="319f4-117">Header</span></span>|<span data-ttu-id="319f4-118">Valor</span><span class="sxs-lookup"><span data-stu-id="319f4-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="319f4-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="319f4-119">Authorization</span></span>|<span data-ttu-id="319f4-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="319f4-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="319f4-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="319f4-121">Accept</span></span>|<span data-ttu-id="319f4-122">application/json</span><span class="sxs-lookup"><span data-stu-id="319f4-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="319f4-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="319f4-123">Request body</span></span>
<span data-ttu-id="319f4-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="319f4-124">In the request body, supply a JSON representation for the [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object.</span></span>

<span data-ttu-id="319f4-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="319f4-125">The following table shows the properties that are required when you create the [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md).</span></span>

|<span data-ttu-id="319f4-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="319f4-126">Property</span></span>|<span data-ttu-id="319f4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="319f4-127">Type</span></span>|<span data-ttu-id="319f4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="319f4-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="319f4-129">id</span><span class="sxs-lookup"><span data-stu-id="319f4-129">id</span></span>|<span data-ttu-id="319f4-130">String</span><span class="sxs-lookup"><span data-stu-id="319f4-130">String</span></span>|<span data-ttu-id="319f4-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="319f4-131">Key of the entity.</span></span>|
|<span data-ttu-id="319f4-132">ajustes</span><span class="sxs-lookup"><span data-stu-id="319f4-132">setting</span></span>|<span data-ttu-id="319f4-133">String</span><span class="sxs-lookup"><span data-stu-id="319f4-133">String</span></span>|<span data-ttu-id="319f4-134">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="319f4-134">The setting class name and property name.</span></span>|
|<span data-ttu-id="319f4-135">settingName</span><span class="sxs-lookup"><span data-stu-id="319f4-135">settingName</span></span>|<span data-ttu-id="319f4-136">String</span><span class="sxs-lookup"><span data-stu-id="319f4-136">String</span></span>|<span data-ttu-id="319f4-137">Nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="319f4-137">Name of the setting.</span></span>|
|<span data-ttu-id="319f4-138">platformType</span><span class="sxs-lookup"><span data-stu-id="319f4-138">platformType</span></span>|[<span data-ttu-id="319f4-139">policyPlatformType</span><span class="sxs-lookup"><span data-stu-id="319f4-139">policyPlatformType</span></span>](../resources/intune_deviceconfig_policyplatformtype.md)|<span data-ttu-id="319f4-140">Plataforma de configuración.</span><span class="sxs-lookup"><span data-stu-id="319f4-140">Setting platform.</span></span> <span data-ttu-id="319f4-141">Los valores posibles son: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile` y `all`.</span><span class="sxs-lookup"><span data-stu-id="319f4-141">Possible values are: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`, `all`.</span></span>|
|<span data-ttu-id="319f4-142">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="319f4-142">unknownDeviceCount</span></span>|<span data-ttu-id="319f4-143">Int32</span><span class="sxs-lookup"><span data-stu-id="319f4-143">Int32</span></span>|<span data-ttu-id="319f4-144">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="319f4-144">Number of unknown devices</span></span>|
|<span data-ttu-id="319f4-145">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="319f4-145">notApplicableDeviceCount</span></span>|<span data-ttu-id="319f4-146">Int32</span><span class="sxs-lookup"><span data-stu-id="319f4-146">Int32</span></span>|<span data-ttu-id="319f4-147">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="319f4-147">Number of not applicable devices</span></span>|
|<span data-ttu-id="319f4-148">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="319f4-148">compliantDeviceCount</span></span>|<span data-ttu-id="319f4-149">Int32</span><span class="sxs-lookup"><span data-stu-id="319f4-149">Int32</span></span>|<span data-ttu-id="319f4-150">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="319f4-150">Number of compliant devices</span></span>|
|<span data-ttu-id="319f4-151">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="319f4-151">remediatedDeviceCount</span></span>|<span data-ttu-id="319f4-152">Int32</span><span class="sxs-lookup"><span data-stu-id="319f4-152">Int32</span></span>|<span data-ttu-id="319f4-153">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="319f4-153">Number of remediated devices</span></span>|
|<span data-ttu-id="319f4-154">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="319f4-154">nonCompliantDeviceCount</span></span>|<span data-ttu-id="319f4-155">Int32</span><span class="sxs-lookup"><span data-stu-id="319f4-155">Int32</span></span>|<span data-ttu-id="319f4-156">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="319f4-156">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="319f4-157">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="319f4-157">errorDeviceCount</span></span>|<span data-ttu-id="319f4-158">Int32</span><span class="sxs-lookup"><span data-stu-id="319f4-158">Int32</span></span>|<span data-ttu-id="319f4-159">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="319f4-159">Number of error devices</span></span>|
|<span data-ttu-id="319f4-160">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="319f4-160">conflictDeviceCount</span></span>|<span data-ttu-id="319f4-161">Int32</span><span class="sxs-lookup"><span data-stu-id="319f4-161">Int32</span></span>|<span data-ttu-id="319f4-162">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="319f4-162">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="319f4-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="319f4-163">Response</span></span>
<span data-ttu-id="319f4-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="319f4-164">If successful, this method returns a `200 OK` response code and an updated [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="319f4-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="319f4-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="319f4-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="319f4-166">Request</span></span>
<span data-ttu-id="319f4-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="319f4-167">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}
Content-type: application/json
Content-length: 391

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingStateSummary",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "platformType": "iOS",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```

### <a name="response"></a><span data-ttu-id="319f4-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="319f4-168">Response</span></span>
<span data-ttu-id="319f4-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="319f4-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 440

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingStateSummary",
  "id": "7474d6d5-d6d5-7474-d5d6-7474d5d67474",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "platformType": "iOS",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```



