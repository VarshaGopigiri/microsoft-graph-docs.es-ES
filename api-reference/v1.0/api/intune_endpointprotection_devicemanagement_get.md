# <a name="get-devicemanagement"></a><span data-ttu-id="f9b8d-101">Obtener deviceManagement</span><span class="sxs-lookup"><span data-stu-id="f9b8d-101">Get deviceManagement</span></span>

> <span data-ttu-id="f9b8d-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f9b8d-103">Lea las propiedades y las relaciones del objeto [deviceManagement](../resources/intune_endpointprotection_devicemanagement.md).</span><span class="sxs-lookup"><span data-stu-id="f9b8d-103">Read properties and relationships of [plannerTaskDetails](../resources/intune_endpointprotection_devicemanagement.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f9b8d-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f9b8d-104">Prerequisites</span></span>
<span data-ttu-id="f9b8d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f9b8d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f9b8d-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9b8d-107">Permission type</span></span>|<span data-ttu-id="f9b8d-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f9b8d-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f9b8d-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9b8d-109">Delegated (work or school account)</span></span>|<span data-ttu-id="f9b8d-110">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="f9b8d-110">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="f9b8d-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9b8d-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f9b8d-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-112">Not supported.</span></span>|
|<span data-ttu-id="f9b8d-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9b8d-113">Application</span></span>|<span data-ttu-id="f9b8d-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f9b8d-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9b8d-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f9b8d-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f9b8d-116">Optional query parameters</span></span>
<span data-ttu-id="f9b8d-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/es-ES/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f9b8d-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9b8d-118">Request headers</span></span>
|<span data-ttu-id="f9b8d-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f9b8d-119">Header</span></span>|<span data-ttu-id="f9b8d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f9b8d-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f9b8d-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="f9b8d-121">Authorization</span></span>|<span data-ttu-id="f9b8d-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-122">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="f9b8d-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f9b8d-123">Accept</span></span>|<span data-ttu-id="f9b8d-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f9b8d-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f9b8d-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9b8d-125">Request body</span></span>
<span data-ttu-id="f9b8d-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f9b8d-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9b8d-127">Response</span></span>
<span data-ttu-id="f9b8d-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceManagement](../resources/intune_endpointprotection_devicemanagement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-128">If successful, this method returns a `200 OK` response code and a [section](../resources/intune_endpointprotection_devicemanagement.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9b8d-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9b8d-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="f9b8d-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9b8d-130">Request</span></span>
<span data-ttu-id="f9b8d-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement
```

### <a name="response"></a><span data-ttu-id="f9b8d-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9b8d-132">Response</span></span>
<span data-ttu-id="f9b8d-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f9b8d-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 130

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceManagement",
    "id": "0b283420-3420-0b28-2034-280b2034280b"
  }
}
```



