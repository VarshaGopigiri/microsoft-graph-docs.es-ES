---
title: 'group: resetUnseenCount'
description: Restablece el valor de unseenCount de todas las publicaciones que el usuario actual no vio desde su última visita. Solo es compatible con Grupos de Office 365.
author: dkershaw10
ms.openlocfilehash: 6cb7533dc44ff86b2e1dbec5c99f4038ed03d224
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337460"
---
# <a name="group-resetunseencount"></a><span data-ttu-id="9d053-104">group: resetUnseenCount</span><span class="sxs-lookup"><span data-stu-id="9d053-104">group: resetUnseenCount</span></span>
<span data-ttu-id="9d053-p102">Restablece el valor de unseenCount de todas las publicaciones que el usuario actual no vio desde su última visita. Solo es compatible con Grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="9d053-p102">Reset the unseenCount of all the posts that the current user has not seen since their last visit. Supported for Office 365 groups only.</span></span>

## <a name="permissions"></a><span data-ttu-id="9d053-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="9d053-107">Permissions</span></span>
<span data-ttu-id="9d053-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9d053-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9d053-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9d053-110">Permission type</span></span>      | <span data-ttu-id="9d053-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9d053-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9d053-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9d053-112">Delegated (work or school account)</span></span> | <span data-ttu-id="9d053-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9d053-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="9d053-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9d053-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9d053-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9d053-115">Not supported.</span></span>    |
|<span data-ttu-id="9d053-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9d053-116">Application</span></span> | <span data-ttu-id="9d053-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9d053-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="9d053-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9d053-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/resetUnseenCount
```
## <a name="request-headers"></a><span data-ttu-id="9d053-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9d053-119">Request headers</span></span>
| <span data-ttu-id="9d053-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9d053-120">Header</span></span>       | <span data-ttu-id="9d053-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9d053-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="9d053-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="9d053-122">Authorization</span></span>  | <span data-ttu-id="9d053-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9d053-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="9d053-125">Prefer</span><span class="sxs-lookup"><span data-stu-id="9d053-125">Prefer</span></span> | <span data-ttu-id="9d053-126">return=minimal.</span><span class="sxs-lookup"><span data-stu-id="9d053-126">return=minimal.</span></span> <span data-ttu-id="9d053-127">Si el encabezado de respuesta “mínimo” se incluye en el encabezado de solicitud, una respuesta correcta devolverá un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="9d053-127">If minimal response header is included in the request header, then a successful response returns `204 No Content` code.</span></span> <span data-ttu-id="9d053-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="9d053-128">Optional.</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="9d053-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9d053-129">Request body</span></span>
<span data-ttu-id="9d053-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9d053-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9d053-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d053-131">Response</span></span>
<span data-ttu-id="9d053-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d053-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9d053-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9d053-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="9d053-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9d053-135">Request</span></span>
<span data-ttu-id="9d053-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9d053-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_resetunseencount"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/resetUnseenCount
```

#### <a name="response"></a><span data-ttu-id="9d053-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9d053-137">Response</span></span>
<span data-ttu-id="9d053-138">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9d053-138">The following is an example of the response.</span></span> 
<!-- {
  "blockType": "response",
  "truncated": true
} -->
```http
HTTP/1.1 200 OK
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: resetUnseenCount",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
