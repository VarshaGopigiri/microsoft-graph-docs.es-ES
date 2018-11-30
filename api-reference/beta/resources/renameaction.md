---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: RenameAction
ms.openlocfilehash: 12956ab51923f6d9f175b25203bf2921a64a8a6b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086479"
---
# <a name="renameaction-resource-type"></a>Tipo de recurso RenameAction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

La presencia del recurso **RenameAction** en un recurso [**itemActivity**][activity] indica que la actividad ha cambiado el nombre de un elemento.

[activity]: itemactivity.md

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.renameAction"
}-->

```json
{
  "oldName": "string",
  "newName": "string"
}
```

## <a name="properties"></a>Propiedades

| Nombre de propiedad | Tipo   | Descripción
|:--------------|:-------|:----------------------------------------------------
| oldName       | string | El nombre anterior del elemento.
| newName       | string | El nuevo nombre del elemento.

## <a name="remarks"></a>Comentarios

Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.

<!-- {
  "type": "#page.annotation",
  "description": "The RenameAction object provides information about an activity that renamed an item.",
  "keywords": "activities,activity,action,rename,renamed",
  "section": "documentation",
  "tocPath": "Resources/RenameAction"
} -->
