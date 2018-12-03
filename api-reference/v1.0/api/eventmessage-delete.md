---
title: Delete eventMessage
description: Elimina el eventMessage.
ms.openlocfilehash: 14b693d44f64e43aa7357d23fe079e381c78c87a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029930"
---
# <a name="delete-eventmessage"></a><span data-ttu-id="b8804-103">Delete eventMessage</span><span class="sxs-lookup"><span data-stu-id="b8804-103">Delete eventMessage</span></span>

<span data-ttu-id="b8804-104">Elimina el eventMessage.</span><span class="sxs-lookup"><span data-stu-id="b8804-104">Delete eventMessage.</span></span>
## <a name="permissions"></a><span data-ttu-id="b8804-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b8804-105">Permissions</span></span>
<span data-ttu-id="b8804-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b8804-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b8804-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b8804-108">Permission type</span></span>      | <span data-ttu-id="b8804-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b8804-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b8804-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b8804-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b8804-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b8804-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="b8804-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b8804-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b8804-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b8804-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="b8804-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b8804-114">Application</span></span> | <span data-ttu-id="b8804-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b8804-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="b8804-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b8804-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}

DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="b8804-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b8804-117">Request headers</span></span>
| <span data-ttu-id="b8804-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="b8804-118">Name</span></span>       | <span data-ttu-id="b8804-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="b8804-119">Type</span></span> | <span data-ttu-id="b8804-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="b8804-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="b8804-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="b8804-121">Authorization</span></span>  | <span data-ttu-id="b8804-122">string</span><span class="sxs-lookup"><span data-stu-id="b8804-122">string</span></span>  | <span data-ttu-id="b8804-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b8804-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="b8804-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b8804-125">Request body</span></span>
<span data-ttu-id="b8804-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b8804-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b8804-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8804-127">Response</span></span>

<span data-ttu-id="b8804-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8804-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b8804-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b8804-130">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b8804-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b8804-131">Request</span></span>
<span data-ttu-id="b8804-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b8804-132">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_eventmessage"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="b8804-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b8804-133">Response</span></span>
<span data-ttu-id="b8804-134">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b8804-134">Here is an example of the response.</span></span> 
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