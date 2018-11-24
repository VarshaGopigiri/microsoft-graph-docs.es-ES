# <a name="create-deviceandappmanagementroledefinition"></a><span data-ttu-id="82662-101">Crear deviceAndAppManagementRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="82662-101">Create deviceAndAppManagementRoleDefinition</span></span>

> <span data-ttu-id="82662-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="82662-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="82662-103">Cree un objeto [deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="82662-103">Create a new [deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="82662-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="82662-104">Prerequisites</span></span>
<span data-ttu-id="82662-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="82662-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="82662-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="82662-107">Permission type</span></span>|<span data-ttu-id="82662-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="82662-108">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="82662-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="82662-109">Delegated (work or school account)</span></span>|<span data-ttu-id="82662-110">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="82662-110">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="82662-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="82662-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="82662-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82662-112">Not supported.</span></span>|
|<span data-ttu-id="82662-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="82662-113">Application</span></span>|<span data-ttu-id="82662-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="82662-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="82662-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="82662-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/roleDefinitions
```

## <a name="request-headers"></a><span data-ttu-id="82662-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="82662-116">Request headers</span></span>
|<span data-ttu-id="82662-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="82662-117">Header</span></span>|<span data-ttu-id="82662-118">Valor</span><span class="sxs-lookup"><span data-stu-id="82662-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="82662-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="82662-119">Authorization</span></span>|<span data-ttu-id="82662-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="82662-120">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="82662-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="82662-121">Accept</span></span>|<span data-ttu-id="82662-122">application/json</span><span class="sxs-lookup"><span data-stu-id="82662-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="82662-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="82662-123">Request body</span></span>
<span data-ttu-id="82662-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceAndAppManagementRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="82662-124">In the request body, supply a JSON representation for the deviceAndAppManagementRoleDefinition object.</span></span>

<span data-ttu-id="82662-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceAndAppManagementRoleDefinition.</span><span class="sxs-lookup"><span data-stu-id="82662-125">The following table shows the properties that are required when you create the deviceAndAppManagementRoleDefinition.</span></span>

|<span data-ttu-id="82662-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="82662-126">Property</span></span>|<span data-ttu-id="82662-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="82662-127">Type</span></span>|<span data-ttu-id="82662-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="82662-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="82662-129">id</span><span class="sxs-lookup"><span data-stu-id="82662-129">id</span></span>|<span data-ttu-id="82662-130">String</span><span class="sxs-lookup"><span data-stu-id="82662-130">String</span></span>|<span data-ttu-id="82662-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="82662-131">Key of the entity.</span></span> <span data-ttu-id="82662-132">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="82662-132">This is read-only and automatically generated.</span></span> <span data-ttu-id="82662-133">Heredado de [roleDefinition](../resources/intune_rbac_roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="82662-133">Inherited from [roleDefinition](../resources/intune_rbac_roledefinition.md)</span></span>|
|<span data-ttu-id="82662-134">displayName</span><span class="sxs-lookup"><span data-stu-id="82662-134">displayName</span></span>|<span data-ttu-id="82662-135">String</span><span class="sxs-lookup"><span data-stu-id="82662-135">String</span></span>|<span data-ttu-id="82662-136">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="82662-136">Display Name of the Role definition.</span></span> <span data-ttu-id="82662-137">Heredado de [roleDefinition](../resources/intune_rbac_roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="82662-137">Inherited from [roleDefinition](../resources/intune_rbac_roledefinition.md)</span></span>|
|<span data-ttu-id="82662-138">description</span><span class="sxs-lookup"><span data-stu-id="82662-138">description</span></span>|<span data-ttu-id="82662-139">String</span><span class="sxs-lookup"><span data-stu-id="82662-139">String</span></span>|<span data-ttu-id="82662-140">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="82662-140">Description of the Role definition.</span></span> <span data-ttu-id="82662-141">Heredado de [roleDefinition](../resources/intune_rbac_roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="82662-141">Inherited from [roleDefinition](../resources/intune_rbac_roledefinition.md)</span></span>|
|<span data-ttu-id="82662-142">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="82662-142">rolePermissions</span></span>|<span data-ttu-id="82662-143">Colección [rolePermission](../resources/intune_rbac_rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="82662-143">[rolePermission](../resources/intune_rbac_rolepermission.md) collection</span></span>|<span data-ttu-id="82662-144">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="82662-144">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="82662-145">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="82662-145">These must match the actionName that is defined as part of the rolePermission.</span></span> <span data-ttu-id="82662-146">Heredado de [roleDefinition](../resources/intune_rbac_roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="82662-146">Inherited from [roleDefinition](../resources/intune_rbac_roledefinition.md)</span></span>|
|<span data-ttu-id="82662-147">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="82662-147">isBuiltIn</span></span>|<span data-ttu-id="82662-148">Booleano</span><span class="sxs-lookup"><span data-stu-id="82662-148">Boolean</span></span>|<span data-ttu-id="82662-149">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="82662-149">Type of Role.</span></span> <span data-ttu-id="82662-150">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="82662-150">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span> <span data-ttu-id="82662-151">Heredado de [roleDefinition](../resources/intune_rbac_roledefinition.md)</span><span class="sxs-lookup"><span data-stu-id="82662-151">Inherited from [roleDefinition](../resources/intune_rbac_roledefinition.md)</span></span>|



## <a name="response"></a><span data-ttu-id="82662-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82662-152">Response</span></span>
<span data-ttu-id="82662-153">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="82662-153">If successful, this method returns a `201 Created` response code and a [deviceAndAppManagementRoleDefinition](../resources/intune_rbac_deviceandappmanagementroledefinition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="82662-154">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="82662-154">Example</span></span>
### <a name="request"></a><span data-ttu-id="82662-155">Solicitud</span><span class="sxs-lookup"><span data-stu-id="82662-155">Request</span></span>
<span data-ttu-id="82662-156">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="82662-156">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions
Content-type: application/json
Content-length: 602

{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleDefinition",
  "displayName": "Display Name value",
  "description": "Description value",
  "rolePermissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "resourceActions": [
        {
          "@odata.type": "microsoft.graph.resourceAction",
          "allowedResourceActions": [
            "Allowed Resource Actions value"
          ],
          "notAllowedResourceActions": [
            "Not Allowed Resource Actions value"
          ]
        }
      ]
    }
  ],
  "isBuiltIn": true
}
```

### <a name="response"></a><span data-ttu-id="82662-157">Respuesta</span><span class="sxs-lookup"><span data-stu-id="82662-157">Response</span></span>
<span data-ttu-id="82662-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="82662-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 651

{
  "@odata.type": "#microsoft.graph.deviceAndAppManagementRoleDefinition",
  "id": "bca1dfb5-dfb5-bca1-b5df-a1bcb5dfa1bc",
  "displayName": "Display Name value",
  "description": "Description value",
  "rolePermissions": [
    {
      "@odata.type": "microsoft.graph.rolePermission",
      "resourceActions": [
        {
          "@odata.type": "microsoft.graph.resourceAction",
          "allowedResourceActions": [
            "Allowed Resource Actions value"
          ],
          "notAllowedResourceActions": [
            "Not Allowed Resource Actions value"
          ]
        }
      ]
    }
  ],
  "isBuiltIn": true
}
```



