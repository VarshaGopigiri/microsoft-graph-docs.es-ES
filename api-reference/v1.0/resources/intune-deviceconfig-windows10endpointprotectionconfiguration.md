---
title: Tipo de recurso windows10EndpointProtectionConfiguration
description: Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso Windows10EndpointProtectionConfiguration.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: c84b20918db07e2000abdd0dcbd26ba0d2ad3e6b
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940242"
---
# <a name="windows10endpointprotectionconfiguration-resource-type"></a>Tipo de recurso windows10EndpointProtectionConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Este tema proporciona descripciones de los métodos declarados, las propiedades y las relaciones expuestas por el recurso Windows10EndpointProtectionConfiguration.

Hereda de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)

## <a name="methods"></a>Métodos
|Método|Tipo de valor devuelto|Descripción|
|:---|:---|:---|
|[Enumerar windows10EndpointProtectionConfigurations](../api/intune-deviceconfig-windows10endpointprotectionconfiguration-list.md)|Colección [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md)|Enumere las propiedades y las relaciones de los objetos [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).|
|[Obtener windows10EndpointProtectionConfiguration](../api/intune-deviceconfig-windows10endpointprotectionconfiguration-get.md)|[windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md)|Lea las propiedades y las relaciones del objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).|
|[Crear windows10EndpointProtectionConfiguration](../api/intune-deviceconfig-windows10endpointprotectionconfiguration-create.md)|[windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md)|Cree un objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).|
|[Eliminar windows10EndpointProtectionConfiguration](../api/intune-deviceconfig-windows10endpointprotectionconfiguration-delete.md)|Ninguno|Elimina un [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).|
|[Actualizar windows10EndpointProtectionConfiguration](../api/intune-deviceconfig-windows10endpointprotectionconfiguration-update.md)|[windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md)|Actualice las propiedades de un objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).|

