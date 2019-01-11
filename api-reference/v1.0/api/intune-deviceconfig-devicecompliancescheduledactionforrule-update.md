---
title: Actualizar deviceComplianceScheduledActionForRule
description: Actualice las propiedades de un objeto deviceComplianceScheduledActionForRule.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e12282024216582941ac4ed63108194a863cdc03
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27818308"
---
# <a name="update-devicecompliancescheduledactionforrule"></a><span data-ttu-id="2ea60-103">Actualizar deviceComplianceScheduledActionForRule</span><span class="sxs-lookup"><span data-stu-id="2ea60-103">Update deviceComplianceScheduledActionForRule</span></span>

> <span data-ttu-id="2ea60-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2ea60-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2ea60-105">Actualice las propiedades de un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="2ea60-105">Update the properties of a [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2ea60-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2ea60-106">Prerequisites</span></span>
<span data-ttu-id="2ea60-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2ea60-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2ea60-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2ea60-109">Permission type</span></span>|<span data-ttu-id="2ea60-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2ea60-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2ea60-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2ea60-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2ea60-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2ea60-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2ea60-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2ea60-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2ea60-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ea60-114">Not supported.</span></span>|
|<span data-ttu-id="2ea60-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2ea60-115">Application</span></span>|<span data-ttu-id="2ea60-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2ea60-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2ea60-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2ea60-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
```

## <a name="request-headers"></a><span data-ttu-id="2ea60-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2ea60-118">Request headers</span></span>
|<span data-ttu-id="2ea60-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2ea60-119">Header</span></span>|<span data-ttu-id="2ea60-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2ea60-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2ea60-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="2ea60-121">Authorization</span></span>|<span data-ttu-id="2ea60-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2ea60-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2ea60-123">Accept</span><span class="sxs-lookup"><span data-stu-id="2ea60-123">Accept</span></span>|<span data-ttu-id="2ea60-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2ea60-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2ea60-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2ea60-125">Request body</span></span>
<span data-ttu-id="2ea60-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="2ea60-126">In the request body, supply a JSON representation for the [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>

<span data-ttu-id="2ea60-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="2ea60-127">The following table shows the properties that are required when you create the [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span></span>

|<span data-ttu-id="2ea60-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2ea60-128">Property</span></span>|<span data-ttu-id="2ea60-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2ea60-129">Type</span></span>|<span data-ttu-id="2ea60-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ea60-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2ea60-131">id</span><span class="sxs-lookup"><span data-stu-id="2ea60-131">id</span></span>|<span data-ttu-id="2ea60-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="2ea60-132">String</span></span>|<span data-ttu-id="2ea60-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2ea60-133">Key of the entity.</span></span>|
|<span data-ttu-id="2ea60-134">ruleName</span><span class="sxs-lookup"><span data-stu-id="2ea60-134">ruleName</span></span>|<span data-ttu-id="2ea60-135">String</span><span class="sxs-lookup"><span data-stu-id="2ea60-135">String</span></span>|<span data-ttu-id="2ea60-136">Nombre de la regla a la que se aplica esta acción programada.</span><span class="sxs-lookup"><span data-stu-id="2ea60-136">Name of the rule which this scheduled action applies to.</span></span>|



## <a name="response"></a><span data-ttu-id="2ea60-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ea60-137">Response</span></span>
<span data-ttu-id="2ea60-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2ea60-138">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2ea60-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2ea60-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="2ea60-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2ea60-140">Request</span></span>
<span data-ttu-id="2ea60-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2ea60-141">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
Content-type: application/json
Content-length: 114

{
  "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
  "ruleName": "Rule Name value"
}
```

### <a name="response"></a><span data-ttu-id="2ea60-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2ea60-142">Response</span></span>
<span data-ttu-id="2ea60-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2ea60-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 163

{
  "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
  "id": "f0075d5e-5d5e-f007-5e5d-07f05e5d07f0",
  "ruleName": "Rule Name value"
}
```



