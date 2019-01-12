---
title: administrador de invitaciones
description: 'Use el Administrador de invitaciones para crear una invitación para agregar un usuario externo a la organización. '
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 72ff2ca13a0de314697961504da9a4203afdb2b1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27981052"
---
# <a name="invitation-manager"></a><span data-ttu-id="6ba7c-103">administrador de invitaciones</span><span class="sxs-lookup"><span data-stu-id="6ba7c-103">invitation manager</span></span>

> <span data-ttu-id="6ba7c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6ba7c-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6ba7c-106">Use el Administrador de invitaciones para crear una invitación para agregar un usuario externo a la organización.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-106">Use the invitation manager to create an invite, in order to add an external user to the organization.</span></span> 

<span data-ttu-id="6ba7c-107">El proceso de invitación sigue el flujo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6ba7c-107">The invitation process uses the following flow:</span></span>

* <span data-ttu-id="6ba7c-108">Se crea una invitación</span><span class="sxs-lookup"><span data-stu-id="6ba7c-108">An invitation is created</span></span>
* <span data-ttu-id="6ba7c-109">Se envía una invitación al usuario invitado (que contiene un vínculo de invitación)</span><span class="sxs-lookup"><span data-stu-id="6ba7c-109">An invitation is sent to the invited user (containing an invitation link)</span></span>
* <span data-ttu-id="6ba7c-110">El usuario invitado hace clic en el vínculo de la invitación, inicia sesión, canjea la invitación y finaliza la creación de la entidad de usuario que representa al usuario invitado</span><span class="sxs-lookup"><span data-stu-id="6ba7c-110">The invited user clicks on the invitation link, signs in and redeems the invitation and creation of the user entity representing the invited user completes</span></span>
* <span data-ttu-id="6ba7c-111">Se redirige al usuario a una página específica después del canje</span><span class="sxs-lookup"><span data-stu-id="6ba7c-111">The user is redirected to a specific page after redemption completes</span></span>

<span data-ttu-id="6ba7c-p102">Al crear una invitación, se devolverá una dirección URL de canje en la respuesta (*inviteRedeemUrl*). La API para crear la invitación puede enviar automáticamente un correo electrónico con la dirección URL de canje al usuario invitado, al establecer *sendInvitationMessage* en true. También puede personalizar el mensaje que se enviará al usuario invitado. En su lugar, si quiere enviar la dirección URL de canje a través de otros medios, puede establecer *sendInvitationMessage* en false y usar la dirección URL de canje de la respuesta para elaborar su propia comunicación. Actualmente, no hay ninguna API para realizar el proceso de canje. El usuario invitado tiene que hacer clic en el vínculo *inviteRedeemUrl* enviado en la comunicación en el paso anterior y pasar por el proceso de canje interactivo en un explorador. Una vez completado, el usuario invitado se convierte en usuario externo de la organización.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-p102">Creating an invitation will return a redemption URL in the response (*inviteRedeemUrl*). The create invitation API can automatically send an email containing the redemption URL to the invited user, by setting the *sendInvitationMessage* to true. You can also customize the message that will be sent to the invited user. Instead, if you wish to send the redemption URL through some other means, you can set the *sendInvitationMessage* to false and use the redeem URL from the response to craft your own communication. Currently, there is no API to perform the redemption process. The invited user has to click on the *inviteRedeemUrl* link sent in the communication in the step above, and go through the interactive redemption process in a browser. Once completed, the invited user becomes an external user in the organization.</span></span>


## <a name="methods"></a><span data-ttu-id="6ba7c-119">Métodos</span><span class="sxs-lookup"><span data-stu-id="6ba7c-119">Methods</span></span>
| <span data-ttu-id="6ba7c-120">Método</span><span class="sxs-lookup"><span data-stu-id="6ba7c-120">Method</span></span>       | <span data-ttu-id="6ba7c-121">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6ba7c-121">Return Type</span></span>  |<span data-ttu-id="6ba7c-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ba7c-122">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="6ba7c-123">Crear invitación</span><span class="sxs-lookup"><span data-stu-id="6ba7c-123">Create invitation</span></span>](../api/invitation-post.md) | <span data-ttu-id="6ba7c-124">invitation</span><span class="sxs-lookup"><span data-stu-id="6ba7c-124">invitation</span></span> | <span data-ttu-id="6ba7c-125">Escriba las propiedades y relaciones del objeto de invitación.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-125">Write properties and relationships of invitation object.</span></span>|

