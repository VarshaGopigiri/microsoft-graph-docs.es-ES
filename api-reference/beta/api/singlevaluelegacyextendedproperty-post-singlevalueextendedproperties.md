---
title: Crear propiedad extendida de valor único
description: 'Cree una o varias propiedades extendidas de valor único en una instancia nueva o existente de un recurso. '
ms.openlocfilehash: c55ab01ecde214feb38857e8d77f83eb3bfbabc4
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085109"
---
# <a name="create-single-value-extended-property"></a>Crear propiedad extendida de valor único

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Cree una o varias propiedades extendidas de valor único en una instancia nueva o existente de un recurso. 

Se admiten los siguientes recursos de usuario:

- [calendar](../resources/calendar.md)
- [contact](../resources/contact.md)
- [contactFolder](../resources/contactfolder.md) 
- [event](../resources/event.md)
- [mailFolder](../resources/mailfolder.md)
- [message](../resources/message.md)
- [Tarea de Outlook](../resources/outlooktask.md)
- [Carpeta de tareas de Outlook](../resources/outlooktaskfolder.md)

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
| [Tarea de Outlook](../resources/outlooktask.md) | Tasks.ReadWrite | Tasks.ReadWrite | No admitido |
| [Carpeta de tareas de Outlook](../resources/outlooktaskfolder.md) | Tasks.ReadWrite | Tasks.ReadWrite | No se admite |
 
## <a name="http-request"></a>Solicitud HTTP
Puede crear propiedades extendidas en una instancia de recurso nueva o existente.

Para crear una o varias de las propiedades extendidas en una _nueva_ instancia de recursos, use la misma solicitud REST como la creación de la instancia y, incluir las propiedades del nuevo recurso instancia _y propiedad extendida_ en el cuerpo de la solicitud.
Tenga en cuenta que algunos recursos admiten la creación de más de una forma. Para obtener más información sobre la creación de instancias de estos recursos, vea los temas correspondientes para crear un [mensaje](../resources/message.md), [mailFolder](../api/user-post-mailfolders.md), [eventos](../api/user-post-events.md), [calendario](../api/user-post-calendars.md), [contactos](../api/user-post-contacts.md), [contactFolder](../api/user-post-contactfolders.md), [, de [tarea de Outlook](../resources/outlooktask.md) Carpeta de tareas de Outlook](../resources/outlooktaskfolder.md), [eventos de grupo](../api/group-post-events.md)y la [entrada de grupo](../resources/post.md). 
 
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

POST /me/outlook/tasks
POST /users/{id|userPrincipalName}/outlook/tasks
POST /me/outlook/taskFolders/{id}/tasks
POST /users/{id|userPrincipalName}/outlook/taskFolders/{id}/tasks
POST /me/outlook/taskGroups/{id}/taskFolders/{id}/tasks
POST /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}/tasks

POST /me/outlook/taskFolders
POST /users/{id|userPrincipalName}/outlook/taskFolders
POST /me/outlook/taskGroups/{id}/taskFolders
POST /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders

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

PATCH /me/outlook/tasks/{id}
PATCH /users/{id|userPrincipalName}/outlook/tasks/{id}
PATCH /me/outlook/taskFolders/{id}/tasks/{id}
PATCH /users/{id|userPrincipalName}/outlook/taskFolders/{id}/tasks/{id}
PATCH /me/outlook/taskGroups/{id}/taskFolders/{id}/tasks/{id}
PATCH /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}/tasks/{id}

PATCH /me/outlook/taskFolders/{id}
PATCH /users/{id|userPrincipalName}/outlook/taskFolders/{id}
PATCH /me/outlook/taskGroups/{id}/taskFolders/{id}
PATCH /users/{id|userPrincipalName}/outlook/taskGroups/{id}/taskFolders/{id}

