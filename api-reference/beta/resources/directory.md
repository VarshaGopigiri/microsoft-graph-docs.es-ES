---
title: Tipo de recurso directory (elementos eliminados)
description: . Los elementos eliminados seguirán estando disponible para su restauración durante 30 días. Después de 30 días, los elementos se eliminan permanentemente.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 2593603afa145d30b5e26a240bb5cd471eab9942
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966555"
---
# <a name="directory-resource-type-deleted-items"></a><span data-ttu-id="fd8cb-105">Tipo de recurso directory (elementos eliminados)</span><span class="sxs-lookup"><span data-stu-id="fd8cb-105">directory resource type (deleted items)</span></span>

> <span data-ttu-id="fd8cb-106">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-106">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="fd8cb-107">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-107">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="fd8cb-108">Representa un elemento eliminado en el directorio.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-108">Represents a deleted item in the directory.</span></span> <span data-ttu-id="fd8cb-109">Cuando se elimina un elemento, se agrega al "contenedor" de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-109">When an item is deleted, it is added to the deleted items "container".</span></span> <span data-ttu-id="fd8cb-110">Los elementos eliminados seguirán estando disponible para su restauración durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-110">Deleted items will remain available to restore for up to 30 days.</span></span> <span data-ttu-id="fd8cb-111">Después de 30 días, los elementos se eliminan permanentemente.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-111">After 30 days, the items are permanently deleted.</span></span>

<span data-ttu-id="fd8cb-112">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los [grupos](group.md) y [usuarios](users.md) de Office 365.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-112">Currently, deleted items functionality is only supported for Office 365 [groups](group.md) and [users](users.md).</span></span>

## <a name="methods"></a><span data-ttu-id="fd8cb-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fd8cb-113">Methods</span></span>

| <span data-ttu-id="fd8cb-114">Método</span><span class="sxs-lookup"><span data-stu-id="fd8cb-114">Method</span></span>         | <span data-ttu-id="fd8cb-115">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fd8cb-115">Return Type</span></span> | <span data-ttu-id="fd8cb-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd8cb-116">Description</span></span> |
|:---------------|:------------|:------------|
|[<span data-ttu-id="fd8cb-117">Obtener elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="fd8cb-117">Get deleted item</span></span>](../api/directory-deleteditems-get.md) | [<span data-ttu-id="fd8cb-118">directoryObject</span><span class="sxs-lookup"><span data-stu-id="fd8cb-118">directoryObject</span></span>](directoryobject.md) | <span data-ttu-id="fd8cb-119">Obtiene las propiedades de un elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-119">Gets the properties of a deleted item.</span></span> |
|[<span data-ttu-id="fd8cb-120">Restaurar elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="fd8cb-120">Restore deleted item</span></span>](../api/directory-deleteditems-restore.md) |[<span data-ttu-id="fd8cb-121">directoryObject</span><span class="sxs-lookup"><span data-stu-id="fd8cb-121">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="fd8cb-122">Restaura un elemento eliminado recientemente.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-122">Restores a recently deleted item.</span></span> |
|[<span data-ttu-id="fd8cb-123">Enumerar elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="fd8cb-123">List deleted items</span></span>](../api/directory-deleteditems-list.md) |<span data-ttu-id="fd8cb-124">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="fd8cb-124">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="fd8cb-125">Obtiene una lista de elementos eliminados recientemente.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-125">Gets a list of recently deleted items.</span></span> |
|[<span data-ttu-id="fd8cb-126">Eliminar permanentemente un elemento</span><span class="sxs-lookup"><span data-stu-id="fd8cb-126">Permanently delete an item</span></span>](../api/directory-deleteditems-delete.md) | <span data-ttu-id="fd8cb-127">Ninguno</span><span class="sxs-lookup"><span data-stu-id="fd8cb-127">None</span></span> | <span data-ttu-id="fd8cb-128">Elimina permanentemente un elemento.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-128">Permanently deletes an item.</span></span> |
|[<span data-ttu-id="fd8cb-129">Lista de los elementos eliminados que pertenecen a un usuario</span><span class="sxs-lookup"><span data-stu-id="fd8cb-129">List deleted items owned by a user</span></span>](../api/directory-deleteditems-user-owned.md) | <span data-ttu-id="fd8cb-130">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="fd8cb-130">[directoryObject](directoryobject.md) collection</span></span> | <span data-ttu-id="fd8cb-131">Se enumeran los elementos de Active directory que pertenecen a un usuario.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-131">Lists directory items owned by a user.</span></span> |

## <a name="properties"></a><span data-ttu-id="fd8cb-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fd8cb-132">Properties</span></span>
| <span data-ttu-id="fd8cb-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fd8cb-133">Property</span></span>   | <span data-ttu-id="fd8cb-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd8cb-134">Type</span></span> |<span data-ttu-id="fd8cb-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd8cb-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fd8cb-136">id</span><span class="sxs-lookup"><span data-stu-id="fd8cb-136">id</span></span>|<span data-ttu-id="fd8cb-137">String</span><span class="sxs-lookup"><span data-stu-id="fd8cb-137">String</span></span>| <span data-ttu-id="fd8cb-138">Identificador único del objeto; por ejemplo, 12345678-9abc-def0-1234-56789abcde.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-138">A unique identifier for the object; for example, 12345678-9abc-def0-1234-56789abcde.</span></span> <span data-ttu-id="fd8cb-139">Clave.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-139">Key.</span></span> <span data-ttu-id="fd8cb-140">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-140">Not nullable.</span></span> <span data-ttu-id="fd8cb-141">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-141">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="fd8cb-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fd8cb-142">Relationships</span></span>
| <span data-ttu-id="fd8cb-143">Relación</span><span class="sxs-lookup"><span data-stu-id="fd8cb-143">Relationship</span></span> | <span data-ttu-id="fd8cb-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd8cb-144">Type</span></span>   |<span data-ttu-id="fd8cb-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd8cb-145">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="fd8cb-146">deleteditems</span><span class="sxs-lookup"><span data-stu-id="fd8cb-146">deleteditems</span></span>|<span data-ttu-id="fd8cb-147">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="fd8cb-147">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="fd8cb-148">Elementos eliminados recientemente</span><span class="sxs-lookup"><span data-stu-id="fd8cb-148">Recently deleted items.</span></span> <span data-ttu-id="fd8cb-149">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-149">Read-only.</span></span> <span data-ttu-id="fd8cb-150">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-150">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="fd8cb-151">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fd8cb-151">JSON representation</span></span>
<span data-ttu-id="fd8cb-152">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="fd8cb-152">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.directory"
}-->

```json
{
  "id": "String (identifier)"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directory resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
