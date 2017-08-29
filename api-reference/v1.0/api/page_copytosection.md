# <a name="page-copytosection"></a><span data-ttu-id="8a3f8-101">página: copyToSection</span><span class="sxs-lookup"><span data-stu-id="8a3f8-101">page: copyToSection</span></span>
<span data-ttu-id="8a3f8-102">Copia una página en una sección específica.</span><span class="sxs-lookup"><span data-stu-id="8a3f8-102">Copies a page to a specific section.</span></span>

<span data-ttu-id="8a3f8-103">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="8a3f8-103">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>

## <a name="permissions"></a><span data-ttu-id="8a3f8-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="8a3f8-104">Permissions</span></span>
<span data-ttu-id="8a3f8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="8a3f8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="8a3f8-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8a3f8-107">Permission type</span></span>      | <span data-ttu-id="8a3f8-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8a3f8-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8a3f8-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8a3f8-109">Delegated (work or school account)</span></span> | <span data-ttu-id="8a3f8-110">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8a3f8-110">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="8a3f8-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8a3f8-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8a3f8-112">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="8a3f8-112">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="8a3f8-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8a3f8-113">Application</span></span> | <span data-ttu-id="8a3f8-114">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8a3f8-114">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8a3f8-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8a3f8-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/pages/{id}/copyToSection
POST /users/{id | userPrincipalName}/onenote/pages/{id}/copyToSection
POST /groups/{id}/onenote/pages/{id}/copyToSection
```
## <a name="request-headers"></a><span data-ttu-id="8a3f8-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8a3f8-116">Request headers</span></span>
| <span data-ttu-id="8a3f8-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="8a3f8-117">Name</span></span>       | <span data-ttu-id="8a3f8-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a3f8-118">Type</span></span> | <span data-ttu-id="8a3f8-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a3f8-119">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="8a3f8-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="8a3f8-120">Authorization</span></span>  | <span data-ttu-id="8a3f8-121">string</span><span class="sxs-lookup"><span data-stu-id="8a3f8-121">string</span></span>  | <span data-ttu-id="8a3f8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8a3f8-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="8a3f8-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8a3f8-124">Content-Type</span></span> | <span data-ttu-id="8a3f8-125">string</span><span class="sxs-lookup"><span data-stu-id="8a3f8-125">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="8a3f8-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8a3f8-126">Request body</span></span>
<span data-ttu-id="8a3f8-127">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación.</span><span class="sxs-lookup"><span data-stu-id="8a3f8-127">In the request body, provide a JSON object that contains the parameters that your operation needs.</span></span>

| <span data-ttu-id="8a3f8-128">Parámetro</span><span class="sxs-lookup"><span data-stu-id="8a3f8-128">Parameter</span></span>    | <span data-ttu-id="8a3f8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a3f8-129">Type</span></span>   |<span data-ttu-id="8a3f8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a3f8-130">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8a3f8-131">groupId</span><span class="sxs-lookup"><span data-stu-id="8a3f8-131">groupId</span></span>|<span data-ttu-id="8a3f8-132">String</span><span class="sxs-lookup"><span data-stu-id="8a3f8-132">String</span></span>|<span data-ttu-id="8a3f8-p103">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="8a3f8-p103">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="8a3f8-135">id</span><span class="sxs-lookup"><span data-stu-id="8a3f8-135">id</span></span>|<span data-ttu-id="8a3f8-136">String</span><span class="sxs-lookup"><span data-stu-id="8a3f8-136">String</span></span>|<span data-ttu-id="8a3f8-p104">Obligatorio. El id. de la sección de destino.</span><span class="sxs-lookup"><span data-stu-id="8a3f8-p104">Required. The id of the destination section.</span></span>|

## <a name="response"></a><span data-ttu-id="8a3f8-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a3f8-139">Response</span></span>

<span data-ttu-id="8a3f8-p105">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteoperation_get.md).</span><span class="sxs-lookup"><span data-stu-id="8a3f8-p105">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteoperation_get.md).</span></span>

## <a name="example"></a><span data-ttu-id="8a3f8-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8a3f8-142">Example</span></span>
<span data-ttu-id="8a3f8-143">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="8a3f8-143">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="8a3f8-144">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8a3f8-144">Request</span></span>
<span data-ttu-id="8a3f8-145">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8a3f8-145">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="8a3f8-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8a3f8-146">Response</span></span>
<span data-ttu-id="8a3f8-147">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8a3f8-147">Here is an example of the response.</span></span>
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