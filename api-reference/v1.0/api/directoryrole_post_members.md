# <a name="add-directory-role-member"></a><span data-ttu-id="7ec22-101">Add directory role member</span><span class="sxs-lookup"><span data-stu-id="7ec22-101">Add directory role member</span></span>

<span data-ttu-id="7ec22-102">Usa esta API para crear un miembro de rol de directorio.</span><span class="sxs-lookup"><span data-stu-id="7ec22-102">Use this API to create a new directory role member.</span></span>

## <a name="permissions"></a><span data-ttu-id="7ec22-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="7ec22-103">Permissions</span></span>
<span data-ttu-id="7ec22-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7ec22-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7ec22-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7ec22-106">Permission type</span></span>      | <span data-ttu-id="7ec22-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7ec22-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7ec22-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7ec22-108">Delegated (work or school account)</span></span> | <span data-ttu-id="7ec22-109">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="7ec22-109">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="7ec22-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7ec22-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7ec22-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7ec22-111">Not supported.</span></span>    |
|<span data-ttu-id="7ec22-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7ec22-112">Application</span></span> | <span data-ttu-id="7ec22-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7ec22-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7ec22-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7ec22-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /directoryRoles/{id}/members/$ref

```
## <a name="request-headers"></a><span data-ttu-id="7ec22-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7ec22-115">Request headers</span></span>
| <span data-ttu-id="7ec22-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="7ec22-116">Name</span></span>       | <span data-ttu-id="7ec22-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="7ec22-117">Type</span></span> | <span data-ttu-id="7ec22-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="7ec22-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7ec22-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="7ec22-119">Authorization</span></span>  | <span data-ttu-id="7ec22-120">string</span><span class="sxs-lookup"><span data-stu-id="7ec22-120">string</span></span>  | <span data-ttu-id="7ec22-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7ec22-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="7ec22-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="7ec22-123">Content-Type</span></span>  | <span data-ttu-id="7ec22-124">application/json</span><span class="sxs-lookup"><span data-stu-id="7ec22-124">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="7ec22-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7ec22-125">Request body</span></span>
<span data-ttu-id="7ec22-126">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [directoryObject](../resources/directoryobject.md) o [user](../resources/user.md) que se va a agregar.</span><span class="sxs-lookup"><span data-stu-id="7ec22-126">In the request body, supply a JSON representation of a [directoryObject](../resources/directoryobject.md) or [user](../resources/user.md) object to be added.</span></span>

## <a name="response"></a><span data-ttu-id="7ec22-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ec22-127">Response</span></span>

<span data-ttu-id="7ec22-128">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="7ec22-128">If successful, this method returns `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="7ec22-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ec22-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7ec22-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7ec22-130">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "create_directoryobject_from_directoryrole"
}-->
```http
POST https://graph.microsoft.com/v1.0/directoryRoles/{id}/members
Content-type: application/json

{
  "@odata.id": "https://graph.microsoft.com/v1.0/directoryObjects/{id}"
}
```

##### <a name="response"></a><span data-ttu-id="7ec22-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7ec22-131">Response</span></span>
<span data-ttu-id="7ec22-132">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar.</span><span class="sxs-lookup"><span data-stu-id="7ec22-132">Note: The response object shown here may be truncated for brevity.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject"
} -->
```http
HTTP/1.1 204 No Content
Content-type: text/plain

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create member",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->