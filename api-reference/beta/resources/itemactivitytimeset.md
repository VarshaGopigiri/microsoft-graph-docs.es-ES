---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActivityTimeSet
localization_priority: Normal
ms.openlocfilehash: 2ff3e1a2356c43457fe251928728632bd2228b10
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27809895"
---
# <a name="itemactivitytimeset-resource-type"></a>Tipo de recurso ItemActivityTimeSet

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El recurso **ItemActivityTimeSet** proporciona información sobre cuándo se produjo una [actividad][activity] en un elemento.

[activity]: itemactivity.md

## <a name="json-representation"></a>Representación JSON

<!-- {
  "blockType": "resource",
  "optionalProperties": [ ],
  "keyProperty": "id",
  "@type": "microsoft.graph.itemActivityTimeSet",
  "@type.aka": "oneDrive.times",
  "@property.aka": "observedDateTime=observedTime recordedDateTime=recordedTime"
}-->

```json
{
  "observedDateTime": "String (timestamp)",
  "recordedDateTime": "String (timestamp)"
}
```

## <a name="properties"></a>Propiedades

| Nombre de la propiedad    | Tipo           | Descripción
|:-----------------|:---------------|:-----------------------------------------
| observedDateTime | DateTimeOffset | Cuándo se observó que se produjo la actividad.
| recordedDateTime | DateTimeOffset | Cuándo se registró la observación en el servicio.

La diferencia entre las horas **observed** y **recorded** es especialmente importante para los escenarios de colaboración sin conexión.
Si un usuario comenta en un archivo mientras está sin conexión, la hora en que hizo el comentario se establece como **observedDateTime**.
En un momento posterior, cuando el usuario se vuelve a conectar a la nube y se cargan los cambios, esa hora posterior se establece como **recordedDateTime**.

## <a name="remarks"></a>Comentarios

Actualmente, los registros de actividad de elementos solo están disponibles en SharePoint y OneDrive para la Empresa.

<!-- {
  "type": "#page.annotation",
  "description": "The ItemActionSet object provides information about an activity that took place on an item.",
  "keywords": "activities,activity,action",
  "section": "documentation",
  "tocPath": "Resources/ItemActionSet"
} -->
