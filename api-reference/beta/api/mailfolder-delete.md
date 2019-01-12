---
title: Delete mailFolder
description: Eliminar el mailFolder especificado o mailSearchFolder.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 6753eaac9e02e5b6c5ff92402f13484dc458b558
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923869"
---
# <a name="delete-mailfolder"></a><span data-ttu-id="33f14-103">Delete mailFolder</span><span class="sxs-lookup"><span data-stu-id="33f14-103">Delete mailFolder</span></span>

> <span data-ttu-id="33f14-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="33f14-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="33f14-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="33f14-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="33f14-106">Eliminar el especificado [mailFolder](../resources/mailfolder.md) o [mailSearchFolder](../resources/mailsearchfolder.md).</span><span class="sxs-lookup"><span data-stu-id="33f14-106">Delete the specified [mailFolder](../resources/mailfolder.md) or [mailSearchFolder](../resources/mailsearchfolder.md).</span></span>

<span data-ttu-id="33f14-107">Puede especificar una carpeta de correo por su identificador de carpeta o por su [nombre de la carpeta conocida](../resources/mailfolder.md), si lo hay.</span><span class="sxs-lookup"><span data-stu-id="33f14-107">You can specify a mail folder by its folder ID, or by its [well-known folder name](../resources/mailfolder.md), if one exists.</span></span> 

><span data-ttu-id="33f14-108">**Nota** Es posible que no pueda eliminar elementos de la carpeta de eliminaciones de elementos recuperables (representado por el nombre de carpeta Well-known `recoverableitemsdeletions`).</span><span class="sxs-lookup"><span data-stu-id="33f14-108">**Note** You may not be able to delete items in the recoverable items deletions folder (represented by the well-known folder name `recoverableitemsdeletions`).</span></span> <span data-ttu-id="33f14-109">Para obtener más información, vea [retención de elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) y [Limpiar los elementos eliminados](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) .</span><span class="sxs-lookup"><span data-stu-id="33f14-109">See [Deleted item retention](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/recoverable-items-folder#deleted-item-retention) and [Clean up deleted items](https://docs.microsoft.com/en-us/exchange/policy-and-compliance/recoverable-items-folder/clean-up-deleted-items) for more information.</span></span>

## <a name="permissions"></a><span data-ttu-id="33f14-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="33f14-110">Permissions</span></span>
<span data-ttu-id="33f14-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="33f14-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="33f14-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="33f14-113">Permission type</span></span>      | <span data-ttu-id="33f14-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="33f14-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="33f14-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="33f14-115">Delegated (work or school account)</span></span> | <span data-ttu-id="33f14-116">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="33f14-116">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="33f14-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="33f14-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="33f14-118">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="33f14-118">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="33f14-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="33f14-119">Application</span></span> | <span data-ttu-id="33f14-120">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="33f14-120">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="33f14-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="33f14-121">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/mailFolders/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}
```
## <a name="request-headers"></a><span data-ttu-id="33f14-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="33f14-122">Request headers</span></span>
| <span data-ttu-id="33f14-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="33f14-123">Name</span></span>       | <span data-ttu-id="33f14-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="33f14-124">Type</span></span> | <span data-ttu-id="33f14-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="33f14-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="33f14-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="33f14-126">Authorization</span></span>  | <span data-ttu-id="33f14-127">string</span><span class="sxs-lookup"><span data-stu-id="33f14-127">string</span></span>  | <span data-ttu-id="33f14-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="33f14-p104">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="33f14-130">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="33f14-130">Request body</span></span>
<span data-ttu-id="33f14-131">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="33f14-131">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="33f14-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33f14-132">Response</span></span>
<span data-ttu-id="33f14-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="33f14-p105">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="33f14-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="33f14-135">Example</span></span>
#### <a name="request"></a><span data-ttu-id="33f14-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="33f14-136">Request</span></span>
<span data-ttu-id="33f14-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="33f14-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_mailfolder"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/mailFolders/AAMkAGVmMDEzM/
```

#### <a name="response"></a><span data-ttu-id="33f14-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="33f14-138">Response</span></span>
<span data-ttu-id="33f14-139">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="33f14-139">The following is an example of the response.</span></span> 
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
