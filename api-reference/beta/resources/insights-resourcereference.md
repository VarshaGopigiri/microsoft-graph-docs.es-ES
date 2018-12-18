---
title: tipo de recurso resourceReference
description: Tipo complejo que contiene las propiedades de conocimientos.
author: simonhult
ms.openlocfilehash: 2f1a44412eebbb7a74895c12db9a07696d6ee409
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27363623"
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

| Propiedad      | Tipo      | Descripción  |
| ------------- |-----------| -------------|
| webUrl        | String    | Una dirección URL conduce al elemento referenciado. |
| id            | String    | Identificador único del elemento.           |
| type          | String    | Un valor de tipo string que se puede usar para clasificar el elemento, como "microsoft.graph.driveItem" |