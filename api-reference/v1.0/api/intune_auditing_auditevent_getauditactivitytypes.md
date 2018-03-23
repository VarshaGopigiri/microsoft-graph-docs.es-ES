# <a name="getauditactivitytypes-function"></a><span data-ttu-id="15907-101">Función getAuditActivityTypes</span><span class="sxs-lookup"><span data-stu-id="15907-101">getAuditActivityTypes function</span></span>

> <span data-ttu-id="15907-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="15907-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="15907-103">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="15907-103">Not yet documented</span></span>
## <a name="prerequisites"></a><span data-ttu-id="15907-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="15907-104">Prerequisites</span></span>
<span data-ttu-id="15907-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="15907-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="15907-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="15907-107">Permission type</span></span>|<span data-ttu-id="15907-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="15907-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="15907-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="15907-109">Delegated (work or school account)</span></span>|<span data-ttu-id="15907-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="15907-110">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="15907-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="15907-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="15907-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15907-112">Not supported.</span></span>|
|<span data-ttu-id="15907-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="15907-113">Application</span></span>|<span data-ttu-id="15907-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="15907-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="15907-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="15907-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/auditEvents/getAuditActivityTypes
```

## <a name="request-headers"></a><span data-ttu-id="15907-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="15907-116">Request headers</span></span>
|<span data-ttu-id="15907-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="15907-117">Header</span></span>|<span data-ttu-id="15907-118">Valor</span><span class="sxs-lookup"><span data-stu-id="15907-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="15907-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="15907-119">Authorization</span></span>|<span data-ttu-id="15907-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="15907-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="15907-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="15907-121">Accept</span></span>|<span data-ttu-id="15907-122">application/json</span><span class="sxs-lookup"><span data-stu-id="15907-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="15907-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="15907-123">Request body</span></span>
<span data-ttu-id="15907-124">En la dirección URL de la solicitud, proporcione los siguientes parámetros de consulta con valores.</span><span class="sxs-lookup"><span data-stu-id="15907-124">In the request URL, provide the following required query parameters with values.</span></span>
<span data-ttu-id="15907-125">La siguiente tabla muestra los parámetros que se pueden usar con esta función.</span><span class="sxs-lookup"><span data-stu-id="15907-125">The following table shows the parameters that can be used with this function.</span></span>

|<span data-ttu-id="15907-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="15907-126">Property</span></span>|<span data-ttu-id="15907-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="15907-127">Type</span></span>|<span data-ttu-id="15907-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="15907-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="15907-129">categoría</span><span class="sxs-lookup"><span data-stu-id="15907-129">category</span></span>|<span data-ttu-id="15907-130">String</span><span class="sxs-lookup"><span data-stu-id="15907-130">String</span></span>|<span data-ttu-id="15907-131">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="15907-131">Not yet documented</span></span>|



## <a name="response"></a><span data-ttu-id="15907-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15907-132">Response</span></span>
<span data-ttu-id="15907-133">Si se ejecuta correctamente, esta función devuelve un código de respuesta `200 OK` y una colección String en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="15907-133">If successful, this method returns `200 OK` response code and String collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="15907-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="15907-134">Example</span></span>
### <a name="request"></a><span data-ttu-id="15907-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="15907-135">Request</span></span>
<span data-ttu-id="15907-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="15907-136">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/auditEvents/getAuditActivityTypes(category='parameterValue')
```

### <a name="response"></a><span data-ttu-id="15907-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="15907-137">Response</span></span>
<span data-ttu-id="15907-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="15907-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 61

{
  "value": [
    "Get Audit Activity Types value"
  ]
}
```



