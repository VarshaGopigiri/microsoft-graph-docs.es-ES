# <a name="delete-educationclass"></a><span data-ttu-id="9246a-101">Eliminar educationClass</span><span class="sxs-lookup"><span data-stu-id="9246a-101">Delete educationClass</span></span>

<span data-ttu-id="9246a-102">Elimine una clase.</span><span class="sxs-lookup"><span data-stu-id="9246a-102">Delete a class.</span></span> <span data-ttu-id="9246a-103">Dado que una clase es también un grupo universal, al eliminar una clase se elimina el grupo.</span><span class="sxs-lookup"><span data-stu-id="9246a-103">Because a class is also a universal group, deleting a class deletes the group.</span></span>

## <a name="permissions"></a><span data-ttu-id="9246a-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="9246a-104">Permissions</span></span>
<span data-ttu-id="9246a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9246a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9246a-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9246a-107">Permission type</span></span>      | <span data-ttu-id="9246a-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9246a-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9246a-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9246a-109">Delegated (work or school account)</span></span> |  <span data-ttu-id="9246a-110">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9246a-110">Not supported.</span></span>  |
|<span data-ttu-id="9246a-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9246a-111">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="9246a-112">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9246a-112">Not supported.</span></span>  |
|<span data-ttu-id="9246a-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9246a-113">Application</span></span> | <span data-ttu-id="9246a-114">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9246a-114">EduRoster.ReadWrite.All</span></span> | 

## <a name="http-request"></a><span data-ttu-id="9246a-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9246a-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/classes/{id}

```
## <a name="request-headers"></a><span data-ttu-id="9246a-116">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9246a-116">Request headers</span></span>
| <span data-ttu-id="9246a-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9246a-117">Header</span></span>       | <span data-ttu-id="9246a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="9246a-118">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9246a-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="9246a-119">Authorization</span></span>  | <span data-ttu-id="9246a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9246a-p103">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9246a-122">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9246a-122">Request body</span></span>
<span data-ttu-id="9246a-123">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9246a-123">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="9246a-124">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9246a-124">Response</span></span>
<span data-ttu-id="9246a-p104">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9246a-p104">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9246a-127">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9246a-127">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9246a-128">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9246a-128">Request</span></span>
<span data-ttu-id="9246a-129">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9246a-129">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationclass"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/classes/{class-id}
```
##### <a name="response"></a><span data-ttu-id="9246a-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9246a-130">Response</span></span>
<span data-ttu-id="9246a-131">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9246a-131">The following is an example of the response.</span></span> 

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