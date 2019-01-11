---
title: administrador de invitaciones
description: 'Use el Administrador de invitaciones para crear una invitación para agregar un usuario externo a la organización. '
localization_priority: Priority
ms.openlocfilehash: 4e47131fd7e3128366d482c314c059d833c8e101
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27867441"
---
# <a name="invitation-manager"></a><span data-ttu-id="a71ea-103">administrador de invitaciones</span><span class="sxs-lookup"><span data-stu-id="a71ea-103">invitation manager</span></span>

<span data-ttu-id="a71ea-104">Use el Administrador de invitaciones para crear una invitación para agregar un usuario externo a la organización.</span><span class="sxs-lookup"><span data-stu-id="a71ea-104">Use the invitation manager to create an invite, in order to add an external user to the organization.</span></span> 

<span data-ttu-id="a71ea-105">El proceso de invitación sigue el flujo siguiente:</span><span class="sxs-lookup"><span data-stu-id="a71ea-105">The invitation process uses the following flow:</span></span>

* <span data-ttu-id="a71ea-106">Se crea una invitación</span><span class="sxs-lookup"><span data-stu-id="a71ea-106">An invitation is created</span></span>
* <span data-ttu-id="a71ea-107">Se envía una invitación al usuario invitado (que contiene un vínculo de invitación)</span><span class="sxs-lookup"><span data-stu-id="a71ea-107">An invitation is sent to the invited user (containing an invitation link)</span></span>
* <span data-ttu-id="a71ea-108">El usuario invitado hace clic en el vínculo de la invitación, inicia sesión, canjea la invitación y finaliza la creación de la entidad de usuario que representa al usuario invitado</span><span class="sxs-lookup"><span data-stu-id="a71ea-108">The invited user clicks on the invitation link, signs in and redeems the invitation and creation of the user entity representing the invited user completes</span></span>
* <span data-ttu-id="a71ea-109">Se redirige al usuario a una página específica después del canje</span><span class="sxs-lookup"><span data-stu-id="a71ea-109">The user is redirected to a specific page after redemption completes</span></span>

<span data-ttu-id="a71ea-p101">Al crear una invitación, se devolverá una dirección URL de canje en la respuesta (*inviteRedeemUrl*). La API para crear la invitación puede enviar automáticamente un correo electrónico con la dirección URL de canje al usuario invitado, al establecer *sendInvitationMessage* en true. También puede personalizar el mensaje que se enviará al usuario invitado. En su lugar, si quiere enviar la dirección URL de canje a través de otros medios, puede establecer *sendInvitationMessage* en false y usar la dirección URL de canje de la respuesta para elaborar su propia comunicación. Actualmente, no hay ninguna API para realizar el proceso de canje. El usuario invitado tiene que hacer clic en el vínculo *inviteRedeemUrl* enviado en la comunicación en el paso anterior y pasar por el proceso de canje interactivo en un explorador. Una vez completado, el usuario invitado se convierte en usuario externo de la organización.</span><span class="sxs-lookup"><span data-stu-id="a71ea-p101">Creating an invitation will return a redemption URL in the response (*inviteRedeemUrl*). The create invitation API can automatically send an email containing the redemption URL to the invited user, by setting the *sendInvitationMessage* to true. You can also customize the message that will be sent to the invited user. Instead, if you wish to send the redemption URL through some other means, you can set the *sendInvitationMessage* to false and use the redeem URL from the response to craft your own communication. Currently, there is no API to perform the redemption process. The invited user has to click on the *inviteRedeemUrl* link sent in the communication in the step above, and go through the interactive redemption process in a browser. Once completed, the invited user becomes an external user in the organization.</span></span>


