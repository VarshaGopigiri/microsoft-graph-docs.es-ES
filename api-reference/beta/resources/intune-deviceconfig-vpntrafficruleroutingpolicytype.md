---
title: tipo de enumeración vpnTrafficRuleRoutingPolicyType
description: Especifica la directiva de enrutamiento para una regla de tráfico VPN.
ms.openlocfilehash: df51851ef0820f5982a6689421503364e9064c78
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085906"
---
# <a name="vpntrafficruleroutingpolicytype-enum-type"></a>tipo de enumeración vpnTrafficRuleRoutingPolicyType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Especifica la directiva de enrutamiento para una regla de tráfico VPN.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|ninguno|0|Ninguna directiva de enrutamiento especificada.|
|splitTunnel|1|El tráfico de red para la aplicación especificada se enrutarán a través de la VPN.|
|forceTunnel|2|Todo el tráfico de red se enrutarán a través de la VPN.|





