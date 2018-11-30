---
author: daspek
ms.author: dspektor
ms.date: 10/06/2017
title: IncompleteData
ms.openlocfilehash: 4319ab0f36e12ddd28ca9bb6c7bfd48043228504
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084186"
---
# <a name="incompletedata-resource-type"></a>tipo de recurso incompleteData

 > **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

El aspecto de **incompleteData** indica que se ha generado un recurso con datos incompletos.
Las propiedades dentro de pueden proporcionar información acerca de por qué hay datos incompletos.

## <a name="json-representation"></a>Representación JSON

<!-- { "blockType": "resource", "@type": "microsoft.graph.incompleteData" } -->

```json
{
  "missingDataBeforeDateTime": "String (timestamp)",
  "wasThrottled": false
}
```

## <a name="properties"></a>Propiedades

| Propiedad                  | Tipo           | Descripción
|:--------------------------|:---------------|:--------------------------------
| missingDataBeforeDateTime | DateTimeOffset | El servicio no tiene datos de origen antes de la hora especificada.
| wasThrottled              | Booleano        | Algunos datos no se grabó debido a una actividad excesiva.

<!-- {
  "type": "#page.annotation",
  "section": "documentation",
  "tocPath": "Facets/IncompleteData"
} -->
