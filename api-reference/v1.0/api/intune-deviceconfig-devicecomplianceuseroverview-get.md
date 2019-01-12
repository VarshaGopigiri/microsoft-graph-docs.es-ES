---
title: Obtener deviceComplianceUserOverview
description: Lea las propiedades y las relaciones del objeto deviceComplianceUserOverview.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: b6e830edd53b780972fed6d548f3c4f733fbe116
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27972022"
---
# <a name="get-devicecomplianceuseroverview"></a><span data-ttu-id="55e28-103">Obtener deviceComplianceUserOverview</span><span class="sxs-lookup"><span data-stu-id="55e28-103">Get deviceComplianceUserOverview</span></span>

> <span data-ttu-id="55e28-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="55e28-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="55e28-105">Lea las propiedades y las relaciones del objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md).</span><span class="sxs-lookup"><span data-stu-id="55e28-105">Read properties and relationships of the [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="55e28-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="55e28-106">Prerequisites</span></span>
<span data-ttu-id="55e28-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="55e28-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="55e28-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="55e28-109">Permission type</span></span>|<span data-ttu-id="55e28-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="55e28-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="55e28-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="55e28-111">Delegated (work or school account)</span></span>|<span data-ttu-id="55e28-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="55e28-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="55e28-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="55e28-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="55e28-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55e28-114">Not supported.</span></span>|
|<span data-ttu-id="55e28-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="55e28-115">Application</span></span>|<span data-ttu-id="55e28-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="55e28-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="55e28-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="55e28-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatusOverview
```

## <a name="optional-query-parameters"></a><span data-ttu-id="55e28-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="55e28-118">Optional query parameters</span></span>
<span data-ttu-id="55e28-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55e28-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="55e28-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="55e28-120">Request headers</span></span>
|<span data-ttu-id="55e28-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55e28-121">Header</span></span>|<span data-ttu-id="55e28-122">Valor</span><span class="sxs-lookup"><span data-stu-id="55e28-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="55e28-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="55e28-123">Authorization</span></span>|<span data-ttu-id="55e28-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="55e28-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="55e28-125">Accept</span><span class="sxs-lookup"><span data-stu-id="55e28-125">Accept</span></span>|<span data-ttu-id="55e28-126">application/json</span><span class="sxs-lookup"><span data-stu-id="55e28-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="55e28-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="55e28-127">Request body</span></span>
<span data-ttu-id="55e28-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="55e28-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="55e28-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55e28-129">Response</span></span>
<span data-ttu-id="55e28-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="55e28-130">If successful, this method returns a `200 OK` response code and [deviceComplianceUserOverview](../resources/intune-deviceconfig-devicecomplianceuseroverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="55e28-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="55e28-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="55e28-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="55e28-132">Request</span></span>
<span data-ttu-id="55e28-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="55e28-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/userStatusOverview
```

### <a name="response"></a><span data-ttu-id="55e28-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="55e28-134">Response</span></span>
<span data-ttu-id="55e28-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="55e28-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 365

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceComplianceUserOverview",
    "id": "2d4f5bf4-5bf4-2d4f-f45b-4f2df45b4f2d",
    "pendingCount": 12,
    "notApplicableCount": 2,
    "successCount": 12,
    "errorCount": 10,
    "failedCount": 11,
    "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
    "configurationVersion": 4
  }
}
```



