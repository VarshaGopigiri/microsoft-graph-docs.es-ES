---
title: tipo de recurso deviceConfigurationGroupAssignment
description: Asignación de grupo de configuración de dispositivo.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: b670ffd828634e244053b8a83e5f1f05f79ebbe1
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27883982"
---
# <a name="deviceconfigurationgroupassignment-resource-type"></a><span data-ttu-id="982d7-103">tipo de recurso deviceConfigurationGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="982d7-103">deviceConfigurationGroupAssignment resource type</span></span>

> <span data-ttu-id="982d7-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="982d7-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="982d7-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="982d7-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="982d7-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="982d7-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="982d7-107">Asignación de grupo de configuración de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="982d7-107">Device configuration group assignment.</span></span>
## <a name="methods"></a><span data-ttu-id="982d7-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="982d7-108">Methods</span></span>
|<span data-ttu-id="982d7-109">Método</span><span class="sxs-lookup"><span data-stu-id="982d7-109">Method</span></span>|<span data-ttu-id="982d7-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="982d7-110">Return Type</span></span>|<span data-ttu-id="982d7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="982d7-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="982d7-112">Lista deviceConfigurationGroupAssignments</span><span class="sxs-lookup"><span data-stu-id="982d7-112">List deviceConfigurationGroupAssignments</span></span>](../api/intune-deviceconfig-deviceconfigurationgroupassignment-list.md)|<span data-ttu-id="982d7-113">colección de [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)</span><span class="sxs-lookup"><span data-stu-id="982d7-113">[deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) collection</span></span>|<span data-ttu-id="982d7-114">Propiedades de la lista y relaciones de los objetos [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="982d7-114">List properties and relationships of the [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) objects.</span></span>|
|[<span data-ttu-id="982d7-115">Obtener deviceConfigurationGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="982d7-115">Get deviceConfigurationGroupAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationgroupassignment-get.md)|[<span data-ttu-id="982d7-116">deviceConfigurationGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="982d7-116">deviceConfigurationGroupAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)|<span data-ttu-id="982d7-117">Leer las propiedades y las relaciones del objeto [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="982d7-117">Read properties and relationships of the [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) object.</span></span>|
|[<span data-ttu-id="982d7-118">Crear deviceConfigurationGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="982d7-118">Create deviceConfigurationGroupAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationgroupassignment-create.md)|[<span data-ttu-id="982d7-119">deviceConfigurationGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="982d7-119">deviceConfigurationGroupAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)|<span data-ttu-id="982d7-120">Crear un nuevo objeto [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="982d7-120">Create a new [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) object.</span></span>|
|[<span data-ttu-id="982d7-121">Eliminar deviceConfigurationGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="982d7-121">Delete deviceConfigurationGroupAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationgroupassignment-delete.md)|<span data-ttu-id="982d7-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="982d7-122">None</span></span>|<span data-ttu-id="982d7-123">Elimina un [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md).</span><span class="sxs-lookup"><span data-stu-id="982d7-123">Deletes a [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md).</span></span>|
|[<span data-ttu-id="982d7-124">Actualizar deviceConfigurationGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="982d7-124">Update deviceConfigurationGroupAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationgroupassignment-update.md)|[<span data-ttu-id="982d7-125">deviceConfigurationGroupAssignment</span><span class="sxs-lookup"><span data-stu-id="982d7-125">deviceConfigurationGroupAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md)|<span data-ttu-id="982d7-126">Actualizar las propiedades de un objeto [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="982d7-126">Update the properties of a [deviceConfigurationGroupAssignment](../resources/intune-deviceconfig-deviceconfigurationgroupassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="982d7-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="982d7-127">Properties</span></span>
|<span data-ttu-id="982d7-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="982d7-128">Property</span></span>|<span data-ttu-id="982d7-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="982d7-129">Type</span></span>|<span data-ttu-id="982d7-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="982d7-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="982d7-131">id</span><span class="sxs-lookup"><span data-stu-id="982d7-131">id</span></span>|<span data-ttu-id="982d7-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="982d7-132">String</span></span>|<span data-ttu-id="982d7-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="982d7-133">Key of the entity.</span></span>|
|<span data-ttu-id="982d7-134">targetGroupId</span><span class="sxs-lookup"><span data-stu-id="982d7-134">targetGroupId</span></span>|<span data-ttu-id="982d7-135">Cadena</span><span class="sxs-lookup"><span data-stu-id="982d7-135">String</span></span>|<span data-ttu-id="982d7-136">El identificador del grupo AAD, nuestro destino son para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="982d7-136">The Id of the AAD group we are targeting the device configuration to.</span></span>|
|<span data-ttu-id="982d7-137">excludeGroup</span><span class="sxs-lookup"><span data-stu-id="982d7-137">excludeGroup</span></span>|<span data-ttu-id="982d7-138">Booleano</span><span class="sxs-lookup"><span data-stu-id="982d7-138">Boolean</span></span>|<span data-ttu-id="982d7-139">Indica si este grupo se deben excluir.</span><span class="sxs-lookup"><span data-stu-id="982d7-139">Indicates if this group is should be excluded.</span></span> <span data-ttu-id="982d7-140">Valores predeterminados que se debe incluir en el grupo</span><span class="sxs-lookup"><span data-stu-id="982d7-140">Defaults that the group should be included</span></span>|

## <a name="relationships"></a><span data-ttu-id="982d7-141">Relaciones</span><span class="sxs-lookup"><span data-stu-id="982d7-141">Relationships</span></span>
|<span data-ttu-id="982d7-142">Relación</span><span class="sxs-lookup"><span data-stu-id="982d7-142">Relationship</span></span>|<span data-ttu-id="982d7-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="982d7-143">Type</span></span>|<span data-ttu-id="982d7-144">Description</span><span class="sxs-lookup"><span data-stu-id="982d7-144">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="982d7-145">deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="982d7-145">deviceConfiguration</span></span>|[<span data-ttu-id="982d7-146">deviceConfiguration</span><span class="sxs-lookup"><span data-stu-id="982d7-146">deviceConfiguration</span></span>](../resources/intune-deviceconfig-deviceconfiguration.md)|<span data-ttu-id="982d7-147">El vínculo de navegación a la configuración de dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="982d7-147">The navigation link to the Device Configuration being targeted.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="982d7-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="982d7-148">JSON Representation</span></span>
<span data-ttu-id="982d7-149">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="982d7-149">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationGroupAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationGroupAssignment",
  "id": "String (identifier)",
  "targetGroupId": "String",
  "excludeGroup": true
}
```





