---
title: Actualizar deviceCompliancePolicyDeviceStateSummary
description: Actualice las propiedades de un objeto deviceCompliancePolicyDeviceStateSummary.
ms.openlocfilehash: 045c9ac7aaecac535f3c4d04f587c74cbe84f442
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086803"
---
# <a name="update-devicecompliancepolicydevicestatesummary"></a><span data-ttu-id="38a82-103">Actualizar deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="38a82-103">Update deviceCompliancePolicyDeviceStateSummary</span></span>

> <span data-ttu-id="38a82-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="38a82-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="38a82-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="38a82-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="38a82-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="38a82-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="38a82-107">Actualice las propiedades de un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="38a82-107">Update the properties of a [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="38a82-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="38a82-108">Prerequisites</span></span>
<span data-ttu-id="38a82-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="38a82-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="38a82-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="38a82-111">Permission type</span></span>|<span data-ttu-id="38a82-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="38a82-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="38a82-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="38a82-113">Delegated (work or school account)</span></span>|<span data-ttu-id="38a82-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="38a82-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="38a82-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="38a82-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="38a82-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38a82-116">Not supported.</span></span>|
|<span data-ttu-id="38a82-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="38a82-117">Application</span></span>|<span data-ttu-id="38a82-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="38a82-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="38a82-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="38a82-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicyDeviceStateSummary
```

## <a name="request-headers"></a><span data-ttu-id="38a82-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="38a82-120">Request headers</span></span>
|<span data-ttu-id="38a82-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38a82-121">Header</span></span>|<span data-ttu-id="38a82-122">Valor</span><span class="sxs-lookup"><span data-stu-id="38a82-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="38a82-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="38a82-123">Authorization</span></span>|<span data-ttu-id="38a82-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="38a82-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="38a82-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="38a82-125">Accept</span></span>|<span data-ttu-id="38a82-126">application/json</span><span class="sxs-lookup"><span data-stu-id="38a82-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="38a82-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="38a82-127">Request body</span></span>
<span data-ttu-id="38a82-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="38a82-128">In the request body, supply a JSON representation for the [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) object.</span></span>

<span data-ttu-id="38a82-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="38a82-129">The following table shows the properties that are required when you create the [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span></span>

|<span data-ttu-id="38a82-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="38a82-130">Property</span></span>|<span data-ttu-id="38a82-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="38a82-131">Type</span></span>|<span data-ttu-id="38a82-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="38a82-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="38a82-133">inGracePeriodCount</span><span class="sxs-lookup"><span data-stu-id="38a82-133">inGracePeriodCount</span></span>|<span data-ttu-id="38a82-134">Int32</span><span class="sxs-lookup"><span data-stu-id="38a82-134">Int32</span></span>|<span data-ttu-id="38a82-135">Número de dispositivos que se encuentran en el período de gracia</span><span class="sxs-lookup"><span data-stu-id="38a82-135">Number of devices that are in grace period</span></span>|
|<span data-ttu-id="38a82-136">configManagerCount</span><span class="sxs-lookup"><span data-stu-id="38a82-136">configManagerCount</span></span>|<span data-ttu-id="38a82-137">Int32</span><span class="sxs-lookup"><span data-stu-id="38a82-137">Int32</span></span>|<span data-ttu-id="38a82-138">Número de dispositivos cuyo cumplimiento lo administra System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="38a82-138">Number of devices that have compliance managed by System Center Configuration Manager</span></span>|
|<span data-ttu-id="38a82-139">id</span><span class="sxs-lookup"><span data-stu-id="38a82-139">id</span></span>|<span data-ttu-id="38a82-140">String</span><span class="sxs-lookup"><span data-stu-id="38a82-140">String</span></span>|<span data-ttu-id="38a82-141">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="38a82-141">Key of the entity.</span></span>|
|<span data-ttu-id="38a82-142">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38a82-142">unknownDeviceCount</span></span>|<span data-ttu-id="38a82-143">Int32</span><span class="sxs-lookup"><span data-stu-id="38a82-143">Int32</span></span>|<span data-ttu-id="38a82-144">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="38a82-144">Number of unknown devices</span></span>|
|<span data-ttu-id="38a82-145">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38a82-145">notApplicableDeviceCount</span></span>|<span data-ttu-id="38a82-146">Int32</span><span class="sxs-lookup"><span data-stu-id="38a82-146">Int32</span></span>|<span data-ttu-id="38a82-147">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="38a82-147">Number of not applicable devices</span></span>|
|<span data-ttu-id="38a82-148">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38a82-148">compliantDeviceCount</span></span>|<span data-ttu-id="38a82-149">Int32</span><span class="sxs-lookup"><span data-stu-id="38a82-149">Int32</span></span>|<span data-ttu-id="38a82-150">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="38a82-150">Number of compliant devices</span></span>|
|<span data-ttu-id="38a82-151">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38a82-151">remediatedDeviceCount</span></span>|<span data-ttu-id="38a82-152">Int32</span><span class="sxs-lookup"><span data-stu-id="38a82-152">Int32</span></span>|<span data-ttu-id="38a82-153">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="38a82-153">Number of remediated devices</span></span>|
|<span data-ttu-id="38a82-154">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38a82-154">nonCompliantDeviceCount</span></span>|<span data-ttu-id="38a82-155">Int32</span><span class="sxs-lookup"><span data-stu-id="38a82-155">Int32</span></span>|<span data-ttu-id="38a82-156">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="38a82-156">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="38a82-157">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38a82-157">errorDeviceCount</span></span>|<span data-ttu-id="38a82-158">Int32</span><span class="sxs-lookup"><span data-stu-id="38a82-158">Int32</span></span>|<span data-ttu-id="38a82-159">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="38a82-159">Number of error devices</span></span>|
|<span data-ttu-id="38a82-160">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="38a82-160">conflictDeviceCount</span></span>|<span data-ttu-id="38a82-161">Int32</span><span class="sxs-lookup"><span data-stu-id="38a82-161">Int32</span></span>|<span data-ttu-id="38a82-162">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="38a82-162">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="38a82-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38a82-163">Response</span></span>
<span data-ttu-id="38a82-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="38a82-164">If successful, this method returns a `200 OK` response code and an updated [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="38a82-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38a82-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="38a82-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="38a82-166">Request</span></span>
<span data-ttu-id="38a82-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="38a82-167">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicyDeviceStateSummary
Content-type: application/json
Content-length: 270

{
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

### <a name="response"></a><span data-ttu-id="38a82-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="38a82-168">Response</span></span>
<span data-ttu-id="38a82-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="38a82-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





