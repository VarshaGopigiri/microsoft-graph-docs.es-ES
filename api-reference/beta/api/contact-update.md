---
title: Actualizar contacto
description: Actualizar las propiedades del objeto de contacto.
author: angelgolfer-ms
ms.openlocfilehash: d25efb55a090c4c0b5fa750b64a0b2a905327a76
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27334107"
---
# <a name="update-contact"></a>Actualizar contacto

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Actualizar las propiedades del objeto de contacto.
## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Contacts.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Contacts.ReadWrite    |
|Aplicación | Contacts.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->Un [contacto](../resources/contact.md) desde de predeterminado del usuario [contactFolder](../resources/contactfolder.md).
```http
PATCH /me/contacts/{id}
PATCH /users/{id | userPrincipalName}/contacts/{id}
```
Un [contact](../resources/contact.md) desde la [contactFolder](../resources/contactfolder.md) de nivel superior de un usuario.
```http
PATCH /me/contactFolders/{id}/contacts/{id}
PATCH /users/{id | userPrincipalName}/contactFolders/{id}/contacts/{id}
```
[Póngase en contacto con](../resources/contact.md) contenidos en una carpeta secundaria de un [contactFolder](../resources/mailfolder.md).  En el ejemplo siguiente se muestra un nivel de anidamiento, pero un contacto puede estar ubicado en un elemento secundario de un elemento secundario y así sucesivamente.
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
|categories|String|Las categorías asociadas con el contacto.|
|children|String||
|companyName|String|El nombre de la empresa del contacto.|
|department|String|El departamento del contacto.|
|displayName|String|El nombre para mostrar del contacto. Tenga en cuenta que las actualizaciones posteriores a otras propiedades pueden causar un valor generado automáticamente sobrescribir el valor de displayName que haya especificado. Para conservar un valor existente, siempre incluirla como displayName en una operación de actualización.|
|emailAddresses|colección de [typedEmailAddress](../resources/typedemailaddress.md)|Las direcciones de correo electrónico del contacto.|
|fileAs|String|El nombre con el que se ha archivado el contacto.|
|gender |String |Género del contacto. |
|generation|String|La generación del contacto.|
|givenName|String|El nombre del contacto.|
|imAddresses|String|Las direcciones de mensajería instantánea (MI) del contacto.|
|initials|String|Las iniciales del contacto.|
|jobTitle|String|El puesto del contacto.|
|manager|String|El nombre del administrador del contacto.
|middleName|String|El segundo nombre del contacto.|
|nickName|String|El sobrenombre del contacto.|
|officeLocation|String|La ubicación de la oficina del contacto.|
|parentFolderId|String|El identificador de la carpeta principal del contacto.|
|personalNotes|String|Las notas del usuario sobre el contacto.|
|phones |Colección [phone](../resources/phone.md) |Números de teléfono asociados con el contacto, por ejemplo, teléfono particular, teléfono móvil y teléfono del trabajo. |
|postalAddresses |colección [physicalAddress](../resources/physicaladdress.md) |Direcciones asociadas con el contacto, por ejemplo, home dirección y dirección de la empresa. |
|profession|String|La profesión del contacto.|
|spouseName|String|El nombre del cónyuge del contacto.|
|surname|String|Los apellidos del contacto.|
|title|String|El título del contacto.|
|websites |Colección [website](../resources/website.md)|Sitios Web asociados con el contacto. |
|weddingAnniversary |Date |Aniversario de boda del contacto. |
|yomiCompanyName|String|El nombre fonético japonés de la empresa del contacto. Esta propiedad es opcional.|
|yomiGivenName|String|El nombre (nombre de pila) fonético japonés del contacto. Esta propiedad es opcional.|
|yomiSurname|String|El apellido fonético japonés del contacto. Esta propiedad es opcional.|

Puesto que el recurso **póngase en contacto con** admite [extensiones](/graph/extensibility-overview), puede usar el `PATCH` operación para agregar, actualizar o eliminar sus propios datos específicas de la aplicación en las propiedades personalizadas de una extensión en una instancia **de contacto** existente.

## <a name="response"></a>Respuesta

Si tiene éxito, este método devuelve una `200 OK` código de respuesta y actualizada [póngase en contacto con](../resources/contact.md) el objeto en el cuerpo de la respuesta.
## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
En el ejemplo siguiente se actualiza la dirección de correo electrónico personal del contacto especificado.
<!-- {
  "blockType": "request",
  "name": "update_contact"
}-->
```http
PATCH https://graph.microsoft.com/beta/me/contacts/AAMkADh6v5AAAvgTCEAAA=
Content-type: application/json

{
    "emailAddresses":[
        {
            "type":"personal",
            "name":"Pavel Bansky",
            "address":"pavelb@adatum.onmicrosoft.com"
        },
        {
          "address": "pavelb@fabrikam.onmicrosoft.com",
          "name": "Pavel Bansky",
          "type": "other",
          "otherLabel": "Volunteer work"
        }
    ]
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

{
    "@odata.context":"https://graph.microsoft.com/beta/$metadata#users('c3e1fcd2-db78-42a8-aec5-1f2cd59abb5c')/contacts/$entity",
    "@odata.etag":"W/\"EQAAABYAAACv7At+UNVFRLhGciJGF6v5AAAve7fh\"",
    "id":"AAMkADh6v5AAAvgTCEAAA=",
    "createdDateTime":"2018-06-11T19:56:07Z",
    "lastModifiedDateTime":"2018-06-11T20:26:23Z",
    "changeKey":"EQAAABYAAACv7At+UNVFRLhGciJGF6v5AAAve7fh",
    "categories":[

    ],
    "parentFolderId":"AAMkADh6v5AAAAAAEOAAA=",
    "birthday":null,
    "fileAs":"",
    "displayName":"Pavel Bansky",
    "givenName":"Pavel",
    "initials":null,
    "middleName":null,
    "nickName":null,
    "surname":"Bansky",
    "title":null,
    "yomiGivenName":null,
    "yomiSurname":null,
    "yomiCompanyName":null,
    "generation":null,
    "imAddresses":[

    ],
    "jobTitle":null,
    "companyName":null,
    "department":null,
    "officeLocation":null,
    "profession":null,
    "assistantName":null,
    "manager":null,
    "spouseName":null,
    "personalNotes":"",
    "children":[

    ],
    "gender":null,
    "isFavorite":null,
    "emailAddresses":[
        {
            "type":"personal",
            "name":"Pavel Bansky",
            "address":"pavelb@adatum.onmicrosoft.com"
        },
        {
            "type":"other",
            "otherLabel":"Volunteer work",
            "name":"Pavel Bansky",
            "address":"pavelb@fabrikam.onmicrosoft.com"
        }
    ],
    "websites":[

    ],
    "phones":[
        {
            "type":"business",
            "number":"+1 732 555 0102"
        }
    ],
    "postalAddresses":[

    ],
    "flag":{
        "flagStatus":"notFlagged"
    }
}
```

## <a name="see-also"></a>Vea también

- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a usuarios mediante extensiones abiertas (versión preliminar)](/graph/extensibility-open-users)
<!--
- [Add custom data to groups using schema extensions (preview)](/graph/extensibility-schema-groups)
-->


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update contact",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->