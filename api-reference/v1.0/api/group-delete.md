---
title: Delete group
description: Elimina el grupo.
ms.openlocfilehash: c4a4f1cb370ec24a8b6bb0f5528e9983d47f206f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032002"
---
# <a name="delete-group"></a><span data-ttu-id="dc114-103">Delete group</span><span class="sxs-lookup"><span data-stu-id="dc114-103">Delete group</span></span>
<span data-ttu-id="dc114-104">Elimina el grupo.</span><span class="sxs-lookup"><span data-stu-id="dc114-104">Delete group.</span></span>

## <a name="permissions"></a><span data-ttu-id="dc114-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="dc114-105">Permissions</span></span>
<span data-ttu-id="dc114-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="dc114-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="dc114-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="dc114-108">Permission type</span></span>      | <span data-ttu-id="dc114-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="dc114-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="dc114-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="dc114-110">Delegated (work or school account)</span></span> | <span data-ttu-id="dc114-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dc114-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="dc114-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="dc114-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="dc114-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="dc114-113">Not supported.</span></span>    |
|<span data-ttu-id="dc114-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="dc114-114">Application</span></span> | <span data-ttu-id="dc114-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="dc114-115">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="dc114-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="dc114-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groups/{id}
```

## <a name="request-headers"></a><span data-ttu-id="dc114-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="dc114-117">Request headers</span></span>
| <span data-ttu-id="dc114-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="dc114-118">Name</span></span>       | <span data-ttu-id="dc114-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="dc114-119">Type</span></span> | <span data-ttu-id="dc114-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc114-120">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="dc114-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="dc114-121">Authorization</span></span>  | <span data-ttu-id="dc114-122">string</span><span class="sxs-lookup"><span data-stu-id="dc114-122">string</span></span>  | <span data-ttu-id="dc114-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="dc114-p102">Bearer {token}. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="dc114-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="dc114-125">Request body</span></span>
<span data-ttu-id="dc114-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="dc114-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="dc114-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc114-127">Response</span></span>
<span data-ttu-id="dc114-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc114-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="dc114-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="dc114-130">Example</span></span>
#### <a name="request"></a><span data-ttu-id="dc114-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="dc114-131">Request</span></span>
<span data-ttu-id="dc114-132">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="dc114-132">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_group"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groups/{id}
```

#### <a name="response"></a><span data-ttu-id="dc114-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="dc114-133">Response</span></span>
<span data-ttu-id="dc114-134">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="dc114-134">The following is an example of the response.</span></span> 
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
  "description": "Delete group",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->