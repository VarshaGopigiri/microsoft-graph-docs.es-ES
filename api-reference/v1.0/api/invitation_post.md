# <a name="create-invitation"></a><span data-ttu-id="31369-101">Crear invitación</span><span class="sxs-lookup"><span data-stu-id="31369-101">Create invitation</span></span>

<span data-ttu-id="31369-p101">Use esta API para crear una [invitación](../resources/invitation.md). La invitación agrega un usuario externo a la organización.</span><span class="sxs-lookup"><span data-stu-id="31369-p101">Use this API to create a new [invitation](../resources/invitation.md). Invitation adds an external user to the organization.</span></span>

<span data-ttu-id="31369-104">Al crear una invitación, dispone de varias opciones:</span><span class="sxs-lookup"><span data-stu-id="31369-104">When creating a new invitation you have several options available:</span></span>

1. <span data-ttu-id="31369-p102">En la creación de la invitación, Microsoft Graph puede enviar de forma automática un correo electrónico de invitación directamente al usuario invitado, o la aplicación puede usar la *inviteRedeemUrl* devuelta en la respuesta de la creación para diseñar su propia invitación (mediante el mecanismo de comunicación que quiera) para el usuario invitado. Si decide que Microsoft Graph envíe un correo electrónico de invitación automáticamente, puede controlar el contenido y el idioma del correo electrónico mediante [*invitedUserMessageInfo*](../resources/invitedusermessageinfo.md).</span><span class="sxs-lookup"><span data-stu-id="31369-p102">On invitation creation, Microsoft Graph can automatically send an invitation email directly to the invited user, or your app can use the *inviteRedeemUrl* returned in the creation response to craft your own invitation (through your communication mechanism of choice) to the invited user. If you decide to have Microsoft Graph send an invitation email automatically, you can control the content and language of the email using [*invitedUserMessageInfo*](../resources/invitedusermessageinfo.md).</span></span>
2. <span data-ttu-id="31369-p103">Cuando se invita al usuario, se crea una entidad de usuario (de userType Guest) y se puede usar ahora para controlar el acceso a los recursos. El usuario invitado tiene que pasar por el proceso de canje para tener acceso a los recursos a los que lo han invitado.</span><span class="sxs-lookup"><span data-stu-id="31369-p103">When the user is invited, a user entity (of userType Guest) is created and can now be used to control access to resources. The invited user has to go through the redemption process to access any resources he has been invited to.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="31369-109">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="31369-109">Prerequisites</span></span>
<span data-ttu-id="31369-110">Se requiere uno de los siguientes ámbitos para ejecutar esta API: *User.Invite.All*, *User.ReadWrite.All* o *Directory.ReadWrite.All*</span><span class="sxs-lookup"><span data-stu-id="31369-110">One of the following scopes is required to execute this API: *User.Invite.All* or *User.ReadWrite.All*  or *Directory.ReadWrite.All*</span></span>

## <a name="http-request"></a><span data-ttu-id="31369-111">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="31369-111">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /invitations
```
## <a name="request-headers"></a><span data-ttu-id="31369-112">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="31369-112">Request headers</span></span>
| <span data-ttu-id="31369-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="31369-113">Header</span></span>       | <span data-ttu-id="31369-114">Valor</span><span class="sxs-lookup"><span data-stu-id="31369-114">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="31369-115">Authorization</span><span class="sxs-lookup"><span data-stu-id="31369-115">Authorization</span></span>  | <span data-ttu-id="31369-p104">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="31369-p104">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="31369-118">Content-Type</span><span class="sxs-lookup"><span data-stu-id="31369-118">Content-Type</span></span>  | <span data-ttu-id="31369-119">application/json</span><span class="sxs-lookup"><span data-stu-id="31369-119">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="31369-120">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="31369-120">Request body</span></span>
<span data-ttu-id="31369-121">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [invitation](../resources/invitation.md).</span><span class="sxs-lookup"><span data-stu-id="31369-121">In the request body, supply a JSON representation of an [invitation](../resources/invitation.md) object.</span></span>

<span data-ttu-id="31369-122">En la tabla siguiente, se muestran las propiedades necesarias al crear una invitación.</span><span class="sxs-lookup"><span data-stu-id="31369-122">The following table shows the properties that are required when you create a invitation.</span></span>

| <span data-ttu-id="31369-123">Parámetro</span><span class="sxs-lookup"><span data-stu-id="31369-123">Parameter</span></span> | <span data-ttu-id="31369-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="31369-124">Type</span></span> | <span data-ttu-id="31369-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="31369-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="31369-126">invitedUserEmailAddress</span><span class="sxs-lookup"><span data-stu-id="31369-126">invitedUserEmailAddress</span></span> |<span data-ttu-id="31369-127">string</span><span class="sxs-lookup"><span data-stu-id="31369-127">string</span></span> | <span data-ttu-id="31369-128">Dirección de correo electrónico del usuario al que invita.</span><span class="sxs-lookup"><span data-stu-id="31369-128">The email address of the user you are inviting.</span></span>|
|<span data-ttu-id="31369-129">inviteRedirectUrl</span><span class="sxs-lookup"><span data-stu-id="31369-129">inviteRedirectUrl</span></span> |<span data-ttu-id="31369-130">string</span><span class="sxs-lookup"><span data-stu-id="31369-130">string</span></span> |<span data-ttu-id="31369-131">Dirección URL a la que se redirigirá al usuario después del canje.</span><span class="sxs-lookup"><span data-stu-id="31369-131">The URL that the user will be redirected to after redemption.</span></span>|

## <a name="response"></a><span data-ttu-id="31369-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31369-132">Response</span></span>

<span data-ttu-id="31369-133">Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y un objeto [invitation](../resources/invitation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="31369-133">If successful, this method returns `201, Created` response code and [invitation](../resources/invitation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="31369-134">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="31369-134">Example</span></span>
##### <a name="request"></a><span data-ttu-id="31369-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="31369-135">Request</span></span>
<span data-ttu-id="31369-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="31369-136">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_user_from_users"
}-->
```http
POST https://graph.microsoft.com/v1.0/invitations
Content-type: application/json
Content-length: 551

{
  "invitedUserEmailAddress": "yyy@test.com",
  "inviteRedirectUrl": "https://myapp.com"
}
```

##### <a name="response"></a><span data-ttu-id="31369-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="31369-137">Response</span></span>
<span data-ttu-id="31369-p105">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="31369-p105">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.invitations"
} -->
```http
HTTP/1.1 201 OK
Content-type: application/json
Content-length: 551

{
  "id": "7b92124c-9fa9-406f-8b8e-225df8376ba9",
  "inviteRedeemUrl": "https://invitations.microsoft.com/redeem/?tenant=04dcc6ab-388a-4559-b527-fbec656300ea&user=7b92124c-9fa9-406f-8b8e-225df8376ba9&ticket=VV9dmiExBsfRIVNFjb9ITj9VXAd07Ypv4gTg%2f8PiuJs%3d&lc=1033&ver=2.0",
  "invitedUserDisplayName": "yyy",
  "invitedUserEmailAddress": "yyy@test.com",
  "sendInvitationMessage": false,
  "invitedUserMessageInfo": {
     "messageLanguage": null,
     "ccRecipients": [
          {
             "emailAddress": {
                 "name": null,
                 "address": null
              }
          }
     ],
     "customizedMessageBody": null
  },
  "inviteRedirectUrl": "https://myapp.com/",
  "status": "Completed",
  "invitedUser":  [ {  "id": "243b1de4-ad9f-421c-a933-d55305fb165d" } ]
}
```
