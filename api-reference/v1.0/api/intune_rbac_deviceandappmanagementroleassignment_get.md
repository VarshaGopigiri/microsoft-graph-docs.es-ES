# <a name="get-deviceandappmanagementroleassignment"></a><span data-ttu-id="3f8df-101">Obtener deviceAndAppManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3f8df-101">Get deviceAndAppManagementRoleAssignment</span></span>

> <span data-ttu-id="3f8df-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="3f8df-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="3f8df-103">Lea las propiedades y las relaciones del objeto [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="3f8df-103">Read properties and relationships of the [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="3f8df-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="3f8df-104">Prerequisites</span></span>
<span data-ttu-id="3f8df-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="3f8df-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="3f8df-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3f8df-107">Permission type</span></span>|<span data-ttu-id="3f8df-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3f8df-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="3f8df-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3f8df-109">Delegated (work or school account)</span></span>|<span data-ttu-id="3f8df-110">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span><span class="sxs-lookup"><span data-stu-id="3f8df-110">DeviceManagementRBAC.ReadWrite.All, DeviceManagementRBAC.Read.All</span></span>|
|<span data-ttu-id="3f8df-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3f8df-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="3f8df-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f8df-112">Not supported.</span></span>|
|<span data-ttu-id="3f8df-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3f8df-113">Application</span></span>|<span data-ttu-id="3f8df-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f8df-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="3f8df-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3f8df-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/roleAssignments/{deviceAndAppManagementRoleAssignmentId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="3f8df-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="3f8df-116">Optional query parameters</span></span>
<span data-ttu-id="3f8df-117">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f8df-117">This method supports the [OData Query Parameters](https://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="3f8df-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f8df-118">Request headers</span></span>
|<span data-ttu-id="3f8df-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f8df-119">Header</span></span>|<span data-ttu-id="3f8df-120">Valor</span><span class="sxs-lookup"><span data-stu-id="3f8df-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="3f8df-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="3f8df-121">Authorization</span></span>|<span data-ttu-id="3f8df-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="3f8df-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="3f8df-123">Accept</span><span class="sxs-lookup"><span data-stu-id="3f8df-123">Accept</span></span>|<span data-ttu-id="3f8df-124">application/json</span><span class="sxs-lookup"><span data-stu-id="3f8df-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="3f8df-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3f8df-125">Request body</span></span>
<span data-ttu-id="3f8df-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="3f8df-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="3f8df-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f8df-127">Response</span></span>
<span data-ttu-id="3f8df-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f8df-128">If successful, this method returns a `200 OK` response code and [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3f8df-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f8df-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="3f8df-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3f8df-130">Request</span></span>
<span data-ttu-id="3f8df-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f8df-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/roleAssignments/{deviceAndAppManagementRoleAssignmentId}
```

### <a name="response"></a><span data-ttu-id="3f8df-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f8df-132">Response</span></span>
<span data-ttu-id="3f8df-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="3f8df-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 346

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleAssignment",
    "id": "a12e8ebb-8ebb-a12e-bb8e-2ea1bb8e2ea1",
    "displayName": "Display Name value",
    "description": "Description value",
    "resourceScopes": [
      "Resource Scopes value"
    ],
    "members": [
      "Members value"
    ]
  }
}
```








