---
title: tipo de recurso networkInterface
description: Representa una tarjeta de interfaz de red (NIC) asociado con este host.
localization_priority: Normal
ms.openlocfilehash: 92ea26b76de8fa6ffbcdcf0bc64b85a08d0f51af
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27823306"
---
# <a name="networkinterface-resource-type"></a>tipo de recurso networkInterface

Representa una tarjeta de interfaz de red (NIC) asociado con este host.

## <a name="properties"></a>Propiedades

| Propiedad   | Tipo |Descripción|
|:---------------|:--------|:----------|
|description|Cadena|Descripción de la NIC (por ejemplo, adaptador Ethernet, conexión de área Local del adaptador de red LAN inalámbrica * <> #, etcetera.).|
|ipV4Address|Cadena|Última dirección IPv4 asociado con esta NIC.|
|ipV6Address|Cadena|Última pública (también conocido como) dirección IPv6 global asociado con esta NIC.|
|localIpV6Address|Cadena|Última local (local de vínculo o local del sitio) dirección IPv6 asociada con esta NIC.|
|dirección MAC|Cadena|Dirección MAC de la NIC en este host.|

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
