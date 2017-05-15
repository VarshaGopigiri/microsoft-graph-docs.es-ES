# <a name="create-invitation"></a>Crear invitación

Use esta API para crear una [invitación](../resources/invitation.md). La invitación agrega un usuario externo a la organización.

Al crear una invitación, dispone de varias opciones:

1. En la creación de la invitación, Microsoft Graph puede enviar de forma automática un correo electrónico de invitación directamente al usuario invitado, o la aplicación puede usar la *inviteRedeemUrl* devuelta en la respuesta de la creación para diseñar su propia invitación (mediante el mecanismo de comunicación que quiera) para el usuario invitado. Si decide que Microsoft Graph envíe un correo electrónico de invitación automáticamente, puede controlar el contenido y el idioma del correo electrónico mediante [*invitedUserMessageInfo*](../resources/invitedusermessageinfo.md).
2. Cuando se invita al usuario, se crea una entidad de usuario (de userType Guest) y se puede usar ahora para controlar el acceso a los recursos. El usuario invitado tiene que pasar por el proceso de canje para tener acceso a los recursos a los que lo han invitado.

### <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes ámbitos para ejecutar esta API: *User.Invite.All*, *User.ReadWrite.All* o *Directory.ReadWrite.All*

### <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
POST /invitations
```
### <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Autorización  | Portador de <token>. Necesario.  |
| Content-Type  | application/json  |

### <a name="request-body"></a>Cuerpo de solicitud
En el cuerpo de la solicitud, proporcione una representación JSON de un objeto [invitation](../resources/invitation.md).

En la tabla siguiente, se muestran las propiedades necesarias al crear una invitación.

| Parámetro | Tipo | Descripción|
|:---------------|:--------|:----------|
|invitedUserEmailAddress |string | Dirección de correo electrónico del usuario al que invita.|
|inviteRedirectUrl |string |Dirección URL a la que se redirigirá al usuario después del canje.|


### <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `201, Created` y un objeto [invitation](../resources/invitation.md) en el cuerpo de la respuesta.

### <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
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

##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
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