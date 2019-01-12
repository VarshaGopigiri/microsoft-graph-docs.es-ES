---
title: Update eventMessage
description: Actualiza las propiedades de un objeto eventMessage.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: a906dbbdb9a82e78a49ea41399e3791c9d52645b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943889"
---
# <a name="update-eventmessage"></a><span data-ttu-id="64d07-103">Update eventMessage</span><span class="sxs-lookup"><span data-stu-id="64d07-103">Update eventMessage</span></span>

<span data-ttu-id="64d07-104">Actualiza las propiedades de un objeto [eventMessage](../resources/eventmessage.md).</span><span class="sxs-lookup"><span data-stu-id="64d07-104">Update the properties of an [eventMessage](../resources/eventmessage.md) object.</span></span>
## <a name="permissions"></a><span data-ttu-id="64d07-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="64d07-105">Permissions</span></span>
<span data-ttu-id="64d07-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="64d07-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="64d07-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="64d07-108">Permission type</span></span>      | <span data-ttu-id="64d07-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="64d07-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="64d07-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="64d07-110">Delegated (work or school account)</span></span> | <span data-ttu-id="64d07-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="64d07-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="64d07-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="64d07-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="64d07-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="64d07-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="64d07-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="64d07-114">Application</span></span> | <span data-ttu-id="64d07-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="64d07-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="64d07-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="64d07-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}

PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="64d07-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="64d07-117">Request headers</span></span>
| <span data-ttu-id="64d07-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="64d07-118">Name</span></span>       | <span data-ttu-id="64d07-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="64d07-119">Type</span></span> | <span data-ttu-id="64d07-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="64d07-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="64d07-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="64d07-121">Authorization</span></span>  | <span data-ttu-id="64d07-122">string</span><span class="sxs-lookup"><span data-stu-id="64d07-122">string</span></span>  | <span data-ttu-id="64d07-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64d07-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="64d07-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="64d07-125">Content-Type</span></span> | <span data-ttu-id="64d07-126">string</span><span class="sxs-lookup"><span data-stu-id="64d07-126">string</span></span>  | <span data-ttu-id="64d07-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="64d07-p103">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="64d07-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="64d07-129">Request body</span></span>
<span data-ttu-id="64d07-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado. Son propiedades Writable/Updatable</span><span class="sxs-lookup"><span data-stu-id="64d07-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. Writable/Updatable properties are</span></span>

| <span data-ttu-id="64d07-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="64d07-134">Property</span></span>     | <span data-ttu-id="64d07-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="64d07-135">Type</span></span>   |<span data-ttu-id="64d07-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="64d07-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="64d07-137">categories</span><span class="sxs-lookup"><span data-stu-id="64d07-137">categories</span></span>|<span data-ttu-id="64d07-138">String</span><span class="sxs-lookup"><span data-stu-id="64d07-138">String</span></span>|<span data-ttu-id="64d07-139">Categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="64d07-139">The categories associated with the message.</span></span>|
|<span data-ttu-id="64d07-140">importance</span><span class="sxs-lookup"><span data-stu-id="64d07-140">importance</span></span>|<span data-ttu-id="64d07-141">String</span><span class="sxs-lookup"><span data-stu-id="64d07-141">String</span></span>|<span data-ttu-id="64d07-142">La importancia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="64d07-142">The importance of the message.</span></span> <span data-ttu-id="64d07-143">Los valores posibles son: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="64d07-143">The possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="64d07-144">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="64d07-144">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="64d07-145">Booleano</span><span class="sxs-lookup"><span data-stu-id="64d07-145">Boolean</span></span>|<span data-ttu-id="64d07-146">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="64d07-146">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="64d07-147">isRead</span><span class="sxs-lookup"><span data-stu-id="64d07-147">isRead</span></span>|<span data-ttu-id="64d07-148">Booleano</span><span class="sxs-lookup"><span data-stu-id="64d07-148">Boolean</span></span>|<span data-ttu-id="64d07-149">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="64d07-149">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="64d07-150">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="64d07-150">isReadReceiptRequested</span></span>|<span data-ttu-id="64d07-151">Booleano</span><span class="sxs-lookup"><span data-stu-id="64d07-151">Boolean</span></span>|<span data-ttu-id="64d07-152">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="64d07-152">Indicates whether a read receipt is requested for the message.</span></span>|

## <a name="response"></a><span data-ttu-id="64d07-153">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64d07-153">Response</span></span>

<span data-ttu-id="64d07-154">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [eventMessage](../resources/eventmessage.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="64d07-154">If successful, this method returns a `200 OK` response code and updated [eventMessage](../resources/eventmessage.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="64d07-155">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="64d07-155">Example</span></span>
##### <a name="request"></a><span data-ttu-id="64d07-156">Solicitud</span><span class="sxs-lookup"><span data-stu-id="64d07-156">Request</span></span>
<span data-ttu-id="64d07-157">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="64d07-157">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="64d07-158">Respuesta</span><span class="sxs-lookup"><span data-stu-id="64d07-158">Response</span></span>
<span data-ttu-id="64d07-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="64d07-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
