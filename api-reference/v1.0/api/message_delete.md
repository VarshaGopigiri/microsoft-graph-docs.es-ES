# <a name="delete-message"></a><span data-ttu-id="e83df-101">Borrar mensaje</span><span class="sxs-lookup"><span data-stu-id="e83df-101">Delete message</span></span>

<span data-ttu-id="e83df-102">Eliminar un mensaje en el buzón del usuario especificado, o eliminar una relación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e83df-102">Delete a message in the specified user's mailbox, or delete a relationship of the message.</span></span>

><span data-ttu-id="e83df-103">**Nota** Es posible que no pueda eliminar elementos de la carpeta de eliminaciones de elementos recuperables (representado por el [nombre de carpeta conocido](../resources/mailfolder.md) `recoverableitemsdeletions`).</span><span class="sxs-lookup"><span data-stu-id="e83df-103">**Note** You may not be able to delete items in the recoverable items deletions folder (represented by the [well-known folder name](../resources/mailfolder.md) `recoverableitemsdeletions`).</span></span> <span data-ttu-id="e83df-104">Para obtener más información, vea [Retención de elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) y [Limpiar elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) .</span><span class="sxs-lookup"><span data-stu-id="e83df-104">See [Deleted item retention](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) and [Clean up deleted items](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) for more information.</span></span>

## <a name="permissions"></a><span data-ttu-id="e83df-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e83df-105">Permissions</span></span>
<span data-ttu-id="e83df-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="e83df-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="e83df-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e83df-108">Permission type</span></span>      | <span data-ttu-id="e83df-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e83df-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e83df-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e83df-110">Delegated (work or school account)</span></span> | <span data-ttu-id="e83df-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e83df-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="e83df-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e83df-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e83df-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e83df-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="e83df-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e83df-114">Application</span></span> | <span data-ttu-id="e83df-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e83df-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="e83df-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e83df-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}
DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="e83df-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e83df-117">Request headers</span></span>
| <span data-ttu-id="e83df-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="e83df-118">Name</span></span>       | <span data-ttu-id="e83df-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="e83df-119">Type</span></span> | <span data-ttu-id="e83df-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e83df-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="e83df-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e83df-121">Authorization</span></span>  | <span data-ttu-id="e83df-122">cadena</span><span class="sxs-lookup"><span data-stu-id="e83df-122">string</span></span>  | <span data-ttu-id="e83df-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e83df-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="e83df-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e83df-125">Request body</span></span>
<span data-ttu-id="e83df-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e83df-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e83df-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e83df-127">Response</span></span>

<span data-ttu-id="e83df-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e83df-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e83df-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e83df-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e83df-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e83df-131">Request</span></span>
<span data-ttu-id="e83df-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e83df-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_message"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="e83df-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e83df-133">Response</span></span>
<span data-ttu-id="e83df-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e83df-134">Here is an example of the response.</span></span> 
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