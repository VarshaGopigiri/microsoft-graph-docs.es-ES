---
title: Lista macOSVpnConfigurations
description: Propiedades de la lista y relaciones de los objetos macOSVpnConfiguration.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8d091ffce914fb257f21ae4afde18803a5ea0b6e
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27858250"
---
# <a name="list-macosvpnconfigurations"></a><span data-ttu-id="47c65-103">Lista macOSVpnConfigurations</span><span class="sxs-lookup"><span data-stu-id="47c65-103">List macOSVpnConfigurations</span></span>

> <span data-ttu-id="47c65-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="47c65-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="47c65-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="47c65-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="47c65-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="47c65-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="47c65-107">Propiedades de la lista y relaciones de los objetos [macOSVpnConfiguration](../resources/intune-deviceconfig-macosvpnconfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="47c65-107">List properties and relationships of the [macOSVpnConfiguration](../resources/intune-deviceconfig-macosvpnconfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="47c65-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="47c65-108">Prerequisites</span></span>
<span data-ttu-id="47c65-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="47c65-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="47c65-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="47c65-111">Permission type</span></span>|<span data-ttu-id="47c65-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="47c65-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="47c65-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="47c65-113">Delegated (work or school account)</span></span>|<span data-ttu-id="47c65-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="47c65-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="47c65-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="47c65-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="47c65-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47c65-116">Not supported.</span></span>|
|<span data-ttu-id="47c65-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="47c65-117">Application</span></span>|<span data-ttu-id="47c65-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="47c65-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="47c65-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="47c65-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="47c65-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="47c65-120">Request headers</span></span>
|<span data-ttu-id="47c65-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="47c65-121">Header</span></span>|<span data-ttu-id="47c65-122">Valor</span><span class="sxs-lookup"><span data-stu-id="47c65-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="47c65-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="47c65-123">Authorization</span></span>|<span data-ttu-id="47c65-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="47c65-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="47c65-125">Accept</span><span class="sxs-lookup"><span data-stu-id="47c65-125">Accept</span></span>|<span data-ttu-id="47c65-126">application/json</span><span class="sxs-lookup"><span data-stu-id="47c65-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="47c65-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="47c65-127">Request body</span></span>
<span data-ttu-id="47c65-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="47c65-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="47c65-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47c65-129">Response</span></span>
<span data-ttu-id="47c65-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [macOSVpnConfiguration](../resources/intune-deviceconfig-macosvpnconfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="47c65-130">If successful, this method returns a `200 OK` response code and a collection of [macOSVpnConfiguration](../resources/intune-deviceconfig-macosvpnconfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="47c65-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="47c65-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="47c65-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="47c65-132">Request</span></span>
<span data-ttu-id="47c65-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="47c65-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="47c65-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="47c65-134">Response</span></span>
<span data-ttu-id="47c65-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="47c65-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 2334

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.macOSVpnConfiguration",
      "id": "8ce00178-0178-8ce0-7801-e08c7801e08c",
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
      "optInToDeviceIdSharing": true
    }
  ]
}
```





