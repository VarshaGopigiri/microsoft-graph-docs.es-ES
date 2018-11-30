---
title: Actualizar mensaje
description: Actualice las propiedades del objeto de mensaje.
ms.openlocfilehash: 0411decc2758505f6116b0a7c619887f3d8e239e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27091092"
---
# <a name="update-message"></a><span data-ttu-id="ce4b5-103">Actualizar mensaje</span><span class="sxs-lookup"><span data-stu-id="ce4b5-103">Update message</span></span>

> <span data-ttu-id="ce4b5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ce4b5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ce4b5-106">Actualice las propiedades del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-106">Update the properties of message object.</span></span>
## <a name="permissions"></a><span data-ttu-id="ce4b5-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="ce4b5-107">Permissions</span></span>
<span data-ttu-id="ce4b5-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ce4b5-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ce4b5-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ce4b5-110">Permission type</span></span>      | <span data-ttu-id="ce4b5-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ce4b5-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="ce4b5-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ce4b5-112">Delegated (work or school account)</span></span> | <span data-ttu-id="ce4b5-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ce4b5-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ce4b5-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ce4b5-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="ce4b5-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ce4b5-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="ce4b5-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ce4b5-116">Application</span></span> | <span data-ttu-id="ce4b5-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ce4b5-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="ce4b5-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ce4b5-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}
PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="ce4b5-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ce4b5-119">Request headers</span></span>
| <span data-ttu-id="ce4b5-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="ce4b5-120">Name</span></span>       | <span data-ttu-id="ce4b5-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce4b5-121">Type</span></span> | <span data-ttu-id="ce4b5-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce4b5-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="ce4b5-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="ce4b5-123">Authorization</span></span>  | <span data-ttu-id="ce4b5-124">string</span><span class="sxs-lookup"><span data-stu-id="ce4b5-124">string</span></span>  | <span data-ttu-id="ce4b5-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="ce4b5-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="ce4b5-127">Content-Type</span></span> | <span data-ttu-id="ce4b5-128">string</span><span class="sxs-lookup"><span data-stu-id="ce4b5-128">string</span></span>  | <span data-ttu-id="ce4b5-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-p104">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="ce4b5-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ce4b5-131">Request body</span></span>
<span data-ttu-id="ce4b5-p105">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado. Son propiedades Writable/Updatable</span><span class="sxs-lookup"><span data-stu-id="ce4b5-p105">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. Writable/Updatable properties are</span></span>

