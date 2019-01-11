---
title: Obtener deviceCompliancePolicyDeviceStateSummary
description: Lea las propiedades y las relaciones del objeto deviceCompliancePolicyDeviceStateSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 7eea3b21c2f8cbcd6c003fe8f16c950544e5cce6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27881021"
---
# <a name="get-devicecompliancepolicydevicestatesummary"></a><span data-ttu-id="e2ea5-103">Obtener deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="e2ea5-103">Get deviceCompliancePolicyDeviceStateSummary</span></span>

> <span data-ttu-id="e2ea5-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="e2ea5-105">Lea las propiedades y las relaciones del objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="e2ea5-105">Read properties and relationships of the [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="e2ea5-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e2ea5-106">Prerequisites</span></span>
<span data-ttu-id="e2ea5-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="e2ea5-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="e2ea5-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="e2ea5-109">Permission type</span></span>|<span data-ttu-id="e2ea5-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="e2ea5-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="e2ea5-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="e2ea5-111">Delegated (work or school account)</span></span>|<span data-ttu-id="e2ea5-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="e2ea5-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="e2ea5-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="e2ea5-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="e2ea5-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-114">Not supported.</span></span>|
|<span data-ttu-id="e2ea5-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="e2ea5-115">Application</span></span>|<span data-ttu-id="e2ea5-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="e2ea5-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="e2ea5-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicyDeviceStateSummary
```

## <a name="optional-query-parameters"></a><span data-ttu-id="e2ea5-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="e2ea5-118">Optional query parameters</span></span>
<span data-ttu-id="e2ea5-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="e2ea5-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="e2ea5-120">Request headers</span></span>
|<span data-ttu-id="e2ea5-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e2ea5-121">Header</span></span>|<span data-ttu-id="e2ea5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e2ea5-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="e2ea5-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="e2ea5-123">Authorization</span></span>|<span data-ttu-id="e2ea5-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="e2ea5-125">Accept</span><span class="sxs-lookup"><span data-stu-id="e2ea5-125">Accept</span></span>|<span data-ttu-id="e2ea5-126">application/json</span><span class="sxs-lookup"><span data-stu-id="e2ea5-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="e2ea5-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="e2ea5-127">Request body</span></span>
<span data-ttu-id="e2ea5-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="e2ea5-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2ea5-129">Response</span></span>
<span data-ttu-id="e2ea5-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-130">If successful, this method returns a `200 OK` response code and [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="e2ea5-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e2ea5-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="e2ea5-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="e2ea5-132">Request</span></span>
<span data-ttu-id="e2ea5-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicyDeviceStateSummary
```

### <a name="response"></a><span data-ttu-id="e2ea5-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="e2ea5-134">Response</span></span>
<span data-ttu-id="e2ea5-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="e2ea5-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 439

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceCompliancePolicyDeviceStateSummary",
    "inGracePeriodCount": 2,
    "configManagerCount": 2,
    "id": "8c4de8a7-e8a7-8c4d-a7e8-4d8ca7e84d8c",
    "unknownDeviceCount": 2,
    "notApplicableDeviceCount": 8,
    "compliantDeviceCount": 4,
    "remediatedDeviceCount": 5,
    "nonCompliantDeviceCount": 7,
    "errorDeviceCount": 0,
    "conflictDeviceCount": 3
  }
}
```



