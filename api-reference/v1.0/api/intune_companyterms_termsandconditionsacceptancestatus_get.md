# <a name="get-termsandconditionsacceptancestatus"></a><span data-ttu-id="54bbb-101">Obtener termsAndConditionsAcceptanceStatus</span><span class="sxs-lookup"><span data-stu-id="54bbb-101">Get termsAndConditionsAcceptanceStatus</span></span>

> <span data-ttu-id="54bbb-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="54bbb-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="54bbb-103">Lea las propiedades y las relaciones del objeto [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md).</span><span class="sxs-lookup"><span data-stu-id="54bbb-103">Read properties and relationships of the [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="54bbb-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="54bbb-104">Prerequisites</span></span>
<span data-ttu-id="54bbb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="54bbb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="54bbb-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="54bbb-107">Permission type</span></span>|<span data-ttu-id="54bbb-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="54bbb-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="54bbb-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="54bbb-109">Delegated (work or school account)</span></span>|<span data-ttu-id="54bbb-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="54bbb-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="54bbb-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="54bbb-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="54bbb-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54bbb-112">Not supported.</span></span>|
|<span data-ttu-id="54bbb-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="54bbb-113">Application</span></span>|<span data-ttu-id="54bbb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="54bbb-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="54bbb-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="54bbb-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="54bbb-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="54bbb-116">Optional query parameters</span></span>
<span data-ttu-id="54bbb-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54bbb-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="54bbb-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="54bbb-118">Request headers</span></span>
|<span data-ttu-id="54bbb-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54bbb-119">Header</span></span>|<span data-ttu-id="54bbb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="54bbb-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="54bbb-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="54bbb-121">Authorization</span></span>|<span data-ttu-id="54bbb-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="54bbb-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="54bbb-123">Accept</span><span class="sxs-lookup"><span data-stu-id="54bbb-123">Accept</span></span>|<span data-ttu-id="54bbb-124">application/json</span><span class="sxs-lookup"><span data-stu-id="54bbb-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="54bbb-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="54bbb-125">Request body</span></span>
<span data-ttu-id="54bbb-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="54bbb-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="54bbb-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54bbb-127">Response</span></span>
<span data-ttu-id="54bbb-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="54bbb-128">If successful, this method returns a `200 OK` response code and [termsAndConditionsAcceptanceStatus](../resources/intune_companyterms_termsandconditionsacceptancestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="54bbb-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="54bbb-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="54bbb-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="54bbb-130">Request</span></span>
<span data-ttu-id="54bbb-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="54bbb-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}
```

### <a name="response"></a><span data-ttu-id="54bbb-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="54bbb-132">Response</span></span>
<span data-ttu-id="54bbb-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="54bbb-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 289

{
  "value": {
    "@odata.type": "#microsoft.graph.termsAndConditionsAcceptanceStatus",
    "id": "a045ce1a-ce1a-a045-1ace-45a01ace45a0",
    "userDisplayName": "User Display Name value",
    "acceptedVersion": 15,
    "acceptedDateTime": "2016-12-31T23:57:43.6165506-08:00"
  }
}
```








