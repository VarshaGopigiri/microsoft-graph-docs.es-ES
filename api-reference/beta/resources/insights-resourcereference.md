---
title: tipo de recurso resourceReference
description: Tipo complejo que contiene las propiedades de conocimientos.
author: simonhult
localization_priority: Normal
ms.prod: insights
ms.openlocfilehash: 23a05a362ea57c84dceecbd9523c2620edc21fbf
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966289"
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
| webUrl        | Cadena    | Una dirección URL conduce al elemento referenciado. |
| id            | Cadena    | Identificador único del elemento.           |
| type          | Cadena    | Un valor de tipo string que se puede usar para clasificar el elemento, como "microsoft.graph.driveItem" |
