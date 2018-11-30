---
title: Delete mailFolder
description: Eliminar el mailFolder especificado o mailSearchFolder.
ms.openlocfilehash: 4b1a79a871ebf03656fa33474480e7169943e035
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086769"
---
# <a name="delete-mailfolder"></a><span data-ttu-id="da9c4-103">Delete mailFolder</span><span class="sxs-lookup"><span data-stu-id="da9c4-103">Delete mailFolder</span></span>

> <span data-ttu-id="da9c4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="da9c4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="da9c4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="da9c4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="da9c4-106">Eliminar el especificado [mailFolder](../resources/mailfolder.md) o [mailSearchFolder](../resources/mailsearchfolder.md).</span><span class="sxs-lookup"><span data-stu-id="da9c4-106">Delete the specified [mailFolder](../resources/mailfolder.md) or [mailSearchFolder](../resources/mailsearchfolder.md).</span></span>

<span data-ttu-id="da9c4-107">Puede especificar una carpeta de correo por su identificador de carpeta o por su [nombre de la carpeta conocida](../resources/mailfolder.md), si lo hay.</span><span class="sxs-lookup"><span data-stu-id="da9c4-107">You can specify a mail folder by its folder ID, or by its [well-known folder name](../resources/mailfolder.md), if one exists.</span></span> 

><span data-ttu-id="da9c4-108">**Nota** Es posible que no pueda eliminar elementos de la carpeta de eliminaciones de elementos recuperables (representado por el nombre de carpeta Well-known `recoverableitemsdeletions`).</span><span class="sxs-lookup"><span data-stu-id="da9c4-108">**Note** You may not be able to delete items in the recoverable items deletions folder (represented by the well-known folder name `recoverableitemsdeletions`).</span></span> <span data-ttu-id="da9c4-109">Para obtener más información, vea [retención de elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) y [Limpiar los elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) .</span><span class="sxs-lookup"><span data-stu-id="da9c4-109">See [Deleted item retention](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) and [Clean up deleted items](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) for more information.</span></span>

## <a name="permissions"></a><span data-ttu-id="da9c4-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="da9c4-110">Permissions</span></span>
<span data-ttu-id="da9c4-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="da9c4-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="da9c4-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="da9c4-113">Permission type</span></span>      | <span data-ttu-id="da9c4-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="da9c4-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="da9c4-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="da9c4-115">Delegated (work or school account)</span></span> | <span data-ttu-id="da9c4-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da9c4-116">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="da9c4-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="da9c4-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="da9c4-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da9c4-118">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="da9c4-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="da9c4-119">Application</span></span> | <span data-ttu-id="da9c4-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="da9c4-120">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="da9c4-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="da9c4-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="da9c4-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="da9c4-122">Request headers</span></span>
| <span data-ttu-id="da9c4-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="da9c4-123">Name</span></span>       | <span data-ttu-id="da9c4-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="da9c4-124">Type</span></span> | <span data-ttu-id="da9c4-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="da9c4-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="da9c4-126">Authorization</span><span class="sxs-lookup"><span data-stu-id="da9c4-126">Authorization</span></span>  | <span data-ttu-id="da9c4-127">string</span><span class="sxs-lookup"><span data-stu-id="da9c4-127">string</span></span>  | <span data-ttu-id="da9c4-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="da9c4-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="da9c4-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="da9c4-130">Request body</span></span>
<span data-ttu-id="da9c4-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="da9c4-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="da9c4-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da9c4-132">Response</span></span>
<span data-ttu-id="da9c4-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da9c4-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="da9c4-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="da9c4-135">Example</span></span>
#### <a name="request"></a><span data-ttu-id="da9c4-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="da9c4-136">Request</span></span>
<span data-ttu-id="da9c4-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="da9c4-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_mailfolder"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/mailFolders/AAMkAGVmMDEzM/
```

#### <a name="response"></a><span data-ttu-id="da9c4-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da9c4-138">Response</span></span>
<span data-ttu-id="da9c4-139">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da9c4-139">The following is an example of the response.</span></span> 
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