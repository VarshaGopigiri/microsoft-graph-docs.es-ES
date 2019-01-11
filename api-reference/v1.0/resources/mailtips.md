---
title: tipo de recurso de sugerencias de correo electrónico
description: 'Mensajes informativos acerca de un destinatario, que se muestran a los usuarios mientras que redactan un mensaje. Por ejemplo, un mensaje de fuera de la oficina '
localization_priority: Normal
ms.openlocfilehash: 0506d10ad4b1c5eb473b04a30eb8d48334685574
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891696"
---
# <a name="mailtips-resource-type"></a><span data-ttu-id="5d88d-104">tipo de recurso de sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="5d88d-104">mailTips resource type</span></span>

<span data-ttu-id="5d88d-105">Mensajes informativos acerca de un destinatario, que se muestran a los usuarios mientras que redactan un mensaje.</span><span class="sxs-lookup"><span data-stu-id="5d88d-105">Informative messages about a recipient, that are displayed to users while they are composing a message.</span></span> <span data-ttu-id="5d88d-106">Por ejemplo, un mensaje de fuera de la oficina como respuesta automática para un destinatario del mensaje.</span><span class="sxs-lookup"><span data-stu-id="5d88d-106">For example, an out-of-office message as an automatic reply for a message recipient.</span></span>


