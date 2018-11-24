# <a name="get-deviceconfigurationdeviceoverview"></a><span data-ttu-id="85e5f-101">Obtener deviceConfigurationDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="85e5f-101">Get deviceConfigurationDeviceOverview</span></span>

> <span data-ttu-id="85e5f-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="85e5f-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="85e5f-103">Lea las propiedades y las relaciones del objeto [deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="85e5f-103">Read properties and relationships of the [deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="85e5f-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="85e5f-104">Prerequisites</span></span>
<span data-ttu-id="85e5f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="85e5f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="85e5f-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="85e5f-107">Permission type</span></span>|<span data-ttu-id="85e5f-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="85e5f-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="85e5f-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="85e5f-109">Delegated (work or school account)</span></span>|<span data-ttu-id="85e5f-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="85e5f-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="85e5f-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="85e5f-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="85e5f-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="85e5f-112">Not supported.</span></span>|
|<span data-ttu-id="85e5f-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="85e5f-113">Application</span></span>|<span data-ttu-id="85e5f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="85e5f-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="85e5f-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="85e5f-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatusOverview
```

## <a name="optional-query-parameters"></a><span data-ttu-id="85e5f-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="85e5f-116">Optional query parameters</span></span>
<span data-ttu-id="85e5f-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85e5f-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="85e5f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="85e5f-118">Request headers</span></span>
|<span data-ttu-id="85e5f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="85e5f-119">Header</span></span>|<span data-ttu-id="85e5f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="85e5f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="85e5f-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="85e5f-121">Authorization</span></span>|<span data-ttu-id="85e5f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="85e5f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="85e5f-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="85e5f-123">Accept</span></span>|<span data-ttu-id="85e5f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="85e5f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="85e5f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="85e5f-125">Request body</span></span>
<span data-ttu-id="85e5f-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="85e5f-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="85e5f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85e5f-127">Response</span></span>
<span data-ttu-id="85e5f-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="85e5f-128">If successful, this method returns a `200 OK` response code and [deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="85e5f-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="85e5f-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="85e5f-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="85e5f-130">Request</span></span>
<span data-ttu-id="85e5f-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="85e5f-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatusOverview
```

### <a name="response"></a><span data-ttu-id="85e5f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="85e5f-132">Response</span></span>
<span data-ttu-id="85e5f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="85e5f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 370

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceConfigurationDeviceOverview",
    "id": "62d48e3a-8e3a-62d4-3a8e-d4623a8ed462",
    "pendingCount": 12,
    "notApplicableCount": 2,
    "successCount": 12,
    "errorCount": 10,
    "failedCount": 11,
    "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
    "configurationVersion": 4
  }
}
```



