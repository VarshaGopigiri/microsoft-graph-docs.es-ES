---
title: tipo de recurso mobileAppInstallStatus
description: Contiene las propiedades para el estado de instalación de una aplicación para un dispositivo móvil.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: cac5c94f0669f784bf4cdd020448e40799d53915
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27982613"
---
# <a name="mobileappinstallstatus-resource-type"></a><span data-ttu-id="7dc95-103">tipo de recurso mobileAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="7dc95-103">mobileAppInstallStatus resource type</span></span>

> <span data-ttu-id="7dc95-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7dc95-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7dc95-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7dc95-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7dc95-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7dc95-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7dc95-107">Contiene las propiedades para el estado de instalación de una aplicación para un dispositivo móvil.</span><span class="sxs-lookup"><span data-stu-id="7dc95-107">Contains properties for the installation state of a mobile app for a device.</span></span>
## <a name="methods"></a><span data-ttu-id="7dc95-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7dc95-108">Methods</span></span>
|<span data-ttu-id="7dc95-109">Método</span><span class="sxs-lookup"><span data-stu-id="7dc95-109">Method</span></span>|<span data-ttu-id="7dc95-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7dc95-110">Return Type</span></span>|<span data-ttu-id="7dc95-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dc95-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="7dc95-112">Lista mobileAppInstallStatuses</span><span class="sxs-lookup"><span data-stu-id="7dc95-112">List mobileAppInstallStatuses</span></span>](../api/intune-apps-mobileappinstallstatus-list.md)|<span data-ttu-id="7dc95-113">colección de [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md)</span><span class="sxs-lookup"><span data-stu-id="7dc95-113">[mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) collection</span></span>|<span data-ttu-id="7dc95-114">Propiedades de la lista y relaciones de los objetos [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc95-114">List properties and relationships of the [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) objects.</span></span>|
|[<span data-ttu-id="7dc95-115">Obtener mobileAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="7dc95-115">Get mobileAppInstallStatus</span></span>](../api/intune-apps-mobileappinstallstatus-get.md)|[<span data-ttu-id="7dc95-116">mobileAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="7dc95-116">mobileAppInstallStatus</span></span>](../resources/intune-apps-mobileappinstallstatus.md)|<span data-ttu-id="7dc95-117">Leer las propiedades y las relaciones del objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc95-117">Read properties and relationships of the [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) object.</span></span>|
|[<span data-ttu-id="7dc95-118">Crear mobileAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="7dc95-118">Create mobileAppInstallStatus</span></span>](../api/intune-apps-mobileappinstallstatus-create.md)|[<span data-ttu-id="7dc95-119">mobileAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="7dc95-119">mobileAppInstallStatus</span></span>](../resources/intune-apps-mobileappinstallstatus.md)|<span data-ttu-id="7dc95-120">Crear un nuevo objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc95-120">Create a new [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) object.</span></span>|
|[<span data-ttu-id="7dc95-121">Eliminar mobileAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="7dc95-121">Delete mobileAppInstallStatus</span></span>](../api/intune-apps-mobileappinstallstatus-delete.md)|<span data-ttu-id="7dc95-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="7dc95-122">None</span></span>|<span data-ttu-id="7dc95-123">Elimina un [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md).</span><span class="sxs-lookup"><span data-stu-id="7dc95-123">Deletes a [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md).</span></span>|
|[<span data-ttu-id="7dc95-124">Actualizar mobileAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="7dc95-124">Update mobileAppInstallStatus</span></span>](../api/intune-apps-mobileappinstallstatus-update.md)|[<span data-ttu-id="7dc95-125">mobileAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="7dc95-125">mobileAppInstallStatus</span></span>](../resources/intune-apps-mobileappinstallstatus.md)|<span data-ttu-id="7dc95-126">Actualizar las propiedades de un objeto [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc95-126">Update the properties of a [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="7dc95-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7dc95-127">Properties</span></span>
|<span data-ttu-id="7dc95-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7dc95-128">Property</span></span>|<span data-ttu-id="7dc95-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="7dc95-129">Type</span></span>|<span data-ttu-id="7dc95-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dc95-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7dc95-131">id</span><span class="sxs-lookup"><span data-stu-id="7dc95-131">id</span></span>|<span data-ttu-id="7dc95-132">String</span><span class="sxs-lookup"><span data-stu-id="7dc95-132">String</span></span>|<span data-ttu-id="7dc95-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7dc95-133">Key of the entity.</span></span>|
|<span data-ttu-id="7dc95-134">deviceName</span><span class="sxs-lookup"><span data-stu-id="7dc95-134">deviceName</span></span>|<span data-ttu-id="7dc95-135">String</span><span class="sxs-lookup"><span data-stu-id="7dc95-135">String</span></span>|<span data-ttu-id="7dc95-136">Nombre de dispositivo</span><span class="sxs-lookup"><span data-stu-id="7dc95-136">Device name</span></span>|
|<span data-ttu-id="7dc95-137">deviceId</span><span class="sxs-lookup"><span data-stu-id="7dc95-137">deviceId</span></span>|<span data-ttu-id="7dc95-138">String</span><span class="sxs-lookup"><span data-stu-id="7dc95-138">String</span></span>|<span data-ttu-id="7dc95-139">Identificador de dispositivo</span><span class="sxs-lookup"><span data-stu-id="7dc95-139">Device ID</span></span>|
|<span data-ttu-id="7dc95-140">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="7dc95-140">lastSyncDateTime</span></span>|<span data-ttu-id="7dc95-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7dc95-141">DateTimeOffset</span></span>|<span data-ttu-id="7dc95-142">Fecha hora de última sincronización</span><span class="sxs-lookup"><span data-stu-id="7dc95-142">Last sync date time</span></span>|
|<span data-ttu-id="7dc95-143">mobileAppInstallStatusValue</span><span class="sxs-lookup"><span data-stu-id="7dc95-143">mobileAppInstallStatusValue</span></span>|[<span data-ttu-id="7dc95-144">resultantAppState</span><span class="sxs-lookup"><span data-stu-id="7dc95-144">resultantAppState</span></span>](../resources/intune-shared-resultantappstate.md)|<span data-ttu-id="7dc95-145">El estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dc95-145">The install state of the app.</span></span> <span data-ttu-id="7dc95-146">Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.</span><span class="sxs-lookup"><span data-stu-id="7dc95-146">Possible values are: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown`, `notApplicable`.</span></span>|
|<span data-ttu-id="7dc95-147">installState</span><span class="sxs-lookup"><span data-stu-id="7dc95-147">installState</span></span>|[<span data-ttu-id="7dc95-148">resultantAppState</span><span class="sxs-lookup"><span data-stu-id="7dc95-148">resultantAppState</span></span>](../resources/intune-shared-resultantappstate.md)|<span data-ttu-id="7dc95-149">El estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dc95-149">The install state of the app.</span></span> <span data-ttu-id="7dc95-150">Los valores posibles son: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown` y `notApplicable`.</span><span class="sxs-lookup"><span data-stu-id="7dc95-150">Possible values are: `installed`, `failed`, `notInstalled`, `uninstallFailed`, `pendingInstall`, `unknown`, `notApplicable`.</span></span>|
|<span data-ttu-id="7dc95-151">installStateDetail</span><span class="sxs-lookup"><span data-stu-id="7dc95-151">installStateDetail</span></span>|[<span data-ttu-id="7dc95-152">resultantAppStateDetail</span><span class="sxs-lookup"><span data-stu-id="7dc95-152">resultantAppStateDetail</span></span>](../resources/intune-apps-resultantappstatedetail.md)|<span data-ttu-id="7dc95-153">Detalle de estado de instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7dc95-153">The install state detail of the app.</span></span> <span data-ttu-id="7dc95-154">Los valores posibles son: `noAdditionalDetails`, `seeInstallErrorCode`, `seeUninstallErrorCode`, `pendingReboot`, `platformNotApplicable`, `minimumCpuSpeedNotMet`, `minimumLogicalProcessorCountNotMet`, `minimumPhysicalMemoryNotMet`, `minimumOsVersionNotMet`, `minimumDiskSpaceNotMet` y `processorArchitectureNotApplicable`.</span><span class="sxs-lookup"><span data-stu-id="7dc95-154">Possible values are: `noAdditionalDetails`, `seeInstallErrorCode`, `seeUninstallErrorCode`, `pendingReboot`, `platformNotApplicable`, `minimumCpuSpeedNotMet`, `minimumLogicalProcessorCountNotMet`, `minimumPhysicalMemoryNotMet`, `minimumOsVersionNotMet`, `minimumDiskSpaceNotMet`, `processorArchitectureNotApplicable`.</span></span>|
|<span data-ttu-id="7dc95-155">errorCode</span><span class="sxs-lookup"><span data-stu-id="7dc95-155">errorCode</span></span>|<span data-ttu-id="7dc95-156">Int32</span><span class="sxs-lookup"><span data-stu-id="7dc95-156">Int32</span></span>|<span data-ttu-id="7dc95-157">El error de código para la instalación o desinstalación de errores.</span><span class="sxs-lookup"><span data-stu-id="7dc95-157">The error code for install or uninstall failures.</span></span>|
|<span data-ttu-id="7dc95-158">osVersion</span><span class="sxs-lookup"><span data-stu-id="7dc95-158">osVersion</span></span>|<span data-ttu-id="7dc95-159">String</span><span class="sxs-lookup"><span data-stu-id="7dc95-159">String</span></span>|<span data-ttu-id="7dc95-160">Versión del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="7dc95-160">OS Version</span></span>|
|<span data-ttu-id="7dc95-161">osDescription</span><span class="sxs-lookup"><span data-stu-id="7dc95-161">osDescription</span></span>|<span data-ttu-id="7dc95-162">String</span><span class="sxs-lookup"><span data-stu-id="7dc95-162">String</span></span>|<span data-ttu-id="7dc95-163">Descripción del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="7dc95-163">OS Description</span></span>|
|<span data-ttu-id="7dc95-164">userName</span><span class="sxs-lookup"><span data-stu-id="7dc95-164">userName</span></span>|<span data-ttu-id="7dc95-165">String</span><span class="sxs-lookup"><span data-stu-id="7dc95-165">String</span></span>|<span data-ttu-id="7dc95-166">Nombre de usuario del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7dc95-166">Device User Name</span></span>|
|<span data-ttu-id="7dc95-167">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7dc95-167">userPrincipalName</span></span>|<span data-ttu-id="7dc95-168">String</span><span class="sxs-lookup"><span data-stu-id="7dc95-168">String</span></span>|<span data-ttu-id="7dc95-169">Nombre principal de usuario</span><span class="sxs-lookup"><span data-stu-id="7dc95-169">User Principal Name</span></span>|
|<span data-ttu-id="7dc95-170">displayVersion</span><span class="sxs-lookup"><span data-stu-id="7dc95-170">displayVersion</span></span>|<span data-ttu-id="7dc95-171">String</span><span class="sxs-lookup"><span data-stu-id="7dc95-171">String</span></span>|<span data-ttu-id="7dc95-172">Versión legible humano de la aplicación</span><span class="sxs-lookup"><span data-stu-id="7dc95-172">Human readable version of the application</span></span>|

## <a name="relationships"></a><span data-ttu-id="7dc95-173">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7dc95-173">Relationships</span></span>
|<span data-ttu-id="7dc95-174">Relación</span><span class="sxs-lookup"><span data-stu-id="7dc95-174">Relationship</span></span>|<span data-ttu-id="7dc95-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="7dc95-175">Type</span></span>|<span data-ttu-id="7dc95-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="7dc95-176">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7dc95-177">aplicación</span><span class="sxs-lookup"><span data-stu-id="7dc95-177">app</span></span>|[<span data-ttu-id="7dc95-178">mobileApp</span><span class="sxs-lookup"><span data-stu-id="7dc95-178">mobileApp</span></span>](../resources/intune-apps-mobileapp.md)|<span data-ttu-id="7dc95-179">El vínculo de navegación a la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="7dc95-179">The navigation link to the mobile app.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7dc95-180">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7dc95-180">JSON Representation</span></span>
<span data-ttu-id="7dc95-181">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7dc95-181">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppInstallStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppInstallStatus",
  "id": "String (identifier)",
  "deviceName": "String",
  "deviceId": "String",
  "lastSyncDateTime": "String (timestamp)",
  "mobileAppInstallStatusValue": "String",
  "installState": "String",
  "installStateDetail": "String",
  "errorCode": 1024,
  "osVersion": "String",
  "osDescription": "String",
  "userName": "String",
  "userPrincipalName": "String",
  "displayVersion": "String"
}
```





