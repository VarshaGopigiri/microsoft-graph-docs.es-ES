# <a name="update-message"></a><span data-ttu-id="c7006-101">Actualizar mensaje</span><span class="sxs-lookup"><span data-stu-id="c7006-101">Update message</span></span>

<span data-ttu-id="c7006-102">Actualice las propiedades del objeto de mensaje.</span><span class="sxs-lookup"><span data-stu-id="c7006-102">Update the properties of message object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c7006-103">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c7006-103">Prerequisites</span></span>
<span data-ttu-id="c7006-104">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API: *Mail.ReadWrite*</span><span class="sxs-lookup"><span data-stu-id="c7006-104">One of the following **scopes** is required to execute this API: *Mail.ReadWrite*</span></span>
## <a name="http-request"></a><span data-ttu-id="c7006-105">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7006-105">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id | userPrincipalName}/messages/{id}
PATCH /me/mailFolders/{id}/messages/{id}
PATCH /users/{id | userPrincipalName}/mailFolders/{id}/messages/{id}
```
## <a name="request-headers"></a><span data-ttu-id="c7006-106">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7006-106">Request headers</span></span>
| <span data-ttu-id="c7006-107">Nombre</span><span class="sxs-lookup"><span data-stu-id="c7006-107">Name</span></span>       | <span data-ttu-id="c7006-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7006-108">Type</span></span> | <span data-ttu-id="c7006-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7006-109">Description</span></span>|
|:-----------|:------|:----------|
| <span data-ttu-id="c7006-110">Authorization</span><span class="sxs-lookup"><span data-stu-id="c7006-110">Authorization</span></span>  | <span data-ttu-id="c7006-111">string</span><span class="sxs-lookup"><span data-stu-id="c7006-111">string</span></span>  | <span data-ttu-id="c7006-p101">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c7006-p101">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="c7006-114">Content-Type</span><span class="sxs-lookup"><span data-stu-id="c7006-114">Content-Type</span></span> | <span data-ttu-id="c7006-115">string</span><span class="sxs-lookup"><span data-stu-id="c7006-115">string</span></span>  | <span data-ttu-id="c7006-p102">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="c7006-p102">Nature of the data in the body of an entity. Required.</span></span> |
## <a name="request-body"></a><span data-ttu-id="c7006-118">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7006-118">Request body</span></span>
<span data-ttu-id="c7006-p103">En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento no debe incluir valores existentes que no hayan cambiado. Son propiedades Writable/Updatable</span><span class="sxs-lookup"><span data-stu-id="c7006-p103">In the request body, supply the values for relevant fields that should be updated. Existing properties that are not included in the request body will maintain their previous values or be recalculated based on changes to other property values. For best performance you shouldn't include existing values that haven't changed. Writable/Updatable properties are</span></span>

| <span data-ttu-id="c7006-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c7006-123">Property</span></span>     | <span data-ttu-id="c7006-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7006-124">Type</span></span>   |<span data-ttu-id="c7006-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7006-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="c7006-126">bccRecipients</span><span class="sxs-lookup"><span data-stu-id="c7006-126">bccRecipients</span></span>|<span data-ttu-id="c7006-127">Destinatario</span><span class="sxs-lookup"><span data-stu-id="c7006-127">Recipient</span></span>|<span data-ttu-id="c7006-p104">Los destinatarios CCO del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="c7006-p104">The Bcc recipients for the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="c7006-130">categories</span><span class="sxs-lookup"><span data-stu-id="c7006-130">categories</span></span>|<span data-ttu-id="c7006-131">Colección string</span><span class="sxs-lookup"><span data-stu-id="c7006-131">String collection</span></span>|<span data-ttu-id="c7006-132">Las categorías asociadas al mensaje.</span><span class="sxs-lookup"><span data-stu-id="c7006-132">The categories associated with the message.</span></span>|
|<span data-ttu-id="c7006-133">ccRecipients</span><span class="sxs-lookup"><span data-stu-id="c7006-133">ccRecipients</span></span>|<span data-ttu-id="c7006-134">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="c7006-134">Recipient collection</span></span>|<span data-ttu-id="c7006-p105">Los destinatarios CC del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="c7006-p105">The Cc recipients for the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="c7006-137">from</span><span class="sxs-lookup"><span data-stu-id="c7006-137">from</span></span>|<span data-ttu-id="c7006-138">Destinatario</span><span class="sxs-lookup"><span data-stu-id="c7006-138">Recipient</span></span>|<span data-ttu-id="c7006-p106">El propietario del buzón y el remitente del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="c7006-p106">The mailbox owner and sender of the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="c7006-141">importance</span><span class="sxs-lookup"><span data-stu-id="c7006-141">importance</span></span>|<span data-ttu-id="c7006-142">String</span><span class="sxs-lookup"><span data-stu-id="c7006-142">String</span></span>|<span data-ttu-id="c7006-p107">La importancia del mensaje. Los valores posibles son: `Low`, `Normal`, `High`.</span><span class="sxs-lookup"><span data-stu-id="c7006-p107">The importance of the message. Possible values are: `Low`, `Normal`, `High`.</span></span>|
|<span data-ttu-id="c7006-145">inferenceClassification</span><span class="sxs-lookup"><span data-stu-id="c7006-145">inferenceClassification</span></span> | <span data-ttu-id="c7006-146">String</span><span class="sxs-lookup"><span data-stu-id="c7006-146">String</span></span> | <span data-ttu-id="c7006-p108">La clasificación del mensaje para el usuario, según relevancia inferida, importancia o según una invalidación explícita. Los valores posibles son: `focused` o `other`.</span><span class="sxs-lookup"><span data-stu-id="c7006-p108">The classification of the message for the user, based on inferred relevance or importance, or on an explicit override. Possible values are: `focused` or `other`.</span></span> |
|<span data-ttu-id="c7006-149">internetMessageId</span><span class="sxs-lookup"><span data-stu-id="c7006-149">internetMessageId</span></span> |<span data-ttu-id="c7006-150">String</span><span class="sxs-lookup"><span data-stu-id="c7006-150">String</span></span> |<span data-ttu-id="c7006-p109">El identificador del mensaje en el formato especificado por [RFC2822](http://www.ietf.org/rfc/rfc2822.txt). Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="c7006-p109">The message ID in the format specified by [RFC2822](http://www.ietf.org/rfc/rfc2822.txt). Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="c7006-153">isRead</span><span class="sxs-lookup"><span data-stu-id="c7006-153">isRead</span></span>|<span data-ttu-id="c7006-154">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7006-154">Boolean</span></span>|<span data-ttu-id="c7006-155">Indica si se ha leído el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c7006-155">Indicates whether the message has been read.</span></span>|
|<span data-ttu-id="c7006-156">replyTo</span><span class="sxs-lookup"><span data-stu-id="c7006-156">replyTo</span></span>|<span data-ttu-id="c7006-157">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="c7006-157">Recipient collection</span></span>|<span data-ttu-id="c7006-p110">Las direcciones de correo electrónico que se usan al responder. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="c7006-p110">The email addresses to use when replying. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="c7006-160">sender</span><span class="sxs-lookup"><span data-stu-id="c7006-160">sender</span></span>|<span data-ttu-id="c7006-161">Destinatario</span><span class="sxs-lookup"><span data-stu-id="c7006-161">Recipient</span></span>|<span data-ttu-id="c7006-p111">La cuenta que se usa realmente para generar el mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="c7006-p111">The account that is actually used to generate the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="c7006-164">toRecipients</span><span class="sxs-lookup"><span data-stu-id="c7006-164">toRecipients</span></span>|<span data-ttu-id="c7006-165">Colección Recipient</span><span class="sxs-lookup"><span data-stu-id="c7006-165">Recipient collection</span></span>|<span data-ttu-id="c7006-p112">Los destinatarios Para del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="c7006-p112">The To recipients for the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="c7006-168">cuerpo</span><span class="sxs-lookup"><span data-stu-id="c7006-168">body</span></span>|<span data-ttu-id="c7006-169">ItemBody</span><span class="sxs-lookup"><span data-stu-id="c7006-169">ItemBody</span></span>|<span data-ttu-id="c7006-p113">El cuerpo del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="c7006-p113">The body of the message. Updatable only if IsDraft = true.</span></span>|
|<span data-ttu-id="c7006-172">isDeliveryReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="c7006-172">isDeliveryReceiptRequested</span></span>|<span data-ttu-id="c7006-173">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7006-173">Boolean</span></span>|<span data-ttu-id="c7006-174">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c7006-174">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="c7006-175">isReadReceiptRequested</span><span class="sxs-lookup"><span data-stu-id="c7006-175">isReadReceiptRequested</span></span>|<span data-ttu-id="c7006-176">Booleano</span><span class="sxs-lookup"><span data-stu-id="c7006-176">Boolean</span></span>|<span data-ttu-id="c7006-177">Indica si se solicita confirmación de lectura para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="c7006-177">Indicates whether a read receipt is requested for the message.</span></span>|
|<span data-ttu-id="c7006-178">subject</span><span class="sxs-lookup"><span data-stu-id="c7006-178">subject</span></span>|<span data-ttu-id="c7006-179">String</span><span class="sxs-lookup"><span data-stu-id="c7006-179">String</span></span>|<span data-ttu-id="c7006-p114">El asunto del mensaje. Solo se puede actualizar si IsDraft = true.</span><span class="sxs-lookup"><span data-stu-id="c7006-p114">The subject of the message. Updatable only if IsDraft = true.</span></span>|

<span data-ttu-id="c7006-182">Dado que el recurso **message** admite [extensiones](../../../concepts/extensibility_overview.md), puede utilizar la operación `PATCH` para agregar, actualizar o eliminar sus propios datos específicos de la aplicación en las propiedades personalizadas de una extensión en una instancia **message** existente.</span><span class="sxs-lookup"><span data-stu-id="c7006-182">Since the **message** resource supports [extensions](../../../concepts/extensibility_overview.md), you can use the `PATCH` operation to add, update, or delete your own app-specific data in custom properties of an extension in an existing **message** instance.</span></span>

## <a name="response"></a><span data-ttu-id="c7006-183">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7006-183">Response</span></span>

<span data-ttu-id="c7006-184">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [message](../resources/message.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7006-184">If successful, this method returns a `200 OK` response code and updated [message](../resources/message.md) object in the response body.</span></span>
## <a name="example"></a><span data-ttu-id="c7006-185">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7006-185">Example</span></span>
##### <a name="request"></a><span data-ttu-id="c7006-186">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7006-186">Request</span></span>
<span data-ttu-id="c7006-187">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7006-187">Here is an example of the request.</span></span>
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
##### <a name="response"></a><span data-ttu-id="c7006-188">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7006-188">Response</span></span>
<span data-ttu-id="c7006-p115">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7006-p115">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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

## <a name="see-also"></a><span data-ttu-id="c7006-192">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="c7006-192">See also</span></span>

- [<span data-ttu-id="c7006-193">Agregar datos personalizados a los recursos mediante extensiones</span><span class="sxs-lookup"><span data-stu-id="c7006-193">Add custom data to resources using extensions</span></span>](../../../concepts/extensibility_overview.md)
- [<span data-ttu-id="c7006-194">Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)</span><span class="sxs-lookup"><span data-stu-id="c7006-194">Add custom data to users using open extensions (preview)</span></span>](../../../concepts/extensibility_open_users.md)
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
