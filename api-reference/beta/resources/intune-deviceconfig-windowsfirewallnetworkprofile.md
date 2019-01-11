---
title: Tipo de recurso windowsFirewallNetworkProfile
description: Directivas de perfiles de firewall de Windows.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8f6431d1a19c2e74dd2cf009ee433f10dc9ecb51
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27877066"
---
# <a name="windowsfirewallnetworkprofile-resource-type"></a>Tipo de recurso windowsFirewallNetworkProfile

> **Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios. No se permite el uso de estas API en aplicaciones de producción.

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directivas de perfiles de firewall de Windows.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|firewallEnabled|[stateManagementSetting](../resources/intune-deviceconfig-statemanagementsetting.md)|Configura los dispositivos de host para permitir o bloquear el servidor de seguridad y cumplimiento de seguridad avanzada para el perfil de red. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.|
|stealthModeRequired|Booleano|Permitir que el servidor para que funcione en modo oculto. Cuando StealthModeRequired y StealthModeBlocked son true, StealthModeBlocked tiene prioridad.|
|stealthModeBlocked|Booleano|Impedir que el servidor funcione en modo oculto. Cuando StealthModeRequired y StealthModeBlocked son true, StealthModeBlocked tiene prioridad.|
|incomingTrafficRequired|Booleano|Configura el firewall para permitir el tráfico entrante con arreglo a otras configuraciones de directiva. Cuando IncomingTrafficRequired y IncomingTrafficBlocked son true, IncomingTrafficBlocked tiene prioridad.|
|incomingTrafficBlocked|Booleano|Configura el servidor de seguridad para bloquear todo el tráfico entrante, independientemente de otras configuraciones de directiva. Cuando IncomingTrafficRequired y IncomingTrafficBlocked son true, IncomingTrafficBlocked tiene prioridad.|
|unicastResponsesToMulticastBroadcastsRequired|Booleano|Configura el firewall para permitir las respuestas de unidifusión al tráfico de difusión de multidifusión. Cuando UnicastResponsesToMulticastBroadcastsRequired y UnicastResponsesToMulticastBroadcastsBlocked son true, UnicastResponsesToMulticastBroadcastsBlocked tiene prioridad.|
|unicastResponsesToMulticastBroadcastsBlocked|Booleano|Configura el firewall para bloquear respuestas de unidifusión al tráfico de difusión de multidifusión. Cuando UnicastResponsesToMulticastBroadcastsRequired y UnicastResponsesToMulticastBroadcastsBlocked son true, UnicastResponsesToMulticastBroadcastsBlocked tiene prioridad.|
|inboundNotificationsRequired|Booleano|Permite que el servidor de seguridad mostrar las notificaciones cuando una aplicación se bloquee en un puerto de escucha. Cuando InboundNotificationsRequired y InboundNotificationsBlocked son true, InboundNotificationsBlocked tiene prioridad.|
|inboundNotificationsBlocked|Booleano|Impide que el firewall muestre notificaciones cuando una aplicación se bloquee en un puerto de escucha. Cuando InboundNotificationsRequired y InboundNotificationsBlocked son true, InboundNotificationsBlocked tiene prioridad.|
|authorizedApplicationRulesFromGroupPolicyMerged|Booleano|Configura el firewall para combinar reglas de aplicación autorizado de directiva de grupo con las del almacén local en lugar de omitir las reglas del almacén local. Cuando AuthorizedApplicationRulesFromGroupPolicyNotMerged y AuthorizedApplicationRulesFromGroupPolicyMerged son true, AuthorizedApplicationRulesFromGroupPolicyMerged tiene prioridad.|
|authorizedApplicationRulesFromGroupPolicyNotMerged|Booleano|Configura el servidor de seguridad para evitar que la combinación de aplicaciones autorizados las reglas de directiva de grupo con las del almacén local en lugar de omitir la local almacenan las reglas. Cuando AuthorizedApplicationRulesFromGroupPolicyNotMerged y AuthorizedApplicationRulesFromGroupPolicyMerged son true, AuthorizedApplicationRulesFromGroupPolicyMerged tiene prioridad.|
|globalPortRulesFromGroupPolicyMerged|Booleano|Configura el firewall para combinar reglas de puerto global de directiva de grupo con las del almacén local en lugar de omitir las reglas del almacén local. Cuando GlobalPortRulesFromGroupPolicyNotMerged y GlobalPortRulesFromGroupPolicyMerged son true, GlobalPortRulesFromGroupPolicyMerged tiene prioridad.|
|globalPortRulesFromGroupPolicyNotMerged|Booleano|Configura el servidor de seguridad para evitar que la combinación de reglas de puerto global de directiva de grupo con las del almacén local en lugar de omitir las reglas del almacén local. Cuando GlobalPortRulesFromGroupPolicyNotMerged y GlobalPortRulesFromGroupPolicyMerged son true, GlobalPortRulesFromGroupPolicyMerged tiene prioridad.|
|connectionSecurityRulesFromGroupPolicyMerged|Booleano|Configura el firewall para combinar las reglas de seguridad de directiva de grupo con las del almacén local en lugar de omitir las reglas del almacén local. Cuando ConnectionSecurityRulesFromGroupPolicyNotMerged y ConnectionSecurityRulesFromGroupPolicyMerged son true, ConnectionSecurityRulesFromGroupPolicyMerged tiene prioridad.|
|connectionSecurityRulesFromGroupPolicyNotMerged|Booleano|Configura el servidor de seguridad para evitar que la combinación de las reglas de seguridad de directiva de grupo con las del almacén local en lugar de omitir la local almacenan las reglas. Cuando ConnectionSecurityRulesFromGroupPolicyNotMerged y ConnectionSecurityRulesFromGroupPolicyMerged son true, ConnectionSecurityRulesFromGroupPolicyMerged tiene prioridad.|
|outboundConnectionsRequired|Booleano|Configura el firewall para permitir que todas las conexiones salientes de forma predeterminada. Cuando OutboundConnectionsRequired y OutboundConnectionsBlocked son true, OutboundConnectionsBlocked tiene prioridad.|
|outboundConnectionsBlocked|Booleano|Configura el servidor de seguridad para bloquear todas las conexiones salientes de forma predeterminada. Cuando OutboundConnectionsRequired y OutboundConnectionsBlocked son true, OutboundConnectionsBlocked tiene prioridad.|
|inboundConnectionsRequired|Booleano|Configura el firewall para permitir que todas las conexiones entrantes de forma predeterminada. Cuando InboundConnectionsRequired y InboundConnectionsBlocked son true, InboundConnectionsBlocked tiene prioridad.|
|inboundConnectionsBlocked|Booleano|Configura el servidor de seguridad para bloquear todas las conexiones entrantes de forma predeterminada. Cuando InboundConnectionsRequired y InboundConnectionsBlocked son true, InboundConnectionsBlocked tiene prioridad.|
|securedPacketExemptionAllowed|Booleano|Configura el firewall para permitir que el equipo host responder al tráfico de red no solicitado de que el tráfico está protegido por IPSec incluso cuando stealthModeBlocked se establece en true. Cuando SecuredPacketExemptionBlocked y SecuredPacketExemptionAllowed son true, SecuredPacketExemptionAllowed tiene prioridad.|
|securedPacketExemptionBlocked|Booleano|Configura el servidor de seguridad para bloquear el equipo host para responder al tráfico de red no solicitado de que el tráfico está protegido por IPSec incluso cuando stealthModeBlocked se establece en true. Cuando SecuredPacketExemptionBlocked y SecuredPacketExemptionAllowed son true, SecuredPacketExemptionAllowed tiene prioridad.|
|policyRulesFromGroupPolicyMerged|Booleano|Configura el firewall para combinar las directivas de la regla de Firewall de directiva de grupo con las del almacén local en lugar de omitir las reglas del almacén local. Cuando PolicyRulesFromGroupPolicyNotMerged y PolicyRulesFromGroupPolicyMerged son true, PolicyRulesFromGroupPolicyMerged tiene prioridad.|
|policyRulesFromGroupPolicyNotMerged|Booleano|Configura el servidor de seguridad para evitar que la combinación de regla de Firewall directivas de directiva de grupo con las del almacén local en lugar de omitir la local almacenan las reglas. Cuando PolicyRulesFromGroupPolicyNotMerged y PolicyRulesFromGroupPolicyMerged son true, PolicyRulesFromGroupPolicyMerged tiene prioridad.|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsFirewallNetworkProfile",
  "firewallEnabled": "String",
  "stealthModeRequired": true,
  "stealthModeBlocked": true,
  "incomingTrafficRequired": true,
  "incomingTrafficBlocked": true,
  "unicastResponsesToMulticastBroadcastsRequired": true,
  "unicastResponsesToMulticastBroadcastsBlocked": true,
  "inboundNotificationsRequired": true,
  "inboundNotificationsBlocked": true,
  "authorizedApplicationRulesFromGroupPolicyMerged": true,
  "authorizedApplicationRulesFromGroupPolicyNotMerged": true,
  "globalPortRulesFromGroupPolicyMerged": true,
  "globalPortRulesFromGroupPolicyNotMerged": true,
  "connectionSecurityRulesFromGroupPolicyMerged": true,
  "connectionSecurityRulesFromGroupPolicyNotMerged": true,
  "outboundConnectionsRequired": true,
  "outboundConnectionsBlocked": true,
  "inboundConnectionsRequired": true,
  "inboundConnectionsBlocked": true,
  "securedPacketExemptionAllowed": true,
  "securedPacketExemptionBlocked": true,
  "policyRulesFromGroupPolicyMerged": true,
  "policyRulesFromGroupPolicyNotMerged": true
}
```





