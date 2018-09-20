# <a name="get-outlook-messages-in-a-shared-or-delegated-folder"></a>Obtener los mensajes de Outlook en una carpeta compartida o delegada

<!-- remove similar content in other topics when ready to publish - list messages, get message, get mail folder.
These topics also have similar section - list events, get event, get calendar, list contacts, get contact, get contact folder.
-->

Outlook permite a los clientes compartir las carpetas de correo entre sí y proporcionar diferentes tipos de acceso a las carpetas individuales como "leer", "crear", "modificar" o "eliminar". Además, Outlook permite que un cliente elija a otro usuario para que actúe en su nombre y para que tenga acceso a carpetas de correo concretas o a todo su buzón. En Outlook, esto también se denomina "delegación".

Mediante programación, Microsoft Graph admite la recepción de mensajes en carpetas de correo que se han compartido con otros usuarios, así como obtener esas carpetas compartidas. La compatibilidad también se aplica a las carpetas que se han delegado.

Por ejemplo, Jorge ha compartido con Juan su bandeja de entrada y le ha dado acceso de lectura. Si Juan ha iniciado sesión en la aplicación y proporciona permisos delegados (Mail.Read.Shared o Mail.ReadWrite.Shared), la aplicación podrá acceder al correo de Jorge y a su bandeja de entrada, tal como se describe a continuación.

## <a name="get-a-message-in-the-shared-folder"></a>Obtener un mensaje en la carpeta compartida

Puede obtener un mensaje específico en la Bandeja de entrada de Jorge:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages/{id}
```

Cuando se complete correctamente, verá HTTP 200 OK y la instancia de [mensaje](../api-reference/v1.0/resources/message.md) identificada por `{id}` de la Bandeja de entrada de Jorge.

## <a name="get-all-messages-in-the-shared-folder"></a>Obtener todos los mensajes en la carpeta compartida

Obtenga todos los mensajes en la Bandeja de entrada de Jorge:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')/messages
```

Cuando se complete correctamente, verá HTTP 200 OK y una colección de instancias de [mensajes](../api-reference/v1.0/resources/message.md) en la Bandeja de entrada de Jorge.

## <a name="get-the-shared-folder"></a>Obtener la carpeta compartida

Obtenga la carpeta (Bandeja de entrada) que compartió Jorge con Juan.

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/mailfolders('Inbox')
```

Cuando se complete correctamente, verá HTTP 200 OK y la instancia [mailFolder](../api-reference/v1.0/resources/mailfolder.md) que representa la Bandeja de entrada de Jorge.

Se aplican las mismas capacidades de GET si Jorge había delegado a Juan acceso a la Bandeja de entrada de Jorge o había delegado Juan todo su buzón.

Si Jorge no ha compartido su bandeja de entrada con Juan ni le ha delegado su buzón, especificar el ID de usuario de Jorge o el nombre principal de usuario en esas operaciones GET producirá un error. 


## <a name="next-steps"></a>Siguientes pasos

Obtenga más información sobre:

- [¿Por qué debería realizar la integración con Correo de Outlook?](outlook-mail-concept-overview.md)
- [Usar la API de correo](../api-reference/v1.0/resources/mail_api_overview.md) y sus [casos de uso](../api-reference/v1.0/resources/mail_api_overview.md#common-use-cases) en la versión 1.0 de Microsoft Graph.