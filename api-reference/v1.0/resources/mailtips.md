# <a name="mailtips-resource-type"></a><span data-ttu-id="0c549-101">Tipo de recurso mailTips</span><span class="sxs-lookup"><span data-stu-id="0c549-101">mailTips resource type</span></span>

<span data-ttu-id="0c549-102">Mensajes informativos acerca de un destinatario, que se muestran a los usuarios mientras que redactan un mensaje.</span><span class="sxs-lookup"><span data-stu-id="0c549-102">Informative messages displayed to users while they are composing a message.</span></span> <span data-ttu-id="0c549-103">Por ejemplo, un mensaje de fuera de la oficina como una respuesta automática para un destinatario del mensaje.</span><span class="sxs-lookup"><span data-stu-id="0c549-103">For example, an out-of-office message as an automatic reply for a message recipient.</span></span>


## <a name="properties"></a><span data-ttu-id="0c549-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c549-104">Properties</span></span>
| <span data-ttu-id="0c549-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0c549-105">Property</span></span>     | <span data-ttu-id="0c549-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c549-106">Type</span></span>   |<span data-ttu-id="0c549-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c549-107">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="0c549-108">automaticReplies</span><span class="sxs-lookup"><span data-stu-id="0c549-108">AutomaticReplies</span></span> | [<span data-ttu-id="0c549-109">automaticRepliesMailTips</span><span class="sxs-lookup"><span data-stu-id="0c549-109">AutomaticRepliesMailTips</span></span>](../resources/automaticrepliesmailtips.md) | <span data-ttu-id="0c549-110">Sugerencias por correo para la respuesta automática si el destinatario lo ha configurado.</span><span class="sxs-lookup"><span data-stu-id="0c549-110">Mail tips for automatic reply if it has been set up by the recipient.</span></span> |
| <span data-ttu-id="0c549-111">customMailTip</span><span class="sxs-lookup"><span data-stu-id="0c549-111">CustomMailTip</span></span> | <span data-ttu-id="0c549-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="0c549-112">String</span></span> | <span data-ttu-id="0c549-113">Una sugerencia de correo personalizada que se puede configurar en el buzón del destinatario.</span><span class="sxs-lookup"><span data-stu-id="0c549-113">A custom mail tip that can be set on the recipient's mailbox.</span></span> |
| <span data-ttu-id="0c549-114">deliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="0c549-114">DeliveryRestricted</span></span>| <span data-ttu-id="0c549-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="0c549-115">Boolean</span></span> | <span data-ttu-id="0c549-116">Si el buzón del destinatario está restringido, por ejemplo, si solo acepta mensajes de una lista predefinida de remitentes, rechaza mensajes de una lista predefinida de remitentes o acepta mensajes de solo remitentes autenticados.</span><span class="sxs-lookup"><span data-stu-id="0c549-116">Whether the recipient's mailbox is restricted, for example, accepting messages from only a predefined list of senders, rejecting messages from a predefined list of senders, or accepting messages from only authenticated senders.</span></span> |
| <span data-ttu-id="0c549-117">emailAddress</span><span class="sxs-lookup"><span data-stu-id="0c549-117">emailAddress</span></span> | [<span data-ttu-id="0c549-118">emailAddress</span><span class="sxs-lookup"><span data-stu-id="0c549-118">emailAddress</span></span>](../resources/emailaddress.md) | <span data-ttu-id="0c549-119">La dirección de correo electrónico del destinatario para recibir sugerencias de correo.</span><span class="sxs-lookup"><span data-stu-id="0c549-119">The email address of the recipient to get mailtips for.</span></span> |
| <span data-ttu-id="0c549-120">error</span><span class="sxs-lookup"><span data-stu-id="0c549-120">error</span></span> | [<span data-ttu-id="0c549-121">mailTipsError</span><span class="sxs-lookup"><span data-stu-id="0c549-121">mailTipsError</span></span>](../resources/mailtipserror.md) | <span data-ttu-id="0c549-122">Errores que ocurren durante la acción [GetMailTips](../api/user_getmailtips.md).</span><span class="sxs-lookup"><span data-stu-id="0c549-122">Errors that occur during the [GetMailTips](../api/user_getmailtips.md) action.</span></span> |
| <span data-ttu-id="0c549-123">externalMemberCount</span><span class="sxs-lookup"><span data-stu-id="0c549-123">ExternalMemberCount</span></span> | <span data-ttu-id="0c549-124">Int32</span><span class="sxs-lookup"><span data-stu-id="0c549-124">Int32</span></span> | <span data-ttu-id="0c549-125">La cantidad de miembros externos si el destinatario es una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="0c549-125">The number of external members if the recipient is a distribution list.</span></span> |
| <span data-ttu-id="0c549-126">isModerated</span><span class="sxs-lookup"><span data-stu-id="0c549-126">IsModerated</span></span> |<span data-ttu-id="0c549-127">Booleano</span><span class="sxs-lookup"><span data-stu-id="0c549-127">Boolean</span></span>  | <span data-ttu-id="0c549-128">Si el envío de mensajes al destinatario requiere aprobación.</span><span class="sxs-lookup"><span data-stu-id="0c549-128">Whether sending messages to the recipient requires approval.</span></span> <span data-ttu-id="0c549-129">Por ejemplo, si el destinatario es una gran lista de distribución y se ha configurado un moderador para aprobar los mensajes enviados a esa lista de distribución, o si el envío de mensajes a un destinatario requiere la aprobación del administrador del destinatario.</span><span class="sxs-lookup"><span data-stu-id="0c549-129">For example, if the recipient is a large distribution list and a moderator has been set up to approve messages sent to that distribution list, or if sending messages to a recipient requires approval of the recipient's manager.</span></span> |
| <span data-ttu-id="0c549-130">mailboxFull</span><span class="sxs-lookup"><span data-stu-id="0c549-130">MailboxFull</span></span> | <span data-ttu-id="0c549-131">Booleano</span><span class="sxs-lookup"><span data-stu-id="0c549-131">Boolean</span></span> | <span data-ttu-id="0c549-132">El estado de lleno del buzón del destinatario.</span><span class="sxs-lookup"><span data-stu-id="0c549-132">The mailbox full status of the recipient.</span></span> |
| <span data-ttu-id="0c549-133">maxMessageSize</span><span class="sxs-lookup"><span data-stu-id="0c549-133">MaxMessageSize</span></span> | <span data-ttu-id="0c549-134">Int32</span><span class="sxs-lookup"><span data-stu-id="0c549-134">Int32</span></span> | <span data-ttu-id="0c549-135">El tamaño máximo de mensaje que se ha configurado para la organización o el buzón del destinatario.</span><span class="sxs-lookup"><span data-stu-id="0c549-135">The maximum message size that has been configured for the recipient's organization or mailbox.</span></span> |
| <span data-ttu-id="0c549-136">recipientScope</span><span class="sxs-lookup"><span data-stu-id="0c549-136">RecipientScope</span></span> | <span data-ttu-id="0c549-137">recipientScopeType</span><span class="sxs-lookup"><span data-stu-id="0c549-137">RecipientScopeType</span></span> | <span data-ttu-id="0c549-138">El ámbito del destinatario.</span><span class="sxs-lookup"><span data-stu-id="0c549-138">The scope of the recipient, such as internal, external, partner.</span></span> <span data-ttu-id="0c549-139">Los valores posibles son: `none`, `internal`, `external`, `externalPartner` y `externalNonParther`.</span><span class="sxs-lookup"><span data-stu-id="0c549-139">Possible values are: `none`, `internal`, `external`, `externalPartner`, `externalNonParther`.</span></span> <span data-ttu-id="0c549-140">Por ejemplo, un administrador puede establecer que otra organización sea su "socio".</span><span class="sxs-lookup"><span data-stu-id="0c549-140">For example, an administrator can set another organization to be its "partner".</span></span> <span data-ttu-id="0c549-141">El ámbito es útil si un administrador desea que ciertas sugerencias de correo sean accesibles para ciertos ámbitos.</span><span class="sxs-lookup"><span data-stu-id="0c549-141">The scope is useful if an administrator wants certain mailtips to be accessible to certain scopes.</span></span> <span data-ttu-id="0c549-142">También es útil para los remitentes, para informarles de que su mensaje puede salir de la organización y ayudarles a tomar las decisiones correctas sobre la redacción, el tono y el contenido.</span><span class="sxs-lookup"><span data-stu-id="0c549-142">It's also useful to senders to inform them that their message may leave the organization, helping them make the correct decisions about wording, tone and content.</span></span>|
| <span data-ttu-id="0c549-143">recipientSuggestions</span><span class="sxs-lookup"><span data-stu-id="0c549-143">RecipientSuggestions</span></span> | <span data-ttu-id="0c549-144">Colección [recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="0c549-144">[recipient](../resources/recipient.md) collection</span></span> | <span data-ttu-id="0c549-145">Destinatarios sugeridos basados ​​en contextos anteriores donde aparecen en el mismo mensaje.</span><span class="sxs-lookup"><span data-stu-id="0c549-145">Recipients suggested based on previous contexts where they appear in the same message.</span></span> |
| <span data-ttu-id="0c549-146">totalMemberCount</span><span class="sxs-lookup"><span data-stu-id="0c549-146">TotalMemberCount</span></span> | <span data-ttu-id="0c549-147">Int32</span><span class="sxs-lookup"><span data-stu-id="0c549-147">Int32</span></span> | <span data-ttu-id="0c549-148">La cantidad de miembros si el destinatario es una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="0c549-148">The number of members if the recipient is a distribution list.</span></span> |

### <a name="recipientscopetype-values"></a><span data-ttu-id="0c549-149">Valores de recipientScopeType</span><span class="sxs-lookup"><span data-stu-id="0c549-149">recipientScopeType values</span></span>

| <span data-ttu-id="0c549-150">Valor</span><span class="sxs-lookup"><span data-stu-id="0c549-150">Value</span></span>
|:-------------------------
| <span data-ttu-id="0c549-151">none</span><span class="sxs-lookup"><span data-stu-id="0c549-151">none</span></span>
| <span data-ttu-id="0c549-152">internal</span><span class="sxs-lookup"><span data-stu-id="0c549-152">Internal</span></span>
| <span data-ttu-id="0c549-153">external</span><span class="sxs-lookup"><span data-stu-id="0c549-153">External</span></span>
| <span data-ttu-id="0c549-154">externalPartner</span><span class="sxs-lookup"><span data-stu-id="0c549-154">ExternalPartner</span></span>
| <span data-ttu-id="0c549-155">externalNonPartner</span><span class="sxs-lookup"><span data-stu-id="0c549-155">ExternalNonPartner</span></span>


## <a name="json-representation"></a><span data-ttu-id="0c549-156">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0c549-156">JSON representation</span></span>

<span data-ttu-id="0c549-157">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="0c549-157">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "automaticReplies",
    "customMailTip",
    "deliveryRestricted",
    "emailAddress",
    "error",
    "externalMemberCount",
    "isModerated",
    "mailboxFull",
    "maxMessageSize",
    "recipientScope",
    "recipientSuggestions",
    "totalMemberCount"
  ],
  "@odata.type": "microsoft.graph.mailTips"
}-->

```json
{
  "automaticReplies": {"@odata.type": "microsoft.graph.automaticRepliesMailTips"},
  "customMailTip": "string",
  "deliveryRestricted": "boolean",
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"},
  "error": {"@odata.type": "microsoft.graph.mailTipsError"},
  "externalMemberCount": 1024,
  "isModerated": "boolean",
  "mailboxFull": "boolean",
  "maxMessageSize": 1024,
  "recipientScope": "string",
  "recipientSuggestions": [{"@odata.type": "microsoft.graph.recipient"}],
  "totalMemberCount": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mailtips resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
