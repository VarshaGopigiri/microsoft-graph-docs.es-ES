# <a name="get-resource"></a><span data-ttu-id="76a90-101">Obtener recurso</span><span class="sxs-lookup"><span data-stu-id="76a90-101">Get resource</span></span>

<span data-ttu-id="76a90-102">Recupera los datos binarios de un objeto [resource](../resources/resource.md) de un archivo o una imagen.</span><span class="sxs-lookup"><span data-stu-id="76a90-102">Retrieve the binary data of a file or image [resource](../resources/resource.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="76a90-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="76a90-103">Permissions</span></span>
<span data-ttu-id="76a90-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="76a90-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="76a90-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="76a90-106">Permission type</span></span>      | <span data-ttu-id="76a90-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="76a90-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="76a90-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="76a90-108">Delegated (work or school account)</span></span> | <span data-ttu-id="76a90-109">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="76a90-109">Notes.Read, Notes.ReadWrite, Notes.Read.All, Notes.ReadWrite.All</span></span>    |
|<span data-ttu-id="76a90-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="76a90-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="76a90-111">Notes.Read, Notes.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="76a90-111">Notes.Read, Notes.ReadWrite</span></span>    |
|<span data-ttu-id="76a90-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="76a90-112">Application</span></span> | <span data-ttu-id="76a90-113">Notes.Read.All, Notes.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="76a90-113">Notes.Read.All, Notes.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="76a90-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="76a90-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
GET /me/onenote/resources/{id}/content
GET /users/{id | userPrincipalName}/onenote/resources/{id}/content
GET /groups/{id}/onenote/resources/{id}/content
GET /sites/{id}/onenote/resources/{id}/content
```

## <a name="request-headers"></a><span data-ttu-id="76a90-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="76a90-115">Request headers</span></span>
| <span data-ttu-id="76a90-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="76a90-116">Name</span></span>       | <span data-ttu-id="76a90-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="76a90-117">Type</span></span> | <span data-ttu-id="76a90-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="76a90-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="76a90-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="76a90-119">Authorization</span></span>  | <span data-ttu-id="76a90-120">cadena</span><span class="sxs-lookup"><span data-stu-id="76a90-120">string</span></span>  | <span data-ttu-id="76a90-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="76a90-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="76a90-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="76a90-123">Request body</span></span>
<span data-ttu-id="76a90-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="76a90-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="76a90-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76a90-125">Response</span></span>

<span data-ttu-id="76a90-126">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y los datos binarios del archivo o la imagen en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76a90-126">If successful, this method returns a `200 OK` response code and the image or file binary data in the response body.</span></span>

<span data-ttu-id="76a90-127">Nota: Las imágenes no se procesan directamente en un explorador porque requieren autorización para recuperarlas, al igual que el resto del contenido de la página.</span><span class="sxs-lookup"><span data-stu-id="76a90-127">Note: Images won't render directly in a browser because they require authorization to retrieve them, like the rest of the page content.</span></span>
## <a name="example"></a><span data-ttu-id="76a90-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="76a90-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="76a90-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="76a90-129">Request</span></span>
<span data-ttu-id="76a90-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="76a90-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "get_resource"
}-->
```http
GET https://graph.microsoft.com/v1.0/me/onenote/resources/{id}/content
```
##### <a name="response"></a><span data-ttu-id="76a90-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="76a90-131">Response</span></span>
<span data-ttu-id="76a90-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="76a90-132">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Edm.Stream"
} -->
```http
HTTP/1.1 200 OK
Content-Type: application/octet-stream

...binary data...
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
