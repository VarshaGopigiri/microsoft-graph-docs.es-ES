# <a name="page-copytosection"></a><span data-ttu-id="2ea6f-101">página: copyToSection</span><span class="sxs-lookup"><span data-stu-id="2ea6f-101">page: copyToSection</span></span>
<span data-ttu-id="2ea6f-102">Copia una página en una sección específica.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-102">Copies a page to a specific section.</span></span>

<span data-ttu-id="2ea6f-103">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-103">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2ea6f-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2ea6f-104">Prerequisites</span></span>
<span data-ttu-id="2ea6f-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="2ea6f-105">One of the following **scopes** is required to execute this API:</span></span>   

<span data-ttu-id="2ea6f-106">Notes.Create, Notes.ReadWrite o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2ea6f-106">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span>  

## <a name="http-request"></a><span data-ttu-id="2ea6f-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2ea6f-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/pages/{id}/copyToSection
POST /users/{id | userPrincipalName}/onenote/pages/{id}/copyToSection
POST /groups/{id}/onenote/pages/{id}/copyToSection
```
## <a name="request-headers"></a><span data-ttu-id="2ea6f-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2ea6f-108">Request headers</span></span>
| <span data-ttu-id="2ea6f-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="2ea6f-109">Name</span></span>       | <span data-ttu-id="2ea6f-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ea6f-110">Type</span></span> | <span data-ttu-id="2ea6f-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ea6f-111">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="2ea6f-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="2ea6f-112">Authorization</span></span>  | <span data-ttu-id="2ea6f-113">string</span><span class="sxs-lookup"><span data-stu-id="2ea6f-113">string</span></span>  | <span data-ttu-id="2ea6f-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="2ea6f-116">Content-Type</span><span class="sxs-lookup"><span data-stu-id="2ea6f-116">Content-Type</span></span> | <span data-ttu-id="2ea6f-117">string</span><span class="sxs-lookup"><span data-stu-id="2ea6f-117">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="2ea6f-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2ea6f-118">Request body</span></span>
<span data-ttu-id="2ea6f-119">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-119">In the request body, provide a JSON object that contains the parameters that your operation needs.</span></span>

| <span data-ttu-id="2ea6f-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2ea6f-120">Parameter</span></span>    | <span data-ttu-id="2ea6f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ea6f-121">Type</span></span>   |<span data-ttu-id="2ea6f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ea6f-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2ea6f-123">groupId</span><span class="sxs-lookup"><span data-stu-id="2ea6f-123">groupId</span></span>|<span data-ttu-id="2ea6f-124">String</span><span class="sxs-lookup"><span data-stu-id="2ea6f-124">String</span></span>|<span data-ttu-id="2ea6f-p102">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-p102">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="2ea6f-127">id</span><span class="sxs-lookup"><span data-stu-id="2ea6f-127">id</span></span>|<span data-ttu-id="2ea6f-128">String</span><span class="sxs-lookup"><span data-stu-id="2ea6f-128">String</span></span>|<span data-ttu-id="2ea6f-p103">Obligatorio. El id. de la sección de destino.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-p103">Required. The id of the destination section.</span></span>|

## <a name="response"></a><span data-ttu-id="2ea6f-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ea6f-131">Response</span></span>

<span data-ttu-id="2ea6f-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation_get.md).</span><span class="sxs-lookup"><span data-stu-id="2ea6f-p104">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteoperation_get.md).</span></span>

## <a name="example"></a><span data-ttu-id="2ea6f-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ea6f-134">Example</span></span>
<span data-ttu-id="2ea6f-135">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-135">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="2ea6f-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ea6f-136">Request</span></span>
<span data-ttu-id="2ea6f-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "page_copytosection"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/pages/{id}/copyToSection
Content-type: application/json
Content-length: 52

{
  "id": "id-value",
  "groupId": "groupId-value"
}
```

##### <a name="response"></a><span data-ttu-id="2ea6f-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ea6f-138">Response</span></span>
<span data-ttu-id="2ea6f-139">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ea6f-139">Here is an example of the response.</span></span>
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
  "description": "page: copyToSection",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->