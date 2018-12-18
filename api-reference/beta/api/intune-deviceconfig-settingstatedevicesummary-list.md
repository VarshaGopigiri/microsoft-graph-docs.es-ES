---
title: Incluir en una lista settingStateDeviceSummaries
description: Enumere las propiedades y las relaciones de los objetos settingStateDeviceSummary.
author: tfitzmac
ms.openlocfilehash: 5a18bb843e11eaf8d87ba9b6977cbd4f47e9d23b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27308333"
---
# <a name="list-settingstatedevicesummaries"></a><span data-ttu-id="ec0ca-103">Incluir en una lista settingStateDeviceSummaries</span><span class="sxs-lookup"><span data-stu-id="ec0ca-103">List settingStateDeviceSummaries</span></span>

> <span data-ttu-id="ec0ca-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ec0ca-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ec0ca-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ec0ca-107">Enumere las propiedades y las relaciones de los objetos [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="ec0ca-107">List properties and relationships of the [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ec0ca-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ec0ca-108">Prerequisites</span></span>
<span data-ttu-id="ec0ca-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ec0ca-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ec0ca-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ec0ca-111">Permission type</span></span>|<span data-ttu-id="ec0ca-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ec0ca-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ec0ca-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ec0ca-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ec0ca-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="ec0ca-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="ec0ca-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ec0ca-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ec0ca-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-116">Not supported.</span></span>|
|<span data-ttu-id="ec0ca-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ec0ca-117">Application</span></span>|<span data-ttu-id="ec0ca-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ec0ca-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ec0ca-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceSettingStateSummaries
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/deviceSettingStateSummaries
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/deviceSettingStateSummaries
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/deviceSettingStateSummaries
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/deviceSettingStateSummaries
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/deviceSettingStateSummaries
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/deviceSettingStateSummaries
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/deviceSettingStateSummaries
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/deviceSettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="ec0ca-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ec0ca-120">Request headers</span></span>
|<span data-ttu-id="ec0ca-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ec0ca-121">Header</span></span>|<span data-ttu-id="ec0ca-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ec0ca-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ec0ca-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ec0ca-123">Authorization</span></span>|<span data-ttu-id="ec0ca-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ec0ca-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="ec0ca-125">Accept</span></span>|<span data-ttu-id="ec0ca-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ec0ca-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ec0ca-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ec0ca-127">Request body</span></span>
<span data-ttu-id="ec0ca-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="ec0ca-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec0ca-129">Response</span></span>
<span data-ttu-id="ec0ca-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-130">If successful, this method returns a `200 OK` response code and a collection of [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ec0ca-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ec0ca-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="ec0ca-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ec0ca-132">Request</span></span>
<span data-ttu-id="ec0ca-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries
```

### <a name="response"></a><span data-ttu-id="ec0ca-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ec0ca-134">Response</span></span>
<span data-ttu-id="ec0ca-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ec0ca-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 486

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.settingStateDeviceSummary",
      "id": "3e2d4526-4526-3e2d-2645-2d3e26452d3e",
      "settingName": "Setting Name value",
      "instancePath": "Instance Path value",
      "unknownDeviceCount": 2,
      "notApplicableDeviceCount": 8,
      "compliantDeviceCount": 4,
      "remediatedDeviceCount": 5,
      "nonCompliantDeviceCount": 7,
      "errorDeviceCount": 0,
      "conflictDeviceCount": 3
    }
  ]
}
```





