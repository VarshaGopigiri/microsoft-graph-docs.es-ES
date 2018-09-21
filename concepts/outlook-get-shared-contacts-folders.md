# <a name="get-outlook-contacts-in-a-shared-folder"></a>Obtener los contactos de Outlook en una carpeta compartida

Outlook permite a los clientes compartir las carpetas entre sí y proporcionar diferentes tipos de acceso como "leer", "crear", "modificar" o "eliminar" a las carpetas de contactos individuales. Además, Outlook permite que un cliente elija a otro usuario para que actúe en su nombre y para que tenga acceso a carpetas de correo concretas o a todo su buzón. En Outlook, esto también se denomina "delegación".

Mediante programación, Microsoft Graph permite obtener los contactos de las carpetas de contactos compartidas por otros usuarios, así como las propias carpetas compartidas. La compatibilidad también se aplica a las carpetas de un buzón delegado.

Por ejemplo, Garth tiene compartida con John una carpeta de contactos personalizada y concede a John acceso de lectura. Si John ha iniciado sesión en su aplicación y ha proporcionado permisos delegados (Contacts.Read.Shared o Contacts.ReadWrite.Shared), la aplicación podrá obtener acceso a carpeta de contactos personalizada de Garth y a los contactos de esa carpeta, tal y como se describe a continuación.

## <a name="get-a-contact-in-the-shared-folder"></a>Obtener un contacto de la carpeta compartida

Puede obtener un contacto específico de la carpeta de contactos personalizada que Garth ha compartido con John:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts/{id}
```

Si esto se completa correctamente, obtendrá HTTP 200 OK y la instancia de [contacto](../api-reference/v1.0/resources/contact.md) identificada por `{id}` de la carpeta de contactos compartida del Garth.

## <a name="get-all-contacts-in-the-shared-folder"></a>Obtener todos los contactos de la carpeta compartida

Obtenga todos los contactos de la carpeta de contactos compartida de Garth:

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}/contacts
```

Si esto se completa correctamente, obtendrá HTTP 200 OK y una colección de instancias de [contacto](../api-reference/v1.0/resources/contact.md) de la carpeta de contactos compartida de Garth.

## <a name="get-the-shared-folder"></a>Obtener la carpeta compartida

Obtenga la carpeta de contactos que Garth ha compartido con John.

<!-- { "blockType": "ignored" } -->
```http
GET users/{Garth-userId | Garth-userPrincipalName}/contactFolders/{folder-id}
```

Si esto se completa correctamente, obtendrá HTTP 200 OK y una instancia de [contactFolder](../api-reference/v1.0/resources/contactfolder.md) que representa la carpeta de contactos compartida de Garth.

Se aplicarían las mismas funciones de GET si Garth hubiera delegado a John todo su buzón.

Si Garth no ha compartido su carpeta de contactos con John ni ha delegado su buzón a John, especificar el ID. de usuario o el nombre principal de usuario de Garth en esas operaciones GET devolverá un error. 


## <a name="next-steps"></a>Siguientes pasos

Obtenga más información sobre:

- [¿Por qué integrar con contactos personales de Outlook?](outlook-contacts-concept-overview.md)
- [API de contactos](../api-reference/v1.0/resources/contact.md) en Microsoft Graph v1.0.