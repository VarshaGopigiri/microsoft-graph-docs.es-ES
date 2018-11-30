---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActionSet
ms.openlocfilehash: 3b2f77ea21f2352b0a8fa647af84d9b0af08a2ab
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083458"
---
# <a name="itemactionset-resource-type"></a>Tipo de recurso ItemActionSet

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **ItemActionSet** proporciona información sobre las acciones que constituyeron una [actividad][itemActivity] en un elemento.

[itemActivity]: itemactivity.md

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "keyProperty": "id",
  "@type": "microsoft.graph.itemActionSet",
  "@type.aka": "oneDrive.action"
}-->

```json
{
  "comment": {"@odata.type": "microsoft.graph.commentAction"},
  "create": {"@odata.type": "microsoft.graph.createAction"},
  "delete": {"@odata.type": "microsoft.graph.deleteAction"},
  "edit": {"@odata.type": "microsoft.graph.editAction"},
  "mention": {"@odata.type": "microsoft.graph.mentionAction"},
  "move": {"@odata.type": "microsoft.graph.moveAction"},
  "rename": {"@odata.type": "microsoft.graph.renameAction"},
  "restore": {"@odata.type": "microsoft.graph.restoreAction"},
  "share": {"@odata.type": "microsoft.graph.shareAction"},
  "version": {"@odata.type": "microsoft.graph.versionAction"},
  
}
```

## <a name="properties"></a>Propiedades

A continuación se muestran las acciones que están disponibles actualmente.
Pueden registrarse nuevas acciones en el futuro, así que asegúrese de que su aplicación es tolerante al control de un recurso **itemActionSet** sin ninguna acción que su aplicación comprenda.

| Nombre de la propiedad | Tipo              | Descripción
|:--------------|:------------------|:-----------------------------------------
| comment       | [commentAction][] | Se ha agregado un comentario al elemento.
| create        | [createAction][]  | Se ha creado un elemento.
| delete        | [deleteAction][]  | Se ha eliminado un elemento.
| edit          | [editAction][]    | Se ha editado un elemento.
| mention       | [mentionAction][] | Se ha mencionado a un usuario en el elemento.
| move          | [moveAction][]    | Se ha movido un elemento.
| rename        | [renameAction][]  | Se ha cambiado el nombre de un elemento.
| restore       | [restoreAction][] | Se ha restaurado un elemento.
| share         | [shareAction][]   | Se ha compartido un elemento.
| version       | [versionAction][] | Se ha cambiado la versión de un elemento.

[commentAction]: commentaction.md
[createAction]: createaction.md
[deleteAction]: deleteaction.md
[editAction]: editaction.md
[mentionAction]: mentionaction.md
[moveAction]: moveaction.md
[renameAction]: renameaction.md
[restoreAction]: restoreaction.md
[shareAction]: shareaction.md
[versionAction]: versionaction.md

## <a name="remarks"></a>Comentarios

Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.

<!-- {
  "type": "#page.annotation",
  "description": "The ItemActionSet object provides information about the actions that took place as part of an activity on an item.",
  "keywords": "activities,activity,action",
  "section": "documentation",
  "tocPath": "Resources/ItemActionSet"
} -->
