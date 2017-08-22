# <a name="send-a-sharing-invitation"></a><span data-ttu-id="2cdaf-101">Enviar una invitación para uso compartido</span><span class="sxs-lookup"><span data-stu-id="2cdaf-101">Send a sharing invitation</span></span>

<span data-ttu-id="2cdaf-p101">Envía una invitación para uso compartido de un objeto **DriveItem**. Una invitación para uso compartido proporciona permisos a los destinatarios y, de forma opcional, envía un correo electrónico a los destinatarios para notificarles que se ha compartido el elemento.</span><span class="sxs-lookup"><span data-stu-id="2cdaf-p101">Sends a sharing invitation for a **DriveItem**. A sharing invitation provides permissions to the recipients and optionally sends an email to the recipients to notify them the item was shared.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2cdaf-104">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2cdaf-104">Prerequisites</span></span>
<span data-ttu-id="2cdaf-105">Se requiere uno de los siguientes **ámbitos** para ejecutar esta API:</span><span class="sxs-lookup"><span data-stu-id="2cdaf-105">One of the following **scopes** is required to execute this API:</span></span>

* <span data-ttu-id="2cdaf-106">Files.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2cdaf-106">Files.ReadWrite</span></span>
* <span data-ttu-id="2cdaf-107">Files.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2cdaf-107">Files.ReadWrite.All</span></span>
* <span data-ttu-id="2cdaf-108">Sites.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2cdaf-108">Sites.ReadWrite.All</span></span>

## <a name="http-request"></a><span data-ttu-id="2cdaf-109">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2cdaf-109">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/items/{item-id}/invite
POST /drive/items/{item-id}/invite
POST /drives/{drive-id}/items/{item-id}/invite
POST /groups/{group-id}/drive/items/{item-id}/invite
```

## <a name="request-body"></a><span data-ttu-id="2cdaf-110">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="2cdaf-110">Request body</span></span>
<span data-ttu-id="2cdaf-111">En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.</span><span class="sxs-lookup"><span data-stu-id="2cdaf-111">In the request body, provide a JSON object with the following parameters.</span></span>

| <span data-ttu-id="2cdaf-112">Parámetro</span><span class="sxs-lookup"><span data-stu-id="2cdaf-112">Parameter</span></span>        | <span data-ttu-id="2cdaf-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="2cdaf-113">Type</span></span>                                            | <span data-ttu-id="2cdaf-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cdaf-114">Description</span></span>                                                                                                |
|:-----------------|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cdaf-115">destinatarios</span><span class="sxs-lookup"><span data-stu-id="2cdaf-115">recipients</span></span>       | <span data-ttu-id="2cdaf-116">Collection([DriveRecipient](../resources/driverecipient.md))</span><span class="sxs-lookup"><span data-stu-id="2cdaf-116">Collection([DriveRecipient](../resources/driverecipient.md))</span></span> | <span data-ttu-id="2cdaf-117">Una colección de los destinatarios que recibirán acceso y la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="2cdaf-117">A collection of recipients who will receive access and the sharing invitation.</span></span>                                            |
| <span data-ttu-id="2cdaf-118">message</span><span class="sxs-lookup"><span data-stu-id="2cdaf-118">message</span></span>          | <span data-ttu-id="2cdaf-119">String</span><span class="sxs-lookup"><span data-stu-id="2cdaf-119">String</span></span>                                          | <span data-ttu-id="2cdaf-p102">Un mensaje con formato de texto sin formato que se incluye en la invitación para uso compartido. La longitud máxima es de 2000 caracteres.</span><span class="sxs-lookup"><span data-stu-id="2cdaf-p102">A plain text formatted message that is included in the sharing invitation. Maximum length 2000 characters.</span></span> |
| <span data-ttu-id="2cdaf-122">requireSignIn</span><span class="sxs-lookup"><span data-stu-id="2cdaf-122">requireSignIn</span></span>    | <span data-ttu-id="2cdaf-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="2cdaf-123">Boolean</span></span>                                         | <span data-ttu-id="2cdaf-124">Especifica si el destinatario de la invitación debe iniciar sesión para ver el elemento compartido.</span><span class="sxs-lookup"><span data-stu-id="2cdaf-124">Specifies where the recipient of the invitation is required to sign-in to view the shared item.</span></span>            |
| <span data-ttu-id="2cdaf-125">sendInvitation</span><span class="sxs-lookup"><span data-stu-id="2cdaf-125">sendInvitation</span></span>   | <span data-ttu-id="2cdaf-126">Boolean</span><span class="sxs-lookup"><span data-stu-id="2cdaf-126">Boolean</span></span>                                         | <span data-ttu-id="2cdaf-127">Especifica si se genera un correo electrónico o una publicación (false) o si se acaba de crear el permiso (true).</span><span class="sxs-lookup"><span data-stu-id="2cdaf-127">Specifies if an email or post is generated (false) or if the permission is just created (true).</span></span>            |
| <span data-ttu-id="2cdaf-128">roles</span><span class="sxs-lookup"><span data-stu-id="2cdaf-128">roles</span></span>            | <span data-ttu-id="2cdaf-129">Collection(String)</span><span class="sxs-lookup"><span data-stu-id="2cdaf-129">Collection(String)</span></span>                              | <span data-ttu-id="2cdaf-130">Especifica los roles que se conceden a los destinatarios de la invitación para uso compartido.</span><span class="sxs-lookup"><span data-stu-id="2cdaf-130">Specify the roles that are be granted to the recipients of the sharing invitation.</span></span>                         |

## <a name="response"></a><span data-ttu-id="2cdaf-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2cdaf-131">Response</span></span>

<span data-ttu-id="2cdaf-132">Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [permission](../resources/permission.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2cdaf-132">If successful, this method returns `200 OK` response code and [permission](../resources/permission.md) collection object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2cdaf-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2cdaf-133">Example</span></span>
<span data-ttu-id="2cdaf-134">Aquí tiene un ejemplo de cómo llamar a esta API.</span><span class="sxs-lookup"><span data-stu-id="2cdaf-134">Here is an example of how to call this API.</span></span>

##### <a name="request"></a><span data-ttu-id="2cdaf-135">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2cdaf-135">Request</span></span>
<span data-ttu-id="2cdaf-136">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2cdaf-136">Here is an example of the request.</span></span>

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

##### <a name="response"></a><span data-ttu-id="2cdaf-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2cdaf-137">Response</span></span>
<span data-ttu-id="2cdaf-138">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2cdaf-138">Here is an example of the response.</span></span>
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

## <a name="remarks"></a><span data-ttu-id="2cdaf-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2cdaf-139">Remarks</span></span>

* <span data-ttu-id="2cdaf-140">Los [Drives](../resources/drive.md) con un **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en el objeto DriveItem raíz.</span><span class="sxs-lookup"><span data-stu-id="2cdaf-140">[Drives](../resources/drive.md) with a **driveType** of `personal` (OneDrive Personal) cannot create or modify permissions on the root DriveItem.</span></span> 
* <span data-ttu-id="2cdaf-141">Para obtener una lista de los roles disponibles, consulte [Enumeración de roles](../resources/permission.md#roles-enumeration).</span><span class="sxs-lookup"><span data-stu-id="2cdaf-141">For a list of available roles, see [Roles enumeration](../resources/permission.md#roles-enumeration).</span></span>

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "item: invite",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
