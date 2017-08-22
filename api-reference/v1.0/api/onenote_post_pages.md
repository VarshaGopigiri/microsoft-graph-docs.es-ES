# <a name="create-page"></a><span data-ttu-id="90601-101">Crear página</span><span class="sxs-lookup"><span data-stu-id="90601-101">Create page</span></span>

<span data-ttu-id="90601-102">Cree una página de OneNote en la sección predeterminada del bloc de notas predeterminado.</span><span class="sxs-lookup"><span data-stu-id="90601-102">Create a new OneNote page in the default section of the default notebook.</span></span>

<span data-ttu-id="90601-p101">Para crear una página en una sección diferente del bloc de notas predeterminado, puede utilizar el parámetro de consulta `sectionName`.  Ejemplo: `../onenote/pages?sectionName=My%20section`</span><span class="sxs-lookup"><span data-stu-id="90601-p101">To create a page in a different section in the default notebook, you can use the `sectionName` query parameter.  Example: `../onenote/pages?sectionName=My%20section`</span></span>

<span data-ttu-id="90601-p102">La operación `POST /onenote/pages` solo se utiliza para crear páginas en el bloc de notas predeterminado del usuario actual. Si su objetivo son otros blocs de notas, puede [crear páginas en una sección especificada](../api/section_post_pages.md).</span><span class="sxs-lookup"><span data-stu-id="90601-p102">The `POST /onenote/pages` operation is used only to create pages in the current user's default notebook. If you're targeting other notebooks, you can [create pages in a specified section](../api/section_post_pages.md).</span></span>           
## <a name="prerequisites"></a><span data-ttu-id="90601-107">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="90601-107">Prerequisites</span></span>
<span data-ttu-id="90601-108">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="90601-108">One of the following **scopes** is required to execute this API:</span></span>  

<span data-ttu-id="90601-109">Notes.Create, Notes.ReadWrite o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="90601-109">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="90601-110">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="90601-110">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->

```http
POST /me/onenote/pages
POST /users/{id | userPrincipalName}/onenote/pages
POST /groups/{id}/onenote/pages
POST /sites/{id}/onenote/pages
```

## <a name="request-headers"></a><span data-ttu-id="90601-111">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="90601-111">Request headers</span></span>  
| <span data-ttu-id="90601-112">Nombre</span><span class="sxs-lookup"><span data-stu-id="90601-112">Name</span></span>       | <span data-ttu-id="90601-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="90601-113">Type</span></span> | <span data-ttu-id="90601-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="90601-114">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="90601-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="90601-115">Authorization</span></span>  | <span data-ttu-id="90601-116">string</span><span class="sxs-lookup"><span data-stu-id="90601-116">string</span></span>  | <span data-ttu-id="90601-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="90601-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="90601-119">Content-Type</span><span class="sxs-lookup"><span data-stu-id="90601-119">Content-Type</span></span> | <span data-ttu-id="90601-120">string</span><span class="sxs-lookup"><span data-stu-id="90601-120">string</span></span> | <span data-ttu-id="90601-p104">`text/html` o `application/xhtml+xml` para el contenido HTML, también para la parte requerida "Presentación" de las solicitudes de varias partes. Las solicitudes de varias partes usan el tipo de contenido `multipart/form-data; boundary=your-boundary`.</span><span class="sxs-lookup"><span data-stu-id="90601-p104">`text/html` or `application/xhtml+xml` for the HTML content, including for the required "Presentation" part of multipart requests. Multipart requests use the `multipart/form-data; boundary=your-boundary` content type.</span></span> |

## <a name="request-body"></a><span data-ttu-id="90601-123">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="90601-123">Request body</span></span>
<span data-ttu-id="90601-124">En el cuerpo de la solicitud, facilite el contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="90601-124">In the request body, supply the HTML content for the page.</span></span>

<span data-ttu-id="90601-p105">El cuerpo puede contener código HTML ubicado directamente en el cuerpo de la solicitud o un formato de mensaje de varias partes, como se muestra en el ejemplo. Si quiere enviar datos binarios, debe enviar una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="90601-p105">The body can contain HTML placed directly in the request body, or it can contain a multipart message format as shown in the example. If you're sending binary data, then you must send a multipart request.</span></span>

## <a name="response"></a><span data-ttu-id="90601-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90601-127">Response</span></span>

<span data-ttu-id="90601-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el nuevo objeto [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="90601-128">If successful, this method returns a `201 Created` response code and the new [page](../resources/page.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="90601-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="90601-129">Example</span></span>
##### <a name="request"></a><span data-ttu-id="90601-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="90601-130">Request</span></span>
<span data-ttu-id="90601-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="90601-131">Here is an example of the request.</span></span>

<span data-ttu-id="90601-p106">En la ruta `../onenote/pages`, puede usar el parámetro de consulta `sectionName` para crear una página en una sección específica del bloc de notas predeterminado. Ejemplo: `../onenote/pages?sectionName=My%20section`. Si la sección no existe (o ha cambiado de nombre), la API creará una.</span><span class="sxs-lookup"><span data-stu-id="90601-p106">In the `../onenote/pages` path, you can use the `sectionName` query parameter to create a page in a specific section in the default notebook. Example: `../onenote/pages?sectionName=My%20section`. If the section doesn't exist (or was renamed), the API will create a new section.</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/pages
Content-length: 312
Content-type: multipart/form-data; boundary=MyPartBoundary198374

--MyPartBoundary198374
Content-Disposition:form-data; name="Presentation"
Content-Type:text/html

<!DOCTYPE html>
<html>
  <head>
    <title>A page with <i>rendered</i> images and an <b>attached</b> file</title>
    <meta name="created" content="2015-07-22T09:00:00-08:00" />
  </head>
  <body>
    <p>Here's an image from an online source:</p>
    <img src="http://..." alt="an image on the page" width="500" />
    <p>Here's an image uploaded as binary data:</p>
    <img src="name:imageBlock1" alt="an image on the page" width="300" />
    <p>Here's a file attachment:</p>
    <object data-attachment="FileName.pdf" data="name:fileBlock1" type="application/pdf" />
  </body>
</html>

--MyPartBoundary198374
Content-Disposition:form-data; name="imageBlock1"
Content-Type:image/jpeg

... binary image data ...

--MyPartBoundary198374
Content-Disposition:form-data; name="fileBlock1"
Content-Type:application/pdf

... binary file data ...

--MyPartBoundary198374--
```
##### <a name="response"></a><span data-ttu-id="90601-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="90601-135">Response</span></span>
<span data-ttu-id="90601-p107">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="90601-p107">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "description": "Create Page",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->