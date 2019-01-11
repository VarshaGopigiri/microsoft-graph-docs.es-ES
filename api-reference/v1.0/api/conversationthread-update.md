---
title: Update conversationthread
description: Bloquea o desbloquea un hilo para permitir o impedir futuras publicaciones en el hilo.
localization_priority: Normal
ms.openlocfilehash: a7f0738314bc071d5d084903fdc46b7fac1cf8cd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846497"
---
# <a name="update-conversationthread"></a><span data-ttu-id="8c282-103">Update conversationthread</span><span class="sxs-lookup"><span data-stu-id="8c282-103">Update conversationthread</span></span>

<span data-ttu-id="8c282-104">Bloquea o desbloquea un hilo para permitir o impedir futuras publicaciones en el hilo.</span><span class="sxs-lookup"><span data-stu-id="8c282-104">Lock or unlock a thread, to allow or avoid further posting to the thread.</span></span>
## <a name="permissions"></a><span data-ttu-id="8c282-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="8c282-105">Permissions</span></span>
<span data-ttu-id="8c282-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8c282-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8c282-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8c282-108">Permission type</span></span>      | <span data-ttu-id="8c282-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8c282-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="8c282-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8c282-110">Delegated (work or school account)</span></span> | <span data-ttu-id="8c282-111">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8c282-111">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="8c282-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8c282-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="8c282-113">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8c282-113">Not supported.</span></span>    |
|<span data-ttu-id="8c282-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8c282-114">Application</span></span> | <span data-ttu-id="8c282-115">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8c282-115">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="8c282-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8c282-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /groups/{id}/threads/{id}
PATCH /groups/{id}/conversations/{id}/threads/{id}

```
## <a name="request-headers"></a><span data-ttu-id="8c282-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8c282-117">Request headers</span></span>
| <span data-ttu-id="8c282-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8c282-118">Header</span></span>       | <span data-ttu-id="8c282-119">Valor</span><span class="sxs-lookup"><span data-stu-id="8c282-119">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="8c282-120">Authorization</span><span class="sxs-lookup"><span data-stu-id="8c282-120">Authorization</span></span>  | <span data-ttu-id="8c282-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8c282-p102">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="8c282-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="8c282-123">Content-Type</span></span>  | <span data-ttu-id="8c282-p103">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="8c282-p103">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="8c282-126">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8c282-126">Request body</span></span>
<span data-ttu-id="8c282-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="8c282-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="8c282-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8c282-130">Property</span></span>     | <span data-ttu-id="8c282-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8c282-131">Type</span></span>   |<span data-ttu-id="8c282-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8c282-132">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8c282-133">isLocked</span><span class="sxs-lookup"><span data-stu-id="8c282-133">isLocked</span></span>|<span data-ttu-id="8c282-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="8c282-134">Boolean</span></span>|<span data-ttu-id="8c282-p105">Indica si el hilo está bloqueado. Establecer en `true` para impedir publicaciones.</span><span class="sxs-lookup"><span data-stu-id="8c282-p105">Indicates if the thread is locked. Set to `true` to disallow posting.</span></span>|

## <a name="response"></a><span data-ttu-id="8c282-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c282-137">Response</span></span>

<span data-ttu-id="8c282-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [conversationThread](../resources/conversationthread.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8c282-138">If successful, this method returns a `200 OK` response code and updated [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="8c282-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8c282-139">Example</span></span>
##### <a name="request"></a><span data-ttu-id="8c282-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8c282-140">Request</span></span>
<span data-ttu-id="8c282-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8c282-141">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_conversationthread"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/groups/{id}/threads/{id}
Content-type: application/json
Content-length: 419

{
  "@odata.type":"#Microsoft.OutlookServices.ConversationThread",
  "isLocked": true
}
```
##### <a name="response"></a><span data-ttu-id="8c282-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8c282-142">Response</span></span>
<span data-ttu-id="8c282-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8c282-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.conversationThread"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 419

{
  "toRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ],
  "topic": "topic-value",
  "hasAttachments": true,
  "lastDeliveredDateTime": "datetime-value",
  "uniqueSenders": [
    "uniqueSenders-value"
  ],
  "ccRecipients": [
    {
      "emailAddress": {
        "name": "name-value",
        "address": "address-value"
      }
    }
  ],
  "isLocked": true 
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update conversationthread",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
