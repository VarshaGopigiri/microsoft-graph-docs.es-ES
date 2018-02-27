# <a name="delete-educationclass"></a><span data-ttu-id="41522-101">Eliminar educationClass</span><span class="sxs-lookup"><span data-stu-id="41522-101">Delete educationClass</span></span>

<span data-ttu-id="41522-102">Elimine una clase.</span><span class="sxs-lookup"><span data-stu-id="41522-102">Delete a class.</span></span> <span data-ttu-id="41522-103">Dado que una clase es también un grupo universal, al eliminar una clase se elimina el grupo.</span><span class="sxs-lookup"><span data-stu-id="41522-103">Because a class is also a universal group, deleting a class deletes the group.</span></span>

## <a name="permissions"></a><span data-ttu-id="41522-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="41522-104">Permissions</span></span>
<span data-ttu-id="41522-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="41522-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="41522-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="41522-107">Permission type</span></span>      | <span data-ttu-id="41522-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="41522-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="41522-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="41522-109">Delegated (work or school account)</span></span> |  <span data-ttu-id="41522-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41522-110">Not supported.</span></span>  |
|<span data-ttu-id="41522-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="41522-111">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="41522-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="41522-112">Not supported.</span></span>  |
|<span data-ttu-id="41522-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="41522-113">Application</span></span> | <span data-ttu-id="41522-114">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="41522-114">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="41522-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="41522-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}

```
## <a name="request-headers"></a><span data-ttu-id="41522-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="41522-116">Request headers</span></span>
| <span data-ttu-id="41522-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41522-117">Header</span></span>       | <span data-ttu-id="41522-118">Valor</span><span class="sxs-lookup"><span data-stu-id="41522-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="41522-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="41522-119">Authorization</span></span>  | <span data-ttu-id="41522-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="41522-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="41522-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="41522-122">Request body</span></span>
<span data-ttu-id="41522-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="41522-123">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="41522-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41522-124">Response</span></span>
<span data-ttu-id="41522-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41522-p104">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="41522-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="41522-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="41522-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="41522-128">Request</span></span>
<span data-ttu-id="41522-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41522-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationclass"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/classes/11022
```
##### <a name="response"></a><span data-ttu-id="41522-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="41522-130">Response</span></span>
<span data-ttu-id="41522-131">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="41522-131">The following is an example of the response.</span></span> 

<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Delete educationClass",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->