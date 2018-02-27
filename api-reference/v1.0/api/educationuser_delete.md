# <a name="delete-educationuser"></a><span data-ttu-id="c6028-101">Eliminar educationUser</span><span class="sxs-lookup"><span data-stu-id="c6028-101">Delete educationUser</span></span>

<span data-ttu-id="c6028-102">Elimine un usuario.</span><span class="sxs-lookup"><span data-stu-id="c6028-102">Delete a user</span></span>


## <a name="permissions"></a><span data-ttu-id="c6028-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="c6028-103">Permissions</span></span>
<span data-ttu-id="c6028-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="c6028-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="c6028-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c6028-106">Permission type</span></span>      | <span data-ttu-id="c6028-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c6028-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c6028-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c6028-108">Delegated (work or school account)</span></span> |  <span data-ttu-id="c6028-109">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6028-109">Not supported.</span></span>  |
|<span data-ttu-id="c6028-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c6028-110">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="c6028-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c6028-111">Not supported.</span></span>  |
|<span data-ttu-id="c6028-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c6028-112">Application</span></span> | <span data-ttu-id="c6028-113">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c6028-113">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c6028-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c6028-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="c6028-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c6028-115">Request headers</span></span>
| <span data-ttu-id="c6028-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c6028-116">Header</span></span>       | <span data-ttu-id="c6028-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c6028-117">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c6028-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="c6028-118">Authorization</span></span>  | <span data-ttu-id="c6028-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6028-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c6028-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6028-121">Request body</span></span>
<span data-ttu-id="c6028-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c6028-122">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="c6028-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6028-123">Response</span></span>
<span data-ttu-id="c6028-p103">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6028-p103">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c6028-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6028-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c6028-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6028-127">Request</span></span>
<span data-ttu-id="c6028-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c6028-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationuser"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/users/13019
```
##### <a name="response"></a><span data-ttu-id="c6028-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6028-129">Response</span></span>
<span data-ttu-id="c6028-130">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6028-130">The following is an example of the response.</span></span> 
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
  "description": "Delete educationUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->