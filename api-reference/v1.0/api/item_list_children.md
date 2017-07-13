# <span data-ttu-id="c59f1-101">Mostrar los elementos secundarios de un objeto driveItem</span><span class="sxs-lookup"><span data-stu-id="c59f1-101">List children of a driveItem</span></span>
<a id="list-children-of-a-driveitem" class="xliff"></a>

<span data-ttu-id="c59f1-102">Devuelva una colección de objetos [DriveItem](../resources/driveitem.md) en la relación **children** de un objeto DriveItem.</span><span class="sxs-lookup"><span data-stu-id="c59f1-102">Return a collection of [DriveItems](../resources/driveitem.md) in the **children** relationship of a DriveItem.</span></span>

<span data-ttu-id="c59f1-103">Los objetos DriveItem con una faceta **folder** o **package** que no es null pueden tener uno o varios objetos DriveItem secundarios.</span><span class="sxs-lookup"><span data-stu-id="c59f1-103">DriveItems with a non-null **folder** or **package** facet can have one or more child DriveItems.</span></span>


## <span data-ttu-id="c59f1-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c59f1-104">Prerequisites</span></span>
<a id="prerequisites" class="xliff"></a>
<span data-ttu-id="c59f1-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="c59f1-105">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="c59f1-106">Files.Read</span><span class="sxs-lookup"><span data-stu-id="c59f1-106">Files.Read</span></span>
* <span data-ttu-id="c59f1-107">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c59f1-107">Files.ReadWrite</span></span>
* <span data-ttu-id="c59f1-108">Files.Read.All</span><span class="sxs-lookup"><span data-stu-id="c59f1-108">Files.Read.All</span></span>
* <span data-ttu-id="c59f1-109">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c59f1-109">Files.ReadWrite.All</span></span>
* <span data-ttu-id="c59f1-110">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="c59f1-110">Sites.Read.All</span></span>
* <span data-ttu-id="c59f1-111">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c59f1-111">Sites.ReadWrite.All</span></span>

## <span data-ttu-id="c59f1-112">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c59f1-112">HTTP request</span></span>
<a id="http-request" class="xliff"></a>
```http
GET /me/drive/root/children
GET /me/drive/items/{item-id}/children
GET /me/drive/root:/{item-path}:/children
GET /drives/{drive-id}/items/{item-id}/children
GET /groups/{group-id}/drive/root/children
GET /groups/{group-id}/drive/items/{item-id}
```

## <span data-ttu-id="c59f1-113">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="c59f1-113">Optional query parameters</span></span>
<a id="optional-query-parameters" class="xliff"></a>
<span data-ttu-id="c59f1-114">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c59f1-114">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <span data-ttu-id="c59f1-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c59f1-115">Request headers</span></span>
<a id="request-headers" class="xliff"></a>

| <span data-ttu-id="c59f1-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="c59f1-116">Name</span></span>          | <span data-ttu-id="c59f1-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="c59f1-117">Type</span></span>   | <span data-ttu-id="c59f1-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="c59f1-118">Description</span></span>                                                                                                                                              |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c59f1-119">if-none-match</span><span class="sxs-lookup"><span data-stu-id="c59f1-119">if-none-match</span></span> | <span data-ttu-id="c59f1-120">String</span><span class="sxs-lookup"><span data-stu-id="c59f1-120">String</span></span> | <span data-ttu-id="c59f1-121">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="c59f1-121">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |

## <span data-ttu-id="c59f1-122">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="c59f1-122">Request body</span></span>
<a id="request-body" class="xliff"></a>
<span data-ttu-id="c59f1-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c59f1-123">Do not supply a request body for this method.</span></span>

## <span data-ttu-id="c59f1-124">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c59f1-124">Example</span></span>
<a id="example" class="xliff"></a>

##### <span data-ttu-id="c59f1-125">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c59f1-125">Request</span></span>
<a id="request" class="xliff"></a>
<span data-ttu-id="c59f1-126">Esta es una solicitud de ejemplo para devolver los objetos DriveItem de la carpeta raíz del OneDrive del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="c59f1-126">Here is an example request to return the DriveItems in the root folder of the current user's OneDrive.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_children"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/children
```

## <span data-ttu-id="c59f1-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c59f1-127">Response</span></span>
<a id="response" class="xliff"></a>

<span data-ttu-id="c59f1-128">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c59f1-128">Here is an example of the response.</span></span>
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

<span data-ttu-id="c59f1-129">**Nota:** Si una colección supera el tamaño de página predeterminado (200 elementos), se devuelve la propiedad **@odata.nextLink** en la respuesta para indicar que hay más elementos disponibles y proporcionar la dirección URL de solicitud de la siguiente página de elementos.</span><span class="sxs-lookup"><span data-stu-id="c59f1-129">**Note:** If a collection exceeds the default page size (200 items), the **@odata.nextLink** property is returned in the response to indicate more items are available and provide the request URL for the next page of items.</span></span>

<span data-ttu-id="c59f1-130">Puede controlar el tamaño de la página mediante los [parámetros de cadena de consulta opcionales](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters)</span><span class="sxs-lookup"><span data-stu-id="c59f1-130">You can control the page size through [optional query string parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters)</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List the children of an item.",
  "keywords": "list,children,collection",
  "section": "documentation",
  "tocPath": "OneDrive/DriveItem/List children"
} -->
