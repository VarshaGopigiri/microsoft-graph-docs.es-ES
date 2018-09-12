# <a name="manageddeviceenrollmentfailuredetails-function"></a><span data-ttu-id="8d659-101">Función managedDeviceEnrollmentFailureDetails</span><span class="sxs-lookup"><span data-stu-id="8d659-101">managedDeviceEnrollmentFailureDetails function</span></span>

> <span data-ttu-id="8d659-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8d659-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8d659-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="8d659-103">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8d659-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8d659-104">Prerequisites</span></span>
<span data-ttu-id="8d659-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8d659-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8d659-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8d659-107">Permission type</span></span>|<span data-ttu-id="8d659-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8d659-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8d659-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8d659-109">Delegated (work or school account)</span></span>||
| <span data-ttu-id="8d659-110">&nbsp; &nbsp; Solución de problemas</span><span class="sxs-lookup"><span data-stu-id="8d659-110">&nbsp; &nbsp;Troubleshooting</span></span> | <span data-ttu-id="8d659-111">DeviceManagementManagedDevices.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8d659-111">DeviceManagementManagedDevices.ReadWrite.All</span></span>|
|<span data-ttu-id="8d659-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8d659-112">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8d659-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d659-113">Not supported.</span></span>|
|<span data-ttu-id="8d659-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8d659-114">Application</span></span>|<span data-ttu-id="8d659-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8d659-115">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8d659-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8d659-116">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/managedDeviceEnrollmentFailureDetails
```

## <a name="request-headers"></a><span data-ttu-id="8d659-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8d659-117">Request headers</span></span>
|<span data-ttu-id="8d659-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8d659-118">Header</span></span>|<span data-ttu-id="8d659-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8d659-119">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8d659-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="8d659-120">Authorization</span></span>|<span data-ttu-id="8d659-121">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8d659-121">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8d659-122">Accept</span><span class="sxs-lookup"><span data-stu-id="8d659-122">Accept</span></span>|<span data-ttu-id="8d659-123">application/json</span><span class="sxs-lookup"><span data-stu-id="8d659-123">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8d659-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8d659-124">Request body</span></span>
<span data-ttu-id="8d659-125">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="8d659-125">In the request URL, provide the following query parameters with values.</span></span>
<span data-ttu-id="8d659-126">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="8d659-126">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="8d659-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8d659-127">Property</span></span>|<span data-ttu-id="8d659-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="8d659-128">Type</span></span>|<span data-ttu-id="8d659-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d659-129">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8d659-130">skip</span><span class="sxs-lookup"><span data-stu-id="8d659-130">skip</span></span>|<span data-ttu-id="8d659-131">Int32</span><span class="sxs-lookup"><span data-stu-id="8d659-131">Int32</span></span>|<span data-ttu-id="8d659-132">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="8d659-132">Not yet documented</span></span>|
|<span data-ttu-id="8d659-133">top</span><span class="sxs-lookup"><span data-stu-id="8d659-133">top</span></span>|<span data-ttu-id="8d659-134">Int32</span><span class="sxs-lookup"><span data-stu-id="8d659-134">Int32</span></span>|<span data-ttu-id="8d659-135">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="8d659-135">Not yet documented</span></span>|
|<span data-ttu-id="8d659-136">filter</span><span class="sxs-lookup"><span data-stu-id="8d659-136">filter</span></span>|<span data-ttu-id="8d659-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="8d659-137">String</span></span>|<span data-ttu-id="8d659-138">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="8d659-138">Not yet documented</span></span>|
|<span data-ttu-id="8d659-139">skipToken</span><span class="sxs-lookup"><span data-stu-id="8d659-139">skipToken</span></span>|<span data-ttu-id="8d659-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="8d659-140">String</span></span>|<span data-ttu-id="8d659-141">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="8d659-141">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="8d659-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d659-142">Response</span></span>
<span data-ttu-id="8d659-143">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune_shared_report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8d659-143">If successful, this function returns a `200 OK` response code and a [report](../resources/intune_shared_report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8d659-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8d659-144">Example</span></span>
### <a name="request"></a><span data-ttu-id="8d659-145">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8d659-145">Request</span></span>
<span data-ttu-id="8d659-146">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8d659-146">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1/reports/managedDeviceEnrollmentFailureDetails(skip=4,top=3,filter='parameterValue',skipToken='parameterValue')
```

### <a name="response"></a><span data-ttu-id="8d659-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8d659-147">Response</span></span>
<span data-ttu-id="8d659-148">Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="8d659-148">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="8d659-149">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8d659-149">All of the properties will be returned from an actual call.</span></span>

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




