---
title: Actualizar mensaje
description: Actualice las propiedades del objeto de mensaje.
author: angelgolfer-ms
localization_priority: Priority
ms.openlocfilehash: 24705fbf986f9ecf1142e66d189ae2071e1be223
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27884787"
---
# <a name="update-message"></a><span data-ttu-id="e4df9-103">Actualizar mensaje</span><span class="sxs-lookup"><span data-stu-id="e4df9-103">Update message</span></span>

<span data-ttu-id="e4df9-104">Actualizar las propiedades de un objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-104">Update the properties of a message object.</span></span>
## <a name="permissions"></a><span data-ttu-id="e4df9-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="e4df9-105">Permissions</span></span>
<span data-ttu-id="e4df9-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e4df9-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e4df9-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e4df9-108">Permission type</span></span>      | <span data-ttu-id="e4df9-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e4df9-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="e4df9-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e4df9-110">Delegated (work or school account)</span></span> | <span data-ttu-id="e4df9-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4df9-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="e4df9-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e4df9-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="e4df9-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4df9-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="e4df9-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e4df9-114">Application</span></span> | <span data-ttu-id="e4df9-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="e4df9-115">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="e4df9-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e4df9-116">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}
PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="e4df9-117">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e4df9-117">Request headers</span></span>
| <span data-ttu-id="e4df9-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="e4df9-118">Name</span></span>       | <span data-ttu-id="e4df9-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4df9-119">Type</span></span> | <span data-ttu-id="e4df9-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4df9-120">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="e4df9-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="e4df9-121">Authorization</span></span>  | <span data-ttu-id="e4df9-122">string</span><span class="sxs-lookup"><span data-stu-id="e4df9-122">string</span></span>  | <span data-ttu-id="e4df9-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e4df9-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="e4df9-125">Content-Type</span><span class="sxs-lookup"><span data-stu-id="e4df9-125">Content-Type</span></span> | <span data-ttu-id="e4df9-126">string</span><span class="sxs-lookup"><span data-stu-id="e4df9-126">string</span></span>  | <span data-ttu-id="e4df9-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="e4df9-p103">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="e4df9-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e4df9-129">Request body</span></span>
<span data-ttu-id="e4df9-130">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="e4df9-130">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="e4df9-131">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="e4df9-131">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="e4df9-132">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="e4df9-132">For best performance you shouldn't include existing values that haven't changed.</span></span> <span data-ttu-id="e4df9-133">Las siguientes propiedades se pueden actualizar.</span><span class="sxs-lookup"><span data-stu-id="e4df9-133">The following properties can be updated.</span></span>

