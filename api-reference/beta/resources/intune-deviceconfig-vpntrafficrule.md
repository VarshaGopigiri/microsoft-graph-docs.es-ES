---
title: tipo de recurso vpnTrafficRule
description: Definición de la regla de tráfico de VPN.
author: tfitzmac
ms.openlocfilehash: 39303510fdfef39cbcb99df3f824ce29bcbfd65c
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27324650"
---
# <a name="vpntrafficrule-resource-type"></a>tipo de recurso vpnTrafficRule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Definición de la regla de tráfico de VPN.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|name|String|Nombre.|
|protocolos|Int32|Protocolos (0-255). Valores válidos de 0 a 255|
|localPortRanges|colección de [numberRange](../resources/intune-deviceconfig-numberrange.md)|Intervalo de puertos locales se puede establecer sólo al protocolo es TCP o UDP (6 o 17). Esta colección puede contener un máximo de 500 elementos.|
|remotePortRanges|colección de [numberRange](../resources/intune-deviceconfig-numberrange.md)|Intervalo de puertos remotos se puede establecer sólo al protocolo es TCP o UDP (6 o 17). Esta colección puede contener un máximo de 500 elementos.|
|localAddressRanges|colección de [iPv4Range](../resources/intune-shared-ipv4range.md)|Intervalo de direcciones local. Esta colección puede contener un máximo de 500 elementos.|
|remoteAddressRanges|colección de [iPv4Range](../resources/intune-shared-ipv4range.md)|Intervalo de direcciones remoto. Esta colección puede contener un máximo de 500 elementos.|
|appId|cadena|Identificador de la aplicación, si se desencadena esta regla de tráfico por una aplicación.|
|tipo de aplicación|[vpnTrafficRuleAppType](../resources/intune-deviceconfig-vpntrafficruleapptype.md)|Tipo de aplicación, si se desencadena esta regla de tráfico por una aplicación. Los valores posibles son: `none`, `desktop` y `universal`.|
|routingPolicyType|[vpnTrafficRuleRoutingPolicyType](../resources/intune-deviceconfig-vpntrafficruleroutingpolicytype.md)|Cuando aplicación desencadena, indica si se debe habilitar el túnel dividido a lo largo de esta ruta. Los valores posibles son: `none`, `splitTunnel` y `forceTunnel`.|
|notificaciones|String|Notificaciones asociados con esta regla de tráfico.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vpnTrafficRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vpnTrafficRule",
  "name": "String",
  "protocols": 1024,
  "localPortRanges": [
    {
      "@odata.type": "microsoft.graph.numberRange",
      "lowerNumber": 1024,
      "upperNumber": 1024
    }
  ],
  "remotePortRanges": [
    {
      "@odata.type": "microsoft.graph.numberRange",
      "lowerNumber": 1024,
      "upperNumber": 1024
    }
  ],
  "localAddressRanges": [
    {
      "@odata.type": "microsoft.graph.iPv4Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "remoteAddressRanges": [
    {
      "@odata.type": "microsoft.graph.iPv4Range",
      "lowerAddress": "String",
      "upperAddress": "String"
    }
  ],
  "appId": "String",
  "appType": "String",
  "routingPolicyType": "String",
  "claims": "String"
}
```





