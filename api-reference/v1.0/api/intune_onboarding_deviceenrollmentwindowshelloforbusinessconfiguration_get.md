# <a name="get-deviceenrollmentwindowshelloforbusinessconfiguration"></a><span data-ttu-id="cf237-101">Obtener deviceEnrollmentWindowsHelloForBusinessConfiguration</span><span class="sxs-lookup"><span data-stu-id="cf237-101">Get deviceEnrollmentWindowsHelloForBusinessConfiguration</span></span>

> <span data-ttu-id="cf237-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cf237-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cf237-103">Lea las propiedades y las relaciones del objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="cf237-103">Read properties and relationships of the [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cf237-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cf237-104">Prerequisites</span></span>
<span data-ttu-id="cf237-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cf237-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="cf237-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cf237-107">Permission type</span></span>|<span data-ttu-id="cf237-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cf237-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cf237-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cf237-109">Delegated (work or school account)</span></span>|<span data-ttu-id="cf237-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="cf237-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="cf237-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cf237-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cf237-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf237-112">Not supported.</span></span>|
|<span data-ttu-id="cf237-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cf237-113">Application</span></span>|<span data-ttu-id="cf237-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cf237-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cf237-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cf237-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="cf237-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cf237-116">Optional query parameters</span></span>
<span data-ttu-id="cf237-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf237-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="cf237-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cf237-118">Request headers</span></span>
|<span data-ttu-id="cf237-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cf237-119">Header</span></span>|<span data-ttu-id="cf237-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cf237-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cf237-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="cf237-121">Authorization</span></span>|<span data-ttu-id="cf237-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cf237-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cf237-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cf237-123">Accept</span></span>|<span data-ttu-id="cf237-124">application/json</span><span class="sxs-lookup"><span data-stu-id="cf237-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cf237-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cf237-125">Request body</span></span>
<span data-ttu-id="cf237-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cf237-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cf237-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf237-127">Response</span></span>
<span data-ttu-id="cf237-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cf237-128">If successful, this method returns a `200 OK` response code and [deviceEnrollmentWindowsHelloForBusinessConfiguration](../resources/intune_onboarding_deviceenrollmentwindowshelloforbusinessconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cf237-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cf237-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="cf237-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cf237-130">Request</span></span>
<span data-ttu-id="cf237-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cf237-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

### <a name="response"></a><span data-ttu-id="cf237-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cf237-132">Response</span></span>
<span data-ttu-id="cf237-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cf237-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 860

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceEnrollmentWindowsHelloForBusinessConfiguration",
    "id": "3068e0cd-e0cd-3068-cde0-6830cde06830",
    "displayName": "Display Name value",
    "description": "Description value",
    "priority": 8,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "version": 7,
    "pinMinimumLength": 0,
    "pinMaximumLength": 0,
    "pinUppercaseCharactersUsage": "required",
    "pinLowercaseCharactersUsage": "required",
    "pinSpecialCharactersUsage": "required",
    "state": "enabled",
    "securityDeviceRequired": true,
    "unlockWithBiometricsEnabled": true,
    "remotePassportEnabled": true,
    "pinPreviousBlockCount": 5,
    "pinExpirationInDays": 3,
    "enhancedBiometricsState": "enabled"
  }
}
```



