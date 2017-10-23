# <a name="activate-directoryrole"></a><span data-ttu-id="ab6f6-101">Activar directoryRole</span><span class="sxs-lookup"><span data-stu-id="ab6f6-101">Activate directoryRole</span></span>

<span data-ttu-id="ab6f6-p101">Active un rol de directorio. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activan de manera predeterminada los administradores de la empresa y los roles del directorio de usuarios implícitos. Para acceder y asignar miembros a otro rol de directorio, primero debe activarlo con la plantilla de rol de directorio correspondiente ([directoryRoleTemplate](../resources/directoryroletemplate.md)).</span><span class="sxs-lookup"><span data-stu-id="ab6f6-p101">Activate a directory role. To read a directory role or update its members, it must first be activated in the tenant. Only the Company Administrators and the implicit Users directory roles are activated by default. To access and assign members to another directory role, you must first activate it with its corresponding directory role template ([directoryRoleTemplate](../resources/directoryroletemplate.md)).</span></span>

## <a name="permissions"></a><span data-ttu-id="ab6f6-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="ab6f6-106">Permissions</span></span>
<span data-ttu-id="ab6f6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="ab6f6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="ab6f6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ab6f6-109">Permission type</span></span>      | <span data-ttu-id="ab6f6-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ab6f6-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ab6f6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ab6f6-111">Delegated (work or school account)</span></span> | <span data-ttu-id="ab6f6-112">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="ab6f6-112">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="ab6f6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ab6f6-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ab6f6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ab6f6-114">Not supported.</span></span>    |
|<span data-ttu-id="ab6f6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ab6f6-115">Application</span></span> | <span data-ttu-id="ab6f6-116">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ab6f6-116">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="ab6f6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ab6f6-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /directoryRoles

```
## <a name="request-headers"></a><span data-ttu-id="ab6f6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ab6f6-118">Request headers</span></span>
| <span data-ttu-id="ab6f6-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="ab6f6-119">Name</span></span>       | <span data-ttu-id="ab6f6-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab6f6-120">Type</span></span> | <span data-ttu-id="ab6f6-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab6f6-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ab6f6-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="ab6f6-122">Authorization</span></span>  | <span data-ttu-id="ab6f6-123">string</span><span class="sxs-lookup"><span data-stu-id="ab6f6-123">string</span></span>  | <span data-ttu-id="ab6f6-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ab6f6-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ab6f6-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ab6f6-126">Content-Type</span></span>  | <span data-ttu-id="ab6f6-127">application/json</span><span class="sxs-lookup"><span data-stu-id="ab6f6-127">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="ab6f6-128">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="ab6f6-128">Request body</span></span>
<span data-ttu-id="ab6f6-129">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).</span><span class="sxs-lookup"><span data-stu-id="ab6f6-129">In the request body, supply a JSON representation of [directoryRole](../resources/directoryrole.md) object.</span></span>

<span data-ttu-id="ab6f6-130">En la tabla siguiente, se muestran las propiedades necesarias al activar un rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="ab6f6-130">The following table shows the properties that are required when you activate a directory role.</span></span>

|<span data-ttu-id="ab6f6-131">Parámetro obligatorio</span><span class="sxs-lookup"><span data-stu-id="ab6f6-131">Required parameter</span></span> | <span data-ttu-id="ab6f6-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="ab6f6-132">Type</span></span> | <span data-ttu-id="ab6f6-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="ab6f6-133">Description</span></span>|
|:---------|:---------|:---------|
|<span data-ttu-id="ab6f6-134">roleTemplateId</span><span class="sxs-lookup"><span data-stu-id="ab6f6-134">roleTemplateId</span></span> | <span data-ttu-id="ab6f6-135">string</span><span class="sxs-lookup"><span data-stu-id="ab6f6-135">string</span></span> | <span data-ttu-id="ab6f6-p104">El identificador de la [directoryRoleTemplate](../resources/directoryroletemplate.md) en que se basa el rol. Es la única propiedad que se puede especificar en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ab6f6-p104">The ID of the [directoryRoleTemplate](../resources/directoryroletemplate.md) that the role is based on. This is the only property that may be specified in the request.</span></span>|

## <a name="response"></a><span data-ttu-id="ab6f6-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab6f6-138">Response</span></span>

<span data-ttu-id="ab6f6-139">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ab6f6-139">If successful, this method returns `201 Created` response code and [directoryRole](../resources/directoryrole.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ab6f6-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab6f6-140">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ab6f6-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ab6f6-141">Request</span></span>

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
<span data-ttu-id="ab6f6-142">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).</span><span class="sxs-lookup"><span data-stu-id="ab6f6-142">In the request body, supply a JSON representation of [directoryRole](../resources/directoryrole.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="ab6f6-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ab6f6-143">Response</span></span>
<span data-ttu-id="ab6f6-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ab6f6-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
