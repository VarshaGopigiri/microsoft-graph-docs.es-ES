---
title: 'group: unsubscribeByMail'
description: 'Llamar a este método, se deshabilitará el usuario actual para recibir notificaciones de correo electrónico para este grupo sobre publicaciones nuevas, eventos y los archivos de ese grupo. Compatible con sólo los grupos de Office 365. '
localization_priority: Normal
ms.openlocfilehash: a9c4777a511010ac42bcc31b2fa0a6dc754ac23f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887531"
---
# <a name="group-unsubscribebymail"></a><span data-ttu-id="bdece-104">group: unsubscribeByMail</span><span class="sxs-lookup"><span data-stu-id="bdece-104">group: unsubscribeByMail</span></span>

> <span data-ttu-id="bdece-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bdece-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bdece-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bdece-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="bdece-107">Llamar a este método, se deshabilitará el usuario actual para recibir notificaciones de correo electrónico para este grupo sobre publicaciones nuevas, eventos y los archivos de ese grupo.</span><span class="sxs-lookup"><span data-stu-id="bdece-107">Calling this method will disable the current user to receive email notifications for this group about new posts, events, and files in that group.</span></span> <span data-ttu-id="bdece-108">Compatible con sólo los grupos de Office 365.</span><span class="sxs-lookup"><span data-stu-id="bdece-108">Supported for Office 365 groups only.</span></span> 

## <a name="permissions"></a><span data-ttu-id="bdece-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="bdece-109">Permissions</span></span>
<span data-ttu-id="bdece-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="bdece-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="bdece-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="bdece-112">Permission type</span></span>      | <span data-ttu-id="bdece-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="bdece-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="bdece-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="bdece-114">Delegated (work or school account)</span></span> | <span data-ttu-id="bdece-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bdece-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="bdece-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="bdece-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="bdece-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="bdece-117">Not supported.</span></span>    |
|<span data-ttu-id="bdece-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="bdece-118">Application</span></span> | <span data-ttu-id="bdece-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="bdece-119">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="bdece-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="bdece-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/unsubscribeByMail
```

## <a name="request-headers"></a><span data-ttu-id="bdece-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="bdece-121">Request headers</span></span>
| <span data-ttu-id="bdece-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bdece-122">Header</span></span>       | <span data-ttu-id="bdece-123">Valor</span><span class="sxs-lookup"><span data-stu-id="bdece-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="bdece-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="bdece-124">Authorization</span></span>  | <span data-ttu-id="bdece-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="bdece-p105">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="bdece-127">Prefer</span><span class="sxs-lookup"><span data-stu-id="bdece-127">Prefer</span></span> | <span data-ttu-id="bdece-128">return=minimal.</span><span class="sxs-lookup"><span data-stu-id="bdece-128">return=minimal.</span></span> <span data-ttu-id="bdece-129">Si el encabezado de respuesta “mínimo” se incluye en el encabezado de solicitud, una respuesta correcta devolverá un código `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="bdece-129">If minimal response header is included in the request header, then a successful response returns `204 No Content` code.</span></span> <span data-ttu-id="bdece-130">Opcional.</span><span class="sxs-lookup"><span data-stu-id="bdece-130">Optional.</span></span>  | 

## <a name="request-body"></a><span data-ttu-id="bdece-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="bdece-131">Request body</span></span>
 <span data-ttu-id="bdece-132">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="bdece-132">Do not supply a request body for this method.</span></span> 

## <a name="response"></a><span data-ttu-id="bdece-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bdece-133">Response</span></span>
<span data-ttu-id="bdece-p107">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bdece-p107">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="bdece-136">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="bdece-136">Example</span></span>
#### <a name="request"></a><span data-ttu-id="bdece-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="bdece-137">Request</span></span>
<span data-ttu-id="bdece-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="bdece-138">The following is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "group_unsubscribebymail"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/unsubscribeByMail
```

#### <a name="response"></a><span data-ttu-id="bdece-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="bdece-139">Response</span></span>
<span data-ttu-id="bdece-140">Este es un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="bdece-140">The following is an example of the response.</span></span> 
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
