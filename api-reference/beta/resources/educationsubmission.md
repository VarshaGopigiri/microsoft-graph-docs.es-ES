---
title: tipo de recurso educationSubmission
description: Envíos de pertenecen a una asignación. Un envío representa los recursos que un turn individual (o de grupo) en una asignación y la calificación o comentarios que se devuelve.
author: dipakboyed
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 9cbfaa46d979e3796ae9128e212bfaa1f6bf8453
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27920880"
---
# <a name="educationsubmission-resource-type"></a>tipo de recurso educationSubmission

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Envíos de pertenecen a una asignación. Un envío representa los recursos que un turn individual (o de grupo) en una asignación y la calificación o comentarios que se devuelve.
Envíos se crean automáticamente cuando se publica una asignación. El envío posee dos listas de recursos. Recursos representan los usuarios o grupos trabajar área mientras los recursos enviados representan los recursos que activamente se ha entregado por los alumnos.  

>**Nota:** El estado es de sólo lectura y el objeto se mueve a través del flujo de trabajo a través de acciones. 

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener educationSubmission](../api/educationsubmission-get.md) | [educationSubmission](educationsubmission.md) |Leer las propiedades y relaciones de un objeto **educationSubmission** .|
|[Recursos de la lista](../api/educationsubmission-list-resources.md) |colección de [educationSubmissionResource](educationsubmissionresource.md)| Obtener una colección de objetos **educationSubmissionResource** .|
|[Lista submittedResources](../api/educationsubmission-list-submittedresources.md) |colección de [educationSubmissionResource](educationsubmissionresource.md)| Obtener una colección de objetos **educationSubmissionResource** .|
|[Update](../api/educationsubmission-update.md) | [educationSubmission](educationsubmission.md) |Actualizar un objeto **educationSubmission** . |
|[Return](../api/educationsubmission-return.md)|[educationSubmission](educationsubmission.md)|Un profesor usa retorno para indicar que se puede mostrar los comentarios de remuneración al alumno.|
|[Submit](../api/educationsubmission-submit.md)|[educationSubmission](educationsubmission.md)|Un estudiante usos de envío para activar en la asignación. Esto copiará los recursos en la carpeta **submittedResources** para la clasificación y actualiza el estado.|
|[Unsubmit](../api/educationsubmission-unsubmit.md)|[educationSubmission](educationsubmission.md)|Un alumno utiliza la unsubmit para mover el estado de la presentación de back enviado a trabajar. Esto copiará los recursos en la carpeta **workingResources** para la clasificación y actualiza el estado.|

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|comentarios|[educationFeedback](educationfeedback.md)|Contiene la propiedad comentarios que almacena las notas del profesor volver a los alumnos.|
|grade|[educationAssignmentGrade](educationassignmentgrade.md)|Contiene la información de calificación que un profesor se asigna a este envío.|
|id|Cadena| Solo lectura.|
|destinatario|[educationSubmissionRecipient](educationsubmissionrecipient.md)|Asignado a este envío.|
|releasedBy|[identitySet](identityset.md)|Usuario que ha movido el estado de este envío liberar.|
|releasedDateTime|DateTimeOffset|Momento en el tiempo cuando se publicó el envío. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|returnedBy|[identitySet](identityset.md)|Usuario que ha movido el estado de este envío a devolver.|
|returnedDateTime|DateTimeOffset|Momento en el tiempo cuando se devolvió el envío. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|resourcesFolderUrl|Cadena|Carpeta donde deben almacenarse todos los recursos de archivo para este envío.|
|status|string| Solo lectura. Los valores posibles son: `working`, `submitted`, `released` y `returned`.|
|submittedBy|[identitySet](identityset.md)|Usuario que ha había movido el recurso en el estado enviado.|
|submittedDateTime|DateTimeOffset|Momento en el tiempo cuando se ha movido el envío en el estado enviado. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|
|unsubmittedBy|[identitySet](identityset.md)|Usuario que movió el recurso desde enviadas en el estado de funcionamiento.|
|unsubmittedDateTime|DateTimeOffset|Momento en el tiempo cuando el envío se ha movido de enviado en el estado de funcionamiento. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|recursos|colección de [educationSubmissionResource](educationsubmissionresource.md)| Admite valores NULL.|
|submittedResources|colección de [educationSubmissionResource](educationsubmissionresource.md)| Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationSubmission"
}-->

```json
{
  "feedback": {"@odata.type": "microsoft.graph.educationFeedback"},
  "grade": {"@odata.type": "microsoft.graph.educationAssignmentGrade"},
  "id": "String (identifier)",
  "recipient": {"@odata.type": "microsoft.graph.educationSubmissionRecipient"},
  "returnedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "returnedDateTime": "String (timestamp)",
  "resourcesFolderUrl": "String",
  "status": "string",
  "submittedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "submittedDateTime": "String (timestamp)",
  "unsubmittedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "unsubmittedDateTime": "String (timestamp)"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationSubmission resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
