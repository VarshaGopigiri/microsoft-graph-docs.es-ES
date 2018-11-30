---
title: 'post: forward'
description: 'Reenvíe una publicación a un destinatario. Puede especificar la conversación primario y el subproceso en la solicitud, '
ms.openlocfilehash: 06dadc321edb1a3e37a0d09e6fcc07ec029d2945
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029034"
---
# <a name="post-forward"></a><span data-ttu-id="3f5d3-104">post: forward</span><span class="sxs-lookup"><span data-stu-id="3f5d3-104">post: forward</span></span>

<span data-ttu-id="3f5d3-p102">Reenvía una publicación a un destinatario. Puede especificar la conversación y el hilo primarios en la solicitud, o bien, especificar solo el hilo primario sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="3f5d3-p102">Forward a post to a recipient. You can specify both the parent conversation and thread in the request, or, you can specify just the parent thread without the parent conversation.</span></span> 

## <a name="permissions"></a><span data-ttu-id="3f5d3-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="3f5d3-107">Permissions</span></span>
<span data-ttu-id="3f5d3-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="3f5d3-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="3f5d3-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="3f5d3-110">Permission type</span></span>      | <span data-ttu-id="3f5d3-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="3f5d3-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="3f5d3-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="3f5d3-112">Delegated (work or school account)</span></span> | <span data-ttu-id="3f5d3-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3f5d3-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="3f5d3-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="3f5d3-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="3f5d3-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="3f5d3-115">Not supported.</span></span>    |
|<span data-ttu-id="3f5d3-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="3f5d3-116">Application</span></span> | <span data-ttu-id="3f5d3-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="3f5d3-117">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="3f5d3-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="3f5d3-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/posts/{id}/forward
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/forward

```
## <a name="request-headers"></a><span data-ttu-id="3f5d3-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="3f5d3-119">Request headers</span></span>
| <span data-ttu-id="3f5d3-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3f5d3-120">Header</span></span>       | <span data-ttu-id="3f5d3-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3f5d3-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="3f5d3-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="3f5d3-122">Authorization</span></span>  | <span data-ttu-id="3f5d3-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="3f5d3-p104">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="3f5d3-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="3f5d3-125">Request body</span></span>
<span data-ttu-id="3f5d3-126">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="3f5d3-126">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="3f5d3-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="3f5d3-127">Parameter</span></span>    | <span data-ttu-id="3f5d3-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f5d3-128">Type</span></span>   |<span data-ttu-id="3f5d3-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f5d3-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3f5d3-130">comment</span><span class="sxs-lookup"><span data-stu-id="3f5d3-130">comment</span></span>|<span data-ttu-id="3f5d3-131">String</span><span class="sxs-lookup"><span data-stu-id="3f5d3-131">String</span></span>|<span data-ttu-id="3f5d3-132">Comentario opcional que se envía junto con la publicación.</span><span class="sxs-lookup"><span data-stu-id="3f5d3-132">Optional comment that is forwarded together with the post.</span></span>|
|<span data-ttu-id="3f5d3-133">toRecipients</span><span class="sxs-lookup"><span data-stu-id="3f5d3-133">toRecipients</span></span>|<span data-ttu-id="3f5d3-134">Colección [recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="3f5d3-134">[recipient](../resources/recipient.md) collection</span></span>|<span data-ttu-id="3f5d3-135">Destinatarios a los que se ha reenviado el encadenado de hilos.</span><span class="sxs-lookup"><span data-stu-id="3f5d3-135">The recipients to whom the threaded is forwarded to.</span></span>|

## <a name="response"></a><span data-ttu-id="3f5d3-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f5d3-136">Response</span></span>

<span data-ttu-id="3f5d3-p105">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f5d3-p105">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="3f5d3-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="3f5d3-139">Example</span></span>
<span data-ttu-id="3f5d3-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="3f5d3-140">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="3f5d3-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="3f5d3-141">Request</span></span>
<span data-ttu-id="3f5d3-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="3f5d3-142">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_forward"
}-->
```http
POST https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}/posts/{id}/forward
Content-type: application/json
Content-length: 166

{
  "comment": "comment-value",
  "toRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ]
}
```

##### <a name="response"></a><span data-ttu-id="3f5d3-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="3f5d3-143">Response</span></span>
<span data-ttu-id="3f5d3-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="3f5d3-144">Here is an example of the response.</span></span>
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
  "description": "post: forward",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->