---
title: Obtener androidForWorkEnterpriseWiFiConfiguration
description: Leer las propiedades y las relaciones del objeto androidForWorkEnterpriseWiFiConfiguration.
author: tfitzmac
ms.openlocfilehash: 68862f02843a50e3673d0fbbb3d293664c1c3d7d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27319897"
---
# <a name="get-androidforworkenterprisewificonfiguration"></a><span data-ttu-id="0f929-103">Obtener androidForWorkEnterpriseWiFiConfiguration</span><span class="sxs-lookup"><span data-stu-id="0f929-103">Get androidForWorkEnterpriseWiFiConfiguration</span></span>

> <span data-ttu-id="0f929-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0f929-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0f929-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0f929-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0f929-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0f929-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0f929-107">Leer las propiedades y las relaciones del objeto [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="0f929-107">Read properties and relationships of the [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0f929-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0f929-108">Prerequisites</span></span>
<span data-ttu-id="0f929-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0f929-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0f929-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0f929-111">Permission type</span></span>|<span data-ttu-id="0f929-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0f929-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0f929-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0f929-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0f929-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="0f929-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="0f929-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0f929-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0f929-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0f929-116">Not supported.</span></span>|
|<span data-ttu-id="0f929-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0f929-117">Application</span></span>|<span data-ttu-id="0f929-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0f929-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0f929-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0f929-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="0f929-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="0f929-120">Optional query parameters</span></span>
<span data-ttu-id="0f929-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0f929-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="0f929-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0f929-122">Request headers</span></span>
|<span data-ttu-id="0f929-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0f929-123">Header</span></span>|<span data-ttu-id="0f929-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0f929-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0f929-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="0f929-125">Authorization</span></span>|<span data-ttu-id="0f929-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0f929-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0f929-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0f929-127">Accept</span></span>|<span data-ttu-id="0f929-128">application/json</span><span class="sxs-lookup"><span data-stu-id="0f929-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0f929-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0f929-129">Request body</span></span>
<span data-ttu-id="0f929-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="0f929-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="0f929-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f929-131">Response</span></span>
<span data-ttu-id="0f929-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0f929-132">If successful, this method returns a `200 OK` response code and [androidForWorkEnterpriseWiFiConfiguration](../resources/intune-deviceconfig-androidforworkenterprisewificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0f929-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0f929-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="0f929-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0f929-134">Request</span></span>
<span data-ttu-id="0f929-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0f929-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="0f929-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0f929-136">Response</span></span>
<span data-ttu-id="0f929-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0f929-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1005

{
  "value": {
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
}
```





