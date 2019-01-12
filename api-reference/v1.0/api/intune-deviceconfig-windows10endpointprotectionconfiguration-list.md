---
title: Enumerar windows10EndpointProtectionConfigurations
description: Enumere las propiedades y las relaciones de los objetos windows10EndpointProtectionConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a05d3949cd1df31db1a18dd0393f0897a663d5ea
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27961732"
---
# <a name="list-windows10endpointprotectionconfigurations"></a><span data-ttu-id="f7d19-103">Enumerar windows10EndpointProtectionConfigurations</span><span class="sxs-lookup"><span data-stu-id="f7d19-103">List windows10EndpointProtectionConfigurations</span></span>

> <span data-ttu-id="f7d19-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f7d19-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f7d19-105">Enumere las propiedades y las relaciones de los objetos [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="f7d19-105">List properties and relationships of the [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f7d19-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f7d19-106">Prerequisites</span></span>
<span data-ttu-id="f7d19-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f7d19-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f7d19-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f7d19-109">Permission type</span></span>|<span data-ttu-id="f7d19-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f7d19-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f7d19-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f7d19-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f7d19-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="f7d19-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="f7d19-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f7d19-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f7d19-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7d19-114">Not supported.</span></span>|
|<span data-ttu-id="f7d19-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f7d19-115">Application</span></span>|<span data-ttu-id="f7d19-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f7d19-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f7d19-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f7d19-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="f7d19-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f7d19-118">Request headers</span></span>
|<span data-ttu-id="f7d19-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7d19-119">Header</span></span>|<span data-ttu-id="f7d19-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f7d19-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f7d19-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="f7d19-121">Authorization</span></span>|<span data-ttu-id="f7d19-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f7d19-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f7d19-123">Accept</span><span class="sxs-lookup"><span data-stu-id="f7d19-123">Accept</span></span>|<span data-ttu-id="f7d19-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f7d19-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f7d19-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f7d19-125">Request body</span></span>
<span data-ttu-id="f7d19-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f7d19-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f7d19-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7d19-127">Response</span></span>
<span data-ttu-id="f7d19-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f7d19-128">If successful, this method returns a `200 OK` response code and a collection of [windows10EndpointProtectionConfiguration](../resources/intune-deviceconfig-windows10endpointprotectionconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f7d19-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7d19-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="f7d19-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f7d19-130">Request</span></span>
<span data-ttu-id="f7d19-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f7d19-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="f7d19-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f7d19-132">Response</span></span>
<span data-ttu-id="f7d19-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f7d19-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 4834

{
  "value": [
    {
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
  ]
}
```



