# <a name="update-page"></a><span data-ttu-id="e5920-101">Actualizar página</span><span class="sxs-lookup"><span data-stu-id="e5920-101">Update page</span></span>

<span data-ttu-id="e5920-102">Actualiza el contenido de una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="e5920-102">Update the content of a OneNote page.</span></span>
## <a name="permissions"></a><span data-ttu-id="e5920-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="e5920-103">Permissions</span></span>
<span data-ttu-id="e5920-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e5920-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e5920-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e5920-106">Permission type</span></span>      | <span data-ttu-id="e5920-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e5920-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e5920-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e5920-108">Delegated (work or school account)</span></span> | <span data-ttu-id="e5920-109">Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e5920-109">Notes.ReadWrite, or Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="e5920-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e5920-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e5920-111">Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e5920-111">Notes.ReadWrite</span></span>    |
|<span data-ttu-id="e5920-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e5920-112">Application</span></span> | <span data-ttu-id="e5920-113">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e5920-113">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="e5920-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e5920-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/onenote/pages/{id}/content
PATCH /users/{id | userPrincipalName}/onenote/pages/{id}/content
PATCH /groups/{id}/onenote/pages/{id}/content
PATCH /sites/{id}/onenote/pages/{id}/content
```
## <a name="request-headers"></a><span data-ttu-id="e5920-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5920-115">Request headers</span></span>
| <span data-ttu-id="e5920-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="e5920-116">Name</span></span>       | <span data-ttu-id="e5920-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="e5920-117">Type</span></span> | <span data-ttu-id="e5920-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5920-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e5920-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="e5920-119">Authorization</span></span>  | <span data-ttu-id="e5920-120">string</span><span class="sxs-lookup"><span data-stu-id="e5920-120">string</span></span>  | <span data-ttu-id="e5920-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e5920-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e5920-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e5920-123">Content-Type</span></span> | <span data-ttu-id="e5920-124">string</span><span class="sxs-lookup"><span data-stu-id="e5920-124">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="e5920-125">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="e5920-125">Request body</span></span>
<span data-ttu-id="e5920-p103">En el cuerpo de la solicitud, proporcione una matriz de objetos [patchContentCommand](../resources/patchcontentcommand.md) que representen los cambios a la página. Para obtener más información y ejemplos, consulte <a href="https://msdn.microsoft.com/office/office365/howto/onenote-update-page">Actualizar páginas de OneNote</a>.</span><span class="sxs-lookup"><span data-stu-id="e5920-p103">In the request body, supply an array of [patchContentCommand](../resources/patchcontentcommand.md) objects that represent the changes to the page. For more information and examples, see <a href="https://msdn.microsoft.com/office/office365/howto/onenote-update-page">Update OneNote pages</a>.</span></span>

## <a name="response"></a><span data-ttu-id="e5920-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5920-128">Response</span></span>

<span data-ttu-id="e5920-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.  No se devuelven datos JSON para una solicitud PATCH.</span><span class="sxs-lookup"><span data-stu-id="e5920-p104">If successful, this method returns a `204 No Content` response code.  No JSON data is returned for a PATCH request.</span></span>
## <a name="example"></a><span data-ttu-id="e5920-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e5920-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e5920-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e5920-132">Request</span></span>
<span data-ttu-id="e5920-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e5920-133">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="e5920-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e5920-134">Response</span></span>
<span data-ttu-id="e5920-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e5920-135">Here is an example of the response.</span></span> 
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
