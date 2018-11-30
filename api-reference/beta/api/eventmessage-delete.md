---
title: Delete eventMessage
description: Elimina el eventMessage.
ms.openlocfilehash: d095fd80b7fed7739c05dafdac4f99ff035c48de
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084976"
---
# <a name="delete-eventmessage"></a><span data-ttu-id="35dc9-103">Delete eventMessage</span><span class="sxs-lookup"><span data-stu-id="35dc9-103">Delete eventMessage</span></span>

> <span data-ttu-id="35dc9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="35dc9-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="35dc9-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="35dc9-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="35dc9-106">Elimina el eventMessage.</span><span class="sxs-lookup"><span data-stu-id="35dc9-106">Delete eventMessage.</span></span>
## <a name="permissions"></a><span data-ttu-id="35dc9-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="35dc9-107">Permissions</span></span>
<span data-ttu-id="35dc9-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="35dc9-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="35dc9-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="35dc9-110">Permission type</span></span>      | <span data-ttu-id="35dc9-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="35dc9-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="35dc9-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="35dc9-112">Delegated (work or school account)</span></span> | <span data-ttu-id="35dc9-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="35dc9-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="35dc9-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="35dc9-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="35dc9-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="35dc9-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="35dc9-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="35dc9-116">Application</span></span> | <span data-ttu-id="35dc9-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="35dc9-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="35dc9-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="35dc9-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /me/messages/{id}
DELETE /users/{id | userPrincipalName}/messages/{id}

DELETE /me/mailFolders/{id}/messages/{id}
DELETE /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="35dc9-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="35dc9-119">Request headers</span></span>
| <span data-ttu-id="35dc9-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="35dc9-120">Name</span></span>       | <span data-ttu-id="35dc9-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="35dc9-121">Type</span></span> | <span data-ttu-id="35dc9-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="35dc9-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="35dc9-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="35dc9-123">Authorization</span></span>  | <span data-ttu-id="35dc9-124">string</span><span class="sxs-lookup"><span data-stu-id="35dc9-124">string</span></span>  | <span data-ttu-id="35dc9-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="35dc9-p103">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="35dc9-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="35dc9-127">Request body</span></span>
<span data-ttu-id="35dc9-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="35dc9-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="35dc9-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35dc9-129">Response</span></span>

<span data-ttu-id="35dc9-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35dc9-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="35dc9-132">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="35dc9-132">Example</span></span>
##### <a name="request"></a><span data-ttu-id="35dc9-133">Solicitud</span><span class="sxs-lookup"><span data-stu-id="35dc9-133">Request</span></span>
<span data-ttu-id="35dc9-134">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="35dc9-134">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_eventmessage"
}-->
```http
DELETE https://graph.microsoft.com/beta/me/messages/{id}
```
##### <a name="response"></a><span data-ttu-id="35dc9-135">Respuesta</span><span class="sxs-lookup"><span data-stu-id="35dc9-135">Response</span></span>
<span data-ttu-id="35dc9-136">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="35dc9-136">Here is an example of the response.</span></span> 
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