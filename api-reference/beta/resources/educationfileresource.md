---
title: tipo de recurso educationFileResource
description: Una subclase de educationResource que representa un objeto de archivo que está asociado con la asignación o el envío.  En este caso, el archivo no es uno de los archivos especiales (Word, Excel etc.), pero es un archivo que no tiene un tratamiento especial dentro del sistema. El recurso de archivo debe almacenarse en el **Carpetarecurso** que está asociada con la asignación o el envío de a que este recurso se adjunta.
localization_priority: Normal
ms.openlocfilehash: 5fda86b80030a2bc0c885b4dd90a384b7ede7fff
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858089"
---
# <a name="educationfileresource-resource-type"></a>tipo de recurso educationFileResource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una subclase de [educationResource](educationresource.md) que representa un objeto de archivo que está asociado con la asignación o el envío.  En este caso, el archivo no es uno de los archivos especiales (Word, Excel etc.), pero es un archivo que no tiene un tratamiento especial dentro del sistema. El recurso de archivo debe almacenarse en el **Carpetarecurso** que está asociada con la asignación o el envío de a que este recurso se adjunta.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Description|
|:---------------|:--------|:----------|
|fileUrl|Cadena|Ubicación en el disco del recurso de archivo.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationFileResource"
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
  "description": "educationFileResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
