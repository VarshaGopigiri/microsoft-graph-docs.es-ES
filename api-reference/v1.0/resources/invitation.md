---
title: administrador de invitaciones
description: 'Use el Administrador de invitaciones para crear una invitación para agregar un usuario externo a la organización. '
localization_priority: Priority
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 0a0ee3ba23cb0c323a660b9afd26fa044a50897c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27976740"
---
# <a name="invitation-manager"></a><span data-ttu-id="8fe69-103">administrador de invitaciones</span><span class="sxs-lookup"><span data-stu-id="8fe69-103">invitation manager</span></span>

<span data-ttu-id="8fe69-104">Use el Administrador de invitaciones para crear una invitación para agregar un usuario externo a la organización.</span><span class="sxs-lookup"><span data-stu-id="8fe69-104">Use the invitation manager to create an invite, in order to add an external user to the organization.</span></span> 

<span data-ttu-id="8fe69-105">El proceso de invitación sigue el flujo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8fe69-105">The invitation process uses the following flow:</span></span>

* <span data-ttu-id="8fe69-106">Se crea una invitación</span><span class="sxs-lookup"><span data-stu-id="8fe69-106">An invitation is created</span></span>
* <span data-ttu-id="8fe69-107">Se envía una invitación al usuario invitado (que contiene un vínculo de invitación)</span><span class="sxs-lookup"><span data-stu-id="8fe69-107">An invitation is sent to the invited user (containing an invitation link)</span></span>
* <span data-ttu-id="8fe69-108">El usuario invitado hace clic en el vínculo de la invitación, inicia sesión, canjea la invitación y finaliza la creación de la entidad de usuario que representa al usuario invitado</span><span class="sxs-lookup"><span data-stu-id="8fe69-108">The invited user clicks on the invitation link, signs in and redeems the invitation and creation of the user entity representing the invited user completes</span></span>
* <span data-ttu-id="8fe69-109">Se redirige al usuario a una página específica después del canje</span><span class="sxs-lookup"><span data-stu-id="8fe69-109">The user is redirected to a specific page after redemption completes</span></span>

<span data-ttu-id="8fe69-p101">Al crear una invitación, se devolverá una dirección URL de canje en la respuesta (*inviteRedeemUrl*). La API para crear la invitación puede enviar automáticamente un correo electrónico con la dirección URL de canje al usuario invitado, al establecer *sendInvitationMessage* en true. También puede personalizar el mensaje que se enviará al usuario invitado. En su lugar, si quiere enviar la dirección URL de canje a través de otros medios, puede establecer *sendInvitationMessage* en false y usar la dirección URL de canje de la respuesta para elaborar su propia comunicación. Actualmente, no hay ninguna API para realizar el proceso de canje. El usuario invitado tiene que hacer clic en el vínculo *inviteRedeemUrl* enviado en la comunicación en el paso anterior y pasar por el proceso de canje interactivo en un explorador. Una vez completado, el usuario invitado se convierte en usuario externo de la organización.</span><span class="sxs-lookup"><span data-stu-id="8fe69-p101">Creating an invitation will return a redemption URL in the response (*inviteRedeemUrl*). The create invitation API can automatically send an email containing the redemption URL to the invited user, by setting the *sendInvitationMessage* to true. You can also customize the message that will be sent to the invited user. Instead, if you wish to send the redemption URL through some other means, you can set the *sendInvitationMessage* to false and use the redeem URL from the response to craft your own communication. Currently, there is no API to perform the redemption process. The invited user has to click on the *inviteRedeemUrl* link sent in the communication in the step above, and go through the interactive redemption process in a browser. Once completed, the invited user becomes an external user in the organization.</span></span>


## <a name="methods"></a><span data-ttu-id="8fe69-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="8fe69-117">Methods</span></span>
| <span data-ttu-id="8fe69-118">Método</span><span class="sxs-lookup"><span data-stu-id="8fe69-118">Method</span></span>       | <span data-ttu-id="8fe69-119">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fe69-119">Return Type</span></span>  |<span data-ttu-id="8fe69-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fe69-120">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="8fe69-121">Crear invitación</span><span class="sxs-lookup"><span data-stu-id="8fe69-121">Create invitation</span></span>](../api/invitation-post.md) | <span data-ttu-id="8fe69-122">invitation</span><span class="sxs-lookup"><span data-stu-id="8fe69-122">invitation</span></span> | <span data-ttu-id="8fe69-123">Escriba las propiedades y relaciones del objeto de invitación.</span><span class="sxs-lookup"><span data-stu-id="8fe69-123">Write properties and relationships of invitation object.</span></span>|

