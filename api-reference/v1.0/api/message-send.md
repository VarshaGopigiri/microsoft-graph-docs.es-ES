---
title: 'message: send'
description: Enviar un mensaje en la carpeta Borrador. El mensaje de borrador puede ser un borrador del mensaje nuevo, borrador de respuesta, borrador de responder a todos, o
localization_priority: Priority
author: angelgolfer-ms
ms.prod: outlook
ms.openlocfilehash: 3f9740f74238012571abcfa7f406fd12ed58c9e8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977062"
---
# <a name="message-send"></a><span data-ttu-id="6257d-104">message: send</span><span class="sxs-lookup"><span data-stu-id="6257d-104">message: send</span></span>

<span data-ttu-id="6257d-p102">Envía un mensaje de la carpeta Borrador. El borrador del mensaje puede ser un borrador de mensaje nuevo, un borrador de respuesta, un borrador de respuesta a todos o un borrador de reenvío. El mensaje se guarda en la carpeta Elementos enviados.</span><span class="sxs-lookup"><span data-stu-id="6257d-p102">Send a message in the draft folder. The draft message can be a new message draft, reply draft, reply-all draft, or a forward draft. The message is then saved in the Sent Items folder.</span></span>

## <a name="permissions"></a><span data-ttu-id="6257d-108">Permisos</span><span class="sxs-lookup"><span data-stu-id="6257d-108">Permissions</span></span>

<span data-ttu-id="6257d-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6257d-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6257d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6257d-111">Permission type</span></span>      | <span data-ttu-id="6257d-112">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6257d-112">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6257d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6257d-113">Delegated (work or school account)</span></span> | <span data-ttu-id="6257d-114">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="6257d-114">Mail.Send</span></span>    |
|<span data-ttu-id="6257d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6257d-115">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6257d-116">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="6257d-116">Mail.Send</span></span>    |
|<span data-ttu-id="6257d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6257d-117">Application</span></span> | <span data-ttu-id="6257d-118">Mail.Send</span><span class="sxs-lookup"><span data-stu-id="6257d-118">Mail.Send</span></span> |

## <a name="http-request"></a><span data-ttu-id="6257d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6257d-119">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /me/messages/{id}/send
POST /users/{id | userPrincipalName}/messages/{id}/send
```

## <a name="request-headers"></a><span data-ttu-id="6257d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6257d-120">Request headers</span></span>

| <span data-ttu-id="6257d-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="6257d-121">Name</span></span>       | <span data-ttu-id="6257d-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="6257d-122">Type</span></span> | <span data-ttu-id="6257d-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="6257d-123">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="6257d-124">Autorización</span><span class="sxs-lookup"><span data-stu-id="6257d-124">Authorization</span></span>  | <span data-ttu-id="6257d-125">string</span><span class="sxs-lookup"><span data-stu-id="6257d-125">string</span></span>  | <span data-ttu-id="6257d-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6257d-p104">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6257d-128">Content-Length</span><span class="sxs-lookup"><span data-stu-id="6257d-128">Content-Length</span></span> | <span data-ttu-id="6257d-129">number</span><span class="sxs-lookup"><span data-stu-id="6257d-129">number</span></span> | <span data-ttu-id="6257d-130">0. necesarios.</span><span class="sxs-lookup"><span data-stu-id="6257d-130">0. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="6257d-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6257d-131">Request body</span></span>

## <a name="response"></a><span data-ttu-id="6257d-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6257d-132">Response</span></span>

<span data-ttu-id="6257d-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `202 Accepted`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6257d-p105">If successful, this method returns `202 Accepted` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="6257d-135">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6257d-135">Example</span></span>

<span data-ttu-id="6257d-136">En el siguiente ejemplo se muestra cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="6257d-136">The following example shows how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="6257d-137">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6257d-137">Request</span></span>

<span data-ttu-id="6257d-138">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6257d-138">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "message_send"
}-->

```http
POST https://graph.microsoft.com/v1.0/me/messages/{id}/send
```

##### <a name="response"></a><span data-ttu-id="6257d-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6257d-139">Response</span></span>

<span data-ttu-id="6257d-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6257d-140">Here is an example of the response.</span></span>
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
