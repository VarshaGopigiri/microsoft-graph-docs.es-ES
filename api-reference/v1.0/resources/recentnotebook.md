---
title: Tipo de recurso recentNotebook
description: Bloc de notas de OneNote al que se ha accedido recientemente. Un **recentNotebook** es similar a un notebook pero tiene menos propiedades.
localization_priority: Normal
ms.openlocfilehash: 67c707043e5b6ca65cd72ddc323b5a484f0f2959
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889228"
---
# <a name="recentnotebook-resource-type"></a>Tipo de recurso recentNotebook

Bloc de notas de OneNote al que se ha accedido recientemente. Un **recentNotebook** es similar a un [notebook](notebook.md) pero tiene menos propiedades.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName|Cadena|Nombre del bloc de notas.|
|lastAccessedTime|DateTimeOffset|La fecha y la hora en que se modificó por última vez el bloc de notas. La marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y siempre pertenece a la zona horaria UTC. Por ejemplo, medianoche en la zona horaria UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`. Solo lectura.|
|links|[recentNotebookLinks](recentnotebooklinks.md)|Vínculos para abrir el bloc de notas. El vínculo `oneNoteClientURL` abre el bloc de notas en el cliente de OneNote si está instalado. El vínculo `oneNoteWebURL` abre el bloc de notas en OneNote Online.|
|sourceService|onenoteSourceService|Almacén de back-end donde reside el Bloc de notas, `OneDriveForBusiness` o `OneDrive`.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recentNotebook"
}-->

```json
{
  "displayName": "String",
  "lastAccessedTime": "String (timestamp)",
  "links": {"@odata.type": "microsoft.graph.recentNotebookLinks"},
  "sourceService": "String"
}
```

## <a name="methods"></a>Métodos

| Método           | Tipo de valor devuelto    |Descripción|
|:---------------|:--------|:----------|
|[getRecentNotebooks](../api/notebook-getrecentnotebooks.md) | Colección [notebook](notebook.md) | Obtener una colección de los blocs de notas a los que el usuario ha accedido más recientemente. |
