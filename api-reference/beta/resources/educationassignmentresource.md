---
title: tipo de recurso educationAssignmentResource
description: Un objeto contenedor que almacena los recursos asociados a una asignación. El contenedor de agrega la propiedad **distributeForStudentWork** y se indica que se va este recurso
localization_priority: Normal
ms.openlocfilehash: 55d978ceb2a3df613ded09682bbdc42009f4e204
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27868841"
---
# <a name="educationassignmentresource-resource-type"></a>tipo de recurso educationAssignmentResource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un objeto contenedor que almacena los recursos asociados a una asignación. El contenedor agrega la propiedad **distributeForStudentWork** y se indica que este recurso se copiarán en el envío de estudiantes.  Si el objeto no se copia, cada alumno verán un vínculo para el recurso en la asignación. El alumno no podrá actualizar este recurso. Se trata de un documento del profesor al alumno con nothing se convierta. Si el recurso se distribuye, cada estudiante recibirá una copia de este recurso en la lista de recursos de su presentación. Cada alumno será capaz de modificar su copia y enviar para clasificación.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener educationAssignmentResource](../api/educationassignmentresource-get.md) | [educationAssignmentResource](educationassignmentresource.md) |Leer las propiedades y relaciones de un objeto **educationAssignmentResource** .|
|[Update](../api/educationassignmentresource-update.md) | [educationAssignmentResource](educationassignmentresource.md) |Actualizar un objeto **educationAssignmentResource** . |
|[Delete](../api/educationassignmentresource-delete.md) | Ninguno |Eliminación de un objeto **educationAssignmentResource** . |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|distributeForStudentWork|Booleano|Indica si se debe copiar este recurso a cada envío estudiantes para el tipo de modificación y envío.|
|id|Cadena| Identificador de este recurso. Solo lectura.|
|resource|[educationResource](educationresource.md)|Objeto de recurso que se ha asociado con esta asignación.|

## <a name="relationships"></a>Relaciones
Ninguna.


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationAssignmentResource"
}-->

```json
{
  "distributeForStudentWork": true,
  "id": "String (identifier)",
  "resource": {"@odata.type": "microsoft.graph.educationResource"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationAssignmentResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
