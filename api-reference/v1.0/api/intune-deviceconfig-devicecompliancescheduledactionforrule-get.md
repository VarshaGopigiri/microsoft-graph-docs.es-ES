---
title: Obtener deviceComplianceScheduledActionForRule
description: Lea las propiedades y las relaciones del objeto deviceComplianceScheduledActionForRule.
author: tfitzmac
ms.openlocfilehash: d8a48426401bff258e285cec51f3d533a6890f2f
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27315480"
---
# <a name="get-devicecompliancescheduledactionforrule"></a><span data-ttu-id="7958a-103">Obtener deviceComplianceScheduledActionForRule</span><span class="sxs-lookup"><span data-stu-id="7958a-103">Get deviceComplianceScheduledActionForRule</span></span>

> <span data-ttu-id="7958a-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7958a-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7958a-105">Lea las propiedades y las relaciones del objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="7958a-105">Read properties and relationships of the [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="7958a-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="7958a-106">Prerequisites</span></span>
<span data-ttu-id="7958a-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="7958a-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="7958a-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="7958a-109">Permission type</span></span>|<span data-ttu-id="7958a-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="7958a-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="7958a-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="7958a-111">Delegated (work or school account)</span></span>|<span data-ttu-id="7958a-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span><span class="sxs-lookup"><span data-stu-id="7958a-112">DeviceManagementConfiguration.ReadWrite.All, DeviceManagementConfiguration.Read.All</span></span>|
|<span data-ttu-id="7958a-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="7958a-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="7958a-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7958a-114">Not supported.</span></span>|
|<span data-ttu-id="7958a-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="7958a-115">Application</span></span>|<span data-ttu-id="7958a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="7958a-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="7958a-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="7958a-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
GET /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
```

## <a name="optional-query-parameters"></a><span data-ttu-id="7958a-118">Parámetros de consulta opcionales</span><span class="sxs-lookup"><span data-stu-id="7958a-118">Optional query parameters</span></span>
<span data-ttu-id="7958a-119">Este método admite los [parámetros de consulta de OData](https://developer.microsoft.com/graph/docs/concepts/query_parameters) a modo de ayuda para personalizar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7958a-119">This method supports the [OData Query Parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) to help customize the response.</span></span>
## <a name="request-headers"></a><span data-ttu-id="7958a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="7958a-120">Request headers</span></span>
|<span data-ttu-id="7958a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7958a-121">Header</span></span>|<span data-ttu-id="7958a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7958a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="7958a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="7958a-123">Authorization</span></span>|<span data-ttu-id="7958a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="7958a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="7958a-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="7958a-125">Accept</span></span>|<span data-ttu-id="7958a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="7958a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="7958a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="7958a-127">Request body</span></span>
<span data-ttu-id="7958a-128">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="7958a-128">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="7958a-129">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7958a-129">Response</span></span>
<span data-ttu-id="7958a-130">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y el objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="7958a-130">If successful, this method returns a `200 OK` response code and [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="7958a-131">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7958a-131">Example</span></span>
### <a name="request"></a><span data-ttu-id="7958a-132">Solicitud</span><span class="sxs-lookup"><span data-stu-id="7958a-132">Request</span></span>
<span data-ttu-id="7958a-133">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="7958a-133">Here is an example of the request.</span></span>
``` http
GET https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
```

### <a name="response"></a><span data-ttu-id="7958a-134">Respuesta</span><span class="sxs-lookup"><span data-stu-id="7958a-134">Response</span></span>
<span data-ttu-id="7958a-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="7958a-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 188

{
  "value": {
    "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
    "id": "f0075d5e-5d5e-f007-5e5d-07f05e5d07f0",
    "ruleName": "Rule Name value"
  }
}
```



