---
title: tipo de recurso outlookTaskFolder
description: 'Una carpeta que contiene las tareas de Outlook (colección de objetos de outlookTask). '
ms.openlocfilehash: e3fb9d73dbd9458048749331d14f933d838d4243
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088655"
---
# <a name="outlooktaskfolder-resource-type"></a>tipo de recurso outlookTaskFolder

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una carpeta que contiene las tareas de Outlook (colección de objetos de [outlookTask](outlooktask.md) ). 

En Outlook, el grupo de tareas de forma predeterminada, `My Tasks`, contiene una carpeta de tareas predeterminada, `Tasks`, para el buzón del usuario. No se puede cambiar el nombre o eliminar estos grupo de tareas de forma predeterminada y la carpeta, pero puede crear otros grupos de tareas y carpetas de tareas.


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener outlookTaskFolder](../api/outlooktaskfolder-get.md) | [outlookTaskFolder](outlooktaskfolder.md) |Obtener las propiedades y relaciones de la carpeta de tareas de Outlook especificada.|
|[Crear outlookTask](../api/outlooktaskfolder-post-tasks.md) |[outlookTask](outlooktask.md)| Crear una tarea de Outlook en la carpeta de la tarea especificada.|
|[Enumerar tareas](../api/outlooktaskfolder-list-tasks.md) |colección de [outlookTask](outlooktask.md)| Obtenga todas las tareas de Outlook en la carpeta especificada.|
|[Update](../api/outlooktaskfolder-update.md) | [outlookTaskFolder](outlooktaskfolder.md)   |Actualizar las propiedades modificables de una carpeta de tarea de Outlook. |
|[Delete](../api/outlooktaskfolder-delete.md) | Ninguno |Elimine la carpeta de tareas de Outlook especificada.|
|**Propiedades extendidas**| | |
|[Crear propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[outlookTaskFolder](outlooktaskfolder.md)  |Cree una o más propiedades extendidas de valor único en una carpeta de tareas de Outlook nueva o existente.   |
|[Obtener la carpeta de tareas con la propiedad extendida de valor único](../api/singlevaluelegacyextendedproperty-get.md)  | [outlookTaskFolder](outlooktaskfolder.md) | Obtener las carpetas de tareas de Outlook que contienen un valor único propiedad extendida mediante el uso de `$expand` o `$filter`. |
|[Crear propiedad extendida de varios valores](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [outlookTaskFolder](outlooktaskfolder.md) | Cree una o más propiedades extendidas de varios valores en una carpeta de tareas de Outlook nueva o existente.  |
|[Obtener la carpeta de tareas con varios valores de propiedad extendida](../api/multivaluelegacyextendedproperty-get.md)  | [outlookTaskFolder](outlooktaskfolder.md) | Obtener una carpeta de tarea de Outlook que contiene una propiedad extendida de varios valor mediante el uso de `$expand`. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|changeKey|String|La versión de la carpeta de tareas.|
|id|String|El identificador de la carpeta de tareas, único en el buzón del usuario. Solo lectura.|
|isDefaultFolder|Booleano|Es True si la carpeta es la carpeta de tareas predeterminada.|
|name|String|El nombre de la carpeta de tareas.|
|parentGroupKey|Guid|El identificador GUID único para el grupo primario de la carpeta de la tarea.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|multiValueExtendedProperties|Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)|La colección de propiedades extendidas de varios valores definidos para la carpeta tareas. Solo lectura. Admite valores NULL.|
|singleValueExtendedProperties|Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)|La colección de propiedades extendidas de un solo valor definido para la carpeta tareas. Solo lectura. Admite valores NULL.|
|tasks|colección de [outlookTask](outlooktask.md)|Las tareas de esta carpeta de tareas. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "multiValueExtendedProperties",
    "singleValueExtendedProperties",
    "tasks"
  ],
  "@odata.type": "microsoft.graph.outlookTaskFolder"
}-->

```json
{
  "changeKey": "String",
  "id": "String (identifier)",
  "isDefaultFolder": true,
  "name": "String",
  "parentGroupKey": "Guid"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookTaskFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->