## <a name="properties"></a><span data-ttu-id="8fe69-124">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8fe69-124">Properties</span></span>
| <span data-ttu-id="8fe69-125">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8fe69-125">Property</span></span>     | <span data-ttu-id="8fe69-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fe69-126">Type</span></span>   |<span data-ttu-id="8fe69-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fe69-127">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8fe69-128">invitedUserDisplayName</span><span class="sxs-lookup"><span data-stu-id="8fe69-128">invitedUserDisplayName</span></span>|<span data-ttu-id="8fe69-129">String</span><span class="sxs-lookup"><span data-stu-id="8fe69-129">String</span></span>|<span data-ttu-id="8fe69-130">Nombre para mostrar del usuario al que se invita.</span><span class="sxs-lookup"><span data-stu-id="8fe69-130">The display name of the user being invited.</span></span>|
|<span data-ttu-id="8fe69-131">invitedUserEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8fe69-131">invitedUserEmailAddress</span></span>|<span data-ttu-id="8fe69-132">String</span><span class="sxs-lookup"><span data-stu-id="8fe69-132">String</span></span>|<span data-ttu-id="8fe69-p102">Dirección de correo electrónico del usuario al que se invita. Necesario.</span><span class="sxs-lookup"><span data-stu-id="8fe69-p102">The email address of the user being invited. Required.</span></span>|
|<span data-ttu-id="8fe69-135">invitedUserMessageInfo</span><span class="sxs-lookup"><span data-stu-id="8fe69-135">invitedUserMessageInfo</span></span>|[<span data-ttu-id="8fe69-136">invitedUserMessageInfo</span><span class="sxs-lookup"><span data-stu-id="8fe69-136">invitedUserMessageInfo</span></span>](invitedusermessageinfo.md)|<span data-ttu-id="8fe69-137">Configuración adicional para el mensaje que se envía al usuario invitado, incluidos la personalización del texto del mensaje, el idioma y la lista de destinatarios CC.</span><span class="sxs-lookup"><span data-stu-id="8fe69-137">Additional configuration for the message being sent to the invited user, including customizing message text, language and cc recipient list.</span></span>|
|<span data-ttu-id="8fe69-138">sendInvitationMessage</span><span class="sxs-lookup"><span data-stu-id="8fe69-138">sendInvitationMessage</span></span>|<span data-ttu-id="8fe69-139">Booleano</span><span class="sxs-lookup"><span data-stu-id="8fe69-139">Boolean</span></span>|<span data-ttu-id="8fe69-p103">Indica si se debe enviar un correo electrónico al usuario al que se invita o no. El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="8fe69-p103">Indicates whether an email should be sent to the user being invited or not. The default is false.</span></span>|
|<span data-ttu-id="8fe69-142">inviteRedirectUrl</span><span class="sxs-lookup"><span data-stu-id="8fe69-142">inviteRedirectUrl</span></span>|<span data-ttu-id="8fe69-143">String</span><span class="sxs-lookup"><span data-stu-id="8fe69-143">String</span></span>|<span data-ttu-id="8fe69-p104">La dirección URL a la que se redirigirá al usuario una vez que se canjee la invitación. Necesario.</span><span class="sxs-lookup"><span data-stu-id="8fe69-p104">The URL user should be redirected to once the invitation is redeemed. Required.</span></span>|
|<span data-ttu-id="8fe69-146">inviteRedeemUrl</span><span class="sxs-lookup"><span data-stu-id="8fe69-146">inviteRedeemUrl</span></span>|<span data-ttu-id="8fe69-147">String</span><span class="sxs-lookup"><span data-stu-id="8fe69-147">String</span></span>|<span data-ttu-id="8fe69-p105">La dirección URL que puede usar el usuario para canjear su invitación. Solo lectura</span><span class="sxs-lookup"><span data-stu-id="8fe69-p105">The URL user can use to redeem his invitation. Read-Only</span></span>|
|<span data-ttu-id="8fe69-150">invitedUserType</span><span class="sxs-lookup"><span data-stu-id="8fe69-150">invitedUserType</span></span>|<span data-ttu-id="8fe69-151">String</span><span class="sxs-lookup"><span data-stu-id="8fe69-151">String</span></span>|<span data-ttu-id="8fe69-152">userType del usuario al que se invita.</span><span class="sxs-lookup"><span data-stu-id="8fe69-152">The userType of the user being invited.</span></span> <span data-ttu-id="8fe69-153">El valor predeterminado es Guest.</span><span class="sxs-lookup"><span data-stu-id="8fe69-153">By default, this is Guest.</span></span> <span data-ttu-id="8fe69-154">Puede invitar como Member si es administrador de una empresa.</span><span class="sxs-lookup"><span data-stu-id="8fe69-154">You can invite as Member if you are a company administrator.</span></span> |
|<span data-ttu-id="8fe69-155">status</span><span class="sxs-lookup"><span data-stu-id="8fe69-155">status</span></span>|<span data-ttu-id="8fe69-156">String</span><span class="sxs-lookup"><span data-stu-id="8fe69-156">String</span></span>|<span data-ttu-id="8fe69-p107">El estado de la invitación. Valores posibles: PendingAcceptance, Completed, InProgress y Error</span><span class="sxs-lookup"><span data-stu-id="8fe69-p107">The status of the invitation. Possible values: PendingAcceptance, Completed, InProgress, and Error</span></span>|

## <a name="relationships"></a><span data-ttu-id="8fe69-159">Relaciones</span><span class="sxs-lookup"><span data-stu-id="8fe69-159">Relationships</span></span>
| <span data-ttu-id="8fe69-160">Relación</span><span class="sxs-lookup"><span data-stu-id="8fe69-160">Relationship</span></span> | <span data-ttu-id="8fe69-161">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fe69-161">Type</span></span>   |<span data-ttu-id="8fe69-162">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fe69-162">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8fe69-163">invitedUser</span><span class="sxs-lookup"><span data-stu-id="8fe69-163">invitedUser</span></span>|[<span data-ttu-id="8fe69-164">User</span><span class="sxs-lookup"><span data-stu-id="8fe69-164">User</span></span>](user.md)|<span data-ttu-id="8fe69-p108">El usuario creado como parte de la creación de la invitación. Solo lectura</span><span class="sxs-lookup"><span data-stu-id="8fe69-p108">The user created as part of the invitation creation. Read-Only</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8fe69-167">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8fe69-167">JSON representation</span></span>
<span data-ttu-id="8fe69-168">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8fe69-168">Here is a JSON representation of the resource</span></span>

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
