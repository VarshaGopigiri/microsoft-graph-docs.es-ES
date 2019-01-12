---
title: Tipo de recurso directory (elementos eliminados)
description: . Los elementos eliminados seguirán estando disponible para su restauración durante 30 días. Después de 30 días, los elementos se eliminan permanentemente.
localization_priority: Normal
author: lleonard-msft
ms.prod: microsoft-identity-platform
ms.openlocfilehash: 090b9bf476fcaa928f2c6358565ef86af627b8a9
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27966989"
---
# <a name="directory-resource-type-deleted-items"></a><span data-ttu-id="b0bdd-105">Tipo de recurso directory (elementos eliminados)</span><span class="sxs-lookup"><span data-stu-id="b0bdd-105">directory resource type (deleted items)</span></span>

<span data-ttu-id="b0bdd-106">Representa un elemento eliminado en el directorio.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-106">Represents a deleted item in the directory.</span></span> <span data-ttu-id="b0bdd-107">Cuando se elimina un elemento, se agrega al "contenedor" de elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-107">When an item is deleted, it is added to the deleted items "container".</span></span> <span data-ttu-id="b0bdd-108">Los elementos eliminados seguirán estando disponible para su restauración durante 30 días.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-108">Deleted items will remain available to restore for up to 30 days.</span></span> <span data-ttu-id="b0bdd-109">Después de 30 días, los elementos se eliminan permanentemente.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-109">After 30 days, the items are permanently deleted.</span></span>

<span data-ttu-id="b0bdd-110">Actualmente, la funcionalidad de elementos eliminados solo es compatible con los [grupos](group.md) y [usuarios](users.md) de Office 365.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-110">Currently, deleted items functionality is only supported for Office 365 [groups](group.md) and [users](users.md).</span></span>

## <a name="methods"></a><span data-ttu-id="b0bdd-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="b0bdd-111">Methods</span></span>

| <span data-ttu-id="b0bdd-112">Método</span><span class="sxs-lookup"><span data-stu-id="b0bdd-112">Method</span></span>         | <span data-ttu-id="b0bdd-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0bdd-113">Return Type</span></span> | <span data-ttu-id="b0bdd-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0bdd-114">Description</span></span> |
|:---------------|:------------|:------------|
|[<span data-ttu-id="b0bdd-115">Obtener elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="b0bdd-115">Get deleted item</span></span>](../api/directory-deleteditems-get.md) | [<span data-ttu-id="b0bdd-116">directoryObject</span><span class="sxs-lookup"><span data-stu-id="b0bdd-116">directoryObject</span></span>](directoryobject.md) | <span data-ttu-id="b0bdd-117">Obtiene las propiedades de un elemento eliminado.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-117">Gets the properties of a deleted item.</span></span> |
|[<span data-ttu-id="b0bdd-118">Restaurar elemento eliminado</span><span class="sxs-lookup"><span data-stu-id="b0bdd-118">Restore deleted item</span></span>](../api/directory-deleteditems-restore.md) |[<span data-ttu-id="b0bdd-119">directoryObject</span><span class="sxs-lookup"><span data-stu-id="b0bdd-119">directoryObject</span></span>](directoryobject.md)| <span data-ttu-id="b0bdd-120">Restaura un elemento eliminado recientemente.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-120">Restores a recently deleted item.</span></span> |
|[<span data-ttu-id="b0bdd-121">Enumerar elementos eliminados</span><span class="sxs-lookup"><span data-stu-id="b0bdd-121">List deleted items</span></span>](../api/directory-deleteditems-list.md) |<span data-ttu-id="b0bdd-122">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="b0bdd-122">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="b0bdd-123">Obtiene una lista de elementos eliminados recientemente.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-123">Gets a list of recently deleted items.</span></span> |
|[<span data-ttu-id="b0bdd-124">Eliminar permanentemente un elemento</span><span class="sxs-lookup"><span data-stu-id="b0bdd-124">Permanently delete an item</span></span>](../api/directory-deleteditems-delete.md) | <span data-ttu-id="b0bdd-125">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b0bdd-125">None</span></span> | <span data-ttu-id="b0bdd-126">Elimina permanentemente un elemento.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-126">Permanently deletes an item.</span></span> |
|[<span data-ttu-id="b0bdd-127">Lista de los elementos eliminados que pertenecen a un usuario</span><span class="sxs-lookup"><span data-stu-id="b0bdd-127">List deleted items owned by a user</span></span>](../api/directory-deleteditems-user-owned.md) | <span data-ttu-id="b0bdd-128">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="b0bdd-128">[directoryObject](directoryobject.md) collection</span></span> | <span data-ttu-id="b0bdd-129">Se enumeran los elementos de Active directory que pertenecen a un usuario.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-129">Lists directory items owned by a user.</span></span> |

## <a name="relationships"></a><span data-ttu-id="b0bdd-130">Relaciones</span><span class="sxs-lookup"><span data-stu-id="b0bdd-130">Relationships</span></span>
| <span data-ttu-id="b0bdd-131">Relación</span><span class="sxs-lookup"><span data-stu-id="b0bdd-131">Relationship</span></span> | <span data-ttu-id="b0bdd-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="b0bdd-132">Type</span></span>   |<span data-ttu-id="b0bdd-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0bdd-133">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b0bdd-134">deletedItems</span><span class="sxs-lookup"><span data-stu-id="b0bdd-134">deletedItems</span></span>|<span data-ttu-id="b0bdd-135">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="b0bdd-135">[directoryObject](directoryobject.md) collection</span></span>| <span data-ttu-id="b0bdd-136">Elementos eliminados recientemente</span><span class="sxs-lookup"><span data-stu-id="b0bdd-136">Recently deleted items.</span></span> <span data-ttu-id="b0bdd-137">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-137">Read-only.</span></span> <span data-ttu-id="b0bdd-138">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-138">Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="b0bdd-139">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b0bdd-139">JSON representation</span></span>
<span data-ttu-id="b0bdd-140">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="b0bdd-140">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.directory"
}-->

```json
{
}
```

## <a name="example"></a><span data-ttu-id="b0bdd-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="b0bdd-141">Example</span></span>

<!--{"blockType": "request"}-->
```http
GET https://graph.microsoft.com/v1.0/directory
```

<!--{"blockType": "response", "truncated": true, "@odata.type": "microsoft.graph.directory"}-->
```json
HTTP/1.1 200 OK
Content-Type: application/json

{
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
