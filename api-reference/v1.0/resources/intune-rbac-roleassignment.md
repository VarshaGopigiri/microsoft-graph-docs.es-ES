---
title: Tipo de recurso roleAssignment
description: El recurso de la asignación de roles. Las asignaciones de roles unen la definición de rol con miembros y ámbitos. Puede haber una o más asignaciones de roles por rol. Esto se aplica a los roles integrados y personalizados.
author: tfitzmac
localization_priority: Normal
ms.openlocfilehash: e8506b87975b69f90cf561e776e557bb472f1ffd
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27846154"
---
# <a name="roleassignment-resource-type"></a><span data-ttu-id="96202-106">Tipo de recurso roleAssignment</span><span class="sxs-lookup"><span data-stu-id="96202-106">roleAssignment resource type</span></span>

> <span data-ttu-id="96202-107">**Nota:** El uso de las API de Microsoft Graph para configurar las directivas y los controles de Intune requiere que el cliente tenga la [licencia correcta](https://go.microsoft.com/fwlink/?linkid=839381) para el servicio Intune.</span><span class="sxs-lookup"><span data-stu-id="96202-107">**Note:** Using the Microsoft Graph APIs to configure Intune controls and policies still requires that the Intune service is [correctly licensed](https://go.microsoft.com/fwlink/?linkid=839381) by the customer.</span></span>

<span data-ttu-id="96202-108">El recurso de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="96202-108">The Role Assignment resource.</span></span> <span data-ttu-id="96202-109">Las asignaciones de roles unen la definición de rol con miembros y ámbitos.</span><span class="sxs-lookup"><span data-stu-id="96202-109">Role assignments tie together a role definition with members and scopes.</span></span> <span data-ttu-id="96202-110">Puede haber una o más asignaciones de roles por rol.</span><span class="sxs-lookup"><span data-stu-id="96202-110">There can be one or more role assignments per role.</span></span> <span data-ttu-id="96202-111">Esto se aplica a los roles integrados y personalizados.</span><span class="sxs-lookup"><span data-stu-id="96202-111">This applies to custom and built-in roles.</span></span>
## <a name="methods"></a><span data-ttu-id="96202-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="96202-112">Methods</span></span>
|<span data-ttu-id="96202-113">Método</span><span class="sxs-lookup"><span data-stu-id="96202-113">Method</span></span>|<span data-ttu-id="96202-114">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96202-114">Return Type</span></span>|<span data-ttu-id="96202-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="96202-115">Description</span></span>|
|:---|:---|:---|
|[<span data-ttu-id="96202-116">Enumerar roleAssignments</span><span class="sxs-lookup"><span data-stu-id="96202-116">List roleAssignments</span></span>](../api/intune-rbac-roleassignment-list.md)|<span data-ttu-id="96202-117">Colección [roleAssignment](../resources/intune-rbac-roleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="96202-117">[roleAssignment](../resources/intune-rbac-roleassignment.md) collection</span></span>|<span data-ttu-id="96202-118">Enumere las propiedades y las relaciones de los objetos [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="96202-118">List properties and relationships of the [roleAssignment](../resources/intune-rbac-roleassignment.md) objects.</span></span>|
|[<span data-ttu-id="96202-119">Obtener roleAssignment</span><span class="sxs-lookup"><span data-stu-id="96202-119">Get roleAssignment</span></span>](../api/intune-rbac-roleassignment-get.md)|[<span data-ttu-id="96202-120">roleAssignment</span><span class="sxs-lookup"><span data-stu-id="96202-120">roleAssignment</span></span>](../resources/intune-rbac-roleassignment.md)|<span data-ttu-id="96202-121">Lea las propiedades y las relaciones del objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="96202-121">Read properties and relationships of the [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>|
|[<span data-ttu-id="96202-122">Crear roleAssignment</span><span class="sxs-lookup"><span data-stu-id="96202-122">Create roleAssignment</span></span>](../api/intune-rbac-roleassignment-create.md)|[<span data-ttu-id="96202-123">roleAssignment</span><span class="sxs-lookup"><span data-stu-id="96202-123">roleAssignment</span></span>](../resources/intune-rbac-roleassignment.md)|<span data-ttu-id="96202-124">Cree un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="96202-124">Create a new [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>|
|[<span data-ttu-id="96202-125">Eliminar roleAssignment</span><span class="sxs-lookup"><span data-stu-id="96202-125">Delete roleAssignment</span></span>](../api/intune-rbac-roleassignment-delete.md)|<span data-ttu-id="96202-126">Ninguna</span><span class="sxs-lookup"><span data-stu-id="96202-126">None</span></span>|<span data-ttu-id="96202-127">Elimina un [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="96202-127">Deletes a [roleAssignment](../resources/intune-rbac-roleassignment.md).</span></span>|
|[<span data-ttu-id="96202-128">Actualizar roleAssignment</span><span class="sxs-lookup"><span data-stu-id="96202-128">Update roleAssignment</span></span>](../api/intune-rbac-roleassignment-update.md)|[<span data-ttu-id="96202-129">roleAssignment</span><span class="sxs-lookup"><span data-stu-id="96202-129">roleAssignment</span></span>](../resources/intune-rbac-roleassignment.md)|<span data-ttu-id="96202-130">Actualice las propiedades de un objeto [roleAssignment](../resources/intune-rbac-roleassignment.md).</span><span class="sxs-lookup"><span data-stu-id="96202-130">Update the properties of a [roleAssignment](../resources/intune-rbac-roleassignment.md) object.</span></span>|

## <a name="properties"></a><span data-ttu-id="96202-131">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96202-131">Properties</span></span>
|<span data-ttu-id="96202-132">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96202-132">Property</span></span>|<span data-ttu-id="96202-133">Tipo</span><span class="sxs-lookup"><span data-stu-id="96202-133">Type</span></span>|<span data-ttu-id="96202-134">Descripción</span><span class="sxs-lookup"><span data-stu-id="96202-134">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="96202-135">id</span><span class="sxs-lookup"><span data-stu-id="96202-135">id</span></span>|<span data-ttu-id="96202-136">Cadena</span><span class="sxs-lookup"><span data-stu-id="96202-136">String</span></span>|<span data-ttu-id="96202-137">Clave de la entidad.</span><span class="sxs-lookup"><span data-stu-id="96202-137">Key of the entity.</span></span> <span data-ttu-id="96202-138">Es de solo lectura y generada automáticamente.</span><span class="sxs-lookup"><span data-stu-id="96202-138">This is read-only and automatically generated.</span></span>|
|<span data-ttu-id="96202-139">displayName</span><span class="sxs-lookup"><span data-stu-id="96202-139">displayName</span></span>|<span data-ttu-id="96202-140">Cadena</span><span class="sxs-lookup"><span data-stu-id="96202-140">String</span></span>|<span data-ttu-id="96202-141">El nombre descriptivo o para mostrar de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="96202-141">The display or friendly name of the role Assignment.</span></span>|
|<span data-ttu-id="96202-142">descripción</span><span class="sxs-lookup"><span data-stu-id="96202-142">description</span></span>|<span data-ttu-id="96202-143">Cadena</span><span class="sxs-lookup"><span data-stu-id="96202-143">String</span></span>|<span data-ttu-id="96202-144">Descripción de la asignación de roles.</span><span class="sxs-lookup"><span data-stu-id="96202-144">Description of the Role Assignment.</span></span>|
|<span data-ttu-id="96202-145">resourceScopes</span><span class="sxs-lookup"><span data-stu-id="96202-145">resourceScopes</span></span>|<span data-ttu-id="96202-146">Colección string</span><span class="sxs-lookup"><span data-stu-id="96202-146">String collection</span></span>|<span data-ttu-id="96202-147">Lista de identificadores de grupos de seguridad de miembros del ámbito de roles.</span><span class="sxs-lookup"><span data-stu-id="96202-147">List of ids of role scope member security groups.</span></span>  <span data-ttu-id="96202-148">Estos son los identificadores de Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="96202-148">These are IDs from Azure Active Directory.</span></span>|

## <a name="relationships"></a><span data-ttu-id="96202-149">Relaciones</span><span class="sxs-lookup"><span data-stu-id="96202-149">Relationships</span></span>
|<span data-ttu-id="96202-150">Relación</span><span class="sxs-lookup"><span data-stu-id="96202-150">Relationship</span></span>|<span data-ttu-id="96202-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="96202-151">Type</span></span>|<span data-ttu-id="96202-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="96202-152">Description</span></span>|
|:---|:---|:---|
|<span data-ttu-id="96202-153">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="96202-153">roleDefinition</span></span>|[<span data-ttu-id="96202-154">roleDefinition</span><span class="sxs-lookup"><span data-stu-id="96202-154">roleDefinition</span></span>](../resources/intune-rbac-roledefinition.md)|<span data-ttu-id="96202-155">Definición de rol del que forma parte esta asignación.</span><span class="sxs-lookup"><span data-stu-id="96202-155">Role definition this assignment is part of.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="96202-156">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="96202-156">JSON Representation</span></span>
<span data-ttu-id="96202-157">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="96202-157">Here is a JSON representation of the resource.</span></span>
<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.roleAssignment"
}
-->
``` json
{
  "@odata.type": "#microsoft.graph.roleAssignment",
  "id": "String (identifier)",
  "displayName": "String",
  "description": "String",
  "resourceScopes": [
    "String"
  ]
}
```



