---
title: Delete mailFolder
description: Eliminar el mailFolder especificado.
author: angelgolfer-ms
ms.openlocfilehash: ea2edfe07554ef0a5e1144dd1aeed00b7dd46155
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301102"
---
# <a name="delete-mailfolder"></a><span data-ttu-id="ac4d5-103">Delete mailFolder</span><span class="sxs-lookup"><span data-stu-id="ac4d5-103">Delete mailFolder</span></span>

<span data-ttu-id="ac4d5-104">Eliminar el especificado [mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="ac4d5-104">Delete the specified [mailFolder](../resources/mailfolder.md).</span></span>

<span data-ttu-id="ac4d5-105">Puede especificar una carpeta de correo por su identificador de carpeta o por su [nombre de la carpeta conocida](../resources/mailfolder.md), si lo hay.</span><span class="sxs-lookup"><span data-stu-id="ac4d5-105">You can specify a mail folder by its folder ID, or by its [well-known folder name](../resources/mailfolder.md), if one exists.</span></span> 

><span data-ttu-id="ac4d5-106">**Nota** Es posible que no pueda eliminar elementos de la carpeta de eliminaciones de elementos recuperables (representado por el nombre de carpeta Well-known `recoverableitemsdeletions`).</span><span class="sxs-lookup"><span data-stu-id="ac4d5-106">**Note** You may not be able to delete items in the recoverable items deletions folder (represented by the well-known folder name `recoverableitemsdeletions`).</span></span> <span data-ttu-id="ac4d5-107">Para obtener más información, vea [retención de elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) y [Limpiar los elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) .</span><span class="sxs-lookup"><span data-stu-id="ac4d5-107">See [Deleted item retention](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) and [Clean up deleted items](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) for more information.</span></span>

## <a name="permissions"></a><span data-ttu-id="ac4d5-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="ac4d5-108">Permissions</span></span>
<span data-ttu-id="ac4d5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ac4d5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ac4d5-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ac4d5-111">Permission type</span></span>      | <span data-ttu-id="ac4d5-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ac4d5-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ac4d5-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ac4d5-113">Delegated (work or school account)</span></span> | <span data-ttu-id="ac4d5-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ac4d5-114">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ac4d5-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ac4d5-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ac4d5-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ac4d5-116">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ac4d5-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ac4d5-117">Application</span></span> | <span data-ttu-id="ac4d5-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ac4d5-118">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ac4d5-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ac4d5-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="ac4d5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ac4d5-120">Request headers</span></span>
| <span data-ttu-id="ac4d5-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="ac4d5-121">Name</span></span>       | <span data-ttu-id="ac4d5-122">Type</span><span class="sxs-lookup"><span data-stu-id="ac4d5-122">Type</span></span> | <span data-ttu-id="ac4d5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="ac4d5-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ac4d5-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="ac4d5-124">Authorization</span></span>  | <span data-ttu-id="ac4d5-125">string</span><span class="sxs-lookup"><span data-stu-id="ac4d5-125">string</span></span>  | <span data-ttu-id="ac4d5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ac4d5-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="ac4d5-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ac4d5-128">Request body</span></span>
<span data-ttu-id="ac4d5-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ac4d5-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ac4d5-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac4d5-130">Response</span></span>

<span data-ttu-id="ac4d5-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac4d5-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ac4d5-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac4d5-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ac4d5-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ac4d5-134">Request</span></span>
<span data-ttu-id="ac4d5-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ac4d5-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_mailfolder"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/mailFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="ac4d5-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ac4d5-136">Response</span></span>
<span data-ttu-id="ac4d5-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ac4d5-137">Here is an example of the response.</span></span> 
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