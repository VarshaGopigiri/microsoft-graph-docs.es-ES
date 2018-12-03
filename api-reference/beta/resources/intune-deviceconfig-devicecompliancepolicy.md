---
title: Tipo de recurso deviceCompliancePolicy
description: 'Esta es la clase base para la directiva de cumplimiento. Las directivas de cumplimiento son específicas de la plataforma y las directivas de cumplimiento por plataforma individual se heredan desde ahí. '
ms.openlocfilehash: 8d41467d686d0f0b4d568a25332af791eda6600a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083985"
---
# <a name="devicecompliancepolicy-resource-type"></a><span data-ttu-id="7e67e-104">Tipo de recurso deviceCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="7e67e-104">deviceCompliancePolicy resource type</span></span>

> <span data-ttu-id="7e67e-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="7e67e-105">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="7e67e-106">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="7e67e-106">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="7e67e-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="7e67e-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="7e67e-108">Esta es la clase base para la directiva de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="7e67e-108">This is the base class for Compliance policy.</span></span> <span data-ttu-id="7e67e-109">Las directivas de cumplimiento son específicas de la plataforma y las directivas de cumplimiento por plataforma individual se heredan desde ahí.</span><span class="sxs-lookup"><span data-stu-id="7e67e-109">Compliance policies are platform specific and individual per-platform compliance policies inherit from here.</span></span> 
## <a name="methods"></a><span data-ttu-id="7e67e-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="7e67e-110">Methods</span></span>
|<span data-ttu-id="7e67e-111">Método</span><span class="sxs-lookup"><span data-stu-id="7e67e-111">Method</span></span>|<span data-ttu-id="7e67e-112">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7e67e-112">Return Type</span></span>|<span data-ttu-id="7e67e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e67e-113">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="7e67e-114">Enumerar deviceCompliancePolicies</span><span class="sxs-lookup"><span data-stu-id="7e67e-114">List deviceCompliancePolicies</span></span>](../api/intune-deviceconfig-devicecompliancepolicy-list.md)|<span data-ttu-id="7e67e-115">Colección [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md)</span><span class="sxs-lookup"><span data-stu-id="7e67e-115">[deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) collection</span></span>|<span data-ttu-id="7e67e-116">Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="7e67e-116">List properties and relationships of the [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) objects.</span></span>|
|[<span data-ttu-id="7e67e-117">Obtener deviceCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="7e67e-117">Get deviceCompliancePolicy</span></span>](../api/intune-deviceconfig-devicecompliancepolicy-get.md)|[<span data-ttu-id="7e67e-118">deviceCompliancePolicy</span><span class="sxs-lookup"><span data-stu-id="7e67e-118">deviceCompliancePolicy</span></span>](../resources/intune-deviceconfig-devicecompliancepolicy.md)|<span data-ttu-id="7e67e-119">Lea las propiedades y las relaciones del objeto [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md).</span><span class="sxs-lookup"><span data-stu-id="7e67e-119">Read properties and relationships of the [deviceCompliancePolicy](../resources/intune-deviceconfig-devicecompliancepolicy.md) object.</span></span>|
|[<span data-ttu-id="7e67e-120">Acción assign</span><span class="sxs-lookup"><span data-stu-id="7e67e-120">assign action</span></span>](../api/intune-deviceconfig-devicecompliancepolicy-assign.md)|<span data-ttu-id="7e67e-121">Colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="7e67e-121">[deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) collection</span></span>|<span data-ttu-id="7e67e-122">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7e67e-122">Not yet documented</span></span>|
|[<span data-ttu-id="7e67e-123">Acción scheduleActionsForRules</span><span class="sxs-lookup"><span data-stu-id="7e67e-123">scheduleActionsForRules action</span></span>](../api/intune-deviceconfig-devicecompliancepolicy-scheduleactionsforrules.md)|<span data-ttu-id="7e67e-124">Ninguna</span><span class="sxs-lookup"><span data-stu-id="7e67e-124">None</span></span>|<span data-ttu-id="7e67e-125">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="7e67e-125">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="7e67e-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7e67e-126">Properties</span></span>
|<span data-ttu-id="7e67e-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="7e67e-127">Property</span></span>|<span data-ttu-id="7e67e-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e67e-128">Type</span></span>|<span data-ttu-id="7e67e-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e67e-129">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7e67e-130">roleScopeTagIds</span><span class="sxs-lookup"><span data-stu-id="7e67e-130">roleScopeTagIds</span></span>|<span data-ttu-id="7e67e-131">Colección String</span><span class="sxs-lookup"><span data-stu-id="7e67e-131">String collection</span></span>|<span data-ttu-id="7e67e-132">Lista de etiquetas de ámbito para esta instancia de entidad.</span><span class="sxs-lookup"><span data-stu-id="7e67e-132">List of Scope Tags for this Entity instance.</span></span>|
|<span data-ttu-id="7e67e-133">id</span><span class="sxs-lookup"><span data-stu-id="7e67e-133">id</span></span>|<span data-ttu-id="7e67e-134">String</span><span class="sxs-lookup"><span data-stu-id="7e67e-134">String</span></span>|<span data-ttu-id="7e67e-135">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="7e67e-135">Key of the entity.</span></span>|
|<span data-ttu-id="7e67e-136">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="7e67e-136">createdDateTime</span></span>|<span data-ttu-id="7e67e-137">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7e67e-137">DateTimeOffset</span></span>|<span data-ttu-id="7e67e-138">Fecha y hora en la que se creó el objeto.</span><span class="sxs-lookup"><span data-stu-id="7e67e-138">DateTime the object was created.</span></span>|
|<span data-ttu-id="7e67e-139">descripción</span><span class="sxs-lookup"><span data-stu-id="7e67e-139">description</span></span>|<span data-ttu-id="7e67e-140">String</span><span class="sxs-lookup"><span data-stu-id="7e67e-140">String</span></span>|<span data-ttu-id="7e67e-141">Descripción proporcionada por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e67e-141">Admin provided description of the Device Configuration.</span></span>|
|<span data-ttu-id="7e67e-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="7e67e-142">lastModifiedDateTime</span></span>|<span data-ttu-id="7e67e-143">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="7e67e-143">DateTimeOffset</span></span>|<span data-ttu-id="7e67e-144">Fecha y hora en la que se modificó el objeto por última vez.</span><span class="sxs-lookup"><span data-stu-id="7e67e-144">DateTime the object was last modified.</span></span>|
|<span data-ttu-id="7e67e-145">displayName</span><span class="sxs-lookup"><span data-stu-id="7e67e-145">displayName</span></span>|<span data-ttu-id="7e67e-146">String</span><span class="sxs-lookup"><span data-stu-id="7e67e-146">String</span></span>|<span data-ttu-id="7e67e-147">Nombre proporcionado por el administrador de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e67e-147">Admin provided name of the device configuration.</span></span>|
|<span data-ttu-id="7e67e-148">versión</span><span class="sxs-lookup"><span data-stu-id="7e67e-148">version</span></span>|<span data-ttu-id="7e67e-149">Int32</span><span class="sxs-lookup"><span data-stu-id="7e67e-149">Int32</span></span>|<span data-ttu-id="7e67e-150">Versión de la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e67e-150">Version of the device configuration.</span></span>|

