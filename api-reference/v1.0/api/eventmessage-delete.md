---
title: Delete eventMessage
description: Elimina el eventMessage.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 19eb4e70ffeee1cb69fa9607010c2e4b97c959ad
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943861"
---
# <a name="delete-eventmessage"></a><span data-ttu-id="87fa0-103">Delete eventMessage</span><span class="sxs-lookup"><span data-stu-id="87fa0-103">Delete eventMessage</span></span>

<span data-ttu-id="87fa0-104">Elimina el eventMessage.</span><span class="sxs-lookup"><span data-stu-id="87fa0-104">Delete eventMessage.</span></span>
## <a name="permissions"></a><span data-ttu-id="87fa0-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="87fa0-105">Permissions</span></span>
<span data-ttu-id="87fa0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="87fa0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="87fa0-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="87fa0-108">Permission type</span></span>      | <span data-ttu-id="87fa0-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="87fa0-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="87fa0-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="87fa0-110">Delegated (work or school account)</span></span> | <span data-ttu-id="87fa0-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="87fa0-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="87fa0-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="87fa0-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="87fa0-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="87fa0-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="87fa0-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="87fa0-114">Application</span></span> | <span data-ttu-id="87fa0-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="87fa0-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="87fa0-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="87fa0-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}

DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="87fa0-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="87fa0-117">Request headers</span></span>
| <span data-ttu-id="87fa0-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="87fa0-118">Name</span></span>       | <span data-ttu-id="87fa0-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="87fa0-119">Type</span></span> | <span data-ttu-id="87fa0-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="87fa0-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="87fa0-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="87fa0-121">Authorization</span></span>  | <span data-ttu-id="87fa0-122">string</span><span class="sxs-lookup"><span data-stu-id="87fa0-122">string</span></span>  | <span data-ttu-id="87fa0-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="87fa0-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="87fa0-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="87fa0-125">Request body</span></span>
<span data-ttu-id="87fa0-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="87fa0-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="87fa0-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="87fa0-127">Response</span></span>

<span data-ttu-id="87fa0-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="87fa0-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="87fa0-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="87fa0-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="87fa0-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="87fa0-131">Request</span></span>
<span data-ttu-id="87fa0-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="87fa0-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_eventmessage"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="87fa0-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="87fa0-133">Response</span></span>
<span data-ttu-id="87fa0-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="87fa0-134">Here is an example of the response.</span></span> 
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
