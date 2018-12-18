---
title: Crear mobileAppInstallStatus
description: Crear un nuevo objeto mobileAppInstallStatus.
author: tfitzmac
ms.openlocfilehash: 12dfa8e7f827ef2d2933249a6089d000ef868769
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27318112"
---
# <a name="create-mobileappinstallstatus"></a><span data-ttu-id="702fa-103">Crear mobileAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="702fa-103">Create mobileAppInstallStatus</span></span>

> <span data-ttu-id="702fa-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="702fa-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="702fa-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="702fa-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="702fa-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="702fa-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="702fa-107">Crear un nuevo objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="702fa-107">Create a new [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) object.</span></span>
## <a name="prerequisites"></a><span data-ttu-id="702fa-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="702fa-108">Prerequisites</span></span>
<span data-ttu-id="702fa-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](/graph/permissions-reference).</span><span class="sxs-lookup"><span data-stu-id="702fa-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](/graph/permissions-reference).</span></span>

|<span data-ttu-id="702fa-111">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="702fa-111">Permission type</span></span>|<span data-ttu-id="702fa-112">Permisos (de más a menos privilegiados)</span><span class="sxs-lookup"><span data-stu-id="702fa-112">Permissions (from most to least privileged)</span></span>|
|:---|:---|
|<span data-ttu-id="702fa-113">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="702fa-113">Delegated (work or school account)</span></span>|<span data-ttu-id="702fa-114">DeviceManagementApps.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="702fa-114">DeviceManagementApps.ReadWrite.All</span></span>|
|<span data-ttu-id="702fa-115">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="702fa-115">Delegated (personal Microsoft account)</span></span>|<span data-ttu-id="702fa-116">No admitida.</span><span class="sxs-lookup"><span data-stu-id="702fa-116">Not supported.</span></span>|
|<span data-ttu-id="702fa-117">Aplicación</span><span class="sxs-lookup"><span data-stu-id="702fa-117">Application</span></span>|<span data-ttu-id="702fa-118">No admitida.</span><span class="sxs-lookup"><span data-stu-id="702fa-118">Not supported.</span></span>|

## <a name="http-request"></a><span data-ttu-id="702fa-119">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="702fa-119">HTTP Request</span></span>
<!-- {
  "blockType": "ignored"
}
-->
``` http
POST /deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses
POST /deviceAppManagement/mobileApps/{mobileAppId}/userStatuses/{userAppInstallStatusId}/deviceStatuses
```

## <a name="request-headers"></a><span data-ttu-id="702fa-120">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="702fa-120">Request headers</span></span>
|<span data-ttu-id="702fa-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="702fa-121">Header</span></span>|<span data-ttu-id="702fa-122">Valor</span><span class="sxs-lookup"><span data-stu-id="702fa-122">Value</span></span>|
|:---|:---|
|<span data-ttu-id="702fa-123">Autorización</span><span class="sxs-lookup"><span data-stu-id="702fa-123">Authorization</span></span>|<span data-ttu-id="702fa-124">Se requiere &lt;token&gt; de portador.</span><span class="sxs-lookup"><span data-stu-id="702fa-124">Bearer &lt;token&gt; Required.</span></span>|
|<span data-ttu-id="702fa-125">Aceptar</span><span class="sxs-lookup"><span data-stu-id="702fa-125">Accept</span></span>|<span data-ttu-id="702fa-126">application/json</span><span class="sxs-lookup"><span data-stu-id="702fa-126">application/json</span></span>|

## <a name="request-body"></a><span data-ttu-id="702fa-127">Cuerpo de la solicitud</span><span class="sxs-lookup"><span data-stu-id="702fa-127">Request body</span></span>
<span data-ttu-id="702fa-128">En el cuerpo de la solicitud, proporcionar una representación de JSON para el objeto mobileAppInstallStatus.</span><span class="sxs-lookup"><span data-stu-id="702fa-128">In the request body, supply a JSON representation for the mobileAppInstallStatus object.</span></span>

<span data-ttu-id="702fa-129">La siguiente tabla muestran las propiedades que son necesarias cuando se crea el mobileAppInstallStatus.</span><span class="sxs-lookup"><span data-stu-id="702fa-129">The following table shows the properties that are required when you create the mobileAppInstallStatus.</span></span>

