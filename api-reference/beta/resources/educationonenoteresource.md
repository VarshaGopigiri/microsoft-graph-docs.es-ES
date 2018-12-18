---
title: tipo de recurso educationOneNoteResource
description: 'Una subclase de educationResource. Esto representa la ubicación de la página de OneNote.  '
author: mmast-msft
ms.openlocfilehash: dc6fc6a71da12a27cb589e072371814e4bc33cc1
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27359867"
---
# <a name="educationonenoteresource-resource-type"></a>tipo de recurso educationOneNoteResource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una subclase de [educationResource](educationresource.md). Esto representa la ubicación de la página de OneNote.  

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|pageUrl|String|La dirección URL Microsoft Graph a la página de OneNote.|
|sectionName|String|Nombre de la sección que se deben copiar en distribuciones o que se han copiado en.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationOneNoteResource"
}-->

```json
{
  "pageUrl": "String",
  "sectionName": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationOneNoteResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
