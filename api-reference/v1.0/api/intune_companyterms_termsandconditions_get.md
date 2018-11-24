# <a name="get-termsandconditions"></a><span data-ttu-id="9f2b1-101">Obtener termsAndConditions</span><span class="sxs-lookup"><span data-stu-id="9f2b1-101">Get termsAndConditions</span></span>

> <span data-ttu-id="9f2b1-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9f2b1-103">Lea las propiedades y las relaciones del objeto [termsAndConditions](../resources/intune_companyterms_termsandconditions.md).</span><span class="sxs-lookup"><span data-stu-id="9f2b1-103">Read properties and relationships of the [termsAndConditions](../resources/intune_companyterms_termsandconditions.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9f2b1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9f2b1-104">Prerequisites</span></span>
<span data-ttu-id="9f2b1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9f2b1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9f2b1-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9f2b1-107">Permission type</span></span>|<span data-ttu-id="9f2b1-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9f2b1-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9f2b1-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9f2b1-109">Delegated (work or school account)</span></span>|<span data-ttu-id="9f2b1-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="9f2b1-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="9f2b1-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9f2b1-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9f2b1-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-112">Not supported.</span></span>|
|<span data-ttu-id="9f2b1-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9f2b1-113">Application</span></span>|<span data-ttu-id="9f2b1-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9f2b1-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9f2b1-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/termsAndConditions/{termsAndConditionsId}
GET /deviceManagement/termsAndConditions/{termsAndConditionsId}/acceptanceStatuses/{termsAndConditionsAcceptanceStatusId}/termsAndConditions
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9f2b1-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9f2b1-116">Optional query parameters</span></span>
<span data-ttu-id="9f2b1-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="9f2b1-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9f2b1-118">Request headers</span></span>
|<span data-ttu-id="9f2b1-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f2b1-119">Header</span></span>|<span data-ttu-id="9f2b1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9f2b1-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9f2b1-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="9f2b1-121">Authorization</span></span>|<span data-ttu-id="9f2b1-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9f2b1-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9f2b1-123">Accept</span></span>|<span data-ttu-id="9f2b1-124">application/json</span><span class="sxs-lookup"><span data-stu-id="9f2b1-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9f2b1-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9f2b1-125">Request body</span></span>
<span data-ttu-id="9f2b1-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9f2b1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f2b1-127">Response</span></span>
<span data-ttu-id="9f2b1-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [termsAndConditions](../resources/intune_companyterms_termsandconditions.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-128">If successful, this method returns a `200 OK` response code and [termsAndConditions](../resources/intune_companyterms_termsandconditions.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9f2b1-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f2b1-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="9f2b1-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9f2b1-130">Request</span></span>
<span data-ttu-id="9f2b1-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/termsAndConditions/{termsAndConditionsId}
```

### <a name="response"></a><span data-ttu-id="9f2b1-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f2b1-132">Response</span></span>
<span data-ttu-id="9f2b1-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9f2b1-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 484

{
  "value": {
    "@odata.type": "#microsoft.graph.termsAndConditions",
    "id": "eefc80cf-80cf-eefc-cf80-fceecf80fcee",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "displayName": "Display Name value",
    "description": "Description value",
    "title": "Title value",
    "bodyText": "Body Text value",
    "acceptanceStatement": "Acceptance Statement value",
    "version": 7
  }
}
```



