# <a name="list-vpptokens"></a><span data-ttu-id="03c97-101">Enumerar vppTokens</span><span class="sxs-lookup"><span data-stu-id="03c97-101">List vppTokens</span></span>

> <span data-ttu-id="03c97-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="03c97-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="03c97-103">Enumera las propiedades y las relaciones de los objetos [vppToken](../resources/intune_onboarding_vpptoken.md).</span><span class="sxs-lookup"><span data-stu-id="03c97-103">List properties and relationships of the [vppToken](../resources/intune_onboarding_vpptoken.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="03c97-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03c97-104">Prerequisites</span></span>
<span data-ttu-id="03c97-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="03c97-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="03c97-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03c97-107">Permission type</span></span>|<span data-ttu-id="03c97-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03c97-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="03c97-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03c97-109">Delegated (work or school account)</span></span>|<span data-ttu-id="03c97-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span><span class="sxs-lookup"><span data-stu-id="03c97-110">DeviceManagementServiceConfig.ReadWrite.All, DeviceManagementServiceConfig.Read.All</span></span>|
|<span data-ttu-id="03c97-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03c97-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="03c97-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03c97-112">Not supported.</span></span>|
|<span data-ttu-id="03c97-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03c97-113">Application</span></span>|<span data-ttu-id="03c97-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03c97-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="03c97-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03c97-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/vppTokens
```

## <a name="request-headers"></a><span data-ttu-id="03c97-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03c97-116">Request headers</span></span>
|<span data-ttu-id="03c97-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03c97-117">Header</span></span>|<span data-ttu-id="03c97-118">Valor</span><span class="sxs-lookup"><span data-stu-id="03c97-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="03c97-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="03c97-119">Authorization</span></span>|<span data-ttu-id="03c97-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="03c97-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="03c97-121">Accept</span><span class="sxs-lookup"><span data-stu-id="03c97-121">Accept</span></span>|<span data-ttu-id="03c97-122">application/json</span><span class="sxs-lookup"><span data-stu-id="03c97-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="03c97-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03c97-123">Request body</span></span>
<span data-ttu-id="03c97-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="03c97-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="03c97-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03c97-125">Response</span></span>
<span data-ttu-id="03c97-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [vppToken](../resources/intune_onboarding_vpptoken.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="03c97-126">If successful, this method returns a `200 OK` response code and a collection of [vppToken](../resources/intune_onboarding_vpptoken.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="03c97-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03c97-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="03c97-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03c97-128">Request</span></span>
<span data-ttu-id="03c97-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03c97-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/vppTokens
```

### <a name="response"></a><span data-ttu-id="03c97-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03c97-130">Response</span></span>
<span data-ttu-id="03c97-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="03c97-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 659

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.vppToken",
      "id": "9ceb2f92-2f92-9ceb-922f-eb9c922feb9c",
      "organizationName": "Organization Name value",
      "vppTokenAccountType": "education",
      "appleId": "Apple Id value",
      "expirationDateTime": "2016-12-31T23:57:57.2481234-08:00",
      "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
      "token": "Token value",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "state": "valid",
      "lastSyncStatus": "inProgress",
      "automaticallyUpdateApps": true,
      "countryOrRegion": "Country Or Region value"
    }
  ]
}
```








