---
title: Actualizar deviceComplianceScheduledActionForRule
description: Actualice las propiedades de un objeto deviceComplianceScheduledActionForRule.
author: tfitzmac
ms.openlocfilehash: 811029446591b33ac38dad5e4a9aaca045d6e9dc
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27330845"
---
# <a name="update-devicecompliancescheduledactionforrule"></a><span data-ttu-id="9fe50-103">Actualizar deviceComplianceScheduledActionForRule</span><span class="sxs-lookup"><span data-stu-id="9fe50-103">Update deviceComplianceScheduledActionForRule</span></span>

> <span data-ttu-id="9fe50-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="9fe50-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="9fe50-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="9fe50-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="9fe50-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9fe50-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9fe50-107">Actualice las propiedades de un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="9fe50-107">Update the properties of a [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9fe50-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9fe50-108">Prerequisites</span></span>
<span data-ttu-id="9fe50-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9fe50-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9fe50-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9fe50-111">Permission type</span></span>|<span data-ttu-id="9fe50-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9fe50-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9fe50-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9fe50-113">Delegated (work or school account)</span></span>|<span data-ttu-id="9fe50-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9fe50-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9fe50-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9fe50-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9fe50-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9fe50-116">Not supported.</span></span>|
|<span data-ttu-id="9fe50-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9fe50-117">Application</span></span>|<span data-ttu-id="9fe50-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9fe50-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9fe50-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9fe50-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
```

## <a name="request-headers"></a><span data-ttu-id="9fe50-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9fe50-120">Request headers</span></span>
|<span data-ttu-id="9fe50-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fe50-121">Header</span></span>|<span data-ttu-id="9fe50-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9fe50-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9fe50-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="9fe50-123">Authorization</span></span>|<span data-ttu-id="9fe50-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9fe50-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9fe50-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9fe50-125">Accept</span></span>|<span data-ttu-id="9fe50-126">application/json</span><span class="sxs-lookup"><span data-stu-id="9fe50-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9fe50-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9fe50-127">Request body</span></span>
<span data-ttu-id="9fe50-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="9fe50-128">In the request body, supply a JSON representation for the [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>

<span data-ttu-id="9fe50-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="9fe50-129">The following table shows the properties that are required when you create the [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span></span>

|<span data-ttu-id="9fe50-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9fe50-130">Property</span></span>|<span data-ttu-id="9fe50-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="9fe50-131">Type</span></span>|<span data-ttu-id="9fe50-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fe50-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9fe50-133">id</span><span class="sxs-lookup"><span data-stu-id="9fe50-133">id</span></span>|<span data-ttu-id="9fe50-134">String</span><span class="sxs-lookup"><span data-stu-id="9fe50-134">String</span></span>|<span data-ttu-id="9fe50-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9fe50-135">Key of the entity.</span></span>|
|<span data-ttu-id="9fe50-136">ruleName</span><span class="sxs-lookup"><span data-stu-id="9fe50-136">ruleName</span></span>|<span data-ttu-id="9fe50-137">String</span><span class="sxs-lookup"><span data-stu-id="9fe50-137">String</span></span>|<span data-ttu-id="9fe50-138">Nombre de la regla a la que se aplica esta acción programada.</span><span class="sxs-lookup"><span data-stu-id="9fe50-138">Name of the rule which this scheduled action applies to.</span></span>|



## <a name="response"></a><span data-ttu-id="9fe50-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fe50-139">Response</span></span>
<span data-ttu-id="9fe50-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9fe50-140">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9fe50-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9fe50-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="9fe50-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9fe50-142">Request</span></span>
<span data-ttu-id="9fe50-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9fe50-143">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule/{deviceComplianceScheduledActionForRuleId}
Content-type: application/json
Content-length: 37

{
  "ruleName": "Rule Name value"
}
```

### <a name="response"></a><span data-ttu-id="9fe50-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9fe50-144">Response</span></span>
<span data-ttu-id="9fe50-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9fe50-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





