---
title: Tipo de recurso calendarGroup
description: Un grupo de calendarios de usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 5b75ebf253276876129859be7d37ecb6748fc0d9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949629"
---
# <a name="calendargroup-resource-type"></a>Tipo de recurso calendarGroup

Un grupo de calendarios de usuario.

## <a name="methods"></a>Métodos

| Método                                                      | Tipo de valor devuelto                        | Descripción                                                   |
| :---------------------------------------------------------- | :--------------------------------- | :------------------------------------------------------------ |
| [List calendar groups](../api/user-list-calendargroups.md)  | Colección [Calendar](calendar.md) | Obtiene los grupos de calendarios del usuario.                               |
| [Create calendar group](../api/user-post-calendargroups.md) | [Calendar](calendar.md)            | Crea un grupo de calendarios.                                  |
| [Get calendar group](../api/calendargroup-get.md)           | [calendarGroup](calendargroup.md)  | Lee las propiedades y relaciones de un objeto de grupo de calendarios. |
| [Update](../api/calendargroup-update.md)                    | [calendarGroup](calendargroup.md)  | Actualiza el objeto calendarGroup.                                  |
| [Delete](../api/calendargroup-delete.md)                    | None                               | Elimina el objeto calendarGroup.                                  |
| [List calendars](../api/calendargroup-list-calendars.md)    | Colección [Calendar](calendar.md) | Muestra la lista de calendarios de un grupo de calendarios.                           |
| [Create Calendar](../api/calendargroup-post-calendars.md)   | [Calendar](calendar.md)            | Crea un calendario en un grupo de calendarios.                    |

## <a name="properties"></a>Propiedades

| Propiedad  | Tipo   | Descripción                                                                                                                                                                                               |
| :-------- | :----- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name      | String | Nombre del grupo.                                                                                                                                                                                           |
| changeKey | String | Identifica la versión del grupo de calendarios. Cada vez que cambia el grupo de calendarios, cambia también ChangeKey. Permite que Exchange aplique los cambios a la versión correcta del objeto. Solo lectura. |
| classId   | Guid   | Identificador de la clase. Solo lectura.                                                                                                                                                                          |
| id        | String | Identificador único del grupo. Solo lectura.                                                                                                                                                                 |

## <a name="relationships"></a>Relaciones

| Relación | Tipo                               | Descripción                                                                    |
| :----------- | :--------------------------------- | :----------------------------------------------------------------------------- |
| calendars    | Colección [calendar](calendar.md) | Calendarios del grupo de calendarios. Propiedad de navegación. Solo lectura. Admite valores NULL. |

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "calendars"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.calendarGroup",
  "@odata.annotations": [
    {
      "property": "calendars",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "navigability": "single",
        "searchable": false
      }
    }
  ]
}-->

```json
{
  "changeKey": "string",
  "classId": "guid",
  "id": "string (identifier)",
  "name": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "calendarGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
