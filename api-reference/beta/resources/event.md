---
title: tipo de recurso de evento
description: Un evento de un calendario.
author: angelgolfer-ms
ms.openlocfilehash: e60b070ab6b02ca0373d4aebcef4202f42a4f1a5
ms.sourcegitcommit: 37591c2299c80e7675cd2b5f781e1eeeba628a60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2019
ms.locfileid: "27748489"
---
# <a name="event-resource-type"></a>tipo de recurso de evento

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un evento en un calendario del [usuario](user.md) o del calendario predeterminado de un [grupo](group.md)de Office 365.

Este recurso admite:

- Adición de sus propios datos a las propiedades personalizadas como [extensiones](/graph/extensibility-overview).
- Suscribirse a [las notificaciones de cambios](/graph/webhooks).
- que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/event-delta.md).

> **Nota:** Existen algunas pequeñas diferencias en la forma en que puede interactuar con los calendarios de usuario, grupo y sus eventos:

 - Puede organizar sólo los calendarios de usuario en un [calendarGroup](calendargroup.md).
 - Outlook acepta automáticamente todas las convocatorias de reunión en nombre de grupos. Para los calendarios de _usuario_ sólo puede [Aceptar](../api/event-accept.md), [Aceptar provisionalmente](../api/event-tentativelyaccept.md)o [Rechazar](../api/event-decline.md) las convocatorias de reunión.
  - Outlook no admite avisos para eventos de grupo. Para los calendarios de _usuario_ sólo puede [Posponer](../api/event-snoozereminder.md) o [Descartar](../api/event-dismissreminder.md) un [aviso](reminder.md) .

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "attachments",
    "calendar",
    "extensions",
    "instances",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "@odata.type": "microsoft.graph.event"
}-->

