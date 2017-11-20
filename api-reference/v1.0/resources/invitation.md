# <a name="invitation-manager"></a><span data-ttu-id="56e71-101">administrador de invitaciones</span><span class="sxs-lookup"><span data-stu-id="56e71-101">invitation manager</span></span>

<span data-ttu-id="56e71-102">Use el Administrador de invitaciones para crear una invitación para agregar un usuario externo a la organización.</span><span class="sxs-lookup"><span data-stu-id="56e71-102">Use the invitation manager to create an invite, in order to add an external user to the organization.</span></span> 

<span data-ttu-id="56e71-103">El proceso de invitación sigue el flujo siguiente:</span><span class="sxs-lookup"><span data-stu-id="56e71-103">The invitation process uses the following flow:</span></span>

* <span data-ttu-id="56e71-104">Se crea una invitación</span><span class="sxs-lookup"><span data-stu-id="56e71-104">An invitation is created</span></span>
* <span data-ttu-id="56e71-105">Se envía una invitación al usuario invitado (que contiene un vínculo de invitación)</span><span class="sxs-lookup"><span data-stu-id="56e71-105">An invitation is sent to the invited user (containing an invitation link)</span></span>
* <span data-ttu-id="56e71-106">El usuario invitado hace clic en el vínculo de la invitación, inicia sesión, canjea la invitación y finaliza la creación de la entidad de usuario que representa al usuario invitado</span><span class="sxs-lookup"><span data-stu-id="56e71-106">The invited user clicks on the invitation link, signs in and redeems the invitation and creation of the user entity representing the invited user completes</span></span>
* <span data-ttu-id="56e71-107">Se redirige al usuario a una página específica después del canje</span><span class="sxs-lookup"><span data-stu-id="56e71-107">The user is redirected to a specific page after redemption completes</span></span>

<span data-ttu-id="56e71-p101">Al crear una invitación, se devolverá una dirección URL de canje en la respuesta (*inviteRedeemUrl*). La API para crear la invitación puede enviar automáticamente un correo electrónico con la dirección URL de canje al usuario invitado, al establecer *sendInvitationMessage* en true. También puede personalizar el mensaje que se enviará al usuario invitado. En su lugar, si quiere enviar la dirección URL de canje a través de otros medios, puede establecer *sendInvitationMessage* en false y usar la dirección URL de canje de la respuesta para elaborar su propia comunicación. Actualmente, no hay ninguna API para realizar el proceso de canje. El usuario invitado tiene que hacer clic en el vínculo *inviteRedeemUrl* enviado en la comunicación en el paso anterior y pasar por el proceso de canje interactivo en un explorador. Una vez completado, el usuario invitado se convierte en usuario externo de la organización.</span><span class="sxs-lookup"><span data-stu-id="56e71-p101">Creating an invitation will return a redemption URL in the response (*inviteRedeemUrl*). The create invitation API can automatically send an email containing the redemption URL to the invited user, by setting the *sendInvitationMessage* to true. You can also customize the message that will be sent to the invited user. Instead, if you wish to send the redemption URL through some other means, you can set the *sendInvitationMessage* to false and use the redeem URL from the response to craft your own communication. Currently, there is no API to perform the redemption process. The invited user has to click on the *inviteRedeemUrl* link sent in the communication in the step above, and go through the interactive redemption process in a browser. Once completed, the invited user becomes an external user in the organization.</span></span>


## <a name="methods"></a><span data-ttu-id="56e71-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="56e71-115">Methods</span></span>
| <span data-ttu-id="56e71-116">Método</span><span class="sxs-lookup"><span data-stu-id="56e71-116">Method</span></span>       | <span data-ttu-id="56e71-117">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="56e71-117">Return Type</span></span>  |<span data-ttu-id="56e71-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="56e71-118">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="56e71-119">Crear invitación</span><span class="sxs-lookup"><span data-stu-id="56e71-119">Create invitation</span></span>](../api/invitation_post.md) | <span data-ttu-id="56e71-120">invitation</span><span class="sxs-lookup"><span data-stu-id="56e71-120">invitation</span></span> | <span data-ttu-id="56e71-121">Escriba las propiedades y relaciones del objeto de invitación.</span><span class="sxs-lookup"><span data-stu-id="56e71-121">Write properties and relationships of invitation object.</span></span>|

