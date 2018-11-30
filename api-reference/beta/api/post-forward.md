---
title: 'post: forward'
description: 'Reenvíe una publicación a un destinatario. Puede especificar la conversación primario y el subproceso en la solicitud, '
ms.openlocfilehash: 736b23aaf90cb7e4af243129e52a014ae623b8f4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086253"
---
# <a name="post-forward"></a><span data-ttu-id="5fa68-104">post: forward</span><span class="sxs-lookup"><span data-stu-id="5fa68-104">post: forward</span></span>

> <span data-ttu-id="5fa68-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5fa68-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5fa68-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5fa68-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5fa68-p103">Reenvía una publicación a un destinatario. Puede especificar la conversación y el hilo primarios en la solicitud, o bien, especificar solo el hilo primario sin la conversación primaria.</span><span class="sxs-lookup"><span data-stu-id="5fa68-p103">Forward a post to a recipient. You can specify both the parent conversation and thread in the request, or, you can specify just the parent thread without the parent conversation.</span></span> 

## <a name="permissions"></a><span data-ttu-id="5fa68-109">Permisos</span><span class="sxs-lookup"><span data-stu-id="5fa68-109">Permissions</span></span>
<span data-ttu-id="5fa68-p104">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5fa68-p104">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5fa68-112">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5fa68-112">Permission type</span></span>      | <span data-ttu-id="5fa68-113">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5fa68-113">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="5fa68-114">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5fa68-114">Delegated (work or school account)</span></span> | <span data-ttu-id="5fa68-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5fa68-115">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="5fa68-116">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5fa68-116">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="5fa68-117">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5fa68-117">Not supported.</span></span>    |
|<span data-ttu-id="5fa68-118">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5fa68-118">Application</span></span> | <span data-ttu-id="5fa68-119">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5fa68-119">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="5fa68-120">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5fa68-120">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /groups/{id}/threads/{id}/posts/{id}/forward
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/forward

```
## <a name="request-headers"></a><span data-ttu-id="5fa68-121">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5fa68-121">Request headers</span></span>
| <span data-ttu-id="5fa68-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5fa68-122">Header</span></span>       | <span data-ttu-id="5fa68-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5fa68-123">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="5fa68-124">Authorization</span><span class="sxs-lookup"><span data-stu-id="5fa68-124">Authorization</span></span>  | <span data-ttu-id="5fa68-p105">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="5fa68-p105">Bearer {token}. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="5fa68-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5fa68-127">Request body</span></span>
<span data-ttu-id="5fa68-128">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="5fa68-128">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="5fa68-129">Parámetro</span><span class="sxs-lookup"><span data-stu-id="5fa68-129">Parameter</span></span>    | <span data-ttu-id="5fa68-130">Tipo</span><span class="sxs-lookup"><span data-stu-id="5fa68-130">Type</span></span>   |<span data-ttu-id="5fa68-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="5fa68-131">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5fa68-132">comment</span><span class="sxs-lookup"><span data-stu-id="5fa68-132">comment</span></span>|<span data-ttu-id="5fa68-133">String</span><span class="sxs-lookup"><span data-stu-id="5fa68-133">String</span></span>|<span data-ttu-id="5fa68-134">Comentario opcional que se envía junto con la publicación.</span><span class="sxs-lookup"><span data-stu-id="5fa68-134">Optional comment that is forwarded together with the post.</span></span>|
|<span data-ttu-id="5fa68-135">toRecipients</span><span class="sxs-lookup"><span data-stu-id="5fa68-135">toRecipients</span></span>|<span data-ttu-id="5fa68-136">Colección [recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="5fa68-136">[recipient](../resources/recipient.md) collection</span></span>|<span data-ttu-id="5fa68-137">Destinatarios a los que se ha reenviado el encadenado de hilos.</span><span class="sxs-lookup"><span data-stu-id="5fa68-137">The recipients to whom the threaded is forwarded to.</span></span>|

## <a name="response"></a><span data-ttu-id="5fa68-138">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5fa68-138">Response</span></span>

<span data-ttu-id="5fa68-p106">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK`. No devuelve nada en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5fa68-p106">If successful, this method returns `200 OK` response code. It does not return anything in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5fa68-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5fa68-141">Example</span></span>
<span data-ttu-id="5fa68-142">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="5fa68-142">Here is an example of how to call this API.</span></span>
##### <a name="request"></a><span data-ttu-id="5fa68-143">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5fa68-143">Request</span></span>
<span data-ttu-id="5fa68-144">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5fa68-144">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "post_forward"
}-->
```http
POST https://graph.microsoft.com/beta/groups/{id}/threads/{id}/posts/{id}/forward
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

##### <a name="response"></a><span data-ttu-id="5fa68-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5fa68-145">Response</span></span>
<span data-ttu-id="5fa68-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5fa68-146">Here is an example of the response.</span></span>
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
