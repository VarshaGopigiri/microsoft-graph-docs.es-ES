# <a name="delete-photo"></a><span data-ttu-id="7feb7-101">Delete photo</span><span class="sxs-lookup"><span data-stu-id="7feb7-101">Delete photo</span></span>

<span data-ttu-id="7feb7-102">Elimina una foto.</span><span class="sxs-lookup"><span data-stu-id="7feb7-102">Delete a photo.</span></span>
## <a name="permissions"></a><span data-ttu-id="7feb7-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="7feb7-103">Permissions</span></span>
<span data-ttu-id="7feb7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="7feb7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="7feb7-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7feb7-106">Permission type</span></span>      | <span data-ttu-id="7feb7-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7feb7-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="7feb7-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7feb7-108">Delegated (work or school account)</span></span> | <span data-ttu-id="7feb7-109">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7feb7-109">Files.ReadWrite</span></span>    |
|<span data-ttu-id="7feb7-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7feb7-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="7feb7-111">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="7feb7-111">Files.ReadWrite</span></span>    |
|<span data-ttu-id="7feb7-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7feb7-112">Application</span></span> | <span data-ttu-id="7feb7-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7feb7-113">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="7feb7-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7feb7-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id | userPrincipalName}/photo
DELETE /groups/{id}/photo
DELETE /drive/root/createdByUser/photo

```
## <a name="request-headers"></a><span data-ttu-id="7feb7-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7feb7-115">Request headers</span></span>
| <span data-ttu-id="7feb7-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="7feb7-116">Name</span></span>       | <span data-ttu-id="7feb7-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="7feb7-117">Type</span></span> | <span data-ttu-id="7feb7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="7feb7-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="7feb7-119">if-match</span><span class="sxs-lookup"><span data-stu-id="7feb7-119">if-match</span></span>  | <span data-ttu-id="7feb7-120">string</span><span class="sxs-lookup"><span data-stu-id="7feb7-120">string</span></span>  | <span data-ttu-id="7feb7-121">Si se incluye el encabezado de la solicitud y la eTag (o cTag) proporcionada no coincide con la etiqueta actual del archivo, se devuelve una respuesta `412 Precondition Failed` y el elemento no se borrará.</span><span class="sxs-lookup"><span data-stu-id="7feb7-121">If this request header is included and the eTag (or cTag) provided does not match the current tag on the item, a `412 Precondition Failed` response is returned and the item will not be deleted.</span></span>|
| <span data-ttu-id="7feb7-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="7feb7-122">Authorization</span></span>  | <span data-ttu-id="7feb7-123">string</span><span class="sxs-lookup"><span data-stu-id="7feb7-123">string</span></span>  | <span data-ttu-id="7feb7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="7feb7-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="7feb7-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7feb7-126">Request body</span></span>
<span data-ttu-id="7feb7-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7feb7-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7feb7-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7feb7-128">Response</span></span>

<span data-ttu-id="7feb7-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7feb7-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7feb7-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7feb7-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="7feb7-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7feb7-132">Request</span></span>
<span data-ttu-id="7feb7-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7feb7-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
"name": "delete_photo"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/users/{id|userPrincipalName}/photo
```
##### <a name="response"></a><span data-ttu-id="7feb7-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7feb7-134">Response</span></span>
<span data-ttu-id="7feb7-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7feb7-135">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": false
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete photo",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