## <a name="properties"></a><span data-ttu-id="56e71-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56e71-122">Properties</span></span>
| <span data-ttu-id="56e71-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="56e71-123">Property</span></span>     | <span data-ttu-id="56e71-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="56e71-124">Type</span></span>   |<span data-ttu-id="56e71-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="56e71-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="56e71-126">invitedUserDisplayName</span><span class="sxs-lookup"><span data-stu-id="56e71-126">invitedUserDisplayName</span></span>|<span data-ttu-id="56e71-127">String</span><span class="sxs-lookup"><span data-stu-id="56e71-127">String</span></span>|<span data-ttu-id="56e71-128">Nombre para mostrar del usuario al que se invita.</span><span class="sxs-lookup"><span data-stu-id="56e71-128">The display name of the user being invited.</span></span>|
|<span data-ttu-id="56e71-129">invitedUserEmailAddress</span><span class="sxs-lookup"><span data-stu-id="56e71-129">invitedUserEmailAddress</span></span>|<span data-ttu-id="56e71-130">String</span><span class="sxs-lookup"><span data-stu-id="56e71-130">String</span></span>|<span data-ttu-id="56e71-p102">Dirección de correo electrónico del usuario al que se invita. Necesario.</span><span class="sxs-lookup"><span data-stu-id="56e71-p102">The email address of the user being invited. Required.</span></span>|
|<span data-ttu-id="56e71-133">invitedUserMessageInfo</span><span class="sxs-lookup"><span data-stu-id="56e71-133">invitedUserMessageInfo</span></span>|[<span data-ttu-id="56e71-134">invitedUserMessageInfo</span><span class="sxs-lookup"><span data-stu-id="56e71-134">invitedUserMessageInfo</span></span>](invitedusermessageinfo.md)|<span data-ttu-id="56e71-135">Configuración adicional para el mensaje que se envía al usuario invitado, incluidos la personalización del texto del mensaje, el idioma y la lista de destinatarios CC.</span><span class="sxs-lookup"><span data-stu-id="56e71-135">Additional configuration for the message being sent to the invited user, including customizing message text, language and cc recipient list.</span></span>|
|<span data-ttu-id="56e71-136">sendInvitationMessage</span><span class="sxs-lookup"><span data-stu-id="56e71-136">sendInvitationMessage</span></span>|<span data-ttu-id="56e71-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="56e71-137">Boolean</span></span>|<span data-ttu-id="56e71-p103">Indica si se debe enviar un correo electrónico al usuario al que se invita o no. El valor predeterminado es false.</span><span class="sxs-lookup"><span data-stu-id="56e71-p103">Indicates whether an email should be sent to the user being invited or not. The default is false.</span></span>|
|<span data-ttu-id="56e71-140">inviteRedirectUrl</span><span class="sxs-lookup"><span data-stu-id="56e71-140">inviteRedirectUrl</span></span>|<span data-ttu-id="56e71-141">String</span><span class="sxs-lookup"><span data-stu-id="56e71-141">String</span></span>|<span data-ttu-id="56e71-p104">La dirección URL a la que se redirigirá al usuario una vez que se canjee la invitación. Necesario.</span><span class="sxs-lookup"><span data-stu-id="56e71-p104">The URL user should be redirected to once the invitation is redeemed. Required.</span></span>|
|<span data-ttu-id="56e71-144">inviteRedeemUrl</span><span class="sxs-lookup"><span data-stu-id="56e71-144">inviteRedeemUrl</span></span>|<span data-ttu-id="56e71-145">String</span><span class="sxs-lookup"><span data-stu-id="56e71-145">String</span></span>|<span data-ttu-id="56e71-p105">La dirección URL que puede usar el usuario para canjear su invitación. Solo lectura</span><span class="sxs-lookup"><span data-stu-id="56e71-p105">The URL user can use to redeem his invitation. Read-Only</span></span>|
|<span data-ttu-id="56e71-148">invitedUserType</span><span class="sxs-lookup"><span data-stu-id="56e71-148">invitedUserType</span></span>|<span data-ttu-id="56e71-149">String</span><span class="sxs-lookup"><span data-stu-id="56e71-149">String</span></span>|<span data-ttu-id="56e71-150">userType del usuario al que se invita.</span><span class="sxs-lookup"><span data-stu-id="56e71-150">The display name of the user being invited.</span></span> <span data-ttu-id="56e71-151">El valor predeterminado es Guest.</span><span class="sxs-lookup"><span data-stu-id="56e71-151">By default, this is Guest.</span></span> <span data-ttu-id="56e71-152">Puede invitar como Member si es administrador de una empresa.</span><span class="sxs-lookup"><span data-stu-id="56e71-152">You can invite as Member if you are a company administrator.</span></span> |
|<span data-ttu-id="56e71-153">status</span><span class="sxs-lookup"><span data-stu-id="56e71-153">status</span></span>|<span data-ttu-id="56e71-154">String</span><span class="sxs-lookup"><span data-stu-id="56e71-154">String</span></span>|<span data-ttu-id="56e71-p107">El estado de la invitación. Valores posibles: PendingAcceptance, Completed, InProgress y Error</span><span class="sxs-lookup"><span data-stu-id="56e71-p107">The status of the invitation. Possible values: PendingAcceptance, Completed, InProgress, and Error</span></span>|

## <a name="relationships"></a><span data-ttu-id="56e71-157">Relaciones</span><span class="sxs-lookup"><span data-stu-id="56e71-157">Relationships</span></span>
| <span data-ttu-id="56e71-158">Relación</span><span class="sxs-lookup"><span data-stu-id="56e71-158">Relationship</span></span> | <span data-ttu-id="56e71-159">Tipo</span><span class="sxs-lookup"><span data-stu-id="56e71-159">Type</span></span>   |<span data-ttu-id="56e71-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="56e71-160">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="56e71-161">invitedUser</span><span class="sxs-lookup"><span data-stu-id="56e71-161">invitedUser</span></span>|[<span data-ttu-id="56e71-162">User</span><span class="sxs-lookup"><span data-stu-id="56e71-162">User</span></span>](user.md)|<span data-ttu-id="56e71-p108">El usuario creado como parte de la creación de la invitación. Solo lectura</span><span class="sxs-lookup"><span data-stu-id="56e71-p108">The user created as part of the invitation creation. Read-Only</span></span>|

## <a name="json-representation"></a><span data-ttu-id="56e71-165">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="56e71-165">JSON representation</span></span>
<span data-ttu-id="56e71-166">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="56e71-166">Here is a JSON representation of the resource</span></span>

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
