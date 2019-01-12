---
title: Tipo de recurso deviceConfigurationAssignment
description: La entidad de asignación de la configuración de dispositivo asigna un grupo AAD a una configuración de dispositivo específico.
author: tfitzmac
localization_priority: Normal
ms.prod: intune
ms.openlocfilehash: 5a4a527f8b9da9f11d521311c54697fd04c4f019
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27940914"
---
# <a name="deviceconfigurationassignment-resource-type"></a><span data-ttu-id="ddad4-103">Tipo de recurso deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="ddad4-103">deviceConfigurationAssignment resource type</span></span>

> <span data-ttu-id="ddad4-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="ddad4-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="ddad4-105">La entidad de asignación de la configuración de dispositivo asigna un grupo AAD a una configuración de dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="ddad4-105">The device configuration assignment entity assigns an AAD group to a specific device configuration.</span></span>
## <a name="methods"></a><span data-ttu-id="ddad4-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="ddad4-106">Methods</span></span>
|<span data-ttu-id="ddad4-107">Método</span><span class="sxs-lookup"><span data-stu-id="ddad4-107">Method</span></span>|<span data-ttu-id="ddad4-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ddad4-108">Return Type</span></span>|<span data-ttu-id="ddad4-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddad4-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="ddad4-110">Enumerar deviceConfigurationAssignments</span><span class="sxs-lookup"><span data-stu-id="ddad4-110">List deviceConfigurationAssignments</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-list.md)|<span data-ttu-id="ddad4-111">Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="ddad4-111">[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) collection</span></span>|<span data-ttu-id="ddad4-112">Enumere las propiedades y las relaciones de los objetos [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ddad4-112">List properties and relationships of the [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) objects.</span></span>|
|[<span data-ttu-id="ddad4-113">Obtener deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="ddad4-113">Get deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-get.md)|[<span data-ttu-id="ddad4-114">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="ddad4-114">deviceConfigurationAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|<span data-ttu-id="ddad4-115">Lea las propiedades y las relaciones del objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ddad4-115">Read properties and relationships of the [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>|
|[<span data-ttu-id="ddad4-116">Crear deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="ddad4-116">Create deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-create.md)|[<span data-ttu-id="ddad4-117">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="ddad4-117">deviceConfigurationAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|<span data-ttu-id="ddad4-118">Cree un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ddad4-118">Create a new [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>|
|[<span data-ttu-id="ddad4-119">Eliminar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="ddad4-119">Delete deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-delete.md)|<span data-ttu-id="ddad4-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ddad4-120">None</span></span>|<span data-ttu-id="ddad4-121">Elimina un [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ddad4-121">Deletes a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span></span>|
|[<span data-ttu-id="ddad4-122">Actualizar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="ddad4-122">Update deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-update.md)|[<span data-ttu-id="ddad4-123">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="ddad4-123">deviceConfigurationAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|<span data-ttu-id="ddad4-124">Actualice las propiedades de un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="ddad4-124">Update the properties of a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="ddad4-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ddad4-125">Properties</span></span>
|<span data-ttu-id="ddad4-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ddad4-126">Property</span></span>|<span data-ttu-id="ddad4-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddad4-127">Type</span></span>|<span data-ttu-id="ddad4-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddad4-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="ddad4-129">id</span><span class="sxs-lookup"><span data-stu-id="ddad4-129">id</span></span>|<span data-ttu-id="ddad4-130">String</span><span class="sxs-lookup"><span data-stu-id="ddad4-130">String</span></span>|<span data-ttu-id="ddad4-131">La clave de la asignación.</span><span class="sxs-lookup"><span data-stu-id="ddad4-131">The key of the assignment.</span></span>|
|<span data-ttu-id="ddad4-132">target</span><span class="sxs-lookup"><span data-stu-id="ddad4-132">target</span></span>|[<span data-ttu-id="ddad4-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="ddad4-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="ddad4-134">El destino de la tarea para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ddad4-134">The assignment target for the device configuration.</span></span>|

## <a name="relationships"></a><span data-ttu-id="ddad4-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="ddad4-135">Relationships</span></span>
<span data-ttu-id="ddad4-136">Ninguna</span><span class="sxs-lookup"><span data-stu-id="ddad4-136">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="ddad4-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ddad4-137">JSON Representation</span></span>
<span data-ttu-id="ddad4-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="ddad4-138">Here is a JSON representation of the resource.</span></span>
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



