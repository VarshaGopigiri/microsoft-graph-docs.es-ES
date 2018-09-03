---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enviar una invitación para obtener acceso a un elemento
ms.openlocfilehash: c68289049503e70e04b2e403ca09cfc1f67e4096
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23268735"
---
# <a name="send-a-sharing-invitation"></a><span data-ttu-id="a023e-102">Enviar una invitación para uso compartido</span><span class="sxs-lookup"><span data-stu-id="a023e-102">Send a sharing invitation</span></span>

<span data-ttu-id="a023e-103">Envía una invitación para uso compartido para un **DriveItem**.</span><span class="sxs-lookup"><span data-stu-id="a023e-103">Sends a sharing invitation for a **DriveItem**.</span></span>
<span data-ttu-id="a023e-104">Una invitación para uso compartido proporciona permisos a los destinatarios y, opcionalmente, les envía un correo electrónico con un [vínculo para uso compartido][].</span><span class="sxs-lookup"><span data-stu-id="a023e-104">A sharing invitation provides permissions to the recipients and optionally sends them an email with a [sharing link][].</span></span>

## <a name="permissions"></a><span data-ttu-id="a023e-105">Permisos</span><span class="sxs-lookup"><span data-stu-id="a023e-105">Permissions</span></span>

<span data-ttu-id="a023e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="a023e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="a023e-108">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a023e-108">Permission type</span></span>      | <span data-ttu-id="a023e-109">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a023e-109">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="a023e-110">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a023e-110">Delegated (work or school account)</span></span> | <span data-ttu-id="a023e-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a023e-111">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="a023e-112">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a023e-112">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="a023e-113">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a023e-113">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="a023e-114">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a023e-114">Application</span></span> | <span data-ttu-id="a023e-115">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a023e-115">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="a023e-116">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a023e-116">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{drive-id}/items/{item-id}/invite
POST /groups/{group-id}/drive/items/{item-id}/invite
POST /me/drive/items/{item-id}/invite
POST /sites/{siteId}/drive/items/{itemId}/invite
POST /users/{userId}/drive/items/{itemId}/invite
```

## <a name="request-body"></a><span data-ttu-id="a023e-117">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a023e-117">Request body</span></span>

<span data-ttu-id="a023e-118">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="a023e-118">In the request body, provide a JSON object with the following parameters.</span></span>

<!-- { "blockType": "ignored", "scopes": "files.readwrite" } -->

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

| <span data-ttu-id="a023e-119">Parámetro</span><span class="sxs-lookup"><span data-stu-id="a023e-119">Parameter</span></span>        | <span data-ttu-id="a023e-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="a023e-120">Type</span></span>                           | <span data-ttu-id="a023e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="a023e-121">Description</span></span>
|:-----------------|:-------------------------------|:-------------------------
| <span data-ttu-id="a023e-122">destinatarios</span><span class="sxs-lookup"><span data-stu-id="a023e-122">recipients</span></span>       | <span data-ttu-id="a023e-123">Colección ([DriveRecipient][])</span><span class="sxs-lookup"><span data-stu-id="a023e-123">Collection([DriveRecipient][])</span></span> | <span data-ttu-id="a023e-124">Una colección de los destinatarios que recibirán acceso y la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="a023e-124">A collection of recipients who will receive access and the sharing invitation.</span></span>
| <span data-ttu-id="a023e-125">message</span><span class="sxs-lookup"><span data-stu-id="a023e-125">message</span></span>          | <span data-ttu-id="a023e-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="a023e-126">String</span></span>                         | <span data-ttu-id="a023e-p103">Un mensaje con formato de texto sin formato que se incluye en la invitación para uso compartido. La longitud máxima es de 2000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="a023e-p103">A plain text formatted message that is included in the sharing invitation. Maximum length 2000 characters.</span></span>
| <span data-ttu-id="a023e-129">requireSignIn</span><span class="sxs-lookup"><span data-stu-id="a023e-129">requireSignIn</span></span>    | <span data-ttu-id="a023e-130">Booleano</span><span class="sxs-lookup"><span data-stu-id="a023e-130">Boolean</span></span>                        | <span data-ttu-id="a023e-131">Especifica si el destinatario de la invitación debe iniciar sesión para ver el elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="a023e-131">Specifies where the recipient of the invitation is required to sign-in to view the shared item.</span></span>
| <span data-ttu-id="a023e-132">sendInvitation</span><span class="sxs-lookup"><span data-stu-id="a023e-132">sendInvitation</span></span>   | <span data-ttu-id="a023e-133">Booleano</span><span class="sxs-lookup"><span data-stu-id="a023e-133">Boolean</span></span>                        | <span data-ttu-id="a023e-134">Si es verdadero, se envía un [vínculo para uso compartido][] al destinatario.</span><span class="sxs-lookup"><span data-stu-id="a023e-134">If true, a [sharing link][] is sent to the recipient.</span></span> <span data-ttu-id="a023e-135">De lo contrario, se concede un permiso directamente sin enviar una notificación.</span><span class="sxs-lookup"><span data-stu-id="a023e-135">Otherwise, a permission is granted directly without sending a notification.</span></span>
| <span data-ttu-id="a023e-136">roles</span><span class="sxs-lookup"><span data-stu-id="a023e-136">roles</span></span>            | <span data-ttu-id="a023e-137">Colección (Cadena)</span><span class="sxs-lookup"><span data-stu-id="a023e-137">Collection(String)</span></span>             | <span data-ttu-id="a023e-138">Especifica los roles que se conceden a los destinatarios de la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="a023e-138">Specify the roles that are be granted to the recipients of the sharing invitation.</span></span>

## <a name="example"></a><span data-ttu-id="a023e-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a023e-139">Example</span></span>

<span data-ttu-id="a023e-140">Este ejemplo envía una invitación para uso compartido a un usuario con la dirección de correo electrónico "ryan@contoso.org" y un mensaje sobre un archivo en el que colabora.</span><span class="sxs-lookup"><span data-stu-id="a023e-140">This example sends a sharing invitation to a user with email address "ryan@contoso.org" with a message about a file being collaborated on.</span></span>
<span data-ttu-id="a023e-141">La invitación concede a Ryan acceso de lectura y escritura al archivo.</span><span class="sxs-lookup"><span data-stu-id="a023e-141">The invitation grants Ryan read-write access to the file.</span></span>

### <a name="http-request"></a><span data-ttu-id="a023e-142">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a023e-142">HTTP Request</span></span>

<span data-ttu-id="a023e-143">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a023e-143">If successful, this method returns `200 OK` response code and [permission](../resources/permission.md) collection object in the response body.</span></span>

<!-- { "blockType": "request", "name": "send-sharing-invite", "scopes": "files.readwrite", "target": "action" } -->

```json
POST /me/drive/items/{item-id}/invite
Content-type: application/json

