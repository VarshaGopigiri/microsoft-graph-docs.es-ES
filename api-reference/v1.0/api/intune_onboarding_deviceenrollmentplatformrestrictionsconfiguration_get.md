# <a name="get-deviceenrollmentplatformrestrictionsconfiguration"></a><span data-ttu-id="adeee-101">Obtener deviceEnrollmentPlatformRestrictionsConfiguration</span><span class="sxs-lookup"><span data-stu-id="adeee-101">Get deviceEnrollmentPlatformRestrictionsConfiguration</span></span>

> <span data-ttu-id="adeee-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="adeee-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="adeee-103">Lea las propiedades y las relaciones del objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="adeee-103">Read properties and relationships of the [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="adeee-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="adeee-104">Prerequisites</span></span>
<span data-ttu-id="adeee-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="adeee-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="adeee-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="adeee-107">Permission type</span></span>|<span data-ttu-id="adeee-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="adeee-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="adeee-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="adeee-109">Delegated (work or school account)</span></span>|<span data-ttu-id="adeee-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="adeee-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="adeee-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="adeee-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="adeee-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="adeee-112">Not supported.</span></span>|
|<span data-ttu-id="adeee-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="adeee-113">Application</span></span>|<span data-ttu-id="adeee-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="adeee-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="adeee-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="adeee-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="adeee-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="adeee-116">Optional query parameters</span></span>
<span data-ttu-id="adeee-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="adeee-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="adeee-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="adeee-118">Request headers</span></span>
|<span data-ttu-id="adeee-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="adeee-119">Header</span></span>|<span data-ttu-id="adeee-120">Valor</span><span class="sxs-lookup"><span data-stu-id="adeee-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="adeee-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="adeee-121">Authorization</span></span>|<span data-ttu-id="adeee-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="adeee-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="adeee-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="adeee-123">Accept</span></span>|<span data-ttu-id="adeee-124">application/json</span><span class="sxs-lookup"><span data-stu-id="adeee-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="adeee-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="adeee-125">Request body</span></span>
<span data-ttu-id="adeee-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="adeee-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="adeee-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="adeee-127">Response</span></span>
<span data-ttu-id="adeee-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="adeee-128">If successful, this method returns a `200 OK` response code and [deviceEnrollmentPlatformRestrictionsConfiguration](../resources/intune_onboarding_deviceenrollmentplatformrestrictionsconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="adeee-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="adeee-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="adeee-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="adeee-130">Request</span></span>
<span data-ttu-id="adeee-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="adeee-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceEnrollmentConfigurations/{deviceEnrollmentConfigurationId}
```

### <a name="response"></a><span data-ttu-id="adeee-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="adeee-132">Response</span></span>
<span data-ttu-id="adeee-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="adeee-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1927

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceEnrollmentPlatformRestrictionsConfiguration",
    "id": "3acb2d75-2d75-3acb-752d-cb3a752dcb3a",
    "displayName": "Display Name value",
    "description": "Description value",
    "priority": 8,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "version": 7,
    "iosRestriction": {
      "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
      "platformBlocked": true,
      "personalDeviceEnrollmentBlocked": true,
      "osMinimumVersion": "Os Minimum Version value",
      "osMaximumVersion": "Os Maximum Version value"
    },
    "windowsRestriction": {
      "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
      "platformBlocked": true,
      "personalDeviceEnrollmentBlocked": true,
      "osMinimumVersion": "Os Minimum Version value",
      "osMaximumVersion": "Os Maximum Version value"
    },
    "windowsMobileRestriction": {
      "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
      "platformBlocked": true,
      "personalDeviceEnrollmentBlocked": true,
      "osMinimumVersion": "Os Minimum Version value",
      "osMaximumVersion": "Os Maximum Version value"
    },
    "androidRestriction": {
      "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
      "platformBlocked": true,
      "personalDeviceEnrollmentBlocked": true,
      "osMinimumVersion": "Os Minimum Version value",
      "osMaximumVersion": "Os Maximum Version value"
    },
    "macOSRestriction": {
      "@odata.type": "microsoft.graph.deviceEnrollmentPlatformRestriction",
      "platformBlocked": true,
      "personalDeviceEnrollmentBlocked": true,
      "osMinimumVersion": "Os Minimum Version value",
      "osMaximumVersion": "Os Maximum Version value"
    }
  }
}
```



