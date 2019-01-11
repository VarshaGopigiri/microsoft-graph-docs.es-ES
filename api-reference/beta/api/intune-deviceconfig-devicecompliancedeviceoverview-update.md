---
title: Actualizar deviceComplianceDeviceOverview
description: Actualice las propiedades de un objeto deviceComplianceDeviceOverview.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 1bcbcd81d70eb01613d33a9acf44737ae9519583
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27882106"
---
# <a name="update-devicecompliancedeviceoverview"></a><span data-ttu-id="b6e57-103">Actualizar deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="b6e57-103">Update deviceComplianceDeviceOverview</span></span>

> <span data-ttu-id="b6e57-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b6e57-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b6e57-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b6e57-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="b6e57-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b6e57-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b6e57-107">Actualice las propiedades de un objeto [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b6e57-107">Update the properties of a [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b6e57-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b6e57-108">Prerequisites</span></span>
<span data-ttu-id="b6e57-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b6e57-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b6e57-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b6e57-111">Permission type</span></span>|<span data-ttu-id="b6e57-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b6e57-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b6e57-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b6e57-113">Delegated (work or school account)</span></span>|<span data-ttu-id="b6e57-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b6e57-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b6e57-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b6e57-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b6e57-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6e57-116">Not supported.</span></span>|
|<span data-ttu-id="b6e57-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b6e57-117">Application</span></span>|<span data-ttu-id="b6e57-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b6e57-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b6e57-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b6e57-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatusOverview
```

## <a name="request-headers"></a><span data-ttu-id="b6e57-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b6e57-120">Request headers</span></span>
|<span data-ttu-id="b6e57-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6e57-121">Header</span></span>|<span data-ttu-id="b6e57-122">Valor</span><span class="sxs-lookup"><span data-stu-id="b6e57-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b6e57-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="b6e57-123">Authorization</span></span>|<span data-ttu-id="b6e57-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b6e57-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b6e57-125">Accept</span><span class="sxs-lookup"><span data-stu-id="b6e57-125">Accept</span></span>|<span data-ttu-id="b6e57-126">application/json</span><span class="sxs-lookup"><span data-stu-id="b6e57-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b6e57-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b6e57-127">Request body</span></span>
<span data-ttu-id="b6e57-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b6e57-128">In the request body, supply a JSON representation for the [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md) object.</span></span>

<span data-ttu-id="b6e57-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b6e57-129">The following table shows the properties that are required when you create the [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md).</span></span>

|<span data-ttu-id="b6e57-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b6e57-130">Property</span></span>|<span data-ttu-id="b6e57-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6e57-131">Type</span></span>|<span data-ttu-id="b6e57-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6e57-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b6e57-133">id</span><span class="sxs-lookup"><span data-stu-id="b6e57-133">id</span></span>|<span data-ttu-id="b6e57-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="b6e57-134">String</span></span>|<span data-ttu-id="b6e57-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b6e57-135">Key of the entity.</span></span>|
|<span data-ttu-id="b6e57-136">pendingCount</span><span class="sxs-lookup"><span data-stu-id="b6e57-136">pendingCount</span></span>|<span data-ttu-id="b6e57-137">Int32</span><span class="sxs-lookup"><span data-stu-id="b6e57-137">Int32</span></span>|<span data-ttu-id="b6e57-138">Número de dispositivos pendientes</span><span class="sxs-lookup"><span data-stu-id="b6e57-138">Number of pending devices</span></span>|
|<span data-ttu-id="b6e57-139">notApplicableCount</span><span class="sxs-lookup"><span data-stu-id="b6e57-139">notApplicableCount</span></span>|<span data-ttu-id="b6e57-140">Int32</span><span class="sxs-lookup"><span data-stu-id="b6e57-140">Int32</span></span>|<span data-ttu-id="b6e57-141">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="b6e57-141">Number of not applicable devices</span></span>|
|<span data-ttu-id="b6e57-142">notApplicablePlatformCount</span><span class="sxs-lookup"><span data-stu-id="b6e57-142">notApplicablePlatformCount</span></span>|<span data-ttu-id="b6e57-143">Int32</span><span class="sxs-lookup"><span data-stu-id="b6e57-143">Int32</span></span>|<span data-ttu-id="b6e57-144">Número de dispositivos no aplicables debido a la plataforma de error de coincidencia y la directiva</span><span class="sxs-lookup"><span data-stu-id="b6e57-144">Number of not applicable devices due to mismatch platform and policy</span></span>|
|<span data-ttu-id="b6e57-145">successCount</span><span class="sxs-lookup"><span data-stu-id="b6e57-145">successCount</span></span>|<span data-ttu-id="b6e57-146">Int32</span><span class="sxs-lookup"><span data-stu-id="b6e57-146">Int32</span></span>|<span data-ttu-id="b6e57-147">Número de dispositivos correctos</span><span class="sxs-lookup"><span data-stu-id="b6e57-147">Number of succeeded devices</span></span>|
|<span data-ttu-id="b6e57-148">errorCount</span><span class="sxs-lookup"><span data-stu-id="b6e57-148">errorCount</span></span>|<span data-ttu-id="b6e57-149">Int32</span><span class="sxs-lookup"><span data-stu-id="b6e57-149">Int32</span></span>|<span data-ttu-id="b6e57-150">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="b6e57-150">Number of error devices</span></span>|
|<span data-ttu-id="b6e57-151">failedCount</span><span class="sxs-lookup"><span data-stu-id="b6e57-151">failedCount</span></span>|<span data-ttu-id="b6e57-152">Int32</span><span class="sxs-lookup"><span data-stu-id="b6e57-152">Int32</span></span>|<span data-ttu-id="b6e57-153">Número de dispositivos erróneos</span><span class="sxs-lookup"><span data-stu-id="b6e57-153">Number of failed devices</span></span>|
|<span data-ttu-id="b6e57-154">conflictCount</span><span class="sxs-lookup"><span data-stu-id="b6e57-154">conflictCount</span></span>|<span data-ttu-id="b6e57-155">Int32</span><span class="sxs-lookup"><span data-stu-id="b6e57-155">Int32</span></span>|<span data-ttu-id="b6e57-156">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="b6e57-156">Number of devices in conflict</span></span>|
|<span data-ttu-id="b6e57-157">lastUpdateDateTime</span><span class="sxs-lookup"><span data-stu-id="b6e57-157">lastUpdateDateTime</span></span>|<span data-ttu-id="b6e57-158">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="b6e57-158">DateTimeOffset</span></span>|<span data-ttu-id="b6e57-159">Última hora de actualización</span><span class="sxs-lookup"><span data-stu-id="b6e57-159">Last update time</span></span>|
|<span data-ttu-id="b6e57-160">configurationVersion</span><span class="sxs-lookup"><span data-stu-id="b6e57-160">configurationVersion</span></span>|<span data-ttu-id="b6e57-161">Int32</span><span class="sxs-lookup"><span data-stu-id="b6e57-161">Int32</span></span>|<span data-ttu-id="b6e57-162">Versión de la directiva para esa información general</span><span class="sxs-lookup"><span data-stu-id="b6e57-162">Version of the policy for that overview</span></span>|



## <a name="response"></a><span data-ttu-id="b6e57-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6e57-163">Response</span></span>
<span data-ttu-id="b6e57-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b6e57-164">If successful, this method returns a `200 OK` response code and an updated [deviceComplianceDeviceOverview](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b6e57-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b6e57-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="b6e57-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b6e57-166">Request</span></span>
<span data-ttu-id="b6e57-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b6e57-167">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceStatusOverview
Content-type: application/json
Content-length: 273

{
  "pendingCount": 12,
  "notApplicableCount": 2,
  "notApplicablePlatformCount": 10,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "conflictCount": 13,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```

### <a name="response"></a><span data-ttu-id="b6e57-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b6e57-168">Response</span></span>
<span data-ttu-id="b6e57-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b6e57-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 391

{
  "@odata.type": "#microsoft.graph.deviceComplianceDeviceOverview",
  "id": "886f167b-167b-886f-7b16-6f887b166f88",
  "pendingCount": 12,
  "notApplicableCount": 2,
  "notApplicablePlatformCount": 10,
  "successCount": 12,
  "errorCount": 10,
  "failedCount": 11,
  "conflictCount": 13,
  "lastUpdateDateTime": "2016-12-31T23:58:21.6459442-08:00",
  "configurationVersion": 4
}
```





