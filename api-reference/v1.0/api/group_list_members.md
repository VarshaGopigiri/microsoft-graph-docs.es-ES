# <a name="list-members"></a><span data-ttu-id="df907-101">Enumerar miembros</span><span class="sxs-lookup"><span data-stu-id="df907-101">List members</span></span>
<span data-ttu-id="df907-p101">Obtiene una lista de los miembros directos del grupo. Un grupo puede tener usuarios, contactos y otros grupos como miembros. Esta operación no es transitiva.</span><span class="sxs-lookup"><span data-stu-id="df907-p101">Get a list of the group's direct members. A group can have users, contacts, and other groups as members. This operation is not transitive.</span></span>

## <a name="permissions"></a><span data-ttu-id="df907-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="df907-105">Permissions</span></span>
<span data-ttu-id="df907-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="df907-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="df907-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="df907-108">Permission type</span></span>      | <span data-ttu-id="df907-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="df907-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="df907-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="df907-110">Delegated (work or school account)</span></span> | <span data-ttu-id="df907-111">User.ReadBasic.All, User.Read.All, Directory.Read.All, Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="df907-111">User.ReadBasic.All, User.Read.All, Directory.Read.All, Directory.AccessAsUser.All</span></span>   |
|<span data-ttu-id="df907-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="df907-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="df907-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="df907-113">Not supported.</span></span>    |
|<span data-ttu-id="df907-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="df907-114">Application</span></span> | <span data-ttu-id="df907-115">User.Read.All, Directory.Read.All</span><span class="sxs-lookup"><span data-stu-id="df907-115">User.Read.All, Directory.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="df907-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="df907-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/members
```

## <a name="optional-query-parameters"></a><span data-ttu-id="df907-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="df907-117">Optional query parameters</span></span>
<span data-ttu-id="df907-118">Este método admite los [parámetros de consulta de OData](../../../concepts/query_parameters.md) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="df907-118">This method supports the [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="df907-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="df907-119">Request headers</span></span>
| <span data-ttu-id="df907-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="df907-120">Name</span></span>       | <span data-ttu-id="df907-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="df907-121">Type</span></span> | <span data-ttu-id="df907-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="df907-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="df907-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="df907-123">Authorization</span></span>  | <span data-ttu-id="df907-124">string</span><span class="sxs-lookup"><span data-stu-id="df907-124">string</span></span>  | <span data-ttu-id="df907-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="df907-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="df907-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="df907-127">Request body</span></span>
<span data-ttu-id="df907-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="df907-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="df907-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df907-129">Response</span></span>
<span data-ttu-id="df907-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="df907-130">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="df907-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="df907-131">Example</span></span>
#### <a name="request"></a><span data-ttu-id="df907-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="df907-132">Request</span></span>
<span data-ttu-id="df907-133">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="df907-133">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_members"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/members
```

#### <a name="response"></a><span data-ttu-id="df907-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="df907-134">Response</span></span>
<span data-ttu-id="df907-135">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="df907-135">Here is an example of the response.</span></span>
><span data-ttu-id="df907-136">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="df907-136">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="df907-137">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="df907-137">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.directoryObject",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 55

{
  "value": [
    {
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List members",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->