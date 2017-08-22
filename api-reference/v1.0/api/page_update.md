# <a name="update-page"></a><span data-ttu-id="c3c42-101">Actualizar página</span><span class="sxs-lookup"><span data-stu-id="c3c42-101">Update page</span></span>

<span data-ttu-id="c3c42-102">Actualice el contenido de una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="c3c42-102">Update the content of a OneNote page.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c3c42-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c3c42-103">Prerequisites</span></span>
<span data-ttu-id="c3c42-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="c3c42-104">One of the following **scopes** is required to execute this API:</span></span>   

<span data-ttu-id="c3c42-105">Notes.ReadWrite o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c3c42-105">Notes.ReadWrite, or Notes.ReadWrite.All</span></span> 

## <a name="http-request"></a><span data-ttu-id="c3c42-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c3c42-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/onenote/pages/{id}/content
PATCH /users/{id | userPrincipalName}/onenote/pages/{id}/content
PATCH /groups/{id}/onenote/pages/{id}/content
PATCH /sites/{id}/onenote/pages/{id}/content
```
## <a name="request-headers"></a><span data-ttu-id="c3c42-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c3c42-107">Request headers</span></span>
| <span data-ttu-id="c3c42-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="c3c42-108">Name</span></span>       | <span data-ttu-id="c3c42-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c3c42-109">Type</span></span> | <span data-ttu-id="c3c42-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c3c42-110">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c3c42-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="c3c42-111">Authorization</span></span>  | <span data-ttu-id="c3c42-112">string</span><span class="sxs-lookup"><span data-stu-id="c3c42-112">string</span></span>  | <span data-ttu-id="c3c42-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c3c42-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c3c42-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c3c42-115">Content-Type</span></span> | <span data-ttu-id="c3c42-116">string</span><span class="sxs-lookup"><span data-stu-id="c3c42-116">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="c3c42-117">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="c3c42-117">Request body</span></span>
<span data-ttu-id="c3c42-p102">En el cuerpo de la solicitud, proporcione una matriz de objetos [patchContentCommand](../resources/patchcontentcommand.md) que representen los cambios a la página. Para obtener más información y ejemplos, consulte <a href="https://msdn.microsoft.com/office/office365/howto/onenote-update-page">Actualizar páginas de OneNote</a>.</span><span class="sxs-lookup"><span data-stu-id="c3c42-p102">In the request body, supply an array of [patchContentCommand](../resources/patchcontentcommand.md) objects that represent the changes to the page. For more information and examples, see <a href="https://msdn.microsoft.com/office/office365/howto/onenote-update-page">Update OneNote pages</a>.</span></span>

## <a name="response"></a><span data-ttu-id="c3c42-120">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3c42-120">Response</span></span>

<span data-ttu-id="c3c42-p103">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.  No se devuelven datos JSON para una solicitud PATCH.</span><span class="sxs-lookup"><span data-stu-id="c3c42-p103">If successful, this method returns a `204 No Content` response code.  No JSON data is returned for a PATCH request.</span></span>
## <a name="example"></a><span data-ttu-id="c3c42-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c3c42-123">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c3c42-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c3c42-124">Request</span></span>
<span data-ttu-id="c3c42-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c3c42-125">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_page"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/onenote/pages/{id}/content
Content-type: application/json
Content-length: 312

[
   {
    'target':'#para-id',
    'action':'insert',
    'position':'before',
    'content':'<img src="image-url-or-part-name" alt="image-alt-text" />'
  }, 
  {
    'target':'#list-id',
    'action':'append',
    'content':'<li>new-page-content</li>'
  }
]
```
##### <a name="response"></a><span data-ttu-id="c3c42-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c3c42-126">Response</span></span>
<span data-ttu-id="c3c42-127">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c3c42-127">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenotePage"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update page",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
