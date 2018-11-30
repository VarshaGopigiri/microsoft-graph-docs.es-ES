---
title: Actualizar mensaje
description: Actualice las propiedades del objeto de mensaje.
ms.openlocfilehash: 7d78f3827618378299043c601fcf490556b5d5b4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029142"
---
# <a name="update-message"></a><span data-ttu-id="fd4b8-103">Actualizar mensaje</span><span class="sxs-lookup"><span data-stu-id="fd4b8-103">Update message</span></span>

<span data-ttu-id="fd4b8-104">Actualice las propiedades del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-104">Update the properties of message object.</span></span>
## <a name="permissions"></a><span data-ttu-id="fd4b8-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="fd4b8-105">Permissions</span></span>
<span data-ttu-id="fd4b8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="fd4b8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="fd4b8-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="fd4b8-108">Permission type</span></span>      | <span data-ttu-id="fd4b8-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="fd4b8-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="fd4b8-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="fd4b8-110">Delegated (work or school account)</span></span> | <span data-ttu-id="fd4b8-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fd4b8-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="fd4b8-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="fd4b8-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="fd4b8-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fd4b8-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="fd4b8-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="fd4b8-114">Application</span></span> | <span data-ttu-id="fd4b8-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fd4b8-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="fd4b8-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="fd4b8-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}
PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="fd4b8-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="fd4b8-117">Request headers</span></span>
| <span data-ttu-id="fd4b8-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="fd4b8-118">Name</span></span>       | <span data-ttu-id="fd4b8-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd4b8-119">Type</span></span> | <span data-ttu-id="fd4b8-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd4b8-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="fd4b8-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="fd4b8-121">Authorization</span></span>  | <span data-ttu-id="fd4b8-122">string</span><span class="sxs-lookup"><span data-stu-id="fd4b8-122">string</span></span>  | <span data-ttu-id="fd4b8-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="fd4b8-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="fd4b8-125">Content-Type</span></span> | <span data-ttu-id="fd4b8-126">string</span><span class="sxs-lookup"><span data-stu-id="fd4b8-126">string</span></span>  | <span data-ttu-id="fd4b8-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-p103">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="fd4b8-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="fd4b8-129">Request body</span></span>
<span data-ttu-id="fd4b8-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado. Son propiedades Writable/Updatable</span><span class="sxs-lookup"><span data-stu-id="fd4b8-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. Writable/Updatable properties are</span></span>