| <span data-ttu-id="ce4b5-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ce4b5-136">Property</span></span>     | <span data-ttu-id="ce4b5-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="ce4b5-137">Type</span></span>   |<span data-ttu-id="ce4b5-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce4b5-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ce4b5-139">bccRecipients</span><span class="sxs-lookup"><span data-stu-id="ce4b5-139">bccRecipients</span></span>|<span data-ttu-id="ce4b5-140">Recipient</span><span class="sxs-lookup"><span data-stu-id="ce4b5-140">Recipient</span></span>|<span data-ttu-id="ce4b5-141">Los destinatarios de CCO del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-141">The Bcc recipients for the message.</span></span> <span data-ttu-id="ce4b5-142">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-142">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="ce4b5-143">categories</span><span class="sxs-lookup"><span data-stu-id="ce4b5-143">categories</span></span>|<span data-ttu-id="ce4b5-144">Colección String</span><span class="sxs-lookup"><span data-stu-id="ce4b5-144">String collection</span></span>|<span data-ttu-id="ce4b5-145">Las categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-145">The categories associated with the message.</span></span>|
|<span data-ttu-id="ce4b5-146">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="ce4b5-146">ccRecipients</span></span>|<span data-ttu-id="ce4b5-147">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="ce4b5-147">Recipient collection</span></span>|<span data-ttu-id="ce4b5-148">Los destinatarios de Cc del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-148">The Cc recipients for the message.</span></span> <span data-ttu-id="ce4b5-149">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-149">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="ce4b5-150">from</span><span class="sxs-lookup"><span data-stu-id="ce4b5-150">from</span></span>|<span data-ttu-id="ce4b5-151">Recipient</span><span class="sxs-lookup"><span data-stu-id="ce4b5-151">Recipient</span></span>|<span data-ttu-id="ce4b5-152">El propietario del buzón y el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-152">The mailbox owner and sender of the message.</span></span> <span data-ttu-id="ce4b5-153">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-153">Updatable only if isDraft = true.</span></span> <span data-ttu-id="ce4b5-154">Debe corresponder con el buzón real que se usa.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-154">Must correspond to the actual mailbox used.</span></span> |
|<span data-ttu-id="ce4b5-155">importance</span><span class="sxs-lookup"><span data-stu-id="ce4b5-155">importance</span></span>|<span data-ttu-id="ce4b5-156">String</span><span class="sxs-lookup"><span data-stu-id="ce4b5-156">String</span></span>|<span data-ttu-id="ce4b5-p109">La importancia del mensaje. Los valores posibles son: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-p109">The importance of the message. Possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="ce4b5-159">inferenceClassification</span><span class="sxs-lookup"><span data-stu-id="ce4b5-159">inferenceClassification</span></span> | <span data-ttu-id="ce4b5-160">String</span><span class="sxs-lookup"><span data-stu-id="ce4b5-160">String</span></span> | <span data-ttu-id="ce4b5-p110">La clasificación del mensaje para el usuario, según relevancia inferida, importancia o según una invalidación explícita. Los valores posibles son: `focused` o `other`.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-p110">The classification of the message for the user, based on inferred relevance or importance, or on an explicit override. Possible values are: `focused` or `other`.</span></span> |
|<span data-ttu-id="ce4b5-163">internetMessageId</span><span class="sxs-lookup"><span data-stu-id="ce4b5-163">internetMessageId</span></span> |<span data-ttu-id="ce4b5-164">String</span><span class="sxs-lookup"><span data-stu-id="ce4b5-164">String</span></span> |<span data-ttu-id="ce4b5-165">El identificador del mensaje en el formato especificado por [RFC2822](https://www.ietf.org/rfc/rfc2822.txt).</span><span class="sxs-lookup"><span data-stu-id="ce4b5-165">The message ID in the format specified by [RFC2822](https://www.ietf.org/rfc/rfc2822.txt).</span></span> <span data-ttu-id="ce4b5-166">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-166">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="ce4b5-167">isRead</span><span class="sxs-lookup"><span data-stu-id="ce4b5-167">isRead</span></span>|<span data-ttu-id="ce4b5-168">Booleano</span><span class="sxs-lookup"><span data-stu-id="ce4b5-168">Boolean</span></span>|<span data-ttu-id="ce4b5-169">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-169">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="ce4b5-170">replyTo</span><span class="sxs-lookup"><span data-stu-id="ce4b5-170">replyTo</span></span>|<span data-ttu-id="ce4b5-171">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="ce4b5-171">Recipient collection</span></span>|<span data-ttu-id="ce4b5-172">Las direcciones de correo electrónico que se utilizan al responder.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-172">The email addresses to use when replying.</span></span> <span data-ttu-id="ce4b5-173">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-173">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="ce4b5-174">sender</span><span class="sxs-lookup"><span data-stu-id="ce4b5-174">sender</span></span>|<span data-ttu-id="ce4b5-175">Recipient</span><span class="sxs-lookup"><span data-stu-id="ce4b5-175">Recipient</span></span>|<span data-ttu-id="ce4b5-176">La cuenta que se utiliza realmente para generar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-176">The account that is actually used to generate the message.</span></span> <span data-ttu-id="ce4b5-177">Actualizable sólo si isDraft = true y cuándo enviar un mensaje desde un [buzón compartido](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes)o enviar un mensaje como un [delegado](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926).</span><span class="sxs-lookup"><span data-stu-id="ce4b5-177">Updatable only if isDraft = true, and when sending a message from a [shared mailbox](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes), or sending a message as a [delegate](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926).</span></span> <span data-ttu-id="ce4b5-178">En cualquier caso, el valor debe corresponder al buzón real que se usa.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-178">In any case, the value must correspond to the actual mailbox used.</span></span>|
|<span data-ttu-id="ce4b5-179">toRecipients</span><span class="sxs-lookup"><span data-stu-id="ce4b5-179">toRecipients</span></span>|<span data-ttu-id="ce4b5-180">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="ce4b5-180">Recipient collection</span></span>|<span data-ttu-id="ce4b5-181">Los destinatarios para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-181">The To recipients for the message.</span></span> <span data-ttu-id="ce4b5-182">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-182">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="ce4b5-183">body</span><span class="sxs-lookup"><span data-stu-id="ce4b5-183">body</span></span>|<span data-ttu-id="ce4b5-184">ItemBody</span><span class="sxs-lookup"><span data-stu-id="ce4b5-184">ItemBody</span></span>|<span data-ttu-id="ce4b5-185">El cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-185">The body of the message.</span></span> <span data-ttu-id="ce4b5-186">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-186">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="ce4b5-187">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="ce4b5-187">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="ce4b5-188">Booleano</span><span class="sxs-lookup"><span data-stu-id="ce4b5-188">Boolean</span></span>|<span data-ttu-id="ce4b5-189">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-189">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="ce4b5-190">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="ce4b5-190">isReadReceiptRequested</span></span>|<span data-ttu-id="ce4b5-191">Booleano</span><span class="sxs-lookup"><span data-stu-id="ce4b5-191">Boolean</span></span>|<span data-ttu-id="ce4b5-192">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-192">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="ce4b5-193">subject</span><span class="sxs-lookup"><span data-stu-id="ce4b5-193">subject</span></span>|<span data-ttu-id="ce4b5-194">String</span><span class="sxs-lookup"><span data-stu-id="ce4b5-194">String</span></span>|<span data-ttu-id="ce4b5-195">El asunto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-195">The subject of the message.</span></span> <span data-ttu-id="ce4b5-196">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-196">Updatable only if isDraft = true.</span></span>|

<span data-ttu-id="ce4b5-197">Dado que el recurso **message** admite [extensiones](/graph/extensibility-overview), puede utilizar la operación `PATCH` para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia **message** existente.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-197">Since the **message** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **message** instance.</span></span>

## <a name="response"></a><span data-ttu-id="ce4b5-198">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce4b5-198">Response</span></span>

<span data-ttu-id="ce4b5-199">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-199">If successful, this method returns a `200 OK` response code and updated [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="ce4b5-200">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ce4b5-200">Example</span></span>
##### <a name="request"></a><span data-ttu-id="ce4b5-201">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ce4b5-201">Request</span></span>
<span data-ttu-id="ce4b5-202">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-202">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "update_message"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/messages/{id}
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
##### <a name="response"></a><span data-ttu-id="ce4b5-203">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ce4b5-203">Response</span></span>
<span data-ttu-id="ce4b5-p117">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ce4b5-p117">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
  "receivedDateTime": "2016-10-19T10:37:00Z",
  "sentDateTime": "2016-10-19T10:37:00Z",
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

## <a name="see-also"></a><span data-ttu-id="ce4b5-207">Vea también</span><span class="sxs-lookup"><span data-stu-id="ce4b5-207">See also</span></span>

- [<span data-ttu-id="ce4b5-208">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="ce4b5-208">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="ce4b5-209">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="ce4b5-209">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="ce4b5-210">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="ce4b5-210">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
