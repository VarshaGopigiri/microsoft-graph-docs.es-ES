---
title: Crear deviceComplianceScheduledActionForRule
description: Cree un objeto deviceComplianceScheduledActionForRule.
ms.openlocfilehash: 79fdd763f3b194d27fad81cebb743f3455749dc8
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028596"
---
# <a name="create-devicecompliancescheduledactionforrule"></a><span data-ttu-id="0e8a2-103">Crear deviceComplianceScheduledActionForRule</span><span class="sxs-lookup"><span data-stu-id="0e8a2-103">Create deviceComplianceScheduledActionForRule</span></span>

> <span data-ttu-id="0e8a2-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0e8a2-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0e8a2-105">Cree un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="0e8a2-105">Create a new [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0e8a2-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0e8a2-106">Prerequisites</span></span>
<span data-ttu-id="0e8a2-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0e8a2-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0e8a2-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0e8a2-109">Permission type</span></span>|<span data-ttu-id="0e8a2-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0e8a2-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0e8a2-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0e8a2-111">Delegated (work or school account)</span></span>|<span data-ttu-id="0e8a2-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0e8a2-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0e8a2-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0e8a2-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0e8a2-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e8a2-114">Not supported.</span></span>|
|<span data-ttu-id="0e8a2-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0e8a2-115">Application</span></span>|<span data-ttu-id="0e8a2-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0e8a2-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0e8a2-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0e8a2-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule
```

## <a name="request-headers"></a><span data-ttu-id="0e8a2-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0e8a2-118">Request headers</span></span>
|<span data-ttu-id="0e8a2-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e8a2-119">Header</span></span>|<span data-ttu-id="0e8a2-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0e8a2-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0e8a2-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="0e8a2-121">Authorization</span></span>|<span data-ttu-id="0e8a2-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0e8a2-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0e8a2-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0e8a2-123">Accept</span></span>|<span data-ttu-id="0e8a2-124">application/json</span><span class="sxs-lookup"><span data-stu-id="0e8a2-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0e8a2-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0e8a2-125">Request body</span></span>
<span data-ttu-id="0e8a2-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceScheduledActionForRule.</span><span class="sxs-lookup"><span data-stu-id="0e8a2-126">In the request body, supply a JSON representation for the deviceComplianceScheduledActionForRule object.</span></span>

<span data-ttu-id="0e8a2-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceScheduledActionForRule.</span><span class="sxs-lookup"><span data-stu-id="0e8a2-127">The following table shows the properties that are required when you create the deviceComplianceScheduledActionForRule.</span></span>

|<span data-ttu-id="0e8a2-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0e8a2-128">Property</span></span>|<span data-ttu-id="0e8a2-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e8a2-129">Type</span></span>|<span data-ttu-id="0e8a2-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e8a2-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0e8a2-131">id</span><span class="sxs-lookup"><span data-stu-id="0e8a2-131">id</span></span>|<span data-ttu-id="0e8a2-132">String</span><span class="sxs-lookup"><span data-stu-id="0e8a2-132">String</span></span>|<span data-ttu-id="0e8a2-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0e8a2-133">Key of the entity.</span></span>|
|<span data-ttu-id="0e8a2-134">ruleName</span><span class="sxs-lookup"><span data-stu-id="0e8a2-134">ruleName</span></span>|<span data-ttu-id="0e8a2-135">String</span><span class="sxs-lookup"><span data-stu-id="0e8a2-135">String</span></span>|<span data-ttu-id="0e8a2-136">Nombre de la regla a la que se aplica esta acción programada.</span><span class="sxs-lookup"><span data-stu-id="0e8a2-136">Name of the rule which this scheduled action applies to.</span></span>|



## <a name="response"></a><span data-ttu-id="0e8a2-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e8a2-137">Response</span></span>
<span data-ttu-id="0e8a2-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0e8a2-138">If successful, this method returns a `201 Created` response code and a [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0e8a2-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0e8a2-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="0e8a2-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0e8a2-140">Request</span></span>
<span data-ttu-id="0e8a2-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0e8a2-141">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule
Content-type: application/json
Content-length: 114

{
  "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
  "ruleName": "Rule Name value"
}
```

### <a name="response"></a><span data-ttu-id="0e8a2-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0e8a2-142">Response</span></span>
<span data-ttu-id="0e8a2-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0e8a2-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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