## <a name="methods"></a><span data-ttu-id="a71ea-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="a71ea-117">Methods</span></span>
| <span data-ttu-id="a71ea-118">Método</span><span class="sxs-lookup"><span data-stu-id="a71ea-118">Method</span></span>       | <span data-ttu-id="a71ea-119">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a71ea-119">Return Type</span></span>  |<span data-ttu-id="a71ea-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="a71ea-120">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="a71ea-121">Crear invitación</span><span class="sxs-lookup"><span data-stu-id="a71ea-121">Create invitation</span></span>](../api/invitation-post.md) | <span data-ttu-id="a71ea-122">invitation</span><span class="sxs-lookup"><span data-stu-id="a71ea-122">invitation</span></span> | <span data-ttu-id="a71ea-123">Escriba las propiedades y relaciones del objeto de invitación.</span><span class="sxs-lookup"><span data-stu-id="a71ea-123">Write properties and relationships of invitation object.</span></span>|

## <a name="properties"></a><span data-ttu-id="a71ea-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a71ea-124">Properties</span></span>
| <span data-ttu-id="a71ea-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a71ea-125">Property</span></span>     | <span data-ttu-id="a71ea-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="a71ea-126">Type</span></span>   |<span data-ttu-id="a71ea-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="a71ea-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a71ea-128">invitedUserDisplayName</span><span class="sxs-lookup"><span data-stu-id="a71ea-128">invitedUserDisplayName</span></span>|<span data-ttu-id="a71ea-129">String</span><span class="sxs-lookup"><span data-stu-id="a71ea-129">String</span></span>|<span data-ttu-id="a71ea-130">Nombre para mostrar del usuario al que se invita.</span><span class="sxs-lookup"><span data-stu-id="a71ea-130">The display name of the user being invited.</span></span>|
|<span data-ttu-id="a71ea-131">invitedUserEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a71ea-131">invitedUserEmailAddress</span></span>|<span data-ttu-id="a71ea-132">String</span><span class="sxs-lookup"><span data-stu-id="a71ea-132">String</span></span>|<span data-ttu-id="a71ea-p102">Dirección de correo electrónico del usuario al que se invita. Necesario.</span><span class="sxs-lookup"><span data-stu-id="a71ea-p102">The email address of the user being invited. Required.</span></span>|
|<span data-ttu-id="a71ea-135">invitedUserMessageInfo</span><span class="sxs-lookup"><span data-stu-id="a71ea-135">invitedUserMessageInfo</span></span>|[<span data-ttu-id="a71ea-136">invitedUserMessageInfo</span><span class="sxs-lookup"><span data-stu-id="a71ea-136">invitedUserMessageInfo</span></span>](invitedusermessageinfo.md)|<span data-ttu-id="a71ea-137">Configuración adicional para el mensaje que se envía al usuario invitado, incluidos la personalización del texto del mensaje, el idioma y la lista de destinatarios CC.</span><span class="sxs-lookup"><span data-stu-id="a71ea-137">Additional configuration for the message being sent to the invited user, including customizing message text, language and cc recipient list.</span></span>|
|<span data-ttu-id="a71ea-138">sendInvitationMessage</span><span class="sxs-lookup"><span data-stu-id="a71ea-138">sendInvitationMessage</span></span>|<span data-ttu-id="a71ea-139">Booleano</span><span class="sxs-lookup"><span data-stu-id="a71ea-139">Boolean</span></span>|<span data-ttu-id="a71ea-p103">Indica si se debe enviar un correo electrónico al usuario al que se invita o no. El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="a71ea-p103">Indicates whether an email should be sent to the user being invited or not. The default is false.</span></span>|
|<span data-ttu-id="a71ea-142">inviteRedirectUrl</span><span class="sxs-lookup"><span data-stu-id="a71ea-142">inviteRedirectUrl</span></span>|<span data-ttu-id="a71ea-143">String</span><span class="sxs-lookup"><span data-stu-id="a71ea-143">String</span></span>|<span data-ttu-id="a71ea-p104">La dirección URL a la que se redirigirá al usuario una vez que se canjee la invitación. Necesario.</span><span class="sxs-lookup"><span data-stu-id="a71ea-p104">The URL user should be redirected to once the invitation is redeemed. Required.</span></span>|
|<span data-ttu-id="a71ea-146">inviteRedeemUrl</span><span class="sxs-lookup"><span data-stu-id="a71ea-146">inviteRedeemUrl</span></span>|<span data-ttu-id="a71ea-147">String</span><span class="sxs-lookup"><span data-stu-id="a71ea-147">String</span></span>|<span data-ttu-id="a71ea-p105">La dirección URL que puede usar el usuario para canjear su invitación. Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a71ea-p105">The URL user can use to redeem his invitation. Read-Only</span></span>|
|<span data-ttu-id="a71ea-150">invitedUserType</span><span class="sxs-lookup"><span data-stu-id="a71ea-150">invitedUserType</span></span>|<span data-ttu-id="a71ea-151">String</span><span class="sxs-lookup"><span data-stu-id="a71ea-151">String</span></span>|<span data-ttu-id="a71ea-152">userType del usuario al que se invita.</span><span class="sxs-lookup"><span data-stu-id="a71ea-152">The userType of the user being invited.</span></span> <span data-ttu-id="a71ea-153">El valor predeterminado es Guest.</span><span class="sxs-lookup"><span data-stu-id="a71ea-153">By default, this is Guest.</span></span> <span data-ttu-id="a71ea-154">Puede invitar como Member si es administrador de una empresa.</span><span class="sxs-lookup"><span data-stu-id="a71ea-154">You can invite as Member if you are a company administrator.</span></span> |
|<span data-ttu-id="a71ea-155">status</span><span class="sxs-lookup"><span data-stu-id="a71ea-155">status</span></span>|<span data-ttu-id="a71ea-156">String</span><span class="sxs-lookup"><span data-stu-id="a71ea-156">String</span></span>|<span data-ttu-id="a71ea-p107">El estado de la invitación. Valores posibles: PendingAcceptance, Completed, InProgress y Error</span><span class="sxs-lookup"><span data-stu-id="a71ea-p107">The status of the invitation. Possible values: PendingAcceptance, Completed, InProgress, and Error</span></span>|

