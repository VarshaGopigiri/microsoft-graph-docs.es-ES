---
title: Obtener windows10VpnConfiguration
description: Leer las propiedades y las relaciones del objeto windows10VpnConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: e74239e1608149f6ad9f33225ca714670a4953af
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27930932"
---
# <a name="get-windows10vpnconfiguration"></a><span data-ttu-id="205ea-103">Obtener windows10VpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="205ea-103">Get windows10VpnConfiguration</span></span>

> <span data-ttu-id="205ea-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="205ea-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="205ea-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="205ea-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="205ea-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="205ea-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="205ea-107">Leer las propiedades y las relaciones del objeto [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="205ea-107">Read properties and relationships of the [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="205ea-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="205ea-108">Prerequisites</span></span>
<span data-ttu-id="205ea-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="205ea-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="205ea-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="205ea-111">Permission type</span></span>|<span data-ttu-id="205ea-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="205ea-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="205ea-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="205ea-113">Delegated (work or school account)</span></span>|<span data-ttu-id="205ea-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="205ea-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="205ea-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="205ea-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="205ea-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="205ea-116">Not supported.</span></span>|
|<span data-ttu-id="205ea-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="205ea-117">Application</span></span>|<span data-ttu-id="205ea-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="205ea-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="205ea-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="205ea-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="205ea-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="205ea-120">Optional query parameters</span></span>
<span data-ttu-id="205ea-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="205ea-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="205ea-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="205ea-122">Request headers</span></span>
|<span data-ttu-id="205ea-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="205ea-123">Header</span></span>|<span data-ttu-id="205ea-124">Valor</span><span class="sxs-lookup"><span data-stu-id="205ea-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="205ea-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="205ea-125">Authorization</span></span>|<span data-ttu-id="205ea-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="205ea-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="205ea-127">Accept</span><span class="sxs-lookup"><span data-stu-id="205ea-127">Accept</span></span>|<span data-ttu-id="205ea-128">application/json</span><span class="sxs-lookup"><span data-stu-id="205ea-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="205ea-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="205ea-129">Request body</span></span>
<span data-ttu-id="205ea-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="205ea-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="205ea-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="205ea-131">Response</span></span>
<span data-ttu-id="205ea-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="205ea-132">If successful, this method returns a `200 OK` response code and [windows10VpnConfiguration](../resources/intune-deviceconfig-windows10vpnconfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="205ea-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="205ea-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="205ea-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="205ea-134">Request</span></span>
<span data-ttu-id="205ea-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="205ea-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="205ea-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="205ea-136">Response</span></span>
<span data-ttu-id="205ea-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="205ea-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 3676

{
  "value": {
    "@odata.type": "#microsoft.graph.windows10VpnConfiguration",
    "id": "c23c9727-9727-c23c-2797-3cc227973cc2",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "supportsScopeTags": true,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "connectionName": "Connection Name value",
    "servers": [
      {
        "@odata.type": "microsoft.graph.vpnServer",
        "description": "Description value",
        "address": "Address value",
        "isDefaultServer": true
      }
    ],
    "customXml": "Y3VzdG9tWG1s",
    "profileTarget": "device",
    "connectionType": "f5EdgeClient",
    "enableSplitTunneling": true,
    "enableAlwaysOn": true,
    "enableDeviceTunnel": true,
    "enableDnsRegistration": true,
    "dnsSuffixes": [
      "Dns Suffixes value"
    ],
    "authenticationMethod": "usernameAndPassword",
    "rememberUserCredentials": true,
    "enableConditionalAccess": true,
    "enableSingleSignOnWithAlternateCertificate": true,
    "singleSignOnEku": {
      "@odata.type": "microsoft.graph.extendedKeyUsage",
      "name": "Name value",
      "objectIdentifier": "Object Identifier value"
    },
    "singleSignOnIssuerHash": "Single Sign On Issuer Hash value",
    "eapXml": "ZWFwWG1s",
    "proxyServer": {
      "@odata.type": "microsoft.graph.windows10VpnProxyServer",
      "automaticConfigurationScriptUrl": "https://example.com/automaticConfigurationScriptUrl/",
      "address": "Address value",
      "port": 4,
      "bypassProxyServerForLocalAddress": true
    },
    "associatedApps": [
      {
        "@odata.type": "microsoft.graph.windows10AssociatedApps",
        "appType": "universal",
        "identifier": "Identifier value"
      }
    ],
    "onlyAssociatedAppsCanUseConnection": true,
    "windowsInformationProtectionDomain": "Windows Information Protection Domain value",
    "trafficRules": [
      {
        "@odata.type": "microsoft.graph.vpnTrafficRule",
        "name": "Name value",
        "protocols": 9,
        "localPortRanges": [
          {
            "@odata.type": "microsoft.graph.numberRange",
            "lowerNumber": 11,
            "upperNumber": 11
          }
        ],
        "remotePortRanges": [
          {
            "@odata.type": "microsoft.graph.numberRange",
            "lowerNumber": 11,
            "upperNumber": 11
          }
        ],
        "localAddressRanges": [
          {
            "@odata.type": "microsoft.graph.iPv4Range",
            "lowerAddress": "Lower Address value",
            "upperAddress": "Upper Address value"
          }
        ],
        "remoteAddressRanges": [
          {
            "@odata.type": "microsoft.graph.iPv4Range",
            "lowerAddress": "Lower Address value",
            "upperAddress": "Upper Address value"
          }
        ],
        "appId": "App Id value",
        "appType": "desktop",
        "routingPolicyType": "splitTunnel",
        "claims": "Claims value"
      }
    ],
    "routes": [
      {
        "@odata.type": "microsoft.graph.vpnRoute",
        "destinationPrefix": "Destination Prefix value",
        "prefixSize": 10
      }
    ],
    "dnsRules": [
      {
        "@odata.type": "microsoft.graph.vpnDnsRule",
        "name": "Name value",
        "servers": [
          "Servers value"
        ],
        "proxyServerUri": "Proxy Server Uri value"
      }
    ]
  }
}
```





