---
title: Eliminar educationUser
description: Elimine un usuario.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 9fc544734d00ba713d6cb3f92020dfbb68a3857e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860357"
---
# <a name="delete-educationuser"></a><span data-ttu-id="9b1d7-103">Eliminar educationUser</span><span class="sxs-lookup"><span data-stu-id="9b1d7-103">Delete educationUser</span></span>

<span data-ttu-id="9b1d7-104">Elimine un usuario.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-104">Delete a user.</span></span>


## <a name="permissions"></a><span data-ttu-id="9b1d7-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="9b1d7-105">Permissions</span></span>
<span data-ttu-id="9b1d7-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9b1d7-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9b1d7-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9b1d7-108">Permission type</span></span>      | <span data-ttu-id="9b1d7-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9b1d7-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="9b1d7-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-111">Not supported.</span></span>  |
|<span data-ttu-id="9b1d7-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9b1d7-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="9b1d7-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-113">Not supported.</span></span>  |
|<span data-ttu-id="9b1d7-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9b1d7-114">Application</span></span> | <span data-ttu-id="9b1d7-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9b1d7-115">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="9b1d7-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9b1d7-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="9b1d7-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9b1d7-117">Request headers</span></span>
| <span data-ttu-id="9b1d7-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9b1d7-118">Header</span></span>       | <span data-ttu-id="9b1d7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="9b1d7-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9b1d7-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="9b1d7-120">Authorization</span></span>  | <span data-ttu-id="9b1d7-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="9b1d7-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9b1d7-123">Request body</span></span>
<span data-ttu-id="9b1d7-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-124">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="9b1d7-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b1d7-125">Response</span></span>
<span data-ttu-id="9b1d7-p103">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-p103">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9b1d7-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9b1d7-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="9b1d7-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9b1d7-129">Request</span></span>
<span data-ttu-id="9b1d7-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationuser"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/users/{user-id}
```
##### <a name="response"></a><span data-ttu-id="9b1d7-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9b1d7-131">Response</span></span>
<span data-ttu-id="9b1d7-132">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9b1d7-132">The following is an example of the response.</span></span> 
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
