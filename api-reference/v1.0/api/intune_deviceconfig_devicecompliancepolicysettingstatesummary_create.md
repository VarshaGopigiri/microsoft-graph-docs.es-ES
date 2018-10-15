# <a name="create-devicecompliancepolicysettingstatesummary"></a><span data-ttu-id="6ac55-101">Crear deviceCompliancePolicySettingStateSummary</span><span class="sxs-lookup"><span data-stu-id="6ac55-101">Create deviceCompliancePolicySettingStateSummary</span></span>

> <span data-ttu-id="6ac55-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6ac55-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6ac55-103">Cree un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="6ac55-103">Create a new [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6ac55-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6ac55-104">Prerequisites</span></span>
<span data-ttu-id="6ac55-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6ac55-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6ac55-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ac55-107">Permission type</span></span>|<span data-ttu-id="6ac55-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ac55-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6ac55-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ac55-109">Delegated (work or school account)</span></span>|<span data-ttu-id="6ac55-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6ac55-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="6ac55-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ac55-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6ac55-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ac55-112">Not supported.</span></span>|
|<span data-ttu-id="6ac55-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ac55-113">Application</span></span>|<span data-ttu-id="6ac55-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ac55-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6ac55-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ac55-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicySettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="6ac55-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ac55-116">Request headers</span></span>
|<span data-ttu-id="6ac55-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ac55-117">Header</span></span>|<span data-ttu-id="6ac55-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ac55-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6ac55-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="6ac55-119">Authorization</span></span>|<span data-ttu-id="6ac55-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6ac55-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6ac55-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6ac55-121">Accept</span></span>|<span data-ttu-id="6ac55-122">application/json</span><span class="sxs-lookup"><span data-stu-id="6ac55-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ac55-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ac55-123">Request body</span></span>
<span data-ttu-id="6ac55-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceCompliancePolicySettingStateSummary.</span><span class="sxs-lookup"><span data-stu-id="6ac55-124">In the request body, supply a JSON representation for the deviceCompliancePolicySettingStateSummary object.</span></span>

<span data-ttu-id="6ac55-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceCompliancePolicySettingStateSummary.</span><span class="sxs-lookup"><span data-stu-id="6ac55-125">The following table shows the properties that are required when you create the deviceCompliancePolicySettingStateSummary.</span></span>

|<span data-ttu-id="6ac55-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6ac55-126">Property</span></span>|<span data-ttu-id="6ac55-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ac55-127">Type</span></span>|<span data-ttu-id="6ac55-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ac55-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6ac55-129">id.</span><span class="sxs-lookup"><span data-stu-id="6ac55-129">id</span></span>|<span data-ttu-id="6ac55-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ac55-130">String</span></span>|<span data-ttu-id="6ac55-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6ac55-131">Key of the entity.</span></span>|
|<span data-ttu-id="6ac55-132">configuración</span><span class="sxs-lookup"><span data-stu-id="6ac55-132">setting</span></span>|<span data-ttu-id="6ac55-133">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ac55-133">String</span></span>|<span data-ttu-id="6ac55-134">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6ac55-134">The setting class name and property name.</span></span>|
|<span data-ttu-id="6ac55-135">settingName</span><span class="sxs-lookup"><span data-stu-id="6ac55-135">settingName</span></span>|<span data-ttu-id="6ac55-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="6ac55-136">String</span></span>|<span data-ttu-id="6ac55-137">Nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="6ac55-137">Name of the setting.</span></span>|
|<span data-ttu-id="6ac55-138">platformType</span><span class="sxs-lookup"><span data-stu-id="6ac55-138">platformType</span></span>|[<span data-ttu-id="6ac55-139">policyPlatformType</span><span class="sxs-lookup"><span data-stu-id="6ac55-139">policyPlatformType</span></span>](../resources/intune_deviceconfig_policyplatformtype.md)|<span data-ttu-id="6ac55-140">Plataforma de configuración.</span><span class="sxs-lookup"><span data-stu-id="6ac55-140">Setting platform.</span></span> <span data-ttu-id="6ac55-141">Los valores posibles son: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile` y `all`.</span><span class="sxs-lookup"><span data-stu-id="6ac55-141">Possible values are: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`, `all`.</span></span>|
|<span data-ttu-id="6ac55-142">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6ac55-142">unknownDeviceCount</span></span>|<span data-ttu-id="6ac55-143">Int32</span><span class="sxs-lookup"><span data-stu-id="6ac55-143">Int32</span></span>|<span data-ttu-id="6ac55-144">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="6ac55-144">Number of unknown devices</span></span>|
|<span data-ttu-id="6ac55-145">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6ac55-145">notApplicableDeviceCount</span></span>|<span data-ttu-id="6ac55-146">Int32</span><span class="sxs-lookup"><span data-stu-id="6ac55-146">Int32</span></span>|<span data-ttu-id="6ac55-147">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="6ac55-147">Number of not applicable devices</span></span>|
|<span data-ttu-id="6ac55-148">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6ac55-148">compliantDeviceCount</span></span>|<span data-ttu-id="6ac55-149">Int32</span><span class="sxs-lookup"><span data-stu-id="6ac55-149">Int32</span></span>|<span data-ttu-id="6ac55-150">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="6ac55-150">Number of compliant devices</span></span>|
|<span data-ttu-id="6ac55-151">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6ac55-151">remediatedDeviceCount</span></span>|<span data-ttu-id="6ac55-152">Int32</span><span class="sxs-lookup"><span data-stu-id="6ac55-152">Int32</span></span>|<span data-ttu-id="6ac55-153">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="6ac55-153">Number of remediated devices</span></span>|
|<span data-ttu-id="6ac55-154">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6ac55-154">nonCompliantDeviceCount</span></span>|<span data-ttu-id="6ac55-155">Int32</span><span class="sxs-lookup"><span data-stu-id="6ac55-155">Int32</span></span>|<span data-ttu-id="6ac55-156">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="6ac55-156">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="6ac55-157">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6ac55-157">errorDeviceCount</span></span>|<span data-ttu-id="6ac55-158">Int32</span><span class="sxs-lookup"><span data-stu-id="6ac55-158">Int32</span></span>|<span data-ttu-id="6ac55-159">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="6ac55-159">Number of error devices</span></span>|
|<span data-ttu-id="6ac55-160">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6ac55-160">conflictDeviceCount</span></span>|<span data-ttu-id="6ac55-161">Int32</span><span class="sxs-lookup"><span data-stu-id="6ac55-161">Int32</span></span>|<span data-ttu-id="6ac55-162">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="6ac55-162">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="6ac55-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ac55-163">Response</span></span>
<span data-ttu-id="6ac55-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ac55-164">If successful, this method returns a `201 Created` response code and a [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6ac55-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ac55-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="6ac55-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ac55-166">Request</span></span>
<span data-ttu-id="6ac55-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ac55-167">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="6ac55-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ac55-168">Response</span></span>
<span data-ttu-id="6ac55-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ac55-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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