## <a name="relationships"></a><span data-ttu-id="7e67e-151">Relaciones</span><span class="sxs-lookup"><span data-stu-id="7e67e-151">Relationships</span></span>
|<span data-ttu-id="7e67e-152">Relación</span><span class="sxs-lookup"><span data-stu-id="7e67e-152">Relationship</span></span>|<span data-ttu-id="7e67e-153">Tipo</span><span class="sxs-lookup"><span data-stu-id="7e67e-153">Type</span></span>|<span data-ttu-id="7e67e-154">Descripción</span><span class="sxs-lookup"><span data-stu-id="7e67e-154">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="7e67e-155">scheduledActionsForRule</span><span class="sxs-lookup"><span data-stu-id="7e67e-155">scheduledActionsForRule</span></span>|<span data-ttu-id="7e67e-156">Colección [deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md)</span><span class="sxs-lookup"><span data-stu-id="7e67e-156">[deviceComplianceScheduledActionForRule](../resources/intune-deviceconfig-devicecompliancescheduledactionforrule.md) collection</span></span>|<span data-ttu-id="7e67e-157">La lista de acción programada para esta regla</span><span class="sxs-lookup"><span data-stu-id="7e67e-157">The list of scheduled action for this rule</span></span>|
|<span data-ttu-id="7e67e-158">deviceStatuses</span><span class="sxs-lookup"><span data-stu-id="7e67e-158">deviceStatuses</span></span>|<span data-ttu-id="7e67e-159">Colección [deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md)</span><span class="sxs-lookup"><span data-stu-id="7e67e-159">[deviceComplianceDeviceStatus](../resources/intune-deviceconfig-devicecompliancedevicestatus.md) collection</span></span>|<span data-ttu-id="7e67e-160">Lista de DeviceComplianceDeviceStatus.</span><span class="sxs-lookup"><span data-stu-id="7e67e-160">List of DeviceComplianceDeviceStatus.</span></span>|
|<span data-ttu-id="7e67e-161">userStatuses</span><span class="sxs-lookup"><span data-stu-id="7e67e-161">userStatuses</span></span>|<span data-ttu-id="7e67e-162">Colección [deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md)</span><span class="sxs-lookup"><span data-stu-id="7e67e-162">[deviceComplianceUserStatus](../resources/intune-deviceconfig-devicecomplianceuserstatus.md) collection</span></span>|<span data-ttu-id="7e67e-163">Lista de DeviceComplianceUserStatus.</span><span class="sxs-lookup"><span data-stu-id="7e67e-163">List of DeviceComplianceUserStatus.</span></span>|
|<span data-ttu-id="7e67e-164">deviceStatusOverview</span><span class="sxs-lookup"><span data-stu-id="7e67e-164">deviceStatusOverview</span></span>|[<span data-ttu-id="7e67e-165">deviceComplianceDeviceOverview</span><span class="sxs-lookup"><span data-stu-id="7e67e-165">deviceComplianceDeviceOverview</span></span>](../resources/intune-deviceconfig-devicecompliancedeviceoverview.md)|<span data-ttu-id="7e67e-166">Información general del estado de los dispositivos sobre el cumplimiento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="7e67e-166">Device compliance devices status overview</span></span>|
|<span data-ttu-id="7e67e-167">userStatusOverview</span><span class="sxs-lookup"><span data-stu-id="7e67e-167">userStatusOverview</span></span>|[<span data-ttu-id="7e67e-168">deviceComplianceUserOverview</span><span class="sxs-lookup"><span data-stu-id="7e67e-168">deviceComplianceUserOverview</span></span>](../resources/intune-deviceconfig-devicecomplianceuseroverview.md)|<span data-ttu-id="7e67e-169">Información general del estado de los usuarios sobre el cumplimiento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="7e67e-169">Device compliance users status overview</span></span>|
|<span data-ttu-id="7e67e-170">deviceSettingStateSummaries</span><span class="sxs-lookup"><span data-stu-id="7e67e-170">deviceSettingStateSummaries</span></span>|<span data-ttu-id="7e67e-171">Colección [settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md)</span><span class="sxs-lookup"><span data-stu-id="7e67e-171">[settingStateDeviceSummary](../resources/intune-deviceconfig-settingstatedevicesummary.md) collection</span></span>|<span data-ttu-id="7e67e-172">Resumen de dispositivo del estado de configuración de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="7e67e-172">Compliance Setting State Device Summary</span></span>|
|<span data-ttu-id="7e67e-173">asignaciones</span><span class="sxs-lookup"><span data-stu-id="7e67e-173">assignments</span></span>|<span data-ttu-id="7e67e-174">Colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="7e67e-174">[deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) collection</span></span>|<span data-ttu-id="7e67e-175">El conjunto de asignaciones para esta directiva de cumplimiento.</span><span class="sxs-lookup"><span data-stu-id="7e67e-175">The collection of assignments for this compliance policy.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="7e67e-176">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="7e67e-176">JSON Representation</span></span>
<span data-ttu-id="7e67e-177">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="7e67e-177">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCompliancePolicy"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicy",
  "roleScopeTagIds": [
    "String"
  ],
  "id": "String (identifier)",
  "createdDateTime": "String (timestamp)",
  "description": "String",
  "lastModifiedDateTime": "String (timestamp)",
  "displayName": "String",
  "version": 1024
}
```




