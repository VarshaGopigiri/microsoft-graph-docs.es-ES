---
title: Tipo de recurso deviceInstallState
description: Contiene las propiedades del estado de la instalación para un dispositivo.
author: tfitzmac
ms.openlocfilehash: fb11f93682093655a38ac554b2816348f9b0c6bc
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27360372"
---
# <a name="deviceinstallstate-resource-type"></a><span data-ttu-id="c2dd9-103">Tipo de recurso deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="c2dd9-103">deviceInstallState resource type</span></span>

> <span data-ttu-id="c2dd9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="c2dd9-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="c2dd9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="c2dd9-107">Contiene las propiedades del estado de la instalación para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-107">Contains properties for the installation state for a device.</span></span>
## <a name="methods"></a><span data-ttu-id="c2dd9-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c2dd9-108">Methods</span></span>
|<span data-ttu-id="c2dd9-109">Método</span><span class="sxs-lookup"><span data-stu-id="c2dd9-109">Method</span></span>|<span data-ttu-id="c2dd9-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c2dd9-110">Return Type</span></span>|<span data-ttu-id="c2dd9-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2dd9-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="c2dd9-112">Enumerar deviceInstallStates</span><span class="sxs-lookup"><span data-stu-id="c2dd9-112">List deviceInstallStates</span></span>](../api/intune-books-deviceinstallstate-list.md)|<span data-ttu-id="c2dd9-113">Colección [deviceInstallState](../resources/intune-books-deviceinstallstate.md)</span><span class="sxs-lookup"><span data-stu-id="c2dd9-113">[deviceInstallState](../resources/intune-books-deviceinstallstate.md) collection</span></span>|<span data-ttu-id="c2dd9-114">Enumere las propiedades y las relaciones de los objetos [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="c2dd9-114">List properties and relationships of the [deviceInstallState](../resources/intune-books-deviceinstallstate.md) objects.</span></span>|
|[<span data-ttu-id="c2dd9-115">Obtener deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="c2dd9-115">Get deviceInstallState</span></span>](../api/intune-books-deviceinstallstate-get.md)|[<span data-ttu-id="c2dd9-116">deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="c2dd9-116">deviceInstallState</span></span>](../resources/intune-books-deviceinstallstate.md)|<span data-ttu-id="c2dd9-117">Lea las propiedades y las relaciones del objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="c2dd9-117">Read properties and relationships of the [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object.</span></span>|
|[<span data-ttu-id="c2dd9-118">Crear deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="c2dd9-118">Create deviceInstallState</span></span>](../api/intune-books-deviceinstallstate-create.md)|[<span data-ttu-id="c2dd9-119">deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="c2dd9-119">deviceInstallState</span></span>](../resources/intune-books-deviceinstallstate.md)|<span data-ttu-id="c2dd9-120">Cree un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="c2dd9-120">Create a new [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object.</span></span>|
|[<span data-ttu-id="c2dd9-121">Eliminar deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="c2dd9-121">Delete deviceInstallState</span></span>](../api/intune-books-deviceinstallstate-delete.md)|<span data-ttu-id="c2dd9-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c2dd9-122">None</span></span>|<span data-ttu-id="c2dd9-123">Elimina un [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="c2dd9-123">Deletes a [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span></span>|
|[<span data-ttu-id="c2dd9-124">Actualizar deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="c2dd9-124">Update deviceInstallState</span></span>](../api/intune-books-deviceinstallstate-update.md)|[<span data-ttu-id="c2dd9-125">deviceInstallState</span><span class="sxs-lookup"><span data-stu-id="c2dd9-125">deviceInstallState</span></span>](../resources/intune-books-deviceinstallstate.md)|<span data-ttu-id="c2dd9-126">Actualice las propiedades de un objeto [deviceInstallState](../resources/intune-books-deviceinstallstate.md).</span><span class="sxs-lookup"><span data-stu-id="c2dd9-126">Update the properties of a [deviceInstallState](../resources/intune-books-deviceinstallstate.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="c2dd9-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c2dd9-127">Properties</span></span>
|<span data-ttu-id="c2dd9-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c2dd9-128">Property</span></span>|<span data-ttu-id="c2dd9-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="c2dd9-129">Type</span></span>|<span data-ttu-id="c2dd9-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="c2dd9-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="c2dd9-131">id</span><span class="sxs-lookup"><span data-stu-id="c2dd9-131">id</span></span>|<span data-ttu-id="c2dd9-132">String</span><span class="sxs-lookup"><span data-stu-id="c2dd9-132">String</span></span>|<span data-ttu-id="c2dd9-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-133">Key of the entity.</span></span>|
|<span data-ttu-id="c2dd9-134">deviceName</span><span class="sxs-lookup"><span data-stu-id="c2dd9-134">deviceName</span></span>|<span data-ttu-id="c2dd9-135">String</span><span class="sxs-lookup"><span data-stu-id="c2dd9-135">String</span></span>|<span data-ttu-id="c2dd9-136">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-136">Device name.</span></span>|
|<span data-ttu-id="c2dd9-137">deviceId</span><span class="sxs-lookup"><span data-stu-id="c2dd9-137">deviceId</span></span>|<span data-ttu-id="c2dd9-138">String</span><span class="sxs-lookup"><span data-stu-id="c2dd9-138">String</span></span>|<span data-ttu-id="c2dd9-139">Id. del dispositivo</span><span class="sxs-lookup"><span data-stu-id="c2dd9-139">Device Id.</span></span>|
|<span data-ttu-id="c2dd9-140">lastSyncDateTime</span><span class="sxs-lookup"><span data-stu-id="c2dd9-140">lastSyncDateTime</span></span>|<span data-ttu-id="c2dd9-141">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="c2dd9-141">DateTimeOffset</span></span>|<span data-ttu-id="c2dd9-142">Fecha y hora de la última sincronización.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-142">Last sync date and time.</span></span>|
|<span data-ttu-id="c2dd9-143">installState</span><span class="sxs-lookup"><span data-stu-id="c2dd9-143">installState</span></span>|[<span data-ttu-id="c2dd9-144">installState</span><span class="sxs-lookup"><span data-stu-id="c2dd9-144">installState</span></span>](../resources/intune-books-installstate.md)|<span data-ttu-id="c2dd9-145">El estado de instalación del libro electrónico.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-145">The install state of the eBook.</span></span> <span data-ttu-id="c2dd9-146">Los valores posibles son: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed` y `unknown`.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-146">Possible values are: `notApplicable`, `installed`, `failed`, `notInstalled`, `uninstallFailed`, `unknown`.</span></span>|
|<span data-ttu-id="c2dd9-147">errorCode</span><span class="sxs-lookup"><span data-stu-id="c2dd9-147">errorCode</span></span>|<span data-ttu-id="c2dd9-148">String</span><span class="sxs-lookup"><span data-stu-id="c2dd9-148">String</span></span>|<span data-ttu-id="c2dd9-149">El código de error si hay errores de instalación.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-149">The error code for install failures.</span></span>|
|<span data-ttu-id="c2dd9-150">osVersion</span><span class="sxs-lookup"><span data-stu-id="c2dd9-150">osVersion</span></span>|<span data-ttu-id="c2dd9-151">String</span><span class="sxs-lookup"><span data-stu-id="c2dd9-151">String</span></span>|<span data-ttu-id="c2dd9-152">Versión del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-152">OS Version.</span></span>|
|<span data-ttu-id="c2dd9-153">osDescription</span><span class="sxs-lookup"><span data-stu-id="c2dd9-153">osDescription</span></span>|<span data-ttu-id="c2dd9-154">String</span><span class="sxs-lookup"><span data-stu-id="c2dd9-154">String</span></span>|<span data-ttu-id="c2dd9-155">Descripción del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-155">OS Description.</span></span>|
|<span data-ttu-id="c2dd9-156">userName</span><span class="sxs-lookup"><span data-stu-id="c2dd9-156">userName</span></span>|<span data-ttu-id="c2dd9-157">String</span><span class="sxs-lookup"><span data-stu-id="c2dd9-157">String</span></span>|<span data-ttu-id="c2dd9-158">Nombre de usuario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-158">Device User Name.</span></span>|

## <a name="relationships"></a><span data-ttu-id="c2dd9-159">Relaciones</span><span class="sxs-lookup"><span data-stu-id="c2dd9-159">Relationships</span></span>
<span data-ttu-id="c2dd9-160">Ninguna</span><span class="sxs-lookup"><span data-stu-id="c2dd9-160">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="c2dd9-161">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c2dd9-161">JSON Representation</span></span>
<span data-ttu-id="c2dd9-162">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c2dd9-162">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceInstallState"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceInstallState",
  "id": "String (identifier)",
  "deviceName": "String",
  "deviceId": "String",
  "lastSyncDateTime": "String (timestamp)",
  "installState": "String",
  "errorCode": "String",
  "osVersion": "String",
  "osDescription": "String",
  "userName": "String"
}
```





