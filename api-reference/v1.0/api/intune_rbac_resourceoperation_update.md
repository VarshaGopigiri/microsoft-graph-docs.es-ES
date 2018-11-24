# <a name="update-resourceoperation"></a><span data-ttu-id="6f091-101">Actualizar resourceOperation</span><span class="sxs-lookup"><span data-stu-id="6f091-101">Update resourceOperation</span></span>

> <span data-ttu-id="6f091-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6f091-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6f091-103">Actualice las propiedades de un objeto [resourceOperation](../resources/intune_rbac_resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="6f091-103">Update the properties of a [resourceOperation](../resources/intune_rbac_resourceoperation.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6f091-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6f091-104">Prerequisites</span></span>
<span data-ttu-id="6f091-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6f091-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6f091-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6f091-107">Permission type</span></span>|<span data-ttu-id="6f091-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6f091-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6f091-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6f091-109">Delegated (work or school account)</span></span>|<span data-ttu-id="6f091-110">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6f091-110">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="6f091-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6f091-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6f091-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6f091-112">Not supported.</span></span>|
|<span data-ttu-id="6f091-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6f091-113">Application</span></span>|<span data-ttu-id="6f091-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6f091-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6f091-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6f091-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/resourceOperations/{resourceOperationId}
```

## <a name="request-headers"></a><span data-ttu-id="6f091-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6f091-116">Request headers</span></span>
|<span data-ttu-id="6f091-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6f091-117">Header</span></span>|<span data-ttu-id="6f091-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6f091-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6f091-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="6f091-119">Authorization</span></span>|<span data-ttu-id="6f091-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6f091-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6f091-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6f091-121">Accept</span></span>|<span data-ttu-id="6f091-122">application/json</span><span class="sxs-lookup"><span data-stu-id="6f091-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6f091-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6f091-123">Request body</span></span>
<span data-ttu-id="6f091-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [resourceOperation](../resources/intune_rbac_resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="6f091-124">In the request body, supply a JSON representation for the [resourceOperation](../resources/intune_rbac_resourceoperation.md) object.</span></span>

<span data-ttu-id="6f091-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [resourceOperation](../resources/intune_rbac_resourceoperation.md).</span><span class="sxs-lookup"><span data-stu-id="6f091-125">The following table shows the properties that are required when you create the [resourceOperation](../resources/intune_rbac_resourceoperation.md).</span></span>

|<span data-ttu-id="6f091-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6f091-126">Property</span></span>|<span data-ttu-id="6f091-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="6f091-127">Type</span></span>|<span data-ttu-id="6f091-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="6f091-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6f091-129">id</span><span class="sxs-lookup"><span data-stu-id="6f091-129">id</span></span>|<span data-ttu-id="6f091-130">String</span><span class="sxs-lookup"><span data-stu-id="6f091-130">String</span></span>|<span data-ttu-id="6f091-131">Clave de la operación de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f091-131">Key of the Resource Operation.</span></span> <span data-ttu-id="6f091-132">Solo lectura, generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="6f091-132">Read-only, automatically generated.</span></span>|
|<span data-ttu-id="6f091-133">resourceName</span><span class="sxs-lookup"><span data-stu-id="6f091-133">resourceName</span></span>|<span data-ttu-id="6f091-134">String</span><span class="sxs-lookup"><span data-stu-id="6f091-134">String</span></span>|<span data-ttu-id="6f091-135">Nombre del recurso en el que se realiza esta operación.</span><span class="sxs-lookup"><span data-stu-id="6f091-135">Name of the Resource this operation is performed on.</span></span>|
|<span data-ttu-id="6f091-136">actionName</span><span class="sxs-lookup"><span data-stu-id="6f091-136">actionName</span></span>|<span data-ttu-id="6f091-137">String</span><span class="sxs-lookup"><span data-stu-id="6f091-137">String</span></span>|<span data-ttu-id="6f091-138">Tipo de acción que va a realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="6f091-138">Type of action this operation is going to perform.</span></span> <span data-ttu-id="6f091-139">El actionName debe ser conciso y limitado al menor número de palabras posible.</span><span class="sxs-lookup"><span data-stu-id="6f091-139">The actionName should be concise and limited to as few words as possible.</span></span>|
|<span data-ttu-id="6f091-140">description</span><span class="sxs-lookup"><span data-stu-id="6f091-140">description</span></span>|<span data-ttu-id="6f091-141">String</span><span class="sxs-lookup"><span data-stu-id="6f091-141">String</span></span>|<span data-ttu-id="6f091-142">Descripción de la operación de recursos.</span><span class="sxs-lookup"><span data-stu-id="6f091-142">Description of the resource operation.</span></span> <span data-ttu-id="6f091-143">La descripción se usa en el texto al pasar el mouse para la operación si se muestra en Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="6f091-143">The description is used in mouse-over text for the operation when shown in the Azure Portal.</span></span>|



## <a name="response"></a><span data-ttu-id="6f091-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f091-144">Response</span></span>
<span data-ttu-id="6f091-145">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [resourceOperation](../resources/intune_rbac_resourceoperation.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6f091-145">If successful, this method returns a `200 OK` response code and an updated [resourceOperation](../resources/intune_rbac_resourceoperation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6f091-146">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6f091-146">Example</span></span>
### <a name="request"></a><span data-ttu-id="6f091-147">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6f091-147">Request</span></span>
<span data-ttu-id="6f091-148">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6f091-148">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/resourceOperations/{resourceOperationId}
Content-type: application/json
Content-length: 178

{
  "@odata.type": "#microsoft.graph.resourceOperation",
  "resourceName": "Resource Name value",
  "actionName": "Action Name value",
  "description": "Description value"
}
```

### <a name="response"></a><span data-ttu-id="6f091-149">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6f091-149">Response</span></span>
<span data-ttu-id="6f091-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6f091-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 227

{
  "@odata.type": "#microsoft.graph.resourceOperation",
  "id": "232b8fee-8fee-232b-ee8f-2b23ee8f2b23",
  "resourceName": "Resource Name value",
  "actionName": "Action Name value",
  "description": "Description value"
}
```



