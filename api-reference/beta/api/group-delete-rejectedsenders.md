---
title: Remove rejectedSender
description: Quita un usuario o grupo de la lista de rejectedSenders.
author: dkershaw10
ms.openlocfilehash: cd84f14f15288207ff8c3362ea0295ae3eba1856
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27311259"
---
# <a name="remove-rejectedsender"></a><span data-ttu-id="ca5ad-103">Remove rejectedSender</span><span class="sxs-lookup"><span data-stu-id="ca5ad-103">Remove rejectedSender</span></span>

> <span data-ttu-id="ca5ad-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ca5ad-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ca5ad-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ca5ad-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ca5ad-106">Quita un usuario o grupo de la lista de rejectedSenders.</span><span class="sxs-lookup"><span data-stu-id="ca5ad-106">Remove a user or group from the rejectedSenders list.</span></span>

## <a name="permissions"></a><span data-ttu-id="ca5ad-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ca5ad-107">Permissions</span></span>
<span data-ttu-id="ca5ad-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ca5ad-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

| <span data-ttu-id="ca5ad-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ca5ad-110">Permission type</span></span>                        | <span data-ttu-id="ca5ad-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ca5ad-111">Permissions (from least to most privileged)</span></span>  |
|:---------------------------------------|:-------------------------------------------- |
| <span data-ttu-id="ca5ad-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ca5ad-112">Delegated (work or school account)</span></span>     | <span data-ttu-id="ca5ad-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ca5ad-113">Group.ReadWrite.All</span></span>  |  
| <span data-ttu-id="ca5ad-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ca5ad-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ca5ad-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ca5ad-115">Not supported.</span></span> |
| <span data-ttu-id="ca5ad-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ca5ad-116">Application</span></span>                            | <span data-ttu-id="ca5ad-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ca5ad-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="ca5ad-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ca5ad-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/rejectedSenders/$ref?$id=<id>
```

## <a name="request-headers"></a><span data-ttu-id="ca5ad-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ca5ad-119">Request headers</span></span>

| <span data-ttu-id="ca5ad-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ca5ad-120">Header</span></span>         | <span data-ttu-id="ca5ad-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ca5ad-121">Value</span></span>                      |
|:---------------|:---------------------------|
| <span data-ttu-id="ca5ad-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="ca5ad-122">Authorization</span></span>  | <span data-ttu-id="ca5ad-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ca5ad-p103">Bearer {token}. Required.</span></span>  

## <a name="request-body"></a><span data-ttu-id="ca5ad-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ca5ad-125">Request body</span></span>
<span data-ttu-id="ca5ad-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ca5ad-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ca5ad-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca5ad-127">Response</span></span>
<span data-ttu-id="ca5ad-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca5ad-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ca5ad-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ca5ad-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="ca5ad-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ca5ad-131">Request</span></span>
<span data-ttu-id="ca5ad-132">Estos son un par de ejemplos de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ca5ad-132">The following are a couple of examples of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "remove_rejectedSender_from_group"
}-->
```http
DELETE https://graph.microsoft.com/beta/groups/{id}/rejectedSenders/$ref?$id=https://graph.microsoft.com/beta/users/{id}

DELETE https://graph.microsoft.com/beta/groups/{id}/rejectedSenders/$ref?$id=https://graph.microsoft.com/beta/groups/{id}
```

#### <a name="response"></a><span data-ttu-id="ca5ad-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ca5ad-133">Response</span></span>
<span data-ttu-id="ca5ad-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ca5ad-134">The following is an example of the response.</span></span> 
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