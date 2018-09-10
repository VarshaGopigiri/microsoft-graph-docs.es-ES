# <a name="update-manageddeviceoverview"></a><span data-ttu-id="6ed74-101">Actualizar managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="6ed74-101">Update managedDeviceOverview</span></span>

> <span data-ttu-id="6ed74-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6ed74-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6ed74-103">Actualice las propiedades de un objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6ed74-103">Update the properties of a [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6ed74-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6ed74-104">Prerequisites</span></span>
<span data-ttu-id="6ed74-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6ed74-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6ed74-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ed74-107">Permission type</span></span>|<span data-ttu-id="6ed74-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ed74-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6ed74-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ed74-109">Delegated (work or school account)</span></span>|<span data-ttu-id="6ed74-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6ed74-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="6ed74-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ed74-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6ed74-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ed74-112">Not supported.</span></span>|
|<span data-ttu-id="6ed74-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ed74-113">Application</span></span>|<span data-ttu-id="6ed74-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ed74-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6ed74-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ed74-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/managedDeviceOverview
```

## <a name="request-headers"></a><span data-ttu-id="6ed74-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ed74-116">Request headers</span></span>
|<span data-ttu-id="6ed74-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ed74-117">Header</span></span>|<span data-ttu-id="6ed74-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ed74-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6ed74-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="6ed74-119">Authorization</span></span>|<span data-ttu-id="6ed74-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6ed74-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6ed74-121">Accept</span><span class="sxs-lookup"><span data-stu-id="6ed74-121">Accept</span></span>|<span data-ttu-id="6ed74-122">application/json</span><span class="sxs-lookup"><span data-stu-id="6ed74-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ed74-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ed74-123">Request body</span></span>
<span data-ttu-id="6ed74-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6ed74-124">In the request body, supply a JSON representation for the [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md) object.</span></span>

<span data-ttu-id="6ed74-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6ed74-125">The following table shows the properties that are required when you create the [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).</span></span>

|<span data-ttu-id="6ed74-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6ed74-126">Property</span></span>|<span data-ttu-id="6ed74-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ed74-127">Type</span></span>|<span data-ttu-id="6ed74-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ed74-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6ed74-129">id</span><span class="sxs-lookup"><span data-stu-id="6ed74-129">id</span></span>|<span data-ttu-id="6ed74-130">String</span><span class="sxs-lookup"><span data-stu-id="6ed74-130">String</span></span>|<span data-ttu-id="6ed74-131">Identificador único del resumen</span><span class="sxs-lookup"><span data-stu-id="6ed74-131">Unique Identifier for the summary</span></span>|
|<span data-ttu-id="6ed74-132">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6ed74-132">enrolledDeviceCount</span></span>|<span data-ttu-id="6ed74-133">Int32</span><span class="sxs-lookup"><span data-stu-id="6ed74-133">Int32</span></span>|<span data-ttu-id="6ed74-134">Número total de dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="6ed74-134">Total enrolled device count.</span></span> <span data-ttu-id="6ed74-135">No incluye equipos administrados mediante el agente de PC de Intune</span><span class="sxs-lookup"><span data-stu-id="6ed74-135">Does not include PC devices managed via Intune PC Agent</span></span>|
|<span data-ttu-id="6ed74-136">mdmEnrolledCount</span><span class="sxs-lookup"><span data-stu-id="6ed74-136">mdmEnrolledCount</span></span>|<span data-ttu-id="6ed74-137">Int32</span><span class="sxs-lookup"><span data-stu-id="6ed74-137">Int32</span></span>|<span data-ttu-id="6ed74-138">El número de dispositivos inscritos en MDM</span><span class="sxs-lookup"><span data-stu-id="6ed74-138">The number of devices enrolled in MDM</span></span>|
|<span data-ttu-id="6ed74-139">dualEnrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="6ed74-139">dualEnrolledDeviceCount</span></span>|<span data-ttu-id="6ed74-140">Int32</span><span class="sxs-lookup"><span data-stu-id="6ed74-140">Int32</span></span>|<span data-ttu-id="6ed74-141">El número de dispositivos inscritos tanto en MDM como EAS</span><span class="sxs-lookup"><span data-stu-id="6ed74-141">The number of devices enrolled in both MDM and EAS</span></span>|
|<span data-ttu-id="6ed74-142">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="6ed74-142">deviceOperatingSystemSummary</span></span>|[<span data-ttu-id="6ed74-143">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="6ed74-143">deviceOperatingSystemSummary</span></span>](../resources/intune_devices_deviceoperatingsystemsummary.md)|<span data-ttu-id="6ed74-144">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6ed74-144">Device operating system summary.</span></span>|
|<span data-ttu-id="6ed74-145">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="6ed74-145">deviceExchangeAccessStateSummary</span></span>|[<span data-ttu-id="6ed74-146">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="6ed74-146">deviceExchangeAccessStateSummary</span></span>](../resources/intune_devices_deviceexchangeaccessstatesummary.md)|<span data-ttu-id="6ed74-147">Distribución del estado de acceso de Exchange en Intune</span><span class="sxs-lookup"><span data-stu-id="6ed74-147">Distribution of Exchange Access State in Intune</span></span>|



## <a name="response"></a><span data-ttu-id="6ed74-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ed74-148">Response</span></span>
<span data-ttu-id="6ed74-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ed74-149">If successful, this method returns a `200 OK` response code and an updated [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6ed74-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ed74-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="6ed74-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ed74-151">Request</span></span>
<span data-ttu-id="6ed74-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ed74-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/managedDeviceOverview
Content-type: application/json
Content-length: 625

{
  "enrolledDeviceCount": 3,
  "mdmEnrolledCount": 0,
  "dualEnrolledDeviceCount": 7,
  "deviceOperatingSystemSummary": {
    "@odata.type": "microsoft.graph.deviceOperatingSystemSummary",
    "androidCount": 12,
    "iosCount": 8,
    "macOSCount": 10,
    "windowsMobileCount": 2,
    "windowsCount": 12,
    "unknownCount": 12
  },
  "deviceExchangeAccessStateSummary": {
    "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary",
    "allowedDeviceCount": 2,
    "blockedDeviceCount": 2,
    "quarantinedDeviceCount": 6,
    "unknownDeviceCount": 2,
    "unavailableDeviceCount": 6
  }
}
```

### <a name="response"></a><span data-ttu-id="6ed74-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ed74-153">Response</span></span>
<span data-ttu-id="6ed74-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ed74-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 734

{
  "@odata.type": "#microsoft.graph.managedDeviceOverview",
  "id": "42a91653-1653-42a9-5316-a9425316a942",
  "enrolledDeviceCount": 3,
  "mdmEnrolledCount": 0,
  "dualEnrolledDeviceCount": 7,
  "deviceOperatingSystemSummary": {
    "@odata.type": "microsoft.graph.deviceOperatingSystemSummary",
    "androidCount": 12,
    "iosCount": 8,
    "macOSCount": 10,
    "windowsMobileCount": 2,
    "windowsCount": 12,
    "unknownCount": 12
  },
  "deviceExchangeAccessStateSummary": {
    "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary",
    "allowedDeviceCount": 2,
    "blockedDeviceCount": 2,
    "quarantinedDeviceCount": 6,
    "unknownDeviceCount": 2,
    "unavailableDeviceCount": 6
  }
}
```








