# <a name="send-a-sharing-invitation"></a><span data-ttu-id="48a66-101">Enviar una invitación para uso compartido</span><span class="sxs-lookup"><span data-stu-id="48a66-101">Send a sharing invitation</span></span>

<span data-ttu-id="48a66-p101">Envía una invitación para uso compartido de un objeto **DriveItem**. Una invitación para uso compartido proporciona permisos a los destinatarios y, de forma opcional, envía un correo electrónico a los destinatarios para notificarles que se ha compartido el elemento.</span><span class="sxs-lookup"><span data-stu-id="48a66-p101">Sends a sharing invitation for a **DriveItem**. A sharing invitation provides permissions to the recipients and optionally sends an email to the recipients to notify them the item was shared.</span></span>

## <a name="permissions"></a><span data-ttu-id="48a66-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="48a66-104">Permissions</span></span>
<span data-ttu-id="48a66-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="48a66-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="48a66-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="48a66-107">Permission type</span></span>      | <span data-ttu-id="48a66-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="48a66-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="48a66-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="48a66-109">Delegated (work or school account)</span></span> | <span data-ttu-id="48a66-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="48a66-110">Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All</span></span>    |
|<span data-ttu-id="48a66-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="48a66-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="48a66-112">Files.ReadWrite, Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="48a66-112">Files.ReadWrite, Files.ReadWrite.All</span></span>    |
|<span data-ttu-id="48a66-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="48a66-113">Application</span></span> | <span data-ttu-id="48a66-114">Files.ReadWrite.All, Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="48a66-114">Files.ReadWrite.All, Sites.ReadWrite.All</span></span> |

## <a name="http-request"></a><span data-ttu-id="48a66-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="48a66-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/items/{item-id}/invite
POST /drive/items/{item-id}/invite
POST /drives/{drive-id}/items/{item-id}/invite
POST /groups/{group-id}/drive/items/{item-id}/invite
```

## <a name="request-body"></a><span data-ttu-id="48a66-116">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="48a66-116">Request body</span></span>
<span data-ttu-id="48a66-117">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="48a66-117">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="48a66-118">Parámetro</span><span class="sxs-lookup"><span data-stu-id="48a66-118">Parameter</span></span>        | <span data-ttu-id="48a66-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="48a66-119">Type</span></span>                                            | <span data-ttu-id="48a66-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="48a66-120">Description</span></span>                                                                                                |
|:-----------------|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48a66-121">destinatarios</span><span class="sxs-lookup"><span data-stu-id="48a66-121">recipients</span></span>       | <span data-ttu-id="48a66-122">Collection([DriveRecipient](../resources/driverecipient.md))</span><span class="sxs-lookup"><span data-stu-id="48a66-122">Collection([DriveRecipient](../resources/driverecipient.md))</span></span> | <span data-ttu-id="48a66-123">Una colección de los destinatarios que recibirán acceso y la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="48a66-123">A collection of recipients who will receive access and the sharing invitation.</span></span>                                            |
| <span data-ttu-id="48a66-124">message</span><span class="sxs-lookup"><span data-stu-id="48a66-124">message</span></span>          | <span data-ttu-id="48a66-125">String</span><span class="sxs-lookup"><span data-stu-id="48a66-125">String</span></span>                                          | <span data-ttu-id="48a66-p103">Un mensaje con formato de texto sin formato que se incluye en la invitación para uso compartido. La longitud máxima es de 2000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="48a66-p103">A plain text formatted message that is included in the sharing invitation. Maximum length 2000 characters.</span></span> |
| <span data-ttu-id="48a66-128">requireSignIn</span><span class="sxs-lookup"><span data-stu-id="48a66-128">requireSignIn</span></span>    | <span data-ttu-id="48a66-129">Boolean</span><span class="sxs-lookup"><span data-stu-id="48a66-129">Boolean</span></span>                                         | <span data-ttu-id="48a66-130">Especifica si el destinatario de la invitación debe iniciar sesión para ver el elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="48a66-130">Specifies where the recipient of the invitation is required to sign-in to view the shared item.</span></span>            |
| <span data-ttu-id="48a66-131">sendInvitation</span><span class="sxs-lookup"><span data-stu-id="48a66-131">sendInvitation</span></span>   | <span data-ttu-id="48a66-132">Boolean</span><span class="sxs-lookup"><span data-stu-id="48a66-132">Boolean</span></span>                                         | <span data-ttu-id="48a66-133">Especifica si se genera un correo electrónico o una publicación (false) o si se acaba de crear el permiso (true).</span><span class="sxs-lookup"><span data-stu-id="48a66-133">Specifies if an email or post is generated (false) or if the permission is just created (true).</span></span>            |
| <span data-ttu-id="48a66-134">roles</span><span class="sxs-lookup"><span data-stu-id="48a66-134">roles</span></span>            | <span data-ttu-id="48a66-135">Collection(String)</span><span class="sxs-lookup"><span data-stu-id="48a66-135">Collection(String)</span></span>                              | <span data-ttu-id="48a66-136">Especifica los roles que se conceden a los destinatarios de la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="48a66-136">Specify the roles that are be granted to the recipients of the sharing invitation.</span></span>                         |

## <a name="response"></a><span data-ttu-id="48a66-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48a66-137">Response</span></span>

<span data-ttu-id="48a66-138">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48a66-138">If successful, this method returns `200 OK` response code and [permission](../resources/permission.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="48a66-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="48a66-139">Example</span></span>
<span data-ttu-id="48a66-140">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="48a66-140">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="48a66-141">Solicitud</span><span class="sxs-lookup"><span data-stu-id="48a66-141">Request</span></span>
<span data-ttu-id="48a66-142">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="48a66-142">Here is an example of the request.</span></span>

<!-- {
  "blockType": "request",
  "name": "item_invite"
}-->
```http
POST https://graph.microsoft.com/v1.0/drive/items/{item-id}/invite
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

##### <a name="response"></a><span data-ttu-id="48a66-143">Respuesta</span><span class="sxs-lookup"><span data-stu-id="48a66-143">Response</span></span>
<span data-ttu-id="48a66-144">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="48a66-144">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.permission",
  "isCollection": true
} -->
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

## <a name="remarks"></a><span data-ttu-id="48a66-145">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48a66-145">Remarks</span></span>

* <span data-ttu-id="48a66-146">Los [Drives](../resources/drive.md) con un **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en el objeto DriveItem raíz.</span><span class="sxs-lookup"><span data-stu-id="48a66-146">[Drives](../resources/drive.md) with a **driveType** of `personal` (OneDrive Personal) cannot create or modify permissions on the root DriveItem.</span></span> 
* <span data-ttu-id="48a66-147">Para obtener una lista de los roles disponibles, consulte [Enumeración de roles](../resources/permission.md#roles-enumeration).</span><span class="sxs-lookup"><span data-stu-id="48a66-147">For a list of available roles, see [Roles enumeration](../resources/permission.md#roles-enumeration).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "item: invite",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
