# <a name="get-devicecategory"></a><span data-ttu-id="a57a9-101">Obtener deviceCategory</span><span class="sxs-lookup"><span data-stu-id="a57a9-101">Get deviceCategory</span></span>

> <span data-ttu-id="a57a9-102">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a57a9-102">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a57a9-103">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a57a9-103">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a57a9-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a57a9-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a57a9-105">Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="a57a9-105">Read properties and relationships of the [deviceCategory](../resources/intune_shared_devicecategory.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a57a9-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a57a9-106">Prerequisites</span></span>
<span data-ttu-id="a57a9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a57a9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a57a9-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a57a9-109">Permission type</span></span>|<span data-ttu-id="a57a9-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a57a9-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a57a9-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a57a9-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a57a9-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="a57a9-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="a57a9-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a57a9-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a57a9-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a57a9-114">Not supported.</span></span>|
|<span data-ttu-id="a57a9-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a57a9-115">Application</span></span>|<span data-ttu-id="a57a9-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a57a9-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a57a9-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a57a9-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deviceCategory
GET /deviceManagement/deviceCategories/{deviceCategoryId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a57a9-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a57a9-118">Optional query parameters</span></span>
<span data-ttu-id="a57a9-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a57a9-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a57a9-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a57a9-120">Request headers</span></span>
|<span data-ttu-id="a57a9-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a57a9-121">Header</span></span>|<span data-ttu-id="a57a9-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a57a9-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a57a9-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a57a9-123">Authorization</span></span>|<span data-ttu-id="a57a9-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a57a9-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a57a9-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a57a9-125">Accept</span></span>|<span data-ttu-id="a57a9-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a57a9-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a57a9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a57a9-127">Request body</span></span>
<span data-ttu-id="a57a9-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a57a9-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a57a9-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a57a9-129">Response</span></span>
<span data-ttu-id="a57a9-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceCategory](../resources/intune_shared_devicecategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a57a9-130">If successful, this method returns a `200 OK` response code and [deviceCategory](../resources/intune_shared_devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a57a9-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a57a9-131">Example</span></span>

### <a name="request"></a><span data-ttu-id="a57a9-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a57a9-132">Request</span></span>
<span data-ttu-id="a57a9-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a57a9-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceCategories/{deviceCategoryId}
```

### <a name="response"></a><span data-ttu-id="a57a9-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a57a9-134">Response</span></span>
<span data-ttu-id="a57a9-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a57a9-135">Here is an example of the response.</span></span> <span data-ttu-id="a57a9-136">Nota: es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="a57a9-136">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="a57a9-137">Las propiedades que devuelve una llamada real varían según el contexto.</span><span class="sxs-lookup"><span data-stu-id="a57a9-137">Properties returned from an actual call vary according to context.</span></span>

``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 211

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceCategory",
    "id": "f881b841-b841-f881-41b8-81f841b881f8",
    "displayName": "Display Name value",
    "description": "Description value"
  }
}
```



