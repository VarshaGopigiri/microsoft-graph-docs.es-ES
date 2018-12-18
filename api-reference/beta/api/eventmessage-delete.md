---
title: Delete eventMessage
description: Elimina el eventMessage.
author: angelgolfer-ms
ms.openlocfilehash: 68d9397f1fc595e864d94b87bdb67d766731411a
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27350221"
---
# <a name="delete-eventmessage"></a><span data-ttu-id="4d0cc-103">Delete eventMessage</span><span class="sxs-lookup"><span data-stu-id="4d0cc-103">Delete eventMessage</span></span>

> <span data-ttu-id="4d0cc-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4d0cc-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4d0cc-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4d0cc-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4d0cc-106">Elimina el eventMessage.</span><span class="sxs-lookup"><span data-stu-id="4d0cc-106">Delete eventMessage.</span></span>
## <a name="permissions"></a><span data-ttu-id="4d0cc-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4d0cc-107">Permissions</span></span>
<span data-ttu-id="4d0cc-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4d0cc-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4d0cc-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4d0cc-110">Permission type</span></span>      | <span data-ttu-id="4d0cc-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4d0cc-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4d0cc-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4d0cc-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4d0cc-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4d0cc-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="4d0cc-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4d0cc-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4d0cc-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4d0cc-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="4d0cc-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4d0cc-116">Application</span></span> | <span data-ttu-id="4d0cc-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4d0cc-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="4d0cc-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4d0cc-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}

DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="4d0cc-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4d0cc-119">Request headers</span></span>
| <span data-ttu-id="4d0cc-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="4d0cc-120">Name</span></span>       | <span data-ttu-id="4d0cc-121">Type</span><span class="sxs-lookup"><span data-stu-id="4d0cc-121">Type</span></span> | <span data-ttu-id="4d0cc-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d0cc-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="4d0cc-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="4d0cc-123">Authorization</span></span>  | <span data-ttu-id="4d0cc-124">string</span><span class="sxs-lookup"><span data-stu-id="4d0cc-124">string</span></span>  | <span data-ttu-id="4d0cc-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4d0cc-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="4d0cc-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4d0cc-127">Request body</span></span>
<span data-ttu-id="4d0cc-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4d0cc-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="4d0cc-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d0cc-129">Response</span></span>

<span data-ttu-id="4d0cc-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d0cc-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4d0cc-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4d0cc-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4d0cc-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4d0cc-133">Request</span></span>
<span data-ttu-id="4d0cc-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4d0cc-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_eventmessage"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="4d0cc-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4d0cc-135">Response</span></span>
<span data-ttu-id="4d0cc-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4d0cc-136">Here is an example of the response.</span></span> 
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
  "description": "Delete eventMessage",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->