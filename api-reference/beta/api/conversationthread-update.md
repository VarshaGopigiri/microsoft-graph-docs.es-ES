---
title: Update conversationthread
description: Bloquea o desbloquea un hilo para permitir o impedir futuras publicaciones en el hilo.
localization_priority: Normal
ms.openlocfilehash: 49c5f26c9e7e995959b5d74f86d4a8a515708e24
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27887524"
---
# <a name="update-conversationthread"></a><span data-ttu-id="17ce8-103">Update conversationthread</span><span class="sxs-lookup"><span data-stu-id="17ce8-103">Update conversationthread</span></span>

> <span data-ttu-id="17ce8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="17ce8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="17ce8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="17ce8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="17ce8-106">Bloquea o desbloquea un hilo para permitir o impedir futuras publicaciones en el hilo.</span><span class="sxs-lookup"><span data-stu-id="17ce8-106">Lock or unlock a thread, to allow or avoid further posting to the thread.</span></span>
## <a name="permissions"></a><span data-ttu-id="17ce8-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="17ce8-107">Permissions</span></span>
<span data-ttu-id="17ce8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="17ce8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="17ce8-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="17ce8-110">Permission type</span></span>      | <span data-ttu-id="17ce8-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="17ce8-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="17ce8-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="17ce8-112">Delegated (work or school account)</span></span> | <span data-ttu-id="17ce8-113">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="17ce8-113">Group.ReadWrite.All</span></span>    |
|<span data-ttu-id="17ce8-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="17ce8-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="17ce8-115">No admitida.</span><span class="sxs-lookup"><span data-stu-id="17ce8-115">Not supported.</span></span>    |
|<span data-ttu-id="17ce8-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="17ce8-116">Application</span></span> | <span data-ttu-id="17ce8-117">Group.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="17ce8-117">Group.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="17ce8-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="17ce8-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /groups/{id}/threads/{id}
PATCH /groups/{id}/conversations/{id}/threads/{id}

```
## <a name="request-headers"></a><span data-ttu-id="17ce8-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="17ce8-119">Request headers</span></span>
| <span data-ttu-id="17ce8-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17ce8-120">Header</span></span>       | <span data-ttu-id="17ce8-121">Valor</span><span class="sxs-lookup"><span data-stu-id="17ce8-121">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="17ce8-122">Authorization</span><span class="sxs-lookup"><span data-stu-id="17ce8-122">Authorization</span></span>  | <span data-ttu-id="17ce8-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="17ce8-p103">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="17ce8-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="17ce8-125">Content-Type</span></span>  | <span data-ttu-id="17ce8-p104">application/json. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="17ce8-p104">application/json. Required.</span></span>  |

## <a name="request-body"></a><span data-ttu-id="17ce8-128">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="17ce8-128">Request body</span></span>
<span data-ttu-id="17ce8-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="17ce8-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed.</span></span>

| <span data-ttu-id="17ce8-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="17ce8-132">Property</span></span>     | <span data-ttu-id="17ce8-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="17ce8-133">Type</span></span>   |<span data-ttu-id="17ce8-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="17ce8-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="17ce8-135">isLocked</span><span class="sxs-lookup"><span data-stu-id="17ce8-135">isLocked</span></span>|<span data-ttu-id="17ce8-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="17ce8-136">Boolean</span></span>|<span data-ttu-id="17ce8-p106">Indica si el hilo está bloqueado. Establecer en `true` para impedir publicaciones.</span><span class="sxs-lookup"><span data-stu-id="17ce8-p106">Indicates if the thread is locked. Set to `true` to disallow posting.</span></span>|

## <a name="response"></a><span data-ttu-id="17ce8-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17ce8-139">Response</span></span>

<span data-ttu-id="17ce8-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [conversationThread](../resources/conversationthread.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="17ce8-140">If successful, this method returns a `200 OK` response code and updated [conversationThread](../resources/conversationthread.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="17ce8-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17ce8-141">Example</span></span>
##### <a name="request"></a><span data-ttu-id="17ce8-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="17ce8-142">Request</span></span>
<span data-ttu-id="17ce8-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="17ce8-143">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_conversationthread"
}-->
```http
PATCH https://graph.microsoft.com/beta/groups/{id}/threads/{id}
Content-type: application/json
Content-length: 419

{
  "@odata.type":"#Microsoft.OutlookServices.ConversationThread",
  "isLocked": true
}
```
##### <a name="response"></a><span data-ttu-id="17ce8-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="17ce8-144">Response</span></span>
<span data-ttu-id="17ce8-p107">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="17ce8-p107">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "lastDeliveredDateTime": "2016-10-19T10:37:00Z",
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
