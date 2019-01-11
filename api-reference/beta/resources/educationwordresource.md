---
title: tipo de recurso educationWordResource
description: 'Una subclase de educationResource. Éste es un recurso de documento de Word. Se debe cargar el archivo de palabras en el directorio **fileResource** asociado con el '
localization_priority: Normal
ms.openlocfilehash: 0fa366a6fb6de70d10a010cf5e0e11ffd26a3b94
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27805141"
---
# <a name="educationwordresource-resource-type"></a>tipo de recurso educationWordResource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una subclase de [educationResource](educationresource.md). Éste es un recurso de documento de Word. En el directorio **fileResource** asociado con la asignación o el envío, se debe cargar el archivo de Word.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|fileUrl|Cadena|Ubicación del archivo en el disco.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationWordResource"
}-->

```json
{
  "fileUrl": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationWordResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
