---
title: Obtener deviceConfigurationDeviceStatus
description: Lea las propiedades y las relaciones del objeto deviceConfigurationDeviceStatus.
author: tfitzmac
ms.openlocfilehash: aec946d5d0daf05989aaf970019563708df10bf6
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27357662"
---
# <a name="get-deviceconfigurationdevicestatus"></a><span data-ttu-id="9a041-103">Obtener deviceConfigurationDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="9a041-103">Get deviceConfigurationDeviceStatus</span></span>

> <span data-ttu-id="9a041-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9a041-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9a041-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9a041-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9a041-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9a041-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9a041-107">Lea las propiedades y las relaciones del objeto [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="9a041-107">Read properties and relationships of the [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9a041-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9a041-108">Prerequisites</span></span>
<span data-ttu-id="9a041-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9a041-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9a041-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9a041-111">Permission type</span></span>|<span data-ttu-id="9a041-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9a041-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9a041-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9a041-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9a041-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="9a041-114">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="9a041-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9a041-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9a041-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9a041-116">Not supported.</span></span>|
|<span data-ttu-id="9a041-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9a041-117">Application</span></span>|<span data-ttu-id="9a041-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9a041-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9a041-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9a041-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses/{deviceConfigurationDeviceStatusId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/deviceStatuses/{deviceConfigurationDeviceStatusId}
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/deviceStatuses/{deviceConfigurationDeviceStatusId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="9a041-120">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="9a041-120">Optional query parameters</span></span>
<span data-ttu-id="9a041-121">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a041-121">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="9a041-122">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9a041-122">Request headers</span></span>
|<span data-ttu-id="9a041-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9a041-123">Header</span></span>|<span data-ttu-id="9a041-124">Valor</span><span class="sxs-lookup"><span data-stu-id="9a041-124">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9a041-125">Autorización</span><span class="sxs-lookup"><span data-stu-id="9a041-125">Authorization</span></span>|<span data-ttu-id="9a041-126">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9a041-126">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9a041-127">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9a041-127">Accept</span></span>|<span data-ttu-id="9a041-128">application/json</span><span class="sxs-lookup"><span data-stu-id="9a041-128">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9a041-129">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9a041-129">Request body</span></span>
<span data-ttu-id="9a041-130">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="9a041-130">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="9a041-131">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a041-131">Response</span></span>
<span data-ttu-id="9a041-132">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9a041-132">If successful, this method returns a `200 OK` response code and [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9a041-133">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9a041-133">Example</span></span>
### <a name="request"></a><span data-ttu-id="9a041-134">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9a041-134">Request</span></span>
<span data-ttu-id="9a041-135">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9a041-135">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses/{deviceConfigurationDeviceStatusId}
```

### <a name="response"></a><span data-ttu-id="9a041-136">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9a041-136">Response</span></span>
<span data-ttu-id="9a041-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9a041-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 535

{
  "value": {
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
}
```





