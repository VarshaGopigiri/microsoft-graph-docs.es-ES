---
title: Tipo de recurso iPv6Range
description: Intervalo IPv6
author: tfitzmac
ms.openlocfilehash: b5a2ad772d45b4be5fa3a8f4da04b28bc965195d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27337551"
---
# <a name="ipv6range-resource-type"></a>Tipo de recurso iPv6Range

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Intervalo IPv6

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
  "@odata.type": "microsoft.graph.iPv6Range"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.iPv6Range",
  "lowerAddress": "String",
  "upperAddress": "String"
}
```



