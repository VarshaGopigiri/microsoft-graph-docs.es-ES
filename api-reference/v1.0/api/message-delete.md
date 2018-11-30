---
title: Delete message
description: Eliminar un mensaje en el buzón del usuario especificado, o eliminar una relación del mensaje.
ms.openlocfilehash: 5bfcb57f3f9c82f79147c30c982f59172e48b51f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031689"
---
# <a name="delete-message"></a><span data-ttu-id="274ad-103">Delete message</span><span class="sxs-lookup"><span data-stu-id="274ad-103">Delete message</span></span>

<span data-ttu-id="274ad-104">Eliminar un mensaje en el buzón del usuario especificado, o eliminar una relación del mensaje.</span><span class="sxs-lookup"><span data-stu-id="274ad-104">Delete a message in the specified user's mailbox, or delete a relationship of the message.</span></span>

><span data-ttu-id="274ad-105">**Nota** Es posible que no pueda eliminar elementos de la carpeta de eliminaciones de elementos recuperables (representado por el [nombre de la carpeta Well-known](../resources/mailfolder.md) `recoverableitemsdeletions`).</span><span class="sxs-lookup"><span data-stu-id="274ad-105">**Note** You may not be able to delete items in the recoverable items deletions folder (represented by the [well-known folder name](../resources/mailfolder.md) `recoverableitemsdeletions`).</span></span> <span data-ttu-id="274ad-106">Para obtener más información, vea [retención de elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) y [Limpiar los elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) .</span><span class="sxs-lookup"><span data-stu-id="274ad-106">See [Deleted item retention](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) and [Clean up deleted items](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) for more information.</span></span>

## <a name="permissions"></a><span data-ttu-id="274ad-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="274ad-107">Permissions</span></span>
<span data-ttu-id="274ad-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="274ad-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="274ad-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="274ad-110">Permission type</span></span>      | <span data-ttu-id="274ad-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="274ad-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="274ad-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="274ad-112">Delegated (work or school account)</span></span> | <span data-ttu-id="274ad-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="274ad-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="274ad-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="274ad-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="274ad-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="274ad-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="274ad-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="274ad-116">Application</span></span> | <span data-ttu-id="274ad-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="274ad-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="274ad-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="274ad-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}
DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="274ad-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="274ad-119">Request headers</span></span>
| <span data-ttu-id="274ad-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="274ad-120">Name</span></span>       | <span data-ttu-id="274ad-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="274ad-121">Type</span></span> | <span data-ttu-id="274ad-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="274ad-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="274ad-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="274ad-123">Authorization</span></span>  | <span data-ttu-id="274ad-124">string</span><span class="sxs-lookup"><span data-stu-id="274ad-124">string</span></span>  | <span data-ttu-id="274ad-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="274ad-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="274ad-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="274ad-127">Request body</span></span>
<span data-ttu-id="274ad-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="274ad-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="274ad-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="274ad-129">Response</span></span>

<span data-ttu-id="274ad-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="274ad-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="274ad-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="274ad-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="274ad-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="274ad-133">Request</span></span>
<span data-ttu-id="274ad-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="274ad-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_message"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="274ad-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="274ad-135">Response</span></span>
<span data-ttu-id="274ad-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="274ad-136">Here is an example of the response.</span></span> 
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