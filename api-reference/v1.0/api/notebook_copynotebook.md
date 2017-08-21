# <a name="notebook-copynotebook"></a><span data-ttu-id="bdf7d-101">bloc de notas: copyNotebook</span><span class="sxs-lookup"><span data-stu-id="bdf7d-101">notebook: copyNotebook</span></span>
<span data-ttu-id="bdf7d-p101">Copia un bloc de notas a la carpeta Blocs de notas de la biblioteca de documentos de destino. Se crea la carpeta si no existe.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-p101">Copies a notebook to the Notebooks folder in the destination Documents library. The folder is created if it doesn't exist.</span></span>

<span data-ttu-id="bdf7d-104">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-104">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bdf7d-105">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="bdf7d-105">Prerequisites</span></span>
<span data-ttu-id="bdf7d-106">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="bdf7d-106">One of the following **scopes** is required to execute this API:</span></span>   

<span data-ttu-id="bdf7d-107">Notes.Create, Notes.ReadWrite o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bdf7d-107">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span> 

## <a name="http-request"></a><span data-ttu-id="bdf7d-108">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bdf7d-108">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/notebooks/{id}/copyNotebook
POST /users/{id | userPrincipalName}/onenote/notebooks/{id}/copyNotebook
POST /groups/{id}/onenote/notebooks/{id}/copyNotebook
```
## <a name="request-headers"></a><span data-ttu-id="bdf7d-109">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bdf7d-109">Request headers</span></span>
| <span data-ttu-id="bdf7d-110">Nombre</span><span class="sxs-lookup"><span data-stu-id="bdf7d-110">Name</span></span>       | <span data-ttu-id="bdf7d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="bdf7d-111">Type</span></span> | <span data-ttu-id="bdf7d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdf7d-112">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="bdf7d-113">Authorization</span><span class="sxs-lookup"><span data-stu-id="bdf7d-113">Authorization</span></span>  | <span data-ttu-id="bdf7d-114">string</span><span class="sxs-lookup"><span data-stu-id="bdf7d-114">string</span></span>  | <span data-ttu-id="bdf7d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="bdf7d-117">Content-Type</span><span class="sxs-lookup"><span data-stu-id="bdf7d-117">Content-Type</span></span> | <span data-ttu-id="bdf7d-118">string</span><span class="sxs-lookup"><span data-stu-id="bdf7d-118">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="bdf7d-119">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="bdf7d-119">Request body</span></span>
<span data-ttu-id="bdf7d-p103">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación. Puede enviarse un cuerpo vacío si no se necesita ninguno.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-p103">In the request body, provide a JSON object that contains the parameters that your operation needs. It's okay to send an empty body if none are needed.</span></span>

| <span data-ttu-id="bdf7d-122">Parámetro</span><span class="sxs-lookup"><span data-stu-id="bdf7d-122">Parameter</span></span>    | <span data-ttu-id="bdf7d-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="bdf7d-123">Type</span></span>   |<span data-ttu-id="bdf7d-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="bdf7d-124">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bdf7d-125">groupId</span><span class="sxs-lookup"><span data-stu-id="bdf7d-125">groupId</span></span>|<span data-ttu-id="bdf7d-126">String</span><span class="sxs-lookup"><span data-stu-id="bdf7d-126">String</span></span>|<span data-ttu-id="bdf7d-p104">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-p104">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="bdf7d-129">renameAs</span><span class="sxs-lookup"><span data-stu-id="bdf7d-129">renameAs</span></span>|<span data-ttu-id="bdf7d-130">String</span><span class="sxs-lookup"><span data-stu-id="bdf7d-130">String</span></span>|<span data-ttu-id="bdf7d-p105">El nombre de la copia. Tiene como valor predeterminado el nombre del elemento existente.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-p105">The name of the copy. Defaults to the name of the existing item.</span></span> |

## <a name="response"></a><span data-ttu-id="bdf7d-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bdf7d-133">Response</span></span>

<span data-ttu-id="bdf7d-p106">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteOperation_get.md).</span><span class="sxs-lookup"><span data-stu-id="bdf7d-p106">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteOperation_get.md).</span></span>

## <a name="example"></a><span data-ttu-id="bdf7d-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bdf7d-136">Example</span></span>
<span data-ttu-id="bdf7d-137">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-137">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="bdf7d-138">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bdf7d-138">Request</span></span>
<span data-ttu-id="bdf7d-139">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-139">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "notebook_copynotebook"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/notebooks/{id}/copyNotebook
Content-type: application/json
Content-length: 108

{
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <a name="response"></a><span data-ttu-id="bdf7d-140">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bdf7d-140">Response</span></span>
<span data-ttu-id="bdf7d-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bdf7d-141">Here is an example of the response.</span></span>
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
  "description": "notebook: copyNotebook",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
