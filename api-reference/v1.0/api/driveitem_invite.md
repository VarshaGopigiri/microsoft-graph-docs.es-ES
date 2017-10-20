---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: "Enviar una invitación para obtener acceso a un elemento"
ms.openlocfilehash: 5be2060c190434c4b9d587d20fe68d69786b3aa5
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="send-a-sharing-invitation"></a><span data-ttu-id="2e4bb-102">Enviar una invitación para uso compartido</span><span class="sxs-lookup"><span data-stu-id="2e4bb-102">Send a sharing invitation</span></span>

<span data-ttu-id="2e4bb-p101">Envía una invitación para uso compartido de un objeto **DriveItem**. Una invitación para uso compartido proporciona permisos a los destinatarios y, de forma opcional, envía un correo electrónico a los destinatarios para notificarles que se ha compartido el elemento.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-p101">Sends a sharing invitation for a **DriveItem**. A sharing invitation provides permissions to the recipients and optionally sends an email to the recipients to notify them the item was shared.</span></span>

## <a name="permissions"></a><span data-ttu-id="2e4bb-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="2e4bb-105">Permissions</span></span>

<span data-ttu-id="2e4bb-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="2e4bb-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="2e4bb-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2e4bb-108">Permission type</span></span>      | <span data-ttu-id="2e4bb-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2e4bb-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="2e4bb-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2e4bb-110">Delegated (work or school account)</span></span> | <span data-ttu-id="2e4bb-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2e4bb-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="2e4bb-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2e4bb-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="2e4bb-113">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2e4bb-113">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="2e4bb-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2e4bb-114">Application</span></span> | <span data-ttu-id="2e4bb-115">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2e4bb-115">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="2e4bb-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2e4bb-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{drive-id}/items/{item-id}/invite
POST /groups/{group-id}/drive/items/{item-id}/invite
POST /me/drive/items/{item-id}/invite
POST /sites/{siteId}/drive/items/{itemId}/invite
POST /users/{userId}/drive/items/{itemId}/invite
```

## <a name="request-body"></a><span data-ttu-id="2e4bb-117">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="2e4bb-117">Request body</span></span>

<span data-ttu-id="2e4bb-118">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-118">In the request body, provide a JSON object with the following parameters.</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.inviteParameters", "scopes": "files.readwrite" } -->

```json
{
  "requireSignIn": false,
  "sendInvitation": false,
  "roles": [ "read | write"],
  "recipients": [
    { "@odata.type": "microsoft.graph.driveRecipient" },
    { "@odata.type": "microsoft.graph.driveRecipient" }
  ],
  "message": "string"
}
```

| <span data-ttu-id="2e4bb-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2e4bb-119">Parameter</span></span>        | <span data-ttu-id="2e4bb-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="2e4bb-120">Type</span></span>                                            | <span data-ttu-id="2e4bb-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="2e4bb-121">Description</span></span>                                                                                                |
|:-----------------|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e4bb-122">destinatarios</span><span class="sxs-lookup"><span data-stu-id="2e4bb-122">recipients</span></span>       | <span data-ttu-id="2e4bb-123">Collection([DriveRecipient](../resources/driverecipient.md))</span><span class="sxs-lookup"><span data-stu-id="2e4bb-123">Collection([DriveRecipient](../resources/driverecipient.md))</span></span> | <span data-ttu-id="2e4bb-124">Una colección de los destinatarios que recibirán acceso y la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-124">A collection of recipients who will receive access and the sharing invitation.</span></span>                                            |
| <span data-ttu-id="2e4bb-125">message</span><span class="sxs-lookup"><span data-stu-id="2e4bb-125">message</span></span>          | <span data-ttu-id="2e4bb-126">String</span><span class="sxs-lookup"><span data-stu-id="2e4bb-126">String</span></span>                                          | <span data-ttu-id="2e4bb-p103">Un mensaje con formato de texto sin formato que se incluye en la invitación para uso compartido. La longitud máxima es de 2000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-p103">A plain text formatted message that is included in the sharing invitation. Maximum length 2000 characters.</span></span> |
| <span data-ttu-id="2e4bb-129">requireSignIn</span><span class="sxs-lookup"><span data-stu-id="2e4bb-129">requireSignIn</span></span>    | <span data-ttu-id="2e4bb-130">Boolean</span><span class="sxs-lookup"><span data-stu-id="2e4bb-130">Boolean</span></span>                                         | <span data-ttu-id="2e4bb-131">Especifica si el destinatario de la invitación debe iniciar sesión para ver el elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-131">Specifies where the recipient of the invitation is required to sign-in to view the shared item.</span></span>            |
| <span data-ttu-id="2e4bb-132">sendInvitation</span><span class="sxs-lookup"><span data-stu-id="2e4bb-132">sendInvitation</span></span>   | <span data-ttu-id="2e4bb-133">Boolean</span><span class="sxs-lookup"><span data-stu-id="2e4bb-133">Boolean</span></span>                                         | <span data-ttu-id="2e4bb-134">Especifica si se genera un correo electrónico o una publicación (false) o si se acaba de crear el permiso (true).</span><span class="sxs-lookup"><span data-stu-id="2e4bb-134">Specifies if an email or post is generated (false) or if the permission is just created (true).</span></span>            |
| <span data-ttu-id="2e4bb-135">roles</span><span class="sxs-lookup"><span data-stu-id="2e4bb-135">roles</span></span>            | <span data-ttu-id="2e4bb-136">Collection(String)</span><span class="sxs-lookup"><span data-stu-id="2e4bb-136">Collection(String)</span></span>                              | <span data-ttu-id="2e4bb-137">Especifica los roles que se conceden a los destinatarios de la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-137">Specify the roles that are be granted to the recipients of the sharing invitation.</span></span>                         |

## <a name="example"></a><span data-ttu-id="2e4bb-138">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2e4bb-138">Example</span></span>

<span data-ttu-id="2e4bb-139">Este ejemplo envía una invitación para uso compartido a un usuario con la dirección de correo electrónico "ryan@contoso.org" y un mensaje sobre un archivo en el que se colabora.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-139">This example sends a sharing invitation to a user with email address "ryan@contoso.org" with a message about a file being collaborated on.</span></span>
<span data-ttu-id="2e4bb-140">La invitación concede a Ryan acceso de lectura y escritura al archivo.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-140">The invitation grants Ryan read-write access to the file.</span></span>

### <a name="http-request"></a><span data-ttu-id="2e4bb-141">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2e4bb-141">HTTP Request</span></span>

<span data-ttu-id="2e4bb-142">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-142">If successful, this method returns `200 OK` response code and [permission](../resources/permission.md) collection object in the response body.</span></span>

<!-- { "blockType": "request", "name": "send-sharing-invite", "@odata.type": "microsoft.graph.inviteParameters", "scopes": "files.readwrite", "target": "action" } -->

```http
POST /me/drive/items/{item-id}/invite
Content-type: application/json

