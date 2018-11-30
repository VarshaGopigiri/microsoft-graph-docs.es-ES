---
title: Actualizar settingStateDeviceSummary
description: Actualice las propiedades de un objeto settingStateDeviceSummary.
ms.openlocfilehash: a530c87ab55eb521ace3464e3feab5f6b8d36b4d
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27084869"
---
# <a name="update-settingstatedevicesummary"></a><span data-ttu-id="37aef-103">Actualizar settingStateDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="37aef-103">Update settingStateDeviceSummary</span></span>

> <span data-ttu-id="37aef-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="37aef-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="37aef-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="37aef-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="37aef-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="37aef-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="37aef-107">Actualice las propiedades de un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="37aef-107">Update the properties of a [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="37aef-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="37aef-108">Prerequisites</span></span>
<span data-ttu-id="37aef-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="37aef-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="37aef-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="37aef-111">Permission type</span></span>|<span data-ttu-id="37aef-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="37aef-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="37aef-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="37aef-113">Delegated (work or school account)</span></span>|<span data-ttu-id="37aef-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="37aef-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="37aef-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="37aef-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="37aef-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37aef-116">Not supported.</span></span>|
|<span data-ttu-id="37aef-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="37aef-117">Application</span></span>|<span data-ttu-id="37aef-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="37aef-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="37aef-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="37aef-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
```

## <a name="request-headers"></a><span data-ttu-id="37aef-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="37aef-120">Request headers</span></span>
|<span data-ttu-id="37aef-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37aef-121">Header</span></span>|<span data-ttu-id="37aef-122">Valor</span><span class="sxs-lookup"><span data-stu-id="37aef-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="37aef-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="37aef-123">Authorization</span></span>|<span data-ttu-id="37aef-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="37aef-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="37aef-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="37aef-125">Accept</span></span>|<span data-ttu-id="37aef-126">application/json</span><span class="sxs-lookup"><span data-stu-id="37aef-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="37aef-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37aef-127">Request body</span></span>
<span data-ttu-id="37aef-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="37aef-128">In the request body, supply a JSON representation for the [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object.</span></span>

<span data-ttu-id="37aef-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="37aef-129">The following table shows the properties that are required when you create the [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span></span>

|<span data-ttu-id="37aef-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="37aef-130">Property</span></span>|<span data-ttu-id="37aef-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="37aef-131">Type</span></span>|<span data-ttu-id="37aef-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="37aef-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="37aef-133">id</span><span class="sxs-lookup"><span data-stu-id="37aef-133">id</span></span>|<span data-ttu-id="37aef-134">String</span><span class="sxs-lookup"><span data-stu-id="37aef-134">String</span></span>|<span data-ttu-id="37aef-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="37aef-135">Key of the entity.</span></span>|
|<span data-ttu-id="37aef-136">settingName</span><span class="sxs-lookup"><span data-stu-id="37aef-136">settingName</span></span>|<span data-ttu-id="37aef-137">String</span><span class="sxs-lookup"><span data-stu-id="37aef-137">String</span></span>|<span data-ttu-id="37aef-138">Nombre de la configuración</span><span class="sxs-lookup"><span data-stu-id="37aef-138">Name of the setting</span></span>|
|<span data-ttu-id="37aef-139">instancePath</span><span class="sxs-lookup"><span data-stu-id="37aef-139">instancePath</span></span>|<span data-ttu-id="37aef-140">String</span><span class="sxs-lookup"><span data-stu-id="37aef-140">String</span></span>|<span data-ttu-id="37aef-141">Nombre de InstancePath para la configuración</span><span class="sxs-lookup"><span data-stu-id="37aef-141">Name of the InstancePath for the setting</span></span>|
|<span data-ttu-id="37aef-142">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="37aef-142">unknownDeviceCount</span></span>|<span data-ttu-id="37aef-143">Int32</span><span class="sxs-lookup"><span data-stu-id="37aef-143">Int32</span></span>|<span data-ttu-id="37aef-144">Número de dispositivos desconocido para la configuración</span><span class="sxs-lookup"><span data-stu-id="37aef-144">Device Unkown count for the setting</span></span>|
|<span data-ttu-id="37aef-145">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="37aef-145">notApplicableDeviceCount</span></span>|<span data-ttu-id="37aef-146">Int32</span><span class="sxs-lookup"><span data-stu-id="37aef-146">Int32</span></span>|<span data-ttu-id="37aef-147">Número de dispositivos no aplicables para la configuración</span><span class="sxs-lookup"><span data-stu-id="37aef-147">Device Not Applicable count for the setting</span></span>|
|<span data-ttu-id="37aef-148">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="37aef-148">compliantDeviceCount</span></span>|<span data-ttu-id="37aef-149">Int32</span><span class="sxs-lookup"><span data-stu-id="37aef-149">Int32</span></span>|<span data-ttu-id="37aef-150">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="37aef-150">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="37aef-151">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="37aef-151">remediatedDeviceCount</span></span>|<span data-ttu-id="37aef-152">Int32</span><span class="sxs-lookup"><span data-stu-id="37aef-152">Int32</span></span>|<span data-ttu-id="37aef-153">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="37aef-153">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="37aef-154">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="37aef-154">nonCompliantDeviceCount</span></span>|<span data-ttu-id="37aef-155">Int32</span><span class="sxs-lookup"><span data-stu-id="37aef-155">Int32</span></span>|<span data-ttu-id="37aef-156">Número de dispositivos no compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="37aef-156">Device NonCompliant count for the setting</span></span>|
|<span data-ttu-id="37aef-157">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="37aef-157">errorDeviceCount</span></span>|<span data-ttu-id="37aef-158">Int32</span><span class="sxs-lookup"><span data-stu-id="37aef-158">Int32</span></span>|<span data-ttu-id="37aef-159">Número de errores de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="37aef-159">Device error count for the setting</span></span>|
|<span data-ttu-id="37aef-160">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="37aef-160">conflictDeviceCount</span></span>|<span data-ttu-id="37aef-161">Int32</span><span class="sxs-lookup"><span data-stu-id="37aef-161">Int32</span></span>|<span data-ttu-id="37aef-162">Número de errores de conflictos de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="37aef-162">Device conflict error count for the setting</span></span>|



## <a name="response"></a><span data-ttu-id="37aef-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37aef-163">Response</span></span>
<span data-ttu-id="37aef-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37aef-164">If successful, this method returns a `200 OK` response code and an updated [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="37aef-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="37aef-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="37aef-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="37aef-166">Request</span></span>
<span data-ttu-id="37aef-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37aef-167">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries/{settingStateDeviceSummaryId}
Content-type: application/json
Content-length: 296

{
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

### <a name="response"></a><span data-ttu-id="37aef-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="37aef-168">Response</span></span>
<span data-ttu-id="37aef-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="37aef-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





