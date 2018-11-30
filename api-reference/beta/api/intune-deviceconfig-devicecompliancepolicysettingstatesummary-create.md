---
title: Crear deviceCompliancePolicySettingStateSummary
description: Cree un objeto deviceCompliancePolicySettingStateSummary.
ms.openlocfilehash: f7fd5a8d65655b4015d0fcf6dee6377e008b9c99
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083924"
---
# <a name="create-devicecompliancepolicysettingstatesummary"></a><span data-ttu-id="07023-103">Crear deviceCompliancePolicySettingStateSummary</span><span class="sxs-lookup"><span data-stu-id="07023-103">Create deviceCompliancePolicySettingStateSummary</span></span>

> <span data-ttu-id="07023-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="07023-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="07023-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="07023-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="07023-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="07023-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="07023-107">Cree un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md).</span><span class="sxs-lookup"><span data-stu-id="07023-107">Create a new [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="07023-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="07023-108">Prerequisites</span></span>
<span data-ttu-id="07023-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="07023-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="07023-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="07023-111">Permission type</span></span>|<span data-ttu-id="07023-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="07023-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="07023-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="07023-113">Delegated (work or school account)</span></span>|<span data-ttu-id="07023-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="07023-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="07023-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="07023-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="07023-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07023-116">Not supported.</span></span>|
|<span data-ttu-id="07023-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="07023-117">Application</span></span>|<span data-ttu-id="07023-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="07023-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="07023-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="07023-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceCompliancePolicySettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="07023-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="07023-120">Request headers</span></span>
|<span data-ttu-id="07023-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="07023-121">Header</span></span>|<span data-ttu-id="07023-122">Valor</span><span class="sxs-lookup"><span data-stu-id="07023-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="07023-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="07023-123">Authorization</span></span>|<span data-ttu-id="07023-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="07023-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="07023-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="07023-125">Accept</span></span>|<span data-ttu-id="07023-126">application/json</span><span class="sxs-lookup"><span data-stu-id="07023-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="07023-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="07023-127">Request body</span></span>
<span data-ttu-id="07023-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto deviceCompliancePolicySettingStateSummary.</span><span class="sxs-lookup"><span data-stu-id="07023-128">In the request body, supply a JSON representation for the deviceCompliancePolicySettingStateSummary object.</span></span>

<span data-ttu-id="07023-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto deviceCompliancePolicySettingStateSummary.</span><span class="sxs-lookup"><span data-stu-id="07023-129">The following table shows the properties that are required when you create the deviceCompliancePolicySettingStateSummary.</span></span>

|<span data-ttu-id="07023-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="07023-130">Property</span></span>|<span data-ttu-id="07023-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="07023-131">Type</span></span>|<span data-ttu-id="07023-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="07023-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="07023-133">id</span><span class="sxs-lookup"><span data-stu-id="07023-133">id</span></span>|<span data-ttu-id="07023-134">String</span><span class="sxs-lookup"><span data-stu-id="07023-134">String</span></span>|<span data-ttu-id="07023-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="07023-135">Key of the entity.</span></span>|
|<span data-ttu-id="07023-136">ajustes</span><span class="sxs-lookup"><span data-stu-id="07023-136">setting</span></span>|<span data-ttu-id="07023-137">String</span><span class="sxs-lookup"><span data-stu-id="07023-137">String</span></span>|<span data-ttu-id="07023-138">El nombre de la clase de configuración y el nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="07023-138">The setting class name and property name.</span></span>|
|<span data-ttu-id="07023-139">settingName</span><span class="sxs-lookup"><span data-stu-id="07023-139">settingName</span></span>|<span data-ttu-id="07023-140">String</span><span class="sxs-lookup"><span data-stu-id="07023-140">String</span></span>|<span data-ttu-id="07023-141">Nombre de la configuración.</span><span class="sxs-lookup"><span data-stu-id="07023-141">Name of the setting.</span></span>|
|<span data-ttu-id="07023-142">platformType</span><span class="sxs-lookup"><span data-stu-id="07023-142">platformType</span></span>|[<span data-ttu-id="07023-143">policyPlatformType</span><span class="sxs-lookup"><span data-stu-id="07023-143">policyPlatformType</span></span>](../resources/intune-deviceconfig-policyplatformtype.md)|<span data-ttu-id="07023-144">Plataforma de configuración.</span><span class="sxs-lookup"><span data-stu-id="07023-144">Setting platform.</span></span> <span data-ttu-id="07023-145">Los valores posibles son: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile` y `all`.</span><span class="sxs-lookup"><span data-stu-id="07023-145">Possible values are: `android`, `androidForWork`, `iOS`, `macOS`, `windowsPhone81`, `windows81AndLater`, `windows10AndLater`, `androidWorkProfile`, `all`.</span></span>|
|<span data-ttu-id="07023-146">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="07023-146">unknownDeviceCount</span></span>|<span data-ttu-id="07023-147">Int32</span><span class="sxs-lookup"><span data-stu-id="07023-147">Int32</span></span>|<span data-ttu-id="07023-148">Número de dispositivos desconocidos</span><span class="sxs-lookup"><span data-stu-id="07023-148">Number of unknown devices</span></span>|
|<span data-ttu-id="07023-149">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="07023-149">notApplicableDeviceCount</span></span>|<span data-ttu-id="07023-150">Int32</span><span class="sxs-lookup"><span data-stu-id="07023-150">Int32</span></span>|<span data-ttu-id="07023-151">Número de dispositivos no aplicables</span><span class="sxs-lookup"><span data-stu-id="07023-151">Number of not applicable devices</span></span>|
|<span data-ttu-id="07023-152">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="07023-152">compliantDeviceCount</span></span>|<span data-ttu-id="07023-153">Int32</span><span class="sxs-lookup"><span data-stu-id="07023-153">Int32</span></span>|<span data-ttu-id="07023-154">Número de dispositivos compatibles</span><span class="sxs-lookup"><span data-stu-id="07023-154">Number of compliant devices</span></span>|
|<span data-ttu-id="07023-155">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="07023-155">remediatedDeviceCount</span></span>|<span data-ttu-id="07023-156">Int32</span><span class="sxs-lookup"><span data-stu-id="07023-156">Int32</span></span>|<span data-ttu-id="07023-157">Número de dispositivos corregidos</span><span class="sxs-lookup"><span data-stu-id="07023-157">Number of remediated devices</span></span>|
|<span data-ttu-id="07023-158">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="07023-158">nonCompliantDeviceCount</span></span>|<span data-ttu-id="07023-159">Int32</span><span class="sxs-lookup"><span data-stu-id="07023-159">Int32</span></span>|<span data-ttu-id="07023-160">Número de dispositivos no compatibles</span><span class="sxs-lookup"><span data-stu-id="07023-160">Number of NonCompliant devices</span></span>|
|<span data-ttu-id="07023-161">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="07023-161">errorDeviceCount</span></span>|<span data-ttu-id="07023-162">Int32</span><span class="sxs-lookup"><span data-stu-id="07023-162">Int32</span></span>|<span data-ttu-id="07023-163">Número de dispositivos con error</span><span class="sxs-lookup"><span data-stu-id="07023-163">Number of error devices</span></span>|
|<span data-ttu-id="07023-164">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="07023-164">conflictDeviceCount</span></span>|<span data-ttu-id="07023-165">Int32</span><span class="sxs-lookup"><span data-stu-id="07023-165">Int32</span></span>|<span data-ttu-id="07023-166">Número de dispositivos en conflicto</span><span class="sxs-lookup"><span data-stu-id="07023-166">Number of conflict devices</span></span>|



## <a name="response"></a><span data-ttu-id="07023-167">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07023-167">Response</span></span>
<span data-ttu-id="07023-168">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="07023-168">If successful, this method returns a `201 Created` response code and a [deviceCompliancePolicySettingStateSummary](../resources/intune-deviceconfig-devicecompliancepolicysettingstatesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="07023-169">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="07023-169">Example</span></span>
### <a name="request"></a><span data-ttu-id="07023-170">Solicitud</span><span class="sxs-lookup"><span data-stu-id="07023-170">Request</span></span>
<span data-ttu-id="07023-171">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="07023-171">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceCompliancePolicySettingStateSummaries
Content-type: application/json
Content-length: 402

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingStateSummary",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "platformType": "androidForWork",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```

### <a name="response"></a><span data-ttu-id="07023-172">Respuesta</span><span class="sxs-lookup"><span data-stu-id="07023-172">Response</span></span>
<span data-ttu-id="07023-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="07023-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
Content-Type: application/json
Content-Length: 451

{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicySettingStateSummary",
  "id": "7474d6d5-d6d5-7474-d5d6-7474d5d67474",
  "setting": "Setting value",
  "settingName": "Setting Name value",
  "platformType": "androidForWork",
  "unknownDeviceCount": 2,
  "notApplicableDeviceCount": 8,
  "compliantDeviceCount": 4,
  "remediatedDeviceCount": 5,
  "nonCompliantDeviceCount": 7,
  "errorDeviceCount": 0,
  "conflictDeviceCount": 3
}
```





