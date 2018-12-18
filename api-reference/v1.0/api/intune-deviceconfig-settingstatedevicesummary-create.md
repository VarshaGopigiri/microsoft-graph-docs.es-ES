---
title: Crear settingStateDeviceSummary
description: Cree un objeto settingStateDeviceSummary.
author: tfitzmac
ms.openlocfilehash: 53cccf3ee6cf11daa6cec1697de89eaf7f0a7140
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27309579"
---
# <a name="create-settingstatedevicesummary"></a><span data-ttu-id="9f564-103">Crear settingStateDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="9f564-103">Create settingStateDeviceSummary</span></span>

> <span data-ttu-id="9f564-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="9f564-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="9f564-105">Cree un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="9f564-105">Create a new [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="9f564-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="9f564-106">Prerequisites</span></span>
<span data-ttu-id="9f564-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="9f564-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="9f564-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9f564-109">Permission type</span></span>|<span data-ttu-id="9f564-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9f564-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="9f564-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9f564-111">Delegated (work or school account)</span></span>|<span data-ttu-id="9f564-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="9f564-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="9f564-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9f564-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="9f564-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f564-114">Not supported.</span></span>|
|<span data-ttu-id="9f564-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9f564-115">Application</span></span>|<span data-ttu-id="9f564-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="9f564-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="9f564-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9f564-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceSettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="9f564-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9f564-118">Request headers</span></span>
|<span data-ttu-id="9f564-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9f564-119">Header</span></span>|<span data-ttu-id="9f564-120">Valor</span><span class="sxs-lookup"><span data-stu-id="9f564-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="9f564-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="9f564-121">Authorization</span></span>|<span data-ttu-id="9f564-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="9f564-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="9f564-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="9f564-123">Accept</span></span>|<span data-ttu-id="9f564-124">application/json</span><span class="sxs-lookup"><span data-stu-id="9f564-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="9f564-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="9f564-125">Request body</span></span>
<span data-ttu-id="9f564-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto settingStateDeviceSummary.</span><span class="sxs-lookup"><span data-stu-id="9f564-126">In the request body, supply a JSON representation for the settingStateDeviceSummary object.</span></span>

<span data-ttu-id="9f564-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto settingStateDeviceSummary.</span><span class="sxs-lookup"><span data-stu-id="9f564-127">The following table shows the properties that are required when you create the settingStateDeviceSummary.</span></span>

|<span data-ttu-id="9f564-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f564-128">Property</span></span>|<span data-ttu-id="9f564-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f564-129">Type</span></span>|<span data-ttu-id="9f564-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f564-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="9f564-131">id</span><span class="sxs-lookup"><span data-stu-id="9f564-131">id</span></span>|<span data-ttu-id="9f564-132">String</span><span class="sxs-lookup"><span data-stu-id="9f564-132">String</span></span>|<span data-ttu-id="9f564-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="9f564-133">Key of the entity.</span></span>|
|<span data-ttu-id="9f564-134">settingName</span><span class="sxs-lookup"><span data-stu-id="9f564-134">settingName</span></span>|<span data-ttu-id="9f564-135">String</span><span class="sxs-lookup"><span data-stu-id="9f564-135">String</span></span>|<span data-ttu-id="9f564-136">Nombre de la configuración</span><span class="sxs-lookup"><span data-stu-id="9f564-136">Name of the setting</span></span>|
|<span data-ttu-id="9f564-137">instancePath</span><span class="sxs-lookup"><span data-stu-id="9f564-137">instancePath</span></span>|<span data-ttu-id="9f564-138">String</span><span class="sxs-lookup"><span data-stu-id="9f564-138">String</span></span>|<span data-ttu-id="9f564-139">Nombre de InstancePath para la configuración</span><span class="sxs-lookup"><span data-stu-id="9f564-139">Name of the InstancePath for the setting</span></span>|
|<span data-ttu-id="9f564-140">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9f564-140">unknownDeviceCount</span></span>|<span data-ttu-id="9f564-141">Int32</span><span class="sxs-lookup"><span data-stu-id="9f564-141">Int32</span></span>|<span data-ttu-id="9f564-142">Número de dispositivos desconocido para la configuración</span><span class="sxs-lookup"><span data-stu-id="9f564-142">Device Unkown count for the setting</span></span>|
|<span data-ttu-id="9f564-143">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9f564-143">notApplicableDeviceCount</span></span>|<span data-ttu-id="9f564-144">Int32</span><span class="sxs-lookup"><span data-stu-id="9f564-144">Int32</span></span>|<span data-ttu-id="9f564-145">Número de dispositivos no aplicables para la configuración</span><span class="sxs-lookup"><span data-stu-id="9f564-145">Device Not Applicable count for the setting</span></span>|
|<span data-ttu-id="9f564-146">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9f564-146">compliantDeviceCount</span></span>|<span data-ttu-id="9f564-147">Int32</span><span class="sxs-lookup"><span data-stu-id="9f564-147">Int32</span></span>|<span data-ttu-id="9f564-148">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="9f564-148">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="9f564-149">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9f564-149">remediatedDeviceCount</span></span>|<span data-ttu-id="9f564-150">Int32</span><span class="sxs-lookup"><span data-stu-id="9f564-150">Int32</span></span>|<span data-ttu-id="9f564-151">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="9f564-151">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="9f564-152">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9f564-152">nonCompliantDeviceCount</span></span>|<span data-ttu-id="9f564-153">Int32</span><span class="sxs-lookup"><span data-stu-id="9f564-153">Int32</span></span>|<span data-ttu-id="9f564-154">Número de dispositivos no compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="9f564-154">Device NonCompliant count for the setting</span></span>|
|<span data-ttu-id="9f564-155">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9f564-155">errorDeviceCount</span></span>|<span data-ttu-id="9f564-156">Int32</span><span class="sxs-lookup"><span data-stu-id="9f564-156">Int32</span></span>|<span data-ttu-id="9f564-157">Número de errores de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="9f564-157">Device error count for the setting</span></span>|
|<span data-ttu-id="9f564-158">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="9f564-158">conflictDeviceCount</span></span>|<span data-ttu-id="9f564-159">Int32</span><span class="sxs-lookup"><span data-stu-id="9f564-159">Int32</span></span>|<span data-ttu-id="9f564-160">Número de errores de conflictos de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="9f564-160">Device conflict error count for the setting</span></span>|



## <a name="response"></a><span data-ttu-id="9f564-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f564-161">Response</span></span>
<span data-ttu-id="9f564-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9f564-162">If successful, this method returns a `201 Created` response code and a [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="9f564-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9f564-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="9f564-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9f564-164">Request</span></span>
<span data-ttu-id="9f564-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9f564-165">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="9f564-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9f564-166">Response</span></span>
<span data-ttu-id="9f564-p102">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="9f564-p102">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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



