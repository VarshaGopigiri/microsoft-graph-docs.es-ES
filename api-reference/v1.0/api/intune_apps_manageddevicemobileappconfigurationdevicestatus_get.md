# <a name="get-manageddevicemobileappconfigurationdevicestatus"></a><span data-ttu-id="bff47-101">Obtener managedDeviceMobileAppConfigurationDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="bff47-101">Get managedDeviceMobileAppConfigurationDeviceStatus</span></span>

> <span data-ttu-id="bff47-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bff47-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bff47-103">Lea las propiedades y las relaciones del objeto [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="bff47-103">Read properties and relationships of the [managedAppPolicy](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="bff47-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bff47-104">Prerequisites</span></span>
<span data-ttu-id="bff47-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="bff47-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="bff47-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bff47-107">Permission type</span></span>|<span data-ttu-id="bff47-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bff47-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="bff47-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bff47-109">Delegated (work or school account)</span></span>|<span data-ttu-id="bff47-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="bff47-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="bff47-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bff47-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="bff47-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bff47-112">Not supported.</span></span>|
|<span data-ttu-id="bff47-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bff47-113">Application</span></span>|<span data-ttu-id="bff47-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bff47-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="bff47-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bff47-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses/{managedDeviceMobileAppConfigurationDeviceStatusId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="bff47-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="bff47-116">Optional query parameters</span></span>
<span data-ttu-id="bff47-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bff47-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="bff47-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bff47-118">Request headers</span></span>
|<span data-ttu-id="bff47-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bff47-119">Header</span></span>|<span data-ttu-id="bff47-120">Valor</span><span class="sxs-lookup"><span data-stu-id="bff47-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="bff47-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="bff47-121">Authorization</span></span>|<span data-ttu-id="bff47-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="bff47-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="bff47-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="bff47-123">Accept</span></span>|<span data-ttu-id="bff47-124">application/json</span><span class="sxs-lookup"><span data-stu-id="bff47-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="bff47-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bff47-125">Request body</span></span>
<span data-ttu-id="bff47-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bff47-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="bff47-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bff47-127">Response</span></span>
<span data-ttu-id="bff47-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bff47-128">If successful, this method returns a `200 OK` response code and a [windowsPhone81CompliancePolicy](../resources/intune_apps_manageddevicemobileappconfigurationdevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bff47-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bff47-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="bff47-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bff47-130">Request</span></span>
<span data-ttu-id="bff47-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bff47-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses/{managedDeviceMobileAppConfigurationDeviceStatusId}
```

### <a name="response"></a><span data-ttu-id="bff47-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bff47-132">Response</span></span>
<span data-ttu-id="bff47-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="bff47-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 531

{
  "value": {
    "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceStatus",
    "id": "477d3651-3651-477d-5136-7d4751367d47",
    "deviceDisplayName": "Device Display Name value",
    "userName": "User Name value",
    "deviceModel": "Device Model value",
    "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
    "status": "notApplicable",
    "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
    "userPrincipalName": "User Principal Name value"
  }
}
```


