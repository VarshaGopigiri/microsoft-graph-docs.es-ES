# <a name="list-devicemanagementtroubleshootingevents"></a><span data-ttu-id="1fb1d-101">Enumerar deviceManagementTroubleshootingEvents</span><span class="sxs-lookup"><span data-stu-id="1fb1d-101">List deviceManagementTroubleshootingEvents</span></span>

> <span data-ttu-id="1fb1d-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1fb1d-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1fb1d-103">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1fb1d-103">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1fb1d-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1fb1d-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1fb1d-105">Enumere las propiedades y las relaciones de los objetos [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md).</span><span class="sxs-lookup"><span data-stu-id="1fb1d-105">List properties and relationships of the [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1fb1d-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1fb1d-106">Prerequisites</span></span>
<span data-ttu-id="1fb1d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1fb1d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1fb1d-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1fb1d-109">Permission type</span></span>|<span data-ttu-id="1fb1d-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1fb1d-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1fb1d-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1fb1d-111">Delegated (work or school account)</span></span>|<span data-ttu-id="1fb1d-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="1fb1d-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="1fb1d-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1fb1d-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1fb1d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1fb1d-114">Not supported.</span></span>|
|<span data-ttu-id="1fb1d-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1fb1d-115">Application</span></span>|<span data-ttu-id="1fb1d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1fb1d-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1fb1d-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1fb1d-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/troubleshootingEvents
```

## <a name="request-headers"></a><span data-ttu-id="1fb1d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1fb1d-118">Request headers</span></span>
|<span data-ttu-id="1fb1d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1fb1d-119">Header</span></span>|<span data-ttu-id="1fb1d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1fb1d-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1fb1d-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="1fb1d-121">Authorization</span></span>|<span data-ttu-id="1fb1d-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1fb1d-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1fb1d-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1fb1d-123">Accept</span></span>|<span data-ttu-id="1fb1d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1fb1d-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1fb1d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1fb1d-125">Request body</span></span>
<span data-ttu-id="1fb1d-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1fb1d-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1fb1d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1fb1d-127">Response</span></span>
<span data-ttu-id="1fb1d-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1fb1d-128">If successful, this method returns a `200 OK` response code and a collection of [deviceManagementTroubleshootingEvent](../resources/intune_troubleshooting_devicemanagementtroubleshootingevent.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1fb1d-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fb1d-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="1fb1d-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1fb1d-130">Request</span></span>
<span data-ttu-id="1fb1d-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1fb1d-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/troubleshootingEvents
```

### <a name="response"></a><span data-ttu-id="1fb1d-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1fb1d-132">Response</span></span>
<span data-ttu-id="1fb1d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1fb1d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 277

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceManagementTroubleshootingEvent",
      "id": "fb26dcee-dcee-fb26-eedc-26fbeedc26fb",
      "eventDateTime": "2016-12-31T23:59:23.3984029-08:00",
      "correlationId": "Correlation Id value"
    }
  ]
}
```