| <span data-ttu-id="e4df9-134">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e4df9-134">Property</span></span>     | <span data-ttu-id="e4df9-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="e4df9-135">Type</span></span>   |<span data-ttu-id="e4df9-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="e4df9-136">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e4df9-137">bccRecipients</span><span class="sxs-lookup"><span data-stu-id="e4df9-137">bccRecipients</span></span>|<span data-ttu-id="e4df9-138">Recipient</span><span class="sxs-lookup"><span data-stu-id="e4df9-138">Recipient</span></span>|<span data-ttu-id="e4df9-139">Los destinatarios de CCO del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-139">The Bcc recipients for the message.</span></span> |
|<span data-ttu-id="e4df9-140">body</span><span class="sxs-lookup"><span data-stu-id="e4df9-140">body</span></span>|<span data-ttu-id="e4df9-141">ItemBody</span><span class="sxs-lookup"><span data-stu-id="e4df9-141">ItemBody</span></span>|<span data-ttu-id="e4df9-142">El cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-142">The body of the message.</span></span> <span data-ttu-id="e4df9-143">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="e4df9-143">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="e4df9-144">categories</span><span class="sxs-lookup"><span data-stu-id="e4df9-144">categories</span></span>|<span data-ttu-id="e4df9-145">Colección String</span><span class="sxs-lookup"><span data-stu-id="e4df9-145">String collection</span></span>|<span data-ttu-id="e4df9-146">Las categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-146">The categories associated with the message.</span></span>|
|<span data-ttu-id="e4df9-147">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="e4df9-147">ccRecipients</span></span>|<span data-ttu-id="e4df9-148">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="e4df9-148">Recipient collection</span></span>|<span data-ttu-id="e4df9-149">Los destinatarios de Cc del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-149">The Cc recipients for the message.</span></span> |
|<span data-ttu-id="e4df9-150">from</span><span class="sxs-lookup"><span data-stu-id="e4df9-150">from</span></span>|<span data-ttu-id="e4df9-151">Recipient</span><span class="sxs-lookup"><span data-stu-id="e4df9-151">Recipient</span></span>|<span data-ttu-id="e4df9-152">El propietario del buzón y el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-152">The mailbox owner and sender of the message.</span></span> <span data-ttu-id="e4df9-153">Debe corresponder con el buzón real que se usa.</span><span class="sxs-lookup"><span data-stu-id="e4df9-153">Must correspond to the actual mailbox used.</span></span>|
|<span data-ttu-id="e4df9-154">importance</span><span class="sxs-lookup"><span data-stu-id="e4df9-154">importance</span></span>|<span data-ttu-id="e4df9-155">Cadena</span><span class="sxs-lookup"><span data-stu-id="e4df9-155">String</span></span>|<span data-ttu-id="e4df9-156">La importancia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-156">The importance of the message.</span></span> <span data-ttu-id="e4df9-157">Los valores posibles son: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="e4df9-157">The possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="e4df9-158">inferenceClassification</span><span class="sxs-lookup"><span data-stu-id="e4df9-158">inferenceClassification</span></span> | <span data-ttu-id="e4df9-159">Cadena</span><span class="sxs-lookup"><span data-stu-id="e4df9-159">String</span></span> | <span data-ttu-id="e4df9-160">La clasificación del mensaje para el usuario, basándose en la relevancia inferida o importancia, o en un reemplazo explícito.</span><span class="sxs-lookup"><span data-stu-id="e4df9-160">The classification of the message for the user, based on inferred relevance or importance, or on an explicit override.</span></span> <span data-ttu-id="e4df9-161">Los valores posibles son: `focused` o `other`.</span><span class="sxs-lookup"><span data-stu-id="e4df9-161">The possible values are: `focused` or `other`.</span></span> |
|<span data-ttu-id="e4df9-162">internetMessageId</span><span class="sxs-lookup"><span data-stu-id="e4df9-162">internetMessageId</span></span> |<span data-ttu-id="e4df9-163">String</span><span class="sxs-lookup"><span data-stu-id="e4df9-163">String</span></span> |<span data-ttu-id="e4df9-164">El identificador del mensaje en el formato especificado por [RFC2822](https://www.ietf.org/rfc/rfc2822.txt).</span><span class="sxs-lookup"><span data-stu-id="e4df9-164">The message ID in the format specified by [RFC2822](https://www.ietf.org/rfc/rfc2822.txt).</span></span> <span data-ttu-id="e4df9-165">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="e4df9-165">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="e4df9-166">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="e4df9-166">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="e4df9-167">Booleano</span><span class="sxs-lookup"><span data-stu-id="e4df9-167">Boolean</span></span>|<span data-ttu-id="e4df9-168">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-168">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="e4df9-169">isRead</span><span class="sxs-lookup"><span data-stu-id="e4df9-169">isRead</span></span>|<span data-ttu-id="e4df9-170">Booleano</span><span class="sxs-lookup"><span data-stu-id="e4df9-170">Boolean</span></span>|<span data-ttu-id="e4df9-171">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-171">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="e4df9-172">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="e4df9-172">isReadReceiptRequested</span></span>|<span data-ttu-id="e4df9-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="e4df9-173">Boolean</span></span>|<span data-ttu-id="e4df9-174">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-174">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="e4df9-175">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="e4df9-175">multiValueExtendedProperties</span></span>|<span data-ttu-id="e4df9-176">Colección [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="e4df9-176">[multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="e4df9-177">La colección de propiedades extendidas de varios valores definidos para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-177">The collection of multi-value extended properties defined for the message.</span></span> <span data-ttu-id="e4df9-178">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="e4df9-178">Nullable.</span></span>|
|<span data-ttu-id="e4df9-179">replyTo</span><span class="sxs-lookup"><span data-stu-id="e4df9-179">replyTo</span></span>|<span data-ttu-id="e4df9-180">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="e4df9-180">Recipient collection</span></span>|<span data-ttu-id="e4df9-181">Las direcciones de correo electrónico que se utilizan al responder.</span><span class="sxs-lookup"><span data-stu-id="e4df9-181">The email addresses to use when replying.</span></span> <span data-ttu-id="e4df9-182">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="e4df9-182">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="e4df9-183">sender</span><span class="sxs-lookup"><span data-stu-id="e4df9-183">sender</span></span>|<span data-ttu-id="e4df9-184">Recipient</span><span class="sxs-lookup"><span data-stu-id="e4df9-184">Recipient</span></span>|<span data-ttu-id="e4df9-185">La cuenta que se utiliza realmente para generar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-185">The account that is actually used to generate the message.</span></span> <span data-ttu-id="e4df9-186">Actualizable cuando se envía un mensaje desde un [buzón compartido](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes)o enviar un mensaje como un [delegado](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926).</span><span class="sxs-lookup"><span data-stu-id="e4df9-186">Updatable when sending a message from a [shared mailbox](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes), or sending a message as a [delegate](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926).</span></span> <span data-ttu-id="e4df9-187">En cualquier caso, el valor debe corresponder al buzón real que se usa.</span><span class="sxs-lookup"><span data-stu-id="e4df9-187">In any case, the value must correspond to the actual mailbox used.</span></span>|
|<span data-ttu-id="e4df9-188">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="e4df9-188">singleValueExtendedProperties</span></span>|<span data-ttu-id="e4df9-189">Colección [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="e4df9-189">[singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="e4df9-190">La colección de propiedades extendidas de valor único definido para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-190">The collection of single-value extended properties defined for the message.</span></span> <span data-ttu-id="e4df9-191">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="e4df9-191">Nullable.</span></span>|
|<span data-ttu-id="e4df9-192">subject</span><span class="sxs-lookup"><span data-stu-id="e4df9-192">subject</span></span>|<span data-ttu-id="e4df9-193">Cadena</span><span class="sxs-lookup"><span data-stu-id="e4df9-193">String</span></span>|<span data-ttu-id="e4df9-194">El asunto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-194">The subject of the message.</span></span> <span data-ttu-id="e4df9-195">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="e4df9-195">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="e4df9-196">toRecipients</span><span class="sxs-lookup"><span data-stu-id="e4df9-196">toRecipients</span></span>|<span data-ttu-id="e4df9-197">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="e4df9-197">Recipient collection</span></span>|<span data-ttu-id="e4df9-198">Los destinatarios para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="e4df9-198">The To recipients for the message.</span></span>|

<span data-ttu-id="e4df9-199">Dado que el recurso **message** admite [extensiones](/graph/extensibility-overview), puede utilizar la operación `PATCH` para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia **message** existente.</span><span class="sxs-lookup"><span data-stu-id="e4df9-199">Since the **message** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **message** instance.</span></span>

## <a name="response"></a><span data-ttu-id="e4df9-200">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4df9-200">Response</span></span>

<span data-ttu-id="e4df9-201">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e4df9-201">If successful, this method returns a `200 OK` response code and updated [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="e4df9-202">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e4df9-202">Example</span></span>
##### <a name="request"></a><span data-ttu-id="e4df9-203">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e4df9-203">Request</span></span>
<span data-ttu-id="e4df9-204">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e4df9-204">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="e4df9-205">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e4df9-205">Response</span></span>
<span data-ttu-id="e4df9-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e4df9-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="e4df9-209">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4df9-209">See also</span></span>

- [<span data-ttu-id="e4df9-210">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="e4df9-210">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="e4df9-211">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="e4df9-211">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
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
