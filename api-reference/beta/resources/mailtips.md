---
title: tipo de recurso de sugerencias de correo electrónico
description: 'Mensajes informativos acerca de un destinatario, que se muestran a los usuarios mientras que redactan un mensaje. Por ejemplo, un mensaje de fuera de la oficina '
localization_priority: Normal
ms.openlocfilehash: 62955594412b2d42a4d05b4b13858c4e511605df
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860644"
---
# <a name="mailtips-resource-type"></a><span data-ttu-id="93fa3-104">tipo de recurso de sugerencias de correo electrónico</span><span class="sxs-lookup"><span data-stu-id="93fa3-104">mailTips resource type</span></span>

> <span data-ttu-id="93fa3-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="93fa3-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="93fa3-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="93fa3-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="93fa3-107">Mensajes informativos acerca de un destinatario, que se muestran a los usuarios mientras que redactan un mensaje.</span><span class="sxs-lookup"><span data-stu-id="93fa3-107">Informative messages about a recipient, that are displayed to users while they are composing a message.</span></span> <span data-ttu-id="93fa3-108">Por ejemplo, un mensaje de fuera de la oficina como respuesta automática para un destinatario del mensaje.</span><span class="sxs-lookup"><span data-stu-id="93fa3-108">For example, an out-of-office message as an automatic reply for a message recipient.</span></span>


