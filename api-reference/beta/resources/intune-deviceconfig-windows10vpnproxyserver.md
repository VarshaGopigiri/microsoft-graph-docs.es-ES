---
title: tipo de recurso windows10VpnProxyServer
description: Servidor de Proxy VPN.
author: tfitzmac
ms.openlocfilehash: e21b964ab1bd648cd042a1364ecf5f0942ded085
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309460"
---
# <a name="windows10vpnproxyserver-resource-type"></a>tipo de recurso windows10VpnProxyServer

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Servidor de Proxy VPN.

Hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|automaticConfigurationScriptUrl|String|Url de secuencia de comandos de configuración automática del proxy. Se hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)|
|address|String|Dirección. Se hereda de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)|
|port|Int32|Puerto. Válido valores heredada de 0 a 65535 de [vpnProxyServer](../resources/intune-deviceconfig-vpnproxyserver.md)|
|bypassProxyServerForLocalAddress|Boolean|No usar servidor proxy para direcciones locales.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windows10VpnProxyServer"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10VpnProxyServer",
  "automaticConfigurationScriptUrl": "String",
  "address": "String",
  "port": 1024,
  "bypassProxyServerForLocalAddress": true
}
```





