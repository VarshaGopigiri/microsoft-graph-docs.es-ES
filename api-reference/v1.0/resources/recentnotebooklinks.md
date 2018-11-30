---
title: Tipo de recurso recentNotebookLinks
description: Vínculos para abrir un bloc de notas de OneNote. Este tipo de recurso existe como propiedad en un recurso recentNotebook.
ms.openlocfilehash: 594616a790becd77086177157f71321ffdd36e24
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029606"
---
# <a name="recentnotebooklinks-resource-type"></a>Tipo de recurso recentNotebookLinks

Vínculos para abrir un bloc de notas de OneNote. Este tipo de recurso existe como propiedad en un recurso [recentNotebook](recentnotebook.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|oneNoteClientUrl|[externalLink](externallink.md)|Abre el bloc de notas en el cliente nativo de OneNote si está instalado.|
|oneNoteWebUrl|[externalLink](externallink.md)|Abre el bloc de notas en OneNote Online.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recentNotebookLinks"
}-->

```json
{
  "oneNoteClientUrl": {"@odata.type": "microsoft.graph.externalLink"},
  "oneNoteWebUrl": {"@odata.type": "microsoft.graph.externalLink"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recentNotebookLinks resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
