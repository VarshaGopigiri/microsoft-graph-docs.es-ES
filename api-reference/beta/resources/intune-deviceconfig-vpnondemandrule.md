---
title: tipo de recurso vpnOnDemandRule
description: Definición de la regla de petición de VPN.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: bd6e494975c8626a25380b3f037d702fb81e082b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27875638"
---
# <a name="vpnondemandrule-resource-type"></a>tipo de recurso vpnOnDemandRule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Definición de la regla de petición de VPN.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Description|
|:---|:---|:---|
|SSID|Colección String|Servicio de red establece identificadores (SSID).|
|dnsSearchDomains|Colección String|Dominios de búsqueda DNS.|
|probeUrl|Cadena|Una dirección URL de sondeo. Si esta dirección URL es correctamente se capturaron (que devuelve un código de estado HTTP 200) sin el redireccionamiento, coincide esta regla.|
|action|[vpnOnDemandRuleConnectionAction](../resources/intune-deviceconfig-vpnondemandruleconnectionaction.md)|Acción. Los valores posibles son: `connect`, `evaluateConnection`, `ignore` y `disconnect`.|
|domainAction|[vpnOnDemandRuleConnectionDomainAction](../resources/intune-deviceconfig-vpnondemandruleconnectiondomainaction.md)|Acción de dominio (sólo se aplica cuando la acción es evaluar la conexión). Los valores posibles son: `connectIfNeeded` y `neverConnect`.|
|dominios|Colección String|Dominios (solo se aplica cuando la acción es evaluar la conexión).|
|probeRequiredUrl|Cadena|Sondeo obligatorio Url (solo se aplica cuando la acción es evaluar la conexión y DomainAction es conectar si es necesario).|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.vpnOnDemandRule"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.vpnOnDemandRule",
  "ssids": [
    "String"
  ],
  "dnsSearchDomains": [
    "String"
  ],
  "probeUrl": "String",
  "action": "String",
  "domainAction": "String",
  "domains": [
    "String"
  ],
  "probeRequiredUrl": "String"
}
```





