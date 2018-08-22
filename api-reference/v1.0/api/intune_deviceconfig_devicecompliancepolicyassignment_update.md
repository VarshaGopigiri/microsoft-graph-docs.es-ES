# <a name="update-devicecompliancepolicyassignment"></a><span data-ttu-id="47b7e-101">Actualizar deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="47b7e-101">Update deviceCompliancePolicyAssignment</span></span>

> <span data-ttu-id="47b7e-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="47b7e-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="47b7e-103">Actualice las propiedades de un objeto [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="47b7e-103">Update the properties of a [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="47b7e-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="47b7e-104">Prerequisites</span></span>
<span data-ttu-id="47b7e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="47b7e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="47b7e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="47b7e-107">Permission type</span></span>|<span data-ttu-id="47b7e-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="47b7e-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="47b7e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="47b7e-109">Delegated (work or school account)</span></span>|<span data-ttu-id="47b7e-110">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="47b7e-110">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="47b7e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="47b7e-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="47b7e-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47b7e-112">Not supported.</span></span>|
|<span data-ttu-id="47b7e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="47b7e-113">Application</span></span>|<span data-ttu-id="47b7e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47b7e-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="47b7e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="47b7e-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments/{deviceCompliancePolicyAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="47b7e-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="47b7e-116">Request headers</span></span>
|<span data-ttu-id="47b7e-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47b7e-117">Header</span></span>|<span data-ttu-id="47b7e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="47b7e-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="47b7e-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="47b7e-119">Authorization</span></span>|<span data-ttu-id="47b7e-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="47b7e-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="47b7e-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="47b7e-121">Accept</span></span>|<span data-ttu-id="47b7e-122">application/json</span><span class="sxs-lookup"><span data-stu-id="47b7e-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="47b7e-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="47b7e-123">Request body</span></span>
<span data-ttu-id="47b7e-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="47b7e-124">In the request body, supply a JSON representation for the [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md) object.</span></span>

<span data-ttu-id="47b7e-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="47b7e-125">The following table shows the properties that are required when you create the [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md).</span></span>

|<span data-ttu-id="47b7e-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="47b7e-126">Property</span></span>|<span data-ttu-id="47b7e-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="47b7e-127">Type</span></span>|<span data-ttu-id="47b7e-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="47b7e-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="47b7e-129">id</span><span class="sxs-lookup"><span data-stu-id="47b7e-129">id</span></span>|<span data-ttu-id="47b7e-130">String</span><span class="sxs-lookup"><span data-stu-id="47b7e-130">String</span></span>|<span data-ttu-id="47b7e-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="47b7e-131">Key of the entity.</span></span>|
|<span data-ttu-id="47b7e-132">target</span><span class="sxs-lookup"><span data-stu-id="47b7e-132">target</span></span>|[<span data-ttu-id="47b7e-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="47b7e-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune_shared_deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="47b7e-134">Destino de la asignación de directivas de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="47b7e-134">Target for the compliance policy assignment.</span></span>|



## <a name="response"></a><span data-ttu-id="47b7e-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47b7e-135">Response</span></span>
<span data-ttu-id="47b7e-136">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="47b7e-136">If successful, this method returns a `200 OK` response code and an updated [deviceCompliancePolicyAssignment](../resources/intune_deviceconfig_devicecompliancepolicyassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="47b7e-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="47b7e-137">Example</span></span>
### <a name="request"></a><span data-ttu-id="47b7e-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="47b7e-138">Request</span></span>
<span data-ttu-id="47b7e-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="47b7e-139">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/assignments/{deviceCompliancePolicyAssignmentId}
Content-type: application/json
Content-length: 101

{
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```

### <a name="response"></a><span data-ttu-id="47b7e-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47b7e-140">Response</span></span>
<span data-ttu-id="47b7e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="47b7e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