PATCH /groups/{id}/events/{id}
```

## <a name="request-headers"></a>Encabezados de solicitud
| Nombre       | Valor |
|:---------------|:----------|
| Authorization | {token} de portador. Obligatorio. |
| Content-Type | application/json |

## <a name="request-body"></a>Cuerpo de solicitud

Proporcione un cuerpo JSON para cada objeto [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md) en la propiedad de la colección **singleValueExtendedProperties** de la instancia de recurso.

|**Propiedad**|**Tipo**|**Descripción**|
|:-----|:-----|:-----|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](../resources/singlevaluelegacyextendedproperty.md)| Una matriz de una o varias propiedades extendidas de valor único. |
|id|String|Para cada propiedad de la colección **singleValueExtendedProperties**, especifique esto para identificar la propiedad. Debe tener uno de los formatos compatibles. Consulte la [Información general de las propiedades extendidas de Outlook](../resources/extended-properties-overview.md) para obtener más información. Necesario.|
|value|string|Para cada propiedad de la colección **singleValueExtendedProperties**, especifique el valor de la propiedad. Necesario.|

Al crear una propiedad extendida en una instancia de recurso _nueva_, además de la nueva colección **singleValueExtendedProperties**, proporcione una representación JSON de esa instancia de recurso (es decir, un [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), etc.).

## <a name="response"></a>Respuesta

#### <a name="response-code"></a>Código de respuesta
Una operación que crea correctamente una propiedad extendida en una nueva instancia de recurso devuelve `201 Created`, excepto en un mensaje de grupo nuevo, ya que, según el método usado, la operación puede devolver `200 OK` o `202 Accepted`.

En una instancia de recurso existente, una operación que se ejecuta correctamente devuelve `200 OK`. 


#### <a name="response-body"></a>Cuerpo de la respuesta

Al crear una propiedad extendida, la respuesta incluye solo la instancia nueva o existente, pero no la nueva propiedad extendida. Para ver la propiedad extendida recién creada, [expanda la instancia con la propiedad extendida](../api/singlevaluelegacyextendedproperty-get.md).

Al crear una propiedad extendida en una [publicación de grupo](../resources/post.md) _nueva_ al responder a un hilo o a una publicación, la respuesta incluye solo un código de respuesta, pero no la nueva publicación ni la propiedad extendida.



## <a name="example"></a>Ejemplo
##### <a name="request-1"></a>Solicitud 1

El primer ejemplo crea un evento nuevo y una propiedad extendida de valor único en la misma operación POST. Aparte de las propiedades que normalmente incluiría en un nuevo evento, el cuerpo de la solicitud incluye la colección **singleValueExtendedProperties** que contiene una propiedad extendida de valor único y lo siguiente para la propiedad:

- **id** especifica el tipo de propiedad como `String`, el GUID y la propiedad denominada `Fun`.
- **value** especifica `Food` como el valor de la propiedad `Fun`. 

<!-- { "blockType": "ignored" } -->
```http
POST https://graph.microsoft.com/beta/me/events
Content-Type: application/json

{
  "subject": "Celebrate Thanksgiving",
  "body": {
    "contentType": "HTML",
    "content": "Let's get together!"
  },
  "start": {
      "dateTime": "2015-11-26T18:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "end": {
      "dateTime": "2015-11-26T23:00:00",
      "timeZone": "Pacific Standard Time"
  },
  "attendees": [
    {
      "emailAddress": {
        "address": "Terrie@contoso.com",
        "name": "Terrie Barrera"
      },
      "type": "Required"
    }
  ],
  "singleValueExtendedProperties": [
     {
           "id":"String {66f5a359-4659-4830-9070-00040ec6ac6e} Name Fun",
           "value":"Food"
     }
  ]
}
```

##### <a name="response-1"></a>Respuesta 1

Una respuesta correcta se indica mediante un código de respuesta `HTTP 201 Created` e incluye el nuevo evento en el cuerpo de la respuesta. Es similar a la respuesta al [crear solo un evento](../api/user-post-events.md). El cuerpo de la respuesta no incluye ninguna propiedad extendida recién creada.

Para ver la propiedad extendida recién creada, [expanda el evento con la propiedad extendida](../api/singlevaluelegacyextendedproperty-get.md).


****

##### <a name="request-2"></a>Solicitud 2

El segundo ejemplo crea una propiedad extendida de valor único para el mensaje existente especificado. La propiedad extendida es el único elemento de la matriz **singleValueExtendedProperties**. El cuerpo de la solicitud incluye lo siguiente para la propiedad extendida:
- **id** especifica el tipo de propiedad como `String`, el GUID y la propiedad denominada `Color`.
- **value** especifica `Green` como el valor de la propiedad `Color`.

<!-- { "blockType": "ignored" } -->
```http
PATCH https://graph.microsoft.com/beta/me/messages('AAMkAGE1M2_bs88AACHsLqWAAA=')

Content-Type: application/json

{
  "singleValueExtendedProperties": [
      {
         "id":"String {66f5a359-4659-4830-9070-00047ec6ac6e} Name Color",
         "value":"Green"
      }
    ]
}
```

##### <a name="response-2"></a>Respuesta 2

Una respuesta correcta se indica mediante un código de respuesta `HTTP 200 OK` e incluye el mensaje especificado en el cuerpo de la respuesta. Es similar a la respuesta al [actualizar un mensaje](../api/message-update.md). El cuerpo de la respuesta no incluye la propiedad extendida recién creada.

Para ver la propiedad extendida recién creada, [expanda el mensaje con la propiedad extendida](../api/singlevaluelegacyextendedproperty-get.md).

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

