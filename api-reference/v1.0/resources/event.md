# <a name="event-resource-type"></a>tipo de recurso de evento

Un evento de un calendario.

Este recurso admite:

- que agregue sus propios datos a las propiedades personalizadas mediante [extensiones](../../../concepts/extensibility_overview.md);
- que use una [consulta delta](../../../concepts/delta_query_overview.md) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/event_delta.md).


## <a name="methods"></a>Métodos

| Método       | Tipo de valor devuelto  |Descripción|
|:---------------|:--------|:----------|
|[Enumerar eventos](../api/user_list_events.md)|Colección [event](event.md) |Recupere una lista de los objetos de [evento](../resources/event.md) del buzón del usuario. La lista contiene patrones de serie y reuniones de instancia única.|
|[Crear evento](../api/user_post_events.md) |[evento](event.md)| Crea un nuevo evento publicando en la colección de instancias.|
|[Obtener evento](../api/event_get.md) | [evento](event.md) |Lee las propiedades y las relaciones del objeto de evento.|
|[Actualizar](../api/event_update.md) | [evento](event.md) |Actualiza el mensaje de evento. |
|[Eliminar](../api/event_delete.md) | Ninguno |Elimina el objeto de evento. |
|[Aceptar](../api/event_accept.md)|Ninguno|Acepta el evento especificado.|
|[tentativelyAccept](../api/event_tentativelyaccept.md)|Ninguno|Acepta provisionalmente el evento especificado.|
|[Rechazar](../api/event_decline.md)|Ninguno|Rechaza la invitación al evento especificado.|
|[delta](../api/event_delta.md)|Colección [event](event.md)|Obtenga un conjunto de eventos que se han agregado, eliminado o actualizado en una **calendarView** (un intervalo de eventos) del calendario principal del usuario.|
|[dismissReminder](../api/event_dismissreminder.md)|Ninguno|Descarta el aviso para el evento especificado.|
|[snoozeReminder](../api/event_snoozereminder.md)|Ninguno|Pospone el aviso para el evento especificado.|
|[Enumerar instancias](../api/event_list_instances.md) |Colección [event](event.md)| Obtiene las instancias (repeticiones) de un evento durante un intervalo de tiempo especificado. Si el evento es de tipo `SeriesMaster`, devuelve las repeticiones y excepciones del evento en el intervalo de tiempo especificado.|
|**Datos adjuntos**| | |
|[Enumerar datos adjuntos](../api/event_list_attachments.md) |Colección [attachment](attachment.md)| Obtener todos los datos adjuntos en un evento.|
|[Agregar datos adjuntos](../api/event_post_attachments.md) |[dato adjunto](attachment.md)| Agrega datos adjuntos nuevos a un evento al publicarlos en la colección de datos adjuntos.|
|**Extensiones abiertas**| | |
|[Crear extensión abierta](../api/opentypeextension_post_opentypeextension.md) |[openTypeExtension](opentypeextension.md)| Crea una extensión abierta y agrega propiedades personalizadas en una instancia nueva o existente de un recurso.|
|[Obtener extensión abierta](../api/opentypeextension_get.md) |Colección [openTypeExtension](opentypeextension.md)| Obtiene un objeto u objetos de extensión abierta identificados por nombre o por nombre completo.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[evento](event.md)  |Crea una o más propiedades extendidas de valor único en un evento nuevo o existente.   |
|[Obtener evento con propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty_get.md)  | [evento](event.md) | Obtiene eventos que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [evento](event.md) | Crea una o más propiedades extendidas de varios valores en un evento nuevo o existente.  |
|[Obtener evento con propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty_get.md)  | [evento](event.md) | Obtiene un evento que contiene una propiedad extendida de varios valores mediante el uso de `$expand`. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|asistentes|Colección [attendee](attendee.md)|La colección de asistentes del evento.|
|body|[itemBody](itembody.md)|El cuerpo del mensaje asociado al evento. Puede mostrarse en formato de texto o HTML.|
|bodyPreview|String|La vista previa del mensaje asociado al evento. Se muestran en formato de texto.|
|categories|Colección string|Las categorías asociadas al evento.|
|changeKey|String|Identifica la versión del objeto de evento. Cada vez que cambia el evento, cambia también ChangeKey. Esto permite que Exchange aplique los cambios a la versión correcta del objeto.|
|createdDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|finalización|[dateTimeTimeZone](datetimetimezone.md)|La fecha, la hora y la zona horaria en que finaliza el evento.|
|hasAttachments|Booleano|Se establece como true si el evento tiene datos adjuntos.|
|iCalUId|String|Un identificador único que comparten todas las instancias de un evento a través de calendarios diferentes.|
|id|Cadena| Solo lectura.|
|importance|String|La importancia del evento: Baja = 0, Normal = 1, Alta = 2. Los valores posibles son: `Low`, `Normal` y `High`.|
|isAllDay|Booleano|Se establece como true si el evento dura todo el día.|
|isCancelled|Booleano|Se establece como true si el evento ha sido cancelado.|
|isOrganizer|Booleano|Se establece como true si el remitente del mensaje también es el organizador.|
|isReminderOn|Booleano|Se establece como true si se crea una alerta para recordarle el evento al usuario.|
|lastModifiedDateTime|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|location|[ubicación](location.md)|La ubicación del evento.|
|onlineMeetingUrl|String|Una dirección URL para una reunión en línea.|
|organizador|[recipient](recipient.md)|El organizador del evento.|
|originalEndTimeZone|String|La zona horaria de finalización que se estableció cuando se creó el evento. Un valor de `tzone://Microsoft/Custom` indica que la zona horaria personalizada legado se estableció en el cliente de escritorio de Outlook.|
|originalStart|DateTimeOffset|El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenecen a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|originalStartTimeZone|String|La zona horaria de inicio que se estableció cuando se creó el evento. Un valor de `tzone://Microsoft/Custom` indica que se ha establecido una zona horaria legado en el cliente de escritorio de Outlook. |
|periodicidad|[patternedRecurrence](patternedrecurrence.md)|El patrón de periodicidad del evento.|
|reminderMinutesBeforeStart|Int32|El número de minutos antes de la hora de inicio del evento en que se producirá la alerta del recordatorio.|
|responseRequested|Booleano|Se establece como true si el remitente quiere una respuesta cuando el evento se acepta o se rechaza.|
|responseStatus|[responseStatus](responsestatus.md)|Indica el tipo de respuesta que se envía en respuesta a un mensaje de evento.|
|confidencialidad|String| Los valores posibles son: `Normal`, `Personal`, `Private` y `Confidential`.|
|seriesMasterId|String|Las categorías asignadas al elemento.|
|showAs|String|El estado que se mostrará. Los valores posibles son: `Free`, `Tentative`, `Busy`, `Oof`, `WorkingElsewhere` y `Unknown`.|
|inicio|[dateTimeTimeZone](datetimetimezone.md)|La fecha, la hora y la zona horaria en que comienza el evento.|
|subject|String|El texto de la línea de asunto del evento.|
|type|String|El tipo de evento. Los valores posibles son: `SingleInstance`, `Occurrence`, `Exception` y `SeriesMaster`. Solo lectura.|
|webLink|String|La dirección URL para abrir el evento en Outlook Web App.<br/><br/>El evento se abrirá en el navegador si está conectado a su buzón mediante Outlook Web App. Se le pedirá que inicie sesión si no la ha iniciado ya en el navegador.<br/><br/>Se puede acceder a esta dirección URL desde un iFrame.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attachments|Colección [attachment](attachment.md)|La colección de datos adjuntos [fileAttachment](fileAttachment.md) y [itemAttachment](itemAttachment.md) del evento. Propiedad de navegación. Solo lectura. Admite valores NULL.|
|calendario|[calendario](calendar.md)|El calendario que contiene el evento. Propiedad de navegación. Solo lectura.|
|extensions|Colección [Extension](extension.md)|La colección de extensiones abiertas definidas para el evento. Solo lectura. Admite valores NULL.|
|instances|Colección [event](event.md)|Las instancias del evento. Propiedad de navegación. Solo lectura. Admite valores NULL.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)| La colección de propiedades extendidas de varios valores definidas para el evento. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)| La colección de propiedades extendidas de valor único definidas para el evento. Solo lectura. Admite valores NULL.|

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
  "keyProperty": "id",
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
  "iCalUId": "string",
  "id": "string (identifier)",
  "importance": "String",
  "isAllDay": true,
  "isCancelled": true,
  "isOrganizer": true,
  "isReminderOn": true,
  "lastModifiedDateTime": "String (timestamp)",
  "location": {"@odata.type": "microsoft.graph.location"},
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


## <a name="see-also"></a>Consulte también

- [Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph](../../../concepts/delta_query_overview.md)
- [Obtener los cambios incrementales de los eventos de una carpeta](../../../concepts/delta_query_events.md)
- [Agregar datos personalizados a los recursos mediante extensiones](../../../concepts/extensibility_overview.md)
- [Agregar datos personalizados a los usuarios mediante extensiones abiertas](../../../concepts/extensibility_open_users.md)
- [Agregar datos personalizados a los grupos mediante extensiones de esquema](../../../concepts/extensibility_schema_groups.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "event resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
