---
title: Tipo de recurso deviceCompliancePolicyAssignment
description: Asignación de directivas de cumplimiento de dispositivos.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: 0f49aaf815730ea2c12ced1a811335c3b2779fb5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27822844"
---
# <a name="devicecompliancepolicyassignment-resource-type"></a><span data-ttu-id="bcdf6-103">Tipo de recurso deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bcdf6-103">deviceCompliancePolicyAssignment resource type</span></span>

> <span data-ttu-id="bcdf6-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="bcdf6-104">**Important:** APIs under the / beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="bcdf6-105">No se permite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="bcdf6-105">Use of these APIs in production applications is not supported.</span></span>

> <span data-ttu-id="bcdf6-106">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="bcdf6-106">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="bcdf6-107">Asignación de directivas de cumplimiento de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="bcdf6-107">Device compliance policy assignment.</span></span>
## <a name="methods"></a><span data-ttu-id="bcdf6-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="bcdf6-108">Methods</span></span>
|<span data-ttu-id="bcdf6-109">Método</span><span class="sxs-lookup"><span data-stu-id="bcdf6-109">Method</span></span>|<span data-ttu-id="bcdf6-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bcdf6-110">Return Type</span></span>|<span data-ttu-id="bcdf6-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcdf6-111">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="bcdf6-112">Enumerar deviceCompliancePolicyAssignments</span><span class="sxs-lookup"><span data-stu-id="bcdf6-112">List deviceCompliancePolicyAssignments</span></span>](../api/intune-deviceconfig-devicecompliancepolicyassignment-list.md)|<span data-ttu-id="bcdf6-113">Colección [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)</span><span class="sxs-lookup"><span data-stu-id="bcdf6-113">[deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) collection</span></span>|<span data-ttu-id="bcdf6-114">Enumere las propiedades y las relaciones de los objetos [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="bcdf6-114">List properties and relationships of the [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) objects.</span></span>|
|[<span data-ttu-id="bcdf6-115">Obtener deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bcdf6-115">Get deviceCompliancePolicyAssignment</span></span>](../api/intune-deviceconfig-devicecompliancepolicyassignment-get.md)|[<span data-ttu-id="bcdf6-116">deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bcdf6-116">deviceCompliancePolicyAssignment</span></span>](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)|<span data-ttu-id="bcdf6-117">Lea las propiedades y las relaciones del objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="bcdf6-117">Read properties and relationships of the [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object.</span></span>|
|[<span data-ttu-id="bcdf6-118">Crear deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bcdf6-118">Create deviceCompliancePolicyAssignment</span></span>](../api/intune-deviceconfig-devicecompliancepolicyassignment-create.md)|[<span data-ttu-id="bcdf6-119">deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bcdf6-119">deviceCompliancePolicyAssignment</span></span>](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)|<span data-ttu-id="bcdf6-120">Cree un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="bcdf6-120">Create a new [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object.</span></span>|
|[<span data-ttu-id="bcdf6-121">Eliminar deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bcdf6-121">Delete deviceCompliancePolicyAssignment</span></span>](../api/intune-deviceconfig-devicecompliancepolicyassignment-delete.md)|<span data-ttu-id="bcdf6-122">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bcdf6-122">None</span></span>|<span data-ttu-id="bcdf6-123">Elimina un [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="bcdf6-123">Deletes a [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span></span>|
|[<span data-ttu-id="bcdf6-124">Actualizar deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bcdf6-124">Update deviceCompliancePolicyAssignment</span></span>](../api/intune-deviceconfig-devicecompliancepolicyassignment-update.md)|[<span data-ttu-id="bcdf6-125">deviceCompliancePolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="bcdf6-125">deviceCompliancePolicyAssignment</span></span>](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md)|<span data-ttu-id="bcdf6-126">Actualice las propiedades de un objeto [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md).</span><span class="sxs-lookup"><span data-stu-id="bcdf6-126">Update the properties of a [deviceCompliancePolicyAssignment](../resources/intune-deviceconfig-devicecompliancepolicyassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="bcdf6-127">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bcdf6-127">Properties</span></span>
|<span data-ttu-id="bcdf6-128">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bcdf6-128">Property</span></span>|<span data-ttu-id="bcdf6-129">Tipo</span><span class="sxs-lookup"><span data-stu-id="bcdf6-129">Type</span></span>|<span data-ttu-id="bcdf6-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcdf6-130">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="bcdf6-131">id</span><span class="sxs-lookup"><span data-stu-id="bcdf6-131">id</span></span>|<span data-ttu-id="bcdf6-132">Cadena</span><span class="sxs-lookup"><span data-stu-id="bcdf6-132">String</span></span>|<span data-ttu-id="bcdf6-133">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="bcdf6-133">Key of the entity.</span></span>|
|<span data-ttu-id="bcdf6-134">target</span><span class="sxs-lookup"><span data-stu-id="bcdf6-134">target</span></span>|[<span data-ttu-id="bcdf6-135">deviceAndAppManagementAssignmentTarget</span><span class="sxs-lookup"><span data-stu-id="bcdf6-135">deviceAndAppManagementAssignmentTarget</span></span>](../resources/intune-shared-deviceandappmanagementassignmenttarget.md)|<span data-ttu-id="bcdf6-136">Destino de la asignación de directivas de cumplimiento</span><span class="sxs-lookup"><span data-stu-id="bcdf6-136">Target for the compliance policy assignment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bcdf6-137">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bcdf6-137">Relationships</span></span>
<span data-ttu-id="bcdf6-138">Ninguna</span><span class="sxs-lookup"><span data-stu-id="bcdf6-138">None</span></span>
## <a name="json-representation"></a><span data-ttu-id="bcdf6-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bcdf6-139">JSON Representation</span></span>
<span data-ttu-id="bcdf6-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bcdf6-140">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.deviceCompliancePolicyAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.deviceCompliancePolicyAssignment",
  "id": "String (identifier)",
  "target": {
    "@odata.type": "microsoft.graph.deviceAndAppManagementAssignmentTarget"
  }
}
```





