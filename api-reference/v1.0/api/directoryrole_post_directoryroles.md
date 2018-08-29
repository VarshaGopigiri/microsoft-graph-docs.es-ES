# <a name="activate-directoryrole"></a><span data-ttu-id="612ba-101">Activar directoryRole</span><span class="sxs-lookup"><span data-stu-id="612ba-101">Activate directoryRole</span></span>

<span data-ttu-id="612ba-p101">Active un rol de directorio. Para leer un rol de directorio o actualizar sus miembros, debe activarse primero en el inquilino. Solo se activan de manera predeterminada los administradores de la empresa y los roles del directorio de usuarios implícitos. Para acceder y asignar miembros a otro rol de directorio, primero debe activarlo con la plantilla de rol de directorio correspondiente ([directoryRoleTemplate](../resources/directoryroletemplate.md)).</span><span class="sxs-lookup"><span data-stu-id="612ba-p101">Activate a directory role. To read a directory role or update its members, it must first be activated in the tenant. Only the Company Administrators and the implicit Users directory roles are activated by default. To access and assign members to another directory role, you must first activate it with its corresponding directory role template ([directoryRoleTemplate](../resources/directoryroletemplate.md)).</span></span>

## <a name="permissions"></a><span data-ttu-id="612ba-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="612ba-106">Permissions</span></span>
<span data-ttu-id="612ba-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="612ba-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="612ba-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="612ba-109">Permission type</span></span>      | <span data-ttu-id="612ba-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="612ba-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="612ba-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="612ba-111">Delegated (work or school account)</span></span> | <span data-ttu-id="612ba-112">Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="612ba-112">Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="612ba-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="612ba-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="612ba-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="612ba-114">Not supported.</span></span>    |
|<span data-ttu-id="612ba-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="612ba-115">Application</span></span> | <span data-ttu-id="612ba-116">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="612ba-116">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="612ba-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="612ba-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /directoryRoles

```
## <a name="request-headers"></a><span data-ttu-id="612ba-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="612ba-118">Request headers</span></span>
| <span data-ttu-id="612ba-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="612ba-119">Name</span></span>       | <span data-ttu-id="612ba-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="612ba-120">Type</span></span> | <span data-ttu-id="612ba-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="612ba-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="612ba-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="612ba-122">Authorization</span></span>  | <span data-ttu-id="612ba-123">cadena</span><span class="sxs-lookup"><span data-stu-id="612ba-123">string</span></span>  | <span data-ttu-id="612ba-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="612ba-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="612ba-126">Content-Type</span><span class="sxs-lookup"><span data-stu-id="612ba-126">Content-Type</span></span>  | <span data-ttu-id="612ba-127">cadena</span><span class="sxs-lookup"><span data-stu-id="612ba-127">string</span></span>  | <span data-ttu-id="612ba-128">application/json</span><span class="sxs-lookup"><span data-stu-id="612ba-128">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="612ba-129">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="612ba-129">Request body</span></span>
<span data-ttu-id="612ba-130">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).</span><span class="sxs-lookup"><span data-stu-id="612ba-130">In the request body, supply a JSON representation of [directoryRole](../resources/directoryrole.md) object.</span></span>

<span data-ttu-id="612ba-131">En la tabla siguiente, se muestran las propiedades necesarias al activar un rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="612ba-131">The following table shows the properties that are required when you activate a directory role.</span></span>

|<span data-ttu-id="612ba-132">Parámetro</span><span class="sxs-lookup"><span data-stu-id="612ba-132">Parameter</span></span> | <span data-ttu-id="612ba-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="612ba-133">Type</span></span> | <span data-ttu-id="612ba-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="612ba-134">Description</span></span>|
|:---------|:---------|:---------|
|<span data-ttu-id="612ba-135">roleTemplateId</span><span class="sxs-lookup"><span data-stu-id="612ba-135">roleTemplateId</span></span> | <span data-ttu-id="612ba-136">cadena</span><span class="sxs-lookup"><span data-stu-id="612ba-136">string</span></span> | <span data-ttu-id="612ba-137">Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="612ba-137">Required.</span></span> <span data-ttu-id="612ba-138">El identificador del [directoryRoleTemplate](../resources/directoryroletemplate.md) en el que se basa el rol.</span><span class="sxs-lookup"><span data-stu-id="612ba-138">The ID of the [directoryRoleTemplate](../resources/directoryroletemplate.md) that the role is based on. This is the only property that may be specified in the request.</span></span> <span data-ttu-id="612ba-139">Esta es la única propiedad que se puede especificar en la solicitud.</span><span class="sxs-lookup"><span data-stu-id="612ba-139">The ID of the directoryRoleTemplate that the role is based on. This is the only property that may be specified in the request.</span></span>|

## <a name="response"></a><span data-ttu-id="612ba-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="612ba-140">Response</span></span>

<span data-ttu-id="612ba-141">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [directoryRole](../resources/directoryrole.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="612ba-141">If successful, this method returns `201 Created` response code and [directoryRole](../resources/directoryrole.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="612ba-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="612ba-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="612ba-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="612ba-143">Request</span></span>

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
<span data-ttu-id="612ba-144">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [directoryRole](../resources/directoryrole.md).</span><span class="sxs-lookup"><span data-stu-id="612ba-144">In the request body, supply a JSON representation of [directoryRole](../resources/directoryrole.md) object.</span></span>
##### <a name="response"></a><span data-ttu-id="612ba-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="612ba-145">Response</span></span>
<span data-ttu-id="612ba-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="612ba-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