## <a name="properties"></a><span data-ttu-id="93fa3-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93fa3-109">Properties</span></span>
| <span data-ttu-id="93fa3-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="93fa3-110">Property</span></span>     | <span data-ttu-id="93fa3-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="93fa3-111">Type</span></span>   |<span data-ttu-id="93fa3-112">Description</span><span class="sxs-lookup"><span data-stu-id="93fa3-112">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="93fa3-113">automaticReplies</span><span class="sxs-lookup"><span data-stu-id="93fa3-113">automaticReplies</span></span> | [<span data-ttu-id="93fa3-114">automaticRepliesMailTips</span><span class="sxs-lookup"><span data-stu-id="93fa3-114">automaticRepliesMailTips</span></span>](../resources/automaticrepliesmailtips.md) | <span data-ttu-id="93fa3-115">Si se ha configurado el destinatario de correo sugerencias para la respuesta automática.</span><span class="sxs-lookup"><span data-stu-id="93fa3-115">Mail tips for automatic reply if it has been set up by the recipient.</span></span> |
| <span data-ttu-id="93fa3-116">customMailTip</span><span class="sxs-lookup"><span data-stu-id="93fa3-116">customMailTip</span></span> | <span data-ttu-id="93fa3-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="93fa3-117">String</span></span> | <span data-ttu-id="93fa3-118">Una sugerencia de correo personalizado que se puede establecer en el buzón del destinatario.</span><span class="sxs-lookup"><span data-stu-id="93fa3-118">A custom mail tip that can be set on the recipient's mailbox.</span></span> |
| <span data-ttu-id="93fa3-119">deliveryRestricted</span><span class="sxs-lookup"><span data-stu-id="93fa3-119">deliveryRestricted</span></span>| <span data-ttu-id="93fa3-120">Booleano</span><span class="sxs-lookup"><span data-stu-id="93fa3-120">Boolean</span></span> | <span data-ttu-id="93fa3-121">Si el buzón del destinatario está restringido, por ejemplo, aceptación de los mensajes de sólo una lista predefinida de remitentes, rechazar los mensajes de una lista predefinida de remitentes o aceptación de los mensajes de los remitentes autenticados sólo.</span><span class="sxs-lookup"><span data-stu-id="93fa3-121">Whether the recipient's mailbox is restricted, for example, accepting messages from only a predefined list of senders, rejecting messages from a predefined list of senders, or accepting messages from only authenticated senders.</span></span> |
| <span data-ttu-id="93fa3-122">emailAddress</span><span class="sxs-lookup"><span data-stu-id="93fa3-122">emailAddress</span></span> | [<span data-ttu-id="93fa3-123">emailAddress</span><span class="sxs-lookup"><span data-stu-id="93fa3-123">emailAddress</span></span>](../resources/emailaddress.md) | <span data-ttu-id="93fa3-124">La dirección de correo electrónico del destinatario para obtener sugerencias de correo electrónico para.</span><span class="sxs-lookup"><span data-stu-id="93fa3-124">The email address of the recipient to get mailtips for.</span></span> |
| <span data-ttu-id="93fa3-125">error</span><span class="sxs-lookup"><span data-stu-id="93fa3-125">error</span></span> | [<span data-ttu-id="93fa3-126">mailTipsError</span><span class="sxs-lookup"><span data-stu-id="93fa3-126">mailTipsError</span></span>](../resources/mailtipserror.md) | <span data-ttu-id="93fa3-127">Errores que se producen durante la acción [getMailTips](../api/user-getmailtips.md) .</span><span class="sxs-lookup"><span data-stu-id="93fa3-127">Errors that occur during the [getMailTips](../api/user-getmailtips.md) action.</span></span> |
| <span data-ttu-id="93fa3-128">externalMemberCount</span><span class="sxs-lookup"><span data-stu-id="93fa3-128">externalMemberCount</span></span> | <span data-ttu-id="93fa3-129">Int32</span><span class="sxs-lookup"><span data-stu-id="93fa3-129">Int32</span></span> | <span data-ttu-id="93fa3-130">El número de miembros externos si el destinatario es una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="93fa3-130">The number of external members if the recipient is a distribution list.</span></span> |
| <span data-ttu-id="93fa3-131">isModerated</span><span class="sxs-lookup"><span data-stu-id="93fa3-131">isModerated</span></span> |<span data-ttu-id="93fa3-132">Booleano</span><span class="sxs-lookup"><span data-stu-id="93fa3-132">Boolean</span></span>  | <span data-ttu-id="93fa3-133">Si requiere aprobación del envío de mensajes al destinatario.</span><span class="sxs-lookup"><span data-stu-id="93fa3-133">Whether sending messages to the recipient requires approval.</span></span> <span data-ttu-id="93fa3-134">Por ejemplo, si el destinatario es una lista de distribución grande y un moderador se ha establecido hasta aprobar los mensajes enviados a esa lista de distribución, o si el envío de mensajes a un destinatario requiere aprobación del administrador del destinatario.</span><span class="sxs-lookup"><span data-stu-id="93fa3-134">For example, if the recipient is a large distribution list and a moderator has been set up to approve messages sent to that distribution list, or if sending messages to a recipient requires approval of the recipient's manager.</span></span> |
| <span data-ttu-id="93fa3-135">mailboxFull</span><span class="sxs-lookup"><span data-stu-id="93fa3-135">mailboxFull</span></span> | <span data-ttu-id="93fa3-136">Booleano</span><span class="sxs-lookup"><span data-stu-id="93fa3-136">Boolean</span></span> | <span data-ttu-id="93fa3-137">El estado completo del buzón de correo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="93fa3-137">The mailbox full status of the recipient.</span></span> |
| <span data-ttu-id="93fa3-138">maxMessageSize</span><span class="sxs-lookup"><span data-stu-id="93fa3-138">maxMessageSize</span></span> | <span data-ttu-id="93fa3-139">Int32</span><span class="sxs-lookup"><span data-stu-id="93fa3-139">Int32</span></span> | <span data-ttu-id="93fa3-140">El tamaño máximo de mensaje que se ha configurado para la organización o el buzón de correo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="93fa3-140">The maximum message size that has been configured for the recipient's organization or mailbox.</span></span> |
| <span data-ttu-id="93fa3-141">recipientScope</span><span class="sxs-lookup"><span data-stu-id="93fa3-141">recipientScope</span></span> | <span data-ttu-id="93fa3-142">Cadena</span><span class="sxs-lookup"><span data-stu-id="93fa3-142">String</span></span> | <span data-ttu-id="93fa3-143">El ámbito del destinatario.</span><span class="sxs-lookup"><span data-stu-id="93fa3-143">The scope of the recipient.</span></span> <span data-ttu-id="93fa3-144">Los valores posibles son: `none`, `internal`, `external`, `externalPartner` y `externalNonParther`.</span><span class="sxs-lookup"><span data-stu-id="93fa3-144">Possible values are: `none`, `internal`, `external`, `externalPartner`, `externalNonParther`.</span></span> <span data-ttu-id="93fa3-145">Por ejemplo, un administrador puede establecer otra organización como su "socio".</span><span class="sxs-lookup"><span data-stu-id="93fa3-145">For example, an administrator can set another organization to be its "partner".</span></span> <span data-ttu-id="93fa3-146">El ámbito es útil si un administrador desea limitar algunas sugerencias de correo electrónico puedan tener acceso a determinados ámbitos.</span><span class="sxs-lookup"><span data-stu-id="93fa3-146">The scope is useful if an administrator wants certain mailtips to be accessible to certain scopes.</span></span> <span data-ttu-id="93fa3-147">También es útil para los remitentes para informarles de que su mensaje puede salir de la organización, ayudarlos a tomar las decisiones correctas acerca de redacción, tono y contenido.</span><span class="sxs-lookup"><span data-stu-id="93fa3-147">It's also useful to senders to inform them that their message may leave the organization, helping them make the correct decisions about wording, tone and content.</span></span>|
| <span data-ttu-id="93fa3-148">recipientSuggestions</span><span class="sxs-lookup"><span data-stu-id="93fa3-148">recipientSuggestions</span></span> | <span data-ttu-id="93fa3-149">Colección [recipient](../resources/recipient.md)</span><span class="sxs-lookup"><span data-stu-id="93fa3-149">[recipient](../resources/recipient.md) collection</span></span> | <span data-ttu-id="93fa3-150">Destinatarios sugieren en función de contextos anteriores donde aparecen en el mismo mensaje.</span><span class="sxs-lookup"><span data-stu-id="93fa3-150">Recipients suggested based on previous contexts where they appear in the same message.</span></span> |
| <span data-ttu-id="93fa3-151">totalMemberCount</span><span class="sxs-lookup"><span data-stu-id="93fa3-151">totalMemberCount</span></span> | <span data-ttu-id="93fa3-152">Int32</span><span class="sxs-lookup"><span data-stu-id="93fa3-152">Int32</span></span> | <span data-ttu-id="93fa3-153">El número de miembros si el destinatario es una lista de distribución.</span><span class="sxs-lookup"><span data-stu-id="93fa3-153">The number of members if the recipient is a distribution list.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="93fa3-154">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="93fa3-154">JSON representation</span></span>

<span data-ttu-id="93fa3-155">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="93fa3-155">Here is a JSON representation of the resource.</span></span>

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