```json
{
  "attendees": [{"@odata.type": "microsoft.graph.attendee"}],
  "body": {"@odata.type": "microsoft.graph.itemBody"},
  "bodyPreview": "string",
  "categories": ["string"],
  "changeKey": "string",
  "createdDateTime": "String (timestamp)",
  "end": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "hasAttachments": true,
  "iud": "string",
  "id": "string (identifier)",
  "importance": "String",
  "isAllDay": true,
  "isCancelled": true,
  "isOrganizer": true,
  "isReminderOn": true,
  "lastModifiedDateTime": "String (timestamp)",
  "location": {"@odata.type": "microsoft.graph.location"},
  "locations": [{"@odata.type": "microsoft.graph.location"}],
  "onlineMeetingUrl": "string",
  "organizer": {"@odata.type": "microsoft.graph.recipient"},
  "originalEndTimeZone": "string",
  "originalStart": "String (timestamp)",
  "originalStartTimeZone": "string",
  "recurrence": {"@odata.type": "microsoft.graph.patternedRecurrence"},
  "reminderMinutesBeforeStart": 1024,
  "responseRequested": true,
  "responseStatus": {"@odata.type": "microsoft.graph.responseStatus"},
  "sensitivity": "String",
  "seriesMasterId": "string",
  "showAs": "String",
  "start": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "subject": "string",
  "type": "String",
  "webLink": "string",
  
  "attachments": [ { "@odata.type": "microsoft.graph.attachment" } ],
  "calendar": { "@odata.type": "microsoft.graph.calendar" },
  "extensions": [ { "@odata.type": "microsoft.graph.extension" } ],
  "instances": [ { "@odata.type": "microsoft.graph.event" }],
  "multiValueExtendedProperties": [ { "@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty" }],
  "singleValueExtendedProperties": [ { "@odata.type": "microsoft.graph.singleValueLegacyExtendedProperty" }]
}

```
## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attendees|Colección de [ATTENDEE](attendee.md)|La colección de asistentes del evento.|
|body|[ItemBody](itembody.md)|El cuerpo del mensaje asociado al evento. Puede mostrarse en formato de texto o HTML.|
|bodyPreview|String|La vista previa del mensaje asociado al evento. Se muestran en formato de texto.|
|categories|Colección string|Las categorías asociadas al evento. Cada categoría corresponde a la propiedad **displayName** de un [outlookCategory](outlookcategory.md) definidos para el usuario.|
|changeKey|String|Identifica la versión del objeto de evento. Cada vez que cambia el evento, cambia también ChangeKey. Esto permite que Exchange aplique los cambios a la versión correcta del objeto.|
|createdDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|end|[DateTimeTimeZone](datetimetimezone.md)|La fecha y hora en que finaliza el evento.|
|hasAttachments|Booleano|Se establece como true si el evento tiene datos adjuntos.|
|id|String| Solo lectura.|
|importance|String|Importancia del evento. Los valores posibles son: `low`, `normal` y `high`.|
|isAllDay|Booleano|Se establece como true si el evento dura todo el día.|
|isCancelled|Booleano|Se establece como true si el evento ha sido cancelado.|
|isOrganizer|Booleano|Se establece como true si el remitente del mensaje también es el organizador.|
|isReminderOn|Booleano|Se establece como true si se crea una alerta para recordarle el evento al usuario.|
|lastModifiedDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|location|[Location](location.md)|La ubicación del evento.|
|locations|Colección de [ubicación](location.md)|Ubicaciones donde se celebra el evento o en las que se asiste. Las propiedades **location** y **locations** siempre se corresponden entre sí. Si se actualiza la propiedad **location**, se eliminarían las ubicaciones anteriores de la colección **locations** y se reemplazarían por el nuevo valor de **location**. |
|onlineMeetingUrl|String|Una dirección URL para una reunión en línea. La propiedad sólo se establece cuando el organizador especifica un evento como una reunión en línea, como Skype. Solo lectura.|
|organizador|[Recipient](recipient.md)|El organizador del evento.|
|originalEndTimeZone|Cadena|Zona horaria de finalización que se estableció cuando se creó el evento. Un valor de `tzone://Microsoft/Custom` indica que se ha establecido una zona horaria heredada en el cliente de escritorio de Outlook.|
|originalStart|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|originalStartTimeZone|String|La zona horaria de inicio que se estableció cuando se creó el evento. Un valor de `tzone://Microsoft/Custom` indica que se ha establecido una zona horaria legado en el cliente de escritorio de Outlook.|
|recurrence|[PatternedRecurrence](patternedrecurrence.md)|El patrón de periodicidad del evento.|
|reminderMinutesBeforeStart|Int32|El número de minutos antes de la hora de inicio del evento en que se producirá la alerta del recordatorio.|
|responseRequested|Booleano|Se establece como true si el remitente quiere una respuesta cuando el evento se acepta o se rechaza.|
|responseStatus|[ResponseStatus](responsestatus.md)|Indica el tipo de respuesta que se envía en respuesta a un mensaje de evento.|
|confidencialidad|String| Los valores posibles son: `normal`, `personal`, `private` y `confidential`.|
|seriesMasterId|String|El identificador para el elemento de patrón de serie periódica, si este evento es parte de una serie periódica.|
|showAs|String|El estado que se mostrará. Los valores posibles son: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.|
|start|[DateTimeTimeZone](datetimetimezone.md)|La hora de inicio del evento.|
|subject|String|El texto de la línea de asunto del evento.|
|type|String|El tipo de evento. Los valores posibles son: `singleInstance`, `occurrence`, `exception` y `seriesMaster`. Solo lectura|
|UID|String|Un identificador único que comparten todas las instancias de un evento a través de calendarios diferentes. **Nota:** esta propiedad tiene el mismo objetivo que el `iCalUid` (propiedad) en el [recurso de evento](/graph/api/resources/event?view=graph-rest-1.0) en el extremo de la versión 1.0, pero no se garantiza que tienen el mismo valor.|
|webLink|String|La dirección URL para abrir el evento en Outlook Web App.<br/><br/>El evento se abrirá en el navegador si está conectado a su buzón mediante Outlook Web App. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.<br/><br/>Se puede acceder a esta dirección URL desde un iFrame.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attachments|Colección [attachment](attachment.md)|La colección de datos adjuntos de [FileAttachment](fileattachment.md), [ItemAttachment](itemattachment.md)y [referenceAttachment](referenceattachment.md) para el evento. Propiedad de navegación. Solo lectura. Admite valores NULL.|
|calendar|[Calendar](calendar.md)|El calendario que contiene el evento. Propiedad de navegación. Solo lectura.|
|extensions|Colección [Extension](extension.md)|La colección de extensiones de open definidas para el evento. Admite valores NULL.|
|instances|Colección [event](event.md)|Las instancias del evento. Propiedad de navegación. Solo lectura. Admite valores NULL.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el evento. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el evento. Solo lectura. Admite valores NULL.|

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Enumerar eventos](../api/user-list-events.md)|Colección [event](event.md) |Recupere una lista de los objetos de [evento](../resources/event.md) del buzón del usuario. La lista contiene patrones de serie y reuniones de instancia única.|
|[Crear evento](../api/user-post-events.md) |[evento](event.md)| Crea un nuevo evento publicando en la colección de instancias.|
|[Obtener evento](../api/event-get.md) | [evento](event.md) |Lee las propiedades y las relaciones del objeto de evento.|
|[Actualizar](../api/event-update.md) | [evento](event.md)   |Actualiza el mensaje de evento. |
|[Eliminar](../api/event-delete.md) | Ninguno |Elimina el objeto de evento. |
|[cancel](../api/event-cancel.md) | Ninguno | Enviar mensaje de cancelación desde el organizador a todos los asistentes y cancelar la reunión especificada. |
|[Aceptar](../api/event-accept.md)|Ninguno|Acepte el evento especificado en un calendario del usuario.|
|[tentativelyAccept](../api/event-tentativelyaccept.md)|Ninguno|Aceptar provisionalmente el evento especificado en un calendario del usuario.|
|[Rechazar](../api/event-decline.md)|Ninguno|Rechazar la invitación para el evento especificado en un calendario del usuario.|
|[forward](../api/event-forward.md)|Ninguno|Permite el organizador o el Asistente de un evento de reunión reenviar la convocatoria de reunión a un destinatario nuevo.|
|[delta](../api/event-delta.md)|Colección [event](event.md)|Obtenga un conjunto de eventos que se han agregado, eliminado o actualizado en una **calendarView** (un intervalo de eventos) del calendario principal del usuario.|
|[dismissReminder](../api/event-dismissreminder.md)|Ninguno|Descartar el aviso para el evento especificado en un calendario del usuario.|
|[snoozeReminder](../api/event-snoozereminder.md)|Ninguno|Posponer un aviso para el evento especificado en un calendario de usuario hasta una nueva hora.|
|[Enumerar instancias](../api/event-list-instances.md) |Colección [event](event.md)| Obtiene una colección de objetos de evento.|
|**Datos adjuntos**| | |
|[Enumerar datos adjuntos](../api/event-list-attachments.md) |Colección [attachment](attachment.md)| Obtener todos los datos adjuntos en un evento.|
|[Agregar datos adjuntos](../api/event-post-attachments.md) |[Dato adjunto](attachment.md)| Agrega datos adjuntos nuevos a un evento al publicarlos en la colección de datos adjuntos.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension-post-opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o un recurso existente.|
|[Obtener extensión abierta](../api/opentypeextension-get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene una extensión abierta identificada por el nombre de extensión.|
|**Extensiones de esquema**| | |
|[Agregar valores de extensión de esquema](/graph/extensibility-schema-groups) || Cree una definición de extensión de esquema y, después, úsela para agregar datos escritos personalizados a un recurso.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[evento](event.md)  |Crea una o más propiedades extendidas de valor único en un evento nuevo o existente.   |
|[Obtener evento con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-get.md)  | [evento](event.md) | Obtiene eventos que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [evento](event.md) | Crea una o más propiedades extendidas de varios valores en un evento nuevo o existente.  |
|[Obtener evento con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-get.md)  | [evento](event.md) | Obtiene un evento que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |

## <a name="see-also"></a>Consulte también

- [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](/graph/delta-query-overview)
- [Obtener los cambios incrementales de los eventos de una carpeta](/graph/delta-query-events)
- [Agregar datos personalizados a los recursos mediante extensiones](/graph/extensibility-overview)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
