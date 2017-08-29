# <a name="update-message"></a><span data-ttu-id="6315d-101">Actualizar mensaje</span><span class="sxs-lookup"><span data-stu-id="6315d-101">Update message</span></span>

<span data-ttu-id="6315d-102">Actualice las propiedades del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="6315d-102">Update the properties of message object.</span></span>
## <a name="permissions"></a><span data-ttu-id="6315d-103">Permisos</span><span class="sxs-lookup"><span data-stu-id="6315d-103">Permissions</span></span>
<span data-ttu-id="6315d-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="6315d-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="6315d-106">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="6315d-106">Permission type</span></span>      | <span data-ttu-id="6315d-107">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="6315d-107">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="6315d-108">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="6315d-108">Delegated (work or school account)</span></span> | <span data-ttu-id="6315d-109">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6315d-109">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6315d-110">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="6315d-110">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="6315d-111">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6315d-111">Mail.ReadWrite</span></span>    |
|<span data-ttu-id="6315d-112">Aplicación</span><span class="sxs-lookup"><span data-stu-id="6315d-112">Application</span></span> | <span data-ttu-id="6315d-113">Mail.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="6315d-113">Mail.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="6315d-114">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="6315d-114">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}
PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="6315d-115">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="6315d-115">Request headers</span></span>
| <span data-ttu-id="6315d-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="6315d-116">Name</span></span>       | <span data-ttu-id="6315d-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="6315d-117">Type</span></span> | <span data-ttu-id="6315d-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="6315d-118">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="6315d-119">Authorization</span><span class="sxs-lookup"><span data-stu-id="6315d-119">Authorization</span></span>  | <span data-ttu-id="6315d-120">string</span><span class="sxs-lookup"><span data-stu-id="6315d-120">string</span></span>  | <span data-ttu-id="6315d-p102">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6315d-p102">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="6315d-123">Content-Type</span><span class="sxs-lookup"><span data-stu-id="6315d-123">Content-Type</span></span> | <span data-ttu-id="6315d-124">string</span><span class="sxs-lookup"><span data-stu-id="6315d-124">string</span></span>  | <span data-ttu-id="6315d-p103">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="6315d-p103">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="6315d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="6315d-127">Request body</span></span>
<span data-ttu-id="6315d-p104">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado. Son propiedades Writable/Updatable</span><span class="sxs-lookup"><span data-stu-id="6315d-p104">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. Writable/Updatable properties are</span></span>

