---
title: Enumerar iosUpdateDeviceStatuses
description: Enumere las propiedades y las relaciones de los objetos iosUpdateDeviceStatus.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: d691d3ea20d3069364d849a3dbabf6f2aea92333
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27990386"
---
# <a name="list-iosupdatedevicestatuses"></a><span data-ttu-id="23e7e-103">Enumerar iosUpdateDeviceStatuses</span><span class="sxs-lookup"><span data-stu-id="23e7e-103">List iosUpdateDeviceStatuses</span></span>

> <span data-ttu-id="23e7e-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="23e7e-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="23e7e-105">Enumere las propiedades y las relaciones de los objetos [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="23e7e-105">List properties and relationships of the [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) objects.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="23e7e-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="23e7e-106">Prerequisites</span></span>
<span data-ttu-id="23e7e-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="23e7e-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="23e7e-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="23e7e-109">Permission type</span></span>|<span data-ttu-id="23e7e-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="23e7e-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="23e7e-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="23e7e-111">Delegated (work or school account)</span></span>|<span data-ttu-id="23e7e-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="23e7e-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="23e7e-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="23e7e-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="23e7e-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="23e7e-114">Not supported.</span></span>|
|<span data-ttu-id="23e7e-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="23e7e-115">Application</span></span>|<span data-ttu-id="23e7e-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="23e7e-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="23e7e-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="23e7e-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/iosUpdateStatuses
```

## <a name="request-headers"></a><span data-ttu-id="23e7e-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="23e7e-118">Request headers</span></span>
|<span data-ttu-id="23e7e-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="23e7e-119">Header</span></span>|<span data-ttu-id="23e7e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="23e7e-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="23e7e-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="23e7e-121">Authorization</span></span>|<span data-ttu-id="23e7e-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="23e7e-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="23e7e-123">Accept</span><span class="sxs-lookup"><span data-stu-id="23e7e-123">Accept</span></span>|<span data-ttu-id="23e7e-124">application/json</span><span class="sxs-lookup"><span data-stu-id="23e7e-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="23e7e-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="23e7e-125">Request body</span></span>
<span data-ttu-id="23e7e-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="23e7e-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="23e7e-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="23e7e-127">Response</span></span>
<span data-ttu-id="23e7e-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y una colección de objetos [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="23e7e-128">If successful, this method returns a `200 OK` response code and a collection of [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) objects in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="23e7e-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="23e7e-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="23e7e-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="23e7e-130">Request</span></span>
<span data-ttu-id="23e7e-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="23e7e-131">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/iosUpdateStatuses
```

### <a name="response"></a><span data-ttu-id="23e7e-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="23e7e-132">Response</span></span>
<span data-ttu-id="23e7e-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="23e7e-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 686

{
  "value": [
    {
      "@odata.type": "#microsoft.graph.iosUpdateDeviceStatus",
      "id": "63a79499-9499-63a7-9994-a7639994a763",
      "installStatus": "available",
      "osVersion": "Os Version value",
      "deviceId": "Device Id value",
      "userId": "User Id value",
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



