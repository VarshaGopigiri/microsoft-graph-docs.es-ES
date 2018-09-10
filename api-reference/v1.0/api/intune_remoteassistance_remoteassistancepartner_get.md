# <a name="get-remoteassistancepartner"></a><span data-ttu-id="e02fd-101">Obtener remoteAssistancePartner</span><span class="sxs-lookup"><span data-stu-id="e02fd-101">Get remoteAssistancePartner</span></span>

> <span data-ttu-id="e02fd-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e02fd-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e02fd-103">Lea las propiedades y las relaciones del objeto [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md).</span><span class="sxs-lookup"><span data-stu-id="e02fd-103">Read properties and relationships of the [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e02fd-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e02fd-104">Prerequisites</span></span>
<span data-ttu-id="e02fd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e02fd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e02fd-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e02fd-107">Permission type</span></span>|<span data-ttu-id="e02fd-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e02fd-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e02fd-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e02fd-109">Delegated (work or school account)</span></span>|<span data-ttu-id="e02fd-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="e02fd-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="e02fd-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e02fd-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e02fd-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e02fd-112">Not supported.</span></span>|
|<span data-ttu-id="e02fd-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e02fd-113">Application</span></span>|<span data-ttu-id="e02fd-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e02fd-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e02fd-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e02fd-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="e02fd-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e02fd-116">Optional query parameters</span></span>
<span data-ttu-id="e02fd-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e02fd-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e02fd-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e02fd-118">Request headers</span></span>
|<span data-ttu-id="e02fd-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e02fd-119">Header</span></span>|<span data-ttu-id="e02fd-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e02fd-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e02fd-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="e02fd-121">Authorization</span></span>|<span data-ttu-id="e02fd-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e02fd-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e02fd-123">Accept</span><span class="sxs-lookup"><span data-stu-id="e02fd-123">Accept</span></span>|<span data-ttu-id="e02fd-124">application/json</span><span class="sxs-lookup"><span data-stu-id="e02fd-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e02fd-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e02fd-125">Request body</span></span>
<span data-ttu-id="e02fd-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e02fd-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e02fd-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e02fd-127">Response</span></span>
<span data-ttu-id="e02fd-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e02fd-128">If successful, this method returns a `200 OK` response code and [remoteAssistancePartner](../resources/intune_remoteassistance_remoteassistancepartner.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e02fd-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e02fd-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="e02fd-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e02fd-130">Request</span></span>
<span data-ttu-id="e02fd-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e02fd-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/remoteAssistancePartners/{remoteAssistancePartnerId}
```

### <a name="response"></a><span data-ttu-id="e02fd-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e02fd-132">Response</span></span>
<span data-ttu-id="e02fd-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e02fd-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 346

{
  "value": {
    "@odata.type": "#microsoft.graph.remoteAssistancePartner",
    "id": "7443c8b9-c8b9-7443-b9c8-4374b9c84374",
    "displayName": "Display Name value",
    "onboardingUrl": "https://example.com/onboardingUrl/",
    "onboardingStatus": "onboarding",
    "lastConnectionDateTime": "2016-12-31T23:58:36.6670033-08:00"
  }
}
```








