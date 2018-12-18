---
title: Crear deviceCompliancePolicySettingStateSummary
description: Cree un objeto deviceCompliancePolicySettingStateSummary.
author: tfitzmac
ms.openlocfilehash: 289fb312e0c4f208a6ac494dfea090c21fc52295
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27307395"
---
# <a name="create-devicecompliancepolicysettingstatesummary"></a><span data-ttu-id="73688-103">Crear deviceCompliancePolicySettingStateSummary</span><span class="sxs-lookup"><span data-stu-id="73688-103">Create deviceCompliancePolicySettingStateSummary</span></span>

> <span data-ttu-id="73688-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="73688-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="73688-105">Cree un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="73688-105">Create a new [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="73688-106">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="73688-106">Prerequisites</span></span>
<span data-ttu-id="73688-p101">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="73688-p101">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="73688-109">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="73688-109">Permission type</span></span>|<span data-ttu-id="73688-110">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="73688-110">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="73688-111">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="73688-111">Delegated (work or school account)</span></span>|<span data-ttu-id="73688-112">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="73688-112">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="73688-113">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="73688-113">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="73688-114">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73688-114">Not supported.</span></span>|
|<span data-ttu-id="73688-115">Aplicación</span><span class="sxs-lookup"><span data-stu-id="73688-115">Application</span></span>|<span data-ttu-id="73688-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="73688-116">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="73688-117">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="73688-117">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicySettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="73688-118">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="73688-118">Request headers</span></span>
|<span data-ttu-id="73688-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="73688-119">Header</span></span>|<span data-ttu-id="73688-120">Valor</span><span class="sxs-lookup"><span data-stu-id="73688-120">Value</span></span>|
|:---|:---|
|<span data-ttu-id="73688-121">Autorización</span><span class="sxs-lookup"><span data-stu-id="73688-121">Authorization</span></span>|<span data-ttu-id="73688-122">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="73688-122">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="73688-123">Aceptar</span><span class="sxs-lookup"><span data-stu-id="73688-123">Accept</span></span>|<span data-ttu-id="73688-124">application/json</span><span class="sxs-lookup"><span data-stu-id="73688-124">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="73688-125">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="73688-125">Request body</span></span>
<span data-ttu-id="73688-126">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceCompliancePolicySettingStateSummary.</span><span class="sxs-lookup"><span data-stu-id="73688-126">In the request body, supply a JSON representation for the deviceCompliancePolicySettingStateSummary object.</span></span>

<span data-ttu-id="73688-127">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceCompliancePolicySettingStateSummary.</span><span class="sxs-lookup"><span data-stu-id="73688-127">The following table shows the properties that are required when you create the deviceCompliancePolicySettingStateSummary.</span></span>

|<span data-ttu-id="73688-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="73688-128">Property</span></span>|<span data-ttu-id="73688-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="73688-129">Type</span></span>|<span data-ttu-id="73688-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="73688-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="73688-131">id</span><span class="sxs-lookup"><span data-stu-id="73688-131">id</span></span>|<span data-ttu-id="73688-132">String</span><span class="sxs-lookup"><span data-stu-id="73688-132">String</span></span>|<span data-ttu-id="73688-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="73688-133">Key of the entity.</span></span>|
|<span data-ttu-id="73688-134">ajustes</span><span class="sxs-lookup"><span data-stu-id="73688-134">setting</span></span>|<span data-ttu-id="73688-135">String</span><span class="sxs-lookup"><span data-stu-id="73688-135">String</span></span>|<span data-ttu-id="73688-136">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="73688-136">The setting class name and property name.</span></span>|
|<span data-ttu-id="73688-137">settingName</span><span class="sxs-lookup"><span data-stu-id="73688-137">settingName</span></span>|<span data-ttu-id="73688-138">String</span><span class="sxs-lookup"><span data-stu-id="73688-138">String</span></span>|<span data-ttu-id="73688-139">Nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="73688-139">Name of the setting.</span></span>|
|<span data-ttu-id="73688-140">platformType</span><span class="sxs-lookup"><span data-stu-id="73688-140">platformType</span></span>|[<span data-ttu-id="73688-141">policyPlatformType</span><span class="sxs-lookup"><span data-stu-id="73688-141">policyPlatformType</span></span>](../resources/intune-deviceconfig-policyplatformtype.md)|<span data-ttu-id="73688-142">Plataforma de configuración.</span><span class="sxs-lookup"><span data-stu-id="73688-142">Setting platform.</span></span> <span data-ttu-id="73688-143">Los valores posibles son: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile` y `all`.</span><span class="sxs-lookup"><span data-stu-id="73688-143">Possible values are: `android`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`, `all`.</span></span>|
|<span data-ttu-id="73688-144">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="73688-144">unknownDeviceCount</span></span>|<span data-ttu-id="73688-145">Int32</span><span class="sxs-lookup"><span data-stu-id="73688-145">Int32</span></span>|<span data-ttu-id="73688-146">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="73688-146">Number of unknown devices</span></span>|
|<span data-ttu-id="73688-147">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="73688-147">notApplicableDeviceCount</span></span>|<span data-ttu-id="73688-148">Int32</span><span class="sxs-lookup"><span data-stu-id="73688-148">Int32</span></span>|<span data-ttu-id="73688-149">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="73688-149">Number of not applicable devices</span></span>|
|<span data-ttu-id="73688-150">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="73688-150">compliantDeviceCount</span></span>|<span data-ttu-id="73688-151">Int32</span><span class="sxs-lookup"><span data-stu-id="73688-151">Int32</span></span>|<span data-ttu-id="73688-152">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="73688-152">Number of compliant devices</span></span>|
|<span data-ttu-id="73688-153">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="73688-153">remediatedDeviceCount</span></span>|<span data-ttu-id="73688-154">Int32</span><span class="sxs-lookup"><span data-stu-id="73688-154">Int32</span></span>|<span data-ttu-id="73688-155">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="73688-155">Number of remediated devices</span></span>|
|<span data-ttu-id="73688-156">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="73688-156">nonCompliantDeviceCount</span></span>|<span data-ttu-id="73688-157">Int32</span><span class="sxs-lookup"><span data-stu-id="73688-157">Int32</span></span>|<span data-ttu-id="73688-158">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="73688-158">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="73688-159">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="73688-159">errorDeviceCount</span></span>|<span data-ttu-id="73688-160">Int32</span><span class="sxs-lookup"><span data-stu-id="73688-160">Int32</span></span>|<span data-ttu-id="73688-161">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="73688-161">Number of error devices</span></span>|
|<span data-ttu-id="73688-162">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="73688-162">conflictDeviceCount</span></span>|<span data-ttu-id="73688-163">Int32</span><span class="sxs-lookup"><span data-stu-id="73688-163">Int32</span></span>|<span data-ttu-id="73688-164">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="73688-164">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="73688-165">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73688-165">Response</span></span>
<span data-ttu-id="73688-166">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="73688-166">If successful, this method returns a `201 Created` response code and a [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="73688-167">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="73688-167">Example</span></span>
### <a name="request"></a><span data-ttu-id="73688-168">Solicitud</span><span class="sxs-lookup"><span data-stu-id="73688-168">Request</span></span>
<span data-ttu-id="73688-169">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="73688-169">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/v1.0/deviceManagement/deviceCompliancePolicySettingStateSummaries
Content-type: application/json
Content-length: 391

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingStateSummary",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "platformType": "iOS",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```

### <a name="response"></a><span data-ttu-id="73688-170">Respuesta</span><span class="sxs-lookup"><span data-stu-id="73688-170">Response</span></span>
<span data-ttu-id="73688-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="73688-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 440

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingStateSummary",
  "id": "7474d6d5-d6d5-7474-d5d6-7474d5d67474",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "platformType": "iOS",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```



