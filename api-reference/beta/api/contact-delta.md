---
title: 'contacto: delta'
description: Obtiene un conjunto de contactos que se hayan agregado, eliminado o actualizado en una carpeta determinada.
ms.openlocfilehash: 1e97a59de7abec0c69a5e02559081f7b344ebad0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087713"
---
# <a name="contact-delta"></a>contacto: delta

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Obtiene un conjunto de contactos que se hayan agregado, eliminado o actualizado en una carpeta determinada.

La llamada de una función **delta** para los contactos de una carpeta funciona de forma similar a una solicitud GET, salvo que, al aplicar correctamente [tokens de estado](/graph/delta-query-overview) en al menos una de estas llamadas, puede realizar una consulta para obtener los cambios incrementales en los contactos de la carpeta. Esto permite mantener y sincronizar un almacén local de contactos de un usuario, sin tener que capturar cada vez todo el conjunto de contactos desde el servidor.  

## <a name="permissions"></a>Permisos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso      | Permisos (de menos a más privilegiados)              |
|:--------------------|:---------------------------------------------------------|
|Delegado (cuenta profesional o educativa) | Contacts.Read, Contacts.ReadWrite    |
|Delegado (cuenta personal de Microsoft) | Contacts.Read, Contacts.ReadWrite    |
|Aplicación | Contacts.Read, Contacts.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
<!-- { "blockType": "ignored" } -->
```http
GET /me/contactFolders/{id}/contacts/delta
GET /users/<id>/contactFolders/{id}/contacts/delta
```

## <a name="query-parameters"></a>Parámetros de consulta

El seguimiento de cambios en los contactos conlleva al menos una llamada de una función **delta**. Si usa cualquier parámetro de consulta (distinto de `$deltatoken` y `$skiptoken`), debe especificarlo en la solicitud **delta** inicial. Microsoft Graph codifica automáticamente cualquier parámetro especificado en la parte del token de la URL `nextLink` o `deltaLink` proporcionada en la respuesta. Solo debe especificar una vez por adelantado los parámetros de consulta deseados. En solicitudes posteriores, basta con copiar y aplicar la dirección URL `nextLink` o `deltaLink` de la respuesta anterior, dado que la dirección URL ya incluye los parámetros codificados deseados.

| Parámetro de consulta      | Tipo   |Descripción|
|:---------------|:--------|:----------|
| $deltatoken | string | [Token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `deltaLink` de la llamada de función **delta** anterior para la misma colección de contactos. Indica el progreso de la ronda de seguimiento de cambios. Guarde y aplique toda la dirección URL `deltaLink`, incluido este token, en la primera solicitud de la siguiente ronda de seguimiento de cambios de la colección.|
| $skiptoken | string | [Token de estado](/graph/delta-query-overview) que se devuelve en la dirección URL de `nextLink` de la llamada de función **delta**. Indica que debe realizarse el seguimiento de más cambios en la misma colección de contactos. |

### <a name="odata-query-parameters"></a>Parámetros de consulta de OData

- Puede utilizar un parámetro de consulta `$select` como en cualquier solicitud GET para especificar solo las propiedades que necesita para un mejor rendimiento. Siempre se devuelve la propiedad _id_. 


## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Tipo | Descripción |
|:---------------|:----------|:----------|
| Authorization  | string  | {token} de portador. Obligatorio. |
| Content-Type  | string  | application/json. Obligatorio. |
| Prefer | string  | odata.maxpagesize={x}. Opcional. |

## <a name="response"></a>Respuesta

Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto de colección [contacto](../resources/contact.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
##### <a name="request"></a>Solicitud
En el ejemplo siguiente se muestra cómo realizar una llamada de función **delta** única, usar un parámetro `$select` para obtener solo la propiedad **displayName** de cada contacto, y limitar el número máximo de contactos en el cuerpo de la respuesta a 2.

Para realizar un seguimiento de los contactos en las carpetas, debería realizar al menos una llamada de función **delta**, con unos tokens de estado adecuados, para obtener el conjunto de cambios incrementales desde la última consulta delta. 

Encontrará un ejemplo similar en el que se muestra cómo usar los tokens de estado para realizar un seguimiento de los cambios en los mensajes de una carpeta de correo: [Obtener los cambios incrementales en los mensajes de una carpeta](/graph/delta-query-messages). Las diferencias principales entre realizar un seguimiento de los contactos y realizar un seguimiento de los mensajes en una carpeta están en las direcciones URL de consulta delta. Además, las respuestas de consulta devuelven colecciones **contact** en lugar de colecciones **message**.
 
<!-- {
  "blockType": "request",
  "name": "contact_delta"
}-->
```http
GET https://graph.microsoft.com/beta/me/contactFolders/{id}/contacts/delta?$select=displayName

Prefer: odata.maxpagesize=2
```

##### <a name="response"></a>Respuesta
Si la solicitud es correcta, la respuesta debería incluir un símbolo de estado, que puede ser un _skipToken_  
(en un encabezado de respuesta de _@odata.nextLink_) o un _deltaToken_ (en un encabezado de respuesta de _@odata.deltaLink_). Respectivamente, indican si debe continuar con la ronda, o bien si ha terminado de obtener todos los cambios de la ronda.

La respuesta siguiente muestra un _skipToken_ en un encabezado de respuesta de _@odata.nextLink_.

Nota: Es posible que el objeto de respuesta que aparezca aquí esté truncado para abreviar. Todas las propiedades se devolverán de una llamada real.
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.contact",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 337

{
  "@odata.nextLink":"https://graph.microsoft.com/beta/me/contactfolders('{id}')/contacts/delta?$skiptoken={_skipToken_}",
  "value": [
    {
      "parentFolderId": "parentFolderId-value",
      "birthday": "2016-10-19T10:37:00Z",
      "fileAs": "fileAs-value",
      "displayName": "displayName-value",
      "givenName": "givenName-value",
      "initials": "initials-value"
    }
  ]
}
```

### <a name="see-also"></a>Recursos adicionales

- [Consulta delta de Microsoft Graph](/graph/delta-query-overview)
- [Obtener los cambios incrementales en los mensajes de una carpeta](/graph/delta-query-messages)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contact: delta",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->