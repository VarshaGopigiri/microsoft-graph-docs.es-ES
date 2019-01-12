---
title: Eliminar educationUser
description: Elimine un usuario.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: be2839a866474acbdd196c3b43503a5b69252c26
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932339"
---
# <a name="delete-educationuser"></a><span data-ttu-id="4a300-103">Eliminar educationUser</span><span class="sxs-lookup"><span data-stu-id="4a300-103">Delete educationUser</span></span>

<span data-ttu-id="4a300-104">Elimine un usuario.</span><span class="sxs-lookup"><span data-stu-id="4a300-104">Delete a user.</span></span>


## <a name="permissions"></a><span data-ttu-id="4a300-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="4a300-105">Permissions</span></span>
<span data-ttu-id="4a300-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4a300-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4a300-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4a300-108">Permission type</span></span>      | <span data-ttu-id="4a300-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4a300-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4a300-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4a300-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="4a300-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4a300-111">Not supported.</span></span>  |
|<span data-ttu-id="4a300-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4a300-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="4a300-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4a300-113">Not supported.</span></span>  |
|<span data-ttu-id="4a300-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4a300-114">Application</span></span> | <span data-ttu-id="4a300-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4a300-115">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4a300-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4a300-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="4a300-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4a300-117">Request headers</span></span>
| <span data-ttu-id="4a300-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4a300-118">Header</span></span>       | <span data-ttu-id="4a300-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4a300-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="4a300-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="4a300-120">Authorization</span></span>  | <span data-ttu-id="4a300-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="4a300-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="4a300-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4a300-123">Request body</span></span>
<span data-ttu-id="4a300-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="4a300-124">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="4a300-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a300-125">Response</span></span>
<span data-ttu-id="4a300-p103">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a300-p103">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4a300-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4a300-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="4a300-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4a300-129">Request</span></span>
<span data-ttu-id="4a300-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4a300-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationuser"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/users/{user-id}
```
##### <a name="response"></a><span data-ttu-id="4a300-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4a300-131">Response</span></span>
<span data-ttu-id="4a300-132">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4a300-132">The following is an example of the response.</span></span> 
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
