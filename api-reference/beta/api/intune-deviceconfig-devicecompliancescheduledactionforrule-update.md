---
title: Actualizar deviceComplianceScheduledActionForRule
description: Actualice las propiedades de un objeto deviceComplianceScheduledActionForRule.
ms.openlocfilehash: 5d5c3d886959873744bdaecdc538b7f142d66665
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090375"
---
# <a name="update-devicecompliancescheduledactionforrule"></a><span data-ttu-id="8810d-103">Actualizar deviceComplianceScheduledActionForRule</span><span class="sxs-lookup"><span data-stu-id="8810d-103">Update deviceComplianceScheduledActionForRule</span></span>

> <span data-ttu-id="8810d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8810d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8810d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8810d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="8810d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="8810d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="8810d-107">Actualice las propiedades de un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="8810d-107">Update the properties of a [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="8810d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8810d-108">Prerequisites</span></span>
<span data-ttu-id="8810d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="8810d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="8810d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="8810d-111">Permission type</span></span>|<span data-ttu-id="8810d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="8810d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="8810d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="8810d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="8810d-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="8810d-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="8810d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="8810d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="8810d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8810d-116">Not supported.</span></span>|
|<span data-ttu-id="8810d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="8810d-117">Application</span></span>|<span data-ttu-id="8810d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="8810d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="8810d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="8810d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
```

## <a name="request-headers"></a><span data-ttu-id="8810d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="8810d-120">Request headers</span></span>
|<span data-ttu-id="8810d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8810d-121">Header</span></span>|<span data-ttu-id="8810d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="8810d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="8810d-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="8810d-123">Authorization</span></span>|<span data-ttu-id="8810d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="8810d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="8810d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="8810d-125">Accept</span></span>|<span data-ttu-id="8810d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="8810d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="8810d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="8810d-127">Request body</span></span>
<span data-ttu-id="8810d-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="8810d-128">In the request body, supply a JSON representation for the [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>

<span data-ttu-id="8810d-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="8810d-129">The following table shows the properties that are required when you create the [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span></span>

|<span data-ttu-id="8810d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8810d-130">Property</span></span>|<span data-ttu-id="8810d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="8810d-131">Type</span></span>|<span data-ttu-id="8810d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8810d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="8810d-133">id</span><span class="sxs-lookup"><span data-stu-id="8810d-133">id</span></span>|<span data-ttu-id="8810d-134">String</span><span class="sxs-lookup"><span data-stu-id="8810d-134">String</span></span>|<span data-ttu-id="8810d-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="8810d-135">Key of the entity.</span></span>|
|<span data-ttu-id="8810d-136">ruleName</span><span class="sxs-lookup"><span data-stu-id="8810d-136">ruleName</span></span>|<span data-ttu-id="8810d-137">String</span><span class="sxs-lookup"><span data-stu-id="8810d-137">String</span></span>|<span data-ttu-id="8810d-138">Nombre de la regla a la que se aplica esta acción programada.</span><span class="sxs-lookup"><span data-stu-id="8810d-138">Name of the rule which this scheduled action applies to.</span></span>|



## <a name="response"></a><span data-ttu-id="8810d-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8810d-139">Response</span></span>
<span data-ttu-id="8810d-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="8810d-140">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="8810d-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8810d-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="8810d-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="8810d-142">Request</span></span>
<span data-ttu-id="8810d-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="8810d-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
Content-type: application/json
Content-length: 37

{
  "ruleName": "Rule Name value"
}
```

### <a name="response"></a><span data-ttu-id="8810d-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8810d-144">Response</span></span>
<span data-ttu-id="8810d-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="8810d-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





