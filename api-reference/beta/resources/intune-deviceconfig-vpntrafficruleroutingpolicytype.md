---
title: tipo de enumeración vpnTrafficRuleRoutingPolicyType
description: Especifica la directiva de enrutamiento para una regla de tráfico VPN.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 2c8ec4303dc16c7cb0606e4b9cf86594446f571e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974955"
---
# <a name="vpntrafficruleroutingpolicytype-enum-type"></a>tipo de enumeración vpnTrafficRuleRoutingPolicyType

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Especifica la directiva de enrutamiento para una regla de tráfico VPN.
## <a name="members"></a>Miembros
|Miembro	|Valor|Descripción|
|:---|:---|:---|
|none|0|Ninguna directiva de enrutamiento especificada.|
|splitTunnel|1|El tráfico de red para la aplicación especificada se enrutarán a través de la VPN.|
|forceTunnel|2|Todo el tráfico de red se enrutarán a través de la VPN.|





