---
title: tipo de recurso deviceManagementScriptAssignment
description: Contiene propiedades que se usan para asignar una secuencia de comandos de administración de dispositivos a un grupo.
author: tfitzmac
ms.openlocfilehash: d0b08363de392a337338bb2cd892359b8b9a9345
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27351243"
---
# <a name="devicemanagementscriptassignment-resource-type"></a><span data-ttu-id="d2e82-103">tipo de recurso deviceManagementScriptAssignment</span><span class="sxs-lookup"><span data-stu-id="d2e82-103">deviceManagementScriptAssignment resource type</span></span>

> <span data-ttu-id="d2e82-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d2e82-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d2e82-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d2e82-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="d2e82-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="d2e82-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="d2e82-107">Contiene propiedades que se usan para asignar una secuencia de comandos de administración de dispositivos a un grupo.</span><span class="sxs-lookup"><span data-stu-id="d2e82-107">Contains properties used to assign a device management script to a group.</span></span>
## <a name="methods"></a><span data-ttu-id="d2e82-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="d2e82-108">Methods</span></span>
|<span data-ttu-id="d2e82-109">Método</span><span class="sxs-lookup"><span data-stu-id="d2e82-109">Method</span></span>|<span data-ttu-id="d2e82-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2e82-110">Return Type</span></span>|<span data-ttu-id="d2e82-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2e82-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="d2e82-112">Lista deviceManagementScriptAssignments</span><span class="sxs-lookup"><span data-stu-id="d2e82-112">List deviceManagementScriptAssignments</span></span>](../api/intune-devices-devicemanagementscriptassignment-list.md)|<span data-ttu-id="d2e82-113">colección de [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md)</span><span class="sxs-lookup"><span data-stu-id="d2e82-113">[deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) collection</span></span>|<span data-ttu-id="d2e82-114">Propiedades de la lista y relaciones de los objetos [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="d2e82-114">List properties and relationships of the [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) objects.</span></span>|
|[<span data-ttu-id="d2e82-115">Obtener deviceManagementScriptAssignment</span><span class="sxs-lookup"><span data-stu-id="d2e82-115">Get deviceManagementScriptAssignment</span></span>](../api/intune-devices-devicemanagementscriptassignment-get.md)|[<span data-ttu-id="d2e82-116">deviceManagementScriptAssignment</span><span class="sxs-lookup"><span data-stu-id="d2e82-116">deviceManagementScriptAssignment</span></span>](../resources/intune-devices-devicemanagementscriptassignment.md)|<span data-ttu-id="d2e82-117">Leer las propiedades y las relaciones del objeto [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="d2e82-117">Read properties and relationships of the [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) object.</span></span>|
|[<span data-ttu-id="d2e82-118">Crear deviceManagementScriptAssignment</span><span class="sxs-lookup"><span data-stu-id="d2e82-118">Create deviceManagementScriptAssignment</span></span>](../api/intune-devices-devicemanagementscriptassignment-create.md)|[<span data-ttu-id="d2e82-119">deviceManagementScriptAssignment</span><span class="sxs-lookup"><span data-stu-id="d2e82-119">deviceManagementScriptAssignment</span></span>](../resources/intune-devices-devicemanagementscriptassignment.md)|<span data-ttu-id="d2e82-120">Crear un nuevo objeto [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="d2e82-120">Create a new [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) object.</span></span>|
|[<span data-ttu-id="d2e82-121">Eliminar deviceManagementScriptAssignment</span><span class="sxs-lookup"><span data-stu-id="d2e82-121">Delete deviceManagementScriptAssignment</span></span>](../api/intune-devices-devicemanagementscriptassignment-delete.md)|<span data-ttu-id="d2e82-122">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d2e82-122">None</span></span>|<span data-ttu-id="d2e82-123">Elimina un [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md).</span><span class="sxs-lookup"><span data-stu-id="d2e82-123">Deletes a [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md).</span></span>|
|[<span data-ttu-id="d2e82-124">Actualizar deviceManagementScriptAssignment</span><span class="sxs-lookup"><span data-stu-id="d2e82-124">Update deviceManagementScriptAssignment</span></span>](../api/intune-devices-devicemanagementscriptassignment-update.md)|[<span data-ttu-id="d2e82-125">deviceManagementScriptAssignment</span><span class="sxs-lookup"><span data-stu-id="d2e82-125">deviceManagementScriptAssignment</span></span>](../resources/intune-devices-devicemanagementscriptassignment.md)|<span data-ttu-id="d2e82-126">Actualizar las propiedades de un objeto [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) .</span><span class="sxs-lookup"><span data-stu-id="d2e82-126">Update the properties of a [deviceManagementScriptAssignment](../resources/intune-devices-devicemanagementscriptassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="d2e82-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d2e82-127">Properties</span></span>
|<span data-ttu-id="d2e82-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d2e82-128">Property</span></span>|<span data-ttu-id="d2e82-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="d2e82-129">Type</span></span>|<span data-ttu-id="d2e82-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="d2e82-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="d2e82-131">id</span><span class="sxs-lookup"><span data-stu-id="d2e82-131">id</span></span>|<span data-ttu-id="d2e82-132">String</span><span class="sxs-lookup"><span data-stu-id="d2e82-132">String</span></span>|<span data-ttu-id="d2e82-133">Clave de la entidad de asignación de grupo de secuencia de comandos de dispositivo administración.</span><span class="sxs-lookup"><span data-stu-id="d2e82-133">Key of the device management script group assignment entity.</span></span>|
|<span data-ttu-id="d2e82-134">target</span><span class="sxs-lookup"><span data-stu-id="d2e82-134">target</span></span>|[<span data-ttu-id="d2e82-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="d2e82-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="d2e82-136">El identificador de grupo de Active Directory de Azure, nuestro destino son la secuencia de comandos.</span><span class="sxs-lookup"><span data-stu-id="d2e82-136">The Id of the Azure Active Directory group we are targeting the script to.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d2e82-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d2e82-137">Relationships</span></span>
<span data-ttu-id="d2e82-138">Ninguna</span><span class="sxs-lookup"><span data-stu-id="d2e82-138">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="d2e82-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d2e82-139">JSON Representation</span></span>
<span data-ttu-id="d2e82-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="d2e82-140">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceManagementScriptAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceManagementScriptAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





