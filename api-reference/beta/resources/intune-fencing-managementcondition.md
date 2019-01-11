---
title: tipo de recurso managementCondition
description: Condiciones de administración son eventos que se pueden desencadenar dinámicamente como ubican-barreras, límites de tiempo y límites de la red.
localization_priority: Normal
ms.openlocfilehash: a836aeaa660de8f02c4e441e9eb390e1513c917c
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834114"
---
# <a name="managementcondition-resource-type"></a><span data-ttu-id="118b8-103">tipo de recurso managementCondition</span><span class="sxs-lookup"><span data-stu-id="118b8-103">managementCondition resource type</span></span>

> <span data-ttu-id="118b8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="118b8-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="118b8-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="118b8-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="118b8-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="118b8-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="118b8-107">Condiciones de administración son eventos que se pueden desencadenar dinámicamente como ubican-barreras, límites de tiempo y límites de la red.</span><span class="sxs-lookup"><span data-stu-id="118b8-107">Management conditions are events that can be triggered dynamically such as geo-fences, time-fences, and network-fences.</span></span>
## <a name="methods"></a><span data-ttu-id="118b8-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="118b8-108">Methods</span></span>
|<span data-ttu-id="118b8-109">Método</span><span class="sxs-lookup"><span data-stu-id="118b8-109">Method</span></span>|<span data-ttu-id="118b8-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="118b8-110">Return Type</span></span>|<span data-ttu-id="118b8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="118b8-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="118b8-112">Lista managementConditions</span><span class="sxs-lookup"><span data-stu-id="118b8-112">List managementConditions</span></span>](../api/intune-fencing-managementcondition-list.md)|<span data-ttu-id="118b8-113">colección de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="118b8-113">[managementCondition](../resources/intune-fencing-managementcondition.md) collection</span></span>|<span data-ttu-id="118b8-114">Propiedades de la lista y relaciones de los objetos [managementCondition](../resources/intune-fencing-managementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="118b8-114">List properties and relationships of the [managementCondition](../resources/intune-fencing-managementcondition.md) objects.</span></span>|
|[<span data-ttu-id="118b8-115">Obtener managementCondition</span><span class="sxs-lookup"><span data-stu-id="118b8-115">Get managementCondition</span></span>](../api/intune-fencing-managementcondition-get.md)|[<span data-ttu-id="118b8-116">managementCondition</span><span class="sxs-lookup"><span data-stu-id="118b8-116">managementCondition</span></span>](../resources/intune-fencing-managementcondition.md)|<span data-ttu-id="118b8-117">Leer las propiedades y las relaciones del objeto [managementCondition](../resources/intune-fencing-managementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="118b8-117">Read properties and relationships of the [managementCondition](../resources/intune-fencing-managementcondition.md) object.</span></span>|
|[<span data-ttu-id="118b8-118">getManagementConditionsForPlatform (función)</span><span class="sxs-lookup"><span data-stu-id="118b8-118">getManagementConditionsForPlatform function</span></span>](../api/intune-fencing-managementcondition-getmanagementconditionsforplatform.md)|<span data-ttu-id="118b8-119">colección de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="118b8-119">[managementCondition](../resources/intune-fencing-managementcondition.md) collection</span></span>|<span data-ttu-id="118b8-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="118b8-120">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="118b8-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="118b8-121">Properties</span></span>
|<span data-ttu-id="118b8-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="118b8-122">Property</span></span>|<span data-ttu-id="118b8-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="118b8-123">Type</span></span>|<span data-ttu-id="118b8-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="118b8-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="118b8-125">id</span><span class="sxs-lookup"><span data-stu-id="118b8-125">id</span></span>|<span data-ttu-id="118b8-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="118b8-126">String</span></span>|<span data-ttu-id="118b8-127">Identificador único de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="118b8-127">Unique identifier for the management condition.</span></span> <span data-ttu-id="118b8-128">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="118b8-128">System generated value assigned when created.</span></span>|
|<span data-ttu-id="118b8-129">uniqueName</span><span class="sxs-lookup"><span data-stu-id="118b8-129">uniqueName</span></span>|<span data-ttu-id="118b8-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="118b8-130">String</span></span>|<span data-ttu-id="118b8-131">Nombre único para la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="118b8-131">Unique name for the management condition.</span></span> <span data-ttu-id="118b8-132">Se usa en expresiones de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="118b8-132">Used in management condition expressions.</span></span>|
|<span data-ttu-id="118b8-133">displayName</span><span class="sxs-lookup"><span data-stu-id="118b8-133">displayName</span></span>|<span data-ttu-id="118b8-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="118b8-134">String</span></span>|<span data-ttu-id="118b8-135">El nombre definido de administración de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="118b8-135">The admin defined name of the management condition.</span></span>|
|<span data-ttu-id="118b8-136">descripción</span><span class="sxs-lookup"><span data-stu-id="118b8-136">description</span></span>|<span data-ttu-id="118b8-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="118b8-137">String</span></span>|<span data-ttu-id="118b8-138">El administrador define la descripción de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="118b8-138">The admin defined description of the management condition.</span></span>|
|<span data-ttu-id="118b8-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="118b8-139">createdDateTime</span></span>|<span data-ttu-id="118b8-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="118b8-140">DateTimeOffset</span></span>|<span data-ttu-id="118b8-141">La hora en que se creó la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="118b8-141">The time the management condition was created.</span></span> <span data-ttu-id="118b8-142">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="118b8-142">Generated service side.</span></span>|
|<span data-ttu-id="118b8-143">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="118b8-143">modifiedDateTime</span></span>|<span data-ttu-id="118b8-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="118b8-144">DateTimeOffset</span></span>|<span data-ttu-id="118b8-145">La hora en que se modificó por última vez la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="118b8-145">The time the management condition was last modified.</span></span> <span data-ttu-id="118b8-146">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="118b8-146">Updated service side.</span></span>|
|<span data-ttu-id="118b8-147">eTag</span><span class="sxs-lookup"><span data-stu-id="118b8-147">eTag</span></span>|<span data-ttu-id="118b8-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="118b8-148">String</span></span>|<span data-ttu-id="118b8-149">ETag de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="118b8-149">ETag of the management condition.</span></span> <span data-ttu-id="118b8-150">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="118b8-150">Updated service side.</span></span>|
|<span data-ttu-id="118b8-151">applicablePlatforms</span><span class="sxs-lookup"><span data-stu-id="118b8-151">applicablePlatforms</span></span>|<span data-ttu-id="118b8-152">colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)</span><span class="sxs-lookup"><span data-stu-id="118b8-152">[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) collection</span></span>|<span data-ttu-id="118b8-153">Las plataformas aplicables para esta condición de administración.</span><span class="sxs-lookup"><span data-stu-id="118b8-153">The applicable platforms for this management condition.</span></span>|

