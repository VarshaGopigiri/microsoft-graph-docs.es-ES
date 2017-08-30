# <a name="list-memberof"></a><span data-ttu-id="fed38-101">List memberOf</span><span class="sxs-lookup"><span data-stu-id="fed38-101">List memberOf</span></span>

<span data-ttu-id="fed38-102">Obtiene grupos de los que el grupo sea miembro directo.</span><span class="sxs-lookup"><span data-stu-id="fed38-102">Get groups that the group is a direct member of.</span></span> 

<span data-ttu-id="fed38-p101">Esta operación no es transitiva. A diferencia de la obtención de grupos de Office 365 de un usuario, devuelve todos los tipos de grupos, no solo los grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="fed38-p101">This operation is not transitive. Unlike getting a user's Office 365 Groups, this returns all types of groups, not just Office 365 groups.</span></span> 

## <a name="permissions"></a><span data-ttu-id="fed38-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="fed38-105">Permissions</span></span>
<span data-ttu-id="fed38-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="fed38-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="fed38-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fed38-108">Permission type</span></span>      | <span data-ttu-id="fed38-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fed38-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fed38-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fed38-110">Delegated (work or school account)</span></span> | <span data-ttu-id="fed38-111">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="fed38-111">Group.Read.All</span></span>    |
|<span data-ttu-id="fed38-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fed38-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fed38-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="fed38-113">Not supported.</span></span>    |
|<span data-ttu-id="fed38-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fed38-114">Application</span></span> | <span data-ttu-id="fed38-115">Group.Read.All</span><span class="sxs-lookup"><span data-stu-id="fed38-115">Group.Read.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="fed38-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fed38-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /groups/{id}/memberOf
```
## <a name="optional-query-parameters"></a><span data-ttu-id="fed38-117">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="fed38-117">Optional query parameters</span></span>
<span data-ttu-id="fed38-118">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fed38-118">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="fed38-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fed38-119">Request headers</span></span>
| <span data-ttu-id="fed38-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="fed38-120">Name</span></span>       | <span data-ttu-id="fed38-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="fed38-121">Type</span></span> | <span data-ttu-id="fed38-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="fed38-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="fed38-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="fed38-123">Authorization</span></span>  | <span data-ttu-id="fed38-124">string</span><span class="sxs-lookup"><span data-stu-id="fed38-124">string</span></span>  | <span data-ttu-id="fed38-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fed38-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="fed38-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fed38-127">Request body</span></span>
<span data-ttu-id="fed38-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="fed38-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="fed38-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fed38-129">Response</span></span>

<span data-ttu-id="fed38-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y la colección de objetos [directoryObject](../resources/directoryobject.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fed38-130">If successful, this method returns a `200 OK` response code and collection of [directoryObject](../resources/directoryobject.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="fed38-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fed38-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fed38-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fed38-132">Request</span></span>
<span data-ttu-id="fed38-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fed38-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_memberof"
}-->
```http
GET https://graph.microsoft.com/v1.0/groups/{id}/memberOf
```
##### <a name="response"></a><span data-ttu-id="fed38-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fed38-134">Response</span></span>
<span data-ttu-id="fed38-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fed38-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "List memberOf",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->