## <a name="properties"></a>Propiedades
|Propiedad|Tipo|Descripción|
|:---|:---|:---|
|id|Cadena|Clave de la entidad. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|lastModifiedDateTime|DateTimeOffset|Fecha y hora en la que se modificó el objeto por última vez. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|createdDateTime|DateTimeOffset|Fecha y hora en la que se creó el objeto. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|descripción|Cadena|Descripción proporcionada por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|displayName|Cadena|Nombre proporcionado por el administrador de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|version|Int32|Versión de la configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|firewallBlockStatefulFTP|Booleano|Bloquea las conexiones FTP con estado en el dispositivo.|
|firewallIdleTimeoutForSecurityAssociationInSeconds|Int32|Configura el tiempo de espera inactivo para asociaciones de seguridad, en segundos, de 300 a 3600 inclusive. Se trata del período tras el cual expiran y se eliminan las asociaciones de seguridad. Valores válidos de 300 a 3600.|
|firewallPreSharedKeyEncodingMethod|[firewallPreSharedKeyEncodingMethodType](../resources/intune-deviceconfig-firewallpresharedkeyencodingmethodtype.md)|Seleccione la clave previamente compartida de codificación que se utilizará. Los valores posibles son: `deviceDefault`, `none` y `utF8`.|
|firewallIPSecExemptionsAllowNeighborDiscovery|Booleano|Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de vecinos.|
|firewallIPSecExemptionsAllowICMP|Booleano|Configura las exenciones IPSec para permitir ICMP.|
|firewallIPSecExemptionsAllowRouterDiscovery|Booleano|Configura las exenciones IPSec para permitir los códigos de tipo ICMP de IPv6 de detección de enrutadores.|
|firewallIPSecExemptionsAllowDHCP|Booleano|Configura las exenciones IPSec para permitir el tráfico DHCP de IPv4 e IPv6.|
|firewallCertificateRevocationListCheckMethod|[firewallCertificateRevocationListCheckMethodType](../resources/intune-deviceconfig-firewallcertificaterevocationlistcheckmethodtype.md)|Especificar cómo se aplica la lista de revocación de certificados. Los valores posibles son: `deviceDefault`, `none`, `attempt` y `require`.|
|firewallMergeKeyingModuleSettings|Booleano|Si un conjunto de autenticación no es totalmente compatible con un módulo de generación de claves, dirija el módulo para que solo ignore los conjuntos de autenticación no admitidos, en lugar de todo el conjunto.|
|firewallPacketQueueingMethod|[firewallPacketQueueingMethodType](../resources/intune-deviceconfig-firewallpacketqueueingmethodtype.md)|Configura cómo debe aplicarse queueing de paquetes en el escenario de puerta de enlace de túnel. Los valores posibles son: `deviceDefault`, `disabled`, `queueInbound`, `queueOutbound` y `queueBoth`.|
|firewallProfileDomain|[windowsFirewallNetworkProfile](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|Configura las opciones del perfil de firewall para redes de dominio.|
|firewallProfilePublic|[windowsFirewallNetworkProfile](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|Configura las opciones del perfil de firewall para redes públicas.|
|firewallProfilePrivate|[windowsFirewallNetworkProfile](../resources/intune-deviceconfig-windowsfirewallnetworkprofile.md)|Configura las opciones del perfil de firewall para redes privadas.|
|defenderAttackSurfaceReductionExcludedPaths|Colección String|Lista de archivos exe y carpetas que se deben excluir de las reglas de reducción de la superficie expuesta a ataques.|
|defenderGuardedFoldersAllowedAppPaths|Colección String|Lista de rutas de acceso a exe que pueden obtener acceso a carpetas protegidas.|
|defenderAdditionalGuardedFolders|Colección String|Lista de las rutas de acceso de carpeta que se van a agregar a la lista de carpetas protegidas.|
|defenderExploitProtectionXml|Binario|Contenido XML que contiene información sobre detalles de protección contra vulnerabilidades de seguridad.|
|defenderExploitProtectionXmlFileName|Cadena|Nombre del archivo del que se obtuvo DefenderExploitProtectionXml.|
|defenderSecurityCenterBlockExploitProtectionOverride|Booleano|Indica si se va a impedir que el usuario invalide la configuración de protección contra vulnerabilidades.|
|appLockerApplicationControl|[appLockerApplicationControlType](../resources/intune-deviceconfig-applockerapplicationcontroltype.md)|Permite que el administrador elija los tipos de aplicación que se permiten en los dispositivos. Los valores posibles son: `notConfigured`, `enforceComponentsAndStoreApps`, `auditComponentsAndStoreApps`, `enforceComponentsStoreAppsAndSmartlocker` y `auditComponentsStoreAppsAndSmartlocker`.|
|smartScreenEnableInShell|Booleano|Permite que los administradores de TI configuren SmartScreen para Windows.|
|smartScreenBlockOverrideForFiles|Booleano|Permite que los administradores de TI controlen si los usuarios pueden omitir advertencias de SmartScreen y ejecutar archivos malintencionados.|
|applicationGuardEnabled|Booleano|Habilita la Protección de aplicaciones de Windows Defender.|
|applicationGuardBlockFileTransfer|[applicationGuardBlockFileTransferType](../resources/intune-deviceconfig-applicationguardblockfiletransfertype.md)|Portapapeles de bloqueo para el archivo de transferencia de imagen, archivo de texto o ninguno de ellos. Los valores posibles son: `notConfigured`, `blockImageAndTextFile`, `blockImageFile`, `blockNone` y `blockTextFile`.|
|applicationGuardBlockNonEnterpriseContent|Booleano|Impide que los sitios de la empresa carguen contenido no empresarial, como complementos de terceros.|
|applicationGuardAllowPersistence|Booleano|Permite el almacenamiento de los datos generados por el usuario en el contenedor de la protección de aplicaciones (favoritos, cookies, contraseñas web, etc.).|
|applicationGuardForceAuditing|Booleano|La auditoría forzada conservará los registros y eventos de Windows para cumplir con los criterios de seguridad y cumplimiento (algunos eventos de ejemplo son el inicio y cierre de sesión del usuario, el uso de derechos de privilegio, la instalación de software, los cambios del sistema, etc.).|
|applicationGuardBlockClipboardSharing|[applicationGuardBlockClipboardSharingType](../resources/intune-deviceconfig-applicationguardblockclipboardsharingtype.md)|Impide que el Portapapeles comparta los datos del host al contenedor, del contenedor al host, en ambas direcciones o en ninguna. Los valores posibles son: `notConfigured`, `blockBoth`, `blockHostToContainer`, `blockContainerToHost` y `blockNone`.|
|applicationGuardAllowPrintToPDF|Booleano|Permite la impresión en PDF desde el contenedor.|
|applicationGuardAllowPrintToXPS|Booleano|Permite la impresión en XPS desde el contenedor.|
|applicationGuardAllowPrintToLocalPrinters|Booleano|Permite la impresión en impresoras locales desde el contenedor.|
|applicationGuardAllowPrintToNetworkPrinters|Booleano|Permite la impresión en impresoras en red desde el contenedor.|
|bitLockerDisableWarningForOtherDiskEncryption|Booleano|Permite que el administrador deshabilite el mensaje de advertencia para otro cifrado de disco en los equipos de usuario.|
|bitLockerEnableStorageCardEncryptionOnMobile|Booleano|Permite que el administrador exija que se active el cifrado con BitLocker. Esta directiva solo es válida para una SKU móvil.|
|bitLockerEncryptDevice|Booleano|Permite que el administrador exija que se active el cifrado con BitLocker.|
|bitLockerRemovableDrivePolicy|[bitLockerRemovableDrivePolicy](../resources/intune-deviceconfig-bitlockerremovabledrivepolicy.md)|Directiva de unidad extraíble de BitLocker.|

## <a name="relationships"></a>Relaciones
|Relación|Tipo|Descripción|
|:---|:---|:---|
|asignaciones|Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|La lista de tareas para el perfil de configuración del dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatuses|Colección [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)|Estado de instalación de configuración del dispositivo por dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|userStatuses|Colección [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)|Estado de instalación de configuración de dispositivo por usuario. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceStatusOverview|[deviceConfigurationDeviceOverview](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|Información general sobre el estado de dispositivos de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|userStatusOverview|[deviceConfigurationUserOverview](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|Información general sobre el estado de usuarios de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|
|deviceSettingStateSummaries|Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)|Resumen de dispositivo sobre el estado de configuración de la configuración de dispositivo. Heredado de [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)|

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