## <a name="relationships"></a><span data-ttu-id="118b8-154">Relaciones</span><span class="sxs-lookup"><span data-stu-id="118b8-154">Relationships</span></span>
|<span data-ttu-id="118b8-155">Relación</span><span class="sxs-lookup"><span data-stu-id="118b8-155">Relationship</span></span>|<span data-ttu-id="118b8-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="118b8-156">Type</span></span>|<span data-ttu-id="118b8-157">Description</span><span class="sxs-lookup"><span data-stu-id="118b8-157">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="118b8-158">managementConditionStatements</span><span class="sxs-lookup"><span data-stu-id="118b8-158">managementConditionStatements</span></span>|<span data-ttu-id="118b8-159">colección de [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)</span><span class="sxs-lookup"><span data-stu-id="118b8-159">[managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) collection</span></span>|<span data-ttu-id="118b8-160">Las instrucciones de condición de administración asociadas a la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="118b8-160">The management condition statements associated to the management condition.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="118b8-161">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="118b8-161">JSON Representation</span></span>
<span data-ttu-id="118b8-162">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="118b8-162">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.managementCondition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.managementCondition",
  "id": "String (identifier)",
  "uniqueName": "String",
  "displayName": "String",
  "description": "String",
  "createdDateTime": "String (timestamp)",
  "modifiedDateTime": "String (timestamp)",
  "eTag": "String",
  "applicablePlatforms": [
    "String"
  ]
}
```





