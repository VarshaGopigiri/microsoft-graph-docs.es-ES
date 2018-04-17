# <a name="get-devicemanagementtroubleshootingevent"></a><span data-ttu-id="857c2-101">Obtener deviceManagementTroubleshootingEvent</span><span class="sxs-lookup"><span data-stu-id="857c2-101">Get deviceManagementTroubleshootingEvent</span></span>

> <span data-ttu-id="857c2-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="857c2-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="857c2-103">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="857c2-103">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="857c2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="857c2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="857c2-105">Lea las propiedades y las relaciones del objeto [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="857c2-105">Read properties and relationships of the [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="857c2-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="857c2-106">Prerequisites</span></span>
<span data-ttu-id="857c2-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="857c2-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="857c2-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="857c2-109">Permission type</span></span>|<span data-ttu-id="857c2-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="857c2-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="857c2-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="857c2-111">Delegated (work or school account)</span></span>|<span data-ttu-id="857c2-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="857c2-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="857c2-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="857c2-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="857c2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="857c2-114">Not supported.</span></span>|
|<span data-ttu-id="857c2-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="857c2-115">Application</span></span>|<span data-ttu-id="857c2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="857c2-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="857c2-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="857c2-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="857c2-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="857c2-118">Optional query parameters</span></span>
<span data-ttu-id="857c2-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="857c2-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="857c2-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="857c2-120">Request headers</span></span>
|<span data-ttu-id="857c2-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="857c2-121">Header</span></span>|<span data-ttu-id="857c2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="857c2-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="857c2-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="857c2-123">Authorization</span></span>|<span data-ttu-id="857c2-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="857c2-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="857c2-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="857c2-125">Accept</span></span>|<span data-ttu-id="857c2-126">application/json</span><span class="sxs-lookup"><span data-stu-id="857c2-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="857c2-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="857c2-127">Request body</span></span>
<span data-ttu-id="857c2-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="857c2-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="857c2-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="857c2-129">Response</span></span>
<span data-ttu-id="857c2-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="857c2-130">If successful, this method returns a `200 OK` response code and [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="857c2-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="857c2-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="857c2-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="857c2-132">Request</span></span>
<span data-ttu-id="857c2-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="857c2-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/troubleshootingEvents/{deviceManagementTroubleshootingEventId}
```

### <a name="response"></a><span data-ttu-id="857c2-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="857c2-134">Response</span></span>
<span data-ttu-id="857c2-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="857c2-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 255

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceManagementTroubleshootingEvent",
    "id": "fb26dcee-dcee-fb26-eedc-26fbeedc26fb",
    "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
    "correlationId": "Correlation Id value"
  }
}
```



