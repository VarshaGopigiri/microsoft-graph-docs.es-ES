# <a name="create-devicecompliancepolicyassignment"></a><span data-ttu-id="fb206-101">Crear deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="fb206-101">Create deviceCompliancePolicyAssignment</span></span>

> <span data-ttu-id="fb206-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="fb206-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="fb206-103">Cree un objeto [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="fb206-103">Create a new [plannerBucket](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="fb206-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fb206-104">Prerequisites</span></span>
<span data-ttu-id="fb206-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fb206-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fb206-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fb206-107">Permission type</span></span>|<span data-ttu-id="fb206-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fb206-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="fb206-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fb206-109">Delegated (work or school account)</span></span>|<span data-ttu-id="fb206-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fb206-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="fb206-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fb206-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="fb206-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb206-112">Not supported.</span></span>|
|<span data-ttu-id="fb206-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fb206-113">Application</span></span>|<span data-ttu-id="fb206-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fb206-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="fb206-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fb206-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="fb206-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fb206-116">Request headers</span></span>
|<span data-ttu-id="fb206-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fb206-117">Header</span></span>|<span data-ttu-id="fb206-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fb206-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="fb206-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="fb206-119">Authorization</span></span>|<span data-ttu-id="fb206-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="fb206-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="fb206-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="fb206-121">Accept</span></span>|<span data-ttu-id="fb206-122">application/json</span><span class="sxs-lookup"><span data-stu-id="fb206-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="fb206-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fb206-123">Request body</span></span>
<span data-ttu-id="fb206-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceCompliancePolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fb206-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="fb206-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceCompliancePolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="fb206-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="fb206-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fb206-126">Property</span></span>|<span data-ttu-id="fb206-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb206-127">Type</span></span>|<span data-ttu-id="fb206-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb206-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="fb206-129">id</span><span class="sxs-lookup"><span data-stu-id="fb206-129">id</span></span>|<span data-ttu-id="fb206-130">String</span><span class="sxs-lookup"><span data-stu-id="fb206-130">String</span></span>|<span data-ttu-id="fb206-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="fb206-131">Key of the setting.</span></span>|
|<span data-ttu-id="fb206-132">target</span><span class="sxs-lookup"><span data-stu-id="fb206-132">target</span></span>|[<span data-ttu-id="fb206-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="fb206-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_deviceconfig_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="fb206-134">Destino de la asignación de directivas de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="fb206-134">Target for the compliance policy assignment.</span></span>|



## <a name="response"></a><span data-ttu-id="fb206-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb206-135">Response</span></span>
<span data-ttu-id="fb206-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fb206-136">If successful, this method returns a `201 Created` response code and a [section](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="fb206-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fb206-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="fb206-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fb206-138">Request</span></span>
<span data-ttu-id="fb206-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fb206-139">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments
Content-type: application/json
Content-length: 172

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyAssignment",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="fb206-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fb206-140">Response</span></span>
<span data-ttu-id="fb206-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fb206-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 221

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyAssignment",
  "id": "92dc3fef-3fef-92dc-ef3f-dc92ef3fdc92",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```



