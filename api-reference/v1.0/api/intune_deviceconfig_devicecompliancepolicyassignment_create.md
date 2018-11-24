# <a name="create-devicecompliancepolicyassignment"></a><span data-ttu-id="32364-101">Crear deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="32364-101">Create deviceCompliancePolicyAssignment</span></span>

> <span data-ttu-id="32364-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="32364-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="32364-103">Cree un objeto [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="32364-103">Create a new [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="32364-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="32364-104">Prerequisites</span></span>
<span data-ttu-id="32364-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="32364-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="32364-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="32364-107">Permission type</span></span>|<span data-ttu-id="32364-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="32364-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="32364-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="32364-109">Delegated (work or school account)</span></span>|<span data-ttu-id="32364-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="32364-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="32364-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="32364-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="32364-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32364-112">Not supported.</span></span>|
|<span data-ttu-id="32364-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="32364-113">Application</span></span>|<span data-ttu-id="32364-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="32364-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="32364-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="32364-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments
```

## <a name="request-headers"></a><span data-ttu-id="32364-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="32364-116">Request headers</span></span>
|<span data-ttu-id="32364-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="32364-117">Header</span></span>|<span data-ttu-id="32364-118">Valor</span><span class="sxs-lookup"><span data-stu-id="32364-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="32364-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="32364-119">Authorization</span></span>|<span data-ttu-id="32364-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="32364-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="32364-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="32364-121">Accept</span></span>|<span data-ttu-id="32364-122">application/json</span><span class="sxs-lookup"><span data-stu-id="32364-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="32364-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="32364-123">Request body</span></span>
<span data-ttu-id="32364-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceCompliancePolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="32364-124">In the request body, supply a JSON representation for the deviceCompliancePolicyAssignment object.</span></span>

<span data-ttu-id="32364-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceCompliancePolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="32364-125">The following table shows the properties that are required when you create the deviceCompliancePolicyAssignment.</span></span>

|<span data-ttu-id="32364-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32364-126">Property</span></span>|<span data-ttu-id="32364-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="32364-127">Type</span></span>|<span data-ttu-id="32364-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="32364-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="32364-129">id</span><span class="sxs-lookup"><span data-stu-id="32364-129">id</span></span>|<span data-ttu-id="32364-130">String</span><span class="sxs-lookup"><span data-stu-id="32364-130">String</span></span>|<span data-ttu-id="32364-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="32364-131">Key of the entity.</span></span>|
|<span data-ttu-id="32364-132">target</span><span class="sxs-lookup"><span data-stu-id="32364-132">target</span></span>|[<span data-ttu-id="32364-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="32364-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="32364-134">Destino de la asignación de directivas de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="32364-134">Target for the compliance policy assignment.</span></span>|



## <a name="response"></a><span data-ttu-id="32364-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32364-135">Response</span></span>
<span data-ttu-id="32364-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="32364-136">If successful, this method returns a `201 Created` response code and a [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="32364-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="32364-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="32364-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="32364-138">Request</span></span>
<span data-ttu-id="32364-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="32364-139">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="32364-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="32364-140">Response</span></span>
<span data-ttu-id="32364-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="32364-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



