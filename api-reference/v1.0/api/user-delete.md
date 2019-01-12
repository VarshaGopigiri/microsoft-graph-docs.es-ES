---
title: Eliminar un usuario
description: Elimina usuario.
author: dkershaw10
localization_priority: Priority
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 93097c1d2f3f88e3e1f6b4a0166883728b402ba4
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27987097"
---
# <a name="delete-a-user"></a><span data-ttu-id="b3884-103">Eliminar un usuario</span><span class="sxs-lookup"><span data-stu-id="b3884-103">Delete a user</span></span>

<span data-ttu-id="b3884-104">Elimina usuario.</span><span class="sxs-lookup"><span data-stu-id="b3884-104">Delete user.</span></span>
## <a name="permissions"></a><span data-ttu-id="b3884-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="b3884-105">Permissions</span></span>
<span data-ttu-id="b3884-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b3884-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b3884-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b3884-108">Permission type</span></span>      | <span data-ttu-id="b3884-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b3884-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="b3884-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b3884-110">Delegated (work or school account)</span></span> | <span data-ttu-id="b3884-111">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="b3884-111">Directory.AccessAsUser.All</span></span>    |
|<span data-ttu-id="b3884-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b3884-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="b3884-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3884-113">Not supported.</span></span>    |
|<span data-ttu-id="b3884-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b3884-114">Application</span></span> | <span data-ttu-id="b3884-115">User.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b3884-115">User.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="b3884-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b3884-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /users/{id | userPrincipalName}
```

## <a name="request-headers"></a><span data-ttu-id="b3884-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b3884-117">Request headers</span></span>
| <span data-ttu-id="b3884-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3884-118">Header</span></span>       | <span data-ttu-id="b3884-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b3884-119">Value</span></span>|
|:-----------|:------|
| <span data-ttu-id="b3884-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="b3884-120">Authorization</span></span>  | <span data-ttu-id="b3884-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="b3884-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="b3884-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b3884-123">Request body</span></span>
<span data-ttu-id="b3884-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b3884-124">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b3884-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3884-125">Response</span></span>

<span data-ttu-id="b3884-p103">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3884-p103">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b3884-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b3884-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="b3884-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b3884-129">Request</span></span>
<span data-ttu-id="b3884-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b3884-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_user"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/users/{user-id}
```
##### <a name="response"></a><span data-ttu-id="b3884-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3884-131">Response</span></span>
<span data-ttu-id="b3884-132">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3884-132">Here is an example of the response.</span></span> 
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
  "description": "Delete user",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
