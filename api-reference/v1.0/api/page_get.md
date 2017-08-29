# <a name="get-page"></a><span data-ttu-id="1535b-101">Obtener página</span><span class="sxs-lookup"><span data-stu-id="1535b-101">Get page</span></span>

<span data-ttu-id="1535b-102">Recupere las propiedades y las relaciones de un objeto [page](../resources/page.md).</span><span class="sxs-lookup"><span data-stu-id="1535b-102">Retrieve the properties and relationships of a [page](../resources/page.md) object.</span></span>

<span data-ttu-id="1535b-103">**Obtener información de la página**</span><span class="sxs-lookup"><span data-stu-id="1535b-103">**Getting page information**</span></span>

<span data-ttu-id="1535b-104">Acceder a los metadatos de una página por el identificador de página:</span><span class="sxs-lookup"><span data-stu-id="1535b-104">Access a page's metadata by page identifier:</span></span>

```
GET /me/onenote/pages/{id}
```

<span data-ttu-id="1535b-105">**Obtener contenido de la página**</span><span class="sxs-lookup"><span data-stu-id="1535b-105">**Getting page content**</span></span>

<span data-ttu-id="1535b-106">Puede usar el punto de conexión `content` de la página para obtener el contenido HTML de una página:</span><span class="sxs-lookup"><span data-stu-id="1535b-106">You can use the page's `content` endpoint to get the HTML content of a page:</span></span>

```
GET /me/onenote/pages/{id}/content[?includeIDs=true]
GET /me/onenote/pages/{id}/$value[?includeIDs=true]
```

<span data-ttu-id="1535b-107">La opción de consulta `includeIDs=true` se usa para [actualizar páginas](../api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="1535b-107">The `includeIDs=true` query option is used to [update pages](../api/page_update.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="1535b-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="1535b-108">Permissions</span></span>
<span data-ttu-id="1535b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="1535b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="1535b-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="1535b-111">Permission type</span></span>      | <span data-ttu-id="1535b-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="1535b-112">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="1535b-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="1535b-113">Delegated (work or school account)</span></span> | <span data-ttu-id="1535b-114">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1535b-114">Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span>    | 
|<span data-ttu-id="1535b-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="1535b-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="1535b-116">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="1535b-116">Notes.Read, Notes.ReadWrite</span></span>    | 
|<span data-ttu-id="1535b-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="1535b-117">Application</span></span> | <span data-ttu-id="1535b-118">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="1535b-118">Notes.Read, Notes.ReadWrite, Notes.Read.All, or Notes.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="1535b-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="1535b-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/pages/{id}
GET /users/{id | userPrincipalName}/onenote/pages/{id}
GET /groups/{id}/onenote/pages/{id}
GET /sites/{id}/onenote/pages/{id}
```
## <a name="optional-query-parameters"></a><span data-ttu-id="1535b-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="1535b-120">Optional query parameters</span></span>
<span data-ttu-id="1535b-121">Este método admite los [parámetros de consulta de OData](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) de `select` y `expand` a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1535b-121">This method supports the `select` and `expand` [OData Query Parameters](http://developer.microsoft.com/en-us/graph/docs/overview/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="1535b-p102">La respuesta predeterminada expande `parentSection` y selecciona las propiedades `id`, `name` y `self` de la sección. Los valores válidos de `expand` de las páginas son `parentNotebook` y `parentSection`.</span><span class="sxs-lookup"><span data-stu-id="1535b-p102">The default response expands `parentSection` and selects the section's `id`, `name`, and `self` properties. Valid `expand` values for pages are `parentNotebook` and `parentSection`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="1535b-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="1535b-124">Request headers</span></span>
| <span data-ttu-id="1535b-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="1535b-125">Name</span></span>       | <span data-ttu-id="1535b-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="1535b-126">Type</span></span> | <span data-ttu-id="1535b-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="1535b-127">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="1535b-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="1535b-128">Authorization</span></span>  | <span data-ttu-id="1535b-129">string</span><span class="sxs-lookup"><span data-stu-id="1535b-129">string</span></span>  | <span data-ttu-id="1535b-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="1535b-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="1535b-132">Aceptar</span><span class="sxs-lookup"><span data-stu-id="1535b-132">Accept</span></span> | <span data-ttu-id="1535b-133">string</span><span class="sxs-lookup"><span data-stu-id="1535b-133">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="1535b-134">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="1535b-134">Request body</span></span>
<span data-ttu-id="1535b-135">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="1535b-135">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="1535b-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1535b-136">Response</span></span>

<span data-ttu-id="1535b-137">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="1535b-137">If successful, this method returns a `200 OK` response code and the [page](../resources/page.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="1535b-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="1535b-138">Example</span></span>
##### <a name="request"></a><span data-ttu-id="1535b-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="1535b-139">Request</span></span>
<span data-ttu-id="1535b-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="1535b-140">Here is an example of the request.</span></span>
 <!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/pages/{id}
```
##### <a name="response"></a><span data-ttu-id="1535b-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="1535b-141">Response</span></span>
<span data-ttu-id="1535b-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="1535b-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
