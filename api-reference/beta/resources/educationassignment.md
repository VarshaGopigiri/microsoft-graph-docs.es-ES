---
title: tipo de recurso educationAssignment
description: El recurso **educationAssignment** representa una tarea o una unidad de trabajo asignada a un miembro de estudiantes o equipo en una clase como parte de sus estudios. Sólo los profesores o los propietarios de equipo pueden crear asignaciones. Las asignaciones de contengan documentos y las tareas que el profesor va al alumno a trabajar en. Cada asignación alumno tiene un envío asociado que contiene cualquier trabajo de que su profesor más frecuentes se convierta. Un profesor puede agregar las puntuaciones y comentarios para el envío activado forma de los estudiantes.
localization_priority: Normal
ms.openlocfilehash: d9d7b11dcd476f0fdd2bbb24364dd0e1e026f200
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812456"
---
# <a name="educationassignment-resource-type"></a>tipo de recurso educationAssignment

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **educationAssignment** representa una tarea o una unidad de trabajo asignada a un miembro de estudiantes o equipo en una clase como parte de sus estudios. Sólo los profesores o los propietarios de equipo pueden crear asignaciones. Las asignaciones de contengan documentos y las tareas que el profesor va al alumno a trabajar en. Cada asignación alumno tiene un [envío](educationsubmissionresource.md) asociado que contiene cualquier trabajo de que su profesor más frecuentes se convierta. Un profesor puede agregar las puntuaciones y comentarios para el envío activado forma de los estudiantes.

Cuando se crea una asignación, está en un estado de borrador. Los alumnos no pueden ver la asignación y no se creará envíos. Puede cambiar el estado de una asignación mediante la acción [Publicar](../api/educationassignment-publish.md) . No puede usar una solicitud de revisión para cambiar el estado de la asignación.

La asignación de API se exponen en el espacio de nombres de clase.

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener la asignación](../api/educationassignment-get.md) | [educationAssignment](educationassignment.md) |Leer las propiedades y relaciones de un objeto **educationAssignment** .|
|[Crear un recurso de asignación](../api/educationassignment-post-resources.md) |[educationAssignmentResource](educationassignmentresource.md)| Crear un nuevo **educationAssignmentResource** por la publicación de la colección de recursos.|
|[Recursos de la lista](../api/educationassignment-list-resources.md) |colección de [educationAssignmentResource](educationassignmentresource.md)| Obtener una colección de objetos **educationAssignmentResource** .|
|[Envíos de lista](../api/educationassignment-list-submissions.md) |colección de [educationSubmission](educationsubmission.md)| Obtener una colección de objetos **educationSubmission** .|
|[Update](../api/educationassignment-update.md) | [educationAssignment](educationassignment.md) |Actualizar un objeto **educationAssignment** . |
|[Delete](../api/educationassignment-delete.md) | Ninguno |Eliminación de un objeto **educationAssignment** . |
|[Publish](../api/educationassignment-publish.md)|[educationAssignment](educationassignment.md)|Cambie el estado de un objeto **educationAssignment** de borrador a publicado.|
|[Obtener la dirección URL de la carpeta de recursos](../api/educationassignment-getresourcesfolderurl.md)| string| La carpeta de OneDrive en la que se deben colocar basado en archivos de recursos para formar parte de un recurso de asignación. Archivos deben estar ubicados en esta carpeta que se agregará como un recurso.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|id|Cadena| Solo lectura.|
|allowLateSubmissions|Booleano| Identifica si se pueden enviar a los alumnos después de la fecha de vencimiento. Si esta propiedad no se especifica durante la creación, el valor predeterminado es true. |
|allowStudentsToAddResourcesToSubmission|Booleano| Identifica si los alumnos pueden agregar sus propios recursos a una presentación o si sólo puede modificar los recursos agregados por el profesor. |
|assignDateTime|DateTimeOffset|La fecha de cuándo debe activarse la asignación.  Si en el futuro, la asignación no se mostrará a los alumnos hasta esta fecha.  El tipo de **marca de tiempo** representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|assignTo|[educationAssignmentRecipient](educationassignmentrecipient.md)| Los usuarios, o que toda clase debe recibir un objeto de envío una vez que se publicó la asignación. |
|assignedDateTime|DateTimeOffset|El momento en que se publicó la asignación a los alumnos y la asignación se muestra en la escala de tiempo a los alumnos.  El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|classId|Cadena| Clase que pertenece esta asignación. |
|createdBy|[identitySet](identityset.md)| Quién creó la asignación. |
|createdDateTime|DateTimeOffset|Momento cuándo se creó la asignación.  El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|displayName|Cadena|Nombre de la asignación.|
|dueDateTime|DateTimeOffset|Fecha de la asignación de los alumnos vencimiento.  El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|Puntuar|[educationAssignmentGradeType](educationassignmentgradetype.md)|¿Cómo se corregirán la asignación. |
|instrucciones|[itemBody](itembody.md)| Instrucciones para la asignación.  Esto junto con el nombre para mostrar indicar qué hacer los estudiantes. |
|lastModifiedBy|[identitySet](identityset.md)| Que modificó por última vez la asignación. |
|lastModifiedDateTime|DateTimeOffset|Momento cuándo se modificó por última vez la asignación.  El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|status|string| Estado de la **asignación**.  No se puede una revisión este valor.  Los valores posibles son: `draft`, `published` y `assigned`.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Description|
|:---------------|:--------|:----------|
|recursos|colección de [educationAssignmentResource](educationassignmentresource.md)| Objetos de aprendizaje que están asociados con esta asignación.  Profesores sólo pueden modificar esta lista. Admite valores NULL.|
|envíos|colección de [educationSubmission](educationsubmission.md)| Una vez publicado, hay un objeto de envío para cada estudiante que representa el trabajo y su calificación.  Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationAssignment"
}-->

```json
{
  "id": "String (identifier)",
  "allowLateSubmissions": true,
  "allowStudentsToAddResourcesToSubmission": true,
  "assignDateTime": "String (timestamp)",
  "assignTo": {"@odata.type": "microsoft.graph.educationAssignmentRecipient"},
  "assignedDateTime": "String (timestamp)",
  "classId": "String",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "displayName": "String",
  "dueDateTime": "String (timestamp)",
  "grading": {"@odata.type": "microsoft.graph.educationAssignmentGradeType"},
  "instructions": {"@odata.type": "microsoft.graph.itemBody"},
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "status": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
