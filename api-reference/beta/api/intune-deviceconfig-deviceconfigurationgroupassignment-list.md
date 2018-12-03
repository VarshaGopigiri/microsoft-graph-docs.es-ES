---
title: Lista deviceConfigurationGroupAssignments
description: Propiedades de la lista y relaciones de los objetos deviceConfigurationGroupAssignment.
ms.openlocfilehash: b43c78d0b8ad99aaaaa86aeb713d45a425c91aee
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085832"
---
# <a name="list-deviceconfigurationgroupassignments"></a><span data-ttu-id="c7a53-103">Lista deviceConfigurationGroupAssignments</span><span class="sxs-lookup"><span data-stu-id="c7a53-103">List deviceConfigurationGroupAssignments</span></span>

> <span data-ttu-id="c7a53-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c7a53-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c7a53-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c7a53-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c7a53-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c7a53-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c7a53-107">Propiedades de la lista y relaciones de los objetos [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="c7a53-107">List properties and relationships of the [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="c7a53-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="c7a53-108">Prerequisites</span></span>
<span data-ttu-id="c7a53-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="c7a53-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="c7a53-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="c7a53-111">Permission type</span></span>|<span data-ttu-id="c7a53-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="c7a53-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="c7a53-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="c7a53-113">Delegated (work or school account)</span></span>|<span data-ttu-id="c7a53-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="c7a53-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="c7a53-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="c7a53-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="c7a53-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7a53-116">Not supported.</span></span>|
|<span data-ttu-id="c7a53-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="c7a53-117">Application</span></span>|<span data-ttu-id="c7a53-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="c7a53-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="c7a53-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="c7a53-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/groupAssignments
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/groupAssignments
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/groupAssignments
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/groupAssignments
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/groupAssignments
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/groupAssignments
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/groupAssignments
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/groupAssignments
```

## <a name="request-headers"></a><span data-ttu-id="c7a53-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="c7a53-120">Request headers</span></span>
|<span data-ttu-id="c7a53-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7a53-121">Header</span></span>|<span data-ttu-id="c7a53-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c7a53-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="c7a53-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="c7a53-123">Authorization</span></span>|<span data-ttu-id="c7a53-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="c7a53-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="c7a53-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="c7a53-125">Accept</span></span>|<span data-ttu-id="c7a53-126">application/json</span><span class="sxs-lookup"><span data-stu-id="c7a53-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="c7a53-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="c7a53-127">Request body</span></span>
<span data-ttu-id="c7a53-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="c7a53-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="c7a53-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7a53-129">Response</span></span>
<span data-ttu-id="c7a53-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="c7a53-130">If successful, this method returns a `200 OK` response code and a collection of [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="c7a53-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="c7a53-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="c7a53-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="c7a53-132">Request</span></span>
<span data-ttu-id="c7a53-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="c7a53-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/groupAssignments
```

### <a name="response"></a><span data-ttu-id="c7a53-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="c7a53-134">Response</span></span>
<span data-ttu-id="c7a53-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="c7a53-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 244

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceConfigurationGroupAssignment",
      "id": "561d26c5-26c5-561d-c526-1d56c5261d56",
      "targetGroupId": "Target Group Id value",
      "excludeGroup": true
    }
  ]
}
```




