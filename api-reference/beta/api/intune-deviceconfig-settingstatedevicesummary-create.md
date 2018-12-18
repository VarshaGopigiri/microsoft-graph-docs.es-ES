---
title: Crear settingStateDeviceSummary
description: Cree un objeto settingStateDeviceSummary.
author: tfitzmac
ms.openlocfilehash: 44cb33bd0445586ead64c5101c297b7a27351344
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27333372"
---
# <a name="create-settingstatedevicesummary"></a><span data-ttu-id="4aba6-103">Crear settingStateDeviceSummary</span><span class="sxs-lookup"><span data-stu-id="4aba6-103">Create settingStateDeviceSummary</span></span>

> <span data-ttu-id="4aba6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="4aba6-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="4aba6-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="4aba6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="4aba6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4aba6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4aba6-107">Cree un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md).</span><span class="sxs-lookup"><span data-stu-id="4aba6-107">Create a new [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="4aba6-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="4aba6-108">Prerequisites</span></span>
<span data-ttu-id="4aba6-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="4aba6-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="4aba6-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="4aba6-111">Permission type</span></span>|<span data-ttu-id="4aba6-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="4aba6-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="4aba6-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="4aba6-113">Delegated (work or school account)</span></span>|<span data-ttu-id="4aba6-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4aba6-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="4aba6-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="4aba6-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="4aba6-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4aba6-116">Not supported.</span></span>|
|<span data-ttu-id="4aba6-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="4aba6-117">Application</span></span>|<span data-ttu-id="4aba6-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="4aba6-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="4aba6-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="4aba6-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries
POST /deviceManagement/deviceCompliancePolicies/{deviceCompliancePolicyId}/deviceSettingStateSummaries
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/deviceSettingStateSummaries
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/deviceSettingStateSummaries
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/deviceSettingStateSummaries
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/deviceSettingStateSummaries
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/deviceSettingStateSummaries
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/deviceSettingStateSummaries
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/deviceSettingStateSummaries
POST /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/deviceSettingStateSummaries
```

## <a name="request-headers"></a><span data-ttu-id="4aba6-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="4aba6-120">Request headers</span></span>
|<span data-ttu-id="4aba6-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="4aba6-121">Header</span></span>|<span data-ttu-id="4aba6-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4aba6-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="4aba6-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="4aba6-123">Authorization</span></span>|<span data-ttu-id="4aba6-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="4aba6-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="4aba6-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="4aba6-125">Accept</span></span>|<span data-ttu-id="4aba6-126">application/json</span><span class="sxs-lookup"><span data-stu-id="4aba6-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="4aba6-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="4aba6-127">Request body</span></span>
<span data-ttu-id="4aba6-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto settingStateDeviceSummary.</span><span class="sxs-lookup"><span data-stu-id="4aba6-128">In the request body, supply a JSON representation for the settingStateDeviceSummary object.</span></span>

<span data-ttu-id="4aba6-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto settingStateDeviceSummary.</span><span class="sxs-lookup"><span data-stu-id="4aba6-129">The following table shows the properties that are required when you create the settingStateDeviceSummary.</span></span>

|<span data-ttu-id="4aba6-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4aba6-130">Property</span></span>|<span data-ttu-id="4aba6-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="4aba6-131">Type</span></span>|<span data-ttu-id="4aba6-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="4aba6-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4aba6-133">id</span><span class="sxs-lookup"><span data-stu-id="4aba6-133">id</span></span>|<span data-ttu-id="4aba6-134">String</span><span class="sxs-lookup"><span data-stu-id="4aba6-134">String</span></span>|<span data-ttu-id="4aba6-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4aba6-135">Key of the entity.</span></span>|
|<span data-ttu-id="4aba6-136">settingName</span><span class="sxs-lookup"><span data-stu-id="4aba6-136">settingName</span></span>|<span data-ttu-id="4aba6-137">String</span><span class="sxs-lookup"><span data-stu-id="4aba6-137">String</span></span>|<span data-ttu-id="4aba6-138">Nombre de la configuración</span><span class="sxs-lookup"><span data-stu-id="4aba6-138">Name of the setting</span></span>|
|<span data-ttu-id="4aba6-139">instancePath</span><span class="sxs-lookup"><span data-stu-id="4aba6-139">instancePath</span></span>|<span data-ttu-id="4aba6-140">String</span><span class="sxs-lookup"><span data-stu-id="4aba6-140">String</span></span>|<span data-ttu-id="4aba6-141">Nombre de InstancePath para la configuración</span><span class="sxs-lookup"><span data-stu-id="4aba6-141">Name of the InstancePath for the setting</span></span>|
|<span data-ttu-id="4aba6-142">unknownDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4aba6-142">unknownDeviceCount</span></span>|<span data-ttu-id="4aba6-143">Int32</span><span class="sxs-lookup"><span data-stu-id="4aba6-143">Int32</span></span>|<span data-ttu-id="4aba6-144">Número de dispositivos desconocido para la configuración</span><span class="sxs-lookup"><span data-stu-id="4aba6-144">Device Unkown count for the setting</span></span>|
|<span data-ttu-id="4aba6-145">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4aba6-145">notApplicableDeviceCount</span></span>|<span data-ttu-id="4aba6-146">Int32</span><span class="sxs-lookup"><span data-stu-id="4aba6-146">Int32</span></span>|<span data-ttu-id="4aba6-147">Número de dispositivos no aplicables para la configuración</span><span class="sxs-lookup"><span data-stu-id="4aba6-147">Device Not Applicable count for the setting</span></span>|
|<span data-ttu-id="4aba6-148">compliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4aba6-148">compliantDeviceCount</span></span>|<span data-ttu-id="4aba6-149">Int32</span><span class="sxs-lookup"><span data-stu-id="4aba6-149">Int32</span></span>|<span data-ttu-id="4aba6-150">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="4aba6-150">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="4aba6-151">remediatedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4aba6-151">remediatedDeviceCount</span></span>|<span data-ttu-id="4aba6-152">Int32</span><span class="sxs-lookup"><span data-stu-id="4aba6-152">Int32</span></span>|<span data-ttu-id="4aba6-153">Número de dispositivos compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="4aba6-153">Device Compliant count for the setting</span></span>|
|<span data-ttu-id="4aba6-154">nonCompliantDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4aba6-154">nonCompliantDeviceCount</span></span>|<span data-ttu-id="4aba6-155">Int32</span><span class="sxs-lookup"><span data-stu-id="4aba6-155">Int32</span></span>|<span data-ttu-id="4aba6-156">Número de dispositivos no compatibles para la configuración</span><span class="sxs-lookup"><span data-stu-id="4aba6-156">Device NonCompliant count for the setting</span></span>|
|<span data-ttu-id="4aba6-157">errorDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4aba6-157">errorDeviceCount</span></span>|<span data-ttu-id="4aba6-158">Int32</span><span class="sxs-lookup"><span data-stu-id="4aba6-158">Int32</span></span>|<span data-ttu-id="4aba6-159">Número de errores de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="4aba6-159">Device error count for the setting</span></span>|
|<span data-ttu-id="4aba6-160">conflictDeviceCount</span><span class="sxs-lookup"><span data-stu-id="4aba6-160">conflictDeviceCount</span></span>|<span data-ttu-id="4aba6-161">Int32</span><span class="sxs-lookup"><span data-stu-id="4aba6-161">Int32</span></span>|<span data-ttu-id="4aba6-162">Número de errores de conflictos de dispositivo para la configuración</span><span class="sxs-lookup"><span data-stu-id="4aba6-162">Device conflict error count for the setting</span></span>|



## <a name="response"></a><span data-ttu-id="4aba6-163">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4aba6-163">Response</span></span>
<span data-ttu-id="4aba6-164">Si se ejecuta correctamente, este método devuelve un código de respuesta `201 Created` y un objeto [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="4aba6-164">If successful, this method returns a `201 Created` response code and a [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="4aba6-165">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="4aba6-165">Example</span></span>
### <a name="request"></a><span data-ttu-id="4aba6-166">Solicitud</span><span class="sxs-lookup"><span data-stu-id="4aba6-166">Request</span></span>
<span data-ttu-id="4aba6-167">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="4aba6-167">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceSettingStateSummaries
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

### <a name="response"></a><span data-ttu-id="4aba6-168">Respuesta</span><span class="sxs-lookup"><span data-stu-id="4aba6-168">Response</span></span>
<span data-ttu-id="4aba6-p103">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="4aba6-p103">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





