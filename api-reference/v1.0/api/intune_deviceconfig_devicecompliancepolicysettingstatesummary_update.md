# <a name="update-devicecompliancepolicysettingstatesummary"></a><span data-ttu-id="9791b-101">Actualizar deviceCompliancePolicySettingStateSummary</span><span class="sxs-lookup"><span data-stu-id="9791b-101">Update deviceCompliancePolicySettingStateSummary</span></span>

> <span data-ttu-id="9791b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9791b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9791b-103">Actualice las propiedades de un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="9791b-103">Update the properties of a [calendar](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9791b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9791b-104">Prerequisites</span></span>
<span data-ttu-id="9791b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9791b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9791b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9791b-107">Permission type</span></span>|<span data-ttu-id="9791b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9791b-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9791b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9791b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="9791b-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9791b-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9791b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9791b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9791b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9791b-112">Not supported.</span></span>|
|<span data-ttu-id="9791b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9791b-113">Application</span></span>|<span data-ttu-id="9791b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9791b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9791b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9791b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="9791b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9791b-116">Request headers</span></span>
|<span data-ttu-id="9791b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9791b-117">Header</span></span>|<span data-ttu-id="9791b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9791b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9791b-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="9791b-119">Authorization</span></span>|<span data-ttu-id="9791b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9791b-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="9791b-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9791b-121">Accept</span></span>|<span data-ttu-id="9791b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="9791b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9791b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9791b-123">Request body</span></span>
<span data-ttu-id="9791b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="9791b-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object.</span></span>

<span data-ttu-id="9791b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="9791b-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="9791b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9791b-126">Property</span></span>|<span data-ttu-id="9791b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="9791b-127">Type</span></span>|<span data-ttu-id="9791b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="9791b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9791b-129">ajustes</span><span class="sxs-lookup"><span data-stu-id="9791b-129">setting</span></span>|<span data-ttu-id="9791b-130">String</span><span class="sxs-lookup"><span data-stu-id="9791b-130">String</span></span>|<span data-ttu-id="9791b-131">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9791b-131">The setting class name and property name.</span></span>|
|<span data-ttu-id="9791b-132">settingName</span><span class="sxs-lookup"><span data-stu-id="9791b-132">settingName</span></span>|<span data-ttu-id="9791b-133">String</span><span class="sxs-lookup"><span data-stu-id="9791b-133">String</span></span>|<span data-ttu-id="9791b-134">Nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="9791b-134">Name of the setting.</span></span>|
|<span data-ttu-id="9791b-135">platformType</span><span class="sxs-lookup"><span data-stu-id="9791b-135">PlatformType</span></span>|<span data-ttu-id="9791b-136">String</span><span class="sxs-lookup"><span data-stu-id="9791b-136">String</span></span>|<span data-ttu-id="9791b-137">Plataforma de configuración Los valores posibles son: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater` y `all`.</span><span class="sxs-lookup"><span data-stu-id="9791b-137">Setting platform Possible values are: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `all`.</span></span>|
|<span data-ttu-id="9791b-138">id</span><span class="sxs-lookup"><span data-stu-id="9791b-138">id</span></span>|<span data-ttu-id="9791b-139">String</span><span class="sxs-lookup"><span data-stu-id="9791b-139">String</span></span>|<span data-ttu-id="9791b-140">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9791b-140">Key of the setting.</span></span>|
|<span data-ttu-id="9791b-141">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9791b-141">unknownDeviceCount</span></span>|<span data-ttu-id="9791b-142">Int32</span><span class="sxs-lookup"><span data-stu-id="9791b-142">Int32</span></span>|<span data-ttu-id="9791b-143">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="9791b-143">Number of unknown devices</span></span>|
|<span data-ttu-id="9791b-144">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9791b-144">notApplicableDeviceCount</span></span>|<span data-ttu-id="9791b-145">Int32</span><span class="sxs-lookup"><span data-stu-id="9791b-145">Int32</span></span>|<span data-ttu-id="9791b-146">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="9791b-146">Number of not applicable devices</span></span>|
|<span data-ttu-id="9791b-147">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9791b-147">compliantDeviceCount</span></span>|<span data-ttu-id="9791b-148">Int32</span><span class="sxs-lookup"><span data-stu-id="9791b-148">Int32</span></span>|<span data-ttu-id="9791b-149">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="9791b-149">Number of compliant devices</span></span>|
|<span data-ttu-id="9791b-150">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9791b-150">remediatedDeviceCount</span></span>|<span data-ttu-id="9791b-151">Int32</span><span class="sxs-lookup"><span data-stu-id="9791b-151">Int32</span></span>|<span data-ttu-id="9791b-152">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="9791b-152">Number of remediated devices</span></span>|
|<span data-ttu-id="9791b-153">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9791b-153">nonCompliantDeviceCount</span></span>|<span data-ttu-id="9791b-154">Int32</span><span class="sxs-lookup"><span data-stu-id="9791b-154">Int32</span></span>|<span data-ttu-id="9791b-155">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="9791b-155">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="9791b-156">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9791b-156">errorDeviceCount</span></span>|<span data-ttu-id="9791b-157">Int32</span><span class="sxs-lookup"><span data-stu-id="9791b-157">Int32</span></span>|<span data-ttu-id="9791b-158">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="9791b-158">Number of error devices</span></span>|
|<span data-ttu-id="9791b-159">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9791b-159">conflictDeviceCount</span></span>|<span data-ttu-id="9791b-160">Int32</span><span class="sxs-lookup"><span data-stu-id="9791b-160">Int32</span></span>|<span data-ttu-id="9791b-161">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="9791b-161">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="9791b-162">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9791b-162">Response</span></span>
<span data-ttu-id="9791b-163">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9791b-163">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9791b-164">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9791b-164">Example</span></span>
### <a name="request"></a><span data-ttu-id="9791b-165">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9791b-165">Request</span></span>
<span data-ttu-id="9791b-166">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9791b-166">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}
Content-type: application/json
Content-length: 311

{
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

### <a name="response"></a><span data-ttu-id="9791b-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9791b-167">Response</span></span>
<span data-ttu-id="9791b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9791b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



