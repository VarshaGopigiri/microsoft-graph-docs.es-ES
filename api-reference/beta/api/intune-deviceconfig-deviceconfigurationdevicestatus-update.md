---
title: Actualizar deviceConfigurationDeviceStatus
description: Actualice las propiedades de un objeto deviceConfigurationDeviceStatus.
ms.openlocfilehash: 3f5671c8e5019e065fd9e085856f28c39fef60f3
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27085226"
---
# <a name="update-deviceconfigurationdevicestatus"></a><span data-ttu-id="f919d-103">Actualizar deviceConfigurationDeviceStatus</span><span class="sxs-lookup"><span data-stu-id="f919d-103">Update deviceConfigurationDeviceStatus</span></span>

> <span data-ttu-id="f919d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f919d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f919d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f919d-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f919d-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f919d-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f919d-107">Actualice las propiedades de un objeto [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="f919d-107">Update the properties of a [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="f919d-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="f919d-108">Prerequisites</span></span>
<span data-ttu-id="f919d-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="f919d-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="f919d-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="f919d-111">Permission type</span></span>|<span data-ttu-id="f919d-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="f919d-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="f919d-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="f919d-113">Delegated (work or school account)</span></span>|<span data-ttu-id="f919d-114">DeviceManagementConfiguration.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="f919d-114">DeviceManagementConfiguration.ReadWrite.All</span></span>|
|<span data-ttu-id="f919d-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="f919d-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="f919d-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f919d-116">Not supported.</span></span>|
|<span data-ttu-id="f919d-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="f919d-117">Application</span></span>|<span data-ttu-id="f919d-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="f919d-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="f919d-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="f919d-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses/{deviceConfigurationDeviceStatusId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/rootCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/identityCertificate/rootCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.iosScepCertificateProfile/rootCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.macOSScepCertificateProfile/rootCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsPhone81VpnConfiguration/identityCertificate/deviceStatuses/{deviceConfigurationDeviceStatusId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/identityCertificateForClientAuthentication/deviceStatuses/{deviceConfigurationDeviceStatusId}
PATCH /deviceManagement/deviceConfigurations/{deviceConfigurationId}/microsoft.graph.windowsWifiEnterpriseEAPConfiguration/rootCertificatesForServerValidation/{windows81TrustedRootCertificateId}/deviceStatuses/{deviceConfigurationDeviceStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="f919d-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="f919d-120">Request headers</span></span>
|<span data-ttu-id="f919d-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f919d-121">Header</span></span>|<span data-ttu-id="f919d-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f919d-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="f919d-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="f919d-123">Authorization</span></span>|<span data-ttu-id="f919d-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="f919d-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="f919d-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="f919d-125">Accept</span></span>|<span data-ttu-id="f919d-126">application/json</span><span class="sxs-lookup"><span data-stu-id="f919d-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="f919d-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="f919d-127">Request body</span></span>
<span data-ttu-id="f919d-128">En el cuerpo de la solicitud, especifique una representación JSON del objeto [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="f919d-128">In the request body, supply a JSON representation for the [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) object.</span></span>

<span data-ttu-id="f919d-129">En la tabla siguiente se muestran las propiedades necesarias para crear el objeto [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).</span><span class="sxs-lookup"><span data-stu-id="f919d-129">The following table shows the properties that are required when you create the [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md).</span></span>

|<span data-ttu-id="f919d-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f919d-130">Property</span></span>|<span data-ttu-id="f919d-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="f919d-131">Type</span></span>|<span data-ttu-id="f919d-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="f919d-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f919d-133">id</span><span class="sxs-lookup"><span data-stu-id="f919d-133">id</span></span>|<span data-ttu-id="f919d-134">String</span><span class="sxs-lookup"><span data-stu-id="f919d-134">String</span></span>|<span data-ttu-id="f919d-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f919d-135">Key of the entity.</span></span>|
|<span data-ttu-id="f919d-136">deviceDisplayName</span><span class="sxs-lookup"><span data-stu-id="f919d-136">deviceDisplayName</span></span>|<span data-ttu-id="f919d-137">String</span><span class="sxs-lookup"><span data-stu-id="f919d-137">String</span></span>|<span data-ttu-id="f919d-138">Nombre de dispositivo de DevicePolicyStatus.</span><span class="sxs-lookup"><span data-stu-id="f919d-138">Device name of the DevicePolicyStatus.</span></span>|
|<span data-ttu-id="f919d-139">userName</span><span class="sxs-lookup"><span data-stu-id="f919d-139">userName</span></span>|<span data-ttu-id="f919d-140">String</span><span class="sxs-lookup"><span data-stu-id="f919d-140">String</span></span>|<span data-ttu-id="f919d-141">El nombre de usuario que se está notificando</span><span class="sxs-lookup"><span data-stu-id="f919d-141">The User Name that is being reported</span></span>|
|<span data-ttu-id="f919d-142">deviceModel</span><span class="sxs-lookup"><span data-stu-id="f919d-142">deviceModel</span></span>|<span data-ttu-id="f919d-143">String</span><span class="sxs-lookup"><span data-stu-id="f919d-143">String</span></span>|<span data-ttu-id="f919d-144">El modelo de dispositivo que se está notificando</span><span class="sxs-lookup"><span data-stu-id="f919d-144">The device model that is being reported</span></span>|
|<span data-ttu-id="f919d-145">platform</span><span class="sxs-lookup"><span data-stu-id="f919d-145">platform</span></span>|<span data-ttu-id="f919d-146">Int32</span><span class="sxs-lookup"><span data-stu-id="f919d-146">Int32</span></span>|<span data-ttu-id="f919d-147">Plataforma del dispositivo que se notifica</span><span class="sxs-lookup"><span data-stu-id="f919d-147">Platform of the device that is being reported</span></span>|
|<span data-ttu-id="f919d-148">complianceGracePeriodExpirationDateTime</span><span class="sxs-lookup"><span data-stu-id="f919d-148">complianceGracePeriodExpirationDateTime</span></span>|<span data-ttu-id="f919d-149">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f919d-149">DateTimeOffset</span></span>|<span data-ttu-id="f919d-150">La fecha y hora en que expira el período de gracia de cumplimiento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="f919d-150">The DateTime when device compliance grace period expires</span></span>|
|<span data-ttu-id="f919d-151">status</span><span class="sxs-lookup"><span data-stu-id="f919d-151">status</span></span>|[<span data-ttu-id="f919d-152">complianceStatus</span><span class="sxs-lookup"><span data-stu-id="f919d-152">complianceStatus</span></span>](../resources/intune-shared-compliancestatus.md)|<span data-ttu-id="f919d-153">Estado de cumplimiento del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="f919d-153">Compliance status of the policy report.</span></span> <span data-ttu-id="f919d-154">Los valores posibles son: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict` y `notAssigned`.</span><span class="sxs-lookup"><span data-stu-id="f919d-154">Possible values are: `unknown`, `notApplicable`, `compliant`, `remediated`, `nonCompliant`, `error`, `conflict`, `notAssigned`.</span></span>|
|<span data-ttu-id="f919d-155">lastReportedDateTime</span><span class="sxs-lookup"><span data-stu-id="f919d-155">lastReportedDateTime</span></span>|<span data-ttu-id="f919d-156">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="f919d-156">DateTimeOffset</span></span>|<span data-ttu-id="f919d-157">Fecha y hora de la última modificación del informe de directiva.</span><span class="sxs-lookup"><span data-stu-id="f919d-157">Last modified date time of the policy report.</span></span>|
|<span data-ttu-id="f919d-158">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f919d-158">userPrincipalName</span></span>|<span data-ttu-id="f919d-159">String</span><span class="sxs-lookup"><span data-stu-id="f919d-159">String</span></span>|<span data-ttu-id="f919d-160">UserPrincipalName.</span><span class="sxs-lookup"><span data-stu-id="f919d-160">UserPrincipalName.</span></span>|



## <a name="response"></a><span data-ttu-id="f919d-161">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f919d-161">Response</span></span>
<span data-ttu-id="f919d-162">Si se ejecuta correctamente, este método devuelve un código de respuesta `200 OK` y un objeto [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) actualizado en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="f919d-162">If successful, this method returns a `200 OK` response code and an updated [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="f919d-163">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="f919d-163">Example</span></span>
### <a name="request"></a><span data-ttu-id="f919d-164">Solicitud</span><span class="sxs-lookup"><span data-stu-id="f919d-164">Request</span></span>
<span data-ttu-id="f919d-165">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="f919d-165">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceManagement/deviceConfigurations/{deviceConfigurationId}/deviceStatuses/{deviceConfigurationDeviceStatusId}
Content-type: application/json
Content-length: 377

{
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "platform": 8,
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```

### <a name="response"></a><span data-ttu-id="f919d-166">Respuesta</span><span class="sxs-lookup"><span data-stu-id="f919d-166">Response</span></span>
<span data-ttu-id="f919d-p104">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="f919d-p104">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 496

{
  "@odata.type": "#microsoft.graph.deviceConfigurationDeviceStatus",
  "id": "674e98e5-98e5-674e-e598-4e67e5984e67",
  "deviceDisplayName": "Device Display Name value",
  "userName": "User Name value",
  "deviceModel": "Device Model value",
  "platform": 8,
  "complianceGracePeriodExpirationDateTime": "2016-12-31T23:56:44.951111-08:00",
  "status": "notApplicable",
  "lastReportedDateTime": "2017-01-01T00:00:17.7769392-08:00",
  "userPrincipalName": "User Principal Name value"
}
```




