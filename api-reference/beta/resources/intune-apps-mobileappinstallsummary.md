---
title: tipo de recurso mobileAppInstallSummary
description: Contiene las propiedades para el resumen de la instalación de una aplicación móvil.
ms.openlocfilehash: bda3f798a86b38ca0d1224ce509c355a8aec998a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083624"
---
# <a name="mobileappinstallsummary-resource-type"></a><span data-ttu-id="48158-103">tipo de recurso mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="48158-103">mobileAppInstallSummary resource type</span></span>

> <span data-ttu-id="48158-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="48158-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="48158-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="48158-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="48158-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="48158-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="48158-107">Contiene las propiedades para el resumen de la instalación de una aplicación móvil.</span><span class="sxs-lookup"><span data-stu-id="48158-107">Contains properties for the installation summary of a mobile app.</span></span>
## <a name="methods"></a><span data-ttu-id="48158-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="48158-108">Methods</span></span>
|<span data-ttu-id="48158-109">Método</span><span class="sxs-lookup"><span data-stu-id="48158-109">Method</span></span>|<span data-ttu-id="48158-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48158-110">Return Type</span></span>|<span data-ttu-id="48158-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="48158-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="48158-112">Obtener mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="48158-112">Get mobileAppInstallSummary</span></span>](../api/intune-apps-mobileappinstallsummary-get.md)|[<span data-ttu-id="48158-113">mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="48158-113">mobileAppInstallSummary</span></span>](../resources/intune-apps-mobileappinstallsummary.md)|<span data-ttu-id="48158-114">Leer las propiedades y las relaciones del objeto [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="48158-114">Read properties and relationships of the [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) object.</span></span>|
|[<span data-ttu-id="48158-115">Actualizar mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="48158-115">Update mobileAppInstallSummary</span></span>](../api/intune-apps-mobileappinstallsummary-update.md)|[<span data-ttu-id="48158-116">mobileAppInstallSummary</span><span class="sxs-lookup"><span data-stu-id="48158-116">mobileAppInstallSummary</span></span>](../resources/intune-apps-mobileappinstallsummary.md)|<span data-ttu-id="48158-117">Actualizar las propiedades de un objeto [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) .</span><span class="sxs-lookup"><span data-stu-id="48158-117">Update the properties of a [mobileAppInstallSummary](../resources/intune-apps-mobileappinstallsummary.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="48158-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48158-118">Properties</span></span>
|<span data-ttu-id="48158-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="48158-119">Property</span></span>|<span data-ttu-id="48158-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="48158-120">Type</span></span>|<span data-ttu-id="48158-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="48158-121">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="48158-122">id</span><span class="sxs-lookup"><span data-stu-id="48158-122">id</span></span>|<span data-ttu-id="48158-123">String</span><span class="sxs-lookup"><span data-stu-id="48158-123">String</span></span>|<span data-ttu-id="48158-124">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="48158-124">Key of the entity.</span></span>|
|<span data-ttu-id="48158-125">installedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="48158-125">installedDeviceCount</span></span>|<span data-ttu-id="48158-126">Int32</span><span class="sxs-lookup"><span data-stu-id="48158-126">Int32</span></span>|<span data-ttu-id="48158-127">Número de dispositivos que haya instalado correctamente esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="48158-127">Number of Devices that have successfully installed this app.</span></span>|
|<span data-ttu-id="48158-128">failedDeviceCount</span><span class="sxs-lookup"><span data-stu-id="48158-128">failedDeviceCount</span></span>|<span data-ttu-id="48158-129">Int32</span><span class="sxs-lookup"><span data-stu-id="48158-129">Int32</span></span>|<span data-ttu-id="48158-130">Número de dispositivos que no haya podido instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="48158-130">Number of Devices that have failed to install this app.</span></span>|
|<span data-ttu-id="48158-131">notApplicableDeviceCount</span><span class="sxs-lookup"><span data-stu-id="48158-131">notApplicableDeviceCount</span></span>|<span data-ttu-id="48158-132">Int32</span><span class="sxs-lookup"><span data-stu-id="48158-132">Int32</span></span>|<span data-ttu-id="48158-133">Número de dispositivos que no son aplicables para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="48158-133">Number of Devices that are not applicable for this app.</span></span>|
|<span data-ttu-id="48158-134">notInstalledDeviceCount</span><span class="sxs-lookup"><span data-stu-id="48158-134">notInstalledDeviceCount</span></span>|<span data-ttu-id="48158-135">Int32</span><span class="sxs-lookup"><span data-stu-id="48158-135">Int32</span></span>|<span data-ttu-id="48158-136">Número de dispositivos que no tienen esta aplicación instalada.</span><span class="sxs-lookup"><span data-stu-id="48158-136">Number of Devices that does not have this app installed.</span></span>|
|<span data-ttu-id="48158-137">pendingInstallDeviceCount</span><span class="sxs-lookup"><span data-stu-id="48158-137">pendingInstallDeviceCount</span></span>|<span data-ttu-id="48158-138">Int32</span><span class="sxs-lookup"><span data-stu-id="48158-138">Int32</span></span>|<span data-ttu-id="48158-139">Número de dispositivos que hayan sido notificados para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="48158-139">Number of Devices that have been notified to install this app.</span></span>|
|<span data-ttu-id="48158-140">installedUserCount</span><span class="sxs-lookup"><span data-stu-id="48158-140">installedUserCount</span></span>|<span data-ttu-id="48158-141">Int32</span><span class="sxs-lookup"><span data-stu-id="48158-141">Int32</span></span>|<span data-ttu-id="48158-142">Número de usuarios cuyos dispositivos han correctas para instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="48158-142">Number of Users whose devices have all succeeded to install this app.</span></span>|
|<span data-ttu-id="48158-143">failedUserCount</span><span class="sxs-lookup"><span data-stu-id="48158-143">failedUserCount</span></span>|<span data-ttu-id="48158-144">Int32</span><span class="sxs-lookup"><span data-stu-id="48158-144">Int32</span></span>|<span data-ttu-id="48158-145">Número de usuarios que tienen 1 o más dispositivos que no se pudo instalar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="48158-145">Number of Users that have 1 or more device that failed to install this app.</span></span>|
|<span data-ttu-id="48158-146">notApplicableUserCount</span><span class="sxs-lookup"><span data-stu-id="48158-146">notApplicableUserCount</span></span>|<span data-ttu-id="48158-147">Int32</span><span class="sxs-lookup"><span data-stu-id="48158-147">Int32</span></span>|<span data-ttu-id="48158-148">Número de usuarios cuyos dispositivos no eran aplicables para esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="48158-148">Number of Users whose devices were all not applicable for this app.</span></span>|
|<span data-ttu-id="48158-149">notInstalledUserCount</span><span class="sxs-lookup"><span data-stu-id="48158-149">notInstalledUserCount</span></span>|<span data-ttu-id="48158-150">Int32</span><span class="sxs-lookup"><span data-stu-id="48158-150">Int32</span></span>|<span data-ttu-id="48158-151">Número de usuarios que tienen 1 o más dispositivos que no se han instalado esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="48158-151">Number of Users that have 1 or more devices that did not install this app.</span></span>|
|<span data-ttu-id="48158-152">pendingInstallUserCount</span><span class="sxs-lookup"><span data-stu-id="48158-152">pendingInstallUserCount</span></span>|<span data-ttu-id="48158-153">Int32</span><span class="sxs-lookup"><span data-stu-id="48158-153">Int32</span></span>|<span data-ttu-id="48158-154">Número de usuarios que tienen 1 o más dispositivos que han sido notificados a instalar esta aplicación y de tener 0 dispositivos con errores.</span><span class="sxs-lookup"><span data-stu-id="48158-154">Number of Users that have 1 or more device that have been notified to install this app and have 0 devices with failures.</span></span>|

## <a name="relationships"></a><span data-ttu-id="48158-155">Relaciones</span><span class="sxs-lookup"><span data-stu-id="48158-155">Relationships</span></span>
<span data-ttu-id="48158-156">Ninguna</span><span class="sxs-lookup"><span data-stu-id="48158-156">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="48158-157">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="48158-157">JSON Representation</span></span>
<span data-ttu-id="48158-158">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="48158-158">Here is a JSON representation of the resource.</span></span>
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





