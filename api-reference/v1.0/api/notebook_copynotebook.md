# <a name="notebook-copynotebook"></a><span data-ttu-id="c31c8-101">bloc de notas: copyNotebook</span><span class="sxs-lookup"><span data-stu-id="c31c8-101">notebook: copyNotebook</span></span>
<span data-ttu-id="c31c8-p101">Copia un bloc de notas a la carpeta Blocs de notas de la biblioteca de documentos de destino. Se crea la carpeta si no existe.</span><span class="sxs-lookup"><span data-stu-id="c31c8-p101">Copies a notebook to the Notebooks folder in the destination Documents library. The folder is created if it doesn't exist.</span></span>

<span data-ttu-id="c31c8-104">En el caso de las operaciones de copia, siga un patrón de llamada asincrónico:  Llame primero a la acción de copiar y, a continuación, sondee el extremo de la operación para obtener el resultado.</span><span class="sxs-lookup"><span data-stu-id="c31c8-104">For Copy operations, you follow an asynchronous calling pattern:  First call the Copy action, and then poll the operation endpoint for the result.</span></span>

## <a name="permissions"></a><span data-ttu-id="c31c8-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c31c8-105">Permissions</span></span>
<span data-ttu-id="c31c8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c31c8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c31c8-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c31c8-108">Permission type</span></span>      | <span data-ttu-id="c31c8-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c31c8-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c31c8-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c31c8-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c31c8-111">Notes.Create, Notes.ReadWrite, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c31c8-111">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="c31c8-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c31c8-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c31c8-113">Notes.Create, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="c31c8-113">Notes.Create, Notes.ReadWrite, or Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="c31c8-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c31c8-114">Application</span></span> | <span data-ttu-id="c31c8-115">Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c31c8-115">Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c31c8-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c31c8-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/onenote/notebooks/{id}/copyNotebook
POST /users/{id | userPrincipalName}/onenote/notebooks/{id}/copyNotebook
POST /groups/{id}/onenote/notebooks/{id}/copyNotebook
```
## <a name="request-headers"></a><span data-ttu-id="c31c8-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c31c8-117">Request headers</span></span>
| <span data-ttu-id="c31c8-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="c31c8-118">Name</span></span>       | <span data-ttu-id="c31c8-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="c31c8-119">Type</span></span> | <span data-ttu-id="c31c8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="c31c8-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c31c8-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="c31c8-121">Authorization</span></span>  | <span data-ttu-id="c31c8-122">string</span><span class="sxs-lookup"><span data-stu-id="c31c8-122">string</span></span>  | <span data-ttu-id="c31c8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c31c8-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c31c8-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c31c8-125">Content-Type</span></span> | <span data-ttu-id="c31c8-126">string</span><span class="sxs-lookup"><span data-stu-id="c31c8-126">string</span></span> | `application/json` |

## <a name="request-body"></a><span data-ttu-id="c31c8-127">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="c31c8-127">Request body</span></span>
<span data-ttu-id="c31c8-p104">En el cuerpo de la solicitud, proporcione un objeto JSON que contenga los parámetros que necesita la operación. Puede enviarse un cuerpo vacío si no se necesita ninguno.</span><span class="sxs-lookup"><span data-stu-id="c31c8-p104">In the request body, provide a JSON object that contains the parameters that your operation needs. It's okay to send an empty body if none are needed.</span></span>

| <span data-ttu-id="c31c8-130">Parámetro</span><span class="sxs-lookup"><span data-stu-id="c31c8-130">Parameter</span></span>    | <span data-ttu-id="c31c8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="c31c8-131">Type</span></span>   |<span data-ttu-id="c31c8-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="c31c8-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c31c8-133">groupId</span><span class="sxs-lookup"><span data-stu-id="c31c8-133">groupId</span></span>|<span data-ttu-id="c31c8-134">String</span><span class="sxs-lookup"><span data-stu-id="c31c8-134">String</span></span>|<span data-ttu-id="c31c8-p105">El id. del grupo al que se debe copiar. Debe usarse solo cuando copie a un grupo de Office 365.</span><span class="sxs-lookup"><span data-stu-id="c31c8-p105">The id of the group to copy to. Use only when copying to an Office 365 group.</span></span>|
|<span data-ttu-id="c31c8-137">renameAs</span><span class="sxs-lookup"><span data-stu-id="c31c8-137">renameAs</span></span>|<span data-ttu-id="c31c8-138">String</span><span class="sxs-lookup"><span data-stu-id="c31c8-138">String</span></span>|<span data-ttu-id="c31c8-p106">El nombre de la copia. Tiene como valor predeterminado el nombre del elemento existente.</span><span class="sxs-lookup"><span data-stu-id="c31c8-p106">The name of the copy. Defaults to the name of the existing item.</span></span> |

## <a name="response"></a><span data-ttu-id="c31c8-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c31c8-141">Response</span></span>

<span data-ttu-id="c31c8-p107">Si se ejecuta correctamente, este método devuelve un código de respuesta `202 Accepted` y un encabezado `Operation-Location`. Sondee el extremo de Operation-Location para [obtener el estado de la operación de copia](onenoteOperation_get.md).</span><span class="sxs-lookup"><span data-stu-id="c31c8-p107">If successful, this method returns a `202 Accepted` response code and an `Operation-Location` header. Poll the Operation-Location endpoint to [get the status of the copy operation](onenoteOperation_get.md).</span></span>

## <a name="example"></a><span data-ttu-id="c31c8-144">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c31c8-144">Example</span></span>
<span data-ttu-id="c31c8-145">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c31c8-145">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c31c8-146">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c31c8-146">Request</span></span>
<span data-ttu-id="c31c8-147">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c31c8-147">Here is an example of the request.</span></span>
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

##### <a name="response"></a><span data-ttu-id="c31c8-148">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c31c8-148">Response</span></span>
<span data-ttu-id="c31c8-149">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c31c8-149">Here is an example of the response.</span></span>
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
