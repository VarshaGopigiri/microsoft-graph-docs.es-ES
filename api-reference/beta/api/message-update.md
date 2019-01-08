---
title: Actualizar mensaje
description: Actualice las propiedades del objeto de mensaje.
author: angelgolfer-ms
ms.openlocfilehash: 04a52e28728eda7d778ac76cdc69080cd5b9edf5
ms.sourcegitcommit: 37591c2299c80e7675cd2b5f781e1eeeba628a60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27748545"
---
# <a name="update-message"></a><span data-ttu-id="6360f-103">Actualizar mensaje</span><span class="sxs-lookup"><span data-stu-id="6360f-103">Update message</span></span>

> <span data-ttu-id="6360f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6360f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6360f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6360f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6360f-106">Actualizar las propiedades de un objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-106">Update the properties of a message object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6360f-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="6360f-107">Permissions</span></span>
<span data-ttu-id="6360f-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="6360f-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="6360f-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6360f-110">Permission type</span></span>      | <span data-ttu-id="6360f-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6360f-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6360f-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6360f-112">Delegated (work or school account)</span></span> | <span data-ttu-id="6360f-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6360f-113">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6360f-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6360f-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6360f-115">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6360f-115">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6360f-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6360f-116">Application</span></span> | <span data-ttu-id="6360f-117">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6360f-117">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="6360f-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6360f-118">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}
PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="6360f-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6360f-119">Request headers</span></span>
| <span data-ttu-id="6360f-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="6360f-120">Name</span></span>       | <span data-ttu-id="6360f-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="6360f-121">Type</span></span> | <span data-ttu-id="6360f-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6360f-122">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6360f-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="6360f-123">Authorization</span></span>  | <span data-ttu-id="6360f-124">string</span><span class="sxs-lookup"><span data-stu-id="6360f-124">string</span></span>  | <span data-ttu-id="6360f-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6360f-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6360f-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6360f-127">Content-Type</span></span> | <span data-ttu-id="6360f-128">string</span><span class="sxs-lookup"><span data-stu-id="6360f-128">string</span></span>  | <span data-ttu-id="6360f-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6360f-p104">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="6360f-131">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6360f-131">Request body</span></span>
<span data-ttu-id="6360f-132">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse.</span><span class="sxs-lookup"><span data-stu-id="6360f-132">In the request body, supply the values for relevant fields that should be updated.</span></span> <span data-ttu-id="6360f-133">Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="6360f-133">Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values.</span></span> <span data-ttu-id="6360f-134">Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado.</span><span class="sxs-lookup"><span data-stu-id="6360f-134">For best performance you shouldn't include existing values that haven't changed.</span></span> <span data-ttu-id="6360f-135">Las siguientes propiedades se pueden actualizar.</span><span class="sxs-lookup"><span data-stu-id="6360f-135">The following properties can be updated.</span></span>

