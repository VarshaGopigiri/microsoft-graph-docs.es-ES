---
title: Tipo de recurso deviceConfiguration
description: Configuración de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 1a508a037dbd1271d30a226d9cf62fb0683b53af
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27953150"
---
# <a name="deviceconfiguration-resource-type"></a><span data-ttu-id="4a9bb-103">Tipo de recurso deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a9bb-103">deviceConfiguration resource type</span></span>

> <span data-ttu-id="4a9bb-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="4a9bb-105">Configuración de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-105">Device Configuration.</span></span>
## <a name="methods"></a><span data-ttu-id="4a9bb-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="4a9bb-106">Methods</span></span>
|<span data-ttu-id="4a9bb-107">Método</span><span class="sxs-lookup"><span data-stu-id="4a9bb-107">Method</span></span>|<span data-ttu-id="4a9bb-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4a9bb-108">Return Type</span></span>|<span data-ttu-id="4a9bb-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a9bb-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="4a9bb-110">Enumerar deviceConfigurations</span><span class="sxs-lookup"><span data-stu-id="4a9bb-110">List deviceConfigurations</span></span>](../api/intune-deviceconfig-deviceconfiguration-list.md)|<span data-ttu-id="4a9bb-111">Colección [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="4a9bb-111">[deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) collection</span></span>|<span data-ttu-id="4a9bb-112">Enumere las propiedades y las relaciones de los objetos [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4a9bb-112">List properties and relationships of the [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) objects.</span></span>|
|[<span data-ttu-id="4a9bb-113">Obtener deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a9bb-113">Get deviceConfiguration</span></span>](../api/intune-deviceconfig-deviceconfiguration-get.md)|[<span data-ttu-id="4a9bb-114">deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4a9bb-114">deviceConfiguration</span></span>](../resources/intune-deviceconfig-deviceconfiguration.md)|<span data-ttu-id="4a9bb-115">Lea las propiedades y las relaciones del objeto [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md).</span><span class="sxs-lookup"><span data-stu-id="4a9bb-115">Read properties and relationships of the [deviceConfiguration](../resources/intune-deviceconfig-deviceconfiguration.md) object.</span></span>|
|[<span data-ttu-id="4a9bb-116">Acción assign</span><span class="sxs-lookup"><span data-stu-id="4a9bb-116">assign action</span></span>](../api/intune-deviceconfig-deviceconfiguration-assign.md)|<span data-ttu-id="4a9bb-117">Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="4a9bb-117">[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) collection</span></span>|<span data-ttu-id="4a9bb-118">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="4a9bb-118">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="4a9bb-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4a9bb-119">Properties</span></span>
|<span data-ttu-id="4a9bb-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4a9bb-120">Property</span></span>|<span data-ttu-id="4a9bb-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a9bb-121">Type</span></span>|<span data-ttu-id="4a9bb-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a9bb-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4a9bb-123">id</span><span class="sxs-lookup"><span data-stu-id="4a9bb-123">id</span></span>|<span data-ttu-id="4a9bb-124">String</span><span class="sxs-lookup"><span data-stu-id="4a9bb-124">String</span></span>|<span data-ttu-id="4a9bb-125">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-125">Key of the entity.</span></span>|
|<span data-ttu-id="4a9bb-126">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="4a9bb-126">lastModifiedDateTime</span></span>|<span data-ttu-id="4a9bb-127">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4a9bb-127">DateTimeOffset</span></span>|<span data-ttu-id="4a9bb-128">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-128">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="4a9bb-129">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="4a9bb-129">createdDateTime</span></span>|<span data-ttu-id="4a9bb-130">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="4a9bb-130">DateTimeOffset</span></span>|<span data-ttu-id="4a9bb-131">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-131">DateTime the object was created.</span></span>|
|<span data-ttu-id="4a9bb-132">descripción</span><span class="sxs-lookup"><span data-stu-id="4a9bb-132">description</span></span>|<span data-ttu-id="4a9bb-133">String</span><span class="sxs-lookup"><span data-stu-id="4a9bb-133">String</span></span>|<span data-ttu-id="4a9bb-134">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-134">Admin provided description of the Device Configuration.</span></span>|
|<span data-ttu-id="4a9bb-135">displayName</span><span class="sxs-lookup"><span data-stu-id="4a9bb-135">displayName</span></span>|<span data-ttu-id="4a9bb-136">String</span><span class="sxs-lookup"><span data-stu-id="4a9bb-136">String</span></span>|<span data-ttu-id="4a9bb-137">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-137">Admin provided name of the device configuration.</span></span>|
|<span data-ttu-id="4a9bb-138">versión</span><span class="sxs-lookup"><span data-stu-id="4a9bb-138">version</span></span>|<span data-ttu-id="4a9bb-139">Int32</span><span class="sxs-lookup"><span data-stu-id="4a9bb-139">Int32</span></span>|<span data-ttu-id="4a9bb-140">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-140">Version of the device configuration.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4a9bb-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4a9bb-141">Relationships</span></span>
|<span data-ttu-id="4a9bb-142">Relación</span><span class="sxs-lookup"><span data-stu-id="4a9bb-142">Relationship</span></span>|<span data-ttu-id="4a9bb-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="4a9bb-143">Type</span></span>|<span data-ttu-id="4a9bb-144">Descripción</span><span class="sxs-lookup"><span data-stu-id="4a9bb-144">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="4a9bb-145">asignaciones</span><span class="sxs-lookup"><span data-stu-id="4a9bb-145">assignments</span></span>|<span data-ttu-id="4a9bb-146">Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="4a9bb-146">[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) collection</span></span>|<span data-ttu-id="4a9bb-147">La lista de tareas para el perfil de configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-147">The list of assignments for the device configuration profile.</span></span>|
|<span data-ttu-id="4a9bb-148">deviceStatuses</span><span class="sxs-lookup"><span data-stu-id="4a9bb-148">deviceStatuses</span></span>|<span data-ttu-id="4a9bb-149">Colección [deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md)</span><span class="sxs-lookup"><span data-stu-id="4a9bb-149">[deviceConfigurationDeviceStatus](../resources/intune-deviceconfig-deviceconfigurationdevicestatus.md) collection</span></span>|<span data-ttu-id="4a9bb-150">Estado de instalación de configuración del dispositivo por dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-150">Device configuration installation status by device.</span></span>|
|<span data-ttu-id="4a9bb-151">userStatuses</span><span class="sxs-lookup"><span data-stu-id="4a9bb-151">userStatuses</span></span>|<span data-ttu-id="4a9bb-152">Colección [deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md)</span><span class="sxs-lookup"><span data-stu-id="4a9bb-152">[deviceConfigurationUserStatus](../resources/intune-deviceconfig-deviceconfigurationuserstatus.md) collection</span></span>|<span data-ttu-id="4a9bb-153">Estado de instalación de configuración de dispositivo por usuario.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-153">Device configuration installation status by user.</span></span>|
|<span data-ttu-id="4a9bb-154">deviceStatusOverview</span><span class="sxs-lookup"><span data-stu-id="4a9bb-154">deviceStatusOverview</span></span>|[<span data-ttu-id="4a9bb-155">deviceConfigurationDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="4a9bb-155">deviceConfigurationDeviceOverview</span></span>](../resources/intune-deviceconfig-deviceconfigurationdeviceoverview.md)|<span data-ttu-id="4a9bb-156">Información general del estado del dispositivo sobre la configuración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="4a9bb-156">Device Configuration devices status overview</span></span>|
|<span data-ttu-id="4a9bb-157">userStatusOverview</span><span class="sxs-lookup"><span data-stu-id="4a9bb-157">userStatusOverview</span></span>|[<span data-ttu-id="4a9bb-158">deviceConfigurationUserOverview</span><span class="sxs-lookup"><span data-stu-id="4a9bb-158">deviceConfigurationUserOverview</span></span>](../resources/intune-deviceconfig-deviceconfigurationuseroverview.md)|<span data-ttu-id="4a9bb-159">Información general del estado de los usuarios sobre la configuración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="4a9bb-159">Device Configuration users status overview</span></span>|
|<span data-ttu-id="4a9bb-160">deviceSettingStateSummaries</span><span class="sxs-lookup"><span data-stu-id="4a9bb-160">deviceSettingStateSummaries</span></span>|<span data-ttu-id="4a9bb-161">Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)</span><span class="sxs-lookup"><span data-stu-id="4a9bb-161">[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) collection</span></span>|<span data-ttu-id="4a9bb-162">Resumen de dispositivo del estado de configuración de la configuración de dispositivos</span><span class="sxs-lookup"><span data-stu-id="4a9bb-162">Device Configuration Setting State Device Summary</span></span>|

## <a name="json-representation"></a><span data-ttu-id="4a9bb-163">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4a9bb-163">JSON Representation</span></span>
<span data-ttu-id="4a9bb-164">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4a9bb-164">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfiguration"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfiguration",
  "id": "String (identifier)",
  "lastModifiedDateTime": "String (timestamp)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "displayName": "String",
  "version": 1024
}
```



