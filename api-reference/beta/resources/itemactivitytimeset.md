---
author: daspek
ms.author: dspektor
ms.date: 09/14/2017
title: ItemActivityTimeSet
ms.openlocfilehash: 7a8852af9fc9c99f69b8d61f53037be91f35b31e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090766"
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

| Nombre de propiedad    | Tipo           | Descripción
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
