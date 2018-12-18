---
title: Tipo de recurso iPv4Range
description: Intervalo IPv4
author: tfitzmac
ms.openlocfilehash: 3dd5479776cf5f497ab6f26e893a78c73fa6ad86
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27316670"
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



