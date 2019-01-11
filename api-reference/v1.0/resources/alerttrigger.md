---
title: tipo de recurso alertTrigger
description: Contiene información acerca de las propiedades que desencadena una detección (existen propiedades de la entidad de alerta).
author: Preetikr
localization_priority: Normal
ms.openlocfilehash: 1dc8bb2b18380da50134aa67e742da89dea3c057
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894344"
---
# <a name="alerttrigger-resource-type"></a>tipo de recurso alertTrigger

Contiene información acerca de las propiedades que desencadena una detección (existen propiedades de la entidad de alerta).

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo|Descripción|
|:---------------|:--------|:----------|
|name|Cadena|Nombre de la propiedad que actúa como un desencadenador de detección.|
|type|Cadena|Tipo de la propiedad en el par de clave: valor de interpretación. Por ejemplo, String, Boolean, etcetera.|
|valor|String|Valor de la propiedad que actúa como un desencadenador de detección.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.alertTrigger"
}-->

```json
{
  "name": "String",
  "type": "String",
  "value": "String"
}

```

## <a name="example"></a>Ejemplo

```json
{
  "name": "hostState.privateIpAddress",
  "type": "String",
  "value": "10.154.9.40"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "alertTrigger resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
