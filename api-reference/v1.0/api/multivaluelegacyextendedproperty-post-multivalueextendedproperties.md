---
title: Crear propiedad extendida de varios valores
description: 'Cree una o más propiedades extendidas de varios valores en una instancia nueva o existente de un recurso. '
ms.openlocfilehash: 2eb3c337b89be8dc6109dc26de35fcaea88d6609
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032523"
---
# <a name="create-multi-value-extended-property"></a>Crear propiedad extendida de varios valores

Cree una o más propiedades extendidas de varios valores en una instancia nueva o existente de un recurso. 

Se admiten los siguientes recursos de usuario:

- [calendar](../resources/calendar.md)
- [contact](../resources/contact.md)
- [contactFolder](../resources/contactfolder.md) 
- [event](../resources/event.md)
- [mailFolder](../resources/mailfolder.md)
- [message](../resources/message.md)

También los siguientes recursos de grupo:

- [calendar](../resources/calendar.md) de grupo
- [event](../resources/event.md) de grupo
- [post](../resources/post.md) de grupo 

Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.

## <a name="permissions"></a>Permisos
Dependiendo del recurso que está creando la propiedad extendida en y el permiso escriba (delegada o de la aplicación) se solicitud, el permiso especificado en la tabla siguiente es el requisito mínimo para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

| Recurso admitido | Delegado (cuenta profesional o educativa) | Delegado (cuenta personal de Microsoft) | Aplicación |
|:-----|:-----|:-----|:-----|
| [calendario](../resources/calendar.md) | Calendars.ReadWrite | Calendars.ReadWrite | Calendars.ReadWrite |
| [contact](../resources/contact.md) | Contacts.ReadWrite | Contacts.ReadWrite | Contacts.ReadWrite |
| [contactFolder](../resources/contactfolder.md) | Contacts.ReadWrite | Contacts.ReadWrite | Contacts.ReadWrite |
| [evento](../resources/event.md) | Calendars.ReadWrite | Calendars.ReadWrite |  Calendars.ReadWrite|
| [calendar](../resources/calendar.md) de grupo | Group.ReadWrite.All | No admitido | No admitido |
| [event](../resources/event.md) de grupo | Group.ReadWrite.All | No admitido | No admitido |
| [post](../resources/post.md) de grupo | Group.ReadWrite.All | No admitido | No admitido |
| [mailFolder](../resources/mailfolder.md) | Mail.ReadWrite | Mail.ReadWrite | Mail.ReadWrite |
| [mensaje](../resources/message.md) | Mail.ReadWrite | Mail.ReadWrite | Mail.ReadWrite |

## <a name="http-request"></a>Solicitud HTTP
Puede crear propiedades extendidas en una instancia de recurso nueva o existente.

Para crear una o varias propiedades extendidas en una instancia de recurso _nueva_, use la misma solicitud de REST que al crear la instancia e incluya las propiedades de la nueva instancia de recurso _y de la propiedad extendida_ en el cuerpo de la solicitud. Tenga en cuenta que algunos recursos admiten más de una forma de creación. Para obtener más información sobre cómo crear estas instancias de recurso, consulte los temas correspondientes para crear un [message](../resources/message.md), [mailFolder](../api/user-post-mailfolders.md), [event](../api/user-post-events.md), [calendar](../api/user-post-calendars.md), [contact](../api/user-post-contacts.md), [contactFolder](../api/user-post-contactfolders.md), [group event](../api/group-post-events.md) y [group post](../resources/post.md). 
 
A continuación tiene la sintaxis de las solicitudes. 

<!-- { "blockType": "ignored" } -->
```http
POST /me/messages
POST /users/{id|userPrincipalName}/messages
POST /me/mailFolders/{id}/messages

POST /me/mailFolders
POST /users/{id|userPrincipalName}/mailFolders

POST /me/events
POST /users/{id|userPrincipalName}/events

POST /me/calendars
POST /users/{id|userPrincipalName}/calendars

POST /me/contacts
POST /users/{id|userPrincipalName}/contacts

POST /me/contactFolders
POST /users/{id|userPrincipalName}/contactFolders

POST /groups/{id}/events

POST /groups/{id}/threads/{id}/posts/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/posts/{id}/reply
POST /groups/{id}/threads/{id}/reply
POST /groups/{id}/conversations/{id}/threads/{id}/reply
POST /groups/{id}/threads
POST /groups/{id}/conversations
```

Para crear una o varias propiedades extendidas en una instancia de recurso existente, especifique la instancia en la solicitud e incluya la propiedad extendida en el cuerpo de la solicitud.

**Nota** No puede crear una propiedad extendida en una publicación de grupo existente.

