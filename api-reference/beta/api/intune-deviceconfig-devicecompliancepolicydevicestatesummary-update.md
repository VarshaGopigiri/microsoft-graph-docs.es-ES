---
title: Actualizar deviceCompliancePolicyDeviceStateSummary
description: Actualice las propiedades de un objeto deviceCompliancePolicyDeviceStateSummary.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 51f43fb99fbb53f42bca37cb9f9d4943aa4635a0
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817442"
---
# <a name="update-devicecompliancepolicydevicestatesummary"></a><span data-ttu-id="ff289-103">Actualizar deviceCompliancePolicyDeviceStateSummary</span><span class="sxs-lookup"><span data-stu-id="ff289-103">Update deviceCompliancePolicyDeviceStateSummary</span></span>

> <span data-ttu-id="ff289-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ff289-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ff289-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ff289-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ff289-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ff289-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ff289-107">Actualice las propiedades de un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="ff289-107">Update the properties of a [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="ff289-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="ff289-108">Prerequisites</span></span>
<span data-ttu-id="ff289-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="ff289-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="ff289-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="ff289-111">Permission type</span></span>|<span data-ttu-id="ff289-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="ff289-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="ff289-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="ff289-113">Delegated (work or school account)</span></span>|<span data-ttu-id="ff289-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="ff289-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="ff289-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="ff289-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="ff289-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff289-116">Not supported.</span></span>|
|<span data-ttu-id="ff289-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="ff289-117">Application</span></span>|<span data-ttu-id="ff289-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="ff289-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="ff289-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="ff289-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicyDeviceStateSummary
```

## <a name="request-headers"></a><span data-ttu-id="ff289-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="ff289-120">Request headers</span></span>
|<span data-ttu-id="ff289-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ff289-121">Header</span></span>|<span data-ttu-id="ff289-122">Valor</span><span class="sxs-lookup"><span data-stu-id="ff289-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="ff289-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="ff289-123">Authorization</span></span>|<span data-ttu-id="ff289-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="ff289-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="ff289-125">Accept</span><span class="sxs-lookup"><span data-stu-id="ff289-125">Accept</span></span>|<span data-ttu-id="ff289-126">application/json</span><span class="sxs-lookup"><span data-stu-id="ff289-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="ff289-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="ff289-127">Request body</span></span>
<span data-ttu-id="ff289-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="ff289-128">In the request body, supply a JSON representation for the [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) object.</span></span>

<span data-ttu-id="ff289-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="ff289-129">The following table shows the properties that are required when you create the [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md).</span></span>

|<span data-ttu-id="ff289-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ff289-130">Property</span></span>|<span data-ttu-id="ff289-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="ff289-131">Type</span></span>|<span data-ttu-id="ff289-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="ff289-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ff289-133">inGracePeriodCount</span><span class="sxs-lookup"><span data-stu-id="ff289-133">inGracePeriodCount</span></span>|<span data-ttu-id="ff289-134">Int32</span><span class="sxs-lookup"><span data-stu-id="ff289-134">Int32</span></span>|<span data-ttu-id="ff289-135">Número de dispositivos que se encuentran en el período de gracia</span><span class="sxs-lookup"><span data-stu-id="ff289-135">Number of devices that are in grace period</span></span>|
|<span data-ttu-id="ff289-136">configManagerCount</span><span class="sxs-lookup"><span data-stu-id="ff289-136">configManagerCount</span></span>|<span data-ttu-id="ff289-137">Int32</span><span class="sxs-lookup"><span data-stu-id="ff289-137">Int32</span></span>|<span data-ttu-id="ff289-138">Número de dispositivos cuyo cumplimiento lo administra System Center Configuration Manager</span><span class="sxs-lookup"><span data-stu-id="ff289-138">Number of devices that have compliance managed by System Center Configuration Manager</span></span>|
|<span data-ttu-id="ff289-139">id</span><span class="sxs-lookup"><span data-stu-id="ff289-139">id</span></span>|<span data-ttu-id="ff289-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="ff289-140">String</span></span>|<span data-ttu-id="ff289-141">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="ff289-141">Key of the entity.</span></span>|
|<span data-ttu-id="ff289-142">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ff289-142">unknownDeviceCount</span></span>|<span data-ttu-id="ff289-143">Int32</span><span class="sxs-lookup"><span data-stu-id="ff289-143">Int32</span></span>|<span data-ttu-id="ff289-144">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="ff289-144">Number of unknown devices</span></span>|
|<span data-ttu-id="ff289-145">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ff289-145">notApplicableDeviceCount</span></span>|<span data-ttu-id="ff289-146">Int32</span><span class="sxs-lookup"><span data-stu-id="ff289-146">Int32</span></span>|<span data-ttu-id="ff289-147">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="ff289-147">Number of not applicable devices</span></span>|
|<span data-ttu-id="ff289-148">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ff289-148">compliantDeviceCount</span></span>|<span data-ttu-id="ff289-149">Int32</span><span class="sxs-lookup"><span data-stu-id="ff289-149">Int32</span></span>|<span data-ttu-id="ff289-150">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="ff289-150">Number of compliant devices</span></span>|
|<span data-ttu-id="ff289-151">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ff289-151">remediatedDeviceCount</span></span>|<span data-ttu-id="ff289-152">Int32</span><span class="sxs-lookup"><span data-stu-id="ff289-152">Int32</span></span>|<span data-ttu-id="ff289-153">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="ff289-153">Number of remediated devices</span></span>|
|<span data-ttu-id="ff289-154">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ff289-154">nonCompliantDeviceCount</span></span>|<span data-ttu-id="ff289-155">Int32</span><span class="sxs-lookup"><span data-stu-id="ff289-155">Int32</span></span>|<span data-ttu-id="ff289-156">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="ff289-156">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="ff289-157">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ff289-157">errorDeviceCount</span></span>|<span data-ttu-id="ff289-158">Int32</span><span class="sxs-lookup"><span data-stu-id="ff289-158">Int32</span></span>|<span data-ttu-id="ff289-159">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="ff289-159">Number of error devices</span></span>|
|<span data-ttu-id="ff289-160">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="ff289-160">conflictDeviceCount</span></span>|<span data-ttu-id="ff289-161">Int32</span><span class="sxs-lookup"><span data-stu-id="ff289-161">Int32</span></span>|<span data-ttu-id="ff289-162">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="ff289-162">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="ff289-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff289-163">Response</span></span>
<span data-ttu-id="ff289-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="ff289-164">If successful, this method returns a `200 OK` response code and an updated [deviceCompliancePolicyDeviceStateSummary](../resources/intune-deviceconfig-devicecompliancepolicydevicestatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="ff289-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ff289-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="ff289-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="ff289-166">Request</span></span>
<span data-ttu-id="ff289-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="ff289-167">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="ff289-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="ff289-168">Response</span></span>
<span data-ttu-id="ff289-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="ff289-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





