---
title: tipo de recurso networkInterface
description: Representa una tarjeta de interfaz de red (NIC) asociado con este host.
ms.openlocfilehash: 7044b4f469e74424b0dc27ffa38c5feb081faa45
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083847"
---
# <a name="networkinterface-resource-type"></a>tipo de recurso networkInterface

Representa una tarjeta de interfaz de red (NIC) asociado con este host.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|description|String|Descripción de la NIC (por ejemplo, adaptador Ethernet, conexión de área Local del adaptador de red LAN inalámbrica * <> #, etcetera.).|
|ipV4Address|String|Última dirección IPv4 asociado con esta NIC.|
|ipV6Address|String|Última pública (también conocido como) dirección IPv6 global asociado con esta NIC.|
|localIpV6Address|String|Última local (local de vínculo o local del sitio) dirección IPv6 asociada con esta NIC.|
|dirección MAC|String|Dirección MAC de la NIC en este host.|

## <a name="json-representation"></a>Representación JSON

La siguiente es una representación JSON del recurso

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.networkInterface"
}-->

```json
{
  "description": "String",
  "ipV4Address": "String",
  "ipV6Address": "String",
  "localIpV6Address": "String",
  "macAddress": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "networkInterface resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->