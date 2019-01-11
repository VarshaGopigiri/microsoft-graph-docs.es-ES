---
title: Tipo de recurso detectedApp
description: Una aplicación administrada o no administrada que está instalada en un dispositivo administrado. Las aplicaciones no administradas solo aparecerán para los dispositivos marcados como propiedad de la empresa.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: f62e41b51d2b22d9524a0e86775e5f1cf9526618
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890079"
---
# <a name="detectedapp-resource-type"></a><span data-ttu-id="2faca-104">Tipo de recurso detectedApp</span><span class="sxs-lookup"><span data-stu-id="2faca-104">detectedApp resource type</span></span>

> <span data-ttu-id="2faca-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2faca-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2faca-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2faca-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="2faca-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="2faca-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="2faca-108">Una aplicación administrada o no administrada que está instalada en un dispositivo administrado.</span><span class="sxs-lookup"><span data-stu-id="2faca-108">A managed or unmanaged app that is installed on a managed device.</span></span> <span data-ttu-id="2faca-109">Las aplicaciones no administradas solo aparecerán para los dispositivos marcados como propiedad de la empresa.</span><span class="sxs-lookup"><span data-stu-id="2faca-109">Unmanaged apps will only appear for devices marked as corporate owned.</span></span>
## <a name="methods"></a><span data-ttu-id="2faca-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2faca-110">Methods</span></span>
|<span data-ttu-id="2faca-111">Método</span><span class="sxs-lookup"><span data-stu-id="2faca-111">Method</span></span>|<span data-ttu-id="2faca-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2faca-112">Return Type</span></span>|<span data-ttu-id="2faca-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="2faca-113">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="2faca-114">Enumerar detectedApps</span><span class="sxs-lookup"><span data-stu-id="2faca-114">List detectedApps</span></span>](../api/intune-devices-detectedapp-list.md)|<span data-ttu-id="2faca-115">Colección [detectedApp](../resources/intune-devices-detectedapp.md)</span><span class="sxs-lookup"><span data-stu-id="2faca-115">[detectedApp](../resources/intune-devices-detectedapp.md) collection</span></span>|<span data-ttu-id="2faca-116">Enumere las propiedades y las relaciones de los objetos [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="2faca-116">List properties and relationships of the [detectedApp](../resources/intune-devices-detectedapp.md) objects.</span></span>|
|[<span data-ttu-id="2faca-117">Obtener detectedApp</span><span class="sxs-lookup"><span data-stu-id="2faca-117">Get detectedApp</span></span>](../api/intune-devices-detectedapp-get.md)|[<span data-ttu-id="2faca-118">detectedApp</span><span class="sxs-lookup"><span data-stu-id="2faca-118">detectedApp</span></span>](../resources/intune-devices-detectedapp.md)|<span data-ttu-id="2faca-119">Lea las propiedades y las relaciones del objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="2faca-119">Read properties and relationships of the [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>|
|[<span data-ttu-id="2faca-120">Crear detectedApp</span><span class="sxs-lookup"><span data-stu-id="2faca-120">Create detectedApp</span></span>](../api/intune-devices-detectedapp-create.md)|[<span data-ttu-id="2faca-121">detectedApp</span><span class="sxs-lookup"><span data-stu-id="2faca-121">detectedApp</span></span>](../resources/intune-devices-detectedapp.md)|<span data-ttu-id="2faca-122">Cree un objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="2faca-122">Create a new [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>|
|[<span data-ttu-id="2faca-123">Eliminar detectedApp</span><span class="sxs-lookup"><span data-stu-id="2faca-123">Delete detectedApp</span></span>](../api/intune-devices-detectedapp-delete.md)|<span data-ttu-id="2faca-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="2faca-124">None</span></span>|<span data-ttu-id="2faca-125">Elimina un [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="2faca-125">Deletes a [detectedApp](../resources/intune-devices-detectedapp.md).</span></span>|
|[<span data-ttu-id="2faca-126">Actualizar detectedApp</span><span class="sxs-lookup"><span data-stu-id="2faca-126">Update detectedApp</span></span>](../api/intune-devices-detectedapp-update.md)|[<span data-ttu-id="2faca-127">detectedApp</span><span class="sxs-lookup"><span data-stu-id="2faca-127">detectedApp</span></span>](../resources/intune-devices-detectedapp.md)|<span data-ttu-id="2faca-128">Actualice las propiedades de un objeto [detectedApp](../resources/intune-devices-detectedapp.md).</span><span class="sxs-lookup"><span data-stu-id="2faca-128">Update the properties of a [detectedApp](../resources/intune-devices-detectedapp.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="2faca-129">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2faca-129">Properties</span></span>
|<span data-ttu-id="2faca-130">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2faca-130">Property</span></span>|<span data-ttu-id="2faca-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="2faca-131">Type</span></span>|<span data-ttu-id="2faca-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="2faca-132">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2faca-133">id</span><span class="sxs-lookup"><span data-stu-id="2faca-133">id</span></span>|<span data-ttu-id="2faca-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="2faca-134">String</span></span>|<span data-ttu-id="2faca-135">El identificador único de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="2faca-135">The unique Identifier for the detected application.</span></span> <span data-ttu-id="2faca-136">Intune lo genera automáticamente en el momento en que se crea la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2faca-136">This is automatically generated by Intune at the time the application is created.</span></span> <span data-ttu-id="2faca-137">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="2faca-137">Read-only.</span></span>|
|<span data-ttu-id="2faca-138">displayName</span><span class="sxs-lookup"><span data-stu-id="2faca-138">displayName</span></span>|<span data-ttu-id="2faca-139">Cadena</span><span class="sxs-lookup"><span data-stu-id="2faca-139">String</span></span>|<span data-ttu-id="2faca-140">Nombre de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="2faca-140">Name of the discovered application.</span></span> <span data-ttu-id="2faca-141">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="2faca-141">Read-only</span></span>|
|<span data-ttu-id="2faca-142">version</span><span class="sxs-lookup"><span data-stu-id="2faca-142">version</span></span>|<span data-ttu-id="2faca-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="2faca-143">String</span></span>|<span data-ttu-id="2faca-144">Versión de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="2faca-144">Version of the discovered application.</span></span> <span data-ttu-id="2faca-145">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="2faca-145">Read-only</span></span>|
|<span data-ttu-id="2faca-146">sizeInByte</span><span class="sxs-lookup"><span data-stu-id="2faca-146">sizeInByte</span></span>|<span data-ttu-id="2faca-147">Int64</span><span class="sxs-lookup"><span data-stu-id="2faca-147">Int64</span></span>|<span data-ttu-id="2faca-148">Tamaño en bytes de la aplicación detectada.</span><span class="sxs-lookup"><span data-stu-id="2faca-148">Discovered application size in bytes.</span></span> <span data-ttu-id="2faca-149">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="2faca-149">Read-only</span></span>|
|<span data-ttu-id="2faca-150">deviceCount</span><span class="sxs-lookup"><span data-stu-id="2faca-150">deviceCount</span></span>|<span data-ttu-id="2faca-151">Int32</span><span class="sxs-lookup"><span data-stu-id="2faca-151">Int32</span></span>|<span data-ttu-id="2faca-152">El número de dispositivos que han instalado esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="2faca-152">The number of devices that have installed this application</span></span>|

## <a name="relationships"></a><span data-ttu-id="2faca-153">Relaciones</span><span class="sxs-lookup"><span data-stu-id="2faca-153">Relationships</span></span>
|<span data-ttu-id="2faca-154">Relación</span><span class="sxs-lookup"><span data-stu-id="2faca-154">Relationship</span></span>|<span data-ttu-id="2faca-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="2faca-155">Type</span></span>|<span data-ttu-id="2faca-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="2faca-156">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="2faca-157">managedDevices</span><span class="sxs-lookup"><span data-stu-id="2faca-157">managedDevices</span></span>|<span data-ttu-id="2faca-158">Colección [managedDevice](../resources/intune-devices-manageddevice.md)</span><span class="sxs-lookup"><span data-stu-id="2faca-158">[managedDevice](../resources/intune-devices-manageddevice.md) collection</span></span>|<span data-ttu-id="2faca-159">Los dispositivos que tienen instalada la aplicación detectada</span><span class="sxs-lookup"><span data-stu-id="2faca-159">The devices that have the discovered application installed</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2faca-160">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2faca-160">JSON Representation</span></span>
<span data-ttu-id="2faca-161">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="2faca-161">Here is a JSON representation of the resource.</span></span>
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





