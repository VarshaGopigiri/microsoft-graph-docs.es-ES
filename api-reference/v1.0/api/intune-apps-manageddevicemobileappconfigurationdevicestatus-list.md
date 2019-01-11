---
title: Lista managedDeviceMobileAppConfigurationDeviceStatuses
description: Propiedades de la lista y relaciones de los objetos managedDeviceMobileAppConfigurationDeviceStatus.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 810be50eb9532b0de226cb5b8264b464fc9c420b
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27873216"
---
# <a name="list-manageddevicemobileappconfigurationdevicestatuses"></a><span data-ttu-id="00155-103">Lista managedDeviceMobileAppConfigurationDeviceStatuses</span><span class="sxs-lookup"><span data-stu-id="00155-103">List managedDeviceMobileAppConfigurationDeviceStatuses</span></span>

> <span data-ttu-id="00155-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="00155-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="00155-105">Propiedades de la lista y relaciones de los objetos [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="00155-105">List properties and relationships of the [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="00155-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="00155-106">Prerequisites</span></span>
<span data-ttu-id="00155-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="00155-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="00155-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="00155-109">Permission type</span></span>|<span data-ttu-id="00155-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="00155-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="00155-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="00155-111">Delegated (work or school account)</span></span>|<span data-ttu-id="00155-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="00155-112">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="00155-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="00155-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="00155-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="00155-114">Not supported.</span></span>|
|<span data-ttu-id="00155-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="00155-115">Application</span></span>|<span data-ttu-id="00155-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="00155-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="00155-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="00155-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="00155-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="00155-118">Request headers</span></span>
|<span data-ttu-id="00155-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00155-119">Header</span></span>|<span data-ttu-id="00155-120">Valor</span><span class="sxs-lookup"><span data-stu-id="00155-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="00155-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="00155-121">Authorization</span></span>|<span data-ttu-id="00155-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="00155-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="00155-123">Accept</span><span class="sxs-lookup"><span data-stu-id="00155-123">Accept</span></span>|<span data-ttu-id="00155-124">application/json</span><span class="sxs-lookup"><span data-stu-id="00155-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="00155-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="00155-125">Request body</span></span>
<span data-ttu-id="00155-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="00155-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="00155-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00155-127">Response</span></span>
<span data-ttu-id="00155-128">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="00155-128">If successful, this method returns a `200 OK` response code and a collection of [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="00155-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="00155-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="00155-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="00155-130">Request</span></span>
<span data-ttu-id="00155-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="00155-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses
```

### <a name="response"></a><span data-ttu-id="00155-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="00155-132">Response</span></span>
<span data-ttu-id="00155-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="00155-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 563

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceStatus",
      "id": "477d3651-3651-477d-5136-7d4751367d47",
      "deviceDisplayName": "Device Display Name value",
      "userName": "User Name value",
      "deviceModel": "Device Model value",
      "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
      "status": "notApplicable",
      "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
      "userPrincipalName": "User Principal Name value"
    }
  ]
}
```



