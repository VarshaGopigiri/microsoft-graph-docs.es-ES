---
title: Tipo de recurso outlookTask
description: 'Un elemento de Outlook que puede realizar un seguimiento de un elemento de trabajo. '
author: angelgolfer-ms
localization_priority: Priority
ms.prod: outlook
ms.openlocfilehash: f49c74af92037f430b72d7b9fffa4a85aba00942
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27943278"
---
# <a name="outlooktask-resource-type"></a>Tipo de recurso outlookTask

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un elemento de Outlook que puede realizar un seguimiento de un elemento de trabajo. 

Puede usar una tarea para realizar un seguimiento de inicio, vencimiento y las fechas de finalización real y las horas, su progreso o estado, si lo es periódica y requiere recuerde.

Propiedades relacionadas con la fecha en el recurso **outlookTask** incluyen las siguientes:

- completedDateTime
- createdDateTime
- dueDateTime
- lastModifiedDateTime
- reminderDateTime
- startDateTime

De forma predeterminada, las operaciones POST, GET, revisión y [completa](../api/outlooktask-complete.md) devuelven propiedades relacionadas con la fecha en sus respuestas REST en UTC. Puede usar el `Prefer: outlook.timezone` encabezado para que todas las propiedades relacionadas con la fecha en la respuesta representada en una zona horaria diferente a la hora UTC. El ejemplo siguiente devuelve las propiedades relacionadas con fechas en EST en la respuesta correspondiente:

```
Prefer: outlook.timezone="Eastern Standard Time"
```

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener outlookTask](../api/outlooktask-get.md) | [outlookTask](outlooktask.md) |Obtener las propiedades y relaciones de una tarea de Outlook en el buzón del usuario.|
|[Update](../api/outlooktask-update.md) | [outlookTask](outlooktask.md) |Cambiar las propiedades grabables de una tarea de Outlook. |
|[Delete](../api/outlooktask-delete.md) | Ninguno |Eliminar la tarea especificada en el buzón del usuario. |
|[Complete](../api/outlooktask-complete.md)|colección de [outlookTask](outlooktask.md)|Completar una tarea de Outlook que establece la propiedad **completedDateTime** a la fecha actual y la propiedad **status** para `completed`.|
|**Datos adjuntos**| | |
|[Enumerar datos adjuntos](../api/outlooktask-list-attachments.md) |Colección de [datos adjuntos](attachment.md)| Obtener todos los datos adjuntos en una tarea de Outlook.|
|[Agregar datos adjuntos](../api/outlooktask-post-attachments.md) |[attachment](attachment.md)| Agregar un archivo, un elemento (mensaje, evento o contacto) o un vínculo a un archivo como datos adjuntos a una tarea.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[outlookTask](outlooktask.md)  |Cree una o más propiedades extendidas de valor único en una tarea de Outlook nueva o existente.   |
|[Obtener tarea con un solo valor de propiedad extendida](../api/singlevaluelegacyextendedproperty-get.md)  | [outlookTask](outlooktask.md) | Obtener las tareas de Outlook que contienen un valor único propiedad extendida mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [outlookTask](outlooktask.md) | Cree una o más propiedades extendidas de varios valores en una tarea de Outlook nueva o existente.  |
|[Obtener tarea con varios valor de propiedad extendida](../api/multivaluelegacyextendedproperty-get.md)  | [outlookTask](outlooktask.md) | Obtener una tarea de Outlook que contiene una propiedad extendida de varios valor mediante el uso de `$expand`. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|assignedTo|Cadena|El nombre de la persona que se le ha asignado la tarea.|
|body|[itemBody](itembody.md)|El cuerpo de la tarea que normalmente contiene información acerca de la tarea. Tenga en cuenta que sólo el tipo HTML es compatible.|
|categories|Colección String|Las categorías asociadas con la tarea. Cada categoría corresponde a la propiedad **displayName** de un [outlookCategory](outlookcategory.md) que ha definido el usuario.|
|changeKey|Cadena|La versión de la tarea.|
|completedDateTime|[dateTimeTimeZone](datetimetimezone.md)|La fecha en la zona horaria especificada que se ha finalizado la tarea.|
|createdDateTime|DateTimeOffset|La fecha y la hora cuando se creó la tarea. De forma predeterminada, está en UTC. Puede proporcionar una zona horaria personalizada en el encabezado de solicitud. El valor de la propiedad usa formato ISO 8601. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|dueDateTime|[dateTimeTimeZone](datetimetimezone.md)|La fecha en la zona horaria especificada que se va finalizado la tarea.|
|hasAttachments|Booleano|Se establece en true si la tarea tiene datos adjuntos.|
|id|Cadena|El identificador único de la tarea. Solo lectura.|
|importance|string|Importancia del evento. Los valores posibles son: `low`, `normal` y `high`.|
|isReminderOn|Booleano|Se establece en true si se establece una alerta para recordarle al usuario de la tarea.|
|lastModifiedDateTime|DateTimeOffset|La fecha y hora de última modificación de la tarea. De forma predeterminada, está en UTC. Puede proporcionar una zona horaria personalizada en el encabezado de solicitud. El valor de la propiedad utiliza el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`.|
|owner|Cadena|El nombre de la persona que creó la tarea.|
|parentFolderId|Cadena|El identificador único para la carpeta principal de la tarea.|
|periodicidad|[patternedRecurrence](patternedrecurrence.md)|El patrón de periodicidad de la tarea.|
|reminderDateTime|[dateTimeTimeZone](datetimetimezone.md)|La fecha y hora para un aviso de la tarea que se produzca.|
|sensitivity|string|Indica el nivel de privacidad para la tarea. Los valores posibles son: `normal`, `personal`, `private` y `confidential`.|
|startDateTime|[dateTimeTimeZone](datetimetimezone.md)|La fecha en la zona horaria especificada cuando la tarea que se va a comenzar.|
|status|string|Indica el estado o el progreso de la tarea. Los valores posibles son: `notStarted`, `inProgress`, `completed`, `waitingOnOthers` y `deferred`.|
|subject|Cadena|Una breve descripción o el título de la tarea.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|attachments|Colección de [datos adjuntos](attachment.md)|La colección de datos adjuntos de [fileAttachment](fileattachment.md), [itemAttachment](itemattachment.md)y [referenceAttachment](referenceattachment.md) para la tarea.  Solo lectura. Admite valores NULL.|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)|La colección de propiedades extendidas de varios valores definidos para la tarea. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)|La colección de propiedades extendidas de un solo valor definido para la tarea. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "attachments",
    "singleValueExtendedProperties",
    "multiValueExtendedProperties"
  ],
  "@odata.type": "microsoft.graph.outlookTask"
}-->

```json
{
  "assignedTo": "String",
  "body": {"@odata.type": "microsoft.graph.itemBody"},
  "categories": ["String"],
  "changeKey": "String",
  "completedDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "createdDateTime": "String (timestamp)",
  "dueDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "hasAttachments": true,
  "id": "String (identifier)",
  "importance": "string",
  "isReminderOn": true,
  "lastModifiedDateTime": "String (timestamp)",
  "owner": "String",
  "parentFolderId": "String",
  "recurrence": {"@odata.type": "microsoft.graph.patternedRecurrence"},
  "reminderDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "sensitivity": "string",
  "startDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "status": "string",
  "subject": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookTask resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
