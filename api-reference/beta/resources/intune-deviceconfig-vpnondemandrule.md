---
title: tipo de recurso vpnOnDemandRule
description: Definición de la regla de petición de VPN.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 43908a55ff43c533d02ace629a80b96dc09c10ef
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27955418"
---
# <a name="vpnondemandrule-resource-type"></a>tipo de recurso vpnOnDemandRule

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Definición de la regla de petición de VPN.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|SSID|Colección String|Servicio de red establece identificadores (SSID).|
|dnsSearchDomains|Colección String|Dominios de búsqueda DNS.|
|probeUrl|String|Una dirección URL de sondeo. Si esta dirección URL es correctamente se capturaron (que devuelve un código de estado HTTP 200) sin el redireccionamiento, coincide esta regla.|
|action|[vpnOnDemandRuleConnectionAction](../resources/intune-deviceconfig-vpnondemandruleconnectionaction.md)|Acción. Los valores posibles son: `connect`, `evaluateConnection`, `ignore` y `disconnect`.|
|domainAction|[vpnOnDemandRuleConnectionDomainAction](../resources/intune-deviceconfig-vpnondemandruleconnectiondomainaction.md)|Acción de dominio (sólo se aplica cuando la acción es evaluar la conexión). Los valores posibles son: `connectIfNeeded` y `neverConnect`.|
|dominios|Colección String|Dominios (solo se aplica cuando la acción es evaluar la conexión).|
|probeRequiredUrl|String|Sondeo obligatorio Url (solo se aplica cuando la acción es evaluar la conexión y DomainAction es conectar si es necesario).|

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





