---
title: Remove rejectedSender
description: Quita un usuario o grupo de la lista de rejectedSenders.
ms.openlocfilehash: f80697b2e9a02b761a1fb9959e0b18cd61a1a4c9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030539"
---
# <a name="remove-rejectedsender"></a><span data-ttu-id="e87f1-103">Remove rejectedSender</span><span class="sxs-lookup"><span data-stu-id="e87f1-103">Remove rejectedSender</span></span>
<span data-ttu-id="e87f1-104">Quita un usuario o grupo de la lista de rejectedSenders.</span><span class="sxs-lookup"><span data-stu-id="e87f1-104">Remove a user or group from the rejectedSenders list.</span></span>

## <a name="permissions"></a><span data-ttu-id="e87f1-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e87f1-105">Permissions</span></span>
<span data-ttu-id="e87f1-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e87f1-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="e87f1-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e87f1-108">Permission type</span></span>                        | <span data-ttu-id="e87f1-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e87f1-109">Permissions (from least to most privileged)</span></span>  |
|:---------------------------------------|:-------------------------------------------- |
| <span data-ttu-id="e87f1-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e87f1-110">Delegated (work or school account)</span></span>     | <span data-ttu-id="e87f1-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="e87f1-111">Group.ReadWrite.All</span></span> |
| <span data-ttu-id="e87f1-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e87f1-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e87f1-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e87f1-113">Not supported.</span></span> |
| <span data-ttu-id="e87f1-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e87f1-114">Application</span></span>                            | <span data-ttu-id="e87f1-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e87f1-115">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="e87f1-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e87f1-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/rejectedSenders/$ref?$id=https://graph.microsoft.com/v1.0/users/{user-id}
DELETE /groups/{id}/rejectedSenders/$ref?$id=https://graph.microsoft.com/v1.0/groups/{other-group-id}
```

## <a name="request-headers"></a><span data-ttu-id="e87f1-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e87f1-117">Request headers</span></span>

| <span data-ttu-id="e87f1-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e87f1-118">Header</span></span>         | <span data-ttu-id="e87f1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e87f1-119">Value</span></span>                      |
|:---------------|:---------------------------|
| <span data-ttu-id="e87f1-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="e87f1-120">Authorization</span></span>  | <span data-ttu-id="e87f1-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e87f1-p102">Bearer {token}. Required.</span></span> 

## <a name="request-body"></a><span data-ttu-id="e87f1-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e87f1-123">Request body</span></span>
<span data-ttu-id="e87f1-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e87f1-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e87f1-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e87f1-125">Response</span></span>
<span data-ttu-id="e87f1-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e87f1-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e87f1-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e87f1-128">Example</span></span>
#### <a name="request"></a><span data-ttu-id="e87f1-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e87f1-129">Request</span></span>
<span data-ttu-id="e87f1-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e87f1-130">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "remove_rejectedSender_from_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/rejectedSenders/$ref?$id=https://graph.microsoft.com/v1.0/users/{user-id}
```

#### <a name="response"></a><span data-ttu-id="e87f1-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e87f1-131">Response</span></span>
<span data-ttu-id="e87f1-132">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e87f1-132">The following is an example of the response.</span></span> 
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
  "description": "Remove rejectedSender",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->