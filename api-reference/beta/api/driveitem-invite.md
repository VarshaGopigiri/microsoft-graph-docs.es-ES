---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Enviar una invitación para obtener acceso a un elemento
localization_priority: Normal
ms.openlocfilehash: 93fa30cc3e7999ba00bbcf591876c90253b77a7f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823936"
---
# <a name="send-a-sharing-invitation"></a><span data-ttu-id="4ef86-102">Enviar una invitación para uso compartido</span><span class="sxs-lookup"><span data-stu-id="4ef86-102">Send a sharing invitation</span></span>

> <span data-ttu-id="4ef86-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4ef86-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4ef86-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4ef86-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="4ef86-p102">Envía una invitación para uso compartido de un objeto **DriveItem**. Una invitación para uso compartido proporciona permisos a los destinatarios y, de forma opcional, envía un correo electrónico a los destinatarios para notificarles que se ha compartido el elemento.</span><span class="sxs-lookup"><span data-stu-id="4ef86-p102">Sends a sharing invitation for a **DriveItem**. A sharing invitation provides permissions to the recipients and optionally sends an email to the recipients to notify them the item was shared.</span></span>

## <a name="permissions"></a><span data-ttu-id="4ef86-107">Permisos</span><span class="sxs-lookup"><span data-stu-id="4ef86-107">Permissions</span></span>

<span data-ttu-id="4ef86-p103">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4ef86-p103">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4ef86-110">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4ef86-110">Permission type</span></span>      | <span data-ttu-id="4ef86-111">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4ef86-111">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="4ef86-112">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4ef86-112">Delegated (work or school account)</span></span> | <span data-ttu-id="4ef86-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4ef86-113">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="4ef86-114">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4ef86-114">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="4ef86-115">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4ef86-115">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="4ef86-116">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4ef86-116">Application</span></span> | <span data-ttu-id="4ef86-117">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4ef86-117">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="4ef86-118">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4ef86-118">HTTP request</span></span>

<!-- { "blockType": "ignored" } -->

```http
POST /drives/{drive-id}/items/{item-id}/invite
POST /groups/{group-id}/drive/items/{item-id}/invite
POST /me/drive/items/{item-id}/invite
POST /sites/{siteId}/drive/items/{itemId}/invite
POST /users/{userId}/drive/items/{itemId}/invite
```

## <a name="request-body"></a><span data-ttu-id="4ef86-119">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4ef86-119">Request body</span></span>

<span data-ttu-id="4ef86-120">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="4ef86-120">In the request body, provide a JSON object with the following parameters.</span></span>

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

| <span data-ttu-id="4ef86-121">Parámetro</span><span class="sxs-lookup"><span data-stu-id="4ef86-121">Parameter</span></span>        | <span data-ttu-id="4ef86-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="4ef86-122">Type</span></span>                                            | <span data-ttu-id="4ef86-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="4ef86-123">Description</span></span>                                                                                                |
|:-----------------|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ef86-124">destinatarios</span><span class="sxs-lookup"><span data-stu-id="4ef86-124">recipients</span></span>       | <span data-ttu-id="4ef86-125">Collection([DriveRecipient](../resources/driverecipient.md))</span><span class="sxs-lookup"><span data-stu-id="4ef86-125">Collection([DriveRecipient](../resources/driverecipient.md))</span></span> | <span data-ttu-id="4ef86-126">Una colección de los destinatarios que recibirán acceso y la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="4ef86-126">A collection of recipients who will receive access and the sharing invitation.</span></span>                                            |
| <span data-ttu-id="4ef86-127">message</span><span class="sxs-lookup"><span data-stu-id="4ef86-127">message</span></span>          | <span data-ttu-id="4ef86-128">String</span><span class="sxs-lookup"><span data-stu-id="4ef86-128">String</span></span>                                          | <span data-ttu-id="4ef86-p104">Un mensaje con formato de texto sin formato que se incluye en la invitación para uso compartido. La longitud máxima es de 2000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="4ef86-p104">A plain text formatted message that is included in the sharing invitation. Maximum length 2000 characters.</span></span> |
| <span data-ttu-id="4ef86-131">requireSignIn</span><span class="sxs-lookup"><span data-stu-id="4ef86-131">requireSignIn</span></span>    | <span data-ttu-id="4ef86-132">Boolean</span><span class="sxs-lookup"><span data-stu-id="4ef86-132">Boolean</span></span>                                         | <span data-ttu-id="4ef86-133">Especifica si el destinatario de la invitación debe iniciar sesión para ver el elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="4ef86-133">Specifies where the recipient of the invitation is required to sign-in to view the shared item.</span></span>            |
| <span data-ttu-id="4ef86-134">sendInvitation</span><span class="sxs-lookup"><span data-stu-id="4ef86-134">sendInvitation</span></span>   | <span data-ttu-id="4ef86-135">Boolean</span><span class="sxs-lookup"><span data-stu-id="4ef86-135">Boolean</span></span>                                         | <span data-ttu-id="4ef86-136">Especifica si se genera un correo electrónico o una publicación (false) o si se acaba de crear el permiso (true).</span><span class="sxs-lookup"><span data-stu-id="4ef86-136">Specifies if an email or post is generated (false) or if the permission is just created (true).</span></span>            |
| <span data-ttu-id="4ef86-137">roles</span><span class="sxs-lookup"><span data-stu-id="4ef86-137">roles</span></span>            | <span data-ttu-id="4ef86-138">Collection(String)</span><span class="sxs-lookup"><span data-stu-id="4ef86-138">Collection(String)</span></span>                              | <span data-ttu-id="4ef86-139">Especifica los roles que se conceden a los destinatarios de la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="4ef86-139">Specify the roles that are be granted to the recipients of the sharing invitation.</span></span>                         |

