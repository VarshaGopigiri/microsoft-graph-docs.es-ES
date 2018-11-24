# <a name="list-pages"></a><span data-ttu-id="347ba-101">Enumerar páginas</span><span class="sxs-lookup"><span data-stu-id="347ba-101">List pages</span></span>

<span data-ttu-id="347ba-102">Recupera una lista de objetos [page](../resources/page.md).</span><span class="sxs-lookup"><span data-stu-id="347ba-102">Retrieve a list of [page](../resources/page.md) objects.</span></span>
## <a name="permissions"></a><span data-ttu-id="347ba-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="347ba-103">Permissions</span></span>
<span data-ttu-id="347ba-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="347ba-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="347ba-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="347ba-106">Permission type</span></span>      | <span data-ttu-id="347ba-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="347ba-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="347ba-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="347ba-108">Delegated (work or school account)</span></span> | <span data-ttu-id="347ba-109">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="347ba-109">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="347ba-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="347ba-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="347ba-111">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="347ba-111">Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="347ba-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="347ba-112">Application</span></span> | <span data-ttu-id="347ba-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="347ba-113">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="347ba-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="347ba-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/pages
GET /users/{id | userPrincipalName}/onenote/pages
GET /groups/{id}/onenote/pages
GET /sites/{id}/onenote/pages
```
## <a name="optional-query-parameters"></a><span data-ttu-id="347ba-115">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="347ba-115">Optional query parameters</span></span>
<span data-ttu-id="347ba-116">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="347ba-116">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>

<span data-ttu-id="347ba-p102">La consulta predeterminada para páginas devuelve las primeras 20 páginas ordenadas por `lastModifiedTime desc`. Si la consulta predeterminada devuelve más de 20 páginas, la respuesta contendrá un `@odata.nextLink` que podrá usar para revisar el conjunto de resultados. El número máximo de páginas devueltas para una solicitud `top` es de 100.</span><span class="sxs-lookup"><span data-stu-id="347ba-p102">The default query for pages returns the top 20 pages ordered by `lastModifiedTime desc`. If the default query returns more than 20 pages, the response contains an `@odata.nextLink` that you can use to page through the result set. The maximum number of pages returned for a `top` request is 100.</span></span>

<span data-ttu-id="347ba-p103">La respuesta predeterminada expande `parentSection` y selecciona las propiedades `id`, `displayName` y `self` de la sección. Los valores válidos de `expand` de las páginas son `parentNotebook` y `parentSection`.</span><span class="sxs-lookup"><span data-stu-id="347ba-p103">The default response expands `parentSection` and selects the section's `id`, `displayName`, and `self` properties. Valid `expand` values for pages are `parentNotebook` and `parentSection`.</span></span>

## <a name="request-headers"></a><span data-ttu-id="347ba-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="347ba-122">Request headers</span></span>
| <span data-ttu-id="347ba-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="347ba-123">Name</span></span>       | <span data-ttu-id="347ba-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="347ba-124">Type</span></span> | <span data-ttu-id="347ba-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="347ba-125">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="347ba-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="347ba-126">Authorization</span></span>  | <span data-ttu-id="347ba-127">string</span><span class="sxs-lookup"><span data-stu-id="347ba-127">string</span></span>  | <span data-ttu-id="347ba-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="347ba-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="347ba-130">Aceptar</span><span class="sxs-lookup"><span data-stu-id="347ba-130">Accept</span></span> | <span data-ttu-id="347ba-131">string</span><span class="sxs-lookup"><span data-stu-id="347ba-131">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="347ba-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="347ba-132">Request body</span></span>
<span data-ttu-id="347ba-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="347ba-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="347ba-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="347ba-134">Response</span></span>

<span data-ttu-id="347ba-135">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="347ba-135">If successful, this method returns a `200 OK` response code and a collection of [page](../resources/page.md) objects in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="347ba-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="347ba-136">Example</span></span>
##### <a name="request"></a><span data-ttu-id="347ba-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="347ba-137">Request</span></span>
<span data-ttu-id="347ba-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="347ba-138">Here is an example of the request.</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/pages
```
##### <a name="response"></a><span data-ttu-id="347ba-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="347ba-139">Response</span></span>
<span data-ttu-id="347ba-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="347ba-140">Here is an example of the response.</span></span> <span data-ttu-id="347ba-141">Nota: El objeto de respuesta que se muestra aquí se trunca por razones de brevedad.</span><span class="sxs-lookup"><span data-stu-id="347ba-141">Note: The response object shown here is truncated for brevity.</span></span> <span data-ttu-id="347ba-142">Todas las propiedades se devolverán desde una llamada real.</span><span class="sxs-lookup"><span data-stu-id="347ba-142">All of the properties will be returned from an actual call.</span></span>
<!-- { "blockType": "ignored" } -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 393

{
  "value": [
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
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List pages",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->