## <a name="properties"></a><span data-ttu-id="5d88d-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d88d-107">Properties</span></span>
| <span data-ttu-id="5d88d-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5d88d-108">Property</span></span>     | <span data-ttu-id="5d88d-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d88d-109">Type</span></span>   |<span data-ttu-id="5d88d-110">Description</span><span class="sxs-lookup"><span data-stu-id="5d88d-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5d88d-111">automaticReplies</span><span class="sxs-lookup"><span data-stu-id="5d88d-111">automaticReplies</span></span> | [<span data-ttu-id="5d88d-112">automaticRepliesMailTips</span><span class="sxs-lookup"><span data-stu-id="5d88d-112">automaticRepliesMailTips</span></span>](../resources/automaticrepliesmailtips.md) | <span data-ttu-id="5d88d-113">Si se ha configurado el destinatario de correo sugerencias para la respuesta automática.</span><span class="sxs-lookup"><span data-stu-id="5d88d-113">Mail tips for automatic reply if it has been set up by the recipient.</span></span> |
| <span data-ttu-id="5d88d-114">customMailTip</span><span class="sxs-lookup"><span data-stu-id="5d88d-114">customMailTip</span></span> | <span data-ttu-id="5d88d-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="5d88d-115">String</span></span> | <span data-ttu-id="5d88d-116">Una sugerencia de correo personalizado que se puede establecer en el buzón del destinatario.</span><span class="sxs-lookup"><span data-stu-id="5d88d-116">A custom mail tip that can be set on the recipient's mailbox.</span></span> |
| <span data-ttu-id="5d88d-117">deliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="5d88d-117">deliveryRestricted</span></span>| <span data-ttu-id="5d88d-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="5d88d-118">Boolean</span></span> | <span data-ttu-id="5d88d-119">Si el buzón del destinatario está restringido, por ejemplo, aceptación de los mensajes de sólo una lista predefinida de remitentes, rechazar los mensajes de una lista predefinida de remitentes o aceptación de los mensajes de los remitentes autenticados sólo.</span><span class="sxs-lookup"><span data-stu-id="5d88d-119">Whether the recipient's mailbox is restricted, for example, accepting messages from only a predefined list of senders, rejecting messages from a predefined list of senders, or accepting messages from only authenticated senders.</span></span> |
| <span data-ttu-id="5d88d-120">emailAddress</span><span class="sxs-lookup"><span data-stu-id="5d88d-120">emailAddress</span></span> | [<span data-ttu-id="5d88d-121">emailAddress</span><span class="sxs-lookup"><span data-stu-id="5d88d-121">emailAddress</span></span>](../resources/emailaddress.md) | <span data-ttu-id="5d88d-122">La dirección de correo electrónico del destinatario para obtener sugerencias de correo electrónico para.</span><span class="sxs-lookup"><span data-stu-id="5d88d-122">The email address of the recipient to get mailtips for.</span></span> |
| <span data-ttu-id="5d88d-123">error</span><span class="sxs-lookup"><span data-stu-id="5d88d-123">error</span></span> | [<span data-ttu-id="5d88d-124">mailTipsError</span><span class="sxs-lookup"><span data-stu-id="5d88d-124">mailTipsError</span></span>](../resources/mailtipserror.md) | <span data-ttu-id="5d88d-125">Errores que se producen durante la acción [getMailTips](../api/user-getmailtips.md) .</span><span class="sxs-lookup"><span data-stu-id="5d88d-125">Errors that occur during the [getMailTips](../api/user-getmailtips.md) action.</span></span> |
| <span data-ttu-id="5d88d-126">externalMemberCount</span><span class="sxs-lookup"><span data-stu-id="5d88d-126">externalMemberCount</span></span> | <span data-ttu-id="5d88d-127">Int32</span><span class="sxs-lookup"><span data-stu-id="5d88d-127">Int32</span></span> | <span data-ttu-id="5d88d-128">El número de miembros externos si el destinatario es una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="5d88d-128">The number of external members if the recipient is a distribution list.</span></span> |
| <span data-ttu-id="5d88d-129">isModerated</span><span class="sxs-lookup"><span data-stu-id="5d88d-129">isModerated</span></span> |<span data-ttu-id="5d88d-130">Booleano</span><span class="sxs-lookup"><span data-stu-id="5d88d-130">Boolean</span></span>  | <span data-ttu-id="5d88d-131">Si requiere aprobación del envío de mensajes al destinatario.</span><span class="sxs-lookup"><span data-stu-id="5d88d-131">Whether sending messages to the recipient requires approval.</span></span> <span data-ttu-id="5d88d-132">Por ejemplo, si el destinatario es una lista de distribución grande y un moderador se ha establecido hasta aprobar los mensajes enviados a esa lista de distribución, o si el envío de mensajes a un destinatario requiere aprobación del administrador del destinatario.</span><span class="sxs-lookup"><span data-stu-id="5d88d-132">For example, if the recipient is a large distribution list and a moderator has been set up to approve messages sent to that distribution list, or if sending messages to a recipient requires approval of the recipient's manager.</span></span> |
| <span data-ttu-id="5d88d-133">mailboxFull</span><span class="sxs-lookup"><span data-stu-id="5d88d-133">mailboxFull</span></span> | <span data-ttu-id="5d88d-134">Booleano</span><span class="sxs-lookup"><span data-stu-id="5d88d-134">Boolean</span></span> | <span data-ttu-id="5d88d-135">El estado completo del buzón de correo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="5d88d-135">The mailbox full status of the recipient.</span></span> |
| <span data-ttu-id="5d88d-136">maxMessageSize</span><span class="sxs-lookup"><span data-stu-id="5d88d-136">maxMessageSize</span></span> | <span data-ttu-id="5d88d-137">Int32</span><span class="sxs-lookup"><span data-stu-id="5d88d-137">Int32</span></span> | <span data-ttu-id="5d88d-138">El tamaño máximo de mensaje que se ha configurado para la organización o el buzón de correo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="5d88d-138">The maximum message size that has been configured for the recipient's organization or mailbox.</span></span> |
| <span data-ttu-id="5d88d-139">recipientScope</span><span class="sxs-lookup"><span data-stu-id="5d88d-139">recipientScope</span></span> | <span data-ttu-id="5d88d-140">recipientScopeType</span><span class="sxs-lookup"><span data-stu-id="5d88d-140">recipientScopeType</span></span> | <span data-ttu-id="5d88d-141">El ámbito del destinatario.</span><span class="sxs-lookup"><span data-stu-id="5d88d-141">The scope of the recipient.</span></span> <span data-ttu-id="5d88d-142">Los valores posibles son: `none`, `internal`, `external`, `externalPartner` y `externalNonParther`.</span><span class="sxs-lookup"><span data-stu-id="5d88d-142">Possible values are: `none`, `internal`, `external`, `externalPartner`, `externalNonParther`.</span></span> <span data-ttu-id="5d88d-143">Por ejemplo, un administrador puede establecer otra organización como su "socio".</span><span class="sxs-lookup"><span data-stu-id="5d88d-143">For example, an administrator can set another organization to be its "partner".</span></span> <span data-ttu-id="5d88d-144">El ámbito es útil si un administrador desea limitar algunas sugerencias de correo electrónico puedan tener acceso a determinados ámbitos.</span><span class="sxs-lookup"><span data-stu-id="5d88d-144">The scope is useful if an administrator wants certain mailtips to be accessible to certain scopes.</span></span> <span data-ttu-id="5d88d-145">También es útil para los remitentes para informarles de que su mensaje puede salir de la organización, ayudarlos a tomar las decisiones correctas acerca de redacción, tono y contenido.</span><span class="sxs-lookup"><span data-stu-id="5d88d-145">It's also useful to senders to inform them that their message may leave the organization, helping them make the correct decisions about wording, tone and content.</span></span>|
| <span data-ttu-id="5d88d-146">recipientSuggestions</span><span class="sxs-lookup"><span data-stu-id="5d88d-146">recipientSuggestions</span></span> | <span data-ttu-id="5d88d-147">Colección [recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="5d88d-147">[recipient](../resources/recipient.md) collection</span></span> | <span data-ttu-id="5d88d-148">Destinatarios sugieren en función de contextos anteriores donde aparecen en el mismo mensaje.</span><span class="sxs-lookup"><span data-stu-id="5d88d-148">Recipients suggested based on previous contexts where they appear in the same message.</span></span> |
| <span data-ttu-id="5d88d-149">totalMemberCount</span><span class="sxs-lookup"><span data-stu-id="5d88d-149">totalMemberCount</span></span> | <span data-ttu-id="5d88d-150">Int32</span><span class="sxs-lookup"><span data-stu-id="5d88d-150">Int32</span></span> | <span data-ttu-id="5d88d-151">El número de miembros si el destinatario es una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="5d88d-151">The number of members if the recipient is a distribution list.</span></span> |

### <a name="recipientscopetype-values"></a><span data-ttu-id="5d88d-152">valores de recipientScopeType</span><span class="sxs-lookup"><span data-stu-id="5d88d-152">recipientScopeType values</span></span>

| <span data-ttu-id="5d88d-153">Valor</span><span class="sxs-lookup"><span data-stu-id="5d88d-153">Value</span></span>
|:-------------------------
| <span data-ttu-id="5d88d-154">none</span><span class="sxs-lookup"><span data-stu-id="5d88d-154">none</span></span>
| <span data-ttu-id="5d88d-155">interno</span><span class="sxs-lookup"><span data-stu-id="5d88d-155">internal</span></span>
| <span data-ttu-id="5d88d-156">externo</span><span class="sxs-lookup"><span data-stu-id="5d88d-156">external</span></span>
| <span data-ttu-id="5d88d-157">externalPartner</span><span class="sxs-lookup"><span data-stu-id="5d88d-157">externalPartner</span></span>
| <span data-ttu-id="5d88d-158">externalNonPartner</span><span class="sxs-lookup"><span data-stu-id="5d88d-158">externalNonPartner</span></span>


## <a name="json-representation"></a><span data-ttu-id="5d88d-159">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5d88d-159">JSON representation</span></span>

<span data-ttu-id="5d88d-160">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5d88d-160">Here is a JSON representation of the resource.</span></span>

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
