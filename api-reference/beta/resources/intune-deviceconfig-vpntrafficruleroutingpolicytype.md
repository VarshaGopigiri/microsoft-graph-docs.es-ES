---
title: tipo de enumeración vpnTrafficRuleRoutingPolicyType
description: Especifica la directiva de enrutamiento para una regla de tráfico VPN.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 2b44a2b58cc42e9f3f88964d79473327f4ca2b74
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27855324"
---
# <a name="vpntrafficruleroutingpolicytype-enum-type"></a>tipo de enumeración vpnTrafficRuleRoutingPolicyType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Especifica la directiva de enrutamiento para una regla de tráfico VPN.
## <a name="members"></a>Miembros
|Miembro	|Valor|Description|
|:---|:---|:---|
|none|0|Ninguna directiva de enrutamiento especificada.|
|splitTunnel|1|El tráfico de red para la aplicación especificada se enrutarán a través de la VPN.|
|forceTunnel|2|Todo el tráfico de red se enrutarán a través de la VPN.|





