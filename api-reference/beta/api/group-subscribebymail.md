---
title: 'group: subscribeByMail'
description: Llamar a este método, se habilitará el usuario actual recibir notificaciones de correo electrónico para este grupo, sobre publicaciones nuevas, eventos y los archivos de ese grupo. Compatible con sólo los grupos de Office 365.
ms.openlocfilehash: 3e43f3805974fa518bf006682e8dd1f211e20417
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089768"
---
# <a name="group-subscribebymail"></a><span data-ttu-id="5308e-104">group: subscribeByMail</span><span class="sxs-lookup"><span data-stu-id="5308e-104">group: subscribeByMail</span></span>

> <span data-ttu-id="5308e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5308e-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5308e-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5308e-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5308e-107">Llamar a este método, se habilitará el usuario actual recibir notificaciones de correo electrónico para este grupo, sobre publicaciones nuevas, eventos y los archivos de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="5308e-107">Calling this method will enable the current user to receive email notifications for this group, about new posts, events, and files in that group.</span></span> <span data-ttu-id="5308e-108">Compatible con sólo los grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="5308e-108">Supported for Office 365 Groups only.</span></span>

## <a name="permissions"></a><span data-ttu-id="5308e-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="5308e-109">Permissions</span></span>
<span data-ttu-id="5308e-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5308e-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5308e-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5308e-112">Permission type</span></span>      | <span data-ttu-id="5308e-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5308e-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5308e-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5308e-114">Delegated (work or school account)</span></span> | <span data-ttu-id="5308e-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5308e-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="5308e-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5308e-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5308e-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5308e-117">Not supported.</span></span>    |
|<span data-ttu-id="5308e-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5308e-118">Application</span></span> | <span data-ttu-id="5308e-119">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5308e-119">Not supported.</span></span> |

## <a name="http-request"></a><span data-ttu-id="5308e-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5308e-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/subscribeByMail
```
## <a name="request-headers"></a><span data-ttu-id="5308e-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5308e-121">Request headers</span></span>
| <span data-ttu-id="5308e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5308e-122">Header</span></span>       | <span data-ttu-id="5308e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5308e-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5308e-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="5308e-124">Authorization</span></span>  | <span data-ttu-id="5308e-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5308e-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="5308e-127">Prefer</span><span class="sxs-lookup"><span data-stu-id="5308e-127">Prefer</span></span> | <span data-ttu-id="5308e-128">return=minimal.</span><span class="sxs-lookup"><span data-stu-id="5308e-128">return=minimal.</span></span> <span data-ttu-id="5308e-129">Si el encabezado de respuesta “mínimo” se incluye en el encabezado de solicitud, una respuesta correcta devolverá un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="5308e-129">If minimal response header is included in the request header, then a successful response returns `204 No Content` code.</span></span> <span data-ttu-id="5308e-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="5308e-130">Optional.</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="5308e-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5308e-131">Request body</span></span>

## <a name="response"></a><span data-ttu-id="5308e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5308e-132">Response</span></span>
<span data-ttu-id="5308e-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5308e-p107">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5308e-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5308e-135">Example</span></span>
#### <a name="request"></a><span data-ttu-id="5308e-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5308e-136">Request</span></span>
<span data-ttu-id="5308e-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5308e-137">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_subscribebymail"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/subscribeByMail
```

#### <a name="response"></a><span data-ttu-id="5308e-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5308e-138">Response</span></span>
<span data-ttu-id="5308e-139">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5308e-139">The following is an example of the response.</span></span> 
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
  "description": "group: subscribeByMail",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->