---
title: Actualizar deviceComplianceScheduledActionForRule
description: Actualice las propiedades de un objeto deviceComplianceScheduledActionForRule.
author: tfitzmac
ms.openlocfilehash: e63602cf39aa89bfdcda2db900d993d8e0a56d9d
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27301662"
---
# <a name="update-devicecompliancescheduledactionforrule"></a><span data-ttu-id="2d058-103">Actualizar deviceComplianceScheduledActionForRule</span><span class="sxs-lookup"><span data-stu-id="2d058-103">Update deviceComplianceScheduledActionForRule</span></span>

> <span data-ttu-id="2d058-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2d058-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2d058-105">Actualice las propiedades de un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="2d058-105">Update the properties of a [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="2d058-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="2d058-106">Prerequisites</span></span>
<span data-ttu-id="2d058-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="2d058-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="2d058-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="2d058-109">Permission type</span></span>|<span data-ttu-id="2d058-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="2d058-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="2d058-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="2d058-111">Delegated (work or school account)</span></span>|<span data-ttu-id="2d058-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="2d058-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="2d058-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="2d058-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="2d058-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d058-114">Not supported.</span></span>|
|<span data-ttu-id="2d058-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="2d058-115">Application</span></span>|<span data-ttu-id="2d058-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="2d058-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="2d058-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="2d058-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
```

## <a name="request-headers"></a><span data-ttu-id="2d058-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="2d058-118">Request headers</span></span>
|<span data-ttu-id="2d058-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2d058-119">Header</span></span>|<span data-ttu-id="2d058-120">Valor</span><span class="sxs-lookup"><span data-stu-id="2d058-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="2d058-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="2d058-121">Authorization</span></span>|<span data-ttu-id="2d058-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="2d058-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="2d058-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="2d058-123">Accept</span></span>|<span data-ttu-id="2d058-124">application/json</span><span class="sxs-lookup"><span data-stu-id="2d058-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="2d058-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="2d058-125">Request body</span></span>
<span data-ttu-id="2d058-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="2d058-126">In the request body, supply a JSON representation for the [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>

<span data-ttu-id="2d058-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="2d058-127">The following table shows the properties that are required when you create the [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span></span>

|<span data-ttu-id="2d058-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2d058-128">Property</span></span>|<span data-ttu-id="2d058-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="2d058-129">Type</span></span>|<span data-ttu-id="2d058-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d058-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2d058-131">id</span><span class="sxs-lookup"><span data-stu-id="2d058-131">id</span></span>|<span data-ttu-id="2d058-132">String</span><span class="sxs-lookup"><span data-stu-id="2d058-132">String</span></span>|<span data-ttu-id="2d058-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="2d058-133">Key of the entity.</span></span>|
|<span data-ttu-id="2d058-134">ruleName</span><span class="sxs-lookup"><span data-stu-id="2d058-134">ruleName</span></span>|<span data-ttu-id="2d058-135">String</span><span class="sxs-lookup"><span data-stu-id="2d058-135">String</span></span>|<span data-ttu-id="2d058-136">Nombre de la regla a la que se aplica esta acción programada.</span><span class="sxs-lookup"><span data-stu-id="2d058-136">Name of the rule which this scheduled action applies to.</span></span>|



## <a name="response"></a><span data-ttu-id="2d058-137">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d058-137">Response</span></span>
<span data-ttu-id="2d058-138">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="2d058-138">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="2d058-139">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="2d058-139">Example</span></span>
### <a name="request"></a><span data-ttu-id="2d058-140">Solicitud</span><span class="sxs-lookup"><span data-stu-id="2d058-140">Request</span></span>
<span data-ttu-id="2d058-141">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="2d058-141">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
Content-type: application/json
Content-length: 114

{
  "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
  "ruleName": "Rule Name value"
}
```

### <a name="response"></a><span data-ttu-id="2d058-142">Respuesta</span><span class="sxs-lookup"><span data-stu-id="2d058-142">Response</span></span>
<span data-ttu-id="2d058-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="2d058-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



