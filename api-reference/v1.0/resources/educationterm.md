---
title: Tipo de recurso educationTerm
description: Período. Representa una parte designada del año académico. Se usa en educationClass.
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: af11aa6b4a110417152c76dd606245a18ad51c28
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851453"
---
# <a name="educationterm-resource-type"></a>Tipo de recurso educationTerm

Período. Representa una parte designada del año académico. Se usa en [educationClass](educationclass.md).

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|displayName| String| Nombre para mostrar del período.| 
|externalId|String| Identificador del período en el sistema de sincronización.|
|startDate|Date|Inicio del período.|
|endDate|Date|Final del período.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationTerm"
}-->

```json
{
  "displayName": "String",
  "externalId": "String",
  "startDate": "Date",
  "endDate": "Date"
}
```

<!-- uuid: 4e9d671f-3068-4e09-aba2-b39e81a0e452
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationTerm resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