| <span data-ttu-id="6315d-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6315d-132">Property</span></span>     | <span data-ttu-id="6315d-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="6315d-133">Type</span></span>   |<span data-ttu-id="6315d-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="6315d-134">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6315d-135">bccRecipients</span><span class="sxs-lookup"><span data-stu-id="6315d-135">bccRecipients</span></span>|<span data-ttu-id="6315d-136">Destinatario</span><span class="sxs-lookup"><span data-stu-id="6315d-136">Recipient</span></span>|<span data-ttu-id="6315d-p105">Los destinatarios CCO del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6315d-p105">The Bcc recipients for the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="6315d-139">categories</span><span class="sxs-lookup"><span data-stu-id="6315d-139">categories</span></span>|<span data-ttu-id="6315d-140">Colección string</span><span class="sxs-lookup"><span data-stu-id="6315d-140">String collection</span></span>|<span data-ttu-id="6315d-141">Las categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="6315d-141">The categories associated with the message.</span></span>|
|<span data-ttu-id="6315d-142">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="6315d-142">ccRecipients</span></span>|<span data-ttu-id="6315d-143">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="6315d-143">Recipient collection</span></span>|<span data-ttu-id="6315d-p106">Los destinatarios CC del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6315d-p106">The Cc recipients for the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="6315d-146">from</span><span class="sxs-lookup"><span data-stu-id="6315d-146">from</span></span>|<span data-ttu-id="6315d-147">Destinatario</span><span class="sxs-lookup"><span data-stu-id="6315d-147">Recipient</span></span>|<span data-ttu-id="6315d-p107">El propietario del buzón y el remitente del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6315d-p107">The mailbox owner and sender of the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="6315d-150">importance</span><span class="sxs-lookup"><span data-stu-id="6315d-150">importance</span></span>|<span data-ttu-id="6315d-151">String</span><span class="sxs-lookup"><span data-stu-id="6315d-151">String</span></span>|<span data-ttu-id="6315d-p108">La importancia del mensaje. Los valores posibles son: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="6315d-p108">The importance of the message. Possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="6315d-154">inferenceClassification</span><span class="sxs-lookup"><span data-stu-id="6315d-154">inferenceClassification</span></span> | <span data-ttu-id="6315d-155">String</span><span class="sxs-lookup"><span data-stu-id="6315d-155">String</span></span> | <span data-ttu-id="6315d-p109">La clasificación del mensaje para el usuario, según relevancia inferida, importancia o según una invalidación explícita. Los valores posibles son: `focused` o `other`.</span><span class="sxs-lookup"><span data-stu-id="6315d-p109">The classification of the message for the user, based on inferred relevance or importance, or on an explicit override. Possible values are: `focused` or `other`.</span></span> |
|<span data-ttu-id="6315d-158">internetMessageId</span><span class="sxs-lookup"><span data-stu-id="6315d-158">internetMessageId</span></span> |<span data-ttu-id="6315d-159">String</span><span class="sxs-lookup"><span data-stu-id="6315d-159">String</span></span> |<span data-ttu-id="6315d-p110">El identificador del mensaje en el formato especificado por [RFC2822](http://www.ietf.org/rfc/rfc2822.txt). Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6315d-p110">The message ID in the format specified by [RFC2822](http://www.ietf.org/rfc/rfc2822.txt). Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="6315d-162">isRead</span><span class="sxs-lookup"><span data-stu-id="6315d-162">isRead</span></span>|<span data-ttu-id="6315d-163">Booleano</span><span class="sxs-lookup"><span data-stu-id="6315d-163">Boolean</span></span>|<span data-ttu-id="6315d-164">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6315d-164">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="6315d-165">replyTo</span><span class="sxs-lookup"><span data-stu-id="6315d-165">replyTo</span></span>|<span data-ttu-id="6315d-166">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="6315d-166">Recipient collection</span></span>|<span data-ttu-id="6315d-p111">Las direcciones de correo electrónico que se usan al responder. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6315d-p111">The email addresses to use when replying. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="6315d-169">sender</span><span class="sxs-lookup"><span data-stu-id="6315d-169">sender</span></span>|<span data-ttu-id="6315d-170">Destinatario</span><span class="sxs-lookup"><span data-stu-id="6315d-170">Recipient</span></span>|<span data-ttu-id="6315d-p112">La cuenta que se usa realmente para generar el mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6315d-p112">The account that is actually used to generate the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="6315d-173">toRecipients</span><span class="sxs-lookup"><span data-stu-id="6315d-173">toRecipients</span></span>|<span data-ttu-id="6315d-174">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="6315d-174">Recipient collection</span></span>|<span data-ttu-id="6315d-p113">Los destinatarios Para del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6315d-p113">The To recipients for the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="6315d-177">cuerpo</span><span class="sxs-lookup"><span data-stu-id="6315d-177">body</span></span>|<span data-ttu-id="6315d-178">ItemBody</span><span class="sxs-lookup"><span data-stu-id="6315d-178">ItemBody</span></span>|<span data-ttu-id="6315d-p114">El cuerpo del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6315d-p114">The body of the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="6315d-181">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="6315d-181">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="6315d-182">Booleano</span><span class="sxs-lookup"><span data-stu-id="6315d-182">Boolean</span></span>|<span data-ttu-id="6315d-183">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6315d-183">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="6315d-184">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="6315d-184">isReadReceiptRequested</span></span>|<span data-ttu-id="6315d-185">Booleano</span><span class="sxs-lookup"><span data-stu-id="6315d-185">Boolean</span></span>|<span data-ttu-id="6315d-186">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6315d-186">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="6315d-187">subject</span><span class="sxs-lookup"><span data-stu-id="6315d-187">subject</span></span>|<span data-ttu-id="6315d-188">String</span><span class="sxs-lookup"><span data-stu-id="6315d-188">String</span></span>|<span data-ttu-id="6315d-p115">El asunto del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="6315d-p115">The subject of the message. Updatable only if IsDraft = true.</span></span>|

<span data-ttu-id="6315d-191">Dado que el recurso **message** admite [extensiones](../../../concepts/extensibility_overview.md), puede utilizar la operación `PATCH` para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia **message** existente.</span><span class="sxs-lookup"><span data-stu-id="6315d-191">Since the **message** resource supports [extensions](../../../concepts/extensibility_overview.md), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **message** instance.</span></span>

## <a name="response"></a><span data-ttu-id="6315d-192">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6315d-192">Response</span></span>

<span data-ttu-id="6315d-193">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="6315d-193">If successful, this method returns a `200 OK` response code and updated [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="6315d-194">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="6315d-194">Example</span></span>
##### <a name="request"></a><span data-ttu-id="6315d-195">Solicitud</span><span class="sxs-lookup"><span data-stu-id="6315d-195">Request</span></span>
<span data-ttu-id="6315d-196">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="6315d-196">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="6315d-197">Respuesta</span><span class="sxs-lookup"><span data-stu-id="6315d-197">Response</span></span>
<span data-ttu-id="6315d-p116">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="6315d-p116">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="6315d-201">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="6315d-201">See also</span></span>

- [<span data-ttu-id="6315d-202">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="6315d-202">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="6315d-203">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="6315d-203">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
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
