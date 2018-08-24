# <a name="delete-mailfolder"></a><span data-ttu-id="2284a-101">Eliminar mailFolder</span><span class="sxs-lookup"><span data-stu-id="2284a-101">Delete mailFolder</span></span>

<span data-ttu-id="2284a-102">Elimina el objeto [mailFolder](../resources/mailfolder.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="2284a-102">Delete the specified mailFolder object.</span></span>

<span data-ttu-id="2284a-103">Puede especificar una carpeta de correo por su identificador de carpeta o por su [nombre de carpeta conocido](../resources/mailfolder.md), si lo hay.</span><span class="sxs-lookup"><span data-stu-id="2284a-103">You can specify a mail folder by its folder ID, or by its [well-known folder name](../resources/mailfolder.md), if one exists.</span></span> 

><span data-ttu-id="2284a-104">**Nota** Es posible que no pueda eliminar elementos de la carpeta de eliminaciones de elementos recuperables (representado por el nombre de carpeta conocido `recoverableitemsdeletions`).</span><span class="sxs-lookup"><span data-stu-id="2284a-104">**Note** You may not be able to delete items in the recoverable items deletions folder (represented by the well-known folder name `recoverableitemsdeletions`).</span></span> <span data-ttu-id="2284a-105">Para obtener más información, vea [Retención de elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) y [Limpiar elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items).</span><span class="sxs-lookup"><span data-stu-id="2284a-105">See [Deleted item retention](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) and [Clean up deleted items](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) for more information.</span></span>

## <a name="permissions"></a><span data-ttu-id="2284a-106">Permisos</span><span class="sxs-lookup"><span data-stu-id="2284a-106">Permissions</span></span>
<span data-ttu-id="2284a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2284a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2284a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2284a-109">Permission type</span></span>      | <span data-ttu-id="2284a-110">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2284a-110">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2284a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2284a-111">Delegated (work or school account)</span></span> | <span data-ttu-id="2284a-112">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2284a-112">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="2284a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2284a-113">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2284a-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2284a-114">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="2284a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2284a-115">Application</span></span> | <span data-ttu-id="2284a-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2284a-116">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="2284a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2284a-117">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="2284a-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2284a-118">Request headers</span></span>
| <span data-ttu-id="2284a-119">Nombre</span><span class="sxs-lookup"><span data-stu-id="2284a-119">Name</span></span>       | <span data-ttu-id="2284a-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="2284a-120">Type</span></span> | <span data-ttu-id="2284a-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2284a-121">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="2284a-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="2284a-122">Authorization</span></span>  | <span data-ttu-id="2284a-123">cadena</span><span class="sxs-lookup"><span data-stu-id="2284a-123">string</span></span>  | <span data-ttu-id="2284a-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="2284a-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="2284a-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2284a-126">Request body</span></span>
<span data-ttu-id="2284a-127">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2284a-127">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2284a-128">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2284a-128">Response</span></span>

<span data-ttu-id="2284a-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2284a-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2284a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2284a-131">Example</span></span>
##### <a name="request"></a><span data-ttu-id="2284a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2284a-132">Request</span></span>
<span data-ttu-id="2284a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2284a-133">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_mailfolder"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/mailFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="2284a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2284a-134">Response</span></span>
<span data-ttu-id="2284a-135">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2284a-135">Here is an example of the response.</span></span> 
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