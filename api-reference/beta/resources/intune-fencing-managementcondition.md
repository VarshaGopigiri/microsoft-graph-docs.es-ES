---
title: tipo de recurso managementCondition
description: Condiciones de administración son eventos que se pueden desencadenar dinámicamente como ubican-barreras, límites de tiempo y límites de la red.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: e0aeb73a93cd4c61b6d4680f73c2a9b8cee830c6
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27986748"
---
# <a name="managementcondition-resource-type"></a><span data-ttu-id="a6419-103">tipo de recurso managementCondition</span><span class="sxs-lookup"><span data-stu-id="a6419-103">managementCondition resource type</span></span>

> <span data-ttu-id="a6419-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a6419-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a6419-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a6419-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="a6419-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="a6419-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="a6419-107">Condiciones de administración son eventos que se pueden desencadenar dinámicamente como ubican-barreras, límites de tiempo y límites de la red.</span><span class="sxs-lookup"><span data-stu-id="a6419-107">Management conditions are events that can be triggered dynamically such as geo-fences, time-fences, and network-fences.</span></span>
## <a name="methods"></a><span data-ttu-id="a6419-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="a6419-108">Methods</span></span>
|<span data-ttu-id="a6419-109">Método</span><span class="sxs-lookup"><span data-stu-id="a6419-109">Method</span></span>|<span data-ttu-id="a6419-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a6419-110">Return Type</span></span>|<span data-ttu-id="a6419-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6419-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="a6419-112">Lista managementConditions</span><span class="sxs-lookup"><span data-stu-id="a6419-112">List managementConditions</span></span>](../api/intune-fencing-managementcondition-list.md)|<span data-ttu-id="a6419-113">colección de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="a6419-113">[managementCondition](../resources/intune-fencing-managementcondition.md) collection</span></span>|<span data-ttu-id="a6419-114">Propiedades de la lista y relaciones de los objetos [managementCondition](../resources/intune-fencing-managementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="a6419-114">List properties and relationships of the [managementCondition](../resources/intune-fencing-managementcondition.md) objects.</span></span>|
|[<span data-ttu-id="a6419-115">Obtener managementCondition</span><span class="sxs-lookup"><span data-stu-id="a6419-115">Get managementCondition</span></span>](../api/intune-fencing-managementcondition-get.md)|[<span data-ttu-id="a6419-116">managementCondition</span><span class="sxs-lookup"><span data-stu-id="a6419-116">managementCondition</span></span>](../resources/intune-fencing-managementcondition.md)|<span data-ttu-id="a6419-117">Leer las propiedades y las relaciones del objeto [managementCondition](../resources/intune-fencing-managementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="a6419-117">Read properties and relationships of the [managementCondition](../resources/intune-fencing-managementcondition.md) object.</span></span>|
|[<span data-ttu-id="a6419-118">getManagementConditionsForPlatform (función)</span><span class="sxs-lookup"><span data-stu-id="a6419-118">getManagementConditionsForPlatform function</span></span>](../api/intune-fencing-managementcondition-getmanagementconditionsforplatform.md)|<span data-ttu-id="a6419-119">colección de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="a6419-119">[managementCondition](../resources/intune-fencing-managementcondition.md) collection</span></span>|<span data-ttu-id="a6419-120">Todavía no documentado</span><span class="sxs-lookup"><span data-stu-id="a6419-120">Not yet documented</span></span>|

## <a name="properties"></a><span data-ttu-id="a6419-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a6419-121">Properties</span></span>
|<span data-ttu-id="a6419-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="a6419-122">Property</span></span>|<span data-ttu-id="a6419-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6419-123">Type</span></span>|<span data-ttu-id="a6419-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6419-124">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a6419-125">id</span><span class="sxs-lookup"><span data-stu-id="a6419-125">id</span></span>|<span data-ttu-id="a6419-126">Cadena</span><span class="sxs-lookup"><span data-stu-id="a6419-126">String</span></span>|<span data-ttu-id="a6419-127">Identificador único de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="a6419-127">Unique identifier for the management condition.</span></span> <span data-ttu-id="a6419-128">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="a6419-128">System generated value assigned when created.</span></span>|
|<span data-ttu-id="a6419-129">uniqueName</span><span class="sxs-lookup"><span data-stu-id="a6419-129">uniqueName</span></span>|<span data-ttu-id="a6419-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="a6419-130">String</span></span>|<span data-ttu-id="a6419-131">Nombre único para la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="a6419-131">Unique name for the management condition.</span></span> <span data-ttu-id="a6419-132">Se usa en expresiones de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="a6419-132">Used in management condition expressions.</span></span>|
|<span data-ttu-id="a6419-133">displayName</span><span class="sxs-lookup"><span data-stu-id="a6419-133">displayName</span></span>|<span data-ttu-id="a6419-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="a6419-134">String</span></span>|<span data-ttu-id="a6419-135">El nombre definido de administración de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="a6419-135">The admin defined name of the management condition.</span></span>|
|<span data-ttu-id="a6419-136">descripción</span><span class="sxs-lookup"><span data-stu-id="a6419-136">description</span></span>|<span data-ttu-id="a6419-137">Cadena</span><span class="sxs-lookup"><span data-stu-id="a6419-137">String</span></span>|<span data-ttu-id="a6419-138">El administrador define la descripción de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="a6419-138">The admin defined description of the management condition.</span></span>|
|<span data-ttu-id="a6419-139">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="a6419-139">createdDateTime</span></span>|<span data-ttu-id="a6419-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a6419-140">DateTimeOffset</span></span>|<span data-ttu-id="a6419-141">La hora en que se creó la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="a6419-141">The time the management condition was created.</span></span> <span data-ttu-id="a6419-142">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="a6419-142">Generated service side.</span></span>|
|<span data-ttu-id="a6419-143">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="a6419-143">modifiedDateTime</span></span>|<span data-ttu-id="a6419-144">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="a6419-144">DateTimeOffset</span></span>|<span data-ttu-id="a6419-145">La hora en que se modificó por última vez la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="a6419-145">The time the management condition was last modified.</span></span> <span data-ttu-id="a6419-146">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="a6419-146">Updated service side.</span></span>|
|<span data-ttu-id="a6419-147">eTag</span><span class="sxs-lookup"><span data-stu-id="a6419-147">eTag</span></span>|<span data-ttu-id="a6419-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="a6419-148">String</span></span>|<span data-ttu-id="a6419-149">ETag de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="a6419-149">ETag of the management condition.</span></span> <span data-ttu-id="a6419-150">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="a6419-150">Updated service side.</span></span>|
|<span data-ttu-id="a6419-151">applicablePlatforms</span><span class="sxs-lookup"><span data-stu-id="a6419-151">applicablePlatforms</span></span>|<span data-ttu-id="a6419-152">colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)</span><span class="sxs-lookup"><span data-stu-id="a6419-152">[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) collection</span></span>|<span data-ttu-id="a6419-153">Las plataformas aplicables para esta condición de administración.</span><span class="sxs-lookup"><span data-stu-id="a6419-153">The applicable platforms for this management condition.</span></span>|

## <a name="relationships"></a><span data-ttu-id="a6419-154">Relaciones</span><span class="sxs-lookup"><span data-stu-id="a6419-154">Relationships</span></span>
|<span data-ttu-id="a6419-155">Relación</span><span class="sxs-lookup"><span data-stu-id="a6419-155">Relationship</span></span>|<span data-ttu-id="a6419-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="a6419-156">Type</span></span>|<span data-ttu-id="a6419-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="a6419-157">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="a6419-158">managementConditionStatements</span><span class="sxs-lookup"><span data-stu-id="a6419-158">managementConditionStatements</span></span>|<span data-ttu-id="a6419-159">colección de [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)</span><span class="sxs-lookup"><span data-stu-id="a6419-159">[managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) collection</span></span>|<span data-ttu-id="a6419-160">Las instrucciones de condición de administración asociadas a la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="a6419-160">The management condition statements associated to the management condition.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="a6419-161">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a6419-161">JSON Representation</span></span>
<span data-ttu-id="a6419-162">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="a6419-162">Here is a JSON representation of the resource.</span></span>
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





