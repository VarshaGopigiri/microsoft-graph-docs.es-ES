---
title: Lista androidForWorkEnterpriseWiFiConfigurations
description: Propiedades de la lista y relaciones de los objetos androidForWorkEnterpriseWiFiConfiguration.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: ff650d12d1f9b87936be52365bb75fcd846e1322
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27974388"
---
# <a name="list-androidforworkenterprisewificonfigurations"></a><span data-ttu-id="cff43-103">Lista androidForWorkEnterpriseWiFiConfigurations</span><span class="sxs-lookup"><span data-stu-id="cff43-103">List androidForWorkEnterpriseWiFiConfigurations</span></span>

> <span data-ttu-id="cff43-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cff43-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cff43-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cff43-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cff43-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cff43-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cff43-107">Propiedades de la lista y relaciones de los objetos [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="cff43-107">List properties and relationships of the [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cff43-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cff43-108">Prerequisites</span></span>
<span data-ttu-id="cff43-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cff43-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cff43-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cff43-111">Permission type</span></span>|<span data-ttu-id="cff43-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cff43-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cff43-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cff43-113">Delegated (work or school account)</span></span>|<span data-ttu-id="cff43-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="cff43-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="cff43-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cff43-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cff43-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cff43-116">Not supported.</span></span>|
|<span data-ttu-id="cff43-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cff43-117">Application</span></span>|<span data-ttu-id="cff43-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cff43-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cff43-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cff43-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="cff43-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cff43-120">Request headers</span></span>
|<span data-ttu-id="cff43-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cff43-121">Header</span></span>|<span data-ttu-id="cff43-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cff43-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cff43-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="cff43-123">Authorization</span></span>|<span data-ttu-id="cff43-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cff43-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cff43-125">Accept</span><span class="sxs-lookup"><span data-stu-id="cff43-125">Accept</span></span>|<span data-ttu-id="cff43-126">application/json</span><span class="sxs-lookup"><span data-stu-id="cff43-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cff43-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cff43-127">Request body</span></span>
<span data-ttu-id="cff43-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cff43-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cff43-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cff43-129">Response</span></span>
<span data-ttu-id="cff43-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cff43-130">If successful, this method returns a `200 OK` response code and a collection of [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cff43-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cff43-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="cff43-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cff43-132">Request</span></span>
<span data-ttu-id="cff43-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cff43-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="cff43-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cff43-134">Response</span></span>
<span data-ttu-id="cff43-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cff43-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1061

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.androidForWorkEnterpriseWiFiConfiguration",
      "id": "742d953a-953a-742d-3a95-2d743a952d74",
      "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
      "roleScopeTagIds": [
        "Role Scope Tag Ids value"
      ],
      "supportsScopeTags": true,
      "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
      "description": "Description value",
      "displayName": "Display Name value",
      "version": 7,
      "networkName": "Network Name value",
      "ssid": "Ssid value",
      "connectAutomatically": true,
      "connectWhenNetworkNameIsHidden": true,
      "wiFiSecurityType": "wpaEnterprise",
      "eapType": "eapTtls",
      "authenticationMethod": "usernameAndPassword",
      "innerAuthenticationProtocolForEapTtls": "challengeHandshakeAuthenticationProtocol",
      "innerAuthenticationProtocolForPeap": "microsoftChapVersionTwo",
      "outerIdentityPrivacyTemporaryValue": "Outer Identity Privacy Temporary Value value"
    }
  ]
}
```





