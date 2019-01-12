---
title: 'group: renew'
description: Renueva la expiración de un grupo. Cuando se renueva un grupo, la expiración del grupo se amplía por el número de días definidos en la directiva.
localization_priority: Normal
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: 46a51d0a1d4bea5cebc4c3178f6776d80f313fbd
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922735"
---
# <a name="group-renew"></a><span data-ttu-id="cd24c-104">group: renew</span><span class="sxs-lookup"><span data-stu-id="cd24c-104">group: renew</span></span>

<span data-ttu-id="cd24c-105">Renueva la expiración de un grupo.</span><span class="sxs-lookup"><span data-stu-id="cd24c-105">Renews a group's expiration.</span></span> <span data-ttu-id="cd24c-106">Cuando se renueva un grupo, la expiración del grupo se amplía por el número de días definidos en la directiva.</span><span class="sxs-lookup"><span data-stu-id="cd24c-106">When a group is renewed, the group expiration is extended by the number of days defined in the policy.</span></span>

## <a name="permissions"></a><span data-ttu-id="cd24c-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="cd24c-107">Permissions</span></span>

<span data-ttu-id="cd24c-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cd24c-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>
 

|<span data-ttu-id="cd24c-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cd24c-110">Permission type</span></span>      | <span data-ttu-id="cd24c-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cd24c-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="cd24c-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cd24c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="cd24c-113">Group.ReadWrite.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cd24c-113">Group.ReadWrite.All or Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="cd24c-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cd24c-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="cd24c-115">No admitido</span><span class="sxs-lookup"><span data-stu-id="cd24c-115">Not supported</span></span> |
|<span data-ttu-id="cd24c-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cd24c-116">Application</span></span> | <span data-ttu-id="cd24c-117">Group.ReadWrite.All o Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="cd24c-117">Group.ReadWrite.All or Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="cd24c-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cd24c-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/renew
```

## <a name="request-headers"></a><span data-ttu-id="cd24c-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cd24c-119">Request headers</span></span>
| <span data-ttu-id="cd24c-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="cd24c-120">Name</span></span>       | <span data-ttu-id="cd24c-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="cd24c-121">Description</span></span>|
|:---------------|:----------|
| <span data-ttu-id="cd24c-122">Autorización</span><span class="sxs-lookup"><span data-stu-id="cd24c-122">Authorization</span></span>  | <span data-ttu-id="cd24c-123">Bearer {token}</span><span class="sxs-lookup"><span data-stu-id="cd24c-123">Bearer {token}</span></span> |


## <a name="request-body"></a><span data-ttu-id="cd24c-124">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cd24c-124">Request body</span></span>

<span data-ttu-id="cd24c-125">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cd24c-125">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cd24c-126">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd24c-126">Response</span></span>

<span data-ttu-id="cd24c-p104">Si se ejecuta correctamente, este método devuelve el código de respuesta `204 No Content`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cd24c-p104">If successful, this method returns `204 No Content` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cd24c-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cd24c-129">Example</span></span>

##### <a name="request"></a><span data-ttu-id="cd24c-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cd24c-130">Request</span></span>

<!-- {
  "blockType": "request",
  "name": "group_renew"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/renew
```

##### <a name="response"></a><span data-ttu-id="cd24c-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cd24c-131">Response</span></span>
<span data-ttu-id="cd24c-p105">Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cd24c-p105">Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "Boolean"
} -->
```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "group: renew",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
