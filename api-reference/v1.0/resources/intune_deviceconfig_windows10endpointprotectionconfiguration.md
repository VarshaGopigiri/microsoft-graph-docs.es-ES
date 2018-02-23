# <a name="windows10endpointprotectionconfiguration-resource-type"></a>Tipo de recurso windows10EndpointProtectionConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso Windows10EndpointProtectionConfiguration.

Hereda de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windows10EndpointProtectionConfigurations](../api/intune_deviceconfig_windows10endpointprotectionconfiguration_list.md)|Colección [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md).|
|[Obtener windows10EndpointProtectionConfiguration](../api/intune_deviceconfig_windows10endpointprotectionconfiguration_get.md)|[windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md)|Lea las propiedades y las relaciones del objeto [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md).|
|[Crear windows10EndpointProtectionConfiguration](../api/intune_deviceconfig_windows10endpointprotectionconfiguration_create.md)|[windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md)|Cree un objeto [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md).|
|[Eliminar windows10EndpointProtectionConfiguration](../api/intune_deviceconfig_windows10endpointprotectionconfiguration_delete.md)|Ninguno|Elimina un [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md).|
|[Actualizar windows10EndpointProtectionConfiguration](../api/intune_deviceconfig_windows10endpointprotectionconfiguration_update.md)|[windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md)|Actualice las propiedades de un objeto [windows10EndpointProtectionConfiguration](../resources/intune_deviceconfig_windows10endpointprotectionconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|description|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|versión|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|firewallBlockStatefulFTP|Booleano|Bloquea las conexiones FTP con estado en el dispositivo|
|firewallIdleTimeoutForSecurityAssociationInSeconds|Int32|Configura el tiempo de espera inactivo para asociaciones de seguridad, en segundos, de 300 a 3600 inclusive. Este es el período tras el cual expiran y se eliminan las asociaciones de seguridad. Valores válidos de 300 a 3600|
|firewallPreSharedKeyEncodingMethod|Cadena|Seleccione qué codificación de clave previamente compartida se debe usar. Los valores posibles son: `deviceDefault`, `none` y `utF8`.|
|firewallIPSecExemptionsAllowNeighborDiscovery|Booleano|Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de descubrimiento cercano|
|firewallIPSecExemptionsAllowICMP|Booleano|Configura las exenciones IPSec para permitir ICMP|
|firewallIPSecExemptionsAllowRouterDiscovery|Booleano|Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de descubrimiento de enrutamiento|
|firewallIPSecExemptionsAllowDHCP|Booleano|Configura las exenciones IPSec para permitir el tráfico DHCP de IPv4 e IPv6|
|firewallCertificateRevocationListCheckMethod|Cadena|Especifique cómo se exige la lista de revocación de certificados. Los valores posibles son: `deviceDefault`, `none`, `attempt` y `require`.|
|firewallMergeKeyingModuleSettings|Booleano|Si un conjunto de autenticación no es totalmente compatible con un módulo de generación de claves, dirija el módulo para que ignore solo los conjuntos de autenticación no admitidos, en lugar de todo el conjunto|
|firewallPacketQueueingMethod|Cadena|Configura cómo debe aplicarse la cola de paquetes en el escenario de puerta de enlace de túnel. Los valores posibles son: `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound` y `queueBoth`.|
|firewallProfileDomain|[windowsFirewallNetworkProfile](../resources/intune_deviceconfig_windowsfirewallnetworkprofile.md)|Configura las opciones del perfil de firewall para redes de dominio|
|firewallProfilePublic|[windowsFirewallNetworkProfile](../resources/intune_deviceconfig_windowsfirewallnetworkprofile.md)|Configura las opciones del perfil de firewall para redes públicas|
|firewallProfilePrivate|[windowsFirewallNetworkProfile](../resources/intune_deviceconfig_windowsfirewallnetworkprofile.md)|Configura las opciones del perfil de firewall para redes privadas|
|defenderAttackSurfaceReductionExcludedPaths|Colección de cadenas|Lista de archivos exe y carpetas que se deben excluir de las reglas de reducción de la superficie expuesta a ataques|
|defenderGuardedFoldersAllowedAppPaths|Colección de cadenas|Lista de rutas de acceso a exe que pueden obtener acceso a carpetas protegidas|
|defenderAdditionalGuardedFolders|Colección de cadenas|Lista de las rutas de acceso de carpeta para agregar a la lista de carpetas protegidas|
|defenderExploitProtectionXml|Binario|Contenido XML que contiene información sobre detalles de protección contra vulnerabilidades.|
|defenderExploitProtectionXmlFileName|Cadena|Nombre del archivo del que se obtuvo DefenderExploitProtectionXml.|
|defenderSecurityCenterBlockExploitProtectionOverride|Booleano|Indica si se va a impedir que el usuario invalide la configuración de la protección contra vulnerabilidades.|
|appLockerApplicationControl|Cadena|Permite que el administrador elija qué tipos de aplicación permitir en los dispositivos. Los valores posibles son: `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker` y `auditComponentsStoreAppsAndSmartlocker`.|
|smartScreenEnableInShell|Booleano|Permite a los administradores de TI configurar SmartScreen para Windows.|
|smartScreenBlockOverrideForFiles|Booleano|Permite a los administradores de TI controlar si los usuarios pueden omitir advertencias de SmartScreen y ejecutar archivos malintencionados.|
|applicationGuardEnabled|Booleano|Habilita la Protección de aplicaciones de Windows Defender|
|applicationGuardBlockFileTransfer|Cadena|Impedir que el Portapapeles transfiera archivos de imagen, de texto o ambos. Los valores posibles son: `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone` y `blockTextFile`.|
|applicationGuardBlockNonEnterpriseContent|Booleano|Impide que los sitios de la empresa carguen contenido no empresarial, como complementos de terceros|
|applicationGuardAllowPersistence|Booleano|Permite los datos generados por el usuario en el contenedor de la protección de aplicaciones (favoritos, cookies, contraseñas web, etc.)|
|applicationGuardForceAuditing|Booleano|La auditoría forzada persistirá a los registros y eventos de Windows para cumplir con los criterios de seguridad y cumplimiento (algunos eventos de ejemplo son el inicio y cierre de sesión del usuario, el uso de derechos de privilegio, la instalación de software, los cambios del sistema, etc.)|
|applicationGuardBlockClipboardSharing|Cadena|Impedir que el Portapapeles comparta los datos del host al contenedor, del contenedor al host, ambas o ninguna de ellas. Los valores posibles son: `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost` y `blockNone`.|
|applicationGuardAllowPrintToPDF|Booleano|Permite la impresión en PDF desde el contenedor|
|applicationGuardAllowPrintToXPS|Booleano|Permite la impresión en XPS desde el contenedor|
|applicationGuardAllowPrintToLocalPrinters|Booleano|Permite la impresión en impresoras locales desde el contenedor|
|applicationGuardAllowPrintToNetworkPrinters|Booleano|Permite la impresión en impresoras en red desde el contenedor|
|bitLockerDisableWarningForOtherDiskEncryption|Booleano|Permite que el administrador deshabilite el mensaje de advertencia para otro cifrado de disco en los equipos de usuario.|
|bitLockerEnableStorageCardEncryptionOnMobile|Booleano|Permite que el administrador solicite que se active el cifrado con BitLocker. Esta directiva solo es válida para una SKU móvil.|
|bitLockerEncryptDevice|Booleano|Permite que el administrador solicite que se active el cifrado con BitLocker.|
|bitLockerRemovableDrivePolicy|[bitLockerRemovableDrivePolicy](../resources/intune_deviceconfig_bitlockerremovabledrivepolicy.md)|Directiva de unidad extraíble de BitLocker.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [deviceConfigurationAssignment](../resources/intune_deviceconfig_deviceconfigurationassignment.md)|La lista de tareas para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceStatuses|Colección [deviceConfigurationDeviceStatus](../resources/intune_deviceconfig_deviceconfigurationdevicestatus.md)|Estado de instalación de configuración del dispositivo por dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|userStatuses|Colección [deviceConfigurationUserStatus](../resources/intune_deviceconfig_deviceconfigurationuserstatus.md)|Estado de instalación de configuración del dispositivo por usuario. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune_deviceconfig_deviceconfigurationdeviceoverview.md)|Información general sobre el estado de dispositivos de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune_deviceconfig_deviceconfigurationuseroverview.md)|Información general sobre el estado de usuarios de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune_deviceconfig_settingstatedevicesummary.md)|Resumen de dispositivo sobre el estado de configuración de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune_deviceconfig_deviceconfiguration.md)|

