---
title: Actualizar mobileAppInstallStatus
description: Actualizar las propiedades de un objeto mobileAppInstallStatus.
ms.openlocfilehash: bb3df95caeed90a883e2323898080a23c742f5eb
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090238"
---
# <a name="update-mobileappinstallstatus"></a><span data-ttu-id="5dd15-103">Actualizar mobileAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="5dd15-103">Update mobileAppInstallStatus</span></span>

> <span data-ttu-id="5dd15-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5dd15-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5dd15-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5dd15-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="5dd15-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="5dd15-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="5dd15-107">Actualizar las propiedades de un objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd15-107">Update the properties of a [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="5dd15-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="5dd15-108">Prerequisites</span></span>
<span data-ttu-id="5dd15-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="5dd15-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="5dd15-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="5dd15-111">Permission type</span></span>|<span data-ttu-id="5dd15-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="5dd15-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="5dd15-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="5dd15-113">Delegated (work or school account)</span></span>|<span data-ttu-id="5dd15-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="5dd15-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="5dd15-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="5dd15-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="5dd15-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5dd15-116">Not supported.</span></span>|
|<span data-ttu-id="5dd15-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="5dd15-117">Application</span></span>|<span data-ttu-id="5dd15-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="5dd15-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="5dd15-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="5dd15-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/deviceStatuses/{mobileAppInstallStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="5dd15-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="5dd15-120">Request headers</span></span>
|<span data-ttu-id="5dd15-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5dd15-121">Header</span></span>|<span data-ttu-id="5dd15-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5dd15-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="5dd15-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="5dd15-123">Authorization</span></span>|<span data-ttu-id="5dd15-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="5dd15-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="5dd15-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="5dd15-125">Accept</span></span>|<span data-ttu-id="5dd15-126">application/json</span><span class="sxs-lookup"><span data-stu-id="5dd15-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="5dd15-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="5dd15-127">Request body</span></span>
<span data-ttu-id="5dd15-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="5dd15-128">In the request body, supply a JSON representation for the [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) object.</span></span>

<span data-ttu-id="5dd15-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md).</span><span class="sxs-lookup"><span data-stu-id="5dd15-129">The following table shows the properties that are required when you create the [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md).</span></span>

|<span data-ttu-id="5dd15-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5dd15-130">Property</span></span>|<span data-ttu-id="5dd15-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="5dd15-131">Type</span></span>|<span data-ttu-id="5dd15-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="5dd15-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="5dd15-133">id</span><span class="sxs-lookup"><span data-stu-id="5dd15-133">id</span></span>|<span data-ttu-id="5dd15-134">String</span><span class="sxs-lookup"><span data-stu-id="5dd15-134">String</span></span>|<span data-ttu-id="5dd15-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="5dd15-135">Key of the entity.</span></span>|
|<span data-ttu-id="5dd15-136">deviceName</span><span class="sxs-lookup"><span data-stu-id="5dd15-136">deviceName</span></span>|<span data-ttu-id="5dd15-137">String</span><span class="sxs-lookup"><span data-stu-id="5dd15-137">String</span></span>|<span data-ttu-id="5dd15-138">Nombre de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5dd15-138">Device name</span></span>|
|<span data-ttu-id="5dd15-139">deviceId</span><span class="sxs-lookup"><span data-stu-id="5dd15-139">deviceId</span></span>|<span data-ttu-id="5dd15-140">String</span><span class="sxs-lookup"><span data-stu-id="5dd15-140">String</span></span>|<span data-ttu-id="5dd15-141">Identificador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="5dd15-141">Device ID</span></span>|
|<span data-ttu-id="5dd15-142">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="5dd15-142">lastSyncDateTime</span></span>|<span data-ttu-id="5dd15-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="5dd15-143">DateTimeOffset</span></span>|<span data-ttu-id="5dd15-144">Fecha hora de última sincronización</span><span class="sxs-lookup"><span data-stu-id="5dd15-144">Last sync date time</span></span>|
|<span data-ttu-id="5dd15-145">mobileAppInstallStatusValue</span><span class="sxs-lookup"><span data-stu-id="5dd15-145">mobileAppInstallStatusValue</span></span>|[<span data-ttu-id="5dd15-146">resultantAppState</span><span class="sxs-lookup"><span data-stu-id="5dd15-146">resultantAppState</span></span>](../resources/intune-shared-resultantappstate.md)|<span data-ttu-id="5dd15-147">El estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5dd15-147">The install state of the app.</span></span> <span data-ttu-id="5dd15-148">Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.</span><span class="sxs-lookup"><span data-stu-id="5dd15-148">Possible values are: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown`, `notApplicable`.</span></span>|
|<span data-ttu-id="5dd15-149">installState</span><span class="sxs-lookup"><span data-stu-id="5dd15-149">installState</span></span>|[<span data-ttu-id="5dd15-150">resultantAppState</span><span class="sxs-lookup"><span data-stu-id="5dd15-150">resultantAppState</span></span>](../resources/intune-shared-resultantappstate.md)|<span data-ttu-id="5dd15-151">El estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5dd15-151">The install state of the app.</span></span> <span data-ttu-id="5dd15-152">Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.</span><span class="sxs-lookup"><span data-stu-id="5dd15-152">Possible values are: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown`, `notApplicable`.</span></span>|
|<span data-ttu-id="5dd15-153">installStateDetail</span><span class="sxs-lookup"><span data-stu-id="5dd15-153">installStateDetail</span></span>|[<span data-ttu-id="5dd15-154">resultantAppStateDetail</span><span class="sxs-lookup"><span data-stu-id="5dd15-154">resultantAppStateDetail</span></span>](../resources/intune-apps-resultantappstatedetail.md)|<span data-ttu-id="5dd15-155">Detalle de estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5dd15-155">The install state detail of the app.</span></span> <span data-ttu-id="5dd15-156">Los valores posibles son: `noAdditionalDetails`, `seeInstallErrorCode`, `seeUninstallErrorCode`, `pendingReboot`, `platformNotApplicable`, `minimumCpuSpeedNotMet`, `minimumLogicalProcessorCountNotMet`, `minimumPhysicalMemoryNotMet`, `minimumOsVersionNotMet`, `minimumDiskSpaceNotMet` y `processorArchitectureNotApplicable`.</span><span class="sxs-lookup"><span data-stu-id="5dd15-156">Possible values are: `noAdditionalDetails`, `seeInstallErrorCode`, `seeUninstallErrorCode`, `pendingReboot`, `platformNotApplicable`, `minimumCpuSpeedNotMet`, `minimumLogicalProcessorCountNotMet`, `minimumPhysicalMemoryNotMet`, `minimumOsVersionNotMet`, `minimumDiskSpaceNotMet`, `processorArchitectureNotApplicable`.</span></span>|
|<span data-ttu-id="5dd15-157">errorCode</span><span class="sxs-lookup"><span data-stu-id="5dd15-157">errorCode</span></span>|<span data-ttu-id="5dd15-158">Int32</span><span class="sxs-lookup"><span data-stu-id="5dd15-158">Int32</span></span>|<span data-ttu-id="5dd15-159">El error de código para la instalación o desinstalación de errores.</span><span class="sxs-lookup"><span data-stu-id="5dd15-159">The error code for install or uninstall failures.</span></span>|
|<span data-ttu-id="5dd15-160">osVersion</span><span class="sxs-lookup"><span data-stu-id="5dd15-160">osVersion</span></span>|<span data-ttu-id="5dd15-161">String</span><span class="sxs-lookup"><span data-stu-id="5dd15-161">String</span></span>|<span data-ttu-id="5dd15-162">Versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="5dd15-162">OS Version</span></span>|
|<span data-ttu-id="5dd15-163">osDescription</span><span class="sxs-lookup"><span data-stu-id="5dd15-163">osDescription</span></span>|<span data-ttu-id="5dd15-164">String</span><span class="sxs-lookup"><span data-stu-id="5dd15-164">String</span></span>|<span data-ttu-id="5dd15-165">Descripción del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="5dd15-165">OS Description</span></span>|
|<span data-ttu-id="5dd15-166">userName</span><span class="sxs-lookup"><span data-stu-id="5dd15-166">userName</span></span>|<span data-ttu-id="5dd15-167">String</span><span class="sxs-lookup"><span data-stu-id="5dd15-167">String</span></span>|<span data-ttu-id="5dd15-168">Nombre de usuario del dispositivo</span><span class="sxs-lookup"><span data-stu-id="5dd15-168">Device User Name</span></span>|
|<span data-ttu-id="5dd15-169">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="5dd15-169">userPrincipalName</span></span>|<span data-ttu-id="5dd15-170">String</span><span class="sxs-lookup"><span data-stu-id="5dd15-170">String</span></span>|<span data-ttu-id="5dd15-171">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="5dd15-171">User Principal Name</span></span>|
|<span data-ttu-id="5dd15-172">displayVersion</span><span class="sxs-lookup"><span data-stu-id="5dd15-172">displayVersion</span></span>|<span data-ttu-id="5dd15-173">String</span><span class="sxs-lookup"><span data-stu-id="5dd15-173">String</span></span>|<span data-ttu-id="5dd15-174">Versión legible humano de la aplicación</span><span class="sxs-lookup"><span data-stu-id="5dd15-174">Human readable version of the application</span></span>|



## <a name="response"></a><span data-ttu-id="5dd15-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5dd15-175">Response</span></span>
<span data-ttu-id="5dd15-176">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="5dd15-176">If successful, this method returns a `200 OK` response code and an updated [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="5dd15-177">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="5dd15-177">Example</span></span>
### <a name="request"></a><span data-ttu-id="5dd15-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="5dd15-178">Request</span></span>
<span data-ttu-id="5dd15-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="5dd15-179">Here is an example of the request.</span></span>
``` http
PATCH https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}
Content-type: application/json
Content-length: 488

{
  "deviceName": "Device Name value",
  "deviceId": "Device Id value",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "mobileAppInstallStatusValue": "failed",
  "installState": "failed",
  "installStateDetail": "seeInstallErrorCode",
  "errorCode": 9,
  "osVersion": "Os Version value",
  "osDescription": "Os Description value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "displayVersion": "Display Version value"
}
```

### <a name="response"></a><span data-ttu-id="5dd15-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="5dd15-180">Response</span></span>
<span data-ttu-id="5dd15-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="5dd15-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 200 OK
Content-Type: application/json
Content-Length: 598

{
  "@odata.type": "#microsoft.graph.mobileAppInstallStatus",
  "id": "7560ee45-ee45-7560-45ee-607545ee6075",
  "deviceName": "Device Name value",
  "deviceId": "Device Id value",
  "lastSyncDateTime": "2017-01-01T00:02:49.3205976-08:00",
  "mobileAppInstallStatusValue": "failed",
  "installState": "failed",
  "installStateDetail": "seeInstallErrorCode",
  "errorCode": 9,
  "osVersion": "Os Version value",
  "osDescription": "Os Description value",
  "userName": "User Name value",
  "userPrincipalName": "User Principal Name value",
  "displayVersion": "Display Version value"
}
```





