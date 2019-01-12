---
title: tipo de recurso mobileAppInstallSummary
description: Contiene las propiedades para el resumen de la instalación de una aplicación móvil.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: a75dba8303d254aff911cc66931d52abb8b76c07
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27916029"
---
# <a name="mobileappinstallsummary-resource-type"></a><span data-ttu-id="7cc1e-103">tipo de recurso mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="7cc1e-103">mobileAppInstallSummary resource type</span></span>

> <span data-ttu-id="7cc1e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7cc1e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7cc1e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7cc1e-107">Contiene las propiedades para el resumen de la instalación de una aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-107">Contains properties for the installation summary of a mobile app.</span></span>
## <a name="methods"></a><span data-ttu-id="7cc1e-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="7cc1e-108">Methods</span></span>
|<span data-ttu-id="7cc1e-109">Método</span><span class="sxs-lookup"><span data-stu-id="7cc1e-109">Method</span></span>|<span data-ttu-id="7cc1e-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7cc1e-110">Return Type</span></span>|<span data-ttu-id="7cc1e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cc1e-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="7cc1e-112">Obtener mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="7cc1e-112">Get mobileAppInstallSummary</span></span>](../api/intune-apps-mobileappinstallsummary-get.md)|[<span data-ttu-id="7cc1e-113">mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="7cc1e-113">mobileAppInstallSummary</span></span>](../resources/intune-apps-mobileappinstallsummary.md)|<span data-ttu-id="7cc1e-114">Leer las propiedades y las relaciones del objeto [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="7cc1e-114">Read properties and relationships of the [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) object.</span></span>|
|[<span data-ttu-id="7cc1e-115">Actualizar mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="7cc1e-115">Update mobileAppInstallSummary</span></span>](../api/intune-apps-mobileappinstallsummary-update.md)|[<span data-ttu-id="7cc1e-116">mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="7cc1e-116">mobileAppInstallSummary</span></span>](../resources/intune-apps-mobileappinstallsummary.md)|<span data-ttu-id="7cc1e-117">Actualizar las propiedades de un objeto [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="7cc1e-117">Update the properties of a [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="7cc1e-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7cc1e-118">Properties</span></span>
|<span data-ttu-id="7cc1e-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7cc1e-119">Property</span></span>|<span data-ttu-id="7cc1e-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="7cc1e-120">Type</span></span>|<span data-ttu-id="7cc1e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="7cc1e-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7cc1e-122">id</span><span class="sxs-lookup"><span data-stu-id="7cc1e-122">id</span></span>|<span data-ttu-id="7cc1e-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="7cc1e-123">String</span></span>|<span data-ttu-id="7cc1e-124">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-124">Key of the entity.</span></span>|
|<span data-ttu-id="7cc1e-125">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="7cc1e-125">installedDeviceCount</span></span>|<span data-ttu-id="7cc1e-126">Int32</span><span class="sxs-lookup"><span data-stu-id="7cc1e-126">Int32</span></span>|<span data-ttu-id="7cc1e-127">Número de dispositivos que haya instalado correctamente esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-127">Number of Devices that have successfully installed this app.</span></span>|
|<span data-ttu-id="7cc1e-128">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="7cc1e-128">failedDeviceCount</span></span>|<span data-ttu-id="7cc1e-129">Int32</span><span class="sxs-lookup"><span data-stu-id="7cc1e-129">Int32</span></span>|<span data-ttu-id="7cc1e-130">Número de dispositivos que no haya podido instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-130">Number of Devices that have failed to install this app.</span></span>|
|<span data-ttu-id="7cc1e-131">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="7cc1e-131">notApplicableDeviceCount</span></span>|<span data-ttu-id="7cc1e-132">Int32</span><span class="sxs-lookup"><span data-stu-id="7cc1e-132">Int32</span></span>|<span data-ttu-id="7cc1e-133">Número de dispositivos que no son aplicables para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-133">Number of Devices that are not applicable for this app.</span></span>|
|<span data-ttu-id="7cc1e-134">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="7cc1e-134">notInstalledDeviceCount</span></span>|<span data-ttu-id="7cc1e-135">Int32</span><span class="sxs-lookup"><span data-stu-id="7cc1e-135">Int32</span></span>|<span data-ttu-id="7cc1e-136">Número de dispositivos que no tienen esta aplicación instalada.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-136">Number of Devices that does not have this app installed.</span></span>|
|<span data-ttu-id="7cc1e-137">pendingInstallDeviceCount</span><span class="sxs-lookup"><span data-stu-id="7cc1e-137">pendingInstallDeviceCount</span></span>|<span data-ttu-id="7cc1e-138">Int32</span><span class="sxs-lookup"><span data-stu-id="7cc1e-138">Int32</span></span>|<span data-ttu-id="7cc1e-139">Número de dispositivos que hayan sido notificados para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-139">Number of Devices that have been notified to install this app.</span></span>|
|<span data-ttu-id="7cc1e-140">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="7cc1e-140">installedUserCount</span></span>|<span data-ttu-id="7cc1e-141">Int32</span><span class="sxs-lookup"><span data-stu-id="7cc1e-141">Int32</span></span>|<span data-ttu-id="7cc1e-142">Número de usuarios cuyos dispositivos han correctas para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-142">Number of Users whose devices have all succeeded to install this app.</span></span>|
|<span data-ttu-id="7cc1e-143">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="7cc1e-143">failedUserCount</span></span>|<span data-ttu-id="7cc1e-144">Int32</span><span class="sxs-lookup"><span data-stu-id="7cc1e-144">Int32</span></span>|<span data-ttu-id="7cc1e-145">Número de usuarios que tienen 1 o más dispositivos que no se pudo instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-145">Number of Users that have 1 or more device that failed to install this app.</span></span>|
|<span data-ttu-id="7cc1e-146">notApplicableUserCount</span><span class="sxs-lookup"><span data-stu-id="7cc1e-146">notApplicableUserCount</span></span>|<span data-ttu-id="7cc1e-147">Int32</span><span class="sxs-lookup"><span data-stu-id="7cc1e-147">Int32</span></span>|<span data-ttu-id="7cc1e-148">Número de usuarios cuyos dispositivos no eran aplicables para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-148">Number of Users whose devices were all not applicable for this app.</span></span>|
|<span data-ttu-id="7cc1e-149">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="7cc1e-149">notInstalledUserCount</span></span>|<span data-ttu-id="7cc1e-150">Int32</span><span class="sxs-lookup"><span data-stu-id="7cc1e-150">Int32</span></span>|<span data-ttu-id="7cc1e-151">Número de usuarios que tienen 1 o más dispositivos que no se han instalado esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-151">Number of Users that have 1 or more devices that did not install this app.</span></span>|
|<span data-ttu-id="7cc1e-152">pendingInstallUserCount</span><span class="sxs-lookup"><span data-stu-id="7cc1e-152">pendingInstallUserCount</span></span>|<span data-ttu-id="7cc1e-153">Int32</span><span class="sxs-lookup"><span data-stu-id="7cc1e-153">Int32</span></span>|<span data-ttu-id="7cc1e-154">Número de usuarios que tienen 1 o más dispositivos que han sido notificados a instalar esta aplicación y de tener 0 dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-154">Number of Users that have 1 or more device that have been notified to install this app and have 0 devices with failures.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7cc1e-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7cc1e-155">Relationships</span></span>
<span data-ttu-id="7cc1e-156">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7cc1e-156">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="7cc1e-157">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7cc1e-157">JSON Representation</span></span>
<span data-ttu-id="7cc1e-158">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7cc1e-158">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.mobileAppInstallSummary"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.mobileAppInstallSummary",
  "id": "String (identifier)",
  "installedDeviceCount": 1024,
  "failedDeviceCount": 1024,
  "notApplicableDeviceCount": 1024,
  "notInstalledDeviceCount": 1024,
  "pendingInstallDeviceCount": 1024,
  "installedUserCount": 1024,
  "failedUserCount": 1024,
  "notApplicableUserCount": 1024,
  "notInstalledUserCount": 1024,
  "pendingInstallUserCount": 1024
}
```





