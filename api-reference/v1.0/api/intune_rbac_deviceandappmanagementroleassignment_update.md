# <a name="update-deviceandappmanagementroleassignment"></a><span data-ttu-id="cb9e3-101">Actualizar deviceAndAppManagementRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="cb9e3-101">Update deviceAndAppManagementRoleAssignment</span></span>

> <span data-ttu-id="cb9e3-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cb9e3-103">Actualice las propiedades de un objeto [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="cb9e3-103">Update the properties of a [calendar](../resources/intune_rbac_deviceandappmanagementroleassignment.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cb9e3-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cb9e3-104">Prerequisites</span></span>
<span data-ttu-id="cb9e3-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cb9e3-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="cb9e3-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cb9e3-107">Permission type</span></span>|<span data-ttu-id="cb9e3-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cb9e3-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cb9e3-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cb9e3-109">Delegated (work or school account)</span></span>|<span data-ttu-id="cb9e3-110">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cb9e3-110">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="cb9e3-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cb9e3-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cb9e3-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-112">Not supported.</span></span>|
|<span data-ttu-id="cb9e3-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cb9e3-113">Application</span></span>|<span data-ttu-id="cb9e3-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cb9e3-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cb9e3-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleAssignments/{deviceAndAppManagementRoleAssignmentId}
```

## <a name="request-headers"></a><span data-ttu-id="cb9e3-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cb9e3-116">Request headers</span></span>
|<span data-ttu-id="cb9e3-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb9e3-117">Header</span></span>|<span data-ttu-id="cb9e3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="cb9e3-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cb9e3-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="cb9e3-119">Authorization</span></span>|<span data-ttu-id="cb9e3-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="cb9e3-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cb9e3-121">Accept</span></span>|<span data-ttu-id="cb9e3-122">application/json</span><span class="sxs-lookup"><span data-stu-id="cb9e3-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cb9e3-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cb9e3-123">Request body</span></span>
<span data-ttu-id="cb9e3-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="cb9e3-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_rbac_deviceandappmanagementroleassignment.md) object.</span></span>

<span data-ttu-id="cb9e3-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="cb9e3-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="cb9e3-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cb9e3-126">Property</span></span>|<span data-ttu-id="cb9e3-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="cb9e3-127">Type</span></span>|<span data-ttu-id="cb9e3-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="cb9e3-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="cb9e3-129">id</span><span class="sxs-lookup"><span data-stu-id="cb9e3-129">id</span></span>|<span data-ttu-id="cb9e3-130">String</span><span class="sxs-lookup"><span data-stu-id="cb9e3-130">String</span></span>|<span data-ttu-id="cb9e3-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-131">Key of the setting.</span></span> <span data-ttu-id="cb9e3-132">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-132">This is read-only and automatically generated.</span></span> <span data-ttu-id="cb9e3-133">Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="cb9e3-133">Inherited from [roleAssignment](../resources/intune_rbac_roleassignment.md)</span></span>|
|<span data-ttu-id="cb9e3-134">displayName</span><span class="sxs-lookup"><span data-stu-id="cb9e3-134">displayName</span></span>|<span data-ttu-id="cb9e3-135">String</span><span class="sxs-lookup"><span data-stu-id="cb9e3-135">String</span></span>|<span data-ttu-id="cb9e3-136">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-136">The display or friendly name of the role Assignment.</span></span> <span data-ttu-id="cb9e3-137">Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="cb9e3-137">Inherited from [roleAssignment](../resources/intune_rbac_roleassignment.md)</span></span>|
|<span data-ttu-id="cb9e3-138">description</span><span class="sxs-lookup"><span data-stu-id="cb9e3-138">description</span></span>|<span data-ttu-id="cb9e3-139">String</span><span class="sxs-lookup"><span data-stu-id="cb9e3-139">String</span></span>|<span data-ttu-id="cb9e3-140">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-140">Description of the Role Assignment.</span></span> <span data-ttu-id="cb9e3-141">Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="cb9e3-141">Inherited from [roleAssignment](../resources/intune_rbac_roleassignment.md)</span></span>|
|<span data-ttu-id="cb9e3-142">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="cb9e3-142">resourceScopes</span></span>|<span data-ttu-id="cb9e3-143">Colección string</span><span class="sxs-lookup"><span data-stu-id="cb9e3-143">String collection</span></span>|<span data-ttu-id="cb9e3-144">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-144">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="cb9e3-145">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-145">These are IDs from Azure Active Directory.</span></span> <span data-ttu-id="cb9e3-146">Heredado de [roleAssignment](../resources/intune_rbac_roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="cb9e3-146">Inherited from [roleAssignment](../resources/intune_rbac_roleassignment.md)</span></span>|
|<span data-ttu-id="cb9e3-147">members</span><span class="sxs-lookup"><span data-stu-id="cb9e3-147">members</span></span>|<span data-ttu-id="cb9e3-148">Colección string</span><span class="sxs-lookup"><span data-stu-id="cb9e3-148">String collection</span></span>|<span data-ttu-id="cb9e3-149">La lista de identificadores de grupos de seguridad de miembros de roles.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-149">The list of ids of role member security groups.</span></span> <span data-ttu-id="cb9e3-150">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-150">These are IDs from Azure Active Directory.</span></span>|



## <a name="response"></a><span data-ttu-id="cb9e3-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb9e3-151">Response</span></span>
<span data-ttu-id="cb9e3-152">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceAndAppManagementRoleAssignment](../resources/intune_rbac_deviceandappmanagementroleassignment.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-152">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_rbac_deviceandappmanagementroleassignment.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cb9e3-153">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cb9e3-153">Example</span></span>
### <a name="request"></a><span data-ttu-id="cb9e3-154">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cb9e3-154">Request</span></span>
<span data-ttu-id="cb9e3-155">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-155">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/roleAssignments/{deviceAndAppManagementRoleAssignmentId}
Content-type: application/json
Content-length: 183

{
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

### <a name="response"></a><span data-ttu-id="cb9e3-156">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb9e3-156">Response</span></span>
<span data-ttu-id="cb9e3-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cb9e3-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
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