| <span data-ttu-id="6360f-136">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6360f-136">Property</span></span>     | <span data-ttu-id="6360f-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="6360f-137">Type</span></span>   |<span data-ttu-id="6360f-138">Descripción</span><span class="sxs-lookup"><span data-stu-id="6360f-138">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6360f-139">bccRecipients</span><span class="sxs-lookup"><span data-stu-id="6360f-139">bccRecipients</span></span>|<span data-ttu-id="6360f-140">Recipient</span><span class="sxs-lookup"><span data-stu-id="6360f-140">Recipient</span></span>|<span data-ttu-id="6360f-141">Los destinatarios de CCO del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-141">The Bcc recipients for the message.</span></span> |
|<span data-ttu-id="6360f-142">body</span><span class="sxs-lookup"><span data-stu-id="6360f-142">body</span></span>|<span data-ttu-id="6360f-143">ItemBody</span><span class="sxs-lookup"><span data-stu-id="6360f-143">ItemBody</span></span>|<span data-ttu-id="6360f-144">El cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-144">The body of the message.</span></span> <span data-ttu-id="6360f-145">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6360f-145">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="6360f-146">categories</span><span class="sxs-lookup"><span data-stu-id="6360f-146">categories</span></span>|<span data-ttu-id="6360f-147">Colección String</span><span class="sxs-lookup"><span data-stu-id="6360f-147">String collection</span></span>|<span data-ttu-id="6360f-148">Las categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-148">The categories associated with the message.</span></span>|
|<span data-ttu-id="6360f-149">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="6360f-149">ccRecipients</span></span>|<span data-ttu-id="6360f-150">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="6360f-150">Recipient collection</span></span>|<span data-ttu-id="6360f-151">Los destinatarios de Cc del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-151">The Cc recipients for the message.</span></span> |
|<span data-ttu-id="6360f-152">from</span><span class="sxs-lookup"><span data-stu-id="6360f-152">from</span></span>|<span data-ttu-id="6360f-153">Recipient</span><span class="sxs-lookup"><span data-stu-id="6360f-153">Recipient</span></span>|<span data-ttu-id="6360f-154">El propietario del buzón y el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-154">The mailbox owner and sender of the message.</span></span> <span data-ttu-id="6360f-155">Debe corresponder con el buzón real que se usa.</span><span class="sxs-lookup"><span data-stu-id="6360f-155">Must correspond to the actual mailbox used.</span></span> |
|<span data-ttu-id="6360f-156">importance</span><span class="sxs-lookup"><span data-stu-id="6360f-156">importance</span></span>|<span data-ttu-id="6360f-157">String</span><span class="sxs-lookup"><span data-stu-id="6360f-157">String</span></span>|<span data-ttu-id="6360f-p108">La importancia del mensaje. Los valores posibles son: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="6360f-p108">The importance of the message. Possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="6360f-160">inferenceClassification</span><span class="sxs-lookup"><span data-stu-id="6360f-160">inferenceClassification</span></span> | <span data-ttu-id="6360f-161">String</span><span class="sxs-lookup"><span data-stu-id="6360f-161">String</span></span> | <span data-ttu-id="6360f-p109">La clasificación del mensaje para el usuario, según relevancia inferida, importancia o según una invalidación explícita. Los valores posibles son: `focused` o `other`.</span><span class="sxs-lookup"><span data-stu-id="6360f-p109">The classification of the message for the user, based on inferred relevance or importance, or on an explicit override. Possible values are: `focused` or `other`.</span></span> |
|<span data-ttu-id="6360f-164">internetMessageId</span><span class="sxs-lookup"><span data-stu-id="6360f-164">internetMessageId</span></span> |<span data-ttu-id="6360f-165">String</span><span class="sxs-lookup"><span data-stu-id="6360f-165">String</span></span> |<span data-ttu-id="6360f-166">El identificador del mensaje en el formato especificado por [RFC2822](https://www.ietf.org/rfc/rfc2822.txt).</span><span class="sxs-lookup"><span data-stu-id="6360f-166">The message ID in the format specified by [RFC2822](https://www.ietf.org/rfc/rfc2822.txt).</span></span> <span data-ttu-id="6360f-167">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6360f-167">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="6360f-168">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="6360f-168">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="6360f-169">Booleano</span><span class="sxs-lookup"><span data-stu-id="6360f-169">Boolean</span></span>|<span data-ttu-id="6360f-170">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-170">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="6360f-171">isRead</span><span class="sxs-lookup"><span data-stu-id="6360f-171">isRead</span></span>|<span data-ttu-id="6360f-172">Booleano</span><span class="sxs-lookup"><span data-stu-id="6360f-172">Boolean</span></span>|<span data-ttu-id="6360f-173">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-173">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="6360f-174">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="6360f-174">isReadReceiptRequested</span></span>|<span data-ttu-id="6360f-175">Booleano</span><span class="sxs-lookup"><span data-stu-id="6360f-175">Boolean</span></span>|<span data-ttu-id="6360f-176">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-176">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="6360f-177">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="6360f-177">multiValueExtendedProperties</span></span>|<span data-ttu-id="6360f-178">Colección [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="6360f-178">[multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="6360f-179">La colección de propiedades extendidas de varios valores definidos para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-179">The collection of multi-value extended properties defined for the message.</span></span> <span data-ttu-id="6360f-180">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6360f-180">Nullable.</span></span>|
|<span data-ttu-id="6360f-181">replyTo</span><span class="sxs-lookup"><span data-stu-id="6360f-181">replyTo</span></span>|<span data-ttu-id="6360f-182">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="6360f-182">Recipient collection</span></span>|<span data-ttu-id="6360f-183">Las direcciones de correo electrónico que se utilizan al responder.</span><span class="sxs-lookup"><span data-stu-id="6360f-183">The email addresses to use when replying.</span></span> <span data-ttu-id="6360f-184">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6360f-184">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="6360f-185">sender</span><span class="sxs-lookup"><span data-stu-id="6360f-185">sender</span></span>|<span data-ttu-id="6360f-186">Recipient</span><span class="sxs-lookup"><span data-stu-id="6360f-186">Recipient</span></span>|<span data-ttu-id="6360f-187">La cuenta que se utiliza realmente para generar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-187">The account that is actually used to generate the message.</span></span> <span data-ttu-id="6360f-188">Actualizable cuando se envía un mensaje desde un [buzón compartido](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes)o enviar un mensaje como un [delegado](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926).</span><span class="sxs-lookup"><span data-stu-id="6360f-188">Updatable when sending a message from a [shared mailbox](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes), or sending a message as a [delegate](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926).</span></span> <span data-ttu-id="6360f-189">En cualquier caso, el valor debe corresponder al buzón real que se usa.</span><span class="sxs-lookup"><span data-stu-id="6360f-189">In any case, the value must correspond to the actual mailbox used.</span></span>|
|<span data-ttu-id="6360f-190">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="6360f-190">singleValueExtendedProperties</span></span>|<span data-ttu-id="6360f-191">Colección [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="6360f-191">[singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="6360f-192">La colección de propiedades extendidas de valor único definido para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-192">The collection of single-value extended properties defined for the message.</span></span> <span data-ttu-id="6360f-193">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6360f-193">Nullable.</span></span>|
|<span data-ttu-id="6360f-194">subject</span><span class="sxs-lookup"><span data-stu-id="6360f-194">subject</span></span>|<span data-ttu-id="6360f-195">String</span><span class="sxs-lookup"><span data-stu-id="6360f-195">String</span></span>|<span data-ttu-id="6360f-196">El asunto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-196">The subject of the message.</span></span> <span data-ttu-id="6360f-197">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6360f-197">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="6360f-198">toRecipients</span><span class="sxs-lookup"><span data-stu-id="6360f-198">toRecipients</span></span>|<span data-ttu-id="6360f-199">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="6360f-199">Recipient collection</span></span>|<span data-ttu-id="6360f-200">Los destinatarios para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6360f-200">The To recipients for the message.</span></span> |

<span data-ttu-id="6360f-201">Dado que el recurso **message** admite [extensiones](/graph/extensibility-overview), puede utilizar la operación `PATCH` para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia **message** existente.</span><span class="sxs-lookup"><span data-stu-id="6360f-201">Since the **message** resource supports [extensions](/graph/extensibility-overview), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **message** instance.</span></span>

## <a name="response"></a><span data-ttu-id="6360f-202">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6360f-202">Response</span></span>

<span data-ttu-id="6360f-203">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6360f-203">If successful, this method returns a `200 OK` response code and updated [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6360f-204">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6360f-204">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6360f-205">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6360f-205">Request</span></span>
<span data-ttu-id="6360f-206">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6360f-206">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="6360f-207">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6360f-207">Response</span></span>
<span data-ttu-id="6360f-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6360f-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="6360f-211">Vea también</span><span class="sxs-lookup"><span data-stu-id="6360f-211">See also</span></span>

- [<span data-ttu-id="6360f-212">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="6360f-212">Add custom data to resources using extensions</span></span>](/graph/extensibility-overview)
- [<span data-ttu-id="6360f-213">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="6360f-213">Add custom data to users using open extensions (preview)</span></span>](/graph/extensibility-open-users)
- [<span data-ttu-id="6360f-214">Agregar datos personalizados a grupos mediante extensiones de esquema (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="6360f-214">Add custom data to groups using schema extensions (preview)</span></span>](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update message",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
