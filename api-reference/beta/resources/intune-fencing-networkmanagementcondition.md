---
title: tipo de recurso networkManagementCondition
description: Contiene la información para definir una condición de administración de la red.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 00ccc045892290ff03e68a109ccc01c4d5dbf8a1
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27927047"
---
# <a name="networkmanagementcondition-resource-type"></a><span data-ttu-id="1bab9-103">tipo de recurso networkManagementCondition</span><span class="sxs-lookup"><span data-stu-id="1bab9-103">networkManagementCondition resource type</span></span>

> <span data-ttu-id="1bab9-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="1bab9-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="1bab9-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="1bab9-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="1bab9-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="1bab9-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="1bab9-107">Contiene la información para definir una condición de administración de la red.</span><span class="sxs-lookup"><span data-stu-id="1bab9-107">Contains the information to define a network management condition.</span></span>

<span data-ttu-id="1bab9-108">Hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-108">Inherits from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>

## <a name="methods"></a><span data-ttu-id="1bab9-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="1bab9-109">Methods</span></span>
|<span data-ttu-id="1bab9-110">Método</span><span class="sxs-lookup"><span data-stu-id="1bab9-110">Method</span></span>|<span data-ttu-id="1bab9-111">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1bab9-111">Return Type</span></span>|<span data-ttu-id="1bab9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="1bab9-112">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="1bab9-113">Lista networkManagementConditions</span><span class="sxs-lookup"><span data-stu-id="1bab9-113">List networkManagementConditions</span></span>](../api/intune-fencing-networkmanagementcondition-list.md)|<span data-ttu-id="1bab9-114">colección de [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-114">[networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md) collection</span></span>|<span data-ttu-id="1bab9-115">Propiedades de la lista y relaciones de los objetos [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="1bab9-115">List properties and relationships of the [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md) objects.</span></span>|
|[<span data-ttu-id="1bab9-116">Obtener networkManagementCondition</span><span class="sxs-lookup"><span data-stu-id="1bab9-116">Get networkManagementCondition</span></span>](../api/intune-fencing-networkmanagementcondition-get.md)|[<span data-ttu-id="1bab9-117">networkManagementCondition</span><span class="sxs-lookup"><span data-stu-id="1bab9-117">networkManagementCondition</span></span>](../resources/intune-fencing-networkmanagementcondition.md)|<span data-ttu-id="1bab9-118">Leer las propiedades y las relaciones del objeto [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md) .</span><span class="sxs-lookup"><span data-stu-id="1bab9-118">Read properties and relationships of the [networkManagementCondition](../resources/intune-fencing-networkmanagementcondition.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="1bab9-119">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1bab9-119">Properties</span></span>
|<span data-ttu-id="1bab9-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1bab9-120">Property</span></span>|<span data-ttu-id="1bab9-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="1bab9-121">Type</span></span>|<span data-ttu-id="1bab9-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="1bab9-122">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1bab9-123">id</span><span class="sxs-lookup"><span data-stu-id="1bab9-123">id</span></span>|<span data-ttu-id="1bab9-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="1bab9-124">String</span></span>|<span data-ttu-id="1bab9-125">Identificador único de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1bab9-125">Unique identifier for the management condition.</span></span> <span data-ttu-id="1bab9-126">Valor asignado al crear generada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="1bab9-126">System generated value assigned when created.</span></span> <span data-ttu-id="1bab9-127">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-127">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1bab9-128">uniqueName</span><span class="sxs-lookup"><span data-stu-id="1bab9-128">uniqueName</span></span>|<span data-ttu-id="1bab9-129">Cadena</span><span class="sxs-lookup"><span data-stu-id="1bab9-129">String</span></span>|<span data-ttu-id="1bab9-130">Nombre único para la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1bab9-130">Unique name for the management condition.</span></span> <span data-ttu-id="1bab9-131">Se usa en expresiones de condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1bab9-131">Used in management condition expressions.</span></span> <span data-ttu-id="1bab9-132">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-132">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1bab9-133">displayName</span><span class="sxs-lookup"><span data-stu-id="1bab9-133">displayName</span></span>|<span data-ttu-id="1bab9-134">Cadena</span><span class="sxs-lookup"><span data-stu-id="1bab9-134">String</span></span>|<span data-ttu-id="1bab9-135">El nombre definido de administración de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1bab9-135">The admin defined name of the management condition.</span></span> <span data-ttu-id="1bab9-136">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-136">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1bab9-137">descripción</span><span class="sxs-lookup"><span data-stu-id="1bab9-137">description</span></span>|<span data-ttu-id="1bab9-138">Cadena</span><span class="sxs-lookup"><span data-stu-id="1bab9-138">String</span></span>|<span data-ttu-id="1bab9-139">El administrador define la descripción de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1bab9-139">The admin defined description of the management condition.</span></span> <span data-ttu-id="1bab9-140">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-140">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1bab9-141">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="1bab9-141">createdDateTime</span></span>|<span data-ttu-id="1bab9-142">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1bab9-142">DateTimeOffset</span></span>|<span data-ttu-id="1bab9-143">La hora en que se creó la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1bab9-143">The time the management condition was created.</span></span> <span data-ttu-id="1bab9-144">Servicio generado al lado.</span><span class="sxs-lookup"><span data-stu-id="1bab9-144">Generated service side.</span></span> <span data-ttu-id="1bab9-145">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-145">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1bab9-146">modifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="1bab9-146">modifiedDateTime</span></span>|<span data-ttu-id="1bab9-147">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1bab9-147">DateTimeOffset</span></span>|<span data-ttu-id="1bab9-148">La hora en que se modificó por última vez la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1bab9-148">The time the management condition was last modified.</span></span> <span data-ttu-id="1bab9-149">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="1bab9-149">Updated service side.</span></span> <span data-ttu-id="1bab9-150">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-150">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1bab9-151">eTag</span><span class="sxs-lookup"><span data-stu-id="1bab9-151">eTag</span></span>|<span data-ttu-id="1bab9-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="1bab9-152">String</span></span>|<span data-ttu-id="1bab9-153">ETag de la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1bab9-153">ETag of the management condition.</span></span> <span data-ttu-id="1bab9-154">Se actualizó el lado de servicio.</span><span class="sxs-lookup"><span data-stu-id="1bab9-154">Updated service side.</span></span> <span data-ttu-id="1bab9-155">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-155">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|
|<span data-ttu-id="1bab9-156">applicablePlatforms</span><span class="sxs-lookup"><span data-stu-id="1bab9-156">applicablePlatforms</span></span>|<span data-ttu-id="1bab9-157">colección de [devicePlatformType](../resources/intune-shared-deviceplatformtype.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-157">[devicePlatformType](../resources/intune-shared-deviceplatformtype.md) collection</span></span>|<span data-ttu-id="1bab9-158">Las plataformas aplicables para esta condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1bab9-158">The applicable platforms for this management condition.</span></span> <span data-ttu-id="1bab9-159">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-159">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|

## <a name="relationships"></a><span data-ttu-id="1bab9-160">Relaciones</span><span class="sxs-lookup"><span data-stu-id="1bab9-160">Relationships</span></span>
|<span data-ttu-id="1bab9-161">Relación</span><span class="sxs-lookup"><span data-stu-id="1bab9-161">Relationship</span></span>|<span data-ttu-id="1bab9-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="1bab9-162">Type</span></span>|<span data-ttu-id="1bab9-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="1bab9-163">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="1bab9-164">managementConditionStatements</span><span class="sxs-lookup"><span data-stu-id="1bab9-164">managementConditionStatements</span></span>|<span data-ttu-id="1bab9-165">colección de [managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-165">[managementConditionStatement](../resources/intune-fencing-managementconditionstatement.md) collection</span></span>|<span data-ttu-id="1bab9-166">Las instrucciones de condición de administración asociadas a la condición de administración.</span><span class="sxs-lookup"><span data-stu-id="1bab9-166">The management condition statements associated to the management condition.</span></span> <span data-ttu-id="1bab9-167">Se hereda de [managementCondition](../resources/intune-fencing-managementcondition.md)</span><span class="sxs-lookup"><span data-stu-id="1bab9-167">Inherited from [managementCondition](../resources/intune-fencing-managementcondition.md)</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1bab9-168">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1bab9-168">JSON Representation</span></span>
<span data-ttu-id="1bab9-169">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1bab9-169">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.networkManagementCondition"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.networkManagementCondition",
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