|<span data-ttu-id="702fa-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="702fa-130">Property</span></span>|<span data-ttu-id="702fa-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="702fa-131">Type</span></span>|<span data-ttu-id="702fa-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="702fa-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="702fa-133">id</span><span class="sxs-lookup"><span data-stu-id="702fa-133">id</span></span>|<span data-ttu-id="702fa-134">String</span><span class="sxs-lookup"><span data-stu-id="702fa-134">String</span></span>|<span data-ttu-id="702fa-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="702fa-135">Key of the entity.</span></span>|
|<span data-ttu-id="702fa-136">deviceName</span><span class="sxs-lookup"><span data-stu-id="702fa-136">deviceName</span></span>|<span data-ttu-id="702fa-137">String</span><span class="sxs-lookup"><span data-stu-id="702fa-137">String</span></span>|<span data-ttu-id="702fa-138">Nombre de dispositivo</span><span class="sxs-lookup"><span data-stu-id="702fa-138">Device name</span></span>|
|<span data-ttu-id="702fa-139">deviceId</span><span class="sxs-lookup"><span data-stu-id="702fa-139">deviceId</span></span>|<span data-ttu-id="702fa-140">String</span><span class="sxs-lookup"><span data-stu-id="702fa-140">String</span></span>|<span data-ttu-id="702fa-141">Identificador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="702fa-141">Device ID</span></span>|
|<span data-ttu-id="702fa-142">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="702fa-142">lastSyncDateTime</span></span>|<span data-ttu-id="702fa-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="702fa-143">DateTimeOffset</span></span>|<span data-ttu-id="702fa-144">Fecha hora de última sincronización</span><span class="sxs-lookup"><span data-stu-id="702fa-144">Last sync date time</span></span>|
|<span data-ttu-id="702fa-145">mobileAppInstallStatusValue</span><span class="sxs-lookup"><span data-stu-id="702fa-145">mobileAppInstallStatusValue</span></span>|[<span data-ttu-id="702fa-146">resultantAppState</span><span class="sxs-lookup"><span data-stu-id="702fa-146">resultantAppState</span></span>](../resources/intune-shared-resultantappstate.md)|<span data-ttu-id="702fa-147">El estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="702fa-147">The install state of the app.</span></span> <span data-ttu-id="702fa-148">Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.</span><span class="sxs-lookup"><span data-stu-id="702fa-148">Possible values are: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown`, `notApplicable`.</span></span>|
|<span data-ttu-id="702fa-149">installState</span><span class="sxs-lookup"><span data-stu-id="702fa-149">installState</span></span>|[<span data-ttu-id="702fa-150">resultantAppState</span><span class="sxs-lookup"><span data-stu-id="702fa-150">resultantAppState</span></span>](../resources/intune-shared-resultantappstate.md)|<span data-ttu-id="702fa-151">El estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="702fa-151">The install state of the app.</span></span> <span data-ttu-id="702fa-152">Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.</span><span class="sxs-lookup"><span data-stu-id="702fa-152">Possible values are: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown`, `notApplicable`.</span></span>|
|<span data-ttu-id="702fa-153">installStateDetail</span><span class="sxs-lookup"><span data-stu-id="702fa-153">installStateDetail</span></span>|[<span data-ttu-id="702fa-154">resultantAppStateDetail</span><span class="sxs-lookup"><span data-stu-id="702fa-154">resultantAppStateDetail</span></span>](../resources/intune-apps-resultantappstatedetail.md)|<span data-ttu-id="702fa-155">Detalle de estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="702fa-155">The install state detail of the app.</span></span> <span data-ttu-id="702fa-156">Los valores posibles son: `noAdditionalDetails`, `seeInstallErrorCode`, `seeUninstallErrorCode`, `pendingReboot`, `platformNotApplicable`, `minimumCpuSpeedNotMet`, `minimumLogicalProcessorCountNotMet`, `minimumPhysicalMemoryNotMet`, `minimumOsVersionNotMet`, `minimumDiskSpaceNotMet` y `processorArchitectureNotApplicable`.</span><span class="sxs-lookup"><span data-stu-id="702fa-156">Possible values are: `noAdditionalDetails`, `seeInstallErrorCode`, `seeUninstallErrorCode`, `pendingReboot`, `platformNotApplicable`, `minimumCpuSpeedNotMet`, `minimumLogicalProcessorCountNotMet`, `minimumPhysicalMemoryNotMet`, `minimumOsVersionNotMet`, `minimumDiskSpaceNotMet`, `processorArchitectureNotApplicable`.</span></span>|
|<span data-ttu-id="702fa-157">errorCode</span><span class="sxs-lookup"><span data-stu-id="702fa-157">errorCode</span></span>|<span data-ttu-id="702fa-158">Int32</span><span class="sxs-lookup"><span data-stu-id="702fa-158">Int32</span></span>|<span data-ttu-id="702fa-159">El error de código para la instalación o desinstalación de errores.</span><span class="sxs-lookup"><span data-stu-id="702fa-159">The error code for install or uninstall failures.</span></span>|
|<span data-ttu-id="702fa-160">osVersion</span><span class="sxs-lookup"><span data-stu-id="702fa-160">osVersion</span></span>|<span data-ttu-id="702fa-161">String</span><span class="sxs-lookup"><span data-stu-id="702fa-161">String</span></span>|<span data-ttu-id="702fa-162">Versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="702fa-162">OS Version</span></span>|
|<span data-ttu-id="702fa-163">osDescription</span><span class="sxs-lookup"><span data-stu-id="702fa-163">osDescription</span></span>|<span data-ttu-id="702fa-164">String</span><span class="sxs-lookup"><span data-stu-id="702fa-164">String</span></span>|<span data-ttu-id="702fa-165">Descripción del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="702fa-165">OS Description</span></span>|
|<span data-ttu-id="702fa-166">userName</span><span class="sxs-lookup"><span data-stu-id="702fa-166">userName</span></span>|<span data-ttu-id="702fa-167">String</span><span class="sxs-lookup"><span data-stu-id="702fa-167">String</span></span>|<span data-ttu-id="702fa-168">Nombre de usuario del dispositivo</span><span class="sxs-lookup"><span data-stu-id="702fa-168">Device User Name</span></span>|
|<span data-ttu-id="702fa-169">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="702fa-169">userPrincipalName</span></span>|<span data-ttu-id="702fa-170">String</span><span class="sxs-lookup"><span data-stu-id="702fa-170">String</span></span>|<span data-ttu-id="702fa-171">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="702fa-171">User Principal Name</span></span>|
|<span data-ttu-id="702fa-172">displayVersion</span><span class="sxs-lookup"><span data-stu-id="702fa-172">displayVersion</span></span>|<span data-ttu-id="702fa-173">String</span><span class="sxs-lookup"><span data-stu-id="702fa-173">String</span></span>|<span data-ttu-id="702fa-174">Versión legible humano de la aplicación</span><span class="sxs-lookup"><span data-stu-id="702fa-174">Human readable version of the application</span></span>|



