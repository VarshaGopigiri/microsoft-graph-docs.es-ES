---
title: Eliminar educationUser
description: Elimine un usuario.
author: mmast-msft
ms.openlocfilehash: 445bfb84a67dfe598ac2de696b49d07db447e0e0
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27328542"
---
# <a name="delete-educationuser"></a><span data-ttu-id="01bdc-103">Eliminar educationUser</span><span class="sxs-lookup"><span data-stu-id="01bdc-103">Delete educationUser</span></span>

<span data-ttu-id="01bdc-104">Elimine un usuario.</span><span class="sxs-lookup"><span data-stu-id="01bdc-104">Delete a user.</span></span>


## <a name="permissions"></a><span data-ttu-id="01bdc-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="01bdc-105">Permissions</span></span>
<span data-ttu-id="01bdc-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="01bdc-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="01bdc-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="01bdc-108">Permission type</span></span>      | <span data-ttu-id="01bdc-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="01bdc-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="01bdc-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="01bdc-110">Delegated (work or school account)</span></span> |  <span data-ttu-id="01bdc-111">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01bdc-111">Not supported.</span></span>  |
|<span data-ttu-id="01bdc-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="01bdc-112">Delegated (personal Microsoft account)</span></span> |  <span data-ttu-id="01bdc-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="01bdc-113">Not supported.</span></span>  |
|<span data-ttu-id="01bdc-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="01bdc-114">Application</span></span> | <span data-ttu-id="01bdc-115">EduRoster.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="01bdc-115">EduRoster.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="01bdc-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="01bdc-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
DELETE /education/users/{id}
```
## <a name="request-headers"></a><span data-ttu-id="01bdc-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="01bdc-117">Request headers</span></span>
| <span data-ttu-id="01bdc-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="01bdc-118">Header</span></span>       | <span data-ttu-id="01bdc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="01bdc-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="01bdc-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="01bdc-120">Authorization</span></span>  | <span data-ttu-id="01bdc-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="01bdc-p102">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="01bdc-123">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="01bdc-123">Request body</span></span>
<span data-ttu-id="01bdc-124">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="01bdc-124">Do not supply a request body for this method.</span></span>


## <a name="response"></a><span data-ttu-id="01bdc-125">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01bdc-125">Response</span></span>
<span data-ttu-id="01bdc-p103">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01bdc-p103">If successful, this method returns a `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="01bdc-128">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="01bdc-128">Example</span></span>
##### <a name="request"></a><span data-ttu-id="01bdc-129">Solicitud</span><span class="sxs-lookup"><span data-stu-id="01bdc-129">Request</span></span>
<span data-ttu-id="01bdc-130">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="01bdc-130">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "delete_educationuser"
}-->
```http
DELETE https://graph.microsoft.com/v1.0/education/users/{user-id}
```
##### <a name="response"></a><span data-ttu-id="01bdc-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="01bdc-131">Response</span></span>
<span data-ttu-id="01bdc-132">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="01bdc-132">The following is an example of the response.</span></span> 
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