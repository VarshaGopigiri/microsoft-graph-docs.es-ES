---
title: Obtener windows10EndpointProtectionConfiguration
description: Lea las propiedades y las relaciones del objeto windows10EndpointProtectionConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 17af14b4f47324356a669ad11bd76228ada01616
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27932044"
---
# <a name="get-windows10endpointprotectionconfiguration"></a>Obtener windows10EndpointProtectionConfiguration

> **Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.

Lea las propiedades y las relaciones del objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).
## <a name="prerequisites"></a>Requisitos previos
Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).

|Tipo de permiso|Permisos (de más a menos privilegiados)|
|:---|:---|
|Delegado (cuenta profesional o educativa)|DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All|
|Delegado (cuenta personal de Microsoft)|No admitida.|
|Aplicación|No admitida.|

## <a name="http-request"></a>Solicitud HTTP
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a>Parámetros de consulta opcionales
Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.
## <a name="request-headers"></a>Encabezados de solicitud
|Encabezado|Valor|
|:---|:---|
|Autorización|Se requiere &lt;token&gt; de portador.|
|Accept|application/json|

## <a name="request-body"></a>Cuerpo de la solicitud
No proporcione un cuerpo de solicitud para este método.

## <a name="response"></a>Respuesta
Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) en el cuerpo de la respuesta.

## <a name="example"></a>Ejemplo
### <a name="request"></a>Solicitud
Aquí tiene un ejemplo de la solicitud.
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a>Respuesta
Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4628

{
  "value": {
    "@odata.type": "#microsoft.graph.windows10EndpointProtectionConfiguration",
    "id": "09709403-9403-0970-0394-700903947009",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "firewallBlockStatefulFTP": true,
    "firewallIdleTimeoutForSecurityAssociationInSeconds": 2,
    "firewallPreSharedKeyEncodingMethod": "none",
    "firewallIPSecExemptionsAllowNeighborDiscovery": true,
    "firewallIPSecExemptionsAllowICMP": true,
    "firewallIPSecExemptionsAllowRouterDiscovery": true,
    "firewallIPSecExemptionsAllowDHCP": true,
    "firewallCertificateRevocationListCheckMethod": "none",
    "firewallMergeKeyingModuleSettings": true,
    "firewallPacketQueueingMethod": "disabled",
    "firewallProfileDomain": {
      "@odata.type": "microsoft.graph.windowsFirewallNetworkProfile",
      "firewallEnabled": "blocked",
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
      "firewallEnabled": "blocked",
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
      "firewallEnabled": "blocked",
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
      "Defender Attack Surface Reduction Excluded Paths value"
    ],
    "defenderGuardedFoldersAllowedAppPaths": [
      "Defender Guarded Folders Allowed App Paths value"
    ],
    "defenderAdditionalGuardedFolders": [
      "Defender Additional Guarded Folders value"
    ],
    "defenderExploitProtectionXml": "ZGVmZW5kZXJFeHBsb2l0UHJvdGVjdGlvblhtbA==",
    "defenderExploitProtectionXmlFileName": "Defender Exploit Protection Xml File Name value",
    "defenderSecurityCenterBlockExploitProtectionOverride": true,
    "appLockerApplicationControl": "enforceComponentsAndStoreApps",
    "smartScreenEnableInShell": true,
    "smartScreenBlockOverrideForFiles": true,
    "applicationGuardEnabled": true,
    "applicationGuardBlockFileTransfer": "blockImageAndTextFile",
    "applicationGuardBlockNonEnterpriseContent": true,
    "applicationGuardAllowPersistence": true,
    "applicationGuardForceAuditing": true,
    "applicationGuardBlockClipboardSharing": "blockBoth",
    "applicationGuardAllowPrintToPDF": true,
    "applicationGuardAllowPrintToXPS": true,
    "applicationGuardAllowPrintToLocalPrinters": true,
    "applicationGuardAllowPrintToNetworkPrinters": true,
    "bitLockerDisableWarningForOtherDiskEncryption": true,
    "bitLockerEnableStorageCardEncryptionOnMobile": true,
    "bitLockerEncryptDevice": true,
    "bitLockerRemovableDrivePolicy": {
      "@odata.type": "microsoft.graph.bitLockerRemovableDrivePolicy",
      "encryptionMethod": "aesCbc256",
      "requireEncryptionForWriteAccess": true,
      "blockCrossOrganizationWriteAccess": true
    }
  }
}
```