## <a name="properties"></a><span data-ttu-id="6ba7c-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6ba7c-126">Properties</span></span>
| <span data-ttu-id="6ba7c-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6ba7c-127">Property</span></span>     | <span data-ttu-id="6ba7c-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ba7c-128">Type</span></span>   |<span data-ttu-id="6ba7c-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ba7c-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6ba7c-130">invitedUserDisplayName</span><span class="sxs-lookup"><span data-stu-id="6ba7c-130">invitedUserDisplayName</span></span>|<span data-ttu-id="6ba7c-131">String</span><span class="sxs-lookup"><span data-stu-id="6ba7c-131">String</span></span>|<span data-ttu-id="6ba7c-132">Nombre para mostrar del usuario al que se invita.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-132">The display name of the user being invited.</span></span>|
|<span data-ttu-id="6ba7c-133">invitedUserEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6ba7c-133">invitedUserEmailAddress</span></span>|<span data-ttu-id="6ba7c-134">String</span><span class="sxs-lookup"><span data-stu-id="6ba7c-134">String</span></span>|<span data-ttu-id="6ba7c-p103">Dirección de correo electrónico del usuario al que se invita. Necesario.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-p103">The email address of the user being invited. Required.</span></span>|
|<span data-ttu-id="6ba7c-137">invitedUserMessageInfo</span><span class="sxs-lookup"><span data-stu-id="6ba7c-137">invitedUserMessageInfo</span></span>|[<span data-ttu-id="6ba7c-138">invitedUserMessageInfo</span><span class="sxs-lookup"><span data-stu-id="6ba7c-138">invitedUserMessageInfo</span></span>](invitedusermessageinfo.md)|<span data-ttu-id="6ba7c-139">Configuración adicional para el mensaje que se envía al usuario invitado, incluidos la personalización del texto del mensaje, el idioma y la lista de destinatarios CC.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-139">Additional configuration for the message being sent to the invited user, including customizing message text, language and cc recipient list.</span></span>|
|<span data-ttu-id="6ba7c-140">sendInvitationMessage</span><span class="sxs-lookup"><span data-stu-id="6ba7c-140">sendInvitationMessage</span></span>|<span data-ttu-id="6ba7c-141">Booleano</span><span class="sxs-lookup"><span data-stu-id="6ba7c-141">Boolean</span></span>|<span data-ttu-id="6ba7c-p104">Indica si se debe enviar un correo electrónico al usuario al que se invita o no. El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-p104">Indicates whether an email should be sent to the user being invited or not. The default is false.</span></span>|
|<span data-ttu-id="6ba7c-144">inviteRedirectUrl</span><span class="sxs-lookup"><span data-stu-id="6ba7c-144">inviteRedirectUrl</span></span>|<span data-ttu-id="6ba7c-145">String</span><span class="sxs-lookup"><span data-stu-id="6ba7c-145">String</span></span>|<span data-ttu-id="6ba7c-p105">La dirección URL a la que se redirigirá al usuario una vez que se canjee la invitación. Necesario.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-p105">The URL user should be redirected to once the invitation is redeemed. Required.</span></span>|
|<span data-ttu-id="6ba7c-148">inviteRedeemUrl</span><span class="sxs-lookup"><span data-stu-id="6ba7c-148">inviteRedeemUrl</span></span>|<span data-ttu-id="6ba7c-149">String</span><span class="sxs-lookup"><span data-stu-id="6ba7c-149">String</span></span>|<span data-ttu-id="6ba7c-p106">La dirección URL que puede usar el usuario para canjear su invitación. Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba7c-p106">The URL user can use to redeem his invitation. Read-Only</span></span>|
|<span data-ttu-id="6ba7c-152">invitedUserType</span><span class="sxs-lookup"><span data-stu-id="6ba7c-152">invitedUserType</span></span>|<span data-ttu-id="6ba7c-153">String</span><span class="sxs-lookup"><span data-stu-id="6ba7c-153">String</span></span>|<span data-ttu-id="6ba7c-p107">userType del usuario al que se invita. El valor predeterminado es Guest. Puede invitar como Member si es administrador de la empresa.</span><span class="sxs-lookup"><span data-stu-id="6ba7c-p107">The userType of the user being invited. By default, this is Guest. You can invite as Member if you're are company administrator.</span></span> |
|<span data-ttu-id="6ba7c-157">status</span><span class="sxs-lookup"><span data-stu-id="6ba7c-157">status</span></span>|<span data-ttu-id="6ba7c-158">String</span><span class="sxs-lookup"><span data-stu-id="6ba7c-158">String</span></span>|<span data-ttu-id="6ba7c-p108">El estado de la invitación. Valores posibles: PendingAcceptance, Completed, InProgress y Error</span><span class="sxs-lookup"><span data-stu-id="6ba7c-p108">The status of the invitation. Possible values: PendingAcceptance, Completed, InProgress, and Error</span></span>|

## <a name="relationships"></a><span data-ttu-id="6ba7c-161">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6ba7c-161">Relationships</span></span>
| <span data-ttu-id="6ba7c-162">Relación</span><span class="sxs-lookup"><span data-stu-id="6ba7c-162">Relationship</span></span> | <span data-ttu-id="6ba7c-163">Tipo</span><span class="sxs-lookup"><span data-stu-id="6ba7c-163">Type</span></span>   |<span data-ttu-id="6ba7c-164">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ba7c-164">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6ba7c-165">invitedUser</span><span class="sxs-lookup"><span data-stu-id="6ba7c-165">invitedUser</span></span>|[<span data-ttu-id="6ba7c-166">User</span><span class="sxs-lookup"><span data-stu-id="6ba7c-166">User</span></span>](user.md)|<span data-ttu-id="6ba7c-p109">El usuario creado como parte de la creación de la invitación. Solo lectura</span><span class="sxs-lookup"><span data-stu-id="6ba7c-p109">The user created as part of the invitation creation. Read-Only</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6ba7c-169">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6ba7c-169">JSON representation</span></span>
<span data-ttu-id="6ba7c-170">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6ba7c-170">Here is a JSON representation of the resource</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.invitations" } -->
```json
{
  "invitedUserDisplayName": "string",
  "invitedUserEmailAddress": "string",
  "invitedUserMessageInfo": {"@odata.type": "microsoft.graph.invitedUserMessageInfo"},
  "sendInvitationMessage": false,
  "inviteRedirectUrl": "string",
  "inviteRedeemUrl": "string",
  "status": "string",

  "invitedUser": [{"@odata.type": "microsoft.graph.user"}]
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