{
  "recipients": [
    {
      "email": "ryan@contoso.com"
    }
  ],
  "message": "Here's the file that we're collaborating on.",
  "requireSignIn": true,
  "sendInvitation": true,
  "roles": [ "write" ]
}
```

### <a name="response"></a><span data-ttu-id="a023e-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a023e-144">Response</span></span>

<span data-ttu-id="a023e-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a023e-145">Here is an example of the response.</span></span>

<!-- { "blockType": "response", "@odata.type": "Collection(microsoft.graph.permission)", "truncated": true } -->

```json
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

## <a name="remarks"></a><span data-ttu-id="a023e-146">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a023e-146">Remarks</span></span>

* <span data-ttu-id="a023e-147">Los objetos [Drives](../resources/drive.md) con un valor **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en el objeto DriveItem raíz.</span><span class="sxs-lookup"><span data-stu-id="a023e-147">[Drives](../resources/drive.md) with a **driveType** of `personal` (OneDrive personal) cannot create or modify permissions on the root DriveItem.</span></span>
* <span data-ttu-id="a023e-148">Para obtener una lista de los roles disponibles, consulte [Enumeración de roles](../resources/permission.md#roles-enumeration).</span><span class="sxs-lookup"><span data-stu-id="a023e-148">For a list of available roles, see [Roles enumeration](../resources/permission.md#roles-enumeration).</span></span>

## <a name="error-responses"></a><span data-ttu-id="a023e-149">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="a023e-149">Error Responses</span></span>

<span data-ttu-id="a023e-150">Consulte [Respuestas de error][error-response] para obtener más información sobre la manera en que se reciben los errores.</span><span class="sxs-lookup"><span data-stu-id="a023e-150">Read the [Error Responses][error-response] topic for more information about how errors are returned.</span></span>


[driveRecipient]: ../resources/driverecipient.md
[DriveRecipient]: ../resources/driverecipient.md
[error-response]: ../../../concepts/errors.md
[vínculo para uso compartido]: ../resources/permission.md#sharing-links
[Create sharing link]: ../resources/permission.md#sharing-links

<!-- {
  "type": "#page.annotation",
  "description": "Add permissions to an item and optionally send a sharing notification.",
  "keywords": "retrieve,item,metadata",
  "section": "documentation",
  "tocPath": "Sharing/Add permissions"
} -->
