# <a name="create-devicecompliancepolicysettingstatesummary"></a><span data-ttu-id="2bfe6-101">Crear deviceCompliancePolicySettingStateSummary</span><span class="sxs-lookup"><span data-stu-id="2bfe6-101">Create deviceCompliancePolicySettingStateSummary</span></span>

> <span data-ttu-id="2bfe6-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2bfe6-103">Cree un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="2bfe6-103">Create a new [plannerBucket](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2bfe6-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2bfe6-104">Prerequisites</span></span>
<span data-ttu-id="2bfe6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2bfe6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2bfe6-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2bfe6-107">Permission type</span></span>|<span data-ttu-id="2bfe6-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2bfe6-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2bfe6-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2bfe6-109">Delegated (work or school account)</span></span>|<span data-ttu-id="2bfe6-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2bfe6-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2bfe6-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2bfe6-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2bfe6-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-112">Not supported.</span></span>|
|<span data-ttu-id="2bfe6-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2bfe6-113">Application</span></span>|<span data-ttu-id="2bfe6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2bfe6-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2bfe6-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicySettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="2bfe6-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2bfe6-116">Request headers</span></span>
|<span data-ttu-id="2bfe6-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2bfe6-117">Header</span></span>|<span data-ttu-id="2bfe6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2bfe6-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2bfe6-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="2bfe6-119">Authorization</span></span>|<span data-ttu-id="2bfe6-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="2bfe6-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2bfe6-121">Accept</span></span>|<span data-ttu-id="2bfe6-122">application/json</span><span class="sxs-lookup"><span data-stu-id="2bfe6-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2bfe6-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2bfe6-123">Request body</span></span>
<span data-ttu-id="2bfe6-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceCompliancePolicySettingStateSummary.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="2bfe6-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceCompliancePolicySettingStateSummary.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="2bfe6-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2bfe6-126">Property</span></span>|<span data-ttu-id="2bfe6-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="2bfe6-127">Type</span></span>|<span data-ttu-id="2bfe6-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="2bfe6-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2bfe6-129">ajustes</span><span class="sxs-lookup"><span data-stu-id="2bfe6-129">setting</span></span>|<span data-ttu-id="2bfe6-130">String</span><span class="sxs-lookup"><span data-stu-id="2bfe6-130">String</span></span>|<span data-ttu-id="2bfe6-131">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-131">The setting class name and property name.</span></span>|
|<span data-ttu-id="2bfe6-132">settingName</span><span class="sxs-lookup"><span data-stu-id="2bfe6-132">settingName</span></span>|<span data-ttu-id="2bfe6-133">String</span><span class="sxs-lookup"><span data-stu-id="2bfe6-133">String</span></span>|<span data-ttu-id="2bfe6-134">Nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-134">Name of the setting.</span></span>|
|<span data-ttu-id="2bfe6-135">platformType</span><span class="sxs-lookup"><span data-stu-id="2bfe6-135">PlatformType</span></span>|<span data-ttu-id="2bfe6-136">String</span><span class="sxs-lookup"><span data-stu-id="2bfe6-136">String</span></span>|<span data-ttu-id="2bfe6-137">Plataforma de configuración Los valores posibles son: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `all`.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-137">Setting platform Possible values are: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `all`.</span></span>|
|<span data-ttu-id="2bfe6-138">id</span><span class="sxs-lookup"><span data-stu-id="2bfe6-138">id</span></span>|<span data-ttu-id="2bfe6-139">String</span><span class="sxs-lookup"><span data-stu-id="2bfe6-139">String</span></span>|<span data-ttu-id="2bfe6-140">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-140">Key of the setting.</span></span>|
|<span data-ttu-id="2bfe6-141">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="2bfe6-141">unknownDeviceCount</span></span>|<span data-ttu-id="2bfe6-142">Int32</span><span class="sxs-lookup"><span data-stu-id="2bfe6-142">Int32</span></span>|<span data-ttu-id="2bfe6-143">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="2bfe6-143">Number of unknown devices</span></span>|
|<span data-ttu-id="2bfe6-144">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="2bfe6-144">notApplicableDeviceCount</span></span>|<span data-ttu-id="2bfe6-145">Int32</span><span class="sxs-lookup"><span data-stu-id="2bfe6-145">Int32</span></span>|<span data-ttu-id="2bfe6-146">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="2bfe6-146">Number of not applicable devices</span></span>|
|<span data-ttu-id="2bfe6-147">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="2bfe6-147">compliantDeviceCount</span></span>|<span data-ttu-id="2bfe6-148">Int32</span><span class="sxs-lookup"><span data-stu-id="2bfe6-148">Int32</span></span>|<span data-ttu-id="2bfe6-149">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="2bfe6-149">Number of compliant devices</span></span>|
|<span data-ttu-id="2bfe6-150">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="2bfe6-150">remediatedDeviceCount</span></span>|<span data-ttu-id="2bfe6-151">Int32</span><span class="sxs-lookup"><span data-stu-id="2bfe6-151">Int32</span></span>|<span data-ttu-id="2bfe6-152">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="2bfe6-152">Number of remediated devices</span></span>|
|<span data-ttu-id="2bfe6-153">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="2bfe6-153">nonCompliantDeviceCount</span></span>|<span data-ttu-id="2bfe6-154">Int32</span><span class="sxs-lookup"><span data-stu-id="2bfe6-154">Int32</span></span>|<span data-ttu-id="2bfe6-155">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="2bfe6-155">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="2bfe6-156">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="2bfe6-156">errorDeviceCount</span></span>|<span data-ttu-id="2bfe6-157">Int32</span><span class="sxs-lookup"><span data-stu-id="2bfe6-157">Int32</span></span>|<span data-ttu-id="2bfe6-158">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="2bfe6-158">Number of error devices</span></span>|
|<span data-ttu-id="2bfe6-159">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="2bfe6-159">conflictDeviceCount</span></span>|<span data-ttu-id="2bfe6-160">Int32</span><span class="sxs-lookup"><span data-stu-id="2bfe6-160">Int32</span></span>|<span data-ttu-id="2bfe6-161">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="2bfe6-161">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="2bfe6-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bfe6-162">Response</span></span>
<span data-ttu-id="2bfe6-163">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-163">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2bfe6-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2bfe6-164">Example</span></span>
### <a name="request"></a><span data-ttu-id="2bfe6-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2bfe6-165">Request</span></span>
<span data-ttu-id="2bfe6-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-166">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries
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

### <a name="response"></a><span data-ttu-id="2bfe6-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2bfe6-167">Response</span></span>
<span data-ttu-id="2bfe6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2bfe6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 440

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingStateSummary",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "platformType": "iOS",
  "id": "7474d6d5-d6d5-7474-d5d6-7474d5d67474",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```



