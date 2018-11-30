---
title: Crear invitación
description: Use esta API para crear una invitación. La invitación agrega un usuario externo a la organización.
ms.openlocfilehash: 220b90cafdd7825dbb6dff9bb8635a51de2ee267
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090454"
---
# <a name="create-invitation"></a><span data-ttu-id="58180-104">Crear invitación</span><span class="sxs-lookup"><span data-stu-id="58180-104">Create invitation</span></span>

> <span data-ttu-id="58180-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="58180-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="58180-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="58180-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="58180-p103">Use esta API para crear una [invitación](../resources/invitation.md). La invitación agrega un usuario externo a la organización.</span><span class="sxs-lookup"><span data-stu-id="58180-p103">Use this API to create a new [invitation](../resources/invitation.md). Invitation adds an external user to the organization.</span></span>

<span data-ttu-id="58180-109">Al crear una invitación, dispone de varias opciones:</span><span class="sxs-lookup"><span data-stu-id="58180-109">When creating a new invitation you have several options available:</span></span>

1. <span data-ttu-id="58180-p104">En la creación de la invitación, Microsoft Graph puede enviar de forma automática un correo electrónico de invitación directamente al usuario invitado, o la aplicación puede usar la *inviteRedeemUrl* devuelta en la respuesta de la creación para diseñar su propia invitación (mediante el mecanismo de comunicación que quiera) para el usuario invitado. Si decide que Microsoft Graph envíe un correo electrónico de invitación automáticamente, puede controlar el contenido y el idioma del correo electrónico mediante [*invitedUserMessageInfo*](../resources/invitedusermessageinfo.md).</span><span class="sxs-lookup"><span data-stu-id="58180-p104">On invitation creation, Microsoft Graph can automatically send an invitation email directly to the invited user, or your app can use the *inviteRedeemUrl* returned in the creation response to craft your own invitation (through your communication mechanism of choice) to the invited user. If you decide to have Microsoft Graph send an invitation email automatically, you can control the content and language of the email using [*invitedUserMessageInfo*](../resources/invitedusermessageinfo.md).</span></span>
2. <span data-ttu-id="58180-p105">Cuando se invita al usuario, se crea una entidad de usuario (de userType Guest) y se puede usar ahora para controlar el acceso a los recursos. El usuario invitado tiene que pasar por el proceso de canje para tener acceso a los recursos a los que lo han invitado.</span><span class="sxs-lookup"><span data-stu-id="58180-p105">When the user is invited, a user entity (of userType Guest) is created and can now be used to control access to resources. The invited user has to go through the redemption process to access any resources he has been invited to.</span></span>

## <a name="permissions"></a><span data-ttu-id="58180-114">Permisos</span><span class="sxs-lookup"><span data-stu-id="58180-114">Permissions</span></span>
<span data-ttu-id="58180-p106">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="58180-p106">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>


|<span data-ttu-id="58180-117">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="58180-117">Permission type</span></span>      | <span data-ttu-id="58180-118">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="58180-118">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="58180-119">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="58180-119">Delegated (work or school account)</span></span> | <span data-ttu-id="58180-120">User.Invite.All, User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="58180-120">User.Invite.All, User.ReadWrite.All, Directory.ReadWrite.All</span></span>    |
|<span data-ttu-id="58180-121">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="58180-121">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="58180-122">No admitida.</span><span class="sxs-lookup"><span data-stu-id="58180-122">Not supported.</span></span>    |
|<span data-ttu-id="58180-123">Aplicación</span><span class="sxs-lookup"><span data-stu-id="58180-123">Application</span></span> | <span data-ttu-id="58180-124">User.Invite.All, User.ReadWrite.All, Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="58180-124">User.Invite.All, User.ReadWrite.All, Directory.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="58180-125">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="58180-125">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /invitations
```
## <a name="request-headers"></a><span data-ttu-id="58180-126">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="58180-126">Request headers</span></span>
| <span data-ttu-id="58180-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="58180-127">Header</span></span>       | <span data-ttu-id="58180-128">Valor</span><span class="sxs-lookup"><span data-stu-id="58180-128">Value</span></span> |
|:---------------|:--------|
| <span data-ttu-id="58180-129">Authorization</span><span class="sxs-lookup"><span data-stu-id="58180-129">Authorization</span></span>  | <span data-ttu-id="58180-p107">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="58180-p107">Bearer {token}. Required.</span></span>  |
| <span data-ttu-id="58180-132">Content-Type</span><span class="sxs-lookup"><span data-stu-id="58180-132">Content-Type</span></span>  | <span data-ttu-id="58180-133">application/json</span><span class="sxs-lookup"><span data-stu-id="58180-133">application/json</span></span>  |

## <a name="request-body"></a><span data-ttu-id="58180-134">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="58180-134">Request body</span></span>
<span data-ttu-id="58180-135">En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [invitation](../resources/invitation.md).</span><span class="sxs-lookup"><span data-stu-id="58180-135">In the request body, supply a JSON representation of an [invitation](../resources/invitation.md) object.</span></span>

<span data-ttu-id="58180-136">En la tabla siguiente, se muestran las propiedades necesarias al crear una invitación.</span><span class="sxs-lookup"><span data-stu-id="58180-136">The following table shows the properties that are required when you create a invitation.</span></span>

| <span data-ttu-id="58180-137">Parámetro</span><span class="sxs-lookup"><span data-stu-id="58180-137">Parameter</span></span> | <span data-ttu-id="58180-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="58180-138">Type</span></span> | <span data-ttu-id="58180-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="58180-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="58180-140">invitedUserEmailAddress</span><span class="sxs-lookup"><span data-stu-id="58180-140">invitedUserEmailAddress</span></span> |<span data-ttu-id="58180-141">string</span><span class="sxs-lookup"><span data-stu-id="58180-141">string</span></span> | <span data-ttu-id="58180-142">Dirección de correo electrónico del usuario al que invita.</span><span class="sxs-lookup"><span data-stu-id="58180-142">The email address of the user you are inviting.</span></span>|
|<span data-ttu-id="58180-143">inviteRedirectUrl</span><span class="sxs-lookup"><span data-stu-id="58180-143">inviteRedirectUrl</span></span> |<span data-ttu-id="58180-144">string</span><span class="sxs-lookup"><span data-stu-id="58180-144">string</span></span> |<span data-ttu-id="58180-145">Dirección URL a la que se redirigirá al usuario después del canje.</span><span class="sxs-lookup"><span data-stu-id="58180-145">The URL that the user will be redirected to after redemption.</span></span>|

## <a name="response"></a><span data-ttu-id="58180-146">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58180-146">Response</span></span>

<span data-ttu-id="58180-147">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [invitation](../resources/invitation.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="58180-147">If successful, this method returns `201 Created` response code and [invitation](../resources/invitation.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="58180-148">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="58180-148">Example</span></span>
##### <a name="request"></a><span data-ttu-id="58180-149">Solicitud</span><span class="sxs-lookup"><span data-stu-id="58180-149">Request</span></span>
<span data-ttu-id="58180-150">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="58180-150">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_user_from_users"
}-->
```http
POST https://graph.microsoft.com/beta/invitations
Content-type: application/json
Content-length: 551

{
  "invitedUserEmailAddress": "yyy@test.com",
  "inviteRedirectUrl": "https://myapp.com"
}
```

##### <a name="response"></a><span data-ttu-id="58180-151">Respuesta</span><span class="sxs-lookup"><span data-stu-id="58180-151">Response</span></span>
<span data-ttu-id="58180-p108">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="58180-p108">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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
