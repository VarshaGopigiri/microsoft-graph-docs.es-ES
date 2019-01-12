---
title: tipo de recurso locationManagementCondition
description: Contiene la información para definir una condición de administración de la ubicación, un área de interés, para supervisar.
localization_priority: Normal
author: tfitzmac
ms.prod: intune
ms.openlocfilehash: 541cf74decad641f6dc7751945e1d0ffceee1366
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27922980"
---
# <a name="locationmanagementcondition-resource-type"></a><span data-ttu-id="ad13e-103">tipo de recurso locationManagementCondition</span><span class="sxs-lookup"><span data-stu-id="ad13e-103">locationManagementCondition resource type</span></span>

> <span data-ttu-id="ad13e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ad13e-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ad13e-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ad13e-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="ad13e-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ad13e-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ad13e-107">Contiene la información para definir una condición de administración de la ubicación, un área de interés, para supervisar.</span><span class="sxs-lookup"><span data-stu-id="ad13e-107">Contains the information to define a location management condition, an area of interest, to monitor.</span></span>

<span data-ttu-id="ad13e-108">Hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-108">Inherits from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>

## <a name="methods"></a><span data-ttu-id="ad13e-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="ad13e-109">Methods</span></span>
|<span data-ttu-id="ad13e-110">Método</span><span class="sxs-lookup"><span data-stu-id="ad13e-110">Method</span></span>|<span data-ttu-id="ad13e-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ad13e-111">Return Type</span></span>|<span data-ttu-id="ad13e-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad13e-112">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="ad13e-113">Lista locationManagementConditions</span><span class="sxs-lookup"><span data-stu-id="ad13e-113">List locationManagementConditions</span></span>](../api/intune-fencing-locationmanagementcondition-list.md)|<span data-ttu-id="ad13e-114">colección de [locationManagementCondition](../resources/intune-fencing-locationmanagementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-114">[locationManagementCondition](../resources/intune-fencing-locationmanagementcondition.md) collection</span></span>|<span data-ttu-id="ad13e-115">Propiedades de la lista y relaciones de los objetos [locationManagementCondition](../resources/intune-fencing-locationmanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="ad13e-115">List properties and relationships of the [locationManagementCondition](../resources/intune-fencing-locationmanagementcondition.md) objects.</span></span>|
|[<span data-ttu-id="ad13e-116">Obtener locationManagementCondition</span><span class="sxs-lookup"><span data-stu-id="ad13e-116">Get locationManagementCondition</span></span>](../api/intune-fencing-locationmanagementcondition-get.md)|[<span data-ttu-id="ad13e-117">locationManagementCondition</span><span class="sxs-lookup"><span data-stu-id="ad13e-117">locationManagementCondition</span></span>](../resources/intune-fencing-locationmanagementcondition.md)|<span data-ttu-id="ad13e-118">Leer las propiedades y las relaciones del objeto [locationManagementCondition](../resources/intune-fencing-locationmanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="ad13e-118">Read properties and relationships of the [locationManagementCondition](../resources/intune-fencing-locationmanagementcondition.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="ad13e-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ad13e-119">Properties</span></span>
|<span data-ttu-id="ad13e-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ad13e-120">Property</span></span>|<span data-ttu-id="ad13e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad13e-121">Type</span></span>|<span data-ttu-id="ad13e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad13e-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ad13e-123">id</span><span class="sxs-lookup"><span data-stu-id="ad13e-123">id</span></span>|<span data-ttu-id="ad13e-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="ad13e-124">String</span></span>|<span data-ttu-id="ad13e-125">Identificador único de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="ad13e-125">Unique identifier for the management condition.</span></span> <span data-ttu-id="ad13e-126">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="ad13e-126">System generated value assigned when created.</span></span> <span data-ttu-id="ad13e-127">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-127">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="ad13e-128">uniqueName</span><span class="sxs-lookup"><span data-stu-id="ad13e-128">uniqueName</span></span>|<span data-ttu-id="ad13e-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="ad13e-129">String</span></span>|<span data-ttu-id="ad13e-130">Nombre único para la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="ad13e-130">Unique name for the management condition.</span></span> <span data-ttu-id="ad13e-131">Se usa en expresiones de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="ad13e-131">Used in management condition expressions.</span></span> <span data-ttu-id="ad13e-132">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-132">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="ad13e-133">displayName</span><span class="sxs-lookup"><span data-stu-id="ad13e-133">displayName</span></span>|<span data-ttu-id="ad13e-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="ad13e-134">String</span></span>|<span data-ttu-id="ad13e-135">El nombre definido de administración de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="ad13e-135">The admin defined name of the management condition.</span></span> <span data-ttu-id="ad13e-136">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-136">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="ad13e-137">descripción</span><span class="sxs-lookup"><span data-stu-id="ad13e-137">description</span></span>|<span data-ttu-id="ad13e-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="ad13e-138">String</span></span>|<span data-ttu-id="ad13e-139">El administrador define la descripción de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="ad13e-139">The admin defined description of the management condition.</span></span> <span data-ttu-id="ad13e-140">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-140">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="ad13e-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="ad13e-141">createdDateTime</span></span>|<span data-ttu-id="ad13e-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ad13e-142">DateTimeOffset</span></span>|<span data-ttu-id="ad13e-143">La hora en que se creó la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="ad13e-143">The time the management condition was created.</span></span> <span data-ttu-id="ad13e-144">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="ad13e-144">Generated service side.</span></span> <span data-ttu-id="ad13e-145">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-145">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="ad13e-146">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="ad13e-146">modifiedDateTime</span></span>|<span data-ttu-id="ad13e-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="ad13e-147">DateTimeOffset</span></span>|<span data-ttu-id="ad13e-148">La hora en que se modificó por última vez la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="ad13e-148">The time the management condition was last modified.</span></span> <span data-ttu-id="ad13e-149">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="ad13e-149">Updated service side.</span></span> <span data-ttu-id="ad13e-150">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-150">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="ad13e-151">eTag</span><span class="sxs-lookup"><span data-stu-id="ad13e-151">eTag</span></span>|<span data-ttu-id="ad13e-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="ad13e-152">String</span></span>|<span data-ttu-id="ad13e-153">ETag de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="ad13e-153">ETag of the management condition.</span></span> <span data-ttu-id="ad13e-154">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="ad13e-154">Updated service side.</span></span> <span data-ttu-id="ad13e-155">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-155">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="ad13e-156">applicablePlatforms</span><span class="sxs-lookup"><span data-stu-id="ad13e-156">applicablePlatforms</span></span>|<span data-ttu-id="ad13e-157">colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-157">[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) collection</span></span>|<span data-ttu-id="ad13e-158">Las plataformas aplicables para esta condición de administración.</span><span class="sxs-lookup"><span data-stu-id="ad13e-158">The applicable platforms for this management condition.</span></span> <span data-ttu-id="ad13e-159">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-159">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="ad13e-160">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ad13e-160">Relationships</span></span>
|<span data-ttu-id="ad13e-161">Relación</span><span class="sxs-lookup"><span data-stu-id="ad13e-161">Relationship</span></span>|<span data-ttu-id="ad13e-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad13e-162">Type</span></span>|<span data-ttu-id="ad13e-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad13e-163">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ad13e-164">managementConditionStatements</span><span class="sxs-lookup"><span data-stu-id="ad13e-164">managementConditionStatements</span></span>|<span data-ttu-id="ad13e-165">colección de [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-165">[managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) collection</span></span>|<span data-ttu-id="ad13e-166">Las instrucciones de condición de administración asociadas a la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="ad13e-166">The management condition statements associated to the management condition.</span></span> <span data-ttu-id="ad13e-167">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="ad13e-167">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ad13e-168">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ad13e-168">JSON Representation</span></span>
<span data-ttu-id="ad13e-169">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ad13e-169">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.locationManagementCondition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.locationManagementCondition",
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





