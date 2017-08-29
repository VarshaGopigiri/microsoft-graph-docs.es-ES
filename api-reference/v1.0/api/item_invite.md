# <a name="send-a-sharing-invitation"></a>Enviar una invitación para uso compartido

Envía una invitación para uso compartido de un objeto **DriveItem**. Una invitación para uso compartido proporciona permisos a los destinatarios y, de forma opcional, envía un correo electrónico a los destinatarios para notificarles que se ha compartido el elemento.

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Files.ReadWrite, Files.ReadWrite.All, Sites.ReadWrite.All    |
|Delegado (cuenta personal de Microsoft) | Files.ReadWrite, Files.ReadWrite.All    |
|Aplicación | Files.ReadWrite.All, Sites.ReadWrite.All |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /me/drive/items/{item-id}/invite
POST /drive/items/{item-id}/invite
POST /drives/{drive-id}/items/{item-id}/invite
POST /groups/{group-id}/drive/items/{item-id}/invite
```

## <a name="request-body"></a>Cuerpo de solicitud
En el cuerpo de la solicitud, proporcione un objeto JSON con los siguientes parámetros.

| Parámetro        | Tipo                                            | Descripción                                                                                                |
|:-----------------|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| destinatarios       | Collection([DriveRecipient](../resources/driverecipient.md)) | Una colección de los destinatarios que recibirán acceso y la invitación para uso compartido.                                            |
| message          | String                                          | Un mensaje con formato de texto sin formato que se incluye en la invitación para uso compartido. La longitud máxima es de 2000 caracteres. |
| requireSignIn    | Boolean                                         | Especifica si el destinatario de la invitación debe iniciar sesión para ver el elemento compartido.            |
| sendInvitation   | Boolean                                         | Especifica si se genera un correo electrónico o una publicación (false) o si se acaba de crear el permiso (true).            |
| roles            | Collection(String)                              | Especifica los roles que se conceden a los destinatarios de la invitación para uso compartido.                         |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve el código de respuesta `200 OK` y el objeto de colección [permission](../resources/permission.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
Aquí tiene un ejemplo de cómo llamar a esta API.

##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.

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

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta.
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

## <a name="remarks"></a>Comentarios

* Los [Drives](../resources/drive.md) con un **driveType** de `personal` (OneDrive Personal) no pueden crear ni modificar permisos en el objeto DriveItem raíz. 
* Para obtener una lista de los roles disponibles, consulte [Enumeración de roles](../resources/permission.md#roles-enumeration).

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "item: invite",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
