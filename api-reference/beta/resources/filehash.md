---
title: tipo de recurso fileHash
description: Contiene información de estado acerca de los valores de hash de archivo (criptográficas y la ubicación).
localization_priority: Normal
ms.openlocfilehash: f5d865a7ded230ca611b8628c3648ec1e331c67d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27815648"
---
# <a name="filehash-resource-type"></a>tipo de recurso fileHash

Contiene información de estado acerca de los valores de hash de archivo (criptográficas y la ubicación).

## <a name="properties"></a>Propiedades

| Propiedad     | Tipo        | Description |
|:-------------|:------------|:------------|
|hashType|enumeración [fileHashType](filehashtypeenumtype.md)|Tipo de hash de archivo. Los valores posibles son: `unknown`, `sha1`, `sha256`, `md5`, `authenticodeHash256`, `lsHash`, `ctph`, `peSha1` y `peSha256`.|
|hashValue|Cadena|Valor de hash de archivo.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileHash"
}-->

```json
{
  "hashType": "@odata.type: microsoft.graph.fileHashType",
  "hashValue": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fileHash resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
