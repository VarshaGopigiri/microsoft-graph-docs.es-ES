---
title: tipo de recurso alertTrigger
description: Contiene información acerca de las propiedades que desencadena una detección (existen propiedades de la entidad de alerta).
author: preetikr
localization_priority: Normal
ms.prod: security
ms.openlocfilehash: 3a2f6818bad0c5600e4b2a2a2682707643d1900c
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27991261"
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
