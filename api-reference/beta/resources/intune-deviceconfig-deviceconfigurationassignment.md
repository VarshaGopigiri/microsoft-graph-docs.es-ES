---
title: Tipo de recurso deviceConfigurationAssignment
description: La entidad de asignación de la configuración de dispositivo asigna un grupo AAD a una configuración de dispositivo específico.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 086ff1f3c9d06a1afe394afff0bd7ee6c543804d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888700"
---
# <a name="deviceconfigurationassignment-resource-type"></a><span data-ttu-id="24e0c-103">Tipo de recurso deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="24e0c-103">deviceConfigurationAssignment resource type</span></span>

> <span data-ttu-id="24e0c-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="24e0c-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="24e0c-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="24e0c-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="24e0c-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="24e0c-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="24e0c-107">La entidad de asignación de la configuración de dispositivo asigna un grupo AAD a una configuración de dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="24e0c-107">The device configuration assignment entity assigns an AAD group to a specific device configuration.</span></span>
## <a name="methods"></a><span data-ttu-id="24e0c-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="24e0c-108">Methods</span></span>
|<span data-ttu-id="24e0c-109">Método</span><span class="sxs-lookup"><span data-stu-id="24e0c-109">Method</span></span>|<span data-ttu-id="24e0c-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24e0c-110">Return Type</span></span>|<span data-ttu-id="24e0c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e0c-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="24e0c-112">Enumerar deviceConfigurationAssignments</span><span class="sxs-lookup"><span data-stu-id="24e0c-112">List deviceConfigurationAssignments</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-list.md)|<span data-ttu-id="24e0c-113">Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="24e0c-113">[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) collection</span></span>|<span data-ttu-id="24e0c-114">Enumere las propiedades y las relaciones de los objetos [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="24e0c-114">List properties and relationships of the [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) objects.</span></span>|
|[<span data-ttu-id="24e0c-115">Obtener deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="24e0c-115">Get deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-get.md)|[<span data-ttu-id="24e0c-116">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="24e0c-116">deviceConfigurationAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|<span data-ttu-id="24e0c-117">Lea las propiedades y las relaciones del objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="24e0c-117">Read properties and relationships of the [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>|
|[<span data-ttu-id="24e0c-118">Crear deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="24e0c-118">Create deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-create.md)|[<span data-ttu-id="24e0c-119">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="24e0c-119">deviceConfigurationAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|<span data-ttu-id="24e0c-120">Cree un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="24e0c-120">Create a new [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>|
|[<span data-ttu-id="24e0c-121">Eliminar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="24e0c-121">Delete deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-delete.md)|<span data-ttu-id="24e0c-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="24e0c-122">None</span></span>|<span data-ttu-id="24e0c-123">Elimina un [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="24e0c-123">Deletes a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span></span>|
|[<span data-ttu-id="24e0c-124">Actualizar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="24e0c-124">Update deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-update.md)|[<span data-ttu-id="24e0c-125">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="24e0c-125">deviceConfigurationAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|<span data-ttu-id="24e0c-126">Actualice las propiedades de un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="24e0c-126">Update the properties of a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="24e0c-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="24e0c-127">Properties</span></span>
|<span data-ttu-id="24e0c-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="24e0c-128">Property</span></span>|<span data-ttu-id="24e0c-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="24e0c-129">Type</span></span>|<span data-ttu-id="24e0c-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="24e0c-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="24e0c-131">id</span><span class="sxs-lookup"><span data-stu-id="24e0c-131">id</span></span>|<span data-ttu-id="24e0c-132">String</span><span class="sxs-lookup"><span data-stu-id="24e0c-132">String</span></span>|<span data-ttu-id="24e0c-133">La clave de la asignación.</span><span class="sxs-lookup"><span data-stu-id="24e0c-133">The key of the assignment.</span></span>|
|<span data-ttu-id="24e0c-134">target</span><span class="sxs-lookup"><span data-stu-id="24e0c-134">target</span></span>|[<span data-ttu-id="24e0c-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="24e0c-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="24e0c-136">El destino de la tarea para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="24e0c-136">The assignment target for the device configuration.</span></span>|

## <a name="relationships"></a><span data-ttu-id="24e0c-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="24e0c-137">Relationships</span></span>
<span data-ttu-id="24e0c-138">Ninguna</span><span class="sxs-lookup"><span data-stu-id="24e0c-138">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="24e0c-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="24e0c-139">JSON Representation</span></span>
<span data-ttu-id="24e0c-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="24e0c-140">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceConfigurationAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceConfigurationAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





