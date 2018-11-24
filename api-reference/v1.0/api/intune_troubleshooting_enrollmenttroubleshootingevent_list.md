# <a name="list-enrollmenttroubleshootingevents"></a><span data-ttu-id="6ef40-101">Enumerar enrollmentTroubleshootingEvents</span><span class="sxs-lookup"><span data-stu-id="6ef40-101">List enrollmentTroubleshootingEvents</span></span>

> <span data-ttu-id="6ef40-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6ef40-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6ef40-103">Enumere las propiedades y las relaciones de los objetos [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="6ef40-103">List properties and relationships of the [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6ef40-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6ef40-104">Prerequisites</span></span>
<span data-ttu-id="6ef40-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6ef40-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6ef40-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ef40-107">Permission type</span></span>|<span data-ttu-id="6ef40-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ef40-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6ef40-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ef40-109">Delegated (work or school account)</span></span>|<span data-ttu-id="6ef40-110">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="6ef40-110">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="6ef40-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ef40-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6ef40-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ef40-112">Not supported.</span></span>|
|<span data-ttu-id="6ef40-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ef40-113">Application</span></span>|<span data-ttu-id="6ef40-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ef40-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6ef40-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ef40-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/troubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="6ef40-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ef40-116">Request headers</span></span>
|<span data-ttu-id="6ef40-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ef40-117">Header</span></span>|<span data-ttu-id="6ef40-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ef40-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6ef40-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="6ef40-119">Authorization</span></span>|<span data-ttu-id="6ef40-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6ef40-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6ef40-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6ef40-121">Accept</span></span>|<span data-ttu-id="6ef40-122">application/json</span><span class="sxs-lookup"><span data-stu-id="6ef40-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ef40-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ef40-123">Request body</span></span>
<span data-ttu-id="6ef40-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="6ef40-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="6ef40-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ef40-125">Response</span></span>
<span data-ttu-id="6ef40-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ef40-126">If successful, this method returns a `200 OK` response code and a collection of [enrollmentTroubleshootingEvent](../resources/intune_troubleshooting_enrollmenttroubleshootingevent.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6ef40-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ef40-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="6ef40-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ef40-128">Request</span></span>
<span data-ttu-id="6ef40-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ef40-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/troubleshootingEvents
```

### <a name="response"></a><span data-ttu-id="6ef40-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ef40-130">Response</span></span>
<span data-ttu-id="6ef40-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ef40-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 639

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.enrollmentTroubleshootingEvent",
      "id": "c4a623f5-23f5-c4a6-f523-a6c4f523a6c4",
      "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
      "correlationId": "Correlation Id value",
      "managedDeviceIdentifier": "Managed Device Identifier value",
      "operatingSystem": "Operating System value",
      "osVersion": "Os Version value",
      "userId": "User Id value",
      "deviceId": "Device Id value",
      "enrollmentType": "userEnrollment",
      "failureCategory": "authentication",
      "failureReason": "Failure Reason value"
    }
  ]
}
```



