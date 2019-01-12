---
title: tipo de recurso educationFileResource
description: Una subclase de educationResource que representa un objeto de archivo que está asociado con la asignación o el envío.  En este caso, el archivo no es uno de los archivos especiales (Word, Excel etc.), pero es un archivo que no tiene un tratamiento especial dentro del sistema. El recurso de archivo debe almacenarse en el **Carpetarecurso** que está asociada con la asignación o el envío de a que este recurso se adjunta.
localization_priority: Normal
author: mmast-msft
ms.prod: education
ms.openlocfilehash: 96c03dc1571e0f8686116f169706aa35003f92a3
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953661"
---
# <a name="educationfileresource-resource-type"></a>tipo de recurso educationFileResource

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Una subclase de [educationResource](educationresource.md) que representa un objeto de archivo que está asociado con la asignación o el envío.  En este caso, el archivo no es uno de los archivos especiales (Word, Excel etc.), pero es un archivo que no tiene un tratamiento especial dentro del sistema. El recurso de archivo debe almacenarse en el **Carpetarecurso** que está asociada con la asignación o el envío de a que este recurso se adjunta.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
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
