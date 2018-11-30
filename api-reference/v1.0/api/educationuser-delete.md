---
title: Eliminar educationUser
description: Elimine un usuario.
ms.openlocfilehash: d9e3cab7d34cdf418b3553d69881bb951217ae22
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029655"
---
# <a name="delete-educationuser"></a><span data-ttu-id="c4958-103">Eliminar educationUser</span><span class="sxs-lookup"><span data-stu-id="c4958-103">Delete educationUser</span></span>

<span data-ttu-id="c4958-104">Elimine un usuario.</span><span class="sxs-lookup"><span data-stu-id="c4958-104">Delete a user.</span></span>


## <a name="permissions"></a><span data-ttu-id="c4958-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="c4958-105">Permissions</span></span>
<span data-ttu-id="c4958-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c4958-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c4958-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c4958-108">Permission type</span></span>      | <span data-ttu-id="c4958-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c4958-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c4958-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c4958-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="c4958-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c4958-111">Not supported.</span></span>  |
|<span data-ttu-id="c4958-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c4958-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="c4958-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c4958-113">Not supported.</span></span>  |
|<span data-ttu-id="c4958-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c4958-114">Application</span></span> | <span data-ttu-id="c4958-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="c4958-115">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="c4958-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c4958-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="c4958-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c4958-117">Request headers</span></span>
| <span data-ttu-id="c4958-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c4958-118">Header</span></span>       | <span data-ttu-id="c4958-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c4958-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="c4958-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="c4958-120">Authorization</span></span>  | <span data-ttu-id="c4958-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c4958-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="c4958-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c4958-123">Request body</span></span>
<span data-ttu-id="c4958-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c4958-124">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="c4958-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4958-125">Response</span></span>
<span data-ttu-id="c4958-p103">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c4958-p103">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c4958-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c4958-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c4958-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c4958-129">Request</span></span>
<span data-ttu-id="c4958-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c4958-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationuser"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/users/{user-id}
```
##### <a name="response"></a><span data-ttu-id="c4958-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c4958-131">Response</span></span>
<span data-ttu-id="c4958-132">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c4958-132">The following is an example of the response.</span></span> 
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
  "description": "Delete educationUser",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->