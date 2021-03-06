---
title: tipo de recurso educationOrganization
description: Entidades abstractas que se utiliza para modelar la uniformidad entre los tipos de organización diferentes en el sector de educación.
author: mmast-msft
localization_priority: Normal
ms.prod: education
ms.openlocfilehash: 99f3294f76a246e4e78f0f61b0fc1f62532c3a03
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977426"
---
# <a name="educationorganization-resource-type"></a>tipo de recurso educationOrganization

Entidades abstractas que se utiliza para modelar la uniformidad entre los tipos de organización diferentes en el sector de educación.

## <a name="properties"></a>Propiedades
| Propiedad     | Tipo   |Descripción|
|:---------------|:--------|:----------|
|description|Cadena| Descripción de la organización.|
|displayName|Cadena| Nombre para mostrar de organización.|
|externalSource|educationExternalSource| Origen donde se creó esta organización. Los valores posibles son: `sis`, `manual`, `unknownFutureValue`.|

## <a name="relationships"></a>Relaciones
Ninguna.


## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "abstract": true,
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.educationOrganization"
}-->

```json
{
  "description": "String",
  "displayName": "String",
  "externalSource": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "educationOrganization resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
