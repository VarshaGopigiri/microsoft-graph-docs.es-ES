---
title: Enumerar deviceConfigurationDeviceStatuses
description: Enumere las propiedades y las relaciones de los objetos deviceConfigurationDeviceStatus.
author: tfitzmac
ms.openlocfilehash: 13eb5d81fd9d0527c6004eebf7aa909c6f4049ec
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27348464"
---
# <a name="list-deviceconfigurationdevicestatuses"></a><span data-ttu-id="043fb-103">Enumerar deviceConfigurationDeviceStatuses</span><span class="sxs-lookup"><span data-stu-id="043fb-103">List deviceConfigurationDeviceStatuses</span></span>

> <span data-ttu-id="043fb-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="043fb-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="043fb-105">Enumere las propiedades y las relaciones de los objetos [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="043fb-105">List properties and relationships of the [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="043fb-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="043fb-106">Prerequisites</span></span>
<span data-ttu-id="043fb-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="043fb-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="043fb-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="043fb-109">Permission type</span></span>|<span data-ttu-id="043fb-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="043fb-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="043fb-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="043fb-111">Delegated (work or school account)</span></span>|<span data-ttu-id="043fb-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="043fb-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="043fb-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="043fb-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="043fb-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="043fb-114">Not supported.</span></span>|
|<span data-ttu-id="043fb-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="043fb-115">Application</span></span>|<span data-ttu-id="043fb-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="043fb-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="043fb-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="043fb-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="043fb-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="043fb-118">Request headers</span></span>
|<span data-ttu-id="043fb-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="043fb-119">Header</span></span>|<span data-ttu-id="043fb-120">Valor</span><span class="sxs-lookup"><span data-stu-id="043fb-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="043fb-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="043fb-121">Authorization</span></span>|<span data-ttu-id="043fb-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="043fb-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="043fb-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="043fb-123">Accept</span></span>|<span data-ttu-id="043fb-124">application/json</span><span class="sxs-lookup"><span data-stu-id="043fb-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="043fb-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="043fb-125">Request body</span></span>
<span data-ttu-id="043fb-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="043fb-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="043fb-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="043fb-127">Response</span></span>
<span data-ttu-id="043fb-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="043fb-128">If successful, this method returns a `200 OK` response code and a collection of [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="043fb-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="043fb-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="043fb-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="043fb-130">Request</span></span>
<span data-ttu-id="043fb-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="043fb-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses
```

### <a name="response"></a><span data-ttu-id="043fb-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="043fb-132">Response</span></span>
<span data-ttu-id="043fb-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="043fb-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



