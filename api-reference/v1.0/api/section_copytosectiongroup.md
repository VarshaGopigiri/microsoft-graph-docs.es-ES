# <a name="section-copytosectiongroup"></a><span data-ttu-id="fee93-101">sección: copyToSectionGroup</span><span class="sxs-lookup"><span data-stu-id="fee93-101">section: copyToSectionGroup</span></span>
<span data-ttu-id="fee93-102">Copia una sección a un grupo de secciones específico.</span><span class="sxs-lookup"><span data-stu-id="fee93-102">Copies a section to a specific section group.</span></span>

<span data-ttu-id="fee93-103">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="fee93-103">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fee93-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="fee93-104">Prerequisites</span></span>
<span data-ttu-id="fee93-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="fee93-105">One of the following **scopes** is required to execute this API:</span></span>   

<span data-ttu-id="fee93-106">Notes.Create, Notes.ReadWrite o Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="fee93-106">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span> 

## <a name="http-request"></a><span data-ttu-id="fee93-107">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fee93-107">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/sections/{id}/copyToSectionGroup
POST /users/{id | userPrincipalName}/onenote/sections/{id}/copyToSectionGroup
POST /groups/{id}/onenote/sections/{id}/copyToSectionGroup
```
## <a name="request-headers"></a><span data-ttu-id="fee93-108">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fee93-108">Request headers</span></span>
| <span data-ttu-id="fee93-109">Nombre</span><span class="sxs-lookup"><span data-stu-id="fee93-109">Name</span></span>       | <span data-ttu-id="fee93-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="fee93-110">Type</span></span> | <span data-ttu-id="fee93-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="fee93-111">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="fee93-112">Authorization</span><span class="sxs-lookup"><span data-stu-id="fee93-112">Authorization</span></span>  | <span data-ttu-id="fee93-113">string</span><span class="sxs-lookup"><span data-stu-id="fee93-113">string</span></span>  | <span data-ttu-id="fee93-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fee93-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fee93-116">Content-Type</span><span class="sxs-lookup"><span data-stu-id="fee93-116">Content-Type</span></span> | <span data-ttu-id="fee93-117">string</span><span class="sxs-lookup"><span data-stu-id="fee93-117">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="fee93-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fee93-118">Request body</span></span>
<span data-ttu-id="fee93-119">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación.</span><span class="sxs-lookup"><span data-stu-id="fee93-119">In the request body, provide a JSON object that contains the parameters that your operation needs.</span></span>

| <span data-ttu-id="fee93-120">Parámetro</span><span class="sxs-lookup"><span data-stu-id="fee93-120">Parameter</span></span>    | <span data-ttu-id="fee93-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="fee93-121">Type</span></span>   |<span data-ttu-id="fee93-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="fee93-122">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fee93-123">groupId</span><span class="sxs-lookup"><span data-stu-id="fee93-123">groupId</span></span>|<span data-ttu-id="fee93-124">String</span><span class="sxs-lookup"><span data-stu-id="fee93-124">String</span></span>|<span data-ttu-id="fee93-p102">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="fee93-p102">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="fee93-127">id</span><span class="sxs-lookup"><span data-stu-id="fee93-127">id</span></span>|<span data-ttu-id="fee93-128">String</span><span class="sxs-lookup"><span data-stu-id="fee93-128">String</span></span>|<span data-ttu-id="fee93-p103">Obligatorio. El id. del grupo de secciones de destino.</span><span class="sxs-lookup"><span data-stu-id="fee93-p103">Required. The id of the destination section group.</span></span> |
|<span data-ttu-id="fee93-131">renameAs</span><span class="sxs-lookup"><span data-stu-id="fee93-131">renameAs</span></span>|<span data-ttu-id="fee93-132">String</span><span class="sxs-lookup"><span data-stu-id="fee93-132">String</span></span>|<span data-ttu-id="fee93-p104">El nombre de la copia. Tiene como valor predeterminado el nombre del elemento existente.</span><span class="sxs-lookup"><span data-stu-id="fee93-p104">The name of the copy. Defaults to the name of the existing item.</span></span> |

<!--groupId missing-->
<!--|siteCollectionId|String||
|siteId|String||-->

## <a name="response"></a><span data-ttu-id="fee93-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fee93-135">Response</span></span>

<span data-ttu-id="fee93-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation_get.md).</span><span class="sxs-lookup"><span data-stu-id="fee93-p105">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteoperation_get.md).</span></span>

## <a name="example"></a><span data-ttu-id="fee93-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fee93-138">Example</span></span>
<span data-ttu-id="fee93-139">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="fee93-139">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="fee93-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fee93-140">Request</span></span>
<span data-ttu-id="fee93-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fee93-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "section_copytosectiongroup"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/onenote/sections/{id}/copyToSectionGroup
Content-type: application/json
Content-length: 84

{
  "id": "id-value",
  "groupId": "groupId-value",
  "renameAs": "renameAs-value"
}
```

##### <a name="response"></a><span data-ttu-id="fee93-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fee93-142">Response</span></span>
<span data-ttu-id="fee93-143">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fee93-143">Here is an example of the response.</span></span>
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
  "description": "section: copyToSectionGroup",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->