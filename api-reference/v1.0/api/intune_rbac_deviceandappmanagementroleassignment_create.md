# <a name="create-deviceandappmanagementroleassignment"></a><span data-ttu-id="59e9b-101">Crear deviceAndAppManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="59e9b-101">Create deviceAndAppManagementRoleAssignment</span></span>

> <span data-ttu-id="59e9b-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="59e9b-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="59e9b-103">Cree un objeto [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="59e9b-103">Create a new [plannerBucket](../resources/intune_rbac_deviceandappmanagementroleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="59e9b-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="59e9b-104">Prerequisites</span></span>
<span data-ttu-id="59e9b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="59e9b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="59e9b-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="59e9b-107">Permission type</span></span>|<span data-ttu-id="59e9b-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="59e9b-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="59e9b-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="59e9b-109">Delegated (work or school account)</span></span>|<span data-ttu-id="59e9b-110">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="59e9b-110">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="59e9b-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="59e9b-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="59e9b-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59e9b-112">Not supported.</span></span>|
|<span data-ttu-id="59e9b-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="59e9b-113">Application</span></span>|<span data-ttu-id="59e9b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="59e9b-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="59e9b-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="59e9b-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleAssignments
```

## <a name="request-headers"></a><span data-ttu-id="59e9b-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="59e9b-116">Request headers</span></span>
|<span data-ttu-id="59e9b-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="59e9b-117">Header</span></span>|<span data-ttu-id="59e9b-118">Valor</span><span class="sxs-lookup"><span data-stu-id="59e9b-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="59e9b-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="59e9b-119">Authorization</span></span>|<span data-ttu-id="59e9b-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="59e9b-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="59e9b-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="59e9b-121">Accept</span></span>|<span data-ttu-id="59e9b-122">application/json</span><span class="sxs-lookup"><span data-stu-id="59e9b-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="59e9b-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="59e9b-123">Request body</span></span>
<span data-ttu-id="59e9b-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceAndAppManagementRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="59e9b-124">In the request body, supply a JSON representation of the schemaExtension object.</span></span>

<span data-ttu-id="59e9b-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceAndAppManagementRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="59e9b-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="59e9b-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="59e9b-126">Property</span></span>|<span data-ttu-id="59e9b-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="59e9b-127">Type</span></span>|<span data-ttu-id="59e9b-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="59e9b-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="59e9b-129">id</span><span class="sxs-lookup"><span data-stu-id="59e9b-129">id</span></span>|<span data-ttu-id="59e9b-130">String</span><span class="sxs-lookup"><span data-stu-id="59e9b-130">String</span></span>|<span data-ttu-id="59e9b-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="59e9b-131">Key of the setting.</span></span> <span data-ttu-id="59e9b-132">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="59e9b-132">This is read-only and automatically generated.</span></span> <span data-ttu-id="59e9b-133">Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="59e9b-133">Inherited from [roleAssignment](../resources/intune_rbac_roleassignment.md)</span></span>|
|<span data-ttu-id="59e9b-134">displayName</span><span class="sxs-lookup"><span data-stu-id="59e9b-134">displayName</span></span>|<span data-ttu-id="59e9b-135">String</span><span class="sxs-lookup"><span data-stu-id="59e9b-135">String</span></span>|<span data-ttu-id="59e9b-136">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="59e9b-136">The display or friendly name of the role Assignment.</span></span> <span data-ttu-id="59e9b-137">Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="59e9b-137">Inherited from [roleAssignment](../resources/intune_rbac_roleassignment.md)</span></span>|
|<span data-ttu-id="59e9b-138">description</span><span class="sxs-lookup"><span data-stu-id="59e9b-138">description</span></span>|<span data-ttu-id="59e9b-139">String</span><span class="sxs-lookup"><span data-stu-id="59e9b-139">String</span></span>|<span data-ttu-id="59e9b-140">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="59e9b-140">Description of the Role Assignment.</span></span> <span data-ttu-id="59e9b-141">Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="59e9b-141">Inherited from [roleAssignment](../resources/intune_rbac_roleassignment.md)</span></span>|
|<span data-ttu-id="59e9b-142">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="59e9b-142">resourceScopes</span></span>|<span data-ttu-id="59e9b-143">Colección string</span><span class="sxs-lookup"><span data-stu-id="59e9b-143">String collection</span></span>|<span data-ttu-id="59e9b-144">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="59e9b-144">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="59e9b-145">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="59e9b-145">These are IDs from Azure Active Directory.</span></span> <span data-ttu-id="59e9b-146">Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="59e9b-146">Inherited from [roleAssignment](../resources/intune_rbac_roleassignment.md)</span></span>|
|<span data-ttu-id="59e9b-147">members</span><span class="sxs-lookup"><span data-stu-id="59e9b-147">members</span></span>|<span data-ttu-id="59e9b-148">Colección string</span><span class="sxs-lookup"><span data-stu-id="59e9b-148">String collection</span></span>|<span data-ttu-id="59e9b-149">La lista de identificadores de grupos de seguridad de miembros de roles.</span><span class="sxs-lookup"><span data-stu-id="59e9b-149">The list of ids of role member security groups.</span></span> <span data-ttu-id="59e9b-150">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="59e9b-150">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="59e9b-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59e9b-151">Response</span></span>
<span data-ttu-id="59e9b-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="59e9b-152">If successful, this method returns a `201 Created` response code and a [DriveItemVersion](../resources/intune_rbac_deviceandappmanagementroleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="59e9b-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="59e9b-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="59e9b-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="59e9b-154">Request</span></span>
<span data-ttu-id="59e9b-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="59e9b-155">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/roleAssignments
Content-type: application/json
Content-length: 258

{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleAssignment",
  "displayName": "Display Name value",
  "description": "Description value",
  "resourceScopes": [
    "Resource Scopes value"
  ],
  "members": [
    "Members value"
  ]
}
```

### <a name="response"></a><span data-ttu-id="59e9b-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="59e9b-156">Response</span></span>
<span data-ttu-id="59e9b-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="59e9b-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 307

{
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
```



