# <a name="update-message"></a><span data-ttu-id="99a4c-101">Actualizar mensaje</span><span class="sxs-lookup"><span data-stu-id="99a4c-101">Update message</span></span>

<span data-ttu-id="99a4c-102">Actualice las propiedades del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-102">Update the properties of message object.</span></span>
## <a name="permissions"></a><span data-ttu-id="99a4c-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="99a4c-103">Permissions</span></span>
<span data-ttu-id="99a4c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="99a4c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="99a4c-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="99a4c-106">Permission type</span></span>      | <span data-ttu-id="99a4c-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="99a4c-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="99a4c-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="99a4c-108">Delegated (work or school account)</span></span> | <span data-ttu-id="99a4c-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="99a4c-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="99a4c-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="99a4c-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="99a4c-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="99a4c-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="99a4c-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="99a4c-112">Application</span></span> | <span data-ttu-id="99a4c-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="99a4c-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="99a4c-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="99a4c-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}
PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="99a4c-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="99a4c-115">Request headers</span></span>
| <span data-ttu-id="99a4c-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="99a4c-116">Name</span></span>       | <span data-ttu-id="99a4c-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="99a4c-117">Type</span></span> | <span data-ttu-id="99a4c-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="99a4c-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="99a4c-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="99a4c-119">Authorization</span></span>  | <span data-ttu-id="99a4c-120">string</span><span class="sxs-lookup"><span data-stu-id="99a4c-120">string</span></span>  | <span data-ttu-id="99a4c-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="99a4c-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="99a4c-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="99a4c-123">Content-Type</span></span> | <span data-ttu-id="99a4c-124">string</span><span class="sxs-lookup"><span data-stu-id="99a4c-124">string</span></span>  | <span data-ttu-id="99a4c-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="99a4c-p103">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="99a4c-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="99a4c-127">Request body</span></span>
<span data-ttu-id="99a4c-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado. Son propiedades Writable/Updatable</span><span class="sxs-lookup"><span data-stu-id="99a4c-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. Writable/Updatable properties are</span></span>

