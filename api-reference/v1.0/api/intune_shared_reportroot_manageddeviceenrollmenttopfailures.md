# <a name="manageddeviceenrollmenttopfailures-function"></a><span data-ttu-id="70b7c-101">Función managedDeviceEnrollmentTopFailures</span><span class="sxs-lookup"><span data-stu-id="70b7c-101">managedDeviceEnrollmentTopFailures function</span></span>

> <span data-ttu-id="70b7c-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="70b7c-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="70b7c-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="70b7c-103">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="70b7c-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="70b7c-104">Prerequisites</span></span>
<span data-ttu-id="70b7c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="70b7c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="70b7c-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="70b7c-107">Permission type</span></span>|<span data-ttu-id="70b7c-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="70b7c-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="70b7c-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="70b7c-109">Delegated (work or school account)</span></span>||
| <span data-ttu-id="70b7c-110">&nbsp; &nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="70b7c-110">&nbsp; &nbsp;Troubleshooting</span></span> | <span data-ttu-id="70b7c-111">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="70b7c-111">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="70b7c-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="70b7c-112">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="70b7c-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70b7c-113">Not supported.</span></span>|
|<span data-ttu-id="70b7c-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="70b7c-114">Application</span></span>|<span data-ttu-id="70b7c-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="70b7c-115">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="70b7c-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="70b7c-116">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentTopFailures
```

## <a name="request-headers"></a><span data-ttu-id="70b7c-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="70b7c-117">Request headers</span></span>
|<span data-ttu-id="70b7c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70b7c-118">Header</span></span>|<span data-ttu-id="70b7c-119">Valor</span><span class="sxs-lookup"><span data-stu-id="70b7c-119">Value</span></span>|
|:---|:---|
|<span data-ttu-id="70b7c-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="70b7c-120">Authorization</span></span>|<span data-ttu-id="70b7c-121">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="70b7c-121">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="70b7c-122">Accept</span><span class="sxs-lookup"><span data-stu-id="70b7c-122">Accept</span></span>|<span data-ttu-id="70b7c-123">application/json</span><span class="sxs-lookup"><span data-stu-id="70b7c-123">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="70b7c-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="70b7c-124">Request body</span></span>
<span data-ttu-id="70b7c-125">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="70b7c-125">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="70b7c-126">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="70b7c-126">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="70b7c-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="70b7c-127">Property</span></span>|<span data-ttu-id="70b7c-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="70b7c-128">Type</span></span>|<span data-ttu-id="70b7c-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="70b7c-129">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="70b7c-130">period</span><span class="sxs-lookup"><span data-stu-id="70b7c-130">period</span></span>|<span data-ttu-id="70b7c-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="70b7c-131">String</span></span>|<span data-ttu-id="70b7c-132">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="70b7c-132">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="70b7c-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70b7c-133">Response</span></span>
<span data-ttu-id="70b7c-134">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune_shared_report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="70b7c-134">If successful, this function returns a `200 OK` response code and a [report](../resources/intune_shared_report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="70b7c-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="70b7c-135">Example</span></span>
### <a name="request"></a><span data-ttu-id="70b7c-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="70b7c-136">Request</span></span>
<span data-ttu-id="70b7c-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="70b7c-137">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1/reports/managedDeviceEnrollmentTopFailures(period='parameterValue')
```

### <a name="response"></a><span data-ttu-id="70b7c-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="70b7c-138">Response</span></span>
<span data-ttu-id="70b7c-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="70b7c-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 123

{
  "value": {
    "@odata.type": "microsoft.graph.report",
    "content": "<Unknown Primitive Type Edm.Stream>"
  }
}
```




