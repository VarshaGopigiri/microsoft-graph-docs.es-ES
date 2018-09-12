# <a name="get-deviceappmanagement"></a><span data-ttu-id="32d27-101">Obtener deviceAppManagement</span><span class="sxs-lookup"><span data-stu-id="32d27-101">Get deviceAppManagement</span></span>

> <span data-ttu-id="32d27-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="32d27-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="32d27-103">Lea las propiedades y las relaciones del objeto [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md).</span><span class="sxs-lookup"><span data-stu-id="32d27-103">Read properties and relationships of the [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="32d27-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="32d27-104">Prerequisites</span></span>

<span data-ttu-id="32d27-105">Se requiere uno de los siguientes permisos para llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="32d27-105">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see Permissions.</span></span> <span data-ttu-id="32d27-106">Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="32d27-106">To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>  <span data-ttu-id="32d27-107">Tenga en cuenta que el permiso adecuado varía según el flujo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="32d27-107">Note that the appropriate permission varies according to the workflow.</span></span>

|<span data-ttu-id="32d27-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="32d27-108">Permission type</span></span>|<span data-ttu-id="32d27-109">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="32d27-109">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="32d27-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="32d27-110">Delegated (work or school account)</span></span>|<span data-ttu-id="32d27-111">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="32d27-111">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span> |
|<span data-ttu-id="32d27-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="32d27-112">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="32d27-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32d27-113">Not supported.</span></span>|
|<span data-ttu-id="32d27-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="32d27-114">Application</span></span>|<span data-ttu-id="32d27-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32d27-115">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="32d27-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="32d27-116">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement
```

## <a name="optional-query-parameters"></a><span data-ttu-id="32d27-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="32d27-117">Optional query parameters</span></span>
<span data-ttu-id="32d27-118">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32d27-118">This method supports the [OData Query Parameters](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="32d27-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="32d27-119">Request headers</span></span>
|<span data-ttu-id="32d27-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32d27-120">Header</span></span>|<span data-ttu-id="32d27-121">Valor</span><span class="sxs-lookup"><span data-stu-id="32d27-121">Value</span></span>|
|:---|:---|
|<span data-ttu-id="32d27-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="32d27-122">Authorization</span></span>|<span data-ttu-id="32d27-123">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="32d27-123">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="32d27-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="32d27-124">Accept</span></span>|<span data-ttu-id="32d27-125">application/json</span><span class="sxs-lookup"><span data-stu-id="32d27-125">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="32d27-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="32d27-126">Request body</span></span>
<span data-ttu-id="32d27-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="32d27-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="32d27-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32d27-128">Response</span></span>
<span data-ttu-id="32d27-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32d27-129">If successful, this method returns a `200 OK` response code and [deviceAppManagement](../resources/intune_shared_deviceappmanagement.md) object in the response body.</span></span>

## <a name="example-request"></a><span data-ttu-id="32d27-130">Solicitud de ejemplo</span><span class="sxs-lookup"><span data-stu-id="32d27-130">Example request</span></span>

``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement
```

## <a name="example-response"></a><span data-ttu-id="32d27-131">Respuesta de ejemplo</span><span class="sxs-lookup"><span data-stu-id="32d27-131">Example response</span></span>
<span data-ttu-id="32d27-132">Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="32d27-132">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="32d27-133">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="32d27-133">All the properties will be returned from an actual call.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 133

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceAppManagement",
    "id": "bbb801a3-01a3-bbb8-a301-b8bba301b8bb"
  }
}
```



