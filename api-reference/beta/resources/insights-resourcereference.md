---
title: tipo de recurso resourceReference
description: Tipo complejo que contiene las propiedades de conocimientos.
ms.openlocfilehash: d171151a1c3547aa6863a7f70cc3a42ddec13e5d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087950"
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