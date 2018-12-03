---
title: 'message: send'
description: Enviar un mensaje en la carpeta Borrador. El mensaje de borrador puede ser un borrador del mensaje nuevo, borrador de respuesta, borrador de responder a todos, o
ms.openlocfilehash: 8fe04db6a7fe4a469374cd54a00f308e01341274
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032215"
---
# <a name="message-send"></a><span data-ttu-id="48132-104">message: send</span><span class="sxs-lookup"><span data-stu-id="48132-104">message: send</span></span>

<span data-ttu-id="48132-p102">Envía un mensaje de la carpeta Borrador. El borrador del mensaje puede ser un borrador de mensaje nuevo, un borrador de respuesta, un borrador de respuesta a todos o un borrador de reenvío. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="48132-p102">Send a message in the draft folder. The draft message can be a new message draft, reply draft, reply-all draft, or a forward draft. The message is then saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="48132-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="48132-108">Permissions</span></span>

<span data-ttu-id="48132-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="48132-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="48132-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="48132-111">Permission type</span></span>      | <span data-ttu-id="48132-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="48132-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="48132-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="48132-113">Delegated (work or school account)</span></span> | <span data-ttu-id="48132-114">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="48132-114">Mail.Send</span></span>    |
|<span data-ttu-id="48132-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="48132-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="48132-116">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="48132-116">Mail.Send</span></span>    |
|<span data-ttu-id="48132-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="48132-117">Application</span></span> | <span data-ttu-id="48132-118">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="48132-118">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="48132-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="48132-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/send
POST /users/{id | userPrincipalName}/messages/{id}/send
```

## <a name="request-headers"></a><span data-ttu-id="48132-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="48132-120">Request headers</span></span>

| <span data-ttu-id="48132-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="48132-121">Name</span></span>       | <span data-ttu-id="48132-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="48132-122">Type</span></span> | <span data-ttu-id="48132-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="48132-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="48132-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="48132-124">Authorization</span></span>  | <span data-ttu-id="48132-125">string</span><span class="sxs-lookup"><span data-stu-id="48132-125">string</span></span>  | <span data-ttu-id="48132-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="48132-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="48132-128">Content-Length</span><span class="sxs-lookup"><span data-stu-id="48132-128">Content-Length</span></span> | <span data-ttu-id="48132-129">n?mero</span><span class="sxs-lookup"><span data-stu-id="48132-129">number</span></span> | <span data-ttu-id="48132-130">0. necesarios.</span><span class="sxs-lookup"><span data-stu-id="48132-130">0. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="48132-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="48132-131">Request body</span></span>

## <a name="response"></a><span data-ttu-id="48132-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48132-132">Response</span></span>

<span data-ttu-id="48132-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48132-p105">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="48132-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48132-135">Example</span></span>

<span data-ttu-id="48132-136">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="48132-136">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="48132-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48132-137">Request</span></span>

<span data-ttu-id="48132-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="48132-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_send"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/send
```

##### <a name="response"></a><span data-ttu-id="48132-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48132-139">Response</span></span>

<span data-ttu-id="48132-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48132-140">Here is an example of the response.</span></span>
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
