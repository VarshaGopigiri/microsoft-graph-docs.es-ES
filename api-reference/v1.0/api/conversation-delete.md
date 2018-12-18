---
title: Eliminar conversation
description: Elimina la conversación.
author: dkershaw10
ms.openlocfilehash: 2d35472f611b6f49ba1683ba127444d91753fac7
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27335752"
---
# <a name="delete-conversation"></a><span data-ttu-id="73a9a-103">Eliminar conversation</span><span class="sxs-lookup"><span data-stu-id="73a9a-103">Delete conversation</span></span>

<span data-ttu-id="73a9a-104">Elimina la conversación.</span><span class="sxs-lookup"><span data-stu-id="73a9a-104">Delete conversation.</span></span>
## <a name="permissions"></a><span data-ttu-id="73a9a-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="73a9a-105">Permissions</span></span>
<span data-ttu-id="73a9a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="73a9a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="73a9a-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="73a9a-108">Permission type</span></span>      | <span data-ttu-id="73a9a-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="73a9a-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="73a9a-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="73a9a-110">Delegated (work or school account)</span></span> | <span data-ttu-id="73a9a-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="73a9a-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="73a9a-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="73a9a-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="73a9a-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73a9a-113">Not supported.</span></span>    |
|<span data-ttu-id="73a9a-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="73a9a-114">Application</span></span> | <span data-ttu-id="73a9a-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="73a9a-115">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="73a9a-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="73a9a-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}/conversations/{id}
```
## <a name="request-headers"></a><span data-ttu-id="73a9a-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="73a9a-117">Request headers</span></span>
| <span data-ttu-id="73a9a-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73a9a-118">Header</span></span>       | <span data-ttu-id="73a9a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="73a9a-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="73a9a-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="73a9a-120">Authorization</span></span>  | <span data-ttu-id="73a9a-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="73a9a-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="73a9a-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="73a9a-123">Request body</span></span>
<span data-ttu-id="73a9a-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="73a9a-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="73a9a-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73a9a-125">Response</span></span>

<span data-ttu-id="73a9a-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73a9a-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="73a9a-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="73a9a-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="73a9a-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="73a9a-129">Request</span></span>
<span data-ttu-id="73a9a-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="73a9a-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_conversation"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}/conversations/{id}
```
##### <a name="response"></a><span data-ttu-id="73a9a-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73a9a-131">Response</span></span>
<span data-ttu-id="73a9a-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73a9a-132">Here is an example of the response.</span></span> 
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
  "description": "Delete conversation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
