---
title: Crear deviceComplianceScheduledActionForRule
description: Cree un objeto deviceComplianceScheduledActionForRule.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f6eca5f5f381c069410477ff98004ac5ebd094ba
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870172"
---
# <a name="create-devicecompliancescheduledactionforrule"></a><span data-ttu-id="40bf6-103">Crear deviceComplianceScheduledActionForRule</span><span class="sxs-lookup"><span data-stu-id="40bf6-103">Create deviceComplianceScheduledActionForRule</span></span>

> <span data-ttu-id="40bf6-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="40bf6-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="40bf6-105">Cree un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="40bf6-105">Create a new [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="40bf6-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="40bf6-106">Prerequisites</span></span>
<span data-ttu-id="40bf6-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="40bf6-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="40bf6-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="40bf6-109">Permission type</span></span>|<span data-ttu-id="40bf6-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="40bf6-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="40bf6-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="40bf6-111">Delegated (work or school account)</span></span>|<span data-ttu-id="40bf6-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="40bf6-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="40bf6-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="40bf6-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="40bf6-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="40bf6-114">Not supported.</span></span>|
|<span data-ttu-id="40bf6-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="40bf6-115">Application</span></span>|<span data-ttu-id="40bf6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="40bf6-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="40bf6-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="40bf6-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule
```

## <a name="request-headers"></a><span data-ttu-id="40bf6-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="40bf6-118">Request headers</span></span>
|<span data-ttu-id="40bf6-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="40bf6-119">Header</span></span>|<span data-ttu-id="40bf6-120">Valor</span><span class="sxs-lookup"><span data-stu-id="40bf6-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="40bf6-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="40bf6-121">Authorization</span></span>|<span data-ttu-id="40bf6-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="40bf6-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="40bf6-123">Accept</span><span class="sxs-lookup"><span data-stu-id="40bf6-123">Accept</span></span>|<span data-ttu-id="40bf6-124">application/json</span><span class="sxs-lookup"><span data-stu-id="40bf6-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="40bf6-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="40bf6-125">Request body</span></span>
<span data-ttu-id="40bf6-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceScheduledActionForRule.</span><span class="sxs-lookup"><span data-stu-id="40bf6-126">In the request body, supply a JSON representation for the deviceComplianceScheduledActionForRule object.</span></span>

<span data-ttu-id="40bf6-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceScheduledActionForRule.</span><span class="sxs-lookup"><span data-stu-id="40bf6-127">The following table shows the properties that are required when you create the deviceComplianceScheduledActionForRule.</span></span>

|<span data-ttu-id="40bf6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="40bf6-128">Property</span></span>|<span data-ttu-id="40bf6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="40bf6-129">Type</span></span>|<span data-ttu-id="40bf6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="40bf6-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="40bf6-131">id</span><span class="sxs-lookup"><span data-stu-id="40bf6-131">id</span></span>|<span data-ttu-id="40bf6-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="40bf6-132">String</span></span>|<span data-ttu-id="40bf6-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="40bf6-133">Key of the entity.</span></span>|
|<span data-ttu-id="40bf6-134">ruleName</span><span class="sxs-lookup"><span data-stu-id="40bf6-134">ruleName</span></span>|<span data-ttu-id="40bf6-135">String</span><span class="sxs-lookup"><span data-stu-id="40bf6-135">String</span></span>|<span data-ttu-id="40bf6-136">Nombre de la regla a la que se aplica esta acción programada.</span><span class="sxs-lookup"><span data-stu-id="40bf6-136">Name of the rule which this scheduled action applies to.</span></span>|



## <a name="response"></a><span data-ttu-id="40bf6-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40bf6-137">Response</span></span>
<span data-ttu-id="40bf6-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="40bf6-138">If successful, this method returns a `201 Created` response code and a [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="40bf6-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="40bf6-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="40bf6-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="40bf6-140">Request</span></span>
<span data-ttu-id="40bf6-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="40bf6-141">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule
Content-type: application/json
Content-length: 114

{
  "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
  "ruleName": "Rule Name value"
}
```

### <a name="response"></a><span data-ttu-id="40bf6-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="40bf6-142">Response</span></span>
<span data-ttu-id="40bf6-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="40bf6-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 163

{
  "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
  "id": "f0075d5e-5d5e-f007-5e5d-07f05e5d07f0",
  "ruleName": "Rule Name value"
}
```



