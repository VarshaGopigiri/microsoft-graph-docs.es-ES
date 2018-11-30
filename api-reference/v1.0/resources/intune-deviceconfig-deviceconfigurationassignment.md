---
title: Tipo de recurso deviceConfigurationAssignment
description: La entidad de asignación de la configuración de dispositivo asigna un grupo AAD a una configuración de dispositivo específico.
ms.openlocfilehash: 75a1c3ceaecf3f19bfbcbeda1baf20ddedce606b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029058"
---
# <a name="deviceconfigurationassignment-resource-type"></a><span data-ttu-id="14caa-103">Tipo de recurso deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="14caa-103">deviceConfigurationAssignment resource type</span></span>

> <span data-ttu-id="14caa-104">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="14caa-104">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="14caa-105">La entidad de asignación de la configuración de dispositivo asigna un grupo AAD a una configuración de dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="14caa-105">The device configuration assignment entity assigns an AAD group to a specific device configuration.</span></span>
## <a name="methods"></a><span data-ttu-id="14caa-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="14caa-106">Methods</span></span>
|<span data-ttu-id="14caa-107">Método</span><span class="sxs-lookup"><span data-stu-id="14caa-107">Method</span></span>|<span data-ttu-id="14caa-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="14caa-108">Return Type</span></span>|<span data-ttu-id="14caa-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="14caa-109">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="14caa-110">Enumerar deviceConfigurationAssignments</span><span class="sxs-lookup"><span data-stu-id="14caa-110">List deviceConfigurationAssignments</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-list.md)|<span data-ttu-id="14caa-111">Colección [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md)</span><span class="sxs-lookup"><span data-stu-id="14caa-111">[deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) collection</span></span>|<span data-ttu-id="14caa-112">Enumere las propiedades y las relaciones de los objetos [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="14caa-112">List properties and relationships of the [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) objects.</span></span>|
|[<span data-ttu-id="14caa-113">Obtener deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="14caa-113">Get deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-get.md)|[<span data-ttu-id="14caa-114">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="14caa-114">deviceConfigurationAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|<span data-ttu-id="14caa-115">Lea las propiedades y las relaciones del objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="14caa-115">Read properties and relationships of the [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>|
|[<span data-ttu-id="14caa-116">Crear deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="14caa-116">Create deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-create.md)|[<span data-ttu-id="14caa-117">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="14caa-117">deviceConfigurationAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|<span data-ttu-id="14caa-118">Cree un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="14caa-118">Create a new [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>|
|[<span data-ttu-id="14caa-119">Eliminar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="14caa-119">Delete deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-delete.md)|<span data-ttu-id="14caa-120">Ninguna</span><span class="sxs-lookup"><span data-stu-id="14caa-120">None</span></span>|<span data-ttu-id="14caa-121">Elimina un [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="14caa-121">Deletes a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span></span>|
|[<span data-ttu-id="14caa-122">Actualizar deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="14caa-122">Update deviceConfigurationAssignment</span></span>](../api/intune-deviceconfig-deviceconfigurationassignment-update.md)|[<span data-ttu-id="14caa-123">deviceConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="14caa-123">deviceConfigurationAssignment</span></span>](../resources/intune-deviceconfig-deviceconfigurationassignment.md)|<span data-ttu-id="14caa-124">Actualice las propiedades de un objeto [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md).</span><span class="sxs-lookup"><span data-stu-id="14caa-124">Update the properties of a [deviceConfigurationAssignment](../resources/intune-deviceconfig-deviceconfigurationassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="14caa-125">Propiedades</span><span class="sxs-lookup"><span data-stu-id="14caa-125">Properties</span></span>
|<span data-ttu-id="14caa-126">Propiedad</span><span class="sxs-lookup"><span data-stu-id="14caa-126">Property</span></span>|<span data-ttu-id="14caa-127">Tipo</span><span class="sxs-lookup"><span data-stu-id="14caa-127">Type</span></span>|<span data-ttu-id="14caa-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="14caa-128">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="14caa-129">id</span><span class="sxs-lookup"><span data-stu-id="14caa-129">id</span></span>|<span data-ttu-id="14caa-130">String</span><span class="sxs-lookup"><span data-stu-id="14caa-130">String</span></span>|<span data-ttu-id="14caa-131">La clave de la asignación.</span><span class="sxs-lookup"><span data-stu-id="14caa-131">The key of the assignment.</span></span>|
|<span data-ttu-id="14caa-132">target</span><span class="sxs-lookup"><span data-stu-id="14caa-132">target</span></span>|[<span data-ttu-id="14caa-133">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="14caa-133">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="14caa-134">El destino de la tarea para la configuración del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="14caa-134">The assignment target for the device configuration.</span></span>|

## <a name="relationships"></a><span data-ttu-id="14caa-135">Relaciones</span><span class="sxs-lookup"><span data-stu-id="14caa-135">Relationships</span></span>
<span data-ttu-id="14caa-136">Ninguna</span><span class="sxs-lookup"><span data-stu-id="14caa-136">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="14caa-137">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="14caa-137">JSON Representation</span></span>
<span data-ttu-id="14caa-138">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="14caa-138">Here is a JSON representation of the resource.</span></span>
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



