---
title: tipo de recurso privilegedRole
description: 'Representa una función de administrador de Azure AD, tales como: **Administrador Global, Administrador de facturación, Administrador de servicio, Administrador de usuarios, Administrador de contraseñas**, etcetera.'
localization_priority: Normal
ms.openlocfilehash: 75763e18731cb969623cc4df6360d50abc018b41
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27860861"
---
# <a name="privilegedrole-resource-type"></a><span data-ttu-id="6cb04-103">tipo de recurso privilegedRole</span><span class="sxs-lookup"><span data-stu-id="6cb04-103">privilegedRole resource type</span></span>

> <span data-ttu-id="6cb04-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="6cb04-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="6cb04-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="6cb04-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="6cb04-106">Representa una función de administrador de Azure AD, tales como: **Administrador Global, Administrador de facturación, Administrador de servicio, Administrador de usuarios, Administrador de contraseñas**, etcetera.</span><span class="sxs-lookup"><span data-stu-id="6cb04-106">Represents an Azure AD administrator role, such as: **Global Administrator, Billing Administrator, Service Administrator, User Administrator, Password Administrator**, etc.</span></span>


## <a name="methods"></a><span data-ttu-id="6cb04-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="6cb04-107">Methods</span></span>

| <span data-ttu-id="6cb04-108">Método</span><span class="sxs-lookup"><span data-stu-id="6cb04-108">Method</span></span>           | <span data-ttu-id="6cb04-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6cb04-109">Return Type</span></span>    |<span data-ttu-id="6cb04-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cb04-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="6cb04-111">Objetos de lista de privilegedRole</span><span class="sxs-lookup"><span data-stu-id="6cb04-111">List privilegedRole objects</span></span>](../api/privilegedrole-list.md) | <span data-ttu-id="6cb04-112">colección de [privilegedRole](privilegedrole.md)</span><span class="sxs-lookup"><span data-stu-id="6cb04-112">[privilegedRole](privilegedrole.md) collection</span></span>|<span data-ttu-id="6cb04-113">Obtener la colección de privilegedRole.</span><span class="sxs-lookup"><span data-stu-id="6cb04-113">Get the collection of privilegedRole.</span></span>|
|[<span data-ttu-id="6cb04-114">Obtener privilegedRole</span><span class="sxs-lookup"><span data-stu-id="6cb04-114">Get privilegedRole</span></span>](../api/privilegedrole-get.md) | [<span data-ttu-id="6cb04-115">privilegedRole</span><span class="sxs-lookup"><span data-stu-id="6cb04-115">privilegedRole</span></span>](privilegedrole.md) |<span data-ttu-id="6cb04-116">Leer las propiedades y las relaciones del objeto privilegedRole.</span><span class="sxs-lookup"><span data-stu-id="6cb04-116">Read properties and relationships of privilegedRole object.</span></span>|
|[<span data-ttu-id="6cb04-117">Asignaciones de listas</span><span class="sxs-lookup"><span data-stu-id="6cb04-117">List assignments</span></span>](../api/privilegedrole-list-assignments.md) |<span data-ttu-id="6cb04-118">colección de [privilegedRoleAssignment](privilegedroleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="6cb04-118">[privilegedRoleAssignment](privilegedroleassignment.md) collection</span></span>| <span data-ttu-id="6cb04-119">Obtener una colección de objetos de asignación para esta función.</span><span class="sxs-lookup"><span data-stu-id="6cb04-119">Get a assignment object collection for this role.</span></span>|
|[<span data-ttu-id="6cb04-120">selfActivate</span><span class="sxs-lookup"><span data-stu-id="6cb04-120">selfActivate</span></span>](../api/privilegedrole-selfactivate.md)|[<span data-ttu-id="6cb04-121">privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6cb04-121">privilegedRoleAssignment</span></span>](privilegedroleassignment.md)|<span data-ttu-id="6cb04-122">Activar el rol asignado.</span><span class="sxs-lookup"><span data-stu-id="6cb04-122">Activate the assigned role.</span></span>|
|[<span data-ttu-id="6cb04-123">selfDeactivate</span><span class="sxs-lookup"><span data-stu-id="6cb04-123">selfDeactivate</span></span>](../api/privilegedrole-selfdeactivate.md)|[<span data-ttu-id="6cb04-124">privilegedRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="6cb04-124">privilegedRoleAssignment</span></span>](privilegedroleassignment.md)|<span data-ttu-id="6cb04-125">Desactivar el rol asignado.</span><span class="sxs-lookup"><span data-stu-id="6cb04-125">Deactivate the assigned role.</span></span>|

## <a name="properties"></a><span data-ttu-id="6cb04-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6cb04-126">Properties</span></span>
| <span data-ttu-id="6cb04-127">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6cb04-127">Property</span></span>     | <span data-ttu-id="6cb04-128">Tipo</span><span class="sxs-lookup"><span data-stu-id="6cb04-128">Type</span></span>   |<span data-ttu-id="6cb04-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cb04-129">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6cb04-130">id</span><span class="sxs-lookup"><span data-stu-id="6cb04-130">id</span></span>|<span data-ttu-id="6cb04-131">string</span><span class="sxs-lookup"><span data-stu-id="6cb04-131">string</span></span>|<span data-ttu-id="6cb04-132">El identificador único para el rol de administrador.</span><span class="sxs-lookup"><span data-stu-id="6cb04-132">The unique identifier for administrator role.</span></span> <span data-ttu-id="6cb04-133">Es una cadena GUID y tiene el mismo valor que el identificador de plantilla de rol de Azure AD para el rol determinado.</span><span class="sxs-lookup"><span data-stu-id="6cb04-133">It is a GUID string and has the same value as the role template id from Azure AD for the given role.</span></span> <span data-ttu-id="6cb04-134">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6cb04-134">Read-only.</span></span>|
|<span data-ttu-id="6cb04-135">name</span><span class="sxs-lookup"><span data-stu-id="6cb04-135">name</span></span>|<span data-ttu-id="6cb04-136">string</span><span class="sxs-lookup"><span data-stu-id="6cb04-136">string</span></span>|<span data-ttu-id="6cb04-137">Nombre de la función.</span><span class="sxs-lookup"><span data-stu-id="6cb04-137">Role name.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6cb04-138">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6cb04-138">Relationships</span></span>
| <span data-ttu-id="6cb04-139">Relación</span><span class="sxs-lookup"><span data-stu-id="6cb04-139">Relationship</span></span> | <span data-ttu-id="6cb04-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="6cb04-140">Type</span></span>   |<span data-ttu-id="6cb04-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="6cb04-141">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6cb04-142">asignaciones</span><span class="sxs-lookup"><span data-stu-id="6cb04-142">assignments</span></span>|<span data-ttu-id="6cb04-143">colección de [privilegedRoleAssignment](privilegedroleassignment.md)</span><span class="sxs-lookup"><span data-stu-id="6cb04-143">[privilegedRoleAssignment](privilegedroleassignment.md) collection</span></span>| <span data-ttu-id="6cb04-144">Las asignaciones de este rol.</span><span class="sxs-lookup"><span data-stu-id="6cb04-144">The assignments for this role.</span></span> <span data-ttu-id="6cb04-145">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6cb04-145">Read-only.</span></span> <span data-ttu-id="6cb04-146">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6cb04-146">Nullable.</span></span>|
|<span data-ttu-id="6cb04-147">settings</span><span class="sxs-lookup"><span data-stu-id="6cb04-147">settings</span></span>|[<span data-ttu-id="6cb04-148">privilegedRoleSettings</span><span class="sxs-lookup"><span data-stu-id="6cb04-148">privilegedRoleSettings</span></span>](privilegedrolesettings.md)| <span data-ttu-id="6cb04-149">La configuración de este rol.</span><span class="sxs-lookup"><span data-stu-id="6cb04-149">The settings for this role.</span></span> <span data-ttu-id="6cb04-150">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6cb04-150">Read-only.</span></span> <span data-ttu-id="6cb04-151">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6cb04-151">Nullable.</span></span>|
|<span data-ttu-id="6cb04-152">Resumen</span><span class="sxs-lookup"><span data-stu-id="6cb04-152">summary</span></span>|[<span data-ttu-id="6cb04-153">privilegedRoleSummary</span><span class="sxs-lookup"><span data-stu-id="6cb04-153">privilegedRoleSummary</span></span>](privilegedrolesummary.md)| <span data-ttu-id="6cb04-154">La información de resumen para este rol.</span><span class="sxs-lookup"><span data-stu-id="6cb04-154">The summary information for this role.</span></span> <span data-ttu-id="6cb04-155">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6cb04-155">Read-only.</span></span> <span data-ttu-id="6cb04-156">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="6cb04-156">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="6cb04-157">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6cb04-157">JSON representation</span></span>

<span data-ttu-id="6cb04-158">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="6cb04-158">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.privilegedRole"
}-->

```json
{
  "id": "string (identifier)",
  "name": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "privilegedRole resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
