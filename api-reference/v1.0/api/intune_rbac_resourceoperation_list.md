# <a name="list-resourceoperations"></a><span data-ttu-id="98273-101">Enumerar resourceOperations</span><span class="sxs-lookup"><span data-stu-id="98273-101">List resourceOperations</span></span>

> <span data-ttu-id="98273-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="98273-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="98273-103">Enumere las propiedades y las relaciones de los objetos [resourceOperation](../resources/intune_rbac_resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="98273-103">List properties and relationships of the [resourceOperation](../resources/intune_rbac_resourceoperation.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="98273-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="98273-104">Prerequisites</span></span>
<span data-ttu-id="98273-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="98273-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="98273-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="98273-107">Permission type</span></span>|<span data-ttu-id="98273-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="98273-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="98273-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="98273-109">Delegated (work or school account)</span></span>|<span data-ttu-id="98273-110">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="98273-110">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="98273-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="98273-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="98273-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98273-112">Not supported.</span></span>|
|<span data-ttu-id="98273-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="98273-113">Application</span></span>|<span data-ttu-id="98273-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="98273-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="98273-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="98273-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/resourceOperations
```

## <a name="request-headers"></a><span data-ttu-id="98273-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="98273-116">Request headers</span></span>
|<span data-ttu-id="98273-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98273-117">Header</span></span>|<span data-ttu-id="98273-118">Valor</span><span class="sxs-lookup"><span data-stu-id="98273-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="98273-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="98273-119">Authorization</span></span>|<span data-ttu-id="98273-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="98273-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="98273-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="98273-121">Accept</span></span>|<span data-ttu-id="98273-122">application/json</span><span class="sxs-lookup"><span data-stu-id="98273-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="98273-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="98273-123">Request body</span></span>
<span data-ttu-id="98273-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="98273-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="98273-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98273-125">Response</span></span>
<span data-ttu-id="98273-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [resourceOperation](../resources/intune_rbac_resourceoperation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="98273-126">If successful, this method returns a `200 OK` response code and a collection of [resourceOperation](../resources/intune_rbac_resourceoperation.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="98273-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="98273-127">Example</span></span>
### <a name="request"></a><span data-ttu-id="98273-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="98273-128">Request</span></span>
<span data-ttu-id="98273-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="98273-129">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/resourceOperations
```

### <a name="response"></a><span data-ttu-id="98273-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="98273-130">Response</span></span>
<span data-ttu-id="98273-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="98273-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 280

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.resourceOperation",
      "id": "232b8fee-8fee-232b-ee8f-2b23ee8f2b23",
      "resourceName": "Resource Name value",
      "actionName": "Action Name value",
      "description": "Description value"
    }
  ]
}
```



