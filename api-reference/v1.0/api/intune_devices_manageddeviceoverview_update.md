# <a name="update-manageddeviceoverview"></a><span data-ttu-id="d0109-101">Actualizar managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="d0109-101">Update managedDeviceOverview</span></span>

> <span data-ttu-id="d0109-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d0109-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d0109-103">Actualice las propiedades de un objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d0109-103">Update the properties of a [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="d0109-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="d0109-104">Prerequisites</span></span>
<span data-ttu-id="d0109-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d0109-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d0109-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d0109-107">Permission type</span></span>|<span data-ttu-id="d0109-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d0109-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="d0109-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d0109-109">Delegated (work or school account)</span></span>|<span data-ttu-id="d0109-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d0109-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="d0109-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d0109-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="d0109-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0109-112">Not supported.</span></span>|
|<span data-ttu-id="d0109-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d0109-113">Application</span></span>|<span data-ttu-id="d0109-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d0109-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="d0109-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d0109-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/managedDeviceOverview
```

## <a name="request-headers"></a><span data-ttu-id="d0109-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d0109-116">Request headers</span></span>
|<span data-ttu-id="d0109-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d0109-117">Header</span></span>|<span data-ttu-id="d0109-118">Valor</span><span class="sxs-lookup"><span data-stu-id="d0109-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="d0109-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="d0109-119">Authorization</span></span>|<span data-ttu-id="d0109-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="d0109-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="d0109-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="d0109-121">Accept</span></span>|<span data-ttu-id="d0109-122">application/json</span><span class="sxs-lookup"><span data-stu-id="d0109-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="d0109-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d0109-123">Request body</span></span>
<span data-ttu-id="d0109-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d0109-124">In the request body, supply a JSON representation for the [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md) object.</span></span>

<span data-ttu-id="d0109-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d0109-125">The following table shows the properties that are required when you create the [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md).</span></span>

|<span data-ttu-id="d0109-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0109-126">Property</span></span>|<span data-ttu-id="d0109-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0109-127">Type</span></span>|<span data-ttu-id="d0109-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0109-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d0109-129">id</span><span class="sxs-lookup"><span data-stu-id="d0109-129">id</span></span>|<span data-ttu-id="d0109-130">String</span><span class="sxs-lookup"><span data-stu-id="d0109-130">String</span></span>|<span data-ttu-id="d0109-131">Identificador único del resumen</span><span class="sxs-lookup"><span data-stu-id="d0109-131">Unique Identifier for the summary</span></span>|
|<span data-ttu-id="d0109-132">enrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d0109-132">enrolledDeviceCount</span></span>|<span data-ttu-id="d0109-133">Int32</span><span class="sxs-lookup"><span data-stu-id="d0109-133">Int32</span></span>|<span data-ttu-id="d0109-134">Número total de dispositivos inscritos.</span><span class="sxs-lookup"><span data-stu-id="d0109-134">Total enrolled device count.</span></span> <span data-ttu-id="d0109-135">No incluye equipos administrados mediante el agente de PC de Intune</span><span class="sxs-lookup"><span data-stu-id="d0109-135">Does not include PC devices managed via Intune PC Agent</span></span>|
|<span data-ttu-id="d0109-136">mdmEnrolledCount</span><span class="sxs-lookup"><span data-stu-id="d0109-136">mdmEnrolledCount</span></span>|<span data-ttu-id="d0109-137">Int32</span><span class="sxs-lookup"><span data-stu-id="d0109-137">Int32</span></span>|<span data-ttu-id="d0109-138">El número de dispositivos inscritos en MDM</span><span class="sxs-lookup"><span data-stu-id="d0109-138">The number of devices enrolled in MDM</span></span>|
|<span data-ttu-id="d0109-139">dualEnrolledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="d0109-139">dualEnrolledDeviceCount</span></span>|<span data-ttu-id="d0109-140">Int32</span><span class="sxs-lookup"><span data-stu-id="d0109-140">Int32</span></span>|<span data-ttu-id="d0109-141">El número de dispositivos inscritos tanto en MDM como EAS</span><span class="sxs-lookup"><span data-stu-id="d0109-141">The number of devices enrolled in both MDM and EAS</span></span>|
|<span data-ttu-id="d0109-142">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="d0109-142">deviceOperatingSystemSummary</span></span>|[<span data-ttu-id="d0109-143">deviceOperatingSystemSummary</span><span class="sxs-lookup"><span data-stu-id="d0109-143">deviceOperatingSystemSummary</span></span>](../resources/intune_devices_deviceoperatingsystemsummary.md)|<span data-ttu-id="d0109-144">Resumen de sistemas operativos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="d0109-144">Device operating system summary.</span></span>|
|<span data-ttu-id="d0109-145">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="d0109-145">deviceExchangeAccessStateSummary</span></span>|[<span data-ttu-id="d0109-146">deviceExchangeAccessStateSummary</span><span class="sxs-lookup"><span data-stu-id="d0109-146">deviceExchangeAccessStateSummary</span></span>](../resources/intune_devices_deviceexchangeaccessstatesummary.md)|<span data-ttu-id="d0109-147">Distribución del estado de acceso de Exchange en Intune</span><span class="sxs-lookup"><span data-stu-id="d0109-147">Distribution of Exchange Access State in Intune</span></span>|



## <a name="response"></a><span data-ttu-id="d0109-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0109-148">Response</span></span>
<span data-ttu-id="d0109-149">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d0109-149">If successful, this method returns a `200 OK` response code and an updated [managedDeviceOverview](../resources/intune_devices_manageddeviceoverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d0109-150">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d0109-150">Example</span></span>
### <a name="request"></a><span data-ttu-id="d0109-151">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d0109-151">Request</span></span>
<span data-ttu-id="d0109-152">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d0109-152">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/managedDeviceOverview
Content-type: application/json
Content-length: 685

{
  "@odata.type": "#microsoft.graph.managedDeviceOverview",
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

### <a name="response"></a><span data-ttu-id="d0109-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d0109-153">Response</span></span>
<span data-ttu-id="d0109-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="d0109-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



