# <span data-ttu-id="1775d-101">Get a DriveItem resource</span><span class="sxs-lookup"><span data-stu-id="1775d-101">Get a DriveItem resource</span></span>
<a id="get-a-driveitem-resource" class="xliff"></a>

<span data-ttu-id="1775d-102">Recupera los metadatos de un [DriveItem](../resources/driveitem.md) en un [Drive](../resources/drive.md) por identificador o ruta de acceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="1775d-102">Retrieve the metadata for a [DriveItem](../resources/driveitem.md) in a [Drive](../resources/drive.md) by file system path or ID.</span></span>

## <span data-ttu-id="1775d-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="1775d-103">Prerequisites</span></span>
<a id="prerequisites" class="xliff"></a>
<span data-ttu-id="1775d-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="1775d-104">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="1775d-105">Files.Read</span><span class="sxs-lookup"><span data-stu-id="1775d-105">Files.Read</span></span>
* <span data-ttu-id="1775d-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1775d-106">Files.ReadWrite</span></span>
* <span data-ttu-id="1775d-107">Files.Read.All</span><span class="sxs-lookup"><span data-stu-id="1775d-107">Files.Read.All</span></span>
* <span data-ttu-id="1775d-108">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1775d-108">Files.ReadWrite.All</span></span>
* <span data-ttu-id="1775d-109">Sites.Read.All</span><span class="sxs-lookup"><span data-stu-id="1775d-109">Sites.Read.All</span></span>
* <span data-ttu-id="1775d-110">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1775d-110">Sites.ReadWrite.All</span></span>

## <span data-ttu-id="1775d-111">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1775d-111">HTTP request</span></span>
<a id="http-request" class="xliff"></a>
<!-- { "blockType": "ignored" } -->
```http
GET /me/drive/items/{item-id}
GET /me/drive/root:/{item-path}
GET /drives/{drive-id}/items/{item-id}
GET /groups/{group-id}/drive/items/{item-id}
```

## <span data-ttu-id="1775d-112">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1775d-112">Optional query parameters</span></span>
<a id="optional-query-parameters" class="xliff"></a>
<span data-ttu-id="1775d-113">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1775d-113">This method supports the [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

## <span data-ttu-id="1775d-114">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1775d-114">Request headers</span></span>
<a id="request-headers" class="xliff"></a>

| <span data-ttu-id="1775d-115">Nombre</span><span class="sxs-lookup"><span data-stu-id="1775d-115">Name</span></span>          | <span data-ttu-id="1775d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="1775d-116">Value</span></span>  | <span data-ttu-id="1775d-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1775d-117">Description</span></span>                                                                                                                                              |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1775d-118">if-none-match</span><span class="sxs-lookup"><span data-stu-id="1775d-118">if-none-match</span></span> | <span data-ttu-id="1775d-119">String</span><span class="sxs-lookup"><span data-stu-id="1775d-119">String</span></span> | <span data-ttu-id="1775d-120">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada coincide con la etiqueta actual del archivo, se devuelve una respuesta `HTTP 304 Not Modified`.</span><span class="sxs-lookup"><span data-stu-id="1775d-120">If this request header is included and the eTag (or cTag) provided matches the current tag on the file, an `HTTP 304 Not Modified` response is returned.</span></span> |


## <span data-ttu-id="1775d-121">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="1775d-121">Request body</span></span>
<a id="request-body" class="xliff"></a>
<span data-ttu-id="1775d-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1775d-122">Do not supply a request body for this method.</span></span>

## <span data-ttu-id="1775d-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1775d-123">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="1775d-124">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el recurso [DriveItem](../resources/driveitem.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1775d-124">If successful, this method returns a `200 OK` response code and the [DriveItem](../resources/driveitem.md) resource in the response body.</span></span>

## <span data-ttu-id="1775d-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1775d-125">Example</span></span>
<a id="example" class="xliff"></a>

##### <span data-ttu-id="1775d-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1775d-126">Request</span></span>
<a id="request" class="xliff"></a>

<span data-ttu-id="1775d-127">Aquí tiene un ejemplo de la solicitud a la carpeta raíz de OneDrive del usuario.</span><span class="sxs-lookup"><span data-stu-id="1775d-127">Here is an example of the request to the root folder of the user's OneDrive.</span></span>

<!-- {
  "blockType": "request",
  "name": "get_item"
}-->
```
GET https://graph.microsoft.com/v1.0//me/drive/root
```

##### <span data-ttu-id="1775d-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1775d-128">Response</span></span>
<a id="response" class="xliff"></a>
<span data-ttu-id="1775d-129">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1775d-129">Here is an example of the response.</span></span>

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.driveItem"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "createdBy": {
      "user": {
          "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
          "displayName": "Ryan Gregg"
      }
  },
  "createdDateTime": "2016-03-21T20:01:37Z",
  "cTag": "\"c:{86EB4C8E-D20D-46B9-AD41-23B8868DDA8A},0\"",
  "eTag": "\"{86EB4C8E-D20D-46B9-AD41-23B8868DDA8A},1\"",
  "folder": { "childCount": 120 },
  "id": "01NKDM7HMOJTVYMDOSXFDK2QJDXCDI3WUK",
  "lastModifiedBy": {
      "user": {
          "id": "efee1b77-fb3b-4f65-99d6-274c11914d12",
          "displayName": "Ryan Gregg"
      }
  },
  "lastModifiedDateTime": "2016-03-21T20:01:37Z",
  "name": "OneDrive",
  "root": { },
  "size": 157286400,
  "webUrl": "https://contoso-my.sharepoint.com/personal/rgregg_contoso_com/Documents"
}
```

## <span data-ttu-id="1775d-130">Notas</span><span class="sxs-lookup"><span data-stu-id="1775d-130">Notes</span></span>
<a id="notes" class="xliff"></a>

<span data-ttu-id="1775d-131">Puede usar el [parámetro de cadena de consulta `$expand`](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) para incluir los elementos secundarios de un elemento en la misma llamada al recuperar los metadatos de un elemento si el elemento tiene una relación **children**.</span><span class="sxs-lookup"><span data-stu-id="1775d-131">You can use the [`$expand` query string parameter](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to include the children of an item in the same call as retrieving the metadata of an item if the item has a **children** relationship.</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get item",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Item/Get item"
}-->
