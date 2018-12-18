---
title: Obtener iosUpdateDeviceStatus
description: Lea las propiedades y las relaciones del objeto iosUpdateDeviceStatus.
author: tfitzmac
ms.openlocfilehash: b09ca55ff43df0041e18090a209659e8f8afbe70
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27339770"
---
# <a name="get-iosupdatedevicestatus"></a><span data-ttu-id="f6a17-103">Obtener iosUpdateDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="f6a17-103">Get iosUpdateDeviceStatus</span></span>

> <span data-ttu-id="f6a17-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f6a17-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f6a17-105">Lea las propiedades y las relaciones del objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="f6a17-105">Read properties and relationships of the [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f6a17-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f6a17-106">Prerequisites</span></span>
<span data-ttu-id="f6a17-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f6a17-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f6a17-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f6a17-109">Permission type</span></span>|<span data-ttu-id="f6a17-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f6a17-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f6a17-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f6a17-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f6a17-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="f6a17-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="f6a17-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f6a17-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f6a17-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6a17-114">Not supported.</span></span>|
|<span data-ttu-id="f6a17-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f6a17-115">Application</span></span>|<span data-ttu-id="f6a17-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f6a17-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f6a17-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f6a17-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="f6a17-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="f6a17-118">Optional query parameters</span></span>
<span data-ttu-id="f6a17-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6a17-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="f6a17-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f6a17-120">Request headers</span></span>
|<span data-ttu-id="f6a17-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f6a17-121">Header</span></span>|<span data-ttu-id="f6a17-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f6a17-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f6a17-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="f6a17-123">Authorization</span></span>|<span data-ttu-id="f6a17-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f6a17-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f6a17-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f6a17-125">Accept</span></span>|<span data-ttu-id="f6a17-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f6a17-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f6a17-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f6a17-127">Request body</span></span>
<span data-ttu-id="f6a17-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="f6a17-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="f6a17-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6a17-129">Response</span></span>
<span data-ttu-id="f6a17-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f6a17-130">If successful, this method returns a `200 OK` response code and [iosUpdateDeviceStatus](../resources/intune-deviceconfig-iosupdatedevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f6a17-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f6a17-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="f6a17-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f6a17-132">Request</span></span>
<span data-ttu-id="f6a17-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f6a17-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/iosUpdateStatuses/{iosUpdateDeviceStatusId}
```

### <a name="response"></a><span data-ttu-id="f6a17-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f6a17-134">Response</span></span>
<span data-ttu-id="f6a17-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f6a17-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 646

{
  "value": {
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
}
```



