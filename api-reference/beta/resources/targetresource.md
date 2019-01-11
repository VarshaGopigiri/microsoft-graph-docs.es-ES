---
title: tipo de recurso targetResource
description: Indica una colección de tipos de recurso de destino asociado con la actividad de auditoría. Cada tipo de recurso de destino heredará las propiedades que se describen a continuación de este recurso.
localization_priority: Normal
ms.openlocfilehash: f86cfe45870292dae93327859c32d38aa2b252fd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27828682"
---
# <a name="targetresource-resource-type"></a><span data-ttu-id="1229e-104">tipo de recurso targetResource</span><span class="sxs-lookup"><span data-stu-id="1229e-104">targetResource resource type</span></span>
<span data-ttu-id="1229e-105">Indica una colección de tipos de recurso de destino asociado con la actividad de auditoría.</span><span class="sxs-lookup"><span data-stu-id="1229e-105">Indicates a collection of  target resource types associated with the audit activity.</span></span> <span data-ttu-id="1229e-106">Cada tipo de recurso de destino heredará las propiedades que se describen a continuación de este recurso.</span><span class="sxs-lookup"><span data-stu-id="1229e-106">Each target resource type will inherit the properties outlined below from this resource.</span></span>


## <a name="properties"></a><span data-ttu-id="1229e-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1229e-107">Properties</span></span>
| <span data-ttu-id="1229e-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1229e-108">Property</span></span>     | <span data-ttu-id="1229e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="1229e-109">Type</span></span>   |<span data-ttu-id="1229e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="1229e-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1229e-111">displayName</span><span class="sxs-lookup"><span data-stu-id="1229e-111">displayName</span></span>|<span data-ttu-id="1229e-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="1229e-112">String</span></span>|<span data-ttu-id="1229e-113">Indica el nombre para mostrar de los recursos que se describen en los siguientes tipos de recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="1229e-113">Indicates the display name of the resources outlined under Target Resource Types below.</span></span>|
|<span data-ttu-id="1229e-114">id</span><span class="sxs-lookup"><span data-stu-id="1229e-114">id</span></span>|<span data-ttu-id="1229e-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="1229e-115">String</span></span>|<span data-ttu-id="1229e-116">Indica el identificador único del recurso (por ejemplo: el identificador de función UserId, AppId,.).</span><span class="sxs-lookup"><span data-stu-id="1229e-116">Indicates the Unique Id of the resource (For example: UserId, AppId, RoleId.).</span></span>|
|<span data-ttu-id="1229e-117">modifiedProperties</span><span class="sxs-lookup"><span data-stu-id="1229e-117">modifiedProperties</span></span>|<span data-ttu-id="1229e-118">colección de [modifiedProperty](modifiedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="1229e-118">[modifiedProperty](modifiedproperty.md) collection</span></span>|<span data-ttu-id="1229e-119">Indica el nombre, el valor anterior y el nuevo valor de cada atributo que ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="1229e-119">Indicates name, old value and new value of each attribute that changed.</span></span> <span data-ttu-id="1229e-120">Esto es aplicable para las actividades de "Actualización"</span><span class="sxs-lookup"><span data-stu-id="1229e-120">This is applicable for any "Update" activities</span></span>|

### <a name="target-resource-types"></a><span data-ttu-id="1229e-121">Tipos de recursos de destino</span><span class="sxs-lookup"><span data-stu-id="1229e-121">Target Resource Types</span></span>

<span data-ttu-id="1229e-122">El tipo de recurso de destino varía según el recurso subyacente:</span><span class="sxs-lookup"><span data-stu-id="1229e-122">The target resource type varies according to the underlying resource:</span></span>

|<span data-ttu-id="1229e-123">Nombre de recurso</span><span class="sxs-lookup"><span data-stu-id="1229e-123">Resource Name</span></span>| <span data-ttu-id="1229e-124">Referencia</span><span class="sxs-lookup"><span data-stu-id="1229e-124">Reference</span></span>|
|-------------|----------|
<span data-ttu-id="1229e-125">Device</span><span class="sxs-lookup"><span data-stu-id="1229e-125">Device</span></span>|[<span data-ttu-id="1229e-126">targetResourceDevice</span><span class="sxs-lookup"><span data-stu-id="1229e-126">targetResourceDevice</span></span>](targetresourcedevice.md)
<span data-ttu-id="1229e-127">Directorio</span><span class="sxs-lookup"><span data-stu-id="1229e-127">Directory</span></span>|<span data-ttu-id="1229e-128">[targetResourceDirectory] (targetresourcedirectory.md]</span><span class="sxs-lookup"><span data-stu-id="1229e-128">[targetResourceDirectory](targetresourcedirectory.md]</span></span>
<span data-ttu-id="1229e-129">Group</span><span class="sxs-lookup"><span data-stu-id="1229e-129">Group</span></span>|[<span data-ttu-id="1229e-130">targetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1229e-130">targetResourceGroup</span></span>](targetresourcegroup.md)
<span data-ttu-id="1229e-131">Directiva</span><span class="sxs-lookup"><span data-stu-id="1229e-131">Policy</span></span>|[<span data-ttu-id="1229e-132">targetResourcePolicy</span><span class="sxs-lookup"><span data-stu-id="1229e-132">targetResourcePolicy</span></span>](targetresourcepolicy.md)
<span data-ttu-id="1229e-133">Role</span><span class="sxs-lookup"><span data-stu-id="1229e-133">Role</span></span>|[<span data-ttu-id="1229e-134">targetResourceRole</span><span class="sxs-lookup"><span data-stu-id="1229e-134">targetResourceRole</span></span>](targetresourcerole.md)
<span data-ttu-id="1229e-135">Entidad de seguridad de servicio</span><span class="sxs-lookup"><span data-stu-id="1229e-135">Service Principal</span></span>|[<span data-ttu-id="1229e-136">targetResourceServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="1229e-136">targetResourceServicePrincipal</span></span>](targetresourceserviceprincipal.md)
<span data-ttu-id="1229e-137">User</span><span class="sxs-lookup"><span data-stu-id="1229e-137">User</span></span>|[<span data-ttu-id="1229e-138">targetResourceUser</span><span class="sxs-lookup"><span data-stu-id="1229e-138">targetResourceUser</span></span>](targetresourceuser.md)
<span data-ttu-id="1229e-139">Otros</span><span class="sxs-lookup"><span data-stu-id="1229e-139">Other</span></span>|[<span data-ttu-id="1229e-140">targetResourceOther</span><span class="sxs-lookup"><span data-stu-id="1229e-140">targetResourceOther</span></span>](targetresourceother.md)

## <a name="json-representation"></a><span data-ttu-id="1229e-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1229e-141">JSON representation</span></span>

<span data-ttu-id="1229e-142">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1229e-142">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.targetResource"
}-->

```json
{
  "displayName": "String",
  "id": "String",
  "modifiedProperties": [{"@odata.type": "microsoft.graph.modifiedProperty"}]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "targetResource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
