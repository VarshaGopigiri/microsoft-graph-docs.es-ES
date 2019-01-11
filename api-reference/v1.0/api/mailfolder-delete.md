---
title: Delete mailFolder
description: Eliminar el mailFolder especificado.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 829a419164c2e4856881a7d6215d6881a53a35f4
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27852965"
---
# <a name="delete-mailfolder"></a><span data-ttu-id="a7ff3-103">Delete mailFolder</span><span class="sxs-lookup"><span data-stu-id="a7ff3-103">Delete mailFolder</span></span>

<span data-ttu-id="a7ff3-104">Eliminar el especificado [mailFolder](../resources/mailfolder.md).</span><span class="sxs-lookup"><span data-stu-id="a7ff3-104">Delete the specified [mailFolder](../resources/mailfolder.md).</span></span>

<span data-ttu-id="a7ff3-105">Puede especificar una carpeta de correo por su identificador de carpeta o por su [nombre de la carpeta conocida](../resources/mailfolder.md), si lo hay.</span><span class="sxs-lookup"><span data-stu-id="a7ff3-105">You can specify a mail folder by its folder ID, or by its [well-known folder name](../resources/mailfolder.md), if one exists.</span></span> 

><span data-ttu-id="a7ff3-106">**Nota** Es posible que no pueda eliminar elementos de la carpeta de eliminaciones de elementos recuperables (representado por el nombre de carpeta Well-known `recoverableitemsdeletions`).</span><span class="sxs-lookup"><span data-stu-id="a7ff3-106">**Note** You may not be able to delete items in the recoverable items deletions folder (represented by the well-known folder name `recoverableitemsdeletions`).</span></span> <span data-ttu-id="a7ff3-107">Para obtener más información, vea [retención de elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) y [Limpiar los elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) .</span><span class="sxs-lookup"><span data-stu-id="a7ff3-107">See [Deleted item retention](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) and [Clean up deleted items](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) for more information.</span></span>

## <a name="permissions"></a><span data-ttu-id="a7ff3-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="a7ff3-108">Permissions</span></span>
<span data-ttu-id="a7ff3-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a7ff3-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a7ff3-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a7ff3-111">Permission type</span></span>      | <span data-ttu-id="a7ff3-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a7ff3-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a7ff3-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a7ff3-113">Delegated (work or school account)</span></span> | <span data-ttu-id="a7ff3-114">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a7ff3-114">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="a7ff3-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a7ff3-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a7ff3-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a7ff3-116">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="a7ff3-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a7ff3-117">Application</span></span> | <span data-ttu-id="a7ff3-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="a7ff3-118">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="a7ff3-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a7ff3-119">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="a7ff3-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a7ff3-120">Request headers</span></span>
| <span data-ttu-id="a7ff3-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="a7ff3-121">Name</span></span>       | <span data-ttu-id="a7ff3-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="a7ff3-122">Type</span></span> | <span data-ttu-id="a7ff3-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="a7ff3-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="a7ff3-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="a7ff3-124">Authorization</span></span>  | <span data-ttu-id="a7ff3-125">string</span><span class="sxs-lookup"><span data-stu-id="a7ff3-125">string</span></span>  | <span data-ttu-id="a7ff3-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a7ff3-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="a7ff3-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a7ff3-128">Request body</span></span>
<span data-ttu-id="a7ff3-129">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a7ff3-129">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a7ff3-130">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7ff3-130">Response</span></span>

<span data-ttu-id="a7ff3-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7ff3-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a7ff3-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a7ff3-133">Example</span></span>
##### <a name="request"></a><span data-ttu-id="a7ff3-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a7ff3-134">Request</span></span>
<span data-ttu-id="a7ff3-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a7ff3-135">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_mailfolder"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/mailFolders/{id}
```
##### <a name="response"></a><span data-ttu-id="a7ff3-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a7ff3-136">Response</span></span>
<span data-ttu-id="a7ff3-137">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a7ff3-137">Here is an example of the response.</span></span> 
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