## <a name="relationships"></a><span data-ttu-id="a71ea-159">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a71ea-159">Relationships</span></span>
| <span data-ttu-id="a71ea-160">Relación</span><span class="sxs-lookup"><span data-stu-id="a71ea-160">Relationship</span></span> | <span data-ttu-id="a71ea-161">Tipo</span><span class="sxs-lookup"><span data-stu-id="a71ea-161">Type</span></span>   |<span data-ttu-id="a71ea-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="a71ea-162">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a71ea-163">invitedUser</span><span class="sxs-lookup"><span data-stu-id="a71ea-163">invitedUser</span></span>|[<span data-ttu-id="a71ea-164">User</span><span class="sxs-lookup"><span data-stu-id="a71ea-164">User</span></span>](user.md)|<span data-ttu-id="a71ea-p108">El usuario creado como parte de la creación de la invitación. Solo lectura</span><span class="sxs-lookup"><span data-stu-id="a71ea-p108">The user created as part of the invitation creation. Read-Only</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a71ea-167">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a71ea-167">JSON representation</span></span>
<span data-ttu-id="a71ea-168">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="a71ea-168">Here is a JSON representation of the resource</span></span>

<!-- { "blockType": "resource", "baseType": "microsoft.graph.entity", "@odata.type": "microsoft.graph.invitation" } -->
```json
{
  "invitedUserDisplayName": "string",
  "invitedUserEmailAddress": "string",
  "invitedUserMessageInfo": {"@odata.type": "microsoft.graph.invitedUserMessageInfo"},
  "sendInvitationMessage": false,
  "inviteRedirectUrl": "string",
  "inviteRedeemUrl": "string",
  "status": "string",
  "invitedUser": {"@odata.type": "microsoft.graph.user"},
  "invitedUserType": "string"
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2016-22-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "invitation resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