| <span data-ttu-id="fd4b8-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fd4b8-134">Property</span></span>     | <span data-ttu-id="fd4b8-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd4b8-135">Type</span></span>   |<span data-ttu-id="fd4b8-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd4b8-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fd4b8-137">bccRecipients</span><span class="sxs-lookup"><span data-stu-id="fd4b8-137">bccRecipients</span></span>|<span data-ttu-id="fd4b8-138">Recipient</span><span class="sxs-lookup"><span data-stu-id="fd4b8-138">Recipient</span></span>|<span data-ttu-id="fd4b8-139">Los destinatarios de CCO del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-139">The Bcc recipients for the message.</span></span> <span data-ttu-id="fd4b8-140">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-140">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="fd4b8-141">categories</span><span class="sxs-lookup"><span data-stu-id="fd4b8-141">categories</span></span>|<span data-ttu-id="fd4b8-142">Colección String</span><span class="sxs-lookup"><span data-stu-id="fd4b8-142">String collection</span></span>|<span data-ttu-id="fd4b8-143">Las categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-143">The categories associated with the message.</span></span>|
|<span data-ttu-id="fd4b8-144">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="fd4b8-144">ccRecipients</span></span>|<span data-ttu-id="fd4b8-145">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="fd4b8-145">Recipient collection</span></span>|<span data-ttu-id="fd4b8-146">Los destinatarios de Cc del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-146">The Cc recipients for the message.</span></span> <span data-ttu-id="fd4b8-147">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-147">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="fd4b8-148">from</span><span class="sxs-lookup"><span data-stu-id="fd4b8-148">from</span></span>|<span data-ttu-id="fd4b8-149">Recipient</span><span class="sxs-lookup"><span data-stu-id="fd4b8-149">Recipient</span></span>|<span data-ttu-id="fd4b8-150">El propietario del buzón y el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-150">The mailbox owner and sender of the message.</span></span> <span data-ttu-id="fd4b8-151">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-151">Updatable only if isDraft = true.</span></span> <span data-ttu-id="fd4b8-152">Debe corresponder con el buzón real que se usa.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-152">Must correspond to the actual mailbox used.</span></span>|
|<span data-ttu-id="fd4b8-153">importance</span><span class="sxs-lookup"><span data-stu-id="fd4b8-153">importance</span></span>|<span data-ttu-id="fd4b8-154">String</span><span class="sxs-lookup"><span data-stu-id="fd4b8-154">String</span></span>|<span data-ttu-id="fd4b8-155">La importancia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-155">The importance of the message.</span></span> <span data-ttu-id="fd4b8-156">Los valores posibles son: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-156">The possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="fd4b8-157">inferenceClassification</span><span class="sxs-lookup"><span data-stu-id="fd4b8-157">inferenceClassification</span></span> | <span data-ttu-id="fd4b8-158">String</span><span class="sxs-lookup"><span data-stu-id="fd4b8-158">String</span></span> | <span data-ttu-id="fd4b8-159">La clasificación del mensaje para el usuario, basándose en la relevancia inferida o importancia, o en un reemplazo explícito.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-159">The classification of the message for the user, based on inferred relevance or importance, or on an explicit override.</span></span> <span data-ttu-id="fd4b8-160">Los valores posibles son: `focused` o `other`.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-160">The possible values are: `focused` or `other`.</span></span> |
|<span data-ttu-id="fd4b8-161">internetMessageId</span><span class="sxs-lookup"><span data-stu-id="fd4b8-161">internetMessageId</span></span> |<span data-ttu-id="fd4b8-162">String</span><span class="sxs-lookup"><span data-stu-id="fd4b8-162">String</span></span> |<span data-ttu-id="fd4b8-163">El identificador del mensaje en el formato especificado por [RFC2822](https://www.ietf.org/rfc/rfc2822.txt).</span><span class="sxs-lookup"><span data-stu-id="fd4b8-163">The message ID in the format specified by [RFC2822](https://www.ietf.org/rfc/rfc2822.txt).</span></span> <span data-ttu-id="fd4b8-164">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-164">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="fd4b8-165">isRead</span><span class="sxs-lookup"><span data-stu-id="fd4b8-165">isRead</span></span>|<span data-ttu-id="fd4b8-166">Booleano</span><span class="sxs-lookup"><span data-stu-id="fd4b8-166">Boolean</span></span>|<span data-ttu-id="fd4b8-167">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-167">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="fd4b8-168">replyTo</span><span class="sxs-lookup"><span data-stu-id="fd4b8-168">replyTo</span></span>|<span data-ttu-id="fd4b8-169">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="fd4b8-169">Recipient collection</span></span>|<span data-ttu-id="fd4b8-170">Las direcciones de correo electrónico que se utilizan al responder.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-170">The email addresses to use when replying.</span></span> <span data-ttu-id="fd4b8-171">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-171">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="fd4b8-172">sender</span><span class="sxs-lookup"><span data-stu-id="fd4b8-172">sender</span></span>|<span data-ttu-id="fd4b8-173">Recipient</span><span class="sxs-lookup"><span data-stu-id="fd4b8-173">Recipient</span></span>|<span data-ttu-id="fd4b8-174">La cuenta que se utiliza realmente para generar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-174">The account that is actually used to generate the message.</span></span> <span data-ttu-id="fd4b8-175">Actualizable sólo si isDraft = true y cuándo enviar un mensaje desde un [buzón compartido](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes)o enviar un mensaje como un [delegado](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926).</span><span class="sxs-lookup"><span data-stu-id="fd4b8-175">Updatable only if isDraft = true, and when sending a message from a [shared mailbox](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes), or sending a message as a [delegate](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926).</span></span> <span data-ttu-id="fd4b8-176">En cualquier caso, el valor debe corresponder al buzón real que se usa.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-176">In any case, the value must correspond to the actual mailbox used.</span></span>|
|<span data-ttu-id="fd4b8-177">toRecipients</span><span class="sxs-lookup"><span data-stu-id="fd4b8-177">toRecipients</span></span>|<span data-ttu-id="fd4b8-178">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="fd4b8-178">Recipient collection</span></span>|<span data-ttu-id="fd4b8-179">Los destinatarios para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-179">The To recipients for the message.</span></span> <span data-ttu-id="fd4b8-180">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-180">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="fd4b8-181">body</span><span class="sxs-lookup"><span data-stu-id="fd4b8-181">body</span></span>|<span data-ttu-id="fd4b8-182">ItemBody</span><span class="sxs-lookup"><span data-stu-id="fd4b8-182">ItemBody</span></span>|<span data-ttu-id="fd4b8-183">El cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-183">The body of the message.</span></span> <span data-ttu-id="fd4b8-184">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-184">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="fd4b8-185">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="fd4b8-185">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="fd4b8-186">Booleano</span><span class="sxs-lookup"><span data-stu-id="fd4b8-186">Boolean</span></span>|<span data-ttu-id="fd4b8-187">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-187">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="fd4b8-188">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="fd4b8-188">isReadReceiptRequested</span></span>|<span data-ttu-id="fd4b8-189">Booleano</span><span class="sxs-lookup"><span data-stu-id="fd4b8-189">Boolean</span></span>|<span data-ttu-id="fd4b8-190">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-190">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="fd4b8-191">subject</span><span class="sxs-lookup"><span data-stu-id="fd4b8-191">subject</span></span>|<span data-ttu-id="fd4b8-192">String</span><span class="sxs-lookup"><span data-stu-id="fd4b8-192">String</span></span>|<span data-ttu-id="fd4b8-193">El asunto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-193">The subject of the message.</span></span> <span data-ttu-id="fd4b8-194">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-194">Updatable only if isDraft = true.</span></span>|

<span data-ttu-id="fd4b8-195">Dado que el recurso **message** admite [extensiones](/graph/extensibility-overview), puede utilizar la operación `PATCH` para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia **message** existente.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-195">Since the **message** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **message** instance.</span></span>

## <a name="response"></a><span data-ttu-id="fd4b8-196">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd4b8-196">Response</span></span>

<span data-ttu-id="fd4b8-197">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-197">If successful, this method returns a `200 OK` response code and updated [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="fd4b8-198">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="fd4b8-198">Example</span></span>
##### <a name="request"></a><span data-ttu-id="fd4b8-199">Solicitud</span><span class="sxs-lookup"><span data-stu-id="fd4b8-199">Request</span></span>
<span data-ttu-id="fd4b8-200">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-200">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_message"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages/{id}
Content-type: application/json
Content-length: 248

{
  "subject": "subject-value",
  "body": {
    "contentType": "",
    "content": "content-value"
  },
  "inferenceClassification": "other"
}
```
##### <a name="response"></a><span data-ttu-id="fd4b8-201">Respuesta</span><span class="sxs-lookup"><span data-stu-id="fd4b8-201">Response</span></span>
<span data-ttu-id="fd4b8-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="fd4b8-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.message"
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
  "inferenceClassification": "other"
}
```

## <a name="see-also"></a><span data-ttu-id="fd4b8-205">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd4b8-205">See also</span></span>

- [<span data-ttu-id="fd4b8-206">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="fd4b8-206">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="fd4b8-207">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="fd4b8-207">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
