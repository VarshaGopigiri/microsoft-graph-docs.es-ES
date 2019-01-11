---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: DeleteAction
localization_priority: Normal
ms.openlocfilehash: a845a6609991041f12266cd97e95460f96bf742f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27876765"
---
# <a name="deleteaction-resource-type"></a>Tipo de recurso DeleteAction

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

La presencia del recurso **DeleteAction** en un recurso [**itemActivity**][activity] indica que la actividad ha eliminado un elemento.

[activity]: itemactivity.md

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "@type": "microsoft.graph.deleteAction"
}-->

```json
{
  "name": "string",
  "objectType": "File | Folder"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad | Tipo   | Descripción
|:--------------|:-------|:----------------------------------------------------
| name          | string | El nombre del elemento que se ha eliminado.
| objectType    | string | `File`o `Folder`, en función del tipo de los elementos eliminados.

## <a name="remarks"></a>Comentarios

Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.

<!-- {
  "type": "#page.annotation",
  "description": "The DeleteAction object provides information about the deletion of an item.",
  "keywords": "activities,activity,action,delete,deletion",
  "section": "documentation",
  "tocPath": "Resources/DeleteAction"
} -->
