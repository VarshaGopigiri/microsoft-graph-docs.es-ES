# <a name="update-devicecompliancepolicydevicestatesummary"></a><span data-ttu-id="ca600-101">Actualizar deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="ca600-101">Update deviceCompliancePolicyDeviceStateSummary</span></span>

> <span data-ttu-id="ca600-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ca600-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ca600-103">Actualice las propiedades de un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="ca600-103">Update the properties of a [calendar](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ca600-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ca600-104">Prerequisites</span></span>
<span data-ttu-id="ca600-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ca600-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ca600-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ca600-107">Permission type</span></span>|<span data-ttu-id="ca600-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ca600-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ca600-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ca600-109">Delegated (work or school account)</span></span>|<span data-ttu-id="ca600-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ca600-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ca600-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ca600-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ca600-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ca600-112">Not supported.</span></span>|
|<span data-ttu-id="ca600-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ca600-113">Application</span></span>|<span data-ttu-id="ca600-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ca600-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ca600-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ca600-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicyDeviceStateSummary
```

## <a name="request-headers"></a><span data-ttu-id="ca600-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ca600-116">Request headers</span></span>
|<span data-ttu-id="ca600-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca600-117">Header</span></span>|<span data-ttu-id="ca600-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ca600-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ca600-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="ca600-119">Authorization</span></span>|<span data-ttu-id="ca600-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ca600-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="ca600-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ca600-121">Accept</span></span>|<span data-ttu-id="ca600-122">application/json</span><span class="sxs-lookup"><span data-stu-id="ca600-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ca600-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ca600-123">Request body</span></span>
<span data-ttu-id="ca600-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="ca600-124">In the request body, supply a JSON representation of [ContactFolder](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) object.</span></span>

<span data-ttu-id="ca600-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="ca600-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="ca600-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ca600-126">Property</span></span>|<span data-ttu-id="ca600-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="ca600-127">Type</span></span>|<span data-ttu-id="ca600-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ca600-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ca600-129">inGracePeriodCount</span><span class="sxs-lookup"><span data-stu-id="ca600-129">inGracePeriodCount</span></span>|<span data-ttu-id="ca600-130">Int32</span><span class="sxs-lookup"><span data-stu-id="ca600-130">Int32</span></span>|<span data-ttu-id="ca600-131">Número de dispositivos que se encuentran en el período de gracia</span><span class="sxs-lookup"><span data-stu-id="ca600-131">Number of devices that are in grace period</span></span>|
|<span data-ttu-id="ca600-132">configManagerCount</span><span class="sxs-lookup"><span data-stu-id="ca600-132">configManagerCount</span></span>|<span data-ttu-id="ca600-133">Int32</span><span class="sxs-lookup"><span data-stu-id="ca600-133">Int32</span></span>|<span data-ttu-id="ca600-134">Número de dispositivos cuyo cumplimiento lo administra System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ca600-134">Number of devices that have compliance managed by System Center Configuration Manager</span></span>|
|<span data-ttu-id="ca600-135">id</span><span class="sxs-lookup"><span data-stu-id="ca600-135">id</span></span>|<span data-ttu-id="ca600-136">String</span><span class="sxs-lookup"><span data-stu-id="ca600-136">String</span></span>|<span data-ttu-id="ca600-137">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ca600-137">Key of the setting.</span></span>|
|<span data-ttu-id="ca600-138">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ca600-138">unknownDeviceCount</span></span>|<span data-ttu-id="ca600-139">Int32</span><span class="sxs-lookup"><span data-stu-id="ca600-139">Int32</span></span>|<span data-ttu-id="ca600-140">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="ca600-140">Number of unknown devices</span></span>|
|<span data-ttu-id="ca600-141">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ca600-141">notApplicableDeviceCount</span></span>|<span data-ttu-id="ca600-142">Int32</span><span class="sxs-lookup"><span data-stu-id="ca600-142">Int32</span></span>|<span data-ttu-id="ca600-143">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="ca600-143">Number of not applicable devices</span></span>|
|<span data-ttu-id="ca600-144">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ca600-144">compliantDeviceCount</span></span>|<span data-ttu-id="ca600-145">Int32</span><span class="sxs-lookup"><span data-stu-id="ca600-145">Int32</span></span>|<span data-ttu-id="ca600-146">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="ca600-146">Number of compliant devices</span></span>|
|<span data-ttu-id="ca600-147">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ca600-147">remediatedDeviceCount</span></span>|<span data-ttu-id="ca600-148">Int32</span><span class="sxs-lookup"><span data-stu-id="ca600-148">Int32</span></span>|<span data-ttu-id="ca600-149">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="ca600-149">Number of remediated devices</span></span>|
|<span data-ttu-id="ca600-150">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ca600-150">nonCompliantDeviceCount</span></span>|<span data-ttu-id="ca600-151">Int32</span><span class="sxs-lookup"><span data-stu-id="ca600-151">Int32</span></span>|<span data-ttu-id="ca600-152">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="ca600-152">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="ca600-153">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ca600-153">errorDeviceCount</span></span>|<span data-ttu-id="ca600-154">Int32</span><span class="sxs-lookup"><span data-stu-id="ca600-154">Int32</span></span>|<span data-ttu-id="ca600-155">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="ca600-155">Number of error devices</span></span>|
|<span data-ttu-id="ca600-156">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ca600-156">conflictDeviceCount</span></span>|<span data-ttu-id="ca600-157">Int32</span><span class="sxs-lookup"><span data-stu-id="ca600-157">Int32</span></span>|<span data-ttu-id="ca600-158">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="ca600-158">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="ca600-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca600-159">Response</span></span>
<span data-ttu-id="ca600-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca600-160">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_deviceconfig_devicecompliancepolicydevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ca600-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ca600-161">Example</span></span>
### <a name="request"></a><span data-ttu-id="ca600-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ca600-162">Request</span></span>
<span data-ttu-id="ca600-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ca600-163">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="ca600-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca600-164">Response</span></span>
<span data-ttu-id="ca600-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ca600-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