## <a name="json-representation"></a>Representación JSON
Aquí tiene una representación JSON del recurso.
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.windows10EndpointProtectionConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.windows10EndpointProtectionConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024,
  "firewallBlockStatefulFTP": true,
  "firewallIdleTimeoutForSecurityAssociationInSeconds": 1024,
  "firewallPreSharedKeyEncodingMethod": "String",
  "firewallIPSecExemptionsAllowNeighborDiscovery": true,
  "firewallIPSecExemptionsAllowICMP": true,
  "firewallIPSecExemptionsAllowRouterDiscovery": true,
  "firewallIPSecExemptionsAllowDHCP": true,
  "firewallCertificateRevocationListCheckMethod": "String",
  "firewallMergeKeyingModuleSettings": true,
  "firewallPacketQueueingMethod": "String",
  "firewallProfileDomain": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
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
  },
  "firewallProfilePublic": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
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
  },
  "firewallProfilePrivate": {
    "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
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
  },
  "defenderAttackSurfaceReductionExcludedPaths": [
    "String"
  ],
  "defenderGuardedFoldersAllowedAppPaths": [
    "String"
  ],
  "defenderAdditionalGuardedFolders": [
    "String"
  ],
  "defenderExploitProtectionXml": "binary",
  "defenderExploitProtectionXmlFileName": "String",
  "defenderSecurityCenterBlockExploitProtectionOverride": true,
  "appLockerApplicationControl": "String",
  "smartScreenEnableInShell": true,
  "smartScreenBlockOverrideForFiles": true,
  "applicationGuardEnabled": true,
  "applicationGuardBlockFileTransfer": "String",
  "applicationGuardBlockNonEnterpriseContent": true,
  "applicationGuardAllowPersistence": true,
  "applicationGuardForceAuditing": true,
  "applicationGuardBlockClipboardSharing": "String",
  "applicationGuardAllowPrintToPDF": true,
  "applicationGuardAllowPrintToXPS": true,
  "applicationGuardAllowPrintToLocalPrinters": true,
  "applicationGuardAllowPrintToNetworkPrinters": true,
  "bitLockerDisableWarningForOtherDiskEncryption": true,
  "bitLockerEnableStorageCardEncryptionOnMobile": true,
  "bitLockerEncryptDevice": true,
  "bitLockerRemovableDrivePolicy": {
    "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy",
    "encryptionMethod": "String",
    "requireEncryptionForWriteAccess": true,
    "blockCrossOrganizationWriteAccess": true
  }
}
```



