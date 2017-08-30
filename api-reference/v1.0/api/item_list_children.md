# <a name="list-children-of-a-driveitem"></a><span data-ttu-id="79582-101">Mostrar los elementos secundarios de un objeto driveItem</span><span class="sxs-lookup"><span data-stu-id="79582-101">List children of a driveItem</span></span>

<span data-ttu-id="79582-102">Devuelva una colección de objetos [DriveItem](../resources/driveitem.md) en la relación **children** de un objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="79582-102">Return a collection of [DriveItems](../resources/driveitem.md) in the **children** relationship of a DriveItem.</span></span>

<span data-ttu-id="79582-103">Los objetos DriveItem con una faceta **folder** o **package** que no es null pueden tener uno o varios objetos DriveItem secundarios.</span><span class="sxs-lookup"><span data-stu-id="79582-103">DriveItems with a non-null **folder** or **package** facet can have one or more child DriveItems.</span></span>


## <a name="permissions"></a><span data-ttu-id="79582-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="79582-104">Permissions</span></span>
<span data-ttu-id="79582-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="79582-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="79582-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="79582-107">Permission type</span></span>      | <span data-ttu-id="79582-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="79582-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="79582-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="79582-109">Delegated (work or school account)</span></span> | <span data-ttu-id="79582-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="79582-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="79582-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="79582-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="79582-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="79582-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="79582-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="79582-113">Application</span></span> | <span data-ttu-id="79582-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="79582-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="79582-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="79582-115">HTTP request</span></span>
```http
GET /me/drive/root/children
GET /me/drive/items/{item-id}/children
GET /me/drive/root:/{item-path}:/children
GET /drives/{drive-id}/items/{item-id}/children
GET /groups/{group-id}/drive/root/children
GET /groups/{group-id}/drive/items/{item-id}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="79582-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="79582-116">Optional query parameters</span></span>
<span data-ttu-id="79582-117">Este método admite los [parámetros de consulta OData](../../../concepts/query_parameters.md) `$expand`, `$select`, `$skipToken`, `$top` y `$orderby` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79582-117">This method supports the `$expand` and `$orderby` [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-headers"></a><span data-ttu-id="79582-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="79582-118">Request headers</span></span>

| <span data-ttu-id="79582-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="79582-119">Name</span></span>          | <span data-ttu-id="79582-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="79582-120">Type</span></span>   | <span data-ttu-id="79582-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="79582-121">Description</span></span>                                                                                                                                              |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79582-122">if-none-match</span><span class="sxs-lookup"><span data-stu-id="79582-122">if-none-match</span></span> | <span data-ttu-id="79582-123">String</span><span class="sxs-lookup"><span data-stu-id="79582-123">String</span></span> | <span data-ttu-id="79582-124">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="79582-124">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <a name="request-body"></a><span data-ttu-id="79582-125">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="79582-125">Request body</span></span>
<span data-ttu-id="79582-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="79582-126">Do not supply a request body for this method.</span></span>

## <a name="example"></a><span data-ttu-id="79582-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="79582-127">Example</span></span>

##### <a name="request"></a><span data-ttu-id="79582-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="79582-128">Request</span></span>
<span data-ttu-id="79582-129">Esta es una solicitud de ejemplo para devolver los objetos DriveItem de la carpeta raíz del OneDrive del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="79582-129">Here is an example request to return the DriveItems in the root folder of the current user's OneDrive.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_children"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/children
```

## <a name="response"></a><span data-ttu-id="79582-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="79582-130">Response</span></span>

<span data-ttu-id="79582-131">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="79582-131">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {"name": "myfile.jpg", "size": 2048, "file": {} },
    {"name": "Documents", "folder": { "childCount": 4} },
    {"name": "Photos", "folder": { "childCount": 203} },
    {"name": "my sheet(1).xlsx", "size": 197 }
  ],
  "@odata.nextLink": "https://..."
}
```

<span data-ttu-id="79582-132">**Nota:** Si una colección supera el tamaño de página predeterminado (200 elementos), se devuelve la propiedad **@odata.nextLink** en la respuesta para indicar que hay más elementos disponibles y proporcionar la dirección URL de solicitud de la siguiente página de elementos.</span><span class="sxs-lookup"><span data-stu-id="79582-132">**Note:** If a collection exceeds the default page size (200 items), the **@odata.nextLink** property is returned in the response to indicate more items are available and provide the request URL for the next page of items.</span></span>

<span data-ttu-id="79582-133">Puede controlar el tamaño de la página mediante los [parámetros de cadena de consulta opcionales](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters)</span><span class="sxs-lookup"><span data-stu-id="79582-133">You can control the page size through [optional query string parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters)</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List the children of an item.",
  "keywords": "list,children,collection",
  "section": "documentation",
  "tocPath": "OneDrive/DriveItem/List children"
} -->
