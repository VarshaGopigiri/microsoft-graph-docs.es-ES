---
title: Actualizar deviceCompliancePolicyDeviceStateSummary
description: Actualice las propiedades de un objeto deviceCompliancePolicyDeviceStateSummary.
ms.openlocfilehash: 0cf0fe68f87bfe92536a5e13684818dabad1b2bd
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27030355"
---
# <a name="update-devicecompliancepolicydevicestatesummary"></a><span data-ttu-id="0859c-103">Actualizar deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="0859c-103">Update deviceCompliancePolicyDeviceStateSummary</span></span>

> <span data-ttu-id="0859c-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="0859c-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="0859c-105">Actualice las propiedades de un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="0859c-105">Update the properties of a [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="0859c-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="0859c-106">Prerequisites</span></span>
<span data-ttu-id="0859c-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="0859c-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="0859c-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="0859c-109">Permission type</span></span>|<span data-ttu-id="0859c-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="0859c-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="0859c-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="0859c-111">Delegated (work or school account)</span></span>|<span data-ttu-id="0859c-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="0859c-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="0859c-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="0859c-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="0859c-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0859c-114">Not supported.</span></span>|
|<span data-ttu-id="0859c-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="0859c-115">Application</span></span>|<span data-ttu-id="0859c-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="0859c-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="0859c-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="0859c-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicyDeviceStateSummary
```

## <a name="request-headers"></a><span data-ttu-id="0859c-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="0859c-118">Request headers</span></span>
|<span data-ttu-id="0859c-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0859c-119">Header</span></span>|<span data-ttu-id="0859c-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0859c-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="0859c-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="0859c-121">Authorization</span></span>|<span data-ttu-id="0859c-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="0859c-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="0859c-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="0859c-123">Accept</span></span>|<span data-ttu-id="0859c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="0859c-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="0859c-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="0859c-125">Request body</span></span>
<span data-ttu-id="0859c-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="0859c-126">In the request body, supply a JSON representation for the [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) object.</span></span>

<span data-ttu-id="0859c-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="0859c-127">The following table shows the properties that are required when you create the [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span></span>

|<span data-ttu-id="0859c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0859c-128">Property</span></span>|<span data-ttu-id="0859c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="0859c-129">Type</span></span>|<span data-ttu-id="0859c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="0859c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="0859c-131">inGracePeriodCount</span><span class="sxs-lookup"><span data-stu-id="0859c-131">inGracePeriodCount</span></span>|<span data-ttu-id="0859c-132">Int32</span><span class="sxs-lookup"><span data-stu-id="0859c-132">Int32</span></span>|<span data-ttu-id="0859c-133">Número de dispositivos que se encuentran en el período de gracia</span><span class="sxs-lookup"><span data-stu-id="0859c-133">Number of devices that are in grace period</span></span>|
|<span data-ttu-id="0859c-134">configManagerCount</span><span class="sxs-lookup"><span data-stu-id="0859c-134">configManagerCount</span></span>|<span data-ttu-id="0859c-135">Int32</span><span class="sxs-lookup"><span data-stu-id="0859c-135">Int32</span></span>|<span data-ttu-id="0859c-136">Número de dispositivos cuyo cumplimiento lo administra System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="0859c-136">Number of devices that have compliance managed by System Center Configuration Manager</span></span>|
|<span data-ttu-id="0859c-137">id</span><span class="sxs-lookup"><span data-stu-id="0859c-137">id</span></span>|<span data-ttu-id="0859c-138">String</span><span class="sxs-lookup"><span data-stu-id="0859c-138">String</span></span>|<span data-ttu-id="0859c-139">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="0859c-139">Key of the entity.</span></span>|
|<span data-ttu-id="0859c-140">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="0859c-140">unknownDeviceCount</span></span>|<span data-ttu-id="0859c-141">Int32</span><span class="sxs-lookup"><span data-stu-id="0859c-141">Int32</span></span>|<span data-ttu-id="0859c-142">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="0859c-142">Number of unknown devices</span></span>|
|<span data-ttu-id="0859c-143">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="0859c-143">notApplicableDeviceCount</span></span>|<span data-ttu-id="0859c-144">Int32</span><span class="sxs-lookup"><span data-stu-id="0859c-144">Int32</span></span>|<span data-ttu-id="0859c-145">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="0859c-145">Number of not applicable devices</span></span>|
|<span data-ttu-id="0859c-146">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="0859c-146">compliantDeviceCount</span></span>|<span data-ttu-id="0859c-147">Int32</span><span class="sxs-lookup"><span data-stu-id="0859c-147">Int32</span></span>|<span data-ttu-id="0859c-148">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="0859c-148">Number of compliant devices</span></span>|
|<span data-ttu-id="0859c-149">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="0859c-149">remediatedDeviceCount</span></span>|<span data-ttu-id="0859c-150">Int32</span><span class="sxs-lookup"><span data-stu-id="0859c-150">Int32</span></span>|<span data-ttu-id="0859c-151">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="0859c-151">Number of remediated devices</span></span>|
|<span data-ttu-id="0859c-152">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="0859c-152">nonCompliantDeviceCount</span></span>|<span data-ttu-id="0859c-153">Int32</span><span class="sxs-lookup"><span data-stu-id="0859c-153">Int32</span></span>|<span data-ttu-id="0859c-154">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="0859c-154">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="0859c-155">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="0859c-155">errorDeviceCount</span></span>|<span data-ttu-id="0859c-156">Int32</span><span class="sxs-lookup"><span data-stu-id="0859c-156">Int32</span></span>|<span data-ttu-id="0859c-157">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="0859c-157">Number of error devices</span></span>|
|<span data-ttu-id="0859c-158">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="0859c-158">conflictDeviceCount</span></span>|<span data-ttu-id="0859c-159">Int32</span><span class="sxs-lookup"><span data-stu-id="0859c-159">Int32</span></span>|<span data-ttu-id="0859c-160">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="0859c-160">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="0859c-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0859c-161">Response</span></span>
<span data-ttu-id="0859c-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="0859c-162">If successful, this method returns a `200 OK` response code and an updated [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="0859c-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="0859c-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="0859c-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="0859c-164">Request</span></span>
<span data-ttu-id="0859c-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="0859c-165">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicyDeviceStateSummary
Content-type: application/json
Content-length: 349

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyDeviceStateSummary",
  "inGracePeriodCount": 2,
  "configManagerCount": 2,
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```

### <a name="response"></a><span data-ttu-id="0859c-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="0859c-166">Response</span></span>
<span data-ttu-id="0859c-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="0859c-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 398

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyDeviceStateSummary",
  "inGracePeriodCount": 2,
  "configManagerCount": 2,
  "id": "8c4de8a7-e8a7-8c4d-a7e8-4d8ca7e84d8c",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```


