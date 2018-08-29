# <a name="delete-a-user"></a><span data-ttu-id="d84dd-101">Eliminar un usuario</span><span class="sxs-lookup"><span data-stu-id="d84dd-101">Delete a user</span></span>

<span data-ttu-id="d84dd-102">Elimina usuario.</span><span class="sxs-lookup"><span data-stu-id="d84dd-102">Delete user.</span></span>
## <a name="permissions"></a><span data-ttu-id="d84dd-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="d84dd-103">Permissions</span></span>
<span data-ttu-id="d84dd-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="d84dd-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="d84dd-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="d84dd-106">Permission type</span></span>      | <span data-ttu-id="d84dd-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="d84dd-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="d84dd-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="d84dd-108">Delegated (work or school account)</span></span> | <span data-ttu-id="d84dd-109">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="d84dd-109">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="d84dd-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="d84dd-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="d84dd-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="d84dd-111">Not supported.</span></span>    |
|<span data-ttu-id="d84dd-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="d84dd-112">Application</span></span> | <span data-ttu-id="d84dd-113">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="d84dd-113">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="d84dd-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="d84dd-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id | userPrincipalName}
```

## <a name="request-headers"></a><span data-ttu-id="d84dd-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="d84dd-115">Request headers</span></span>
| <span data-ttu-id="d84dd-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d84dd-116">Header</span></span>       | <span data-ttu-id="d84dd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d84dd-117">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="d84dd-118">Authorization</span><span class="sxs-lookup"><span data-stu-id="d84dd-118">Authorization</span></span>  | <span data-ttu-id="d84dd-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="d84dd-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="d84dd-121">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="d84dd-121">Request body</span></span>
<span data-ttu-id="d84dd-122">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="d84dd-122">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="d84dd-123">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d84dd-123">Response</span></span>

<span data-ttu-id="d84dd-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d84dd-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="d84dd-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="d84dd-126">Example</span></span>
##### <a name="request"></a><span data-ttu-id="d84dd-127">Solicitud</span><span class="sxs-lookup"><span data-stu-id="d84dd-127">Request</span></span>
<span data-ttu-id="d84dd-128">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d84dd-128">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_user"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/users/{user-id}
```
##### <a name="response"></a><span data-ttu-id="d84dd-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="d84dd-129">Response</span></span>
<span data-ttu-id="d84dd-130">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="d84dd-130">Here is an example of the response.</span></span> 
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
  "description": "Delete user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->