| <span data-ttu-id="99a4c-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="99a4c-132">Property</span></span>     | <span data-ttu-id="99a4c-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="99a4c-133">Type</span></span>   |<span data-ttu-id="99a4c-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="99a4c-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="99a4c-135">bccRecipients</span><span class="sxs-lookup"><span data-stu-id="99a4c-135">bccRecipients</span></span>|<span data-ttu-id="99a4c-136">Recipient</span><span class="sxs-lookup"><span data-stu-id="99a4c-136">Recipient</span></span>|<span data-ttu-id="99a4c-137">Los destinatarios de CCO del mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-137">The Bcc recipients for the message.</span></span> <span data-ttu-id="99a4c-138">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="99a4c-138">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="99a4c-139">categories</span><span class="sxs-lookup"><span data-stu-id="99a4c-139">categories</span></span>|<span data-ttu-id="99a4c-140">Colección String</span><span class="sxs-lookup"><span data-stu-id="99a4c-140">String collection</span></span>|<span data-ttu-id="99a4c-141">Las categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-141">The categories associated with the message.</span></span>|
|<span data-ttu-id="99a4c-142">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="99a4c-142">ccRecipients</span></span>|<span data-ttu-id="99a4c-143">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="99a4c-143">Recipient collection</span></span>|<span data-ttu-id="99a4c-144">Los destinatarios de Cc del mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-144">The Cc recipients for the message.</span></span> <span data-ttu-id="99a4c-145">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="99a4c-145">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="99a4c-146">from</span><span class="sxs-lookup"><span data-stu-id="99a4c-146">from</span></span>|<span data-ttu-id="99a4c-147">Recipient</span><span class="sxs-lookup"><span data-stu-id="99a4c-147">Recipient</span></span>|<span data-ttu-id="99a4c-148">El propietario del buzón y el remitente del mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-148">The mailbox owner and sender of the message.</span></span> <span data-ttu-id="99a4c-149">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="99a4c-149">Updatable only if isDraft = true.</span></span> <span data-ttu-id="99a4c-150">Debe corresponder con el buzón real que se usa.</span><span class="sxs-lookup"><span data-stu-id="99a4c-150">Must correspond to the actual mailbox used.</span></span>|
|<span data-ttu-id="99a4c-151">importance</span><span class="sxs-lookup"><span data-stu-id="99a4c-151">importance</span></span>|<span data-ttu-id="99a4c-152">String</span><span class="sxs-lookup"><span data-stu-id="99a4c-152">String</span></span>|<span data-ttu-id="99a4c-153">La importancia del mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-153">The importance of the message.</span></span> <span data-ttu-id="99a4c-154">Los valores posibles son: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="99a4c-154">The possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="99a4c-155">inferenceClassification</span><span class="sxs-lookup"><span data-stu-id="99a4c-155">inferenceClassification</span></span> | <span data-ttu-id="99a4c-156">String</span><span class="sxs-lookup"><span data-stu-id="99a4c-156">String</span></span> | <span data-ttu-id="99a4c-157">La clasificación del mensaje para el usuario, basándose en la relevancia inferida o importancia, o en un reemplazo explícito.</span><span class="sxs-lookup"><span data-stu-id="99a4c-157">The classification of the message for the user, based on inferred relevance or importance, or on an explicit override.</span></span> <span data-ttu-id="99a4c-158">Los valores posibles son: `focused` o `other`.</span><span class="sxs-lookup"><span data-stu-id="99a4c-158">The possible values are: `focused` or `other`.</span></span> |
|<span data-ttu-id="99a4c-159">internetMessageId</span><span class="sxs-lookup"><span data-stu-id="99a4c-159">internetMessageId</span></span> |<span data-ttu-id="99a4c-160">String</span><span class="sxs-lookup"><span data-stu-id="99a4c-160">String</span></span> |<span data-ttu-id="99a4c-161">El identificador del mensaje en el formato especificado por [RFC2822](https://www.ietf.org/rfc/rfc2822.txt).</span><span class="sxs-lookup"><span data-stu-id="99a4c-161">The message ID in the format specified by [RFC2822](https://www.ietf.org/rfc/rfc2822.txt).</span></span> <span data-ttu-id="99a4c-162">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="99a4c-162">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="99a4c-163">isRead</span><span class="sxs-lookup"><span data-stu-id="99a4c-163">isRead</span></span>|<span data-ttu-id="99a4c-164">Booleano</span><span class="sxs-lookup"><span data-stu-id="99a4c-164">Boolean</span></span>|<span data-ttu-id="99a4c-165">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-165">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="99a4c-166">replyTo</span><span class="sxs-lookup"><span data-stu-id="99a4c-166">replyTo</span></span>|<span data-ttu-id="99a4c-167">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="99a4c-167">Recipient collection</span></span>|<span data-ttu-id="99a4c-168">Las direcciones de correo electrónico que se utilizan al responder.</span><span class="sxs-lookup"><span data-stu-id="99a4c-168">The email addresses to use when replying.</span></span> <span data-ttu-id="99a4c-169">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="99a4c-169">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="99a4c-170">sender</span><span class="sxs-lookup"><span data-stu-id="99a4c-170">sender</span></span>|<span data-ttu-id="99a4c-171">Recipient</span><span class="sxs-lookup"><span data-stu-id="99a4c-171">Recipient</span></span>|<span data-ttu-id="99a4c-172">La cuenta que se utiliza realmente para generar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-172">The account that is actually used to generate the message.</span></span> <span data-ttu-id="99a4c-173">Actualizable sólo si isDraft = true y cuándo enviar un mensaje desde un [buzón compartido](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes)o enviar un mensaje como un [delegado](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926).</span><span class="sxs-lookup"><span data-stu-id="99a4c-173">Updatable only if isDraft = true, and when sending a message from a [shared mailbox](https://docs.microsoft.com/en-us/exchange/collaboration/shared-mailboxes/shared-mailboxes), or sending a message as a [delegate](https://support.office.com/en-us/article/allow-someone-else-to-manage-your-mail-and-calendar-41c40c04-3bd1-4d22-963a-28eafec25926).</span></span> <span data-ttu-id="99a4c-174">En cualquier caso, el valor debe corresponder al buzón real que se usa.</span><span class="sxs-lookup"><span data-stu-id="99a4c-174">In any case, the value must correspond to the actual mailbox used.</span></span>|
|<span data-ttu-id="99a4c-175">toRecipients</span><span class="sxs-lookup"><span data-stu-id="99a4c-175">toRecipients</span></span>|<span data-ttu-id="99a4c-176">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="99a4c-176">Recipient collection</span></span>|<span data-ttu-id="99a4c-177">Los destinatarios para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-177">The To recipients for the message.</span></span> <span data-ttu-id="99a4c-178">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="99a4c-178">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="99a4c-179">body</span><span class="sxs-lookup"><span data-stu-id="99a4c-179">body</span></span>|<span data-ttu-id="99a4c-180">ItemBody</span><span class="sxs-lookup"><span data-stu-id="99a4c-180">ItemBody</span></span>|<span data-ttu-id="99a4c-181">El cuerpo del mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-181">The body of the message.</span></span> <span data-ttu-id="99a4c-182">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="99a4c-182">Updatable only if isDraft = true.</span></span>|
|<span data-ttu-id="99a4c-183">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="99a4c-183">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="99a4c-184">Booleano</span><span class="sxs-lookup"><span data-stu-id="99a4c-184">Boolean</span></span>|<span data-ttu-id="99a4c-185">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-185">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="99a4c-186">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="99a4c-186">isReadReceiptRequested</span></span>|<span data-ttu-id="99a4c-187">Booleano</span><span class="sxs-lookup"><span data-stu-id="99a4c-187">Boolean</span></span>|<span data-ttu-id="99a4c-188">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-188">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="99a4c-189">subject</span><span class="sxs-lookup"><span data-stu-id="99a4c-189">subject</span></span>|<span data-ttu-id="99a4c-190">String</span><span class="sxs-lookup"><span data-stu-id="99a4c-190">String</span></span>|<span data-ttu-id="99a4c-191">El asunto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="99a4c-191">The subject of the message.</span></span> <span data-ttu-id="99a4c-192">Actualizable sólo si isDraft = true.</span><span class="sxs-lookup"><span data-stu-id="99a4c-192">Updatable only if isDraft = true.</span></span>|

<span data-ttu-id="99a4c-193">Dado que el recurso **message** admite [extensiones](../../../concepts/extensibility_overview.md), puede utilizar la operación `PATCH` para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia **message** existente.</span><span class="sxs-lookup"><span data-stu-id="99a4c-193">Since the **message** resource supports [extensions](../../../concepts/extensibility_overview.md), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **message** instance.</span></span>

## <a name="response"></a><span data-ttu-id="99a4c-194">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99a4c-194">Response</span></span>

<span data-ttu-id="99a4c-195">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="99a4c-195">If successful, this method returns a `200 OK` response code and updated [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="99a4c-196">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="99a4c-196">Example</span></span>
##### <a name="request"></a><span data-ttu-id="99a4c-197">Solicitud</span><span class="sxs-lookup"><span data-stu-id="99a4c-197">Request</span></span>
<span data-ttu-id="99a4c-198">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="99a4c-198">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="99a4c-199">Respuesta</span><span class="sxs-lookup"><span data-stu-id="99a4c-199">Response</span></span>
<span data-ttu-id="99a4c-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="99a4c-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="99a4c-203">Vea también</span><span class="sxs-lookup"><span data-stu-id="99a4c-203">See also</span></span>

- [<span data-ttu-id="99a4c-204">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="99a4c-204">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="99a4c-205">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="99a4c-205">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
<!--
- [Add custom data to groups using schema extensions (preview)](../../../concepts/extensibility_schema_groups.md)
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
