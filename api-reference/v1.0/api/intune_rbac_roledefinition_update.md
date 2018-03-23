# <a name="update-roledefinition"></a><span data-ttu-id="7b029-101">Actualizar roleDefinition</span><span class="sxs-lookup"><span data-stu-id="7b029-101">Update roleDefinition</span></span>

> <span data-ttu-id="7b029-102">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7b029-102">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7b029-103">Actualice las propiedades de un objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="7b029-103">Update the properties of a [calendar](../resources/intune_rbac_roledefinition.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7b029-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7b029-104">Prerequisites</span></span>
<span data-ttu-id="7b029-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7b029-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7b029-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7b029-107">Permission type</span></span>|<span data-ttu-id="7b029-108">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7b029-108">Permissions (from least to most privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7b029-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7b029-109">Delegated (work or school account)</span></span>|<span data-ttu-id="7b029-110">DeviceManagementRBAC.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="7b029-110">DeviceManagementRBAC.ReadWrite.All</span></span>|
|<span data-ttu-id="7b029-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7b029-111">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7b029-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7b029-112">Not supported.</span></span>|
|<span data-ttu-id="7b029-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7b029-113">Application</span></span>|<span data-ttu-id="7b029-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7b029-114">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7b029-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7b029-115">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}
PATCH /deviceManagement/roleDefinitions/{roleDefinitionId}/roleAssignments/{roleAssignmentId}/roleDefinition
```

## <a name="request-headers"></a><span data-ttu-id="7b029-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7b029-116">Request headers</span></span>
|<span data-ttu-id="7b029-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7b029-117">Header</span></span>|<span data-ttu-id="7b029-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7b029-118">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7b029-119">Autorización</span><span class="sxs-lookup"><span data-stu-id="7b029-119">Authorization</span></span>|<span data-ttu-id="7b029-120">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7b029-120">Bearer {token}. Required.</span></span>|
|<span data-ttu-id="7b029-121">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7b029-121">Accept</span></span>|<span data-ttu-id="7b029-122">application/json</span><span class="sxs-lookup"><span data-stu-id="7b029-122">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7b029-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7b029-123">Request body</span></span>
<span data-ttu-id="7b029-124">En el cuerpo de la solicitud, especifique una representación JSON del objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="7b029-124">In the request body, supply a JSON representation of the [Contact](../resources/intune_rbac_roledefinition.md) object.</span></span>

<span data-ttu-id="7b029-125">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [roleDefinition](../resources/intune_rbac_roledefinition.md).</span><span class="sxs-lookup"><span data-stu-id="7b029-125">The following table shows the properties that are required when you create a user.</span></span>

|<span data-ttu-id="7b029-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7b029-126">Property</span></span>|<span data-ttu-id="7b029-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="7b029-127">Type</span></span>|<span data-ttu-id="7b029-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="7b029-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7b029-129">id</span><span class="sxs-lookup"><span data-stu-id="7b029-129">id</span></span>|<span data-ttu-id="7b029-130">String</span><span class="sxs-lookup"><span data-stu-id="7b029-130">String</span></span>|<span data-ttu-id="7b029-131">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7b029-131">Key of the setting.</span></span> <span data-ttu-id="7b029-132">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="7b029-132">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="7b029-133">displayName</span><span class="sxs-lookup"><span data-stu-id="7b029-133">displayName</span></span>|<span data-ttu-id="7b029-134">String</span><span class="sxs-lookup"><span data-stu-id="7b029-134">String</span></span>|<span data-ttu-id="7b029-135">Nombre para mostrar de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="7b029-135">Display Name of the Role definition.</span></span>|
|<span data-ttu-id="7b029-136">description</span><span class="sxs-lookup"><span data-stu-id="7b029-136">description</span></span>|<span data-ttu-id="7b029-137">String</span><span class="sxs-lookup"><span data-stu-id="7b029-137">String</span></span>|<span data-ttu-id="7b029-138">Descripción de la definición de rol.</span><span class="sxs-lookup"><span data-stu-id="7b029-138">Description of the Role definition.</span></span>|
|<span data-ttu-id="7b029-139">rolePermissions</span><span class="sxs-lookup"><span data-stu-id="7b029-139">rolePermissions</span></span>|<span data-ttu-id="7b029-140">Colección [rolePermission](../resources/intune_rbac_rolepermission.md)</span><span class="sxs-lookup"><span data-stu-id="7b029-140">[rolePermission](../resources/intune_rbac_rolepermission.md) collection</span></span>|<span data-ttu-id="7b029-141">Lista de los permisos de rol que puede realizar este rol.</span><span class="sxs-lookup"><span data-stu-id="7b029-141">List of Role Permissions this role is allowed to perform.</span></span> <span data-ttu-id="7b029-142">Estos deben coincidir con el actionName que se definió como parte de rolePermission.</span><span class="sxs-lookup"><span data-stu-id="7b029-142">These must match the actionName that is defined as part of the rolePermission.</span></span>|
|<span data-ttu-id="7b029-143">isBuiltIn</span><span class="sxs-lookup"><span data-stu-id="7b029-143">isBuiltIn</span></span>|<span data-ttu-id="7b029-144">Boolean</span><span class="sxs-lookup"><span data-stu-id="7b029-144">Boolean</span></span>|<span data-ttu-id="7b029-145">Tipo de rol.</span><span class="sxs-lookup"><span data-stu-id="7b029-145">Type of Role.</span></span> <span data-ttu-id="7b029-146">Se establece en True si está integrado o en False si es una definición de rol personalizada.</span><span class="sxs-lookup"><span data-stu-id="7b029-146">Set to True if it is built-in, or set to False if it is a custom role definition.</span></span>|



## <a name="response"></a><span data-ttu-id="7b029-147">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b029-147">Response</span></span>
<span data-ttu-id="7b029-148">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [roleDefinition](../resources/intune_rbac_roledefinition.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7b029-148">If successful, this method returns a `200 OK` response code and an updated [contact](../resources/intune_rbac_roledefinition.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7b029-149">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7b029-149">Example</span></span>
### <a name="request"></a><span data-ttu-id="7b029-150">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7b029-150">Request</span></span>
<span data-ttu-id="7b029-151">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7b029-151">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/roleDefinitions/{roleDefinitionId}
Content-type: application/json
Content-length: 527

{
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

### <a name="response"></a><span data-ttu-id="7b029-152">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7b029-152">Response</span></span>
<span data-ttu-id="7b029-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7b029-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 629

{
  "@odata.type": "#microsoft.graph.roleDefinition",
  "id": "70fdcd08-cd08-70fd-08cd-fd7008cdfd70",
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



