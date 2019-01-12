---
title: Tipo de recurso calendarGroup
description: Un grupo de calendarios de usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 10a840fd9ae9835eb5ca6a96b88719605f89245b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27985294"
---
# <a name="calendargroup-resource-type"></a>Tipo de recurso calendarGroup

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

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

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "calendars"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.calendarGroup"
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
