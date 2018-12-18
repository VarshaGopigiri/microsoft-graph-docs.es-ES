---
title: tipo de recurso userAppInstallStatus
description: Contiene las propiedades para el estado de instalación para un usuario.
author: tfitzmac
ms.openlocfilehash: 024fff32aac2a268a2e0bbec81a6d46b31012a11
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27302761"
---
# <a name="userappinstallstatus-resource-type"></a><span data-ttu-id="f142b-103">tipo de recurso userAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="f142b-103">userAppInstallStatus resource type</span></span>

> <span data-ttu-id="f142b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f142b-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f142b-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f142b-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="f142b-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="f142b-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="f142b-107">Contiene las propiedades para el estado de instalación para un usuario.</span><span class="sxs-lookup"><span data-stu-id="f142b-107">Contains properties for the installation status for a user.</span></span>
## <a name="methods"></a><span data-ttu-id="f142b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="f142b-108">Methods</span></span>
|<span data-ttu-id="f142b-109">Método</span><span class="sxs-lookup"><span data-stu-id="f142b-109">Method</span></span>|<span data-ttu-id="f142b-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f142b-110">Return Type</span></span>|<span data-ttu-id="f142b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="f142b-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="f142b-112">Lista userAppInstallStatuses</span><span class="sxs-lookup"><span data-stu-id="f142b-112">List userAppInstallStatuses</span></span>](../api/intune-apps-userappinstallstatus-list.md)|<span data-ttu-id="f142b-113">colección de [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md)</span><span class="sxs-lookup"><span data-stu-id="f142b-113">[userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) collection</span></span>|<span data-ttu-id="f142b-114">Propiedades de la lista y relaciones de los objetos [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="f142b-114">List properties and relationships of the [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) objects.</span></span>|
|[<span data-ttu-id="f142b-115">Obtener userAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="f142b-115">Get userAppInstallStatus</span></span>](../api/intune-apps-userappinstallstatus-get.md)|[<span data-ttu-id="f142b-116">userAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="f142b-116">userAppInstallStatus</span></span>](../resources/intune-apps-userappinstallstatus.md)|<span data-ttu-id="f142b-117">Leer las propiedades y las relaciones del objeto [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="f142b-117">Read properties and relationships of the [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) object.</span></span>|
|[<span data-ttu-id="f142b-118">Crear userAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="f142b-118">Create userAppInstallStatus</span></span>](../api/intune-apps-userappinstallstatus-create.md)|[<span data-ttu-id="f142b-119">userAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="f142b-119">userAppInstallStatus</span></span>](../resources/intune-apps-userappinstallstatus.md)|<span data-ttu-id="f142b-120">Crear un nuevo objeto [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="f142b-120">Create a new [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) object.</span></span>|
|[<span data-ttu-id="f142b-121">Eliminar userAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="f142b-121">Delete userAppInstallStatus</span></span>](../api/intune-apps-userappinstallstatus-delete.md)|<span data-ttu-id="f142b-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f142b-122">None</span></span>|<span data-ttu-id="f142b-123">Elimina un [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md).</span><span class="sxs-lookup"><span data-stu-id="f142b-123">Deletes a [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md).</span></span>|
|[<span data-ttu-id="f142b-124">Actualizar userAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="f142b-124">Update userAppInstallStatus</span></span>](../api/intune-apps-userappinstallstatus-update.md)|[<span data-ttu-id="f142b-125">userAppInstallStatus</span><span class="sxs-lookup"><span data-stu-id="f142b-125">userAppInstallStatus</span></span>](../resources/intune-apps-userappinstallstatus.md)|<span data-ttu-id="f142b-126">Actualizar las propiedades de un objeto [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) .</span><span class="sxs-lookup"><span data-stu-id="f142b-126">Update the properties of a [userAppInstallStatus](../resources/intune-apps-userappinstallstatus.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="f142b-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f142b-127">Properties</span></span>
|<span data-ttu-id="f142b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f142b-128">Property</span></span>|<span data-ttu-id="f142b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="f142b-129">Type</span></span>|<span data-ttu-id="f142b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="f142b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f142b-131">id</span><span class="sxs-lookup"><span data-stu-id="f142b-131">id</span></span>|<span data-ttu-id="f142b-132">String</span><span class="sxs-lookup"><span data-stu-id="f142b-132">String</span></span>|<span data-ttu-id="f142b-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="f142b-133">Key of the entity.</span></span>|
|<span data-ttu-id="f142b-134">userName</span><span class="sxs-lookup"><span data-stu-id="f142b-134">userName</span></span>|<span data-ttu-id="f142b-135">String</span><span class="sxs-lookup"><span data-stu-id="f142b-135">String</span></span>|<span data-ttu-id="f142b-136">Nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="f142b-136">User name.</span></span>|
|<span data-ttu-id="f142b-137">userPrincipalName</span><span class="sxs-lookup"><span data-stu-id="f142b-137">userPrincipalName</span></span>|<span data-ttu-id="f142b-138">String</span><span class="sxs-lookup"><span data-stu-id="f142b-138">String</span></span>|<span data-ttu-id="f142b-139">Nombre Principal de usuario.</span><span class="sxs-lookup"><span data-stu-id="f142b-139">User Principal Name.</span></span>|
|<span data-ttu-id="f142b-140">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f142b-140">installedDeviceCount</span></span>|<span data-ttu-id="f142b-141">Int32</span><span class="sxs-lookup"><span data-stu-id="f142b-141">Int32</span></span>|<span data-ttu-id="f142b-142">Número de dispositivos instalados.</span><span class="sxs-lookup"><span data-stu-id="f142b-142">Installed Device Count.</span></span>|
|<span data-ttu-id="f142b-143">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f142b-143">failedDeviceCount</span></span>|<span data-ttu-id="f142b-144">Int32</span><span class="sxs-lookup"><span data-stu-id="f142b-144">Int32</span></span>|<span data-ttu-id="f142b-145">Número de dispositivos erróneos.</span><span class="sxs-lookup"><span data-stu-id="f142b-145">Failed Device Count.</span></span>|
|<span data-ttu-id="f142b-146">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="f142b-146">notInstalledDeviceCount</span></span>|<span data-ttu-id="f142b-147">Int32</span><span class="sxs-lookup"><span data-stu-id="f142b-147">Int32</span></span>|<span data-ttu-id="f142b-148">Número de dispositivos no instalados.</span><span class="sxs-lookup"><span data-stu-id="f142b-148">Not installed device count.</span></span>|

## <a name="relationships"></a><span data-ttu-id="f142b-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="f142b-149">Relationships</span></span>
|<span data-ttu-id="f142b-150">Relación</span><span class="sxs-lookup"><span data-stu-id="f142b-150">Relationship</span></span>|<span data-ttu-id="f142b-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="f142b-151">Type</span></span>|<span data-ttu-id="f142b-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="f142b-152">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="f142b-153">aplicación</span><span class="sxs-lookup"><span data-stu-id="f142b-153">app</span></span>|[<span data-ttu-id="f142b-154">mobileApp</span><span class="sxs-lookup"><span data-stu-id="f142b-154">mobileApp</span></span>](../resources/intune-apps-mobileapp.md)|<span data-ttu-id="f142b-155">El vínculo de navegación a la aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="f142b-155">The navigation link to the mobile app.</span></span>|
|<span data-ttu-id="f142b-156">deviceStatuses</span><span class="sxs-lookup"><span data-stu-id="f142b-156">deviceStatuses</span></span>|<span data-ttu-id="f142b-157">colección de [mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md)</span><span class="sxs-lookup"><span data-stu-id="f142b-157">[mobileAppInstallStatus](../resources/intune-apps-mobileappinstallstatus.md) collection</span></span>|<span data-ttu-id="f142b-158">El estado de instalación de la aplicación en los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="f142b-158">The install state of the app on devices.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f142b-159">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f142b-159">JSON Representation</span></span>
<span data-ttu-id="f142b-160">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f142b-160">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.userAppInstallStatus"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.userAppInstallStatus",
  "id": "String (identifier)",
  "userName": "String",
  "userPrincipalName": "String",
  "installedDeviceCount": 1024,
  "failedDeviceCount": 1024,
  "notInstalledDeviceCount": 1024
}
```





