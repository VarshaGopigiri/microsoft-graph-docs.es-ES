---
title: Obtener windowsWifiConfiguration
description: Leer las propiedades y las relaciones del objeto windowsWifiConfiguration.
author: tfitzmac
ms.openlocfilehash: 89a20033e38231dc6ed45918ce58a837ef1cebb9
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27349521"
---
# <a name="get-windowswificonfiguration"></a><span data-ttu-id="928b7-103">Obtener windowsWifiConfiguration</span><span class="sxs-lookup"><span data-stu-id="928b7-103">Get windowsWifiConfiguration</span></span>

> <span data-ttu-id="928b7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="928b7-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="928b7-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="928b7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="928b7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="928b7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="928b7-107">Leer las propiedades y las relaciones del objeto [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="928b7-107">Read properties and relationships of the [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="928b7-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="928b7-108">Prerequisites</span></span>
<span data-ttu-id="928b7-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="928b7-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="928b7-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="928b7-111">Permission type</span></span>|<span data-ttu-id="928b7-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="928b7-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="928b7-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="928b7-113">Delegated (work or school account)</span></span>|<span data-ttu-id="928b7-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="928b7-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="928b7-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="928b7-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="928b7-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="928b7-116">Not supported.</span></span>|
|<span data-ttu-id="928b7-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="928b7-117">Application</span></span>|<span data-ttu-id="928b7-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="928b7-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="928b7-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="928b7-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments/{deviceConfigurationGroupAssignmentId}/deviceConfiguration
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations/{deviceConfigurationId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="928b7-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="928b7-120">Optional query parameters</span></span>
<span data-ttu-id="928b7-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="928b7-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="928b7-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="928b7-122">Request headers</span></span>
|<span data-ttu-id="928b7-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="928b7-123">Header</span></span>|<span data-ttu-id="928b7-124">Valor</span><span class="sxs-lookup"><span data-stu-id="928b7-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="928b7-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="928b7-125">Authorization</span></span>|<span data-ttu-id="928b7-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="928b7-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="928b7-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="928b7-127">Accept</span></span>|<span data-ttu-id="928b7-128">application/json</span><span class="sxs-lookup"><span data-stu-id="928b7-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="928b7-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="928b7-129">Request body</span></span>
<span data-ttu-id="928b7-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="928b7-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="928b7-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="928b7-131">Response</span></span>
<span data-ttu-id="928b7-132">Si tiene éxito, este método devuelve una `200 OK` objeto de código y [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) de respuesta en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="928b7-132">If successful, this method returns a `200 OK` response code and [windowsWifiConfiguration](../resources/intune-deviceconfig-windowswificonfiguration.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="928b7-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="928b7-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="928b7-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="928b7-134">Request</span></span>
<span data-ttu-id="928b7-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="928b7-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}
```

### <a name="response"></a><span data-ttu-id="928b7-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="928b7-136">Response</span></span>
<span data-ttu-id="928b7-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="928b7-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 1025

{
  "value": {
    "@odata.type": "#microsoft.graph.windowsWifiConfiguration",
    "id": "8a9e790f-790f-8a9e-0f79-9e8a0f799e8a",
    "lastModifiedDateTime": "2017-01-01T00:00:35.1329464-08:00",
    "roleScopeTagIds": [
      "Role Scope Tag Ids value"
    ],
    "supportsScopeTags": true,
    "createdDateTime": "2017-01-01T00:02:43.5775965-08:00",
    "description": "Description value",
    "displayName": "Display Name value",
    "version": 7,
    "preSharedKey": "Pre Shared Key value",
    "wifiSecurityType": "wpaPersonal",
    "meteredConnectionLimit": "fixed",
    "ssid": "Ssid value",
    "networkName": "Network Name value",
    "connectAutomatically": true,
    "connectToPreferredNetwork": true,
    "connectWhenNetworkNameIsHidden": true,
    "proxySetting": "manual",
    "proxyManualAddress": "Proxy Manual Address value",
    "proxyManualPort": 15,
    "proxyAutomaticConfigurationUrl": "https://example.com/proxyAutomaticConfigurationUrl/",
    "forceFIPSCompliance": true
  }
}
```





