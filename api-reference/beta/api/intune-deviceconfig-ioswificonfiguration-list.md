---
title: Lista iosWiFiConfigurations
description: Propiedades de la lista y relaciones de los objetos iosWiFiConfiguration.
author: tfitzmac
ms.openlocfilehash: aa6468059f62985179a3cac408a634fa6f993e4e
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27338356"
---
# <a name="list-ioswificonfigurations"></a><span data-ttu-id="2e931-103">Lista iosWiFiConfigurations</span><span class="sxs-lookup"><span data-stu-id="2e931-103">List iosWiFiConfigurations</span></span>

> <span data-ttu-id="2e931-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2e931-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2e931-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2e931-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2e931-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2e931-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2e931-107">Propiedades de la lista y relaciones de los objetos [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md) .</span><span class="sxs-lookup"><span data-stu-id="2e931-107">List properties and relationships of the [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2e931-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2e931-108">Prerequisites</span></span>
<span data-ttu-id="2e931-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2e931-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2e931-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2e931-111">Permission type</span></span>|<span data-ttu-id="2e931-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2e931-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2e931-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2e931-113">Delegated (work or school account)</span></span>|<span data-ttu-id="2e931-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="2e931-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="2e931-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2e931-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2e931-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e931-116">Not supported.</span></span>|
|<span data-ttu-id="2e931-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2e931-117">Application</span></span>|<span data-ttu-id="2e931-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2e931-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2e931-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2e931-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsDomainJoinConfiguration/networkAccessConfigurations
```

## <a name="request-headers"></a><span data-ttu-id="2e931-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2e931-120">Request headers</span></span>
|<span data-ttu-id="2e931-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2e931-121">Header</span></span>|<span data-ttu-id="2e931-122">Valor</span><span class="sxs-lookup"><span data-stu-id="2e931-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2e931-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="2e931-123">Authorization</span></span>|<span data-ttu-id="2e931-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2e931-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2e931-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2e931-125">Accept</span></span>|<span data-ttu-id="2e931-126">application/json</span><span class="sxs-lookup"><span data-stu-id="2e931-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2e931-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2e931-127">Request body</span></span>
<span data-ttu-id="2e931-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="2e931-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="2e931-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e931-129">Response</span></span>
<span data-ttu-id="2e931-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2e931-130">If successful, this method returns a `200 OK` response code and a collection of [iosWiFiConfiguration](../resources/intune-deviceconfig-ioswificonfiguration.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2e931-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2e931-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="2e931-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2e931-132">Request</span></span>
<span data-ttu-id="2e931-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2e931-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations
```

### <a name="response"></a><span data-ttu-id="2e931-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2e931-134">Response</span></span>
<span data-ttu-id="2e931-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2e931-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 964

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosWiFiConfiguration",
      "id": "516f9ef9-9ef9-516f-f99e-6f51f99e6f51",
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
      "wiFiSecurityType": "wpaPersonal",
      "proxySettings": "manual",
      "proxyManualAddress": "Proxy Manual Address value",
      "proxyManualPort": 15,
      "proxyAutomaticConfigurationUrl": "https://example.com/proxyAutomaticConfigurationUrl/",
      "preSharedKey": "Pre Shared Key value"
    }
  ]
}
```





