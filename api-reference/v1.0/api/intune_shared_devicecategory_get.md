# <a name="get-devicecategory"></a><span data-ttu-id="a5a53-101">Obtener deviceCategory</span><span class="sxs-lookup"><span data-stu-id="a5a53-101">Get deviceCategory</span></span>



> <span data-ttu-id="a5a53-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a5a53-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a5a53-103">Lea las propiedades y las relaciones del objeto [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="a5a53-103">Read properties and relationships of the [deviceCategory](../resources/intune_shared_devicecategory.md) object.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a5a53-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a5a53-104">Prerequisites</span></span>
<span data-ttu-id="a5a53-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a5a53-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a5a53-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5a53-107">Permission type</span></span>|<span data-ttu-id="a5a53-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5a53-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a5a53-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5a53-109">Delegated (work or school account)</span></span>||
| <span data-ttu-id="a5a53-110">&nbsp; &nbsp; **Administración de dispositivos**</span><span class="sxs-lookup"><span data-stu-id="a5a53-110">&nbsp; &nbsp; **Device management**</span></span> | <span data-ttu-id="a5a53-111">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="a5a53-111">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
| <span data-ttu-id="a5a53-112">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="a5a53-112">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="a5a53-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="a5a53-113">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="a5a53-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5a53-114">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a5a53-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5a53-115">Not supported.</span></span>|
|<span data-ttu-id="a5a53-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5a53-116">Application</span></span>|<span data-ttu-id="a5a53-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5a53-117">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a5a53-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5a53-118">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deviceCategory
GET /deviceManagement/deviceCategories/{deviceCategoryId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="a5a53-119">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="a5a53-119">Optional query parameters</span></span>
<span data-ttu-id="a5a53-120">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5a53-120">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="a5a53-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5a53-121">Request headers</span></span>
|<span data-ttu-id="a5a53-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5a53-122">Header</span></span>|<span data-ttu-id="a5a53-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a5a53-123">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a5a53-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5a53-124">Authorization</span></span>|<span data-ttu-id="a5a53-125">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a5a53-125">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a5a53-126">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a5a53-126">Accept</span></span>|<span data-ttu-id="a5a53-127">application/json</span><span class="sxs-lookup"><span data-stu-id="a5a53-127">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a5a53-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a5a53-128">Request body</span></span>
<span data-ttu-id="a5a53-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a5a53-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a5a53-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5a53-130">Response</span></span>
<span data-ttu-id="a5a53-131">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceCategory](../resources/intune_shared_devicecategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5a53-131">If successful, this method returns a `200 OK` response code and [deviceCategory](../resources/intune_shared_devicecategory.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a5a53-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5a53-132">Example</span></span>

### <a name="request"></a><span data-ttu-id="a5a53-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5a53-133">Request</span></span>
<span data-ttu-id="a5a53-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5a53-134">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/detectedApps/{detectedAppId}/managedDevices/{managedDeviceId}/deviceCategory
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCategories/{deviceCategoryId}

```

### <a name="response"></a><span data-ttu-id="a5a53-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5a53-135">Response</span></span>
<span data-ttu-id="a5a53-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5a53-136">Here is an example of the response.</span></span> <span data-ttu-id="a5a53-137">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="a5a53-137">Note: The response object shown here may be truncated for brevity.</span></span> <span data-ttu-id="a5a53-138">Las propiedades que devuelve una llamada real varían según el contexto.</span><span class="sxs-lookup"><span data-stu-id="a5a53-138">Properties returned from an actual call vary according to context.</span></span>

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



