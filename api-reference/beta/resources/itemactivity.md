---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActivity
ms.openlocfilehash: 7c8cdab7adc705333d1aeaad526aeeb813de10a7
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089501"
---
# <a name="itemactivity-resource-type"></a>Tipo de recurso ItemActivity

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **ItemActivity** proporciona información sobre las actividades que tuvieron lugar en un elemento o contenedor.
Actualmente, solo está disponible en SharePoint y OneDrive para la Empresa.

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "keyProperty": "id",
  "@type": "microsoft.graph.itemActivity",
  "@type.aka": "oneDrive.activityEntity"
}-->

```json
{
  "id": "string (identifier)",
  "access": "microsoft.graph.accessAction",
  "action": {"@odata.type": "microsoft.graph.itemActionSet"},
  "actor": {"@odata.type": "microsoft.graph.identitySet"},
  "driveItem": {"@odata.type": "microsoft.graph.driveItem"},
  "listItem": {"@odata.type": "microsoft.graph.listItem"},
  "location": {"@odata.type": "microsoft.graph.location"},
  "times": {"@odata.type": "microsoft.graph.itemActivityTimeSet"}
}
```

## <a name="properties"></a>Propiedades

| Propiedad | Tipo                    | Descripción
|:---------|:------------------------|:----------------------------------------
| id       | string                  | El identificador único de la actividad. Solo lectura.
| Access   | [accessAction][]        | Se tiene acceso a un elemento.
| action   | [itemActionSet][]       | Detalles sobre la acción que tuvo lugar. Solo lectura.
| actor    | [identitySet][]         | Identidad del usuario que ha realizado la acción. Solo lectura.
| location | [ubicación][]            | Ubicación física donde se llevó a cabo la acción. Solo lectura.
| times    | [itemActivityTimeSet][] | Detalles sobre cuándo tuvo lugar la actividad. Solo lectura.

[identitySet]: identityset.md
[itemActionSet]: itemactionset.md
[itemActivityTimeSet]: itemactivitytimeset.md

## <a name="relationships"></a>Relaciones

| Nombre de la relación | Tipo          | Descripción
|:------------------|:--------------|:-----------------------------------------
| driveItem         | [driveItem][] | Expone el objeto **driveItem** que era el destino de esta actividad.
| listItem          | [listItem][]  | Expone el objeto **listItem** que era el destino de esta actividad.

[driveItem]: driveitem.md
[listItem]: listitem.md

## <a name="actions"></a>Acciones

Las acciones que tuvieron lugar dentro de una actividad se detallan en la propiedad **action**.
A continuación se muestran las acciones que están disponibles actualmente.
Pueden registrarse nuevas acciones en el futuro, así que asegúrese de que su aplicación es tolerante al control de un recurso **itemActivity** sin ninguna acción que su aplicación comprenda.

| Nombre de acción | Tipo              | Descripción
|:------------|:------------------|:-------------------------------------------
| comment     | [commentAction][] | Se ha agregado un comentario al elemento.
| create      | [createAction][]  | Se ha creado un elemento.
| delete      | [deleteAction][]  | Se ha eliminado un elemento.
| edit        | [editAction][]    | Se ha editado un elemento.
| mention     | [mentionAction][] | Se ha mencionado a un usuario en el elemento.
| move        | [moveAction][]    | Se ha movido un elemento.
| rename      | [renameAction][]  | Se ha cambiado el nombre de un elemento.
| restore     | [restoreAction][] | Se ha restaurado un elemento.
| share       | [shareAction][]   | Se ha compartido un elemento.
| version     | [versionAction][] | Se ha cambiado la versión de un elemento.

[accessAction]: accessaction.md
[commentAction]: commentaction.md
[createAction]: createaction.md
[deleteAction]: deleteaction.md
[editAction]: editaction.md
[location]: location.md
[mentionAction]: mentionaction.md
[moveAction]: moveaction.md
[renameAction]: renameaction.md
[restoreAction]: restoreaction.md
[shareAction]: shareaction.md
[versionAction]: versionaction.md

## <a name="remarks"></a>Comentarios

Actualmente, **ItemActivity** solo está disponible en SharePoint y OneDrive para la Empresa.

<!-- {
  "type": "#page.annotation",
  "description": "The ItemActivity object provides information about an activity that took place on an item.",
  "keywords": "activities,activity,action",
  "section": "documentation",
  "tocPath": "Resources/ItemActivity"
} -->
