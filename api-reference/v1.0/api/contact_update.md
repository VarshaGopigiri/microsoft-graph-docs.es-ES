# <a name="update-contact"></a>Actualizar contacto

Actualiza las propiedades de un objeto de contacto.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Contacts.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Contacts.ReadWrite    |
|Aplicación | Contacts.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) predeterminado de un usuario.
```http
PATCH /me/contacts/{id}
PATCH /users/{id | userPrincipalName}/contacts/{id}
```
Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.
```http
PATCH /me/contactFolders/{id}/contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
Un [contact](../resources/contact.md) contenido en una carpeta secundaria de una [contactFolder](../resources/mailfolder.md). En el ejemplo, siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.
```http
PATCH /me/contactFolder/{id}/childFolders/{id}/.../contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/childFolders/{id}/contacts/{id}
```
## <a name="request-headers"></a>Encabezados de solicitud
| Encabezado       | Valor |
|:---------------|:--------|
| Authorization  | {token} de portador. Obligatorio.  |
| Content-Type  | application/json. Obligatorio.  |

## <a name="request-body"></a>Cuerpo de la solicitud
En el cuerpo de la solicitud, proporcione los valores de los campos relevantes que deben actualizarse. Las propiedades existentes que no se incluyan en el cuerpo de la solicitud mantendrán los valores anteriores o se recalcularán según los cambios efectuados en otros valores de propiedad. Para obtener el mejor rendimiento, no debe incluir valores existentes que no hayan cambiado.

| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|assistantName|String|El nombre del ayudante del contacto.|
|birthday|DateTimeOffset|El cumpleaños del contacto.|
|businessAddress|[PhysicalAddress](../resources/physicaladdress.md)|La dirección del trabajo del contacto.|
|businessHomePage|String|La página principal de la empresa del contacto.|
|businessPhones|String|Los números de teléfono del trabajo del contacto.|
|categories|String|Las categorías asociadas con el contacto.|
|children|String|Los nombres de los hijos del contacto.|
|companyName|String|El nombre de la empresa del contacto.|
|department|String|El departamento del contacto.|
|displayName|String|El nombre para mostrar del contacto.|
|emailAddresses|Colección [EmailAddress](../resources/emailaddress.md)|Las direcciones de correo electrónico del contacto.|
|fileAs|String|El nombre con el que se ha archivado el contacto.|
|generation|String|La generación del contacto.|
|givenName|String|El nombre del contacto.|
|homeAddress|[PhysicalAddress](../resources/physicaladdress.md)|La dirección particular del contacto.|
|homePhones|Colección String|Los números de teléfono particular del contacto.|
|imAddresses|String|Las direcciones de mensajería instantánea (MI) del contacto.|
|initials|String|Las iniciales del contacto.|
|jobTitle|String|El puesto del contacto.|
|manager|String|El nombre del administrador del contacto.
|middleName|String|El segundo nombre del contacto.|
|mobilePhone|String|El número de teléfono móvil del contacto.|
|nickName|String|El sobrenombre del contacto.|
|officeLocation|String|La ubicación de la oficina del contacto.|
|otherAddress|[PhysicalAddress](../resources/physicaladdress.md)|Otras direcciones del contacto.|
|parentFolderId|String|El identificador de la carpeta principal del contacto.|
|personalNotes|String|Las notas del usuario sobre el contacto.|
|profession|String|La profesión del contacto.|
|spouseName|String|El nombre del cónyuge del contacto.|
|surname|String|Los apellidos del contacto.|
|title|String|El título del contacto.|
|yomiCompanyName|String|El nombre fonético japonés de la empresa del contacto. Esta propiedad es opcional.|
|yomiGivenName|String|El nombre (nombre de pila) fonético japonés del contacto. Esta propiedad es opcional.|
|yomiSurname|String|El apellido fonético japonés del contacto. Esta propiedad es opcional.|

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [contact](../resources/contact.md) actualizado en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
<!-- {
  "blockType": "request",
  "name": "update_contact"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/me/contacts/{id}
Content-type: application/json
Content-length: 1977

{
  "homeAddress": {
    "street": "123 Some street",
    "city": "Seattle",
    "state": "WA",
    "postalCode": "98121"
  },
  "birthday": "1974-07-22"
}
```
##### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact"
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 1977

{
  "id": "AAMkAGI2THk0AAA=",
  "createdDateTime": "2014-10-19T23:08:24Z",
  "lastModifiedDateTime": "2014-10-19T23:08:24Z",
  "changeKey": "EQAAABYAAACd9nJ/tVysQos2hTfspaWRAAADTIa4",
  "categories": [],
  "parentFolderId": "AAMkAGI2AAEOAAA=",
  "birthday": "1974-07-22",
  "fileAs": "Fort, Garth",
  "displayName": "Garth Fort",
  "givenName": "Garth",
  "initials": "G.F.",
  "middleName": null,
  "nickName": "Garth",
  "surname": "Fort",
  "title": null,
  "yomiGivenName": null,
  "yomiSurname": null,
  "yomiCompanyName": null,
  "generation": null,
  "emailAddresses": [
    {
      "name": "Garth",
      "address": "garth@a830edad9050849NDA1.onmicrosoft.com"
    }
  ],
  "imAddresses": [
    "sip:garthf@a830edad9050849nda1.onmicrosoft.com"
  ],
  "jobTitle": "Web Marketing Manager",
  "companyName": "Contoso, Inc.",
  "department": "Sales & Marketing",
  "officeLocation": "20/1101",
  "profession": null,
  "businessHomePage": "http://www.contoso.com",
  "assistantName": null,
  "manager": null,
  "homePhones": [],
  "mobilePhone": null,
  "businessPhones": [
    "+1 918 555 0101"
  ],
  "homeAddress": {
    "street": "123 Some street",
    "city": "Seattle",
    "state": "WA",
    "postalCode": "98121"
  },
  "businessAddress": {
      "street": "10 Contoso Way",
      "city": "Redmond",
      "state": "WA",
      "countryOrRegion": "USA",
      "postalCode": "98075"  
  },
  "otherAddress": {},
  "spouseName": null,
  "personalNotes": null,
  "children": []
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
