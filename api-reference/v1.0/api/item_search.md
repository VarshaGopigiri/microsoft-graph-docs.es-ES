# <a name="search-for-a-driveitem-within-a-drive"></a><span data-ttu-id="93af8-101">Buscar un objeto DriveItem dentro de una unidad</span><span class="sxs-lookup"><span data-stu-id="93af8-101">Search for a DriveItem within a drive</span></span>

<span data-ttu-id="93af8-p101">Busque elementos que coincidan con una consulta en la jerarquía de elementos. Puede buscar en una jerarquía de carpetas, en una unidad entera o en los archivos que se comparten con el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="93af8-p101">Search the hierarchy of items for items matching a query. You can search within a folder hierarhcy, a whole drive, or files shared with the current user.</span></span>

## <a name="permissions"></a><span data-ttu-id="93af8-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="93af8-104">Permissions</span></span>
<span data-ttu-id="93af8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="93af8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="93af8-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="93af8-107">Permission type</span></span>      | <span data-ttu-id="93af8-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="93af8-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="93af8-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="93af8-109">Delegated (work or school account)</span></span> | <span data-ttu-id="93af8-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="93af8-110">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="93af8-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="93af8-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="93af8-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="93af8-112">Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="93af8-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="93af8-113">Application</span></span> | <span data-ttu-id="93af8-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="93af8-114">Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="93af8-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="93af8-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```
GET /me/drive/root/search(q='{search-text}')
GET /me/drive/items/{item-id}/search(q='{search-text}')
GET /me/drive/root:/{item-path}:/search(q='{search-text}')
GET /drives/{drive-id}/root/search(q='{search-text}')
GET /groups/{group-id}/drive/root/search(q='{search-text}')
```

## <a name="optional-query-parameters"></a><span data-ttu-id="93af8-116">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="93af8-116">Optional query parameters</span></span>
<span data-ttu-id="93af8-117">Este método admite los [parámetros de consulta OData](../../../concepts/query_parameters.md) `$expand`, `$select`, `$skipToken`, `$top` y `$orderby` para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="93af8-117">This method supports the `$expand` and `$orderby` [OData Query Parameters](../../../concepts/query_parameters.md) to help customize the response.</span></span>

## <a name="request-body"></a><span data-ttu-id="93af8-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="93af8-118">Request body</span></span>
<span data-ttu-id="93af8-119">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="93af8-119">Do not supply a request body for this method.</span></span>

#### <a name="function-parameters"></a><span data-ttu-id="93af8-120">Parámetros de función</span><span class="sxs-lookup"><span data-stu-id="93af8-120">Function parameters</span></span>

| <span data-ttu-id="93af8-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="93af8-121">Name</span></span> | <span data-ttu-id="93af8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="93af8-122">Value</span></span>  | <span data-ttu-id="93af8-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="93af8-123">Description</span></span>                                                                                                                          |
|:-----|:-------|:-------------------------------------------------------------------------------------------------------------------------------------|
| `q`  | <span data-ttu-id="93af8-124">string</span><span class="sxs-lookup"><span data-stu-id="93af8-124">string</span></span> | <span data-ttu-id="93af8-p103">El texto de la consulta usado para buscar elementos. Los valores pueden coincidir en varios campos, como el nombre de archivo, los metadatos y el contenido de los archivos.</span><span class="sxs-lookup"><span data-stu-id="93af8-p103">The query text used to search for items. Values may be matched across several fields including filename, metadata, and file content.</span></span> |

## <a name="example"></a><span data-ttu-id="93af8-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="93af8-127">Example</span></span>

##### <a name="request"></a><span data-ttu-id="93af8-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="93af8-128">Request</span></span>

