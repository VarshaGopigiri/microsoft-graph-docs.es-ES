---
title: Enumerar deviceConfigurationDeviceStatuses
description: Enumere las propiedades y las relaciones de los objetos deviceConfigurationDeviceStatus.
author: tfitzmac
ms.openlocfilehash: 2ec7116917891e29798a71b2cb36a75a7468fe1b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27336571"
---
# <a name="list-deviceconfigurationdevicestatuses"></a><span data-ttu-id="cb0bf-103">Enumerar deviceConfigurationDeviceStatuses</span><span class="sxs-lookup"><span data-stu-id="cb0bf-103">List deviceConfigurationDeviceStatuses</span></span>

> <span data-ttu-id="cb0bf-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="cb0bf-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="cb0bf-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="cb0bf-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="cb0bf-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="cb0bf-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="cb0bf-107">Enumere las propiedades y las relaciones de los objetos [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="cb0bf-107">List properties and relationships of the [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="cb0bf-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="cb0bf-108">Prerequisites</span></span>
<span data-ttu-id="cb0bf-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="cb0bf-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="cb0bf-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="cb0bf-111">Permission type</span></span>|<span data-ttu-id="cb0bf-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="cb0bf-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="cb0bf-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="cb0bf-113">Delegated (work or school account)</span></span>|<span data-ttu-id="cb0bf-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="cb0bf-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="cb0bf-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="cb0bf-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="cb0bf-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cb0bf-116">Not supported.</span></span>|
|<span data-ttu-id="cb0bf-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="cb0bf-117">Application</span></span>|<span data-ttu-id="cb0bf-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="cb0bf-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="cb0bf-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="cb0bf-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/deviceStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/deviceStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/deviceStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/deviceStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/deviceStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/deviceStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/deviceStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="cb0bf-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="cb0bf-120">Request headers</span></span>
|<span data-ttu-id="cb0bf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cb0bf-121">Header</span></span>|<span data-ttu-id="cb0bf-122">Valor</span><span class="sxs-lookup"><span data-stu-id="cb0bf-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="cb0bf-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="cb0bf-123">Authorization</span></span>|<span data-ttu-id="cb0bf-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="cb0bf-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="cb0bf-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="cb0bf-125">Accept</span></span>|<span data-ttu-id="cb0bf-126">application/json</span><span class="sxs-lookup"><span data-stu-id="cb0bf-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="cb0bf-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="cb0bf-127">Request body</span></span>
<span data-ttu-id="cb0bf-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="cb0bf-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="cb0bf-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb0bf-129">Response</span></span>
<span data-ttu-id="cb0bf-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="cb0bf-130">If successful, this method returns a `200 OK` response code and a collection of [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="cb0bf-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="cb0bf-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="cb0bf-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="cb0bf-132">Request</span></span>
<span data-ttu-id="cb0bf-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="cb0bf-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses
```

### <a name="response"></a><span data-ttu-id="cb0bf-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="cb0bf-134">Response</span></span>
<span data-ttu-id="cb0bf-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="cb0bf-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 569

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStatus",
      "id": "674e98e5-98e5-674e-e598-4e67e5984e67",
      "deviceDisplayName": "Device Display Name value",
      "userName": "User Name value",
      "deviceModel": "Device Model value",
      "platform": 8,
      "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
      "status": "notApplicable",
      "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
      "userPrincipalName": "User Principal Name value"
    }
  ]
}
```