## <a name="example"></a><span data-ttu-id="4ef86-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4ef86-140">Example</span></span>

<span data-ttu-id="4ef86-141">Este ejemplo envía una invitación para uso compartido a un usuario con la dirección de correo electrónico "ryan@contoso.org" y un mensaje sobre un archivo en el que se colabora.</span><span class="sxs-lookup"><span data-stu-id="4ef86-141">This example sends a sharing invitation to a user with email address "ryan@contoso.org" with a message about a file being collaborated on.</span></span>
<span data-ttu-id="4ef86-142">La invitación concede a Ryan acceso de lectura y escritura al archivo.</span><span class="sxs-lookup"><span data-stu-id="4ef86-142">The invitation grants Ryan read-write access to the file.</span></span>

### <a name="http-request"></a><span data-ttu-id="4ef86-143">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4ef86-143">HTTP Request</span></span>

<span data-ttu-id="4ef86-144">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4ef86-144">If successful, this method returns `200 OK` response code and [permission](../resources/permission.md) collection object in the response body.</span></span>

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

### <a name="response"></a><span data-ttu-id="4ef86-145">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4ef86-145">Response</span></span>

<span data-ttu-id="4ef86-146">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4ef86-146">Here is an example of the response.</span></span>

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

## <a name="remarks"></a><span data-ttu-id="4ef86-147">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4ef86-147">Remarks</span></span>

* <span data-ttu-id="4ef86-148">Los objetos [Drives](../resources/drive.md) con un valor **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en el objeto DriveItem raíz.</span><span class="sxs-lookup"><span data-stu-id="4ef86-148">[Drives](../resources/drive.md) with a **driveType** of `personal` (OneDrive personal) cannot create or modify permissions on the root DriveItem.</span></span>
* <span data-ttu-id="4ef86-149">Para obtener una lista de los roles disponibles, consulte [Enumeración de roles](../resources/permission.md#roles-enumeration-values).</span><span class="sxs-lookup"><span data-stu-id="4ef86-149">For a list of available roles, see [Roles enumeration](../resources/permission.md#roles-enumeration-values).</span></span>

## <a name="error-responses"></a><span data-ttu-id="4ef86-150">Respuestas de error</span><span class="sxs-lookup"><span data-stu-id="4ef86-150">Error Responses</span></span>

<span data-ttu-id="4ef86-151">Lea el tema [Respuestas de error][error-response] para obtener más información sobre la manera en que se devuelven los errores.</span><span class="sxs-lookup"><span data-stu-id="4ef86-151">Read the [Error Responses][error-response] topic for more information about how errors are returned.</span></span>


[error-response]: /graph/errors

<!-- {
  "type": "#page.annotation",
  "description": "Add permissions to an item and optionally send a sharing notification.",
  "keywords": "retrieve,item,metadata",
  "section": "documentation",
  "tocPath": "Sharing/Add permissions"
} -->
