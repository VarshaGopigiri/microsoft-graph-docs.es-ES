# <a name="windowsfirewallnetworkprofile-resource-type"></a>Tipo de recurso windowsFirewallNetworkProfile

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Directivas de perfiles de firewall de Windows.
## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|firewallEnabled|[stateManagementSetting](../resources/intune_deviceconfig_statemanagementsetting.md)|Activa el firewall y el cumplimiento de seguridad avanzada. Los valores posibles son: `notConfigured`, `blocked` y `allowed`.|
|stealthModeBlocked|Booleano|Evita que el servidor funcione en modo silencioso|
|incomingTrafficBlocked|Booleano|Configura el firewall para bloquear todo el tráfico entrante independientemente de otras opciones de configuración de directiva|
|unicastResponsesToMulticastBroadcastsBlocked|Booleano|Configura el firewall para bloquear las respuestas de unidifusión al tráfico de multidifusión.|
|inboundNotificationsBlocked|Booleano|Impide que el firewall muestre notificaciones cuando se impide que una aplicación escuche en un puerto|
|authorizedApplicationRulesFromGroupPolicyMerged|Booleano|Configura el firewall para combinar reglas de aplicaciones autorizadas de directiva de grupo con las de almacén local en lugar de omitir las reglas del almacén local|
|globalPortRulesFromGroupPolicyMerged|Booleano|Configura el firewall para combinar reglas de puerto global de directiva de grupo con las de almacén local en lugar de omitir las reglas del almacén local|
|connectionSecurityRulesFromGroupPolicyMerged|Booleano|Configura el firewall para combinar reglas de seguridad de la conexión de directiva de grupo con las de almacén local en lugar de omitir las reglas del almacén local|
|outboundConnectionsBlocked|Booleano|Configura el firewall para que bloquee todas las conexiones salientes de forma predeterminada|
|inboundConnectionsBlocked|Booleano|Configura el firewall para que bloquee todas las conexiones entrantes de forma predeterminada|
|securedPacketExemptionAllowed|Booleano|Configura el firewall para permitir que el equipo host responda al tráfico de red no solicitado si ese tráfico se protege con IPSec, incluso cuando stealthModeBlocked se establece en true|
|policyRulesFromGroupPolicyMerged|Booleano|Configura el firewall para combinar directivas de regla de firewall de directiva de grupo con las de almacén local en lugar de omitir las reglas del almacén local|

## <a name="relationships"></a>Relaciones
Ninguna
## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!--{
  "blockType": "resource",
  "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile"
}-->
``` json
{
  "@odata.type": "#microsoft.graph.windowsFirewallNetworkProfile",
  "firewallEnabled": "String",
  "stealthModeBlocked": true,
  "incomingTrafficBlocked": true,
  "unicastResponsesToMulticastBroadcastsBlocked": true,
  "inboundNotificationsBlocked": true,
  "authorizedApplicationRulesFromGroupPolicyMerged": true,
  "globalPortRulesFromGroupPolicyMerged": true,
  "connectionSecurityRulesFromGroupPolicyMerged": true,
  "outboundConnectionsBlocked": true,
  "inboundConnectionsBlocked": true,
  "securedPacketExemptionAllowed": true,
  "policyRulesFromGroupPolicyMerged": true
}
```



