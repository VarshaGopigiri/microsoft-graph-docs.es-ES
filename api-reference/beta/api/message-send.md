---
title: 'message: send'
description: Enviar un mensaje en la carpeta Borrador. El mensaje de borrador puede ser un borrador del mensaje nuevo, borrador de respuesta, borrador de responder a todos, o
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 937c2da1bab83c412097f4207f32d07dc98d2ff8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940676"
---
# <a name="message-send"></a><span data-ttu-id="c6cec-104">message: send</span><span class="sxs-lookup"><span data-stu-id="c6cec-104">message: send</span></span>

> <span data-ttu-id="c6cec-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c6cec-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c6cec-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c6cec-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="c6cec-p103">Envía un mensaje de la carpeta Borrador. El borrador del mensaje puede ser un borrador de mensaje nuevo, un borrador de respuesta, un borrador de respuesta a todos o un borrador de reenvío. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="c6cec-p103">Send a message in the draft folder. The draft message can be a new message draft, reply draft, reply-all draft, or a forward draft. The message is then saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="c6cec-110">Permisos</span><span class="sxs-lookup"><span data-stu-id="c6cec-110">Permissions</span></span>

<span data-ttu-id="c6cec-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c6cec-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c6cec-113">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c6cec-113">Permission type</span></span>      | <span data-ttu-id="c6cec-114">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c6cec-114">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="c6cec-115">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c6cec-115">Delegated (work or school account)</span></span> | <span data-ttu-id="c6cec-116">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="c6cec-116">Mail.Send</span></span>    |
|<span data-ttu-id="c6cec-117">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c6cec-117">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="c6cec-118">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="c6cec-118">Mail.Send</span></span>    |
|<span data-ttu-id="c6cec-119">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c6cec-119">Application</span></span> | <span data-ttu-id="c6cec-120">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="c6cec-120">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="c6cec-121">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c6cec-121">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/send
POST /users/{id | userPrincipalName}/messages/{id}/send
```

## <a name="request-headers"></a><span data-ttu-id="c6cec-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c6cec-122">Request headers</span></span>

| <span data-ttu-id="c6cec-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="c6cec-123">Name</span></span>       | <span data-ttu-id="c6cec-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="c6cec-124">Type</span></span> | <span data-ttu-id="c6cec-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="c6cec-125">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c6cec-126">Autorización</span><span class="sxs-lookup"><span data-stu-id="c6cec-126">Authorization</span></span>  | <span data-ttu-id="c6cec-127">string</span><span class="sxs-lookup"><span data-stu-id="c6cec-127">string</span></span>  | <span data-ttu-id="c6cec-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c6cec-p105">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c6cec-130">Content-Length</span><span class="sxs-lookup"><span data-stu-id="c6cec-130">Content-Length</span></span> | <span data-ttu-id="c6cec-131">number</span><span class="sxs-lookup"><span data-stu-id="c6cec-131">number</span></span> | <span data-ttu-id="c6cec-132">0. necesarios.</span><span class="sxs-lookup"><span data-stu-id="c6cec-132">0. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="c6cec-133">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c6cec-133">Request body</span></span>

## <a name="response"></a><span data-ttu-id="c6cec-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6cec-134">Response</span></span>

<span data-ttu-id="c6cec-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6cec-p106">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c6cec-137">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c6cec-137">Example</span></span>

<span data-ttu-id="c6cec-138">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="c6cec-138">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="c6cec-139">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c6cec-139">Request</span></span>

<span data-ttu-id="c6cec-140">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c6cec-140">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_send"
}-->

```http
POST https://graph.microsoft.com/beta/me/messages/{id}/send
```

##### <a name="response"></a><span data-ttu-id="c6cec-141">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c6cec-141">Response</span></span>

<span data-ttu-id="c6cec-142">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c6cec-142">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 202 Accepted
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "message: send",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
