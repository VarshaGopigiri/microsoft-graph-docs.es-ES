---
title: Update eventMessage
description: Actualiza las propiedades de un objeto eventMessage.
ms.openlocfilehash: 3d81977c815737ae96839c6fc883692bf2555597
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083620"
---
# <a name="update-eventmessage"></a><span data-ttu-id="6e297-103">Update eventMessage</span><span class="sxs-lookup"><span data-stu-id="6e297-103">Update eventMessage</span></span>

> <span data-ttu-id="6e297-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6e297-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6e297-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6e297-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6e297-106">Actualiza las propiedades de un objeto [eventMessage](../resources/eventmessage.md).</span><span class="sxs-lookup"><span data-stu-id="6e297-106">Update the properties of an [eventMessage](../resources/eventmessage.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6e297-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6e297-107">Permissions</span></span>
<span data-ttu-id="6e297-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6e297-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6e297-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6e297-110">Permission type</span></span>      | <span data-ttu-id="6e297-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6e297-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6e297-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6e297-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6e297-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e297-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6e297-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6e297-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6e297-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e297-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6e297-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6e297-116">Application</span></span> | <span data-ttu-id="6e297-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6e297-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="6e297-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6e297-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}

PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="6e297-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6e297-119">Request headers</span></span>
| <span data-ttu-id="6e297-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6e297-120">Name</span></span>       | <span data-ttu-id="6e297-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e297-121">Type</span></span> | <span data-ttu-id="6e297-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e297-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6e297-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6e297-123">Authorization</span></span>  | <span data-ttu-id="6e297-124">string</span><span class="sxs-lookup"><span data-stu-id="6e297-124">string</span></span>  | <span data-ttu-id="6e297-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6e297-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6e297-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6e297-127">Content-Type</span></span> | <span data-ttu-id="6e297-128">string</span><span class="sxs-lookup"><span data-stu-id="6e297-128">string</span></span>  | <span data-ttu-id="6e297-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6e297-p104">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="6e297-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6e297-131">Request body</span></span>
<span data-ttu-id="6e297-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado. Son propiedades Writable/Updatable</span><span class="sxs-lookup"><span data-stu-id="6e297-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. Writable/Updatable properties are</span></span>

| <span data-ttu-id="6e297-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6e297-136">Property</span></span>     | <span data-ttu-id="6e297-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e297-137">Type</span></span>   |<span data-ttu-id="6e297-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e297-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6e297-139">categories</span><span class="sxs-lookup"><span data-stu-id="6e297-139">categories</span></span>|<span data-ttu-id="6e297-140">String</span><span class="sxs-lookup"><span data-stu-id="6e297-140">String</span></span>|<span data-ttu-id="6e297-141">Categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="6e297-141">The categories associated with the message.</span></span>|
|<span data-ttu-id="6e297-142">importance</span><span class="sxs-lookup"><span data-stu-id="6e297-142">importance</span></span>|<span data-ttu-id="6e297-143">String</span><span class="sxs-lookup"><span data-stu-id="6e297-143">String</span></span>|<span data-ttu-id="6e297-p106">Importancia del mensaje. Valores posibles: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="6e297-p106">The importance of the message. Possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="6e297-146">isAllDay</span><span class="sxs-lookup"><span data-stu-id="6e297-146">isAllDay</span></span> |<span data-ttu-id="6e297-147">Booleano</span><span class="sxs-lookup"><span data-stu-id="6e297-147">Boolean</span></span>|<span data-ttu-id="6e297-148">Indica si el evento dura todo el día.</span><span class="sxs-lookup"><span data-stu-id="6e297-148">Indicates whether the event lasts the entire day.</span></span> <span data-ttu-id="6e297-149">Ajuste de esta propiedad requiere ajustar las propiedades **startDateTime** y **endDateTime** del evento así como.</span><span class="sxs-lookup"><span data-stu-id="6e297-149">Adjusting this property requires adjusting the **startDateTime** and **endDateTime** properties of the event as well.</span></span>|
|<span data-ttu-id="6e297-150">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="6e297-150">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="6e297-151">Booleano</span><span class="sxs-lookup"><span data-stu-id="6e297-151">Boolean</span></span>|<span data-ttu-id="6e297-152">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6e297-152">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="6e297-153">isRead</span><span class="sxs-lookup"><span data-stu-id="6e297-153">isRead</span></span>|<span data-ttu-id="6e297-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="6e297-154">Boolean</span></span>|<span data-ttu-id="6e297-155">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6e297-155">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="6e297-156">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="6e297-156">isReadReceiptRequested</span></span>|<span data-ttu-id="6e297-157">Booleano</span><span class="sxs-lookup"><span data-stu-id="6e297-157">Boolean</span></span>|<span data-ttu-id="6e297-158">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6e297-158">Indicates whether a read receipt is requested for the message.</span></span>|

## <a name="response"></a><span data-ttu-id="6e297-159">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e297-159">Response</span></span>

<span data-ttu-id="6e297-160">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [eventMessage](../resources/eventmessage.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6e297-160">If successful, this method returns a `200 OK` response code and updated [eventMessage](../resources/eventmessage.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6e297-161">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6e297-161">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6e297-162">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6e297-162">Request</span></span>
<span data-ttu-id="6e297-163">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6e297-163">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_eventmessage"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/messages/{id}
Content-type: application/json
Content-length: 248

{
  "isRead": "true",
}
```
##### <a name="response"></a><span data-ttu-id="6e297-164">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6e297-164">Response</span></span>
<span data-ttu-id="6e297-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6e297-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "receivedDateTime": "2016-10-19T10:37:00Z",
  "sentDateTime": "2016-10-19T10:37:00Z",
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