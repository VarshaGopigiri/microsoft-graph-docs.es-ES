# <a name="get-iosupdateconfiguration"></a><span data-ttu-id="52c0e-101">Obtener iosUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="52c0e-101">Get iosUpdateConfiguration</span></span>

> <span data-ttu-id="52c0e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="52c0e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="52c0e-103">Lea las propiedades y las relaciones del objeto [iosUpdateConfiguration](../resources/intune_deviceconfig_iosupdateconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="52c0e-103">Read properties and relationships of the [iosUpdateConfiguration](../resources/intune_deviceconfig_iosupdateconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="52c0e-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="52c0e-104">Prerequisites</span></span>
<span data-ttu-id="52c0e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="52c0e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="52c0e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="52c0e-107">Permission type</span></span>|<span data-ttu-id="52c0e-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="52c0e-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="52c0e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="52c0e-109">Delegated (work or school account)</span></span>|<span data-ttu-id="52c0e-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="52c0e-110">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="52c0e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="52c0e-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="52c0e-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="52c0e-112">Not supported.</span></span>|
|<span data-ttu-id="52c0e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="52c0e-113">Application</span></span>|<span data-ttu-id="52c0e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="52c0e-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="52c0e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="52c0e-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="52c0e-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="52c0e-116">Optional query parameters</span></span>
<span data-ttu-id="52c0e-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52c0e-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="52c0e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="52c0e-118">Request headers</span></span>
|<span data-ttu-id="52c0e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="52c0e-119">Header</span></span>|<span data-ttu-id="52c0e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="52c0e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="52c0e-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="52c0e-121">Authorization</span></span>|<span data-ttu-id="52c0e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="52c0e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="52c0e-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="52c0e-123">Accept</span></span>|<span data-ttu-id="52c0e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="52c0e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="52c0e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="52c0e-125">Request body</span></span>
<span data-ttu-id="52c0e-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="52c0e-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="52c0e-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52c0e-127">Response</span></span>
<span data-ttu-id="52c0e-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [iosUpdateConfiguration](../resources/intune_deviceconfig_iosupdateconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="52c0e-128">If successful, this method returns a `200 OK` response code and [iosUpdateConfiguration](../resources/intune_deviceconfig_iosupdateconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="52c0e-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="52c0e-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="52c0e-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="52c0e-130">Request</span></span>
<span data-ttu-id="52c0e-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="52c0e-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="52c0e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="52c0e-132">Response</span></span>
<span data-ttu-id="52c0e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="52c0e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 542

{
  "value": {
    "@odata.type": "#microsoft.graph.iosUpdateConfiguration",
    "id": "321aef09-ef09-321a-09ef-1a3209ef1a32",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "activeHoursStart": "12:00:05.5020000",
    "activeHoursEnd": "11:59:00.8990000",
    "scheduledInstallDays": [
      "monday"
    ],
    "utcTimeOffsetInMinutes": 6
  }
}
```



