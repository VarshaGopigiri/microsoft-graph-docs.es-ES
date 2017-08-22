# <a name="create-notebook"></a><span data-ttu-id="702d6-101">Crear bloc de notas</span><span class="sxs-lookup"><span data-stu-id="702d6-101">Create notebook</span></span>

<span data-ttu-id="702d6-102">Cree un [bloc de notas](../resources/notebook.md) de OneNote.</span><span class="sxs-lookup"><span data-stu-id="702d6-102">Create a new OneNote [notebook](../resources/notebook.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="702d6-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="702d6-103">Prerequisites</span></span>
<span data-ttu-id="702d6-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="702d6-104">One of the following **scopes** is required to execute this API:</span></span>   

<span data-ttu-id="702d6-105">Notes.Create, Notes.ReadWrite o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="702d6-105">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="702d6-106">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="702d6-106">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/notebooks
POST /users/{id | userPrincipalName}/onenote/notebooks
POST /groups/{id}/onenote/notebooks
POST /sites/{id}/onenote/notebooks
```
## <a name="request-headers"></a><span data-ttu-id="702d6-107">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="702d6-107">Request headers</span></span>
| <span data-ttu-id="702d6-108">Nombre</span><span class="sxs-lookup"><span data-stu-id="702d6-108">Name</span></span>       | <span data-ttu-id="702d6-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="702d6-109">Type</span></span> | <span data-ttu-id="702d6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="702d6-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="702d6-111">Authorization</span><span class="sxs-lookup"><span data-stu-id="702d6-111">Authorization</span></span>  | <span data-ttu-id="702d6-112">string</span><span class="sxs-lookup"><span data-stu-id="702d6-112">string</span></span>  | <span data-ttu-id="702d6-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="702d6-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="702d6-115">Content-Type</span><span class="sxs-lookup"><span data-stu-id="702d6-115">Content-Type</span></span> | <span data-ttu-id="702d6-116">string</span><span class="sxs-lookup"><span data-stu-id="702d6-116">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="702d6-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="702d6-117">Request body</span></span>
<span data-ttu-id="702d6-118">En el cuerpo de la solicitud, asigne un nombre al bloc de notas.</span><span class="sxs-lookup"><span data-stu-id="702d6-118">In the request body, supply a name for the notebook.</span></span> 

<span data-ttu-id="702d6-p102">Los nombres del bloc de notas deben ser únicos. El nombre no puede contener más de 128 caracteres ni los caracteres siguientes: ?*\/:<>|'"</span><span class="sxs-lookup"><span data-stu-id="702d6-p102">Notebook names must be unique. The name cannot contain more than 128 characters or contain the following characters:  ?*\/:<>|'"</span></span>

## <a name="response"></a><span data-ttu-id="702d6-121">Respuesta</span><span class="sxs-lookup"><span data-stu-id="702d6-121">Response</span></span>

<span data-ttu-id="702d6-122">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y el nuevo objeto [notebook](../resources/notebook.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="702d6-122">If successful, this method returns a `201 Created` response code and the new [notebook](../resources/notebook.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="702d6-123">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="702d6-123">Example</span></span>
##### <a name="request"></a><span data-ttu-id="702d6-124">Solicitud</span><span class="sxs-lookup"><span data-stu-id="702d6-124">Request</span></span>
<span data-ttu-id="702d6-125">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="702d6-125">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_notebook_from_onenote"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/notebooks
Content-type: application/json
Content-length: 30

{
  "displayName": "Notebook name"
}
```

##### <a name="response"></a><span data-ttu-id="702d6-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="702d6-126">Response</span></span>
<span data-ttu-id="702d6-p103">Aquí tiene un ejemplo de la respuesta. Nota: El objeto de respuesta que aparece aquí esté truncado para abreviar. Se devolverán todas las propiedades de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="702d6-p103">Here is an example of the response. Note: The response object shown here is truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.notebook"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 284

{
  "isDefault": true,
  "userRole": {
  },
  "isShared": true,
  "sectionsUrl": "sectionsUrl-value",
  "sectionGroupsUrl": "sectionGroupsUrl-value",
  "links": {
    "oneNoteClientUrl": {
      "href": "href-value"
    },
    "oneNoteWebUrl": {
      "href": "href-value"
    }
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Notebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->