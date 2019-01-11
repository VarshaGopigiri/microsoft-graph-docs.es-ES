---
title: tipo de recurso resourceReference
description: Tipo complejo que contiene las propiedades de conocimientos.
author: simonhult
localization_priority: Normal
ms.openlocfilehash: 8ab2a79d66db6a45ecf3df748cf8f5740721ef80
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874329"
---
# <a name="resourcereference-resource-type"></a>tipo de recurso resourceReference

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se admite el uso de estas API en aplicaciones de producción.

Tipo complejo que contiene las propiedades de [conocimientos](insights.md).

## <a name="json-representation"></a>Representación JSON

Aquí tiene una representación JSON del recurso

```json
{
  "webUrl": "string",
  "id": "string",
  "type": "string"
}
```

## <a name="properties"></a>Propiedades

| Propiedad      | Tipo      | Description  |
| ------------- |-----------| -------------|
| webUrl        | Cadena    | Una dirección URL conduce al elemento referenciado. |
| id            | Cadena    | Identificador único del elemento.           |
| type          | Cadena    | Un valor de tipo string que se puede usar para clasificar el elemento, como "microsoft.graph.driveItem" |
