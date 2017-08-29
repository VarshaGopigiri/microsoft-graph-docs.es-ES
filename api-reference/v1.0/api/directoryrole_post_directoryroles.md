# <a name="activate-directoryrole"></a><span data-ttu-id="e1b29-101">Activar directoryRole</span><span class="sxs-lookup"><span data-stu-id="e1b29-101">Activate directoryRole</span></span>

<span data-ttu-id="e1b29-p101">Active un rol de directorio. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activan de manera predeterminada los administradores de la empresa y los roles del directorio de usuarios implícitos. Para acceder y asignar miembros a otro rol de directorio, primero debe activarlo con la plantilla de rol de directorio correspondiente ([directoryRoleTemplate](../resources/directoryroletemplate.md)).</span><span class="sxs-lookup"><span data-stu-id="e1b29-p101">Activate a directory role. To read a directory role or update its members, it must first be activated in the tenant. Only the Company Administrators and the implicit Users directory roles are activated by default. To access and assign members to another directory role, you must first activate it with its corresponding directory role template ([directoryRoleTemplate](../resources/directoryroletemplate.md)).</span></span>

## <a name="permissions"></a><span data-ttu-id="e1b29-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="e1b29-106">Permissions</span></span>
<span data-ttu-id="e1b29-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e1b29-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e1b29-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e1b29-109">Permission type</span></span>      | <span data-ttu-id="e1b29-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e1b29-110">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="e1b29-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e1b29-111">Delegated (work or school account)</span></span> | <span data-ttu-id="e1b29-112">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="e1b29-112">Directory.ReadWrite.All or Directory.AccessAsUser.All</span></span>    | 
|<span data-ttu-id="e1b29-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e1b29-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e1b29-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e1b29-114">Not supported.</span></span>    | 
|<span data-ttu-id="e1b29-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e1b29-115">Application</span></span> | <span data-ttu-id="e1b29-116">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e1b29-116">Directory.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="e1b29-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e1b29-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /directoryRoles

```
## <a name="request-headers"></a><span data-ttu-id="e1b29-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e1b29-118">Request headers</span></span>
| <span data-ttu-id="e1b29-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="e1b29-119">Name</span></span>       | <span data-ttu-id="e1b29-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1b29-120">Type</span></span> | <span data-ttu-id="e1b29-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1b29-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e1b29-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="e1b29-122">Authorization</span></span>  | <span data-ttu-id="e1b29-123">string</span><span class="sxs-lookup"><span data-stu-id="e1b29-123">string</span></span>  | <span data-ttu-id="e1b29-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e1b29-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e1b29-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e1b29-126">Content-Type</span></span>  | <span data-ttu-id="e1b29-127">application/json</span><span class="sxs-lookup"><span data-stu-id="e1b29-127">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="e1b29-128">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="e1b29-128">Request body</span></span>
<span data-ttu-id="e1b29-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).</span><span class="sxs-lookup"><span data-stu-id="e1b29-129">In the request body, supply a JSON representation of [directoryRole](../resources/directoryrole.md) object.</span></span>

<span data-ttu-id="e1b29-130">En la tabla siguiente, se muestran las propiedades necesarias al activar un rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="e1b29-130">The following table shows the properties that are required when you activate a directory role.</span></span>

|<span data-ttu-id="e1b29-131">Parámetro obligatorio</span><span class="sxs-lookup"><span data-stu-id="e1b29-131">Required parameter</span></span> | <span data-ttu-id="e1b29-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="e1b29-132">Type</span></span> | <span data-ttu-id="e1b29-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="e1b29-133">Description</span></span>|
|:---------|:---------|:---------|
|<span data-ttu-id="e1b29-134">roleTemplateId</span><span class="sxs-lookup"><span data-stu-id="e1b29-134">roleTemplateId</span></span> | <span data-ttu-id="e1b29-135">string</span><span class="sxs-lookup"><span data-stu-id="e1b29-135">string</span></span> | <span data-ttu-id="e1b29-p104">El identificador de la [directoryRoleTemplate](../resources/directoryroletemplate.md) en que se basa el rol. Es la única propiedad que se puede especificar en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e1b29-p104">The ID of the [directoryRoleTemplate](../resources/directoryroletemplate.md) that the role is based on. This is the only property that may be specified in the request.</span></span>|

## <a name="response"></a><span data-ttu-id="e1b29-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1b29-138">Response</span></span>

<span data-ttu-id="e1b29-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `201, Created` y el objeto [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e1b29-139">If successful, this method returns `201, Created` response code and [directoryRole](../resources/directoryrole.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e1b29-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e1b29-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e1b29-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e1b29-141">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_directoryrole_from_directoryroles"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryRoles
Content-type: application/json

{
  "roleTemplateId": "roleTemplateId-value"
}
```
<span data-ttu-id="e1b29-142">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).</span><span class="sxs-lookup"><span data-stu-id="e1b29-142">In the request body, supply a JSON representation of [directoryRole](../resources/directoryrole.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="e1b29-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e1b29-143">Response</span></span>
<span data-ttu-id="e1b29-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e1b29-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryRole"
} -->
```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "description": "description-value",
  "displayName": "displayName-value",
  "roleTemplateId": "roleTemplateId-value",
  "id": "id-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create directoryRole",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