## <a name="response"></a><span data-ttu-id="702fa-175">Respuesta</span><span class="sxs-lookup"><span data-stu-id="702fa-175">Response</span></span>
<span data-ttu-id="702fa-176">Si tiene éxito, este método devuelve una `201 Created` código de respuesta y un objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="702fa-176">If successful, this method returns a `201 Created` response code and a [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) object in the response body.</span></span>

## <a name="example"></a><span data-ttu-id="702fa-177">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="702fa-177">Example</span></span>
### <a name="request"></a><span data-ttu-id="702fa-178">Solicitud</span><span class="sxs-lookup"><span data-stu-id="702fa-178">Request</span></span>
<span data-ttu-id="702fa-179">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="702fa-179">Here is an example of the request.</span></span>
``` http
POST https://graph.microsoft.com/beta/deviceAppManagement/mobileApps/{mobileAppId}/deviceStatuses
Content-type: application/json
Content-length: 549

{
  "@odata.type": "#microsoft.graph.mobileAppInstallStatus",
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

### <a name="response"></a><span data-ttu-id="702fa-180">Respuesta</span><span class="sxs-lookup"><span data-stu-id="702fa-180">Response</span></span>
<span data-ttu-id="702fa-p106">Aquí tiene un ejemplo de la respuesta. Nota: Puede que el objeto de respuesta que aparece aquí se trunque para abreviar. Todas las propiedades se devolverán de una llamada real.</span><span class="sxs-lookup"><span data-stu-id="702fa-p106">Here is an example of the response. Note: The response object shown here may be truncated for brevity. All of the properties will be returned from an actual call.</span></span>
``` http
HTTP/1.1 201 Created
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





