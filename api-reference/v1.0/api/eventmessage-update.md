---
title: Update eventMessage
description: Actualiza las propiedades de un objeto eventMessage.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 128849b2b0a1a156ef68498b345ca30833922d82
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867700"
---
# <a name="update-eventmessage"></a><span data-ttu-id="73265-103">Update eventMessage</span><span class="sxs-lookup"><span data-stu-id="73265-103">Update eventMessage</span></span>

<span data-ttu-id="73265-104">Actualiza las propiedades de un objeto [eventMessage](../resources/eventmessage.md).</span><span class="sxs-lookup"><span data-stu-id="73265-104">Update the properties of an [eventMessage](../resources/eventmessage.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="73265-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="73265-105">Permissions</span></span>
<span data-ttu-id="73265-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="73265-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="73265-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="73265-108">Permission type</span></span>      | <span data-ttu-id="73265-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="73265-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="73265-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="73265-110">Delegated (work or school account)</span></span> | <span data-ttu-id="73265-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="73265-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="73265-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="73265-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="73265-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="73265-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="73265-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="73265-114">Application</span></span> | <span data-ttu-id="73265-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="73265-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="73265-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="73265-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}

PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="73265-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="73265-117">Request headers</span></span>
| <span data-ttu-id="73265-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="73265-118">Name</span></span>       | <span data-ttu-id="73265-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="73265-119">Type</span></span> | <span data-ttu-id="73265-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="73265-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="73265-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="73265-121">Authorization</span></span>  | <span data-ttu-id="73265-122">string</span><span class="sxs-lookup"><span data-stu-id="73265-122">string</span></span>  | <span data-ttu-id="73265-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="73265-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="73265-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="73265-125">Content-Type</span></span> | <span data-ttu-id="73265-126">string</span><span class="sxs-lookup"><span data-stu-id="73265-126">string</span></span>  | <span data-ttu-id="73265-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="73265-p103">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="73265-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="73265-129">Request body</span></span>
<span data-ttu-id="73265-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado. Son propiedades Writable/Updatable</span><span class="sxs-lookup"><span data-stu-id="73265-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. Writable/Updatable properties are</span></span>

| <span data-ttu-id="73265-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="73265-134">Property</span></span>     | <span data-ttu-id="73265-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="73265-135">Type</span></span>   |<span data-ttu-id="73265-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="73265-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="73265-137">categories</span><span class="sxs-lookup"><span data-stu-id="73265-137">categories</span></span>|<span data-ttu-id="73265-138">String</span><span class="sxs-lookup"><span data-stu-id="73265-138">String</span></span>|<span data-ttu-id="73265-139">Categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="73265-139">The categories associated with the message.</span></span>|
|<span data-ttu-id="73265-140">importance</span><span class="sxs-lookup"><span data-stu-id="73265-140">importance</span></span>|<span data-ttu-id="73265-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="73265-141">String</span></span>|<span data-ttu-id="73265-142">La importancia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="73265-142">The importance of the message.</span></span> <span data-ttu-id="73265-143">Los valores posibles son: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="73265-143">The possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="73265-144">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="73265-144">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="73265-145">Booleano</span><span class="sxs-lookup"><span data-stu-id="73265-145">Boolean</span></span>|<span data-ttu-id="73265-146">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="73265-146">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="73265-147">isRead</span><span class="sxs-lookup"><span data-stu-id="73265-147">isRead</span></span>|<span data-ttu-id="73265-148">Booleano</span><span class="sxs-lookup"><span data-stu-id="73265-148">Boolean</span></span>|<span data-ttu-id="73265-149">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="73265-149">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="73265-150">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="73265-150">isReadReceiptRequested</span></span>|<span data-ttu-id="73265-151">Booleano</span><span class="sxs-lookup"><span data-stu-id="73265-151">Boolean</span></span>|<span data-ttu-id="73265-152">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="73265-152">Indicates whether a read receipt is requested for the message.</span></span>|

## <a name="response"></a><span data-ttu-id="73265-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73265-153">Response</span></span>

<span data-ttu-id="73265-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [eventMessage](../resources/eventmessage.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73265-154">If successful, this method returns a `200 OK` response code and updated [eventMessage](../resources/eventmessage.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="73265-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="73265-155">Example</span></span>
##### <a name="request"></a><span data-ttu-id="73265-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="73265-156">Request</span></span>
<span data-ttu-id="73265-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="73265-157">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_eventmessage"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/{id}
Content-type: application/json
Content-length: 248

{
  "isRead": "true",
}
```
##### <a name="response"></a><span data-ttu-id="73265-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73265-158">Response</span></span>
<span data-ttu-id="73265-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="73265-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.eventMessage"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 248

{
  "receivedDateTime": "datetime-value",
  "sentDateTime": "datetime-value",
  "hasAttachments": true,
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "bodyPreview": "bodyPreview-value",
  "meetingMessageType": "meetingMessageType-value"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update eventmessage",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
