# <a name="deviceconfigurationdeviceactivity-function"></a><span data-ttu-id="5a17b-101">Función deviceConfigurationDeviceActivity</span><span class="sxs-lookup"><span data-stu-id="5a17b-101">deviceConfigurationDeviceActivity function</span></span>

> <span data-ttu-id="5a17b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5a17b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5a17b-103">Metadatos para el informe de actividad de dispositivo de configuración de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5a17b-103">Metadata for the device configuration device activity report</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5a17b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5a17b-104">Prerequisites</span></span>
<span data-ttu-id="5a17b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="5a17b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="5a17b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5a17b-107">Permission type</span></span>|<span data-ttu-id="5a17b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5a17b-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5a17b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5a17b-109">Delegated (work or school account)</span></span>||
| <span data-ttu-id="5a17b-110">&nbsp; &nbsp; Configuración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="5a17b-110">&nbsp; &nbsp;Device Configuration.</span></span> | <span data-ttu-id="5a17b-111">DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="5a17b-111">DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="5a17b-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5a17b-112">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5a17b-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5a17b-113">Not supported.</span></span>|
|<span data-ttu-id="5a17b-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5a17b-114">Application</span></span>|<span data-ttu-id="5a17b-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5a17b-115">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5a17b-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5a17b-116">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /reports/deviceConfigurationDeviceActivity
```

## <a name="request-headers"></a><span data-ttu-id="5a17b-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5a17b-117">Request headers</span></span>
|<span data-ttu-id="5a17b-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5a17b-118">Header</span></span>|<span data-ttu-id="5a17b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="5a17b-119">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5a17b-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="5a17b-120">Authorization</span></span>|<span data-ttu-id="5a17b-121">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5a17b-121">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5a17b-122">Accept</span><span class="sxs-lookup"><span data-stu-id="5a17b-122">Accept</span></span>|<span data-ttu-id="5a17b-123">application/json</span><span class="sxs-lookup"><span data-stu-id="5a17b-123">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5a17b-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5a17b-124">Request body</span></span>
<span data-ttu-id="5a17b-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5a17b-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5a17b-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a17b-126">Response</span></span>
<span data-ttu-id="5a17b-127">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y un [informe](../resources/intune_shared_report.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5a17b-127">If successful, this function returns a `200 OK` response code and a [report](../resources/intune_shared_report.md) in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5a17b-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5a17b-128">Example</span></span>
### <a name="request"></a><span data-ttu-id="5a17b-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5a17b-129">Request</span></span>
<span data-ttu-id="5a17b-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5a17b-130">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/reports/deviceConfigurationDeviceActivity
```

### <a name="response"></a><span data-ttu-id="5a17b-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5a17b-131">Response</span></span>
<span data-ttu-id="5a17b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5a17b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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








