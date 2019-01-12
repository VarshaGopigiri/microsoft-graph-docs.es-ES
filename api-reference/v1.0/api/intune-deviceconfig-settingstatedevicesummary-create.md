---
title: Crear settingStateDeviceSummary
description: Cree un objeto settingStateDeviceSummary.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 512d36e348a675534c3c1306045fd8570dc22ef5
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27912270"
---
# <a name="create-settingstatedevicesummary"></a><span data-ttu-id="b4699-103">Crear settingStateDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="b4699-103">Create settingStateDeviceSummary</span></span>

> <span data-ttu-id="b4699-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="b4699-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="b4699-105">Cree un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="b4699-105">Create a new [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="b4699-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="b4699-106">Prerequisites</span></span>
<span data-ttu-id="b4699-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="b4699-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="b4699-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="b4699-109">Permission type</span></span>|<span data-ttu-id="b4699-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="b4699-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="b4699-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="b4699-111">Delegated (work or school account)</span></span>|<span data-ttu-id="b4699-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="b4699-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="b4699-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="b4699-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="b4699-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4699-114">Not supported.</span></span>|
|<span data-ttu-id="b4699-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="b4699-115">Application</span></span>|<span data-ttu-id="b4699-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="b4699-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="b4699-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="b4699-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceSettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="b4699-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="b4699-118">Request headers</span></span>
|<span data-ttu-id="b4699-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b4699-119">Header</span></span>|<span data-ttu-id="b4699-120">Valor</span><span class="sxs-lookup"><span data-stu-id="b4699-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="b4699-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="b4699-121">Authorization</span></span>|<span data-ttu-id="b4699-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="b4699-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="b4699-123">Accept</span><span class="sxs-lookup"><span data-stu-id="b4699-123">Accept</span></span>|<span data-ttu-id="b4699-124">application/json</span><span class="sxs-lookup"><span data-stu-id="b4699-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="b4699-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="b4699-125">Request body</span></span>
<span data-ttu-id="b4699-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto settingStateDeviceSummary.</span><span class="sxs-lookup"><span data-stu-id="b4699-126">In the request body, supply a JSON representation for the settingStateDeviceSummary object.</span></span>

<span data-ttu-id="b4699-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto settingStateDeviceSummary.</span><span class="sxs-lookup"><span data-stu-id="b4699-127">The following table shows the properties that are required when you create the settingStateDeviceSummary.</span></span>

|<span data-ttu-id="b4699-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4699-128">Property</span></span>|<span data-ttu-id="b4699-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4699-129">Type</span></span>|<span data-ttu-id="b4699-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4699-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="b4699-131">id</span><span class="sxs-lookup"><span data-stu-id="b4699-131">id</span></span>|<span data-ttu-id="b4699-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="b4699-132">String</span></span>|<span data-ttu-id="b4699-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="b4699-133">Key of the entity.</span></span>|
|<span data-ttu-id="b4699-134">settingName</span><span class="sxs-lookup"><span data-stu-id="b4699-134">settingName</span></span>|<span data-ttu-id="b4699-135">String</span><span class="sxs-lookup"><span data-stu-id="b4699-135">String</span></span>|<span data-ttu-id="b4699-136">Nombre de la configuración</span><span class="sxs-lookup"><span data-stu-id="b4699-136">Name of the setting</span></span>|
|<span data-ttu-id="b4699-137">instancePath</span><span class="sxs-lookup"><span data-stu-id="b4699-137">instancePath</span></span>|<span data-ttu-id="b4699-138">String</span><span class="sxs-lookup"><span data-stu-id="b4699-138">String</span></span>|<span data-ttu-id="b4699-139">Nombre de InstancePath para la configuración</span><span class="sxs-lookup"><span data-stu-id="b4699-139">Name of the InstancePath for the setting</span></span>|
|<span data-ttu-id="b4699-140">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b4699-140">unknownDeviceCount</span></span>|<span data-ttu-id="b4699-141">Int32</span><span class="sxs-lookup"><span data-stu-id="b4699-141">Int32</span></span>|<span data-ttu-id="b4699-142">Número de dispositivos desconocido para la configuración</span><span class="sxs-lookup"><span data-stu-id="b4699-142">Device Unkown count for the setting</span></span>|
|<span data-ttu-id="b4699-143">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b4699-143">notApplicableDeviceCount</span></span>|<span data-ttu-id="b4699-144">Int32</span><span class="sxs-lookup"><span data-stu-id="b4699-144">Int32</span></span>|<span data-ttu-id="b4699-145">Número de dispositivos no aplicables para la configuración</span><span class="sxs-lookup"><span data-stu-id="b4699-145">Device Not Applicable count for the setting</span></span>|
|<span data-ttu-id="b4699-146">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b4699-146">compliantDeviceCount</span></span>|<span data-ttu-id="b4699-147">Int32</span><span class="sxs-lookup"><span data-stu-id="b4699-147">Int32</span></span>|<span data-ttu-id="b4699-148">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="b4699-148">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="b4699-149">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b4699-149">remediatedDeviceCount</span></span>|<span data-ttu-id="b4699-150">Int32</span><span class="sxs-lookup"><span data-stu-id="b4699-150">Int32</span></span>|<span data-ttu-id="b4699-151">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="b4699-151">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="b4699-152">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b4699-152">nonCompliantDeviceCount</span></span>|<span data-ttu-id="b4699-153">Int32</span><span class="sxs-lookup"><span data-stu-id="b4699-153">Int32</span></span>|<span data-ttu-id="b4699-154">Número de dispositivos no compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="b4699-154">Device NonCompliant count for the setting</span></span>|
|<span data-ttu-id="b4699-155">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b4699-155">errorDeviceCount</span></span>|<span data-ttu-id="b4699-156">Int32</span><span class="sxs-lookup"><span data-stu-id="b4699-156">Int32</span></span>|<span data-ttu-id="b4699-157">Número de errores de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="b4699-157">Device error count for the setting</span></span>|
|<span data-ttu-id="b4699-158">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="b4699-158">conflictDeviceCount</span></span>|<span data-ttu-id="b4699-159">Int32</span><span class="sxs-lookup"><span data-stu-id="b4699-159">Int32</span></span>|<span data-ttu-id="b4699-160">Número de errores de conflictos de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="b4699-160">Device conflict error count for the setting</span></span>|



## <a name="response"></a><span data-ttu-id="b4699-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4699-161">Response</span></span>
<span data-ttu-id="b4699-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="b4699-162">If successful, this method returns a `201 Created` response code and a [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="b4699-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b4699-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="b4699-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="b4699-164">Request</span></span>
<span data-ttu-id="b4699-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b4699-165">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries
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

### <a name="response"></a><span data-ttu-id="b4699-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="b4699-166">Response</span></span>
<span data-ttu-id="b4699-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="b4699-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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



