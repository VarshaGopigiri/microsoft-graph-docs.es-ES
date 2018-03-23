# <a name="update-devicemanagementtroubleshootingevent"></a><span data-ttu-id="a2703-101">Actualizar deviceManagementTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="a2703-101">Update deviceManagementTroubleshootingEvent</span></span>

> <span data-ttu-id="a2703-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a2703-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a2703-103">Actualice las propiedades de un objeto [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="a2703-103">Update the properties of a [calendar](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a2703-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a2703-104">Prerequisites</span></span>
<span data-ttu-id="a2703-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a2703-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a2703-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a2703-107">Permission type</span></span>|<span data-ttu-id="a2703-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a2703-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a2703-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a2703-109">Delegated (work or school account)</span></span>|<span data-ttu-id="a2703-110">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a2703-110">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="a2703-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a2703-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a2703-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2703-112">Not supported.</span></span>|
|<span data-ttu-id="a2703-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a2703-113">Application</span></span>|<span data-ttu-id="a2703-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a2703-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a2703-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a2703-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

## <a name="request-headers"></a><span data-ttu-id="a2703-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a2703-116">Request headers</span></span>
|<span data-ttu-id="a2703-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a2703-117">Header</span></span>|<span data-ttu-id="a2703-118">Valor</span><span class="sxs-lookup"><span data-stu-id="a2703-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a2703-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="a2703-119">Authorization</span></span>|<span data-ttu-id="a2703-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a2703-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="a2703-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a2703-121">Accept</span></span>|<span data-ttu-id="a2703-122">application/json</span><span class="sxs-lookup"><span data-stu-id="a2703-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a2703-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a2703-123">Request body</span></span>
<span data-ttu-id="a2703-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="a2703-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) object.</span></span>

<span data-ttu-id="a2703-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="a2703-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="a2703-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a2703-126">Property</span></span>|<span data-ttu-id="a2703-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="a2703-127">Type</span></span>|<span data-ttu-id="a2703-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="a2703-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a2703-129">id</span><span class="sxs-lookup"><span data-stu-id="a2703-129">id</span></span>|<span data-ttu-id="a2703-130">String</span><span class="sxs-lookup"><span data-stu-id="a2703-130">String</span></span>|<span data-ttu-id="a2703-131">UUID para el objeto</span><span class="sxs-lookup"><span data-stu-id="a2703-131">UUID for the object</span></span>|
|<span data-ttu-id="a2703-132">eventDateTime</span><span class="sxs-lookup"><span data-stu-id="a2703-132">eventDateTime</span></span>|<span data-ttu-id="a2703-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a2703-133">DateTimeOffset</span></span>|<span data-ttu-id="a2703-134">Hora en que ocurrió el evento.</span><span class="sxs-lookup"><span data-stu-id="a2703-134">Time when the event occurred .</span></span>|
|<span data-ttu-id="a2703-135">correlationId</span><span class="sxs-lookup"><span data-stu-id="a2703-135">correlationId</span></span>|<span data-ttu-id="a2703-136">String</span><span class="sxs-lookup"><span data-stu-id="a2703-136">String</span></span>|<span data-ttu-id="a2703-137">Id. utilizado para rastrear el error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="a2703-137">Id used for tracing the failure in the service.</span></span>|



## <a name="response"></a><span data-ttu-id="a2703-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2703-138">Response</span></span>
<span data-ttu-id="a2703-139">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a2703-139">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a2703-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a2703-140">Example</span></span>
### <a name="request"></a><span data-ttu-id="a2703-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a2703-141">Request</span></span>
<span data-ttu-id="a2703-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a2703-142">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
Content-type: application/json
Content-length: 104

{
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value"
}
```

### <a name="response"></a><span data-ttu-id="a2703-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a2703-143">Response</span></span>
<span data-ttu-id="a2703-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a2703-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 228

{
  "@odata.type": "#microsoft.graph.deviceManagementTroubleshootingEvent",
  "id": "fb26dcee-dcee-fb26-eedc-26fbeedc26fb",
  "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
  "correlationId": "Correlation Id value"
}
```



