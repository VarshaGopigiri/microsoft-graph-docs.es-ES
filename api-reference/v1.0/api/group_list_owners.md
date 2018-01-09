# <a name="list-owners"></a><span data-ttu-id="cc410-101">Enumerar propietarios</span><span class="sxs-lookup"><span data-stu-id="cc410-101">List owners</span></span>
<span data-ttu-id="cc410-p101">Recupera una lista de propietarios del grupo. Los propietarios son un conjunto de usuarios no administradores que tienen permiso para modificar el objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="cc410-p101">Retrieve a list of the group's owners. The owners are a set of non-admin users who are allowed to modify the group object.</span></span> 

## <a name="permissions"></a><span data-ttu-id="cc410-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="cc410-104">Permissions</span></span>
<span data-ttu-id="cc410-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="cc410-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="cc410-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cc410-107">Permission type</span></span>      | <span data-ttu-id="cc410-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cc410-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cc410-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cc410-109">Delegated (work or school account)</span></span> | <span data-ttu-id="cc410-110">Group.Read.All y User.ReadBasic.All, Group.Read.All y User.Read.All, Group.Read.All y User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cc410-110">Group.Read.All and User.ReadBasic.All, Group.Read.All and User.Read.All, Group.Read.All and User.ReadWrite.All</span></span>   |
|<span data-ttu-id="cc410-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cc410-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cc410-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cc410-112">Not supported.</span></span>    |
|<span data-ttu-id="cc410-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cc410-113">Application</span></span> | <span data-ttu-id="cc410-114">Group.Read.All y User.Read.All, Group.Read.All y User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cc410-114">Group.Read.All and User.Read.All, Group.Read.All and User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cc410-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cc410-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/owners
```

## <a name="optional-query-parameters"></a><span data-ttu-id="cc410-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="cc410-116">Optional query parameters</span></span>
<span data-ttu-id="cc410-117">Este método admite los [parámetros de consulta de OData](../../../concepts/query_parameters.md) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc410-117">This method supports the [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="cc410-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cc410-118">Request headers</span></span>
| <span data-ttu-id="cc410-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="cc410-119">Name</span></span>       | <span data-ttu-id="cc410-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="cc410-120">Type</span></span> | <span data-ttu-id="cc410-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc410-121">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="cc410-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="cc410-122">Authorization</span></span>  | <span data-ttu-id="cc410-123">string</span><span class="sxs-lookup"><span data-stu-id="cc410-123">string</span></span>  | <span data-ttu-id="cc410-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="cc410-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="cc410-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cc410-126">Request body</span></span>
<span data-ttu-id="cc410-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cc410-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cc410-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc410-128">Response</span></span>
<span data-ttu-id="cc410-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [user](../resources/user.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc410-129">If successful, this method returns a `200 OK` response code and collection of [user](../resources/user.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cc410-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cc410-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="cc410-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cc410-131">Request</span></span>
<span data-ttu-id="cc410-132">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cc410-132">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_owners"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/owners
```

#### <a name="response"></a><span data-ttu-id="cc410-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cc410-133">Response</span></span>
<span data-ttu-id="cc410-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cc410-134">Here is an example of the response.</span></span>
><span data-ttu-id="cc410-135">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="cc410-135">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="cc410-136">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cc410-136">All the properties will be returned from an actual call.</span></span>
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
      "@odata.type": "#microsoft.graph.user"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List owners",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
