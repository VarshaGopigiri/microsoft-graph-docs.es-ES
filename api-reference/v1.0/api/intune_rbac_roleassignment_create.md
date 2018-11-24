# <a name="create-roleassignment"></a><span data-ttu-id="6ab29-101">Crear roleAssignment</span><span class="sxs-lookup"><span data-stu-id="6ab29-101">Create roleAssignment</span></span>

> <span data-ttu-id="6ab29-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="6ab29-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="6ab29-103">Cree un objeto [roleAssignment](../resources/intune_rbac_roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="6ab29-103">Create a new [roleAssignment](../resources/intune_rbac_roleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="6ab29-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6ab29-104">Prerequisites</span></span>
<span data-ttu-id="6ab29-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6ab29-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6ab29-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6ab29-107">Permission type</span></span>|<span data-ttu-id="6ab29-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6ab29-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="6ab29-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6ab29-109">Delegated (work or school account)</span></span>|<span data-ttu-id="6ab29-110">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="6ab29-110">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="6ab29-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6ab29-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="6ab29-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ab29-112">Not supported.</span></span>|
|<span data-ttu-id="6ab29-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6ab29-113">Application</span></span>|<span data-ttu-id="6ab29-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="6ab29-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="6ab29-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6ab29-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments
```

## <a name="request-headers"></a><span data-ttu-id="6ab29-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6ab29-116">Request headers</span></span>
|<span data-ttu-id="6ab29-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ab29-117">Header</span></span>|<span data-ttu-id="6ab29-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6ab29-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="6ab29-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="6ab29-119">Authorization</span></span>|<span data-ttu-id="6ab29-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="6ab29-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="6ab29-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="6ab29-121">Accept</span></span>|<span data-ttu-id="6ab29-122">application/json</span><span class="sxs-lookup"><span data-stu-id="6ab29-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="6ab29-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6ab29-123">Request body</span></span>
<span data-ttu-id="6ab29-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto roleAssignment.</span><span class="sxs-lookup"><span data-stu-id="6ab29-124">In the request body, supply a JSON representation for the roleAssignment object.</span></span>

<span data-ttu-id="6ab29-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto roleAssignment.</span><span class="sxs-lookup"><span data-stu-id="6ab29-125">The following table shows the properties that are required when you create the roleAssignment.</span></span>

|<span data-ttu-id="6ab29-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6ab29-126">Property</span></span>|<span data-ttu-id="6ab29-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ab29-127">Type</span></span>|<span data-ttu-id="6ab29-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ab29-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="6ab29-129">id</span><span class="sxs-lookup"><span data-stu-id="6ab29-129">id</span></span>|<span data-ttu-id="6ab29-130">String</span><span class="sxs-lookup"><span data-stu-id="6ab29-130">String</span></span>|<span data-ttu-id="6ab29-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="6ab29-131">Key of the entity.</span></span> <span data-ttu-id="6ab29-132">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="6ab29-132">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="6ab29-133">displayName</span><span class="sxs-lookup"><span data-stu-id="6ab29-133">displayName</span></span>|<span data-ttu-id="6ab29-134">String</span><span class="sxs-lookup"><span data-stu-id="6ab29-134">String</span></span>|<span data-ttu-id="6ab29-135">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="6ab29-135">The display or friendly name of the role Assignment.</span></span>|
|<span data-ttu-id="6ab29-136">description</span><span class="sxs-lookup"><span data-stu-id="6ab29-136">description</span></span>|<span data-ttu-id="6ab29-137">String</span><span class="sxs-lookup"><span data-stu-id="6ab29-137">String</span></span>|<span data-ttu-id="6ab29-138">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="6ab29-138">Description of the Role Assignment.</span></span>|
|<span data-ttu-id="6ab29-139">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="6ab29-139">resourceScopes</span></span>|<span data-ttu-id="6ab29-140">Colección string</span><span class="sxs-lookup"><span data-stu-id="6ab29-140">String collection</span></span>|<span data-ttu-id="6ab29-141">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="6ab29-141">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="6ab29-142">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6ab29-142">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="6ab29-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ab29-143">Response</span></span>
<span data-ttu-id="6ab29-144">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [roleAssignment](../resources/intune_rbac_roleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6ab29-144">If successful, this method returns a `201 Created` response code and a [roleAssignment](../resources/intune_rbac_roleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6ab29-145">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6ab29-145">Example</span></span>
### <a name="request"></a><span data-ttu-id="6ab29-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6ab29-146">Request</span></span>
<span data-ttu-id="6ab29-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6ab29-147">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments
Content-type: application/json
Content-length: 193

{
  "@odata.type": "#microsoft.graph.roleAssignment",
  "displayName": "Display Name value",
  "description": "Description value",
  "resourceScopes": [
    "Resource Scopes value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="6ab29-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6ab29-148">Response</span></span>
<span data-ttu-id="6ab29-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6ab29-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 242

{
  "@odata.type": "#microsoft.graph.roleAssignment",
  "id": "b3234d24-4d24-b323-244d-23b3244d23b3",
  "displayName": "Display Name value",
  "description": "Description value",
  "resourceScopes": [
    "Resource Scopes value"
  ]
}
```



