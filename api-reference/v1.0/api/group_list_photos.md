# <a name="list-photos"></a><span data-ttu-id="25a0a-101">Enumerar fotos</span><span class="sxs-lookup"><span data-stu-id="25a0a-101">List photos</span></span>
<span data-ttu-id="25a0a-102">Recupere una lista de objetos [profilePhoto](../resources/profilephoto.md).</span><span class="sxs-lookup"><span data-stu-id="25a0a-102">Retrieve a list of [profilePhoto](../resources/profilephoto.md) objects.</span></span>

## <a name="permissions"></a><span data-ttu-id="25a0a-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="25a0a-103">Permissions</span></span>
<span data-ttu-id="25a0a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="25a0a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="25a0a-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="25a0a-106">Permission type</span></span>      | <span data-ttu-id="25a0a-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="25a0a-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="25a0a-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="25a0a-108">Delegated (work or school account)</span></span> | <span data-ttu-id="25a0a-109">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="25a0a-109">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span></span> |
|<span data-ttu-id="25a0a-110">Delegado (cuenta Microsoft personal)</span><span class="sxs-lookup"><span data-stu-id="25a0a-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="25a0a-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="25a0a-111">Not supported.</span></span>    |
|<span data-ttu-id="25a0a-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="25a0a-112">Application</span></span> | <span data-ttu-id="25a0a-113">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="25a0a-113">Group.ReadBasic.All, Group.Read.All, Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="25a0a-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="25a0a-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/photos
GET /users/{id | userPrincipalName}/joinedGroups/{id}/photos
```
## <a name="optional-query-parameters"></a><span data-ttu-id="25a0a-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="25a0a-115">Optional query parameters</span></span>
<span data-ttu-id="25a0a-116">Este método admite los [parámetros de consulta de OData](../../../concepts/query_parameters.md) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25a0a-116">This method supports the [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="25a0a-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="25a0a-117">Request headers</span></span>
| <span data-ttu-id="25a0a-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="25a0a-118">Name</span></span>       | <span data-ttu-id="25a0a-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="25a0a-119">Type</span></span> | <span data-ttu-id="25a0a-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="25a0a-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="25a0a-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="25a0a-121">Authorization</span></span>  | <span data-ttu-id="25a0a-122">string</span><span class="sxs-lookup"><span data-stu-id="25a0a-122">string</span></span>  | <span data-ttu-id="25a0a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="25a0a-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="25a0a-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="25a0a-125">Request body</span></span>
<span data-ttu-id="25a0a-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="25a0a-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="25a0a-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25a0a-127">Response</span></span>
<span data-ttu-id="25a0a-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [profilePhoto](../resources/profilephoto.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25a0a-128">If successful, this method returns a `200 OK` response code and collection of [profilePhoto](../resources/profilephoto.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="25a0a-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="25a0a-129">Example</span></span>
#### <a name="request"></a><span data-ttu-id="25a0a-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="25a0a-130">Request</span></span>
<span data-ttu-id="25a0a-131">Este es un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="25a0a-131">The following is an example of making the request in ASP.NET that uses the TokenHelper file:</span></span>
<!-- {
  "blockType": "request",
  "name": "get_photos"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/photos
```

#### <a name="response"></a><span data-ttu-id="25a0a-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="25a0a-132">Response</span></span>
<span data-ttu-id="25a0a-133">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="25a0a-133">Here is an example of the response.</span></span>
><span data-ttu-id="25a0a-134">**Nota:** Se puede acortar el objeto de respuesta que se muestra aquí para mejorar la legibilidad.</span><span class="sxs-lookup"><span data-stu-id="25a0a-134">**Note:** The response object shown here might be shortened for readability.</span></span> <span data-ttu-id="25a0a-135">Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="25a0a-135">All the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.profilePhoto",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 94

{
  "value": [
    {
      "height": 99,
      "width": 99,
      "id": "id-value"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List photos",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
