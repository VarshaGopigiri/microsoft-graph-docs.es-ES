---
title: Lista managedDeviceMobileAppConfigurationDeviceStatuses
description: Propiedades de la lista y relaciones de los objetos managedDeviceMobileAppConfigurationDeviceStatus.
ms.openlocfilehash: 2765b4640d5991c7833f18da33f89937729eac96
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090161"
---
# <a name="list-manageddevicemobileappconfigurationdevicestatuses"></a><span data-ttu-id="44c95-103">Lista managedDeviceMobileAppConfigurationDeviceStatuses</span><span class="sxs-lookup"><span data-stu-id="44c95-103">List managedDeviceMobileAppConfigurationDeviceStatuses</span></span>

> <span data-ttu-id="44c95-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="44c95-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="44c95-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="44c95-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="44c95-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="44c95-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="44c95-107">Propiedades de la lista y relaciones de los objetos [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="44c95-107">List properties and relationships of the [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="44c95-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="44c95-108">Prerequisites</span></span>
<span data-ttu-id="44c95-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="44c95-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="44c95-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="44c95-111">Permission type</span></span>|<span data-ttu-id="44c95-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="44c95-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="44c95-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="44c95-113">Delegated (work or school account)</span></span>|<span data-ttu-id="44c95-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span><span class="sxs-lookup"><span data-stu-id="44c95-114">DeviceManagementApps.ReadWrite.All, DeviceManagementApps.Read.All</span></span>|
|<span data-ttu-id="44c95-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="44c95-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="44c95-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="44c95-116">Not supported.</span></span>|
|<span data-ttu-id="44c95-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="44c95-117">Application</span></span>|<span data-ttu-id="44c95-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="44c95-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="44c95-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="44c95-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses
GET /deviceAppManagement/iosLobAppProvisioningConfigurations/{iosLobAppProvisioningConfigurationId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="44c95-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="44c95-120">Request headers</span></span>
|<span data-ttu-id="44c95-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="44c95-121">Header</span></span>|<span data-ttu-id="44c95-122">Valor</span><span class="sxs-lookup"><span data-stu-id="44c95-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="44c95-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="44c95-123">Authorization</span></span>|<span data-ttu-id="44c95-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="44c95-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="44c95-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="44c95-125">Accept</span></span>|<span data-ttu-id="44c95-126">application/json</span><span class="sxs-lookup"><span data-stu-id="44c95-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="44c95-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="44c95-127">Request body</span></span>
<span data-ttu-id="44c95-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="44c95-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="44c95-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44c95-129">Response</span></span>
<span data-ttu-id="44c95-130">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y una colección de objetos de [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="44c95-130">If successful, this method returns a `200 OK` response code and a collection of [managedDeviceMobileAppConfigurationDeviceStatus](../resources/intune-apps-manageddevicemobileappconfigurationdevicestatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="44c95-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="44c95-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="44c95-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="44c95-132">Request</span></span>
<span data-ttu-id="44c95-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="44c95-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/beta/deviceAppManagement/mobileAppConfigurations/{managedDeviceMobileAppConfigurationId}/deviceStatuses
```

### <a name="response"></a><span data-ttu-id="44c95-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="44c95-134">Response</span></span>
<span data-ttu-id="44c95-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="44c95-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 585

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.managedDeviceMobileAppConfigurationDeviceStatus",
      "id": "477d3651-3651-477d-5136-7d4751367d47",
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





