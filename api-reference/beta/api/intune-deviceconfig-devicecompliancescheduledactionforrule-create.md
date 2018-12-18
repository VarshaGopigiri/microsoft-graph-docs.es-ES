---
title: Crear deviceComplianceScheduledActionForRule
description: Cree un objeto deviceComplianceScheduledActionForRule.
author: tfitzmac
ms.openlocfilehash: adc4e488d387c5f5087ded96e585a882ee424707
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27345832"
---
# <a name="create-devicecompliancescheduledactionforrule"></a><span data-ttu-id="0abc8-103">Crear deviceComplianceScheduledActionForRule</span><span class="sxs-lookup"><span data-stu-id="0abc8-103">Create deviceComplianceScheduledActionForRule</span></span>

> <span data-ttu-id="0abc8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="0abc8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="0abc8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="0abc8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="0abc8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0abc8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0abc8-107">Cree un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md).</span><span class="sxs-lookup"><span data-stu-id="0abc8-107">Create a new [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0abc8-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0abc8-108">Prerequisites</span></span>
<span data-ttu-id="0abc8-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0abc8-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0abc8-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0abc8-111">Permission type</span></span>|<span data-ttu-id="0abc8-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0abc8-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0abc8-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0abc8-113">Delegated (work or school account)</span></span>|<span data-ttu-id="0abc8-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0abc8-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0abc8-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0abc8-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0abc8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0abc8-116">Not supported.</span></span>|
|<span data-ttu-id="0abc8-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0abc8-117">Application</span></span>|<span data-ttu-id="0abc8-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0abc8-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0abc8-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0abc8-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule
```

## <a name="request-headers"></a><span data-ttu-id="0abc8-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0abc8-120">Request headers</span></span>
|<span data-ttu-id="0abc8-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0abc8-121">Header</span></span>|<span data-ttu-id="0abc8-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0abc8-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0abc8-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="0abc8-123">Authorization</span></span>|<span data-ttu-id="0abc8-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0abc8-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0abc8-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0abc8-125">Accept</span></span>|<span data-ttu-id="0abc8-126">application/json</span><span class="sxs-lookup"><span data-stu-id="0abc8-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0abc8-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0abc8-127">Request body</span></span>
<span data-ttu-id="0abc8-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceComplianceScheduledActionForRule.</span><span class="sxs-lookup"><span data-stu-id="0abc8-128">In the request body, supply a JSON representation for the deviceComplianceScheduledActionForRule object.</span></span>

<span data-ttu-id="0abc8-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceComplianceScheduledActionForRule.</span><span class="sxs-lookup"><span data-stu-id="0abc8-129">The following table shows the properties that are required when you create the deviceComplianceScheduledActionForRule.</span></span>

|<span data-ttu-id="0abc8-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0abc8-130">Property</span></span>|<span data-ttu-id="0abc8-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="0abc8-131">Type</span></span>|<span data-ttu-id="0abc8-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="0abc8-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0abc8-133">id</span><span class="sxs-lookup"><span data-stu-id="0abc8-133">id</span></span>|<span data-ttu-id="0abc8-134">String</span><span class="sxs-lookup"><span data-stu-id="0abc8-134">String</span></span>|<span data-ttu-id="0abc8-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0abc8-135">Key of the entity.</span></span>|
|<span data-ttu-id="0abc8-136">ruleName</span><span class="sxs-lookup"><span data-stu-id="0abc8-136">ruleName</span></span>|<span data-ttu-id="0abc8-137">String</span><span class="sxs-lookup"><span data-stu-id="0abc8-137">String</span></span>|<span data-ttu-id="0abc8-138">Nombre de la regla a la que se aplica esta acción programada.</span><span class="sxs-lookup"><span data-stu-id="0abc8-138">Name of the rule which this scheduled action applies to.</span></span>|



## <a name="response"></a><span data-ttu-id="0abc8-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0abc8-139">Response</span></span>
<span data-ttu-id="0abc8-140">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0abc8-140">If successful, this method returns a `201 Created` response code and a [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0abc8-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0abc8-141">Example</span></span>
### <a name="request"></a><span data-ttu-id="0abc8-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0abc8-142">Request</span></span>
<span data-ttu-id="0abc8-143">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0abc8-143">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/scheduledActionsForRule
Content-type: application/json
Content-length: 114

{
  "@odata.type": "#microsoft.graph.deviceComplianceScheduledActionForRule",
  "ruleName": "Rule Name value"
}
```

### <a name="response"></a><span data-ttu-id="0abc8-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0abc8-144">Response</span></span>
<span data-ttu-id="0abc8-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0abc8-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





