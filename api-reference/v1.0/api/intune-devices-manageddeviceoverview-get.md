---
title: Obtener managedDeviceOverview
description: Lea las propiedades y las relaciones del objeto managedDeviceOverview.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a3a629abd8c7212dde11274cb626f3e3347be3e6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27930204"
---
# <a name="get-manageddeviceoverview"></a><span data-ttu-id="7afd0-103">Obtener managedDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="7afd0-103">Get managedDeviceOverview</span></span>

> <span data-ttu-id="7afd0-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7afd0-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7afd0-105">Lea las propiedades y las relaciones del objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="7afd0-105">Read properties and relationships of the [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7afd0-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7afd0-106">Prerequisites</span></span>
<span data-ttu-id="7afd0-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7afd0-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7afd0-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7afd0-109">Permission type</span></span>|<span data-ttu-id="7afd0-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7afd0-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7afd0-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7afd0-111">Delegated (work or school account)</span></span>|<span data-ttu-id="7afd0-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span><span class="sxs-lookup"><span data-stu-id="7afd0-112">DeviceManagementManagedDevices.ReadWrite.All, DeviceManagementManagedDevices.Read.All</span></span>|
|<span data-ttu-id="7afd0-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7afd0-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7afd0-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7afd0-114">Not supported.</span></span>|
|<span data-ttu-id="7afd0-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7afd0-115">Application</span></span>|<span data-ttu-id="7afd0-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7afd0-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7afd0-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7afd0-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/managedDeviceOverview
```

## <a name="optional-query-parameters"></a><span data-ttu-id="7afd0-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7afd0-118">Optional query parameters</span></span>
<span data-ttu-id="7afd0-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7afd0-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="7afd0-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7afd0-120">Request headers</span></span>
|<span data-ttu-id="7afd0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7afd0-121">Header</span></span>|<span data-ttu-id="7afd0-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7afd0-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7afd0-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7afd0-123">Authorization</span></span>|<span data-ttu-id="7afd0-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7afd0-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7afd0-125">Accept</span><span class="sxs-lookup"><span data-stu-id="7afd0-125">Accept</span></span>|<span data-ttu-id="7afd0-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7afd0-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7afd0-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7afd0-127">Request body</span></span>
<span data-ttu-id="7afd0-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7afd0-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7afd0-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7afd0-129">Response</span></span>
<span data-ttu-id="7afd0-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7afd0-130">If successful, this method returns a `200 OK` response code and [managedDeviceOverview](../resources/intune-devices-manageddeviceoverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7afd0-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7afd0-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="7afd0-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7afd0-132">Request</span></span>
<span data-ttu-id="7afd0-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7afd0-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/managedDeviceOverview
```

### <a name="response"></a><span data-ttu-id="7afd0-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7afd0-134">Response</span></span>
<span data-ttu-id="7afd0-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7afd0-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 797

{
  "value": {
    "@odata.type": "#microsoft.graph.managedDeviceOverview",
    "id": "42a91653-1653-42a9-5316-a9425316a942",
    "enrolledDeviceCount": 3,
    "mdmEnrolledCount": 0,
    "dualEnrolledDeviceCount": 7,
    "deviceOperatingSystemSummary": {
      "@odata.type": "microsoft.graph.deviceOperatingSystemSummary",
      "androidCount": 12,
      "iosCount": 8,
      "macOSCount": 10,
      "windowsMobileCount": 2,
      "windowsCount": 12,
      "unknownCount": 12
    },
    "deviceExchangeAccessStateSummary": {
      "@odata.type": "microsoft.graph.deviceExchangeAccessStateSummary",
      "allowedDeviceCount": 2,
      "blockedDeviceCount": 2,
      "quarantinedDeviceCount": 6,
      "unknownDeviceCount": 2,
      "unavailableDeviceCount": 6
    }
  }
}
```



