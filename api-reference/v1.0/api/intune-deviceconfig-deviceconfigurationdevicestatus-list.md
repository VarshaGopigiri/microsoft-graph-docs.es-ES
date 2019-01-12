---
title: Enumerar deviceConfigurationDeviceStatuses
description: Enumere las propiedades y las relaciones de los objetos deviceConfigurationDeviceStatus.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 7d653e4e6463fa0cba1a85b13777cc8b880f9e1a
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27911836"
---
# <a name="list-deviceconfigurationdevicestatuses"></a><span data-ttu-id="a6d2b-103">Enumerar deviceConfigurationDeviceStatuses</span><span class="sxs-lookup"><span data-stu-id="a6d2b-103">List deviceConfigurationDeviceStatuses</span></span>

> <span data-ttu-id="a6d2b-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a6d2b-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a6d2b-105">Enumere las propiedades y las relaciones de los objetos [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="a6d2b-105">List properties and relationships of the [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a6d2b-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a6d2b-106">Prerequisites</span></span>
<span data-ttu-id="a6d2b-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a6d2b-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a6d2b-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a6d2b-109">Permission type</span></span>|<span data-ttu-id="a6d2b-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a6d2b-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a6d2b-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a6d2b-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a6d2b-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="a6d2b-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="a6d2b-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a6d2b-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a6d2b-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a6d2b-114">Not supported.</span></span>|
|<span data-ttu-id="a6d2b-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a6d2b-115">Application</span></span>|<span data-ttu-id="a6d2b-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a6d2b-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a6d2b-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a6d2b-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="a6d2b-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a6d2b-118">Request headers</span></span>
|<span data-ttu-id="a6d2b-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a6d2b-119">Header</span></span>|<span data-ttu-id="a6d2b-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a6d2b-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a6d2b-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="a6d2b-121">Authorization</span></span>|<span data-ttu-id="a6d2b-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a6d2b-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a6d2b-123">Accept</span><span class="sxs-lookup"><span data-stu-id="a6d2b-123">Accept</span></span>|<span data-ttu-id="a6d2b-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a6d2b-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a6d2b-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a6d2b-125">Request body</span></span>
<span data-ttu-id="a6d2b-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="a6d2b-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="a6d2b-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6d2b-127">Response</span></span>
<span data-ttu-id="a6d2b-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a6d2b-128">If successful, this method returns a `200 OK` response code and a collection of [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a6d2b-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a6d2b-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="a6d2b-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a6d2b-130">Request</span></span>
<span data-ttu-id="a6d2b-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a6d2b-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses
```

### <a name="response"></a><span data-ttu-id="a6d2b-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a6d2b-132">Response</span></span>
<span data-ttu-id="a6d2b-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a6d2b-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 547

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStatus",
      "id": "674e98e5-98e5-674e-e598-4e67e5984e67",
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



