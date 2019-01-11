---
title: Tipo de recurso iPv4Range
description: Intervalo IPv4
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 593fc2287e888b38eadd3c588aaeeb51b31ea78f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27816264"
---
# <a name="ipv4range-resource-type"></a>Tipo de recurso iPv4Range

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Intervalo IPv4

Hereda de [ipRange](../resources/intune-mam-iprange.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|lowerAddress|cadena|Dirección IP inferior|
|upperAddress|cadena|Dirección IP superior|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.iPv4Range"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iPv4Range",
  "lowerAddress": "String",
  "upperAddress": "String"
}
```