<span data-ttu-id="93af8-129">Este es un ejemplo de la solicitud buscando en el OneDrive del usuario actual</span><span class="sxs-lookup"><span data-stu-id="93af8-129">Here is an example of the request searching the current user's OneDrive</span></span>
<!-- {
  "blockType": "request",
  "name": "item_search"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/root/search(q='{search-query}')
```

##### <a name="response"></a><span data-ttu-id="93af8-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93af8-130">Response</span></span>
<span data-ttu-id="93af8-p104">Este método devuelve un objeto que contiene una colección de objetos [DriveItem](../resources/driveitem.md) que coinciden con los criterios de búsqueda. Si no se han encontrado elementos, se devuelve una colección vacía.</span><span class="sxs-lookup"><span data-stu-id="93af8-p104">This method returns an object containing an collection of [DriveItems](../resources/driveitem.md) that match the search criteria. If no items were found, an empty collection is returned.</span></span>

<span data-ttu-id="93af8-p105">Si hay demasiadas coincidencias, se paginará la respuesta y una propiedad **@odata.nextLink** contendrá una dirección URL a la siguiente página de resultados. Puede usar el parámetro de consulta `$top` para especificar el número de elementos en la página.</span><span class="sxs-lookup"><span data-stu-id="93af8-p105">If there are too many matches the response will be paged and an **@odata.nextLink** property will contain a URL to the next page of results. You can use the `$top` query parameter to specify the number of items in the page.</span></span>

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
      {
        "id": "0123456789abc!123",
        "name": "Contoso Project",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!123" }
      },
      {
        "id": "0123456789abc!456",
        "name": "Contoso Project 2016",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!456" }
      }
    ],
    "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/drive/root/search(query='contoso project')&skipToken=1asdlnjnkj1nalkm!asd"
}
```

## <a name="searching-for-items-a-user-can-access"></a><span data-ttu-id="93af8-135">Buscar elementos a los que puede acceder un usuario</span><span class="sxs-lookup"><span data-stu-id="93af8-135">Searching for items a user can access</span></span>

<span data-ttu-id="93af8-p106">Además de buscar elementos de una unidad, la aplicación puede buscar de forma más amplia para incluir elementos que se comparten con el usuario actual. Para ampliar el ámbito de búsqueda, use el método **search** en el recurso [Drive](../resources/drive.md).</span><span class="sxs-lookup"><span data-stu-id="93af8-p106">In addition to searching for items within a drive, your app can search more broadly to include items shared with the current user. To broaden the search scope, use the **search** method on the [Drive](../resources/drive.md) resource.</span></span>

##### <a name="request"></a><span data-ttu-id="93af8-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="93af8-138">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "item_search_all"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/drive/search(q='{search-query}')
```

##### <a name="response"></a><span data-ttu-id="93af8-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="93af8-139">Response</span></span>
<span data-ttu-id="93af8-p107">Las respuestas al buscar desde el recurso **Drive** pueden incluir elementos fuera de la unidad (elementos compartidos con el usuario actual). Estos elementos incluirán la faceta [**remoteItem**](../resources/remoteitem.md) para indicar que se almacenan fuera de la unidad de destino.</span><span class="sxs-lookup"><span data-stu-id="93af8-p107">Responses when searching from the **drive** resource may include items outside of the drive (items shared with the current user). These items will include the [**remoteItem**](../resources/remoteitem.md) facet to indicate they are stored outside of the target drive.</span></span> 

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
      {
        "id": "0123456789abc!123",
        "name": "Contoso Project",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!123" },
        "remoteItem": { "id": "!23141901", "driveId": "s!1020101jlkjl12lx" }
      },
      {
        "id": "0123456789abc!456",
        "name": "Contoso Project 2016",
        "folder": {},
        "searchResult": { "onClickTelemetryUrl": "https://bing.com/0123456789abc!456" }
      }
    ],
    "@odata.nextLink": "https://graph.microsoft.com/v1.0/me/drive/root/search(query='contoso project')&skipToken=1asdlnjnkj1nalkm!asd"
}
```




<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "item: search",
  "keywords": "",
  "section": "documentation",
  "tocPath": "OneDrive/Items/Search items"
}-->
