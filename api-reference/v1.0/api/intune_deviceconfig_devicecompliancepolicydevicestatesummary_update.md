# <a name="update-devicecompliancepolicydevicestatesummary"></a><span data-ttu-id="54993-101">Actualizar deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="54993-101">Update deviceCompliancePolicyDeviceStateSummary</span></span>

> <span data-ttu-id="54993-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="54993-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="54993-103">Actualice las propiedades de un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="54993-103">Update the properties of a [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="54993-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="54993-104">Prerequisites</span></span>
<span data-ttu-id="54993-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="54993-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="54993-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54993-107">Permission type</span></span>|<span data-ttu-id="54993-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54993-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="54993-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54993-109">Delegated (work or school account)</span></span>|<span data-ttu-id="54993-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="54993-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="54993-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54993-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="54993-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54993-112">Not supported.</span></span>|
|<span data-ttu-id="54993-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54993-113">Application</span></span>|<span data-ttu-id="54993-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54993-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="54993-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54993-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicyDeviceStateSummary
```

## <a name="request-headers"></a><span data-ttu-id="54993-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54993-116">Request headers</span></span>
|<span data-ttu-id="54993-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54993-117">Header</span></span>|<span data-ttu-id="54993-118">Valor</span><span class="sxs-lookup"><span data-stu-id="54993-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="54993-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="54993-119">Authorization</span></span>|<span data-ttu-id="54993-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="54993-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="54993-121">Accept</span><span class="sxs-lookup"><span data-stu-id="54993-121">Accept</span></span>|<span data-ttu-id="54993-122">application/json</span><span class="sxs-lookup"><span data-stu-id="54993-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="54993-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54993-123">Request body</span></span>
<span data-ttu-id="54993-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="54993-124">In the request body, supply a JSON representation for the [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) object.</span></span>

<span data-ttu-id="54993-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="54993-125">The following table shows the properties that are required when you create the [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md).</span></span>

|<span data-ttu-id="54993-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="54993-126">Property</span></span>|<span data-ttu-id="54993-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="54993-127">Type</span></span>|<span data-ttu-id="54993-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="54993-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="54993-129">inGracePeriodCount</span><span class="sxs-lookup"><span data-stu-id="54993-129">inGracePeriodCount</span></span>|<span data-ttu-id="54993-130">Int32</span><span class="sxs-lookup"><span data-stu-id="54993-130">Int32</span></span>|<span data-ttu-id="54993-131">Número de dispositivos que se encuentran en el período de gracia</span><span class="sxs-lookup"><span data-stu-id="54993-131">Number of devices that are in grace period</span></span>|
|<span data-ttu-id="54993-132">configManagerCount</span><span class="sxs-lookup"><span data-stu-id="54993-132">configManagerCount</span></span>|<span data-ttu-id="54993-133">Int32</span><span class="sxs-lookup"><span data-stu-id="54993-133">Int32</span></span>|<span data-ttu-id="54993-134">Número de dispositivos cuyo cumplimiento lo administra System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="54993-134">Number of devices that have compliance managed by System Center Configuration Manager</span></span>|
|<span data-ttu-id="54993-135">id</span><span class="sxs-lookup"><span data-stu-id="54993-135">id</span></span>|<span data-ttu-id="54993-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="54993-136">String</span></span>|<span data-ttu-id="54993-137">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="54993-137">Key of the entity.</span></span>|
|<span data-ttu-id="54993-138">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="54993-138">unknownDeviceCount</span></span>|<span data-ttu-id="54993-139">Int32</span><span class="sxs-lookup"><span data-stu-id="54993-139">Int32</span></span>|<span data-ttu-id="54993-140">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="54993-140">Number of unknown devices</span></span>|
|<span data-ttu-id="54993-141">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="54993-141">notApplicableDeviceCount</span></span>|<span data-ttu-id="54993-142">Int32</span><span class="sxs-lookup"><span data-stu-id="54993-142">Int32</span></span>|<span data-ttu-id="54993-143">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="54993-143">Number of not applicable devices</span></span>|
|<span data-ttu-id="54993-144">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="54993-144">compliantDeviceCount</span></span>|<span data-ttu-id="54993-145">Int32</span><span class="sxs-lookup"><span data-stu-id="54993-145">Int32</span></span>|<span data-ttu-id="54993-146">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="54993-146">Number of compliant devices</span></span>|
|<span data-ttu-id="54993-147">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="54993-147">remediatedDeviceCount</span></span>|<span data-ttu-id="54993-148">Int32</span><span class="sxs-lookup"><span data-stu-id="54993-148">Int32</span></span>|<span data-ttu-id="54993-149">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="54993-149">Number of remediated devices</span></span>|
|<span data-ttu-id="54993-150">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="54993-150">nonCompliantDeviceCount</span></span>|<span data-ttu-id="54993-151">Int32</span><span class="sxs-lookup"><span data-stu-id="54993-151">Int32</span></span>|<span data-ttu-id="54993-152">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="54993-152">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="54993-153">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="54993-153">errorDeviceCount</span></span>|<span data-ttu-id="54993-154">Int32</span><span class="sxs-lookup"><span data-stu-id="54993-154">Int32</span></span>|<span data-ttu-id="54993-155">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="54993-155">Number of error devices</span></span>|
|<span data-ttu-id="54993-156">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="54993-156">conflictDeviceCount</span></span>|<span data-ttu-id="54993-157">Int32</span><span class="sxs-lookup"><span data-stu-id="54993-157">Int32</span></span>|<span data-ttu-id="54993-158">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="54993-158">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="54993-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54993-159">Response</span></span>
<span data-ttu-id="54993-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54993-160">If successful, this method returns a `200 OK` response code and an updated [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="54993-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54993-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="54993-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54993-162">Request</span></span>
<span data-ttu-id="54993-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54993-163">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicyDeviceStateSummary
Content-type: application/json
Content-length: 270

{
  "inGracePeriodCount": 2,
  "configManagerCount": 2,
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```

### <a name="response"></a><span data-ttu-id="54993-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54993-164">Response</span></span>
<span data-ttu-id="54993-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="54993-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 398

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyDeviceStateSummary",
  "inGracePeriodCount": 2,
  "configManagerCount": 2,
  "id": "8c4de8a7-e8a7-8c4d-a7e8-4d8ca7e84d8c",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```








