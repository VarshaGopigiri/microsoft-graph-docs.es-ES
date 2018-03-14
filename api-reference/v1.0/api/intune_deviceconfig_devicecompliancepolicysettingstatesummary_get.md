# <a name="get-devicecompliancepolicysettingstatesummary"></a><span data-ttu-id="41c2c-101">Obtener deviceCompliancePolicySettingStateSummary</span><span class="sxs-lookup"><span data-stu-id="41c2c-101">Get deviceCompliancePolicySettingStateSummary</span></span>

> <span data-ttu-id="41c2c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="41c2c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="41c2c-103">Lea las propiedades y las relaciones del objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="41c2c-103">Read properties and relationships of [plannerProgressTaskBoardTaskFormat](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="41c2c-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="41c2c-104">Prerequisites</span></span>
<span data-ttu-id="41c2c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="41c2c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="41c2c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41c2c-107">Permission type</span></span>|<span data-ttu-id="41c2c-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41c2c-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="41c2c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41c2c-109">Delegated (work or school account)</span></span>|<span data-ttu-id="41c2c-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="41c2c-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="41c2c-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41c2c-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="41c2c-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41c2c-112">Not supported.</span></span>|
|<span data-ttu-id="41c2c-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41c2c-113">Application</span></span>|<span data-ttu-id="41c2c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41c2c-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="41c2c-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41c2c-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="41c2c-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="41c2c-116">Optional query parameters</span></span>
<span data-ttu-id="41c2c-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41c2c-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="41c2c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41c2c-118">Request headers</span></span>
|<span data-ttu-id="41c2c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41c2c-119">Header</span></span>|<span data-ttu-id="41c2c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="41c2c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="41c2c-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="41c2c-121">Authorization</span></span>|<span data-ttu-id="41c2c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="41c2c-122">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="41c2c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="41c2c-123">Accept</span></span>|<span data-ttu-id="41c2c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="41c2c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="41c2c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="41c2c-125">Request body</span></span>
<span data-ttu-id="41c2c-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="41c2c-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="41c2c-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41c2c-127">Response</span></span>
<span data-ttu-id="41c2c-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41c2c-128">If successful, this method returns a `200 OK` response code and a [section](../resources/intune_deviceconfig_devicecompliancepolicysettingstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="41c2c-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41c2c-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="41c2c-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41c2c-130">Request</span></span>
<span data-ttu-id="41c2c-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41c2c-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries/{deviceCompliancePolicySettingStateSummaryId}
```

### <a name="response"></a><span data-ttu-id="41c2c-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41c2c-132">Response</span></span>
<span data-ttu-id="41c2c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="41c2c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 483

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingStateSummary",
    "setting": "Setting value",
    "settingName": "Setting Name value",
    "platformType": "iOS",
    "id": "7474d6d5-d6d5-7474-d5d6-7474d5d67474",
    "unknownDeviceCount": 2,
    "notApplicableDeviceCount": 8,
    "compliantDeviceCount": 4,
    "remediatedDeviceCount": 5,
    "nonCompliantDeviceCount": 7,
    "errorDeviceCount": 0,
    "conflictDeviceCount": 3
  }
}
```



