---
title: Tipo de recurso recentNotebookLinks
description: Vínculos para abrir un bloc de notas de OneNote. Este tipo de recurso existe como propiedad en un recurso recentNotebook.
localization_priority: Normal
ms.openlocfilehash: 5ccf861541526a1673d6174176cb8b2a62df6c23
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812876"
---
# <a name="recentnotebooklinks-resource-type"></a>Tipo de recurso recentNotebookLinks

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Vínculos para abrir un bloc de notas de OneNote. Este tipo de recurso existe como propiedad en un recurso [recentNotebook](recentnotebook.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|oneNoteClientUrl|[externalLink](externallink.md)|Se abre el Bloc de notas en el cliente de OneNote, si está instalado.|
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
