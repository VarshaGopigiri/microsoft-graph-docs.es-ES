---
title: Actualizar deviceComplianceDeviceOverview
description: Actualice las propiedades de un objeto deviceComplianceDeviceOverview.
ms.openlocfilehash: 7fdbfb50bf6f0463436376e39541b35364ded5bf
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030255"
---
# <a name="update-devicecompliancedeviceoverview"></a><span data-ttu-id="f57a8-103">Actualizar deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="f57a8-103">Update deviceComplianceDeviceOverview</span></span>

> <span data-ttu-id="f57a8-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f57a8-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f57a8-105">Actualice las propiedades de un objeto [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f57a8-105">Update the properties of a [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f57a8-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f57a8-106">Prerequisites</span></span>
<span data-ttu-id="f57a8-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f57a8-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f57a8-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f57a8-109">Permission type</span></span>|<span data-ttu-id="f57a8-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f57a8-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f57a8-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f57a8-111">Delegated (work or school account)</span></span>|<span data-ttu-id="f57a8-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f57a8-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="f57a8-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f57a8-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f57a8-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f57a8-114">Not supported.</span></span>|
|<span data-ttu-id="f57a8-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f57a8-115">Application</span></span>|<span data-ttu-id="f57a8-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f57a8-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f57a8-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f57a8-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatusOverview
```

## <a name="request-headers"></a><span data-ttu-id="f57a8-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f57a8-118">Request headers</span></span>
|<span data-ttu-id="f57a8-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f57a8-119">Header</span></span>|<span data-ttu-id="f57a8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f57a8-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f57a8-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="f57a8-121">Authorization</span></span>|<span data-ttu-id="f57a8-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f57a8-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f57a8-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f57a8-123">Accept</span></span>|<span data-ttu-id="f57a8-124">application/json</span><span class="sxs-lookup"><span data-stu-id="f57a8-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f57a8-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f57a8-125">Request body</span></span>
<span data-ttu-id="f57a8-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f57a8-126">In the request body, supply a JSON representation for the [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md) object.</span></span>

<span data-ttu-id="f57a8-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f57a8-127">The following table shows the properties that are required when you create the [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md).</span></span>

|<span data-ttu-id="f57a8-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f57a8-128">Property</span></span>|<span data-ttu-id="f57a8-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f57a8-129">Type</span></span>|<span data-ttu-id="f57a8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f57a8-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f57a8-131">id</span><span class="sxs-lookup"><span data-stu-id="f57a8-131">id</span></span>|<span data-ttu-id="f57a8-132">String</span><span class="sxs-lookup"><span data-stu-id="f57a8-132">String</span></span>|<span data-ttu-id="f57a8-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f57a8-133">Key of the entity.</span></span>|
|<span data-ttu-id="f57a8-134">pendingCount</span><span class="sxs-lookup"><span data-stu-id="f57a8-134">pendingCount</span></span>|<span data-ttu-id="f57a8-135">Int32</span><span class="sxs-lookup"><span data-stu-id="f57a8-135">Int32</span></span>|<span data-ttu-id="f57a8-136">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="f57a8-136">Number of pending devices</span></span>|
|<span data-ttu-id="f57a8-137">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="f57a8-137">notApplicableCount</span></span>|<span data-ttu-id="f57a8-138">Int32</span><span class="sxs-lookup"><span data-stu-id="f57a8-138">Int32</span></span>|<span data-ttu-id="f57a8-139">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="f57a8-139">Number of not applicable devices</span></span>|
|<span data-ttu-id="f57a8-140">successCount</span><span class="sxs-lookup"><span data-stu-id="f57a8-140">successCount</span></span>|<span data-ttu-id="f57a8-141">Int32</span><span class="sxs-lookup"><span data-stu-id="f57a8-141">Int32</span></span>|<span data-ttu-id="f57a8-142">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="f57a8-142">Number of succeeded devices</span></span>|
|<span data-ttu-id="f57a8-143">errorCount</span><span class="sxs-lookup"><span data-stu-id="f57a8-143">errorCount</span></span>|<span data-ttu-id="f57a8-144">Int32</span><span class="sxs-lookup"><span data-stu-id="f57a8-144">Int32</span></span>|<span data-ttu-id="f57a8-145">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="f57a8-145">Number of error devices</span></span>|
|<span data-ttu-id="f57a8-146">failedCount</span><span class="sxs-lookup"><span data-stu-id="f57a8-146">failedCount</span></span>|<span data-ttu-id="f57a8-147">Int32</span><span class="sxs-lookup"><span data-stu-id="f57a8-147">Int32</span></span>|<span data-ttu-id="f57a8-148">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="f57a8-148">Number of failed devices</span></span>|
|<span data-ttu-id="f57a8-149">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="f57a8-149">lastUpdateDateTime</span></span>|<span data-ttu-id="f57a8-150">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f57a8-150">DateTimeOffset</span></span>|<span data-ttu-id="f57a8-151">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="f57a8-151">Last update time</span></span>|
|<span data-ttu-id="f57a8-152">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="f57a8-152">configurationVersion</span></span>|<span data-ttu-id="f57a8-153">Int32</span><span class="sxs-lookup"><span data-stu-id="f57a8-153">Int32</span></span>|<span data-ttu-id="f57a8-154">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="f57a8-154">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="f57a8-155">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f57a8-155">Response</span></span>
<span data-ttu-id="f57a8-156">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f57a8-156">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f57a8-157">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f57a8-157">Example</span></span>
### <a name="request"></a><span data-ttu-id="f57a8-158">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f57a8-158">Request</span></span>
<span data-ttu-id="f57a8-159">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f57a8-159">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatusOverview
Content-type: application/json
Content-length: 281

{
  "@odata.type": "#microsoft.graph.deviceComplianceDeviceOverview",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```

### <a name="response"></a><span data-ttu-id="f57a8-160">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f57a8-160">Response</span></span>
<span data-ttu-id="f57a8-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f57a8-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 330

{
  "@odata.type": "#microsoft.graph.deviceComplianceDeviceOverview",
  "id": "886f167b-167b-886f-7b16-6f887b166f88",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```


