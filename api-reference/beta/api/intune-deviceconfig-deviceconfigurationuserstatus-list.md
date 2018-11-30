---
title: Enumerar deviceConfigurationUserStatuses
description: Enumere las propiedades y las relaciones de los objetos deviceConfigurationUserStatus.
ms.openlocfilehash: eb3f3d7cf2ceec95ad998af6315fbf9c49d0accd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086846"
---
# <a name="list-deviceconfigurationuserstatuses"></a><span data-ttu-id="f2875-103">Enumerar deviceConfigurationUserStatuses</span><span class="sxs-lookup"><span data-stu-id="f2875-103">List deviceConfigurationUserStatuses</span></span>

> <span data-ttu-id="f2875-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f2875-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f2875-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f2875-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f2875-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f2875-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f2875-107">Enumere las propiedades y las relaciones de los objetos [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md).</span><span class="sxs-lookup"><span data-stu-id="f2875-107">List properties and relationships of the [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f2875-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f2875-108">Prerequisites</span></span>
<span data-ttu-id="f2875-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f2875-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f2875-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f2875-111">Permission type</span></span>|<span data-ttu-id="f2875-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f2875-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f2875-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f2875-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f2875-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="f2875-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="f2875-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f2875-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f2875-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f2875-116">Not supported.</span></span>|
|<span data-ttu-id="f2875-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f2875-117">Application</span></span>|<span data-ttu-id="f2875-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f2875-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f2875-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f2875-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/userStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/userStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/userStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/userStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/userStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/userStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/userStatuses
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/userStatuses
```

## <a name="request-headers"></a><span data-ttu-id="f2875-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f2875-120">Request headers</span></span>
|<span data-ttu-id="f2875-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f2875-121">Header</span></span>|<span data-ttu-id="f2875-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f2875-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f2875-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f2875-123">Authorization</span></span>|<span data-ttu-id="f2875-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f2875-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f2875-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f2875-125">Accept</span></span>|<span data-ttu-id="f2875-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f2875-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f2875-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f2875-127">Request body</span></span>
<span data-ttu-id="f2875-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f2875-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f2875-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2875-129">Response</span></span>
<span data-ttu-id="f2875-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f2875-130">If successful, this method returns a `200 OK` response code and a collection of [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f2875-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f2875-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f2875-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f2875-132">Request</span></span>
<span data-ttu-id="f2875-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f2875-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/userStatuses
```

### <a name="response"></a><span data-ttu-id="f2875-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f2875-134">Response</span></span>
<span data-ttu-id="f2875-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f2875-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 400

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceConfigurationUserStatus",
      "id": "7e323db2-3db2-7e32-b23d-327eb23d327e",
      "userDisplayName": "User Display Name value",
      "devicesCount": 12,
      "status": "notApplicable",
      "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
      "userPrincipalName": "User Principal Name value"
    }
  ]
}
```





