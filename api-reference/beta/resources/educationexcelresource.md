---
title: tipo de recurso educationExcelResource
description: 'Una subclase de educationResource. Este tipo de recurso representa un documento de Excel.  '
author: mmast-msft
localization_priority: Normal
ms.openlocfilehash: 7f772f7911667c76e64c31a856f3a9f8b6f3e6ff
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858103"
---
# <a name="educationexcelresource-resource-type"></a>tipo de recurso educationExcelResource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una subclase de [educationResource](educationresource.md). Este tipo de recurso representa un documento de Excel.  
 
>**Nota:** El archivo de Excel debe estar en la carpeta de recursos asociada con el objeto de asignación o el envío al que pertenece este recurso.


## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|fileUrl|Cadena|Puntero al objeto de archivo de Excel.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationExcelResource"
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
  "description": "educationExcelResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
