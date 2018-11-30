---
title: tipo de recurso fileSecurityState
description: Contiene información sobre el archivo (no process) relacionados con la alerta.
ms.openlocfilehash: d1358d7fe0d5565845201781e32b3da14a89f412
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27032377"
---
# <a name="filesecuritystate-resource-type"></a>tipo de recurso fileSecurityState

Contiene información sobre el archivo (no process) relacionados con la alerta.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|fileHash|[fileHash](filehash.md)|Tipo complejo que contiene los valores de hash de archivo (criptográficas y la ubicación).|
|name|String|Nombre de archivo (sin ruta de acceso).|
|ruta de acceso|String|Ruta de acceso completa al archivo del archivo/imageFile.|
|riskScore|String|Proveedor generado/calcula el riesgo de puntuación del archivo alerta. Valor recomendado el rango de 0-1, lo que equivale a un porcentaje.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileSecurityState"
}-->

```json
{
  "fileHash": {"@odata.type": "microsoft.graph.fileHash"},
  "name": "String",
  "path": "String",
  "riskScore": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "fileSecurityState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->