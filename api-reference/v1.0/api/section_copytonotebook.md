# <a name="section-copytonotebook"></a><span data-ttu-id="f6986-101">sección: copyToNotebook</span><span class="sxs-lookup"><span data-stu-id="f6986-101">section: copyToNotebook</span></span>
<span data-ttu-id="f6986-102">Copia una sección a un bloc de notas específico.</span><span class="sxs-lookup"><span data-stu-id="f6986-102">Copies a section to a specific notebook.</span></span>

<span data-ttu-id="f6986-103">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="f6986-103">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f6986-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f6986-104">Prerequisites</span></span>
<span data-ttu-id="f6986-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="f6986-105">One of the following **scopes** is required to execute this API:</span></span>   

<span data-ttu-id="f6986-106">Notes.Create, Notes.ReadWrite o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f6986-106">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span> 

## <a name="http-request"></a><span data-ttu-id="f6986-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f6986-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sections/{id}/copyToNotebook
POST /users/{id | userPrincipalName}/onenote/sections/{id}/copyToNotebook
POST /groups/{id}/onenote/sections/{id}/copyToNotebook
```
## <a name="request-headers"></a><span data-ttu-id="f6986-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f6986-108">Request headers</span></span>
| <span data-ttu-id="f6986-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="f6986-109">Name</span></span>       | <span data-ttu-id="f6986-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6986-110">Type</span></span> | <span data-ttu-id="f6986-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6986-111">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f6986-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="f6986-112">Authorization</span></span>  | <span data-ttu-id="f6986-113">string</span><span class="sxs-lookup"><span data-stu-id="f6986-113">string</span></span>  | <span data-ttu-id="f6986-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f6986-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="f6986-116">Content-Type</span><span class="sxs-lookup"><span data-stu-id="f6986-116">Content-Type</span></span> | <span data-ttu-id="f6986-117">string</span><span class="sxs-lookup"><span data-stu-id="f6986-117">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="f6986-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f6986-118">Request body</span></span>
<span data-ttu-id="f6986-119">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación.</span><span class="sxs-lookup"><span data-stu-id="f6986-119">In the request body, provide a JSON object that contains the parameters that your operation needs.</span></span>

| <span data-ttu-id="f6986-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="f6986-120">Parameter</span></span>    | <span data-ttu-id="f6986-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="f6986-121">Type</span></span>   |<span data-ttu-id="f6986-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="f6986-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f6986-123">groupId</span><span class="sxs-lookup"><span data-stu-id="f6986-123">groupId</span></span>|<span data-ttu-id="f6986-124">String</span><span class="sxs-lookup"><span data-stu-id="f6986-124">String</span></span>|<span data-ttu-id="f6986-p102">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="f6986-p102">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="f6986-127">id</span><span class="sxs-lookup"><span data-stu-id="f6986-127">id</span></span>|<span data-ttu-id="f6986-128">String</span><span class="sxs-lookup"><span data-stu-id="f6986-128">String</span></span>|<span data-ttu-id="f6986-p103">Obligatorio. El id. del bloc de notas de destino.</span><span class="sxs-lookup"><span data-stu-id="f6986-p103">Required. The id of the destination notebook.</span></span> |
|<span data-ttu-id="f6986-131">renameAs</span><span class="sxs-lookup"><span data-stu-id="f6986-131">renameAs</span></span>|<span data-ttu-id="f6986-132">String</span><span class="sxs-lookup"><span data-stu-id="f6986-132">String</span></span>|<span data-ttu-id="f6986-p104">El nombre de la copia. Tiene como valor predeterminado el nombre del elemento existente.</span><span class="sxs-lookup"><span data-stu-id="f6986-p104">The name of the copy. Defaults to the name of the existing item.</span></span> |

## <a name="response"></a><span data-ttu-id="f6986-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6986-135">Response</span></span>

<span data-ttu-id="f6986-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation_get.md).</span><span class="sxs-lookup"><span data-stu-id="f6986-p105">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteoperation_get.md).</span></span>

## <a name="example"></a><span data-ttu-id="f6986-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6986-138">Example</span></span>
<span data-ttu-id="f6986-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="f6986-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="f6986-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f6986-140">Request</span></span>
<span data-ttu-id="f6986-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f6986-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "section_copytonotebook"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/sections/{id}/copyToNotebook
Content-type: application/json
Content-length: 84

{
  "id": "id-value",
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <a name="response"></a><span data-ttu-id="f6986-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6986-142">Response</span></span>
<span data-ttu-id="f6986-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6986-143">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.onenoteOperation"
} -->
```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "section: copyToNotebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->