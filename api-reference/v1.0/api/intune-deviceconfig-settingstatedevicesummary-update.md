---
title: Actualizar settingStateDeviceSummary
description: Actualice las propiedades de un objeto settingStateDeviceSummary.
ms.openlocfilehash: 18d4687714893b862bbd89f5d72f4018f5ef9a11
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031410"
---
# <a name="update-settingstatedevicesummary"></a><span data-ttu-id="a5408-103">Actualizar settingStateDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="a5408-103">Update settingStateDeviceSummary</span></span>

> <span data-ttu-id="a5408-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a5408-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a5408-105">Actualice las propiedades de un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="a5408-105">Update the properties of a [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a5408-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a5408-106">Prerequisites</span></span>
<span data-ttu-id="a5408-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a5408-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a5408-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a5408-109">Permission type</span></span>|<span data-ttu-id="a5408-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a5408-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a5408-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a5408-111">Delegated (work or school account)</span></span>|<span data-ttu-id="a5408-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a5408-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="a5408-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a5408-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a5408-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5408-114">Not supported.</span></span>|
|<span data-ttu-id="a5408-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a5408-115">Application</span></span>|<span data-ttu-id="a5408-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a5408-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a5408-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a5408-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="a5408-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a5408-118">Request headers</span></span>
|<span data-ttu-id="a5408-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5408-119">Header</span></span>|<span data-ttu-id="a5408-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a5408-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a5408-121">Authorization</span><span class="sxs-lookup"><span data-stu-id="a5408-121">Authorization</span></span>|<span data-ttu-id="a5408-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a5408-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a5408-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="a5408-123">Accept</span></span>|<span data-ttu-id="a5408-124">application/json</span><span class="sxs-lookup"><span data-stu-id="a5408-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a5408-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a5408-125">Request body</span></span>
<span data-ttu-id="a5408-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="a5408-126">In the request body, supply a JSON representation for the [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object.</span></span>

<span data-ttu-id="a5408-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="a5408-127">The following table shows the properties that are required when you create the [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span></span>

|<span data-ttu-id="a5408-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a5408-128">Property</span></span>|<span data-ttu-id="a5408-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="a5408-129">Type</span></span>|<span data-ttu-id="a5408-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="a5408-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a5408-131">id</span><span class="sxs-lookup"><span data-stu-id="a5408-131">id</span></span>|<span data-ttu-id="a5408-132">String</span><span class="sxs-lookup"><span data-stu-id="a5408-132">String</span></span>|<span data-ttu-id="a5408-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a5408-133">Key of the entity.</span></span>|
|<span data-ttu-id="a5408-134">settingName</span><span class="sxs-lookup"><span data-stu-id="a5408-134">settingName</span></span>|<span data-ttu-id="a5408-135">String</span><span class="sxs-lookup"><span data-stu-id="a5408-135">String</span></span>|<span data-ttu-id="a5408-136">Nombre de la configuración</span><span class="sxs-lookup"><span data-stu-id="a5408-136">Name of the setting</span></span>|
|<span data-ttu-id="a5408-137">instancePath</span><span class="sxs-lookup"><span data-stu-id="a5408-137">instancePath</span></span>|<span data-ttu-id="a5408-138">String</span><span class="sxs-lookup"><span data-stu-id="a5408-138">String</span></span>|<span data-ttu-id="a5408-139">Nombre de InstancePath para la configuración</span><span class="sxs-lookup"><span data-stu-id="a5408-139">Name of the InstancePath for the setting</span></span>|
|<span data-ttu-id="a5408-140">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a5408-140">unknownDeviceCount</span></span>|<span data-ttu-id="a5408-141">Int32</span><span class="sxs-lookup"><span data-stu-id="a5408-141">Int32</span></span>|<span data-ttu-id="a5408-142">Número de dispositivos desconocido para la configuración</span><span class="sxs-lookup"><span data-stu-id="a5408-142">Device Unkown count for the setting</span></span>|
|<span data-ttu-id="a5408-143">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a5408-143">notApplicableDeviceCount</span></span>|<span data-ttu-id="a5408-144">Int32</span><span class="sxs-lookup"><span data-stu-id="a5408-144">Int32</span></span>|<span data-ttu-id="a5408-145">Número de dispositivos no aplicables para la configuración</span><span class="sxs-lookup"><span data-stu-id="a5408-145">Device Not Applicable count for the setting</span></span>|
|<span data-ttu-id="a5408-146">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a5408-146">compliantDeviceCount</span></span>|<span data-ttu-id="a5408-147">Int32</span><span class="sxs-lookup"><span data-stu-id="a5408-147">Int32</span></span>|<span data-ttu-id="a5408-148">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="a5408-148">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="a5408-149">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a5408-149">remediatedDeviceCount</span></span>|<span data-ttu-id="a5408-150">Int32</span><span class="sxs-lookup"><span data-stu-id="a5408-150">Int32</span></span>|<span data-ttu-id="a5408-151">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="a5408-151">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="a5408-152">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a5408-152">nonCompliantDeviceCount</span></span>|<span data-ttu-id="a5408-153">Int32</span><span class="sxs-lookup"><span data-stu-id="a5408-153">Int32</span></span>|<span data-ttu-id="a5408-154">Número de dispositivos no compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="a5408-154">Device NonCompliant count for the setting</span></span>|
|<span data-ttu-id="a5408-155">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a5408-155">errorDeviceCount</span></span>|<span data-ttu-id="a5408-156">Int32</span><span class="sxs-lookup"><span data-stu-id="a5408-156">Int32</span></span>|<span data-ttu-id="a5408-157">Número de errores de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="a5408-157">Device error count for the setting</span></span>|
|<span data-ttu-id="a5408-158">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="a5408-158">conflictDeviceCount</span></span>|<span data-ttu-id="a5408-159">Int32</span><span class="sxs-lookup"><span data-stu-id="a5408-159">Int32</span></span>|<span data-ttu-id="a5408-160">Número de errores de conflictos de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="a5408-160">Device conflict error count for the setting</span></span>|



## <a name="response"></a><span data-ttu-id="a5408-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5408-161">Response</span></span>
<span data-ttu-id="a5408-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a5408-162">If successful, this method returns a `200 OK` response code and an updated [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a5408-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a5408-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="a5408-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a5408-164">Request</span></span>
<span data-ttu-id="a5408-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a5408-165">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
Content-type: application/json
Content-length: 360

{
  "@odata.type": "#microsoft.graph.settingStateDeviceSummary",
  "settingName": "Setting Name value",
  "instancePath": "Instance Path value",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```

### <a name="response"></a><span data-ttu-id="a5408-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a5408-166">Response</span></span>
<span data-ttu-id="a5408-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a5408-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 409

{
  "@odata.type": "#microsoft.graph.settingStateDeviceSummary",
  "id": "3e2d4526-4526-3e2d-2645-2d3e26452d3e",
  "settingName": "Setting Name value",
  "instancePath": "Instance Path value",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```



