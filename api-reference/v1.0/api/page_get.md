# <a name="get-page"></a><span data-ttu-id="5ce0f-101">Obtener página</span><span class="sxs-lookup"><span data-stu-id="5ce0f-101">Get page</span></span>

<span data-ttu-id="5ce0f-102">Recupere las propiedades y las relaciones de un objeto [page](../resources/page.md).</span><span class="sxs-lookup"><span data-stu-id="5ce0f-102">Retrieve the properties and relationships of a [page](../resources/page.md) object.</span></span>

<span data-ttu-id="5ce0f-103">**Obtener información de la página**</span><span class="sxs-lookup"><span data-stu-id="5ce0f-103">**Getting page information**</span></span>

<span data-ttu-id="5ce0f-104">Acceder a los metadatos de una página por el identificador de página:</span><span class="sxs-lookup"><span data-stu-id="5ce0f-104">Access a page's metadata by page identifier:</span></span>

```
GET /me/onenote/pages/{id}
```

<span data-ttu-id="5ce0f-105">**Obtener contenido de la página**</span><span class="sxs-lookup"><span data-stu-id="5ce0f-105">**Getting page content**</span></span>

<span data-ttu-id="5ce0f-106">Puede usar el punto de conexión `content` de la página para obtener el contenido HTML de una página:</span><span class="sxs-lookup"><span data-stu-id="5ce0f-106">You can use the page's `content` endpoint to get the HTML content of a page:</span></span>

```
GET /me/onenote/pages/{id}/content[?includeIDs=true]
GET /me/onenote/pages/{id}/$value[?includeIDs=true]
```

<span data-ttu-id="5ce0f-107">La opción de consulta `includeIDs=true` se utiliza para [actualizar páginas](../api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="5ce0f-107">The `includeIDs=true` query option is used to [update pages](../api/page_update.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5ce0f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5ce0f-108">Prerequisites</span></span>
<span data-ttu-id="5ce0f-109">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="5ce0f-109">One of the following **scopes** is required to execute this API:</span></span>  

<span data-ttu-id="5ce0f-110">Notes.Read, Notes.ReadWrite, Notes.Read.All o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5ce0f-110">Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="5ce0f-111">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5ce0f-111">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/pages/{id}
GET /users/{id | userPrincipalName}/onenote/pages/{id}
GET /groups/{id}/onenote/pages/{id}
GET /sites/{id}/onenote/pages/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="5ce0f-112">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="5ce0f-112">Optional query parameters</span></span>
<span data-ttu-id="5ce0f-113">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5ce0f-113">This method supports the `select` and `expand` [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="5ce0f-p101">La respuesta predeterminada expande `parentSection` y selecciona las propiedades `id`, `name` y `self` de la sección. Los valores válidos de `expand` de las páginas son `parentNotebook` y `parentSection`.</span><span class="sxs-lookup"><span data-stu-id="5ce0f-p101">The default response expands `parentSection` and selects the section's `id`, `name`, and `self` properties. Valid `expand` values for pages are `parentNotebook` and `parentSection`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="5ce0f-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5ce0f-116">Request headers</span></span>
| <span data-ttu-id="5ce0f-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="5ce0f-117">Name</span></span>       | <span data-ttu-id="5ce0f-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="5ce0f-118">Type</span></span> | <span data-ttu-id="5ce0f-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="5ce0f-119">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="5ce0f-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="5ce0f-120">Authorization</span></span>  | <span data-ttu-id="5ce0f-121">string</span><span class="sxs-lookup"><span data-stu-id="5ce0f-121">string</span></span>  | <span data-ttu-id="5ce0f-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5ce0f-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="5ce0f-124">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5ce0f-124">Accept</span></span> | <span data-ttu-id="5ce0f-125">string</span><span class="sxs-lookup"><span data-stu-id="5ce0f-125">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="5ce0f-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5ce0f-126">Request body</span></span>
<span data-ttu-id="5ce0f-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="5ce0f-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="5ce0f-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ce0f-128">Response</span></span>

<span data-ttu-id="5ce0f-129">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5ce0f-129">If successful, this method returns a `200 OK` response code and the [page](../resources/page.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="5ce0f-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5ce0f-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="5ce0f-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5ce0f-131">Request</span></span>
<span data-ttu-id="5ce0f-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5ce0f-132">Here is an example of the request.</span></span>
 <!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/pages/{id}
```
##### <a name="response"></a><span data-ttu-id="5ce0f-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5ce0f-133">Response</span></span>
<span data-ttu-id="5ce0f-p103">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5ce0f-p103">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
 <!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 312

{
  "title": "title-value",
  "createdByAppId": "createdByAppId-value",
  "links": {
    "oneNoteClientUrl": {
      "href": "href-value"
    },
    "oneNoteWebUrl": {
      "href": "href-value"
    }
  },
  "contentUrl": "contentUrl-value",
  "content": "content-value",
  "lastModifiedDateTime": "2016-10-19T10:37:00Z"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get page",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
