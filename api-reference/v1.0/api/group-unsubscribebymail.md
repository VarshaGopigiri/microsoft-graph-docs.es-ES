---
title: 'group: unsubscribeByMail'
description: 'La llamada a este método impedirá que el usuario actual reciba notificaciones por correo electrónico para este grupo, sobre nuevos eventos, publicaciones y archivos de ese grupo. Solo es compatible con Grupos de Office 365. '
localization_priority: Normal
author: dkershaw10
ms.prod: groups
ms.openlocfilehash: b7ac6954c325e0192549c286613ff2794e973a0f
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27957448"
---
# <a name="group-unsubscribebymail"></a><span data-ttu-id="da324-104">group: unsubscribeByMail</span><span class="sxs-lookup"><span data-stu-id="da324-104">group: unsubscribeByMail</span></span>
<span data-ttu-id="da324-p102">La llamada a este método impedirá que el usuario actual reciba notificaciones por correo electrónico para este grupo, sobre nuevos eventos, publicaciones y archivos de ese grupo. Solo es compatible con Grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="da324-p102">Calling this method will prevent the current user from receiving email notifications for this group about new posts, events, and files in that group. Supported for Office 365 groups only.</span></span> 

## <a name="permissions"></a><span data-ttu-id="da324-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="da324-107">Permissions</span></span>
<span data-ttu-id="da324-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="da324-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="da324-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="da324-110">Permission type</span></span>      | <span data-ttu-id="da324-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="da324-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="da324-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="da324-112">Delegated (work or school account)</span></span> | <span data-ttu-id="da324-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="da324-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="da324-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="da324-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="da324-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da324-115">Not supported.</span></span>    |
|<span data-ttu-id="da324-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="da324-116">Application</span></span> | <span data-ttu-id="da324-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="da324-117">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="da324-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="da324-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/unsubscribeByMail
```
## <a name="request-headers"></a><span data-ttu-id="da324-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="da324-119">Request headers</span></span>
| <span data-ttu-id="da324-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="da324-120">Header</span></span>       | <span data-ttu-id="da324-121">Valor</span><span class="sxs-lookup"><span data-stu-id="da324-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="da324-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="da324-122">Authorization</span></span>  | <span data-ttu-id="da324-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="da324-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="da324-125">Prefer</span><span class="sxs-lookup"><span data-stu-id="da324-125">Prefer</span></span> | <span data-ttu-id="da324-126">return=minimal.</span><span class="sxs-lookup"><span data-stu-id="da324-126">return=minimal.</span></span> <span data-ttu-id="da324-127">Si el encabezado de respuesta “mínimo” se incluye en el encabezado de solicitud, una respuesta correcta devolverá un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="da324-127">If minimal response header is included in the request header, then a successful response returns `204 No Content` code.</span></span> <span data-ttu-id="da324-128">Opcional.</span><span class="sxs-lookup"><span data-stu-id="da324-128">Optional.</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="da324-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="da324-129">Request body</span></span>
<span data-ttu-id="da324-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="da324-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="da324-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da324-131">Response</span></span>
<span data-ttu-id="da324-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da324-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="da324-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="da324-134">Example</span></span>
#### <a name="request"></a><span data-ttu-id="da324-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="da324-135">Request</span></span>
<span data-ttu-id="da324-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="da324-136">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_unsubscribebymail"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/unsubscribeByMail
```

#### <a name="response"></a><span data-ttu-id="da324-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="da324-137">Response</span></span>
<span data-ttu-id="da324-138">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="da324-138">The following is an example of the response.</span></span> 
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
  "description": "group: unsubscribeByMail",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