{
  "recipients": [
    {
      "email": "ryan@contoso.org"
    }
  ],
  "message": "Here's the file that we're collaborating on.",
  "requireSignIn": true,
  "sendInvitation": true,
  "roles": [ "write" ]
}
```

### <a name="response"></a><span data-ttu-id="2e4bb-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e4bb-143">Response</span></span>

<span data-ttu-id="2e4bb-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-144">Here is an example of the response.</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.permission)", "truncated": true } -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "grantedTo": {
        "user": {
          "displayName": "Ryan Gregg",
          "id": "42F177F1-22C0-4BE3-900D-4507125C5C20"
        }
      },
      "id": "CCFC7CA3-7A19-4D57-8CEF-149DB9DDFA62",
      "invitation": {
        "email": "ryan@contoso.com",
        "signInRequired": true
      },
      "roles": [ "write" ]
    }
  ]
}
```

## <a name="remarks"></a><span data-ttu-id="2e4bb-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2e4bb-145">Remarks</span></span>

* <span data-ttu-id="2e4bb-146">Los objetos [Drives](../resources/drive.md) con un valor **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en el objeto DriveItem raíz.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-146">[Drives](../resources/drive.md) with a **driveType** of `personal` (OneDrive Personal) cannot create or modify permissions on the root DriveItem.</span></span>
* <span data-ttu-id="2e4bb-147">Para obtener una lista de los roles disponibles, consulte [Enumeración de roles](../resources/permission.md#roles-enumeration).</span><span class="sxs-lookup"><span data-stu-id="2e4bb-147">For a list of available roles, see [Roles enumeration](../resources/permission.md#roles-enumeration).</span></span>

## <a name="error-responses"></a><span data-ttu-id="2e4bb-148">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="2e4bb-148">Error Responses</span></span>

<span data-ttu-id="2e4bb-149">Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="2e4bb-149">Read the [Error Responses][error-response] topic for more information about how errors are returned.</span></span>


[error-response]: ../../../concepts/errors.md

<!-- {
  "type": "#page.annotation",
  "description": "Add permissions to an item and optionally send a sharing notification.",
  "keywords": "retrieve,item,metadata",
  "section": "documentation",
  "tocPath": "Sharing/Add permissions"
} -->
