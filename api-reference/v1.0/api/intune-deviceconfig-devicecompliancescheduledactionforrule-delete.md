---
title: Eliminar deviceComplianceScheduledActionForRule
description: Elimina un deviceComplianceScheduledActionForRule.
ms.openlocfilehash: 5fa3b77a75d602c7fc74a1a88d07a76aa5db4130
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030877"
---
# <a name="delete-devicecompliancescheduledactionforrule"></a><span data-ttu-id="03b0f-103">Eliminar deviceComplianceScheduledActionForRule</span><span class="sxs-lookup"><span data-stu-id="03b0f-103">Delete deviceComplianceScheduledActionForRule</span></span>

> <span data-ttu-id="03b0f-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="03b0f-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="03b0f-105">Elimina un [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="03b0f-105">Deletes a [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span></span>
## <a name="prerequisites"></a><span data-ttu-id="03b0f-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="03b0f-106">Prerequisites</span></span>
<span data-ttu-id="03b0f-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="03b0f-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="03b0f-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="03b0f-109">Permission type</span></span>|<span data-ttu-id="03b0f-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="03b0f-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="03b0f-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="03b0f-111">Delegated (work or school account)</span></span>|<span data-ttu-id="03b0f-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="03b0f-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="03b0f-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="03b0f-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="03b0f-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03b0f-114">Not supported.</span></span>|
|<span data-ttu-id="03b0f-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="03b0f-115">Application</span></span>|<span data-ttu-id="03b0f-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="03b0f-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="03b0f-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="03b0f-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
DELETE /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
```

## <a name="request-headers"></a><span data-ttu-id="03b0f-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="03b0f-118">Request headers</span></span>
|<span data-ttu-id="03b0f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03b0f-119">Header</span></span>|<span data-ttu-id="03b0f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="03b0f-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="03b0f-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="03b0f-121">Authorization</span></span>|<span data-ttu-id="03b0f-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="03b0f-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="03b0f-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="03b0f-123">Accept</span></span>|<span data-ttu-id="03b0f-124">application/json</span><span class="sxs-lookup"><span data-stu-id="03b0f-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="03b0f-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="03b0f-125">Request body</span></span>
<span data-ttu-id="03b0f-126">No proporcione un cuerpo de solicitud para este método.</span><span class="sxs-lookup"><span data-stu-id="03b0f-126">Do not supply a request body for this method.</span></span>

## <a name="response"></a><span data-ttu-id="03b0f-127">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03b0f-127">Response</span></span>
<span data-ttu-id="03b0f-128">Si se ejecuta correctamente, este método devuelve un código de respuesta `204 No Content`.</span><span class="sxs-lookup"><span data-stu-id="03b0f-128">If successful, this method returns a `204 No Content` response code.</span></span>

## <a name="example"></a><span data-ttu-id="03b0f-129">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="03b0f-129">Example</span></span>
### <a name="request"></a><span data-ttu-id="03b0f-130">Solicitud</span><span class="sxs-lookup"><span data-stu-id="03b0f-130">Request</span></span>
<span data-ttu-id="03b0f-131">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="03b0f-131">Here is an example of the request.</span></span>
``` http
DELETE https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
```

### <a name="response"></a><span data-ttu-id="03b0f-132">Respuesta</span><span class="sxs-lookup"><span data-stu-id="03b0f-132">Response</span></span>
<span data-ttu-id="03b0f-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="03b0f-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 204 No Content
```



