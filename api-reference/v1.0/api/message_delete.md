# <a name="delete-message"></a><span data-ttu-id="44a6d-101">Delete message</span><span class="sxs-lookup"><span data-stu-id="44a6d-101">Delete message</span></span>

<span data-ttu-id="44a6d-102">Elimina un mensaje.</span><span class="sxs-lookup"><span data-stu-id="44a6d-102">Delete message.</span></span>
## <a name="permissions"></a><span data-ttu-id="44a6d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="44a6d-103">Permissions</span></span>
<span data-ttu-id="44a6d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="44a6d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="44a6d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="44a6d-106">Permission type</span></span>      | <span data-ttu-id="44a6d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="44a6d-107">Permissions (from least to most privileged)</span></span>              | 
|:--------------------|:---------------------------------------------------------| 
|<span data-ttu-id="44a6d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="44a6d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="44a6d-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="44a6d-109">Mail.ReadWrite</span></span>    | 
|<span data-ttu-id="44a6d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="44a6d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="44a6d-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="44a6d-111">Mail.ReadWrite</span></span>    | 
|<span data-ttu-id="44a6d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="44a6d-112">Application</span></span> | <span data-ttu-id="44a6d-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="44a6d-113">Mail.ReadWrite</span></span> | 

## <a name="http-request"></a><span data-ttu-id="44a6d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="44a6d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}
DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="44a6d-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="44a6d-115">Request headers</span></span>
| <span data-ttu-id="44a6d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="44a6d-116">Name</span></span>       | <span data-ttu-id="44a6d-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="44a6d-117">Type</span></span> | <span data-ttu-id="44a6d-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="44a6d-118">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="44a6d-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="44a6d-119">Authorization</span></span>  | <span data-ttu-id="44a6d-120">string</span><span class="sxs-lookup"><span data-stu-id="44a6d-120">string</span></span>  | <span data-ttu-id="44a6d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="44a6d-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="44a6d-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="44a6d-123">Request body</span></span>
<span data-ttu-id="44a6d-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="44a6d-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="44a6d-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44a6d-125">Response</span></span>

<span data-ttu-id="44a6d-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204, No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="44a6d-p103">If successful, this method returns `204, No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="44a6d-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="44a6d-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="44a6d-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="44a6d-129">Request</span></span>
<span data-ttu-id="44a6d-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="44a6d-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_message"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="44a6d-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44a6d-131">Response</span></span>
<span data-ttu-id="44a6d-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="44a6d-132">Here is an example of the response.</span></span> 
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
  "description": "Delete message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->