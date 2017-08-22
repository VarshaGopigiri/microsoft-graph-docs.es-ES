# <a name="create-page"></a><span data-ttu-id="74660-101">Crear página</span><span class="sxs-lookup"><span data-stu-id="74660-101">Create page</span></span>

<span data-ttu-id="74660-102">Cree una [página](../resources/page.md) en la sección especificada.</span><span class="sxs-lookup"><span data-stu-id="74660-102">Create a new [page](../resources/page.md) in the specified section.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="74660-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="74660-103">Prerequisites</span></span>
<span data-ttu-id="74660-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="74660-104">One of the following **scopes** is required to execute this API:</span></span>   

<span data-ttu-id="74660-105">Notes.Create, Notes.ReadWrite o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="74660-105">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span> 

## <a name="http-request"></a><span data-ttu-id="74660-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="74660-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sections/{id}/pages
POST /users/{id | userPrincipalName}/onenote/sections/{id}/pages
POST /groups/{id}/onenote/sections/{id}/pages
POST /sites/{id}/onenote/sections/{id}/pages
```
## <a name="request-headers"></a><span data-ttu-id="74660-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="74660-107">Request headers</span></span>
| <span data-ttu-id="74660-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="74660-108">Name</span></span>       | <span data-ttu-id="74660-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="74660-109">Type</span></span> | <span data-ttu-id="74660-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="74660-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="74660-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="74660-111">Authorization</span></span>  | <span data-ttu-id="74660-112">string</span><span class="sxs-lookup"><span data-stu-id="74660-112">string</span></span>  | <span data-ttu-id="74660-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="74660-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="74660-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="74660-115">Content-Type</span></span> | <span data-ttu-id="74660-116">string</span><span class="sxs-lookup"><span data-stu-id="74660-116">string</span></span> | <span data-ttu-id="74660-p102">`text/html` o `application/xhtml+xml` para el contenido HTML, también para la parte requerida "Presentación" de las solicitudes de varias partes. Las solicitudes de varias partes usan el tipo de contenido `multipart/form-data; boundary=your-boundary`.</span><span class="sxs-lookup"><span data-stu-id="74660-p102">`text/html` or `application/xhtml+xml` for the HTML content, including for the required "Presentation" part of multipart requests. Multipart requests use the `multipart/form-data; boundary=your-boundary` content type.</span></span> |

## <a name="request-body"></a><span data-ttu-id="74660-119">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="74660-119">Request body</span></span>
<span data-ttu-id="74660-120">En el cuerpo de la solicitud, facilite el contenido HTML de la página.</span><span class="sxs-lookup"><span data-stu-id="74660-120">In the request body, supply the page HTML content.</span></span>

<span data-ttu-id="74660-p103">El cuerpo puede contener código HTML ubicado directamente en el cuerpo de la solicitud o un formato de mensaje de varias partes, como se muestra en el ejemplo. Si quiere enviar datos binarios, debe enviar una solicitud de varias partes.</span><span class="sxs-lookup"><span data-stu-id="74660-p103">The body can contain HTML placed directly in the request body, or it can contain a multipart message format as shown in the example. If you're sending binary data, then you must send a multipart request.</span></span>

## <a name="response"></a><span data-ttu-id="74660-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74660-123">Response</span></span>

<span data-ttu-id="74660-124">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el nuevo objeto [page](../resources/page.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="74660-124">If successful, this method returns `201 Created` response code and the new [page](../resources/page.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="74660-125">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="74660-125">Example</span></span>
##### <a name="request"></a><span data-ttu-id="74660-126">Solicitud</span><span class="sxs-lookup"><span data-stu-id="74660-126">Request</span></span>
<span data-ttu-id="74660-127">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="74660-127">Here is an example of the request.</span></span>

<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/sections/{id}/pages
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
##### <a name="response"></a><span data-ttu-id="74660-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="74660-128">Response</span></span>
<span data-ttu-id="74660-p104">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="74660-p104">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
