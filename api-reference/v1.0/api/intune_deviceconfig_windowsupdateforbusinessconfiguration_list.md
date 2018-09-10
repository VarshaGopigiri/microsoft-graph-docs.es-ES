# <a name="list-windowsupdateforbusinessconfigurations"></a><span data-ttu-id="1c063-101">Enumerar windowsUpdateForBusinessConfigurations</span><span class="sxs-lookup"><span data-stu-id="1c063-101">List windowsUpdateForBusinessConfigurations</span></span>

> <span data-ttu-id="1c063-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1c063-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1c063-103">Enumere las propiedades y las relaciones de los objetos [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="1c063-103">List properties and relationships of the [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="1c063-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1c063-104">Prerequisites</span></span>
<span data-ttu-id="1c063-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1c063-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1c063-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1c063-107">Permission type</span></span>|<span data-ttu-id="1c063-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1c063-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="1c063-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1c063-109">Delegated (work or school account)</span></span>|<span data-ttu-id="1c063-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="1c063-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="1c063-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1c063-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="1c063-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1c063-112">Not supported.</span></span>|
|<span data-ttu-id="1c063-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1c063-113">Application</span></span>|<span data-ttu-id="1c063-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="1c063-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="1c063-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1c063-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="1c063-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1c063-116">Request headers</span></span>
|<span data-ttu-id="1c063-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c063-117">Header</span></span>|<span data-ttu-id="1c063-118">Valor</span><span class="sxs-lookup"><span data-stu-id="1c063-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="1c063-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="1c063-119">Authorization</span></span>|<span data-ttu-id="1c063-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="1c063-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="1c063-121">Accept</span><span class="sxs-lookup"><span data-stu-id="1c063-121">Accept</span></span>|<span data-ttu-id="1c063-122">application/json</span><span class="sxs-lookup"><span data-stu-id="1c063-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="1c063-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1c063-123">Request body</span></span>
<span data-ttu-id="1c063-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1c063-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1c063-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c063-125">Response</span></span>
<span data-ttu-id="1c063-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1c063-126">If successful, this method returns a `200 OK` response code and a collection of [windowsUpdateForBusinessConfiguration](../resources/intune_deviceconfig_windowsupdateforbusinessconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="1c063-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1c063-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="1c063-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1c063-128">Request</span></span>
<span data-ttu-id="1c063-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1c063-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="1c063-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1c063-130">Response</span></span>
<span data-ttu-id="1c063-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1c063-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1211

{
  "value": [
    {
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
  ]
}
```








