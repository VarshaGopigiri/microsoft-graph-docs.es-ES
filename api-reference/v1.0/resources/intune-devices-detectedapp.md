---
title: Tipo de recurso detectedApp
description: Una aplicación administrada o no administrada que está instalada en un dispositivo administrado. Las aplicaciones no administradas solo aparecerán para los dispositivos marcados como propiedad de la empresa.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 8b28965cb506075c8caf7d983ddf41eafcdda78d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27881427"
---
# <a name="detectedapp-resource-type"></a><span data-ttu-id="ec58b-104">Tipo de recurso detectedApp</span><span class="sxs-lookup"><span data-stu-id="ec58b-104">detectedApp resource type</span></span>

> <span data-ttu-id="ec58b-105">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ec58b-105">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ec58b-106">Una aplicación administrada o no administrada que está instalada en un dispositivo administrado.</span><span class="sxs-lookup"><span data-stu-id="ec58b-106">A managed or unmanaged app that is installed on a managed device.</span></span> <span data-ttu-id="ec58b-107">Las aplicaciones no administradas solo aparecerán para los dispositivos marcados como propiedad de la empresa.</span><span class="sxs-lookup"><span data-stu-id="ec58b-107">Unmanaged apps will only appear for devices marked as corporate owned.</span></span>
## <a name="methods"></a><span data-ttu-id="ec58b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="ec58b-108">Methods</span></span>
|<span data-ttu-id="ec58b-109">Método</span><span class="sxs-lookup"><span data-stu-id="ec58b-109">Method</span></span>|<span data-ttu-id="ec58b-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ec58b-110">Return Type</span></span>|<span data-ttu-id="ec58b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec58b-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="ec58b-112">Enumerar detectedApps</span><span class="sxs-lookup"><span data-stu-id="ec58b-112">List detectedApps</span></span>](../api/intune-devices-detectedapp-list.md)|<span data-ttu-id="ec58b-113">Colección [detectedApp](../resources/intune-devices-detectedapp.md)</span><span class="sxs-lookup"><span data-stu-id="ec58b-113">[detectedApp](../resources/intune-devices-detectedapp.md) collection</span></span>|<span data-ttu-id="ec58b-114">Enumere las propiedades y las relaciones de los objetos [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="ec58b-114">List properties and relationships of the [detectedApp](../resources/intune-devices-detectedapp.md) objects.</span></span>|
|[<span data-ttu-id="ec58b-115">Obtener detectedApp</span><span class="sxs-lookup"><span data-stu-id="ec58b-115">Get detectedApp</span></span>](../api/intune-devices-detectedapp-get.md)|[<span data-ttu-id="ec58b-116">detectedApp</span><span class="sxs-lookup"><span data-stu-id="ec58b-116">detectedApp</span></span>](../resources/intune-devices-detectedapp.md)|<span data-ttu-id="ec58b-117">Lea las propiedades y las relaciones del objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="ec58b-117">Read properties and relationships of the [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>|
|[<span data-ttu-id="ec58b-118">Crear detectedApp</span><span class="sxs-lookup"><span data-stu-id="ec58b-118">Create detectedApp</span></span>](../api/intune-devices-detectedapp-create.md)|[<span data-ttu-id="ec58b-119">detectedApp</span><span class="sxs-lookup"><span data-stu-id="ec58b-119">detectedApp</span></span>](../resources/intune-devices-detectedapp.md)|<span data-ttu-id="ec58b-120">Cree un objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="ec58b-120">Create a new [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>|
|[<span data-ttu-id="ec58b-121">Eliminar detectedApp</span><span class="sxs-lookup"><span data-stu-id="ec58b-121">Delete detectedApp</span></span>](../api/intune-devices-detectedapp-delete.md)|<span data-ttu-id="ec58b-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ec58b-122">None</span></span>|<span data-ttu-id="ec58b-123">Elimina un [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="ec58b-123">Deletes a [detectedApp](../resources/intune-devices-detectedapp.md).</span></span>|
|[<span data-ttu-id="ec58b-124">Actualizar detectedApp</span><span class="sxs-lookup"><span data-stu-id="ec58b-124">Update detectedApp</span></span>](../api/intune-devices-detectedapp-update.md)|[<span data-ttu-id="ec58b-125">detectedApp</span><span class="sxs-lookup"><span data-stu-id="ec58b-125">detectedApp</span></span>](../resources/intune-devices-detectedapp.md)|<span data-ttu-id="ec58b-126">Actualice las propiedades de un objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="ec58b-126">Update the properties of a [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="ec58b-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec58b-127">Properties</span></span>
|<span data-ttu-id="ec58b-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ec58b-128">Property</span></span>|<span data-ttu-id="ec58b-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec58b-129">Type</span></span>|<span data-ttu-id="ec58b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec58b-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ec58b-131">id</span><span class="sxs-lookup"><span data-stu-id="ec58b-131">id</span></span>|<span data-ttu-id="ec58b-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="ec58b-132">String</span></span>|<span data-ttu-id="ec58b-133">El identificador único de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="ec58b-133">The unique Identifier for the detected application.</span></span> <span data-ttu-id="ec58b-134">Intune lo genera automáticamente en el momento en que se crea la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ec58b-134">This is automatically generated by Intune at the time the application is created.</span></span> <span data-ttu-id="ec58b-135">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ec58b-135">Read-only.</span></span>|
|<span data-ttu-id="ec58b-136">displayName</span><span class="sxs-lookup"><span data-stu-id="ec58b-136">displayName</span></span>|<span data-ttu-id="ec58b-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="ec58b-137">String</span></span>|<span data-ttu-id="ec58b-138">Nombre de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="ec58b-138">Name of the discovered application.</span></span> <span data-ttu-id="ec58b-139">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec58b-139">Read-only</span></span>|
|<span data-ttu-id="ec58b-140">version</span><span class="sxs-lookup"><span data-stu-id="ec58b-140">version</span></span>|<span data-ttu-id="ec58b-141">Cadena</span><span class="sxs-lookup"><span data-stu-id="ec58b-141">String</span></span>|<span data-ttu-id="ec58b-142">Versión de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="ec58b-142">Version of the discovered application.</span></span> <span data-ttu-id="ec58b-143">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec58b-143">Read-only</span></span>|
|<span data-ttu-id="ec58b-144">sizeInByte</span><span class="sxs-lookup"><span data-stu-id="ec58b-144">sizeInByte</span></span>|<span data-ttu-id="ec58b-145">Int64</span><span class="sxs-lookup"><span data-stu-id="ec58b-145">Int64</span></span>|<span data-ttu-id="ec58b-146">Tamaño en bytes de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="ec58b-146">Discovered application size in bytes.</span></span> <span data-ttu-id="ec58b-147">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="ec58b-147">Read-only</span></span>|
|<span data-ttu-id="ec58b-148">deviceCount</span><span class="sxs-lookup"><span data-stu-id="ec58b-148">deviceCount</span></span>|<span data-ttu-id="ec58b-149">Int32</span><span class="sxs-lookup"><span data-stu-id="ec58b-149">Int32</span></span>|<span data-ttu-id="ec58b-150">El número de dispositivos que han instalado esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="ec58b-150">The number of devices that have installed this application</span></span>|

## <a name="relationships"></a><span data-ttu-id="ec58b-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ec58b-151">Relationships</span></span>
|<span data-ttu-id="ec58b-152">Relación</span><span class="sxs-lookup"><span data-stu-id="ec58b-152">Relationship</span></span>|<span data-ttu-id="ec58b-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec58b-153">Type</span></span>|<span data-ttu-id="ec58b-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec58b-154">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ec58b-155">managedDevices</span><span class="sxs-lookup"><span data-stu-id="ec58b-155">managedDevices</span></span>|<span data-ttu-id="ec58b-156">Colección [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="ec58b-156">[managedDevice](../resources/intune-devices-manageddevice.md) collection</span></span>|<span data-ttu-id="ec58b-157">Los dispositivos que tienen instalada la aplicación detectada</span><span class="sxs-lookup"><span data-stu-id="ec58b-157">The devices that have the discovered application installed</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ec58b-158">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ec58b-158">JSON Representation</span></span>
<span data-ttu-id="ec58b-159">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ec58b-159">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.detectedApp"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.detectedApp",
  "id": "String (identifier)",
  "displayName": "String",
  "version": "String",
  "sizeInByte": 1024,
  "deviceCount": 1024
}
```



