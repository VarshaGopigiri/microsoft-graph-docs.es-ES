---
title: tipo de recurso outlookTaskGroup
description: 'Un grupo de carpetas (outlookTaskFolder) que contienen las tareas de Outlook (colección de objetos de outlookTask). '
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: d1392e07f76d508fe30307294a54429a692f34e8
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27923911"
---
# <a name="outlooktaskgroup-resource-type"></a>tipo de recurso outlookTaskGroup

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Un grupo de carpetas ([outlookTaskFolder](outlooktaskfolder.md)) que contienen las tareas de Outlook (colección de objetos de [outlookTask](outlooktask.md) ). 

En Outlook, hay un grupo de tareas predeterminada `My Tasks` que no se puede cambiar el nombre o eliminar. Sin embargo, puede crear grupos de tareas adicionales. 


## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[Obtener outlookTaskGroup](../api/outlooktaskgroup-get.md) | [outlookTaskGroup](outlooktaskgroup.md) |Obtener las propiedades y relaciones del grupo de tareas de Outlook especificado.|
|[Crear outlookTaskFolder](../api/outlooktaskgroup-post-taskfolders.md) |[outlookTaskFolder](outlooktaskfolder.md)| Crear una carpeta de tareas de Outlook.|
|[Lista taskFolders](../api/outlooktaskgroup-list-taskfolders.md) |colección de [outlookTaskFolder](outlooktaskfolder.md)| Obtener una colección de carpetas de tareas de Outlook.|
|[Update](../api/outlooktaskgroup-update.md) | [outlookTaskGroup](outlooktaskgroup.md)  |Actualizar las propiedades modificables de un grupo de tareas de Outlook. |
|[Delete](../api/outlooktaskgroup-delete.md) | Ninguno |Eliminar el grupo de tareas de Outlook especificado. |

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|changeKey|Cadena|La versión del grupo de tareas.|
|groupKey|Edm.Guid|El identificador GUID único para el grupo de tareas.|
|id|Cadena|El identificador de cadena único del grupo de tareas. Solo lectura.|
|isDefaultGroup|Booleano|Es True si el grupo de tareas es el grupo de tareas predeterminada.|
|name|Cadena|El nombre del grupo de tareas.|

## <a name="relationships"></a>Relaciones
| Relación | Tipo   |Descripción|
|:---------------|:--------|:----------|
|taskFolders|colección de [outlookTaskFolder](outlooktaskfolder.md)| La colección de carpetas de tareas en el grupo de tareas. Solo lectura. Admite valores NULL.|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.outlookTaskGroup"
}-->

```json
{
  "changeKey": "String",
  "groupKey": "Guid",
  "id": "String (identifier)",
  "isDefaultGroup": true,
  "name": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "outlookTaskGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
