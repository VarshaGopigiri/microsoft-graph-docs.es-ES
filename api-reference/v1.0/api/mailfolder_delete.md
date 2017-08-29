# <a name="delete-mailfolder"></a><span data-ttu-id="f9211-101">Delete mailFolder</span><span class="sxs-lookup"><span data-stu-id="f9211-101">Delete mailFolder</span></span>

<span data-ttu-id="f9211-102">Elimina el objeto mailfolder.</span><span class="sxs-lookup"><span data-stu-id="f9211-102">Delete mailFolder.</span></span>
## <a name="permissions"></a><span data-ttu-id="f9211-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="f9211-103">Permissions</span></span>
<span data-ttu-id="f9211-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="f9211-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="f9211-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f9211-106">Permission type</span></span>      | <span data-ttu-id="f9211-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f9211-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="f9211-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f9211-108">Delegated (work or school account)</span></span> | <span data-ttu-id="f9211-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f9211-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="f9211-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f9211-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="f9211-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f9211-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="f9211-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f9211-112">Application</span></span> | <span data-ttu-id="f9211-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="f9211-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="f9211-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f9211-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="f9211-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f9211-115">Request headers</span></span>
| <span data-ttu-id="f9211-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="f9211-116">Name</span></span>       | <span data-ttu-id="f9211-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="f9211-117">Type</span></span> | <span data-ttu-id="f9211-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="f9211-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f9211-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="f9211-119">Authorization</span></span>  | <span data-ttu-id="f9211-120">string</span><span class="sxs-lookup"><span data-stu-id="f9211-120">string</span></span>  | <span data-ttu-id="f9211-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="f9211-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="f9211-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f9211-123">Request body</span></span>
<span data-ttu-id="f9211-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f9211-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f9211-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9211-125">Response</span></span>

<span data-ttu-id="f9211-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9211-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f9211-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f9211-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="f9211-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f9211-129">Request</span></span>
<span data-ttu-id="f9211-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f9211-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_mailfolder"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/mailFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="f9211-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f9211-131">Response</span></span>
<span data-ttu-id="f9211-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f9211-132">Here is an example of the response.</span></span> 
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
  "description": "Delete mailFolder",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->