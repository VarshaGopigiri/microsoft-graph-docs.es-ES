---
title: Lista iosVpnConfigurations
description: Propiedades de la lista y relaciones de los objetos iosVpnConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a13501285ccaaf3322da917eefc0e7face70eda2
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27812988"
---
# <a name="list-iosvpnconfigurations"></a><span data-ttu-id="b3b58-103">Lista iosVpnConfigurations</span><span class="sxs-lookup"><span data-stu-id="b3b58-103">List iosVpnConfigurations</span></span>

> <span data-ttu-id="b3b58-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b3b58-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b3b58-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b3b58-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b3b58-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b3b58-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b3b58-107">Propiedades de la lista y relaciones de los objetos [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="b3b58-107">List properties and relationships of the [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b3b58-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b3b58-108">Prerequisites</span></span>
<span data-ttu-id="b3b58-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b3b58-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b3b58-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b3b58-111">Permission type</span></span>|<span data-ttu-id="b3b58-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b3b58-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b3b58-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b3b58-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b3b58-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="b3b58-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="b3b58-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b3b58-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b3b58-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3b58-116">Not supported.</span></span>|
|<span data-ttu-id="b3b58-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b3b58-117">Application</span></span>|<span data-ttu-id="b3b58-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b3b58-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b3b58-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b3b58-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="b3b58-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b3b58-120">Request headers</span></span>
|<span data-ttu-id="b3b58-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b3b58-121">Header</span></span>|<span data-ttu-id="b3b58-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b3b58-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b3b58-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b3b58-123">Authorization</span></span>|<span data-ttu-id="b3b58-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b3b58-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b3b58-125">Accept</span><span class="sxs-lookup"><span data-stu-id="b3b58-125">Accept</span></span>|<span data-ttu-id="b3b58-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b3b58-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b3b58-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b3b58-127">Request body</span></span>
<span data-ttu-id="b3b58-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="b3b58-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="b3b58-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3b58-129">Response</span></span>
<span data-ttu-id="b3b58-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b3b58-130">If successful, this method returns a `200 OK` response code and a collection of [iosVpnConfiguration](../resources/intune-deviceconfig-iosvpnconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b3b58-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b3b58-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="b3b58-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b3b58-132">Request</span></span>
<span data-ttu-id="b3b58-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b3b58-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="b3b58-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b3b58-134">Response</span></span>
<span data-ttu-id="b3b58-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b3b58-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2547

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosVpnConfiguration",
      "id": "bd12424c-424c-bd12-4c42-12bd4c4212bd",
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
      "connectionType": "pulseSecure",
      "loginGroupOrDomain": "Login Group Or Domain value",
      "role": "Role value",
      "realm": "Realm value",
      "server": {
        "@odata.type": "microsoft.graph.vpnServer",
        "description": "Description value",
        "address": "Address value",
        "isDefaultServer": true
      },
      "identifier": "Identifier value",
      "customData": [
        {
          "@odata.type": "microsoft.graph.keyValue",
          "key": "Key value",
          "value": "Value value"
        }
      ],
      "customKeyValueData": [
        {
          "@odata.type": "microsoft.graph.keyValuePair",
          "name": "Name value",
          "value": "Value value"
        }
      ],
      "enableSplitTunneling": true,
      "authenticationMethod": "usernameAndPassword",
      "enablePerApp": true,
      "safariDomains": [
        "Safari Domains value"
      ],
      "onDemandRules": [
        {
          "@odata.type": "microsoft.graph.vpnOnDemandRule",
          "ssids": [
            "Ssids value"
          ],
          "dnsSearchDomains": [
            "Dns Search Domains value"
          ],
          "probeUrl": "https://example.com/probeUrl/",
          "action": "evaluateConnection",
          "domainAction": "neverConnect",
          "domains": [
            "Domains value"
          ],
          "probeRequiredUrl": "https://example.com/probeRequiredUrl/"
        }
      ],
      "proxyServer": {
        "@odata.type": "microsoft.graph.vpnProxyServer",
        "automaticConfigurationScriptUrl": "https://example.com/automaticConfigurationScriptUrl/",
        "address": "Address value",
        "port": 4
      },
      "optInToDeviceIdSharing": true,
      "providerType": "appProxy",
      "userDomain": "User Domain value",
      "strictEnforcement": true,
      "cloudName": "Cloud Name value",
      "excludeList": [
        "Exclude List value"
      ]
    }
  ]
}
```





