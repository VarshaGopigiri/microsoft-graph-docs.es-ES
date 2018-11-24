# <a name="update-deviceconfigurationdevicestatesummary"></a><span data-ttu-id="67efe-101">Actualizar deviceConfigurationDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="67efe-101">Update deviceConfigurationDeviceStateSummary</span></span>

> <span data-ttu-id="67efe-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="67efe-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="67efe-103">Actualice las propiedades de un objeto [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="67efe-103">Update the properties of a [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="67efe-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="67efe-104">Prerequisites</span></span>
<span data-ttu-id="67efe-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="67efe-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="67efe-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="67efe-107">Permission type</span></span>|<span data-ttu-id="67efe-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="67efe-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="67efe-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="67efe-109">Delegated (work or school account)</span></span>|<span data-ttu-id="67efe-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="67efe-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="67efe-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="67efe-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="67efe-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="67efe-112">Not supported.</span></span>|
|<span data-ttu-id="67efe-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="67efe-113">Application</span></span>|<span data-ttu-id="67efe-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="67efe-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="67efe-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="67efe-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurationDeviceStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="67efe-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="67efe-116">Request headers</span></span>
|<span data-ttu-id="67efe-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="67efe-117">Header</span></span>|<span data-ttu-id="67efe-118">Valor</span><span class="sxs-lookup"><span data-stu-id="67efe-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="67efe-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="67efe-119">Authorization</span></span>|<span data-ttu-id="67efe-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="67efe-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="67efe-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="67efe-121">Accept</span></span>|<span data-ttu-id="67efe-122">application/json</span><span class="sxs-lookup"><span data-stu-id="67efe-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="67efe-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="67efe-123">Request body</span></span>
<span data-ttu-id="67efe-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="67efe-124">In the request body, supply a JSON representation for the [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md) object.</span></span>

<span data-ttu-id="67efe-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="67efe-125">The following table shows the properties that are required when you create the [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md).</span></span>

|<span data-ttu-id="67efe-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67efe-126">Property</span></span>|<span data-ttu-id="67efe-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="67efe-127">Type</span></span>|<span data-ttu-id="67efe-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="67efe-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="67efe-129">id</span><span class="sxs-lookup"><span data-stu-id="67efe-129">id</span></span>|<span data-ttu-id="67efe-130">String</span><span class="sxs-lookup"><span data-stu-id="67efe-130">String</span></span>|<span data-ttu-id="67efe-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="67efe-131">Key of the entity.</span></span>|
|<span data-ttu-id="67efe-132">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="67efe-132">unknownDeviceCount</span></span>|<span data-ttu-id="67efe-133">Int32</span><span class="sxs-lookup"><span data-stu-id="67efe-133">Int32</span></span>|<span data-ttu-id="67efe-134">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="67efe-134">Number of unknown devices</span></span>|
|<span data-ttu-id="67efe-135">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="67efe-135">notApplicableDeviceCount</span></span>|<span data-ttu-id="67efe-136">Int32</span><span class="sxs-lookup"><span data-stu-id="67efe-136">Int32</span></span>|<span data-ttu-id="67efe-137">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="67efe-137">Number of not applicable devices</span></span>|
|<span data-ttu-id="67efe-138">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="67efe-138">compliantDeviceCount</span></span>|<span data-ttu-id="67efe-139">Int32</span><span class="sxs-lookup"><span data-stu-id="67efe-139">Int32</span></span>|<span data-ttu-id="67efe-140">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="67efe-140">Number of compliant devices</span></span>|
|<span data-ttu-id="67efe-141">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="67efe-141">remediatedDeviceCount</span></span>|<span data-ttu-id="67efe-142">Int32</span><span class="sxs-lookup"><span data-stu-id="67efe-142">Int32</span></span>|<span data-ttu-id="67efe-143">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="67efe-143">Number of remediated devices</span></span>|
|<span data-ttu-id="67efe-144">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="67efe-144">nonCompliantDeviceCount</span></span>|<span data-ttu-id="67efe-145">Int32</span><span class="sxs-lookup"><span data-stu-id="67efe-145">Int32</span></span>|<span data-ttu-id="67efe-146">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="67efe-146">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="67efe-147">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="67efe-147">errorDeviceCount</span></span>|<span data-ttu-id="67efe-148">Int32</span><span class="sxs-lookup"><span data-stu-id="67efe-148">Int32</span></span>|<span data-ttu-id="67efe-149">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="67efe-149">Number of error devices</span></span>|
|<span data-ttu-id="67efe-150">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="67efe-150">conflictDeviceCount</span></span>|<span data-ttu-id="67efe-151">Int32</span><span class="sxs-lookup"><span data-stu-id="67efe-151">Int32</span></span>|<span data-ttu-id="67efe-152">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="67efe-152">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="67efe-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67efe-153">Response</span></span>
<span data-ttu-id="67efe-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="67efe-154">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationDeviceStateSummary](../resources/intune_deviceconfig_deviceconfigurationdevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="67efe-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="67efe-155">Example</span></span>
### <a name="request"></a><span data-ttu-id="67efe-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="67efe-156">Request</span></span>
<span data-ttu-id="67efe-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="67efe-157">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurationDeviceStateSummaries
Content-type: application/json
Content-length: 290

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStateSummary",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```

### <a name="response"></a><span data-ttu-id="67efe-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="67efe-158">Response</span></span>
<span data-ttu-id="67efe-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="67efe-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 339

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStateSummary",
  "id": "5db26f5a-6f5a-5db2-5a6f-b25d5a6fb25d",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```