<!-- { "blockType": "ignored" } -->
```http
PATCH /me/messages/{id}
PATCH /users/{id|userPrincipalName}/messages/{id}
PATCH /me/mailFolders/{id}/messages/{id}

PATCH /me/mailFolders/{id}
PATCH /users/{id|userPrincipalName}/mailFolders/{id}

PATCH /me/events/{id}
PATCH /users/{id|userPrincipalName}/events/{id}

PATCH /me/calendars/{id}
PATCH /users/{id|userPrincipalName}/calendars/{id}

PATCH /me/contacts/{id}
PATCH /users/{id|userPrincipalName}/contacts/{id}

PATCH /me/contactFolders/{id}
PATCH /users/{id|userPrincipalName}/contactFolders/{id}

PATCH /groups/{id}/events/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Valor |
|:---------------|:----------|
| Authorization | {token} de portador. Obligatorio. |
| Content-Type | application/json |

## <a name="request-body"></a>Cuerpo de solicitud

Proporcione un cuerpo JSON para cada objeto [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md) en la propiedad de la colección **multiValueExtendedProperties** de la instancia de recurso.

|Propiedad|Tipo|Descripción|
|:-----|:-----|:-----|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](../resources/multivaluelegacyextendedproperty.md)| Una matriz de una o más propiedades extendidas con varios valores. |
|id|String|Para cada propiedad de la colección **multiValueExtendedProperties**, especifique esto para identificar la propiedad. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.|
|value|cadena|Para cada propiedad de la colección **multiValueExtendedProperties**, especifique el valor de la propiedad. Necesario.|

Al crear una propiedad extendida en una _nueva_ instancia de recursos, además de la nueva colección de **multiValueExtendedProperties** , proporcionan una representación JSON de esa instancia de recurso así como (es decir, un [mensaje](../resources/message.md), [mailFolder ](../resources/mailfolder.md), [evento](../resources/event.md), etcetera.).


## <a name="response"></a>Respuesta

#### <a name="response-code"></a>Código de respuesta
Una operación que crea correctamente una propiedad extendida en una nueva instancia de recurso devuelve `201 Created`, excepto en un mensaje de grupo nuevo, ya que, según el método usado, la operación puede devolver `200 OK` o `202 Accepted`.

En una instancia de recurso existente, una operación que se ejecuta correctamente devuelve `200 OK`. 


#### <a name="response-body"></a>Cuerpo de la respuesta

Al crear una propiedad extendida en un recurso compatible distinto a la [publicación de grupo](../resources/post.md), la respuesta incluye solo la instancia nueva o existente, pero no la nueva propiedad extendida. Para ver la propiedad extendida recién creada, [expanda la instancia con la propiedad extendida](../api/multivaluelegacyextendedproperty-get.md).

Al crear una propiedad extendida en una publicación de grupo _nueva_, la respuesta incluye solo un código de respuesta, pero no la nueva publicación ni la propiedad extendida. No puede crear una propiedad extendida en una publicación de grupo existente.


## <a name="example"></a>Ejemplo
##### <a name="request-1"></a>Solicitud 1

En el primer ejemplo se crea una propiedad extendida de varios valores en un nuevo evento durante la misma operación POST. Aparte de las propiedades que normalmente incluiría en un nuevo evento, el cuerpo de la solicitud incluye la colección **multiValueExtendedProperties** que contiene una propiedad extendida. El cuerpo de la solicitud incluye lo siguiente para esa propiedad extendida de varios valores:

- **id**, que especifica la propiedad como una matriz de cadenas con el GUID especificado y el nombre `Recreation`. 
- **value**, que especifica `Recreation` como una matriz de 3 valores de cadena, `["Food", "Hiking", "Swimming"]`.
 

<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/v1.0/me/events
Content-Type: application/json

{
  "subject": "Family reunion",
  "body": {
    "contentType": "HTML",
    "content": "Let's get together this Thanksgiving!"
  },
  "start": {
      "dateTime": "2015-11-26T09:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "end": {
      "dateTime": "2015-11-29T21:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "attendees": [
    {
      "emailAddress": {
        "address": "Terrie@contoso.com",
        "name": "Terrie Barrera"
      },
      "type": "Required"
    },
    {
      "emailAddress": {
        "address": "Lauren@contoso.com",
        "name": "Lauren Solis"
      },
      "type": "Required"
    }
  ],
  "multiValueExtendedProperties": [
     {
           "id":"StringArray {66f5a359-4659-4830-9070-00050ec6ac6e} Name Recreation",
           "value": ["Food", "Hiking", "Swimming"]
     }
  ]
}
```

##### <a name="response-1"></a>Respuesta 1

Una respuesta correcta se indica mediante un código de respuesta `HTTP 201 Created` e incluye el nuevo evento en el cuerpo de la respuesta. Es similar a la respuesta al [crear solo un evento](../api/user-post-events.md). El cuerpo de la respuesta no incluye ninguna propiedad extendida recién creada.

Para ver la propiedad extendida recién creada, [expanda el evento con la propiedad extendida](../api/multivaluelegacyextendedproperty-get.md).


****

##### <a name="request-2"></a>Solicitud 2

El segundo ejemplo crea una propiedad extendida de varios valores para el mensaje especificado. La propiedad extendida es el único elemento de la colección **multiValueExtendedProperties**. El cuerpo de la solicitud incluye lo siguiente para la propiedad extendida de varios valores:

- **id** especifica la propiedad como una matriz de cadenas con el GUID especificado y el nombre `Palette`.
- **valor** especifica `Palette` como una matriz de 3 valores de cadena, `["Green", "Aqua", "Blue"]`.

<!-- { "blockType": "ignored" } -->
```http
PATCH https://graph.microsoft.com/v1.0/me/messages('AAMkAGE1M2_as77AACHsLrBBBA=')

Content-Type: application/json

{
  "multiValueExtendedProperties": [
      {
         "id":"StringArray {66f5a359-4659-4830-9070-00049ec6ac6e} Name Palette",
         "value":["Green", "Aqua", "Blue"]
      }
    ]
}
```

##### <a name="response-2"></a>Respuesta 2

Una respuesta correcta se indica mediante un código de respuesta `HTTP 200 OK` e incluye el mensaje especificado en el cuerpo de la respuesta. Es similar a la respuesta al [actualizar un mensaje](../api/message-update.md). El cuerpo de la respuesta no incluye la propiedad extendida recién creada.

Para ver la propiedad extendida recién creada, [expanda el mensaje con la propiedad extendida](../api/multivaluelegacyextendedproperty-get.md).


<!-- This page was manually created. -->
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create a single-value extended property",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->




