---
title: Delete message
description: Eliminar un mensaje en el buzón del usuario especificado, o eliminar una relación del mensaje.
ms.openlocfilehash: 8f7429dfa4ee586f7bb6c263bdbb80971416d006
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090737"
---
# <a name="delete-message"></a><span data-ttu-id="62f54-103">Delete message</span><span class="sxs-lookup"><span data-stu-id="62f54-103">Delete message</span></span>

> <span data-ttu-id="62f54-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="62f54-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="62f54-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="62f54-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="62f54-106">Eliminar un mensaje en el buzón del usuario especificado, o eliminar una relación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="62f54-106">Delete a message in the specified user's mailbox, or delete a relationship of the message.</span></span>

<span data-ttu-id="62f54-107">Por ejemplo, puede eliminar [@ mención](../resources/mention.md) específica del usuario especificado en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="62f54-107">For example, you can delete a specific [@-mention](../resources/mention.md) of the specified user in the message.</span></span>

><span data-ttu-id="62f54-108">**Nota** Es posible que no pueda eliminar elementos de la carpeta de eliminaciones de elementos recuperables (representado por el [nombre de la carpeta Well-known](../resources/mailfolder.md) `recoverableitemsdeletions`).</span><span class="sxs-lookup"><span data-stu-id="62f54-108">**Note** You may not be able to delete items in the recoverable items deletions folder (represented by the [well-known folder name](../resources/mailfolder.md) `recoverableitemsdeletions`).</span></span> <span data-ttu-id="62f54-109">Para obtener más información, vea [retención de elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) y [Limpiar los elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) .</span><span class="sxs-lookup"><span data-stu-id="62f54-109">See [Deleted item retention](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) and [Clean up deleted items](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) for more information.</span></span>

## <a name="permissions"></a><span data-ttu-id="62f54-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="62f54-110">Permissions</span></span>
<span data-ttu-id="62f54-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="62f54-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="62f54-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="62f54-113">Permission type</span></span>      | <span data-ttu-id="62f54-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="62f54-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="62f54-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="62f54-115">Delegated (work or school account)</span></span> | <span data-ttu-id="62f54-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="62f54-116">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="62f54-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="62f54-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="62f54-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="62f54-118">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="62f54-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="62f54-119">Application</span></span> | <span data-ttu-id="62f54-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="62f54-120">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="62f54-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="62f54-121">HTTP request</span></span>

<span data-ttu-id="62f54-122">Para eliminar el mensaje especificado:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="62f54-122">To delete the specified message: <!-- { "blockType": "ignored" } --></span></span>
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}
DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```

<span data-ttu-id="62f54-123">Para eliminar un específico [mencione](../resources/mention.md) en un mensaje:<!-- { "blockType": "ignored" } --></span><span class="sxs-lookup"><span data-stu-id="62f54-123">To delete a specific [mention](../resources/mention.md) in a message: <!-- { "blockType": "ignored" } --></span></span>
```http
DELETE /me/messages/{id}/mentions/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}/mentions/{id}
DELETE /me/mailFolders/{id}/messages/{id}/mentions/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}/mentions/{id}
```

## <a name="request-headers"></a><span data-ttu-id="62f54-124">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="62f54-124">Request headers</span></span>
| <span data-ttu-id="62f54-125">Nombre</span><span class="sxs-lookup"><span data-stu-id="62f54-125">Name</span></span>       | <span data-ttu-id="62f54-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="62f54-126">Type</span></span> | <span data-ttu-id="62f54-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="62f54-127">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="62f54-128">Authorization</span><span class="sxs-lookup"><span data-stu-id="62f54-128">Authorization</span></span>  | <span data-ttu-id="62f54-129">string</span><span class="sxs-lookup"><span data-stu-id="62f54-129">string</span></span>  | <span data-ttu-id="62f54-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="62f54-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="62f54-132">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="62f54-132">Request body</span></span>
<span data-ttu-id="62f54-133">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="62f54-133">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="62f54-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="62f54-134">Response</span></span>

<span data-ttu-id="62f54-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62f54-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="62f54-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="62f54-137">Example</span></span>
##### <a name="request-1"></a><span data-ttu-id="62f54-138">Solicitud 1</span><span class="sxs-lookup"><span data-stu-id="62f54-138">Request 1</span></span>
<span data-ttu-id="62f54-139">El primer ejemplo elimina el mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="62f54-139">The first example deletes the specified message.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_message"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/messages/{id}
```
##### <a name="response-1"></a><span data-ttu-id="62f54-140">Respuesta 1</span><span class="sxs-lookup"><span data-stu-id="62f54-140">Response 1</span></span>
<span data-ttu-id="62f54-141">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62f54-141">Here is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 204 No Content
```

##### <a name="request-2"></a><span data-ttu-id="62f54-142">Solicitud 2</span><span class="sxs-lookup"><span data-stu-id="62f54-142">Request 2</span></span>
<span data-ttu-id="62f54-143">En el ejemplo siguiente se elimina un determinados **mencionar** en el mensaje especificado.</span><span class="sxs-lookup"><span data-stu-id="62f54-143">The next example deletes a certain **mention** in the specified message.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_mention_in_message"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/messages/{id}/mentions/{id}
```
##### <a name="response-2"></a><span data-ttu-id="62f54-144">Respuesta 2</span><span class="sxs-lookup"><span data-stu-id="62f54-144">Response 2</span></span>
<span data-ttu-id="62f54-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="62f54-145">Here is an example of the response.</span></span> 
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