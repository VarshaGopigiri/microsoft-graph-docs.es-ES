---
title: Eliminar groupLifecyclePolicy
description: Elimina un objeto groupLifecyclePolicy
ms.openlocfilehash: af154d2ff5e7b61a245f3b99d22f10d26f0204fc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032319"
---
# <a name="delete-grouplifecyclepolicy"></a><span data-ttu-id="c2368-103">Eliminar groupLifecyclePolicy</span><span class="sxs-lookup"><span data-stu-id="c2368-103">Delete groupLifecyclePolicy</span></span>

<span data-ttu-id="c2368-104">Elimina un objeto [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md)</span><span class="sxs-lookup"><span data-stu-id="c2368-104">Deletes a [groupLifecyclePolicy](../resources/grouplifecyclepolicy.md).</span></span>

## <a name="permissions"></a><span data-ttu-id="c2368-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c2368-105">Permissions</span></span>

<span data-ttu-id="c2368-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c2368-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c2368-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c2368-108">Permission type</span></span>      | <span data-ttu-id="c2368-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c2368-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c2368-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c2368-110">Delegated (work or school account)</span></span> | <span data-ttu-id="c2368-111">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c2368-111">Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="c2368-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c2368-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c2368-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c2368-113">Not supported.</span></span>    |
|<span data-ttu-id="c2368-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c2368-114">Application</span></span> | <span data-ttu-id="c2368-115">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c2368-115">Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c2368-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c2368-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /groupLifecyclePolicies/{id}

```

## <a name="request-headers"></a><span data-ttu-id="c2368-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c2368-117">Request headers</span></span>

| <span data-ttu-id="c2368-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="c2368-118">Name</span></span> | <span data-ttu-id="c2368-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2368-119">Description</span></span> |
|:---------------|:----------|
| <span data-ttu-id="c2368-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="c2368-120">Authorization</span></span> | <span data-ttu-id="c2368-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c2368-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c2368-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c2368-123">Content-Type</span></span>  | <span data-ttu-id="c2368-124">application/json</span><span class="sxs-lookup"><span data-stu-id="c2368-124">application/json</span></span> |

## <a name="request-body"></a><span data-ttu-id="c2368-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c2368-125">Request body</span></span>
<span data-ttu-id="c2368-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c2368-126">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="c2368-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2368-127">Response</span></span>

<span data-ttu-id="c2368-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c2368-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c2368-130">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c2368-130">Example</span></span>

##### <a name="request"></a><span data-ttu-id="c2368-131">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c2368-131">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "delete_grouplifecyclepolicy"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/groupLifecyclePolicies/{id}
```
##### <a name="response"></a><span data-ttu-id="c2368-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c2368-132">Response</span></span>

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
  "description": "Delete groupLifecyclePolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->