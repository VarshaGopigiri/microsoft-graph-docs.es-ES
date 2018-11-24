# <a name="list-devicecategories"></a><span data-ttu-id="f43c7-101">Enumerar deviceCategories</span><span class="sxs-lookup"><span data-stu-id="f43c7-101">List deviceCategories</span></span>

> <span data-ttu-id="f43c7-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f43c7-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f43c7-103">Enumere las propiedades y las relaciones de los objetos [deviceCategory](../resources/intune_shared_devicecategory.md).</span><span class="sxs-lookup"><span data-stu-id="f43c7-103">List properties and relationships of the [deviceCategory](../resources/intune_shared_devicecategory.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f43c7-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f43c7-104">Prerequisites</span></span>
<span data-ttu-id="f43c7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f43c7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f43c7-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f43c7-107">Permission type</span></span>|<span data-ttu-id="f43c7-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f43c7-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f43c7-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f43c7-109">Delegated (work or school account)</span></span>||
| <span data-ttu-id="f43c7-110">&nbsp;&nbsp; **Incorporación**</span><span class="sxs-lookup"><span data-stu-id="f43c7-110">&nbsp; &nbsp; **Onboarding**</span></span> | <span data-ttu-id="f43c7-111">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="f43c7-111">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="f43c7-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f43c7-112">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f43c7-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f43c7-113">Not supported.</span></span>|
|<span data-ttu-id="f43c7-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f43c7-114">Application</span></span>|<span data-ttu-id="f43c7-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f43c7-115">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f43c7-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f43c7-116">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCategories
```

## <a name="request-headers"></a><span data-ttu-id="f43c7-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f43c7-117">Request headers</span></span>
|<span data-ttu-id="f43c7-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f43c7-118">Header</span></span>|<span data-ttu-id="f43c7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f43c7-119">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f43c7-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="f43c7-120">Authorization</span></span>|<span data-ttu-id="f43c7-121">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f43c7-121">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f43c7-122">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f43c7-122">Accept</span></span>|<span data-ttu-id="f43c7-123">application/json</span><span class="sxs-lookup"><span data-stu-id="f43c7-123">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f43c7-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f43c7-124">Request body</span></span>
<span data-ttu-id="f43c7-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f43c7-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f43c7-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f43c7-126">Response</span></span>
<span data-ttu-id="f43c7-127">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceCategory](../resources/intune_shared_devicecategory.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f43c7-127">If successful, this method returns a `200 OK` response code and a collection of [deviceCategory](../resources/intune_shared_devicecategory.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f43c7-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f43c7-128">Example</span></span>
### <a name="request"></a><span data-ttu-id="f43c7-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f43c7-129">Request</span></span>
<span data-ttu-id="f43c7-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f43c7-130">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCategories
```

### <a name="response"></a><span data-ttu-id="f43c7-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f43c7-131">Response</span></span>
<span data-ttu-id="f43c7-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f43c7-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 233

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceCategory",
      "id": "f881b841-b841-f881-41b8-81f841b881f8",
      "displayName": "Display Name value",
      "description": "Description value"
    }
  ]
}
```



