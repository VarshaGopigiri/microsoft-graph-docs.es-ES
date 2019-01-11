---
title: Actualizar mobileAppInstallStatus
description: Actualizar las propiedades de un objeto mobileAppInstallStatus.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: a60bcf69ded37ea0b4a04430c6a837bb6df95100
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27817953"
---
# <a name="update-mobileappinstallstatus"></a><span data-ttu-id="a188a-103">Actualizar mobileAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="a188a-103">Update mobileAppInstallStatus</span></span>

> <span data-ttu-id="a188a-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a188a-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a188a-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a188a-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a188a-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a188a-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a188a-107">Actualizar las propiedades de un objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="a188a-107">Update the properties of a [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="a188a-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="a188a-108">Prerequisites</span></span>
<span data-ttu-id="a188a-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="a188a-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="a188a-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="a188a-111">Permission type</span></span>|<span data-ttu-id="a188a-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="a188a-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="a188a-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="a188a-113">Delegated (work or school account)</span></span>|<span data-ttu-id="a188a-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="a188a-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="a188a-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="a188a-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="a188a-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a188a-116">Not supported.</span></span>|
|<span data-ttu-id="a188a-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="a188a-117">Application</span></span>|<span data-ttu-id="a188a-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="a188a-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="a188a-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="a188a-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses/{mobileAppInstallStatusId}
PATCH /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/deviceStatuses/{mobileAppInstallStatusId}
```

## <a name="request-headers"></a><span data-ttu-id="a188a-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="a188a-120">Request headers</span></span>
|<span data-ttu-id="a188a-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a188a-121">Header</span></span>|<span data-ttu-id="a188a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a188a-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="a188a-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="a188a-123">Authorization</span></span>|<span data-ttu-id="a188a-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="a188a-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="a188a-125">Accept</span><span class="sxs-lookup"><span data-stu-id="a188a-125">Accept</span></span>|<span data-ttu-id="a188a-126">application/json</span><span class="sxs-lookup"><span data-stu-id="a188a-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="a188a-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="a188a-127">Request body</span></span>
<span data-ttu-id="a188a-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="a188a-128">In the request body, supply a JSON representation for the [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) object.</span></span>

<span data-ttu-id="a188a-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md).</span><span class="sxs-lookup"><span data-stu-id="a188a-129">The following table shows the properties that are required when you create the [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md).</span></span>

|<span data-ttu-id="a188a-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a188a-130">Property</span></span>|<span data-ttu-id="a188a-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="a188a-131">Type</span></span>|<span data-ttu-id="a188a-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="a188a-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a188a-133">id</span><span class="sxs-lookup"><span data-stu-id="a188a-133">id</span></span>|<span data-ttu-id="a188a-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="a188a-134">String</span></span>|<span data-ttu-id="a188a-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="a188a-135">Key of the entity.</span></span>|
|<span data-ttu-id="a188a-136">deviceName</span><span class="sxs-lookup"><span data-stu-id="a188a-136">deviceName</span></span>|<span data-ttu-id="a188a-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="a188a-137">String</span></span>|<span data-ttu-id="a188a-138">Nombre de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a188a-138">Device name</span></span>|
|<span data-ttu-id="a188a-139">deviceId</span><span class="sxs-lookup"><span data-stu-id="a188a-139">deviceId</span></span>|<span data-ttu-id="a188a-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="a188a-140">String</span></span>|<span data-ttu-id="a188a-141">Identificador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a188a-141">Device ID</span></span>|
|<span data-ttu-id="a188a-142">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="a188a-142">lastSyncDateTime</span></span>|<span data-ttu-id="a188a-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a188a-143">DateTimeOffset</span></span>|<span data-ttu-id="a188a-144">Fecha hora de última sincronización</span><span class="sxs-lookup"><span data-stu-id="a188a-144">Last sync date time</span></span>|
|<span data-ttu-id="a188a-145">mobileAppInstallStatusValue</span><span class="sxs-lookup"><span data-stu-id="a188a-145">mobileAppInstallStatusValue</span></span>|[<span data-ttu-id="a188a-146">resultantAppState</span><span class="sxs-lookup"><span data-stu-id="a188a-146">resultantAppState</span></span>](../resources/intune-shared-resultantappstate.md)|<span data-ttu-id="a188a-147">El estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a188a-147">The install state of the app.</span></span> <span data-ttu-id="a188a-148">Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.</span><span class="sxs-lookup"><span data-stu-id="a188a-148">Possible values are: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown`, `notApplicable`.</span></span>|
|<span data-ttu-id="a188a-149">installState</span><span class="sxs-lookup"><span data-stu-id="a188a-149">installState</span></span>|[<span data-ttu-id="a188a-150">resultantAppState</span><span class="sxs-lookup"><span data-stu-id="a188a-150">resultantAppState</span></span>](../resources/intune-shared-resultantappstate.md)|<span data-ttu-id="a188a-151">El estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a188a-151">The install state of the app.</span></span> <span data-ttu-id="a188a-152">Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.</span><span class="sxs-lookup"><span data-stu-id="a188a-152">Possible values are: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown`, `notApplicable`.</span></span>|
|<span data-ttu-id="a188a-153">installStateDetail</span><span class="sxs-lookup"><span data-stu-id="a188a-153">installStateDetail</span></span>|[<span data-ttu-id="a188a-154">resultantAppStateDetail</span><span class="sxs-lookup"><span data-stu-id="a188a-154">resultantAppStateDetail</span></span>](../resources/intune-apps-resultantappstatedetail.md)|<span data-ttu-id="a188a-155">Detalle de estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a188a-155">The install state detail of the app.</span></span> <span data-ttu-id="a188a-156">Los valores posibles son: `noAdditionalDetails`, `seeInstallErrorCode`, `seeUninstallErrorCode`, `pendingReboot`, `platformNotApplicable`, `minimumCpuSpeedNotMet`, `minimumLogicalProcessorCountNotMet`, `minimumPhysicalMemoryNotMet`, `minimumOsVersionNotMet`, `minimumDiskSpaceNotMet` y `processorArchitectureNotApplicable`.</span><span class="sxs-lookup"><span data-stu-id="a188a-156">Possible values are: `noAdditionalDetails`, `seeInstallErrorCode`, `seeUninstallErrorCode`, `pendingReboot`, `platformNotApplicable`, `minimumCpuSpeedNotMet`, `minimumLogicalProcessorCountNotMet`, `minimumPhysicalMemoryNotMet`, `minimumOsVersionNotMet`, `minimumDiskSpaceNotMet`, `processorArchitectureNotApplicable`.</span></span>|
|<span data-ttu-id="a188a-157">errorCode</span><span class="sxs-lookup"><span data-stu-id="a188a-157">errorCode</span></span>|<span data-ttu-id="a188a-158">Int32</span><span class="sxs-lookup"><span data-stu-id="a188a-158">Int32</span></span>|<span data-ttu-id="a188a-159">El error de código para la instalación o desinstalación de errores.</span><span class="sxs-lookup"><span data-stu-id="a188a-159">The error code for install or uninstall failures.</span></span>|
|<span data-ttu-id="a188a-160">osVersion</span><span class="sxs-lookup"><span data-stu-id="a188a-160">osVersion</span></span>|<span data-ttu-id="a188a-161">Cadena</span><span class="sxs-lookup"><span data-stu-id="a188a-161">String</span></span>|<span data-ttu-id="a188a-162">Versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a188a-162">OS Version</span></span>|
|<span data-ttu-id="a188a-163">osDescription</span><span class="sxs-lookup"><span data-stu-id="a188a-163">osDescription</span></span>|<span data-ttu-id="a188a-164">String</span><span class="sxs-lookup"><span data-stu-id="a188a-164">String</span></span>|<span data-ttu-id="a188a-165">Descripción del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a188a-165">OS Description</span></span>|
|<span data-ttu-id="a188a-166">userName</span><span class="sxs-lookup"><span data-stu-id="a188a-166">userName</span></span>|<span data-ttu-id="a188a-167">Cadena</span><span class="sxs-lookup"><span data-stu-id="a188a-167">String</span></span>|<span data-ttu-id="a188a-168">Nombre de usuario del dispositivo</span><span class="sxs-lookup"><span data-stu-id="a188a-168">Device User Name</span></span>|
|<span data-ttu-id="a188a-169">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a188a-169">userPrincipalName</span></span>|<span data-ttu-id="a188a-170">Cadena</span><span class="sxs-lookup"><span data-stu-id="a188a-170">String</span></span>|<span data-ttu-id="a188a-171">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="a188a-171">User Principal Name</span></span>|
|<span data-ttu-id="a188a-172">displayVersion</span><span class="sxs-lookup"><span data-stu-id="a188a-172">displayVersion</span></span>|<span data-ttu-id="a188a-173">Cadena</span><span class="sxs-lookup"><span data-stu-id="a188a-173">String</span></span>|<span data-ttu-id="a188a-174">Versión legible humano de la aplicación</span><span class="sxs-lookup"><span data-stu-id="a188a-174">Human readable version of the application</span></span>|



## <a name="response"></a><span data-ttu-id="a188a-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a188a-175">Response</span></span>
<span data-ttu-id="a188a-176">Si tiene éxito, este método devuelve una `200 OK` código de respuesta y un objeto actualizado [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="a188a-176">If successful, this method returns a `200 OK` response code and an updated [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="a188a-177">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="a188a-177">Example</span></span>
### <a name="request"></a><span data-ttu-id="a188a-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="a188a-178">Request</span></span>
<span data-ttu-id="a188a-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="a188a-179">Here is an example of the request.</span></span>
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

### <a name="response"></a><span data-ttu-id="a188a-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="a188a-180">Response</span></span>
<span data-ttu-id="a188a-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="a188a-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
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





