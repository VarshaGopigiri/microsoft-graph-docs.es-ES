# <a name="get-windowsupdateforbusinessconfiguration"></a><span data-ttu-id="b93ad-101">Obtener windowsUpdateForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="b93ad-101">Get windowsUpdateForBusinessConfiguration</span></span>

> <span data-ttu-id="b93ad-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b93ad-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b93ad-103">Lea las propiedades y las relaciones del objeto [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="b93ad-103">Read properties and relationships of [plannerTaskDetails](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b93ad-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b93ad-104">Prerequisites</span></span>
<span data-ttu-id="b93ad-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="b93ad-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="b93ad-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b93ad-107">Permission type</span></span>|<span data-ttu-id="b93ad-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b93ad-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b93ad-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b93ad-109">Delegated (work or school account)</span></span>|<span data-ttu-id="b93ad-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="b93ad-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="b93ad-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b93ad-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b93ad-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b93ad-112">Not supported.</span></span>|
|<span data-ttu-id="b93ad-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b93ad-113">Application</span></span>|<span data-ttu-id="b93ad-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b93ad-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b93ad-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b93ad-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="b93ad-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="b93ad-116">Optional query parameters</span></span>
<span data-ttu-id="b93ad-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b93ad-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="b93ad-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b93ad-118">Request headers</span></span>
|<span data-ttu-id="b93ad-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b93ad-119">Header</span></span>|<span data-ttu-id="b93ad-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b93ad-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b93ad-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b93ad-121">Authorization</span></span>|<span data-ttu-id="b93ad-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b93ad-122">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="b93ad-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="b93ad-123">Accept</span></span>|<span data-ttu-id="b93ad-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b93ad-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b93ad-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b93ad-125">Request body</span></span>
<span data-ttu-id="b93ad-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b93ad-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b93ad-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b93ad-127">Response</span></span>
<span data-ttu-id="b93ad-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b93ad-128">If successful, this method returns a `200 OK` response code and a [ListItemVersion](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b93ad-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b93ad-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="b93ad-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b93ad-130">Request</span></span>
<span data-ttu-id="b93ad-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b93ad-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="b93ad-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b93ad-132">Response</span></span>
<span data-ttu-id="b93ad-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b93ad-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1149

{
  "value": {
    "@odata.type": "#microsoft.graph.windowsUpdateForBusinessConfiguration",
    "id": "4928dd6a-dd6a-4928-6add-28496add2849",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "deliveryOptimizationMode": "httpOnly",
    "prereleaseFeatures": "settingsOnly",
    "automaticUpdateMode": "notifyDownload",
    "microsoftUpdateServiceAllowed": true,
    "driversExcluded": true,
    "installationSchedule": {
      "@odata.type": "microsoft.graph.windowsUpdateScheduledInstall",
      "scheduledInstallDay": "everyday",
      "scheduledInstallTime": "11:59:31.3170000"
    },
    "qualityUpdatesDeferralPeriodInDays": 2,
    "featureUpdatesDeferralPeriodInDays": 2,
    "qualityUpdatesPaused": true,
    "featureUpdatesPaused": true,
    "qualityUpdatesPauseExpiryDateTime": "2017-01-01T00:00:22.9594683-08:00",
    "featureUpdatesPauseExpiryDateTime": "2016-12-31T23:58:08.068669-08:00",
    "businessReadyUpdatesOnly": "all"
  }
}
```



