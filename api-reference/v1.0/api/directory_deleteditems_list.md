# <a name="list-deleted-items"></a><span data-ttu-id="520f2-101">Enumerar elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="520f2-101">List deleted items</span></span>

<span data-ttu-id="520f2-102">Recuperar una lista de elementos eliminados recientemente de [elementos eliminados](../resources/directory.md).</span><span class="sxs-lookup"><span data-stu-id="520f2-102">Retrieve a list of recently deleted items from [deleted items](../resources/directory.md).</span></span>

<span data-ttu-id="520f2-103">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los recursos [group](../resources/group.md) y [user](../resources/user.md).</span><span class="sxs-lookup"><span data-stu-id="520f2-103">Currently, deleted items functionality is only supported for the [group](../resources/group.md) and [user](../resources/user.md) resources.</span></span>

## <a name="permissions"></a><span data-ttu-id="520f2-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="520f2-104">Permissions</span></span>
<span data-ttu-id="520f2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="520f2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

### <a name="for-users"></a><span data-ttu-id="520f2-107">Para los usuarios:</span><span class="sxs-lookup"><span data-stu-id="520f2-107">For users:</span></span>

|<span data-ttu-id="520f2-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="520f2-108">Permission type</span></span>      | <span data-ttu-id="520f2-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="520f2-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="520f2-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="520f2-110">Delegated (work or school account)</span></span> | <span data-ttu-id="520f2-111">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="520f2-111">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="520f2-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="520f2-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="520f2-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="520f2-113">Not supported.</span></span> |
|<span data-ttu-id="520f2-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="520f2-114">Application</span></span> | <span data-ttu-id="520f2-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="520f2-115">User.Read.All, User.ReadWrite.All, Directory.Read.All, Directory.ReadWrite.All</span></span> |

### <a name="for-groups"></a><span data-ttu-id="520f2-116">Para los grupos:</span><span class="sxs-lookup"><span data-stu-id="520f2-116">For groups:</span></span>

|<span data-ttu-id="520f2-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="520f2-117">Permission type</span></span>      | <span data-ttu-id="520f2-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="520f2-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="520f2-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="520f2-119">Delegated (work or school account)</span></span> | <span data-ttu-id="520f2-120">Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="520f2-120">Group.Read.All, Group.ReadWrite.All, Directory.Read.All, Directory.AccessAsUser.All</span></span> |
|<span data-ttu-id="520f2-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="520f2-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="520f2-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="520f2-122">Not supported.</span></span>    |
|<span data-ttu-id="520f2-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="520f2-123">Application</span></span> | <span data-ttu-id="520f2-124">Group.Read.All, Group.ReadWrite.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="520f2-124">Group.Read.All, Group.ReadWrite.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="520f2-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="520f2-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http 
GET /directory/deletedItems/microsoft.graph.group
GET /directory/deletedItems/microsoft.graph.user
```

<span data-ttu-id="520f2-126">Actualmente, esta API admite la recuperación de tipos de objeto de grupos (microsoft.graph.group) o de usuarios (microsoft.graph.user) de los elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="520f2-126">This API currently supports retrieving object types of groups (microsoft.graph.group) or users (microsoft.graph.user) from deleted items.</span></span> <span data-ttu-id="520f2-127">El tipo se especifica como parte necesaria del URI.</span><span class="sxs-lookup"><span data-stu-id="520f2-127">The type is specified as a required part of the URI.</span></span> <span data-ttu-id="520f2-128">Llamar a GET/directory/deletedItems sin un tipo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="520f2-128">Calling GET /directory/deletedItems without a type is not supported.</span></span>

## <a name="optional-query-parameters"></a><span data-ttu-id="520f2-129">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="520f2-129">Optional query parameters</span></span>
<span data-ttu-id="520f2-130">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="520f2-130">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="520f2-131">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="520f2-131">Request headers</span></span>
| <span data-ttu-id="520f2-132">Nombre</span><span class="sxs-lookup"><span data-stu-id="520f2-132">Name</span></span>      |<span data-ttu-id="520f2-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="520f2-133">Description</span></span>|
|:----------|:----------|
| <span data-ttu-id="520f2-134">Authorization</span><span class="sxs-lookup"><span data-stu-id="520f2-134">Authorization</span></span>  | <span data-ttu-id="520f2-135">&lt;Código&gt; de portador *necesario*</span><span class="sxs-lookup"><span data-stu-id="520f2-135">Bearer &lt;code&gt; *Required*</span></span>|
| <span data-ttu-id="520f2-136">Accept</span><span class="sxs-lookup"><span data-stu-id="520f2-136">Accept</span></span>  | <span data-ttu-id="520f2-137">application/json</span><span class="sxs-lookup"><span data-stu-id="520f2-137">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="520f2-138">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="520f2-138">Request body</span></span>
<span data-ttu-id="520f2-139">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="520f2-139">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="520f2-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="520f2-140">Response</span></span>

<span data-ttu-id="520f2-141">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="520f2-141">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="520f2-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="520f2-142">Example</span></span>
##### <a name="request"></a><span data-ttu-id="520f2-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="520f2-143">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "get_deleteditems"
}-->
```http
GET https://graph.microsoft.com/v1.0/directory/deletedItems/microsoft.graph.group
```
##### <a name="response"></a><span data-ttu-id="520f2-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="520f2-144">Response</span></span>
<span data-ttu-id="520f2-p103">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="520f2-p103">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#groups",
  "value": [
    {
      "id":"46cc6179-19d0-473e-97ad-6ff84347bbbb",
      "displayName":"SampleGroup",
      "groupTypes":["Unified"],
      "mail":"example@contoso.com",
      "mailEnabled":true,
      "mailNickname":"Example",
      "securityEnabled":false,
      "visibility":"Public"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List deleteditems",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->