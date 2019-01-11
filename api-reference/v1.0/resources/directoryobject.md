---
title: Tipo de recurso directoryObject
description: Representa un objeto de Azure Active Directory. El tipo **directoryObject** es el tipo base para muchos otros tipos de entidad del directorio.
localization_priority: Priority
ms.openlocfilehash: 0da74c8f034de37bf442fba6d1609623e81da372
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851711"
---
# <a name="directoryobject-resource-type"></a><span data-ttu-id="6e288-104">Tipo de recurso directoryObject</span><span class="sxs-lookup"><span data-stu-id="6e288-104">directoryObject resource type</span></span>

<span data-ttu-id="6e288-p102">Representa un objeto de Azure Active Directory. El tipo **directoryObject** es el tipo base para muchos otros tipos de entidad del directorio.</span><span class="sxs-lookup"><span data-stu-id="6e288-p102">Represents an Azure Active Directory object. The **directoryObject** type is the base type for many other directory entity types.</span></span>

## <a name="methods"></a><span data-ttu-id="6e288-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="6e288-107">Methods</span></span>

| <span data-ttu-id="6e288-108">Método</span><span class="sxs-lookup"><span data-stu-id="6e288-108">Method</span></span>       | <span data-ttu-id="6e288-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6e288-109">Return Type</span></span>  |<span data-ttu-id="6e288-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e288-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="6e288-111">Get directoryObject</span><span class="sxs-lookup"><span data-stu-id="6e288-111">Get directoryObject</span></span>](../api/directoryobject-get.md) | [<span data-ttu-id="6e288-112">directoryObject</span><span class="sxs-lookup"><span data-stu-id="6e288-112">directoryObject</span></span>](directoryobject.md) |<span data-ttu-id="6e288-113">Lee las propiedades de un objeto directory.</span><span class="sxs-lookup"><span data-stu-id="6e288-113">Read the properties  of a directory object.</span></span>|
|[<span data-ttu-id="6e288-114">Delete directoryObject</span><span class="sxs-lookup"><span data-stu-id="6e288-114">Delete directoryObject</span></span>](../api/directoryobject-delete.md) | <span data-ttu-id="6e288-115">None</span><span class="sxs-lookup"><span data-stu-id="6e288-115">None</span></span> |<span data-ttu-id="6e288-116">Elimina un objeto directory.</span><span class="sxs-lookup"><span data-stu-id="6e288-116">Delete a directory object.</span></span> |
|[<span data-ttu-id="6e288-117">checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="6e288-117">checkMemberGroups</span></span>](../api/directoryobject-checkmembergroups.md)|<span data-ttu-id="6e288-118">Colección string</span><span class="sxs-lookup"><span data-stu-id="6e288-118">String collection</span></span>|<span data-ttu-id="6e288-p103">Comprueba la pertenencia a una lista de grupos. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="6e288-p103">Check for membership in a list of groups. The check is transitive.</span></span>|
|[<span data-ttu-id="6e288-121">getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="6e288-121">getMemberGroups</span></span>](../api/directoryobject-getmembergroups.md)|<span data-ttu-id="6e288-122">Colección string</span><span class="sxs-lookup"><span data-stu-id="6e288-122">String collection</span></span>|<span data-ttu-id="6e288-p104">Devuelve todos los grupos de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="6e288-p104">Return all the groups that the user, group, or directory object is a member of. The check is transitive.</span></span>|
|[<span data-ttu-id="6e288-125">getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="6e288-125">getMemberObjects</span></span>](../api/directoryobject-getmemberobjects.md)|<span data-ttu-id="6e288-126">Colección string</span><span class="sxs-lookup"><span data-stu-id="6e288-126">String collection</span></span>| <span data-ttu-id="6e288-p105">Devuelve todos los grupos y roles de directorio de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="6e288-p105">Return all of the groups and directory roles that the user, group, or directory object is a member of. The check is transitive.</span></span> |
|[<span data-ttu-id="6e288-129">getByIds</span><span class="sxs-lookup"><span data-stu-id="6e288-129">getByIds</span></span>](../api/directoryobject-getbyids.md) | <span data-ttu-id="6e288-130">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="6e288-130">[directoryObject](directoryobject.md) collection</span></span> | <span data-ttu-id="6e288-131">Obtenga un conjunto de objetos de directorio basados en un conjunto de identificadores proporcionados.</span><span class="sxs-lookup"><span data-stu-id="6e288-131">Get a set of directory objects based on a set of supplied ids.</span></span> |

## <a name="properties"></a><span data-ttu-id="6e288-132">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6e288-132">Properties</span></span>

| <span data-ttu-id="6e288-133">Propiedad</span><span class="sxs-lookup"><span data-stu-id="6e288-133">Property</span></span>   | <span data-ttu-id="6e288-134">Tipo</span><span class="sxs-lookup"><span data-stu-id="6e288-134">Type</span></span> |<span data-ttu-id="6e288-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="6e288-135">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="6e288-136">id</span><span class="sxs-lookup"><span data-stu-id="6e288-136">id</span></span>|<span data-ttu-id="6e288-137">String</span><span class="sxs-lookup"><span data-stu-id="6e288-137">String</span></span>|<span data-ttu-id="6e288-p106">Guid que es el identificador único para el objeto; por ejemplo, 12345678-9abc-def0-1234-56789abcde. Clave. No admite valores NULL. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="6e288-p106">A Guid that is the unique identifier for the object; for example, 12345678-9abc-def0-1234-56789abcde. Key. Not nullable. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="6e288-142">Relaciones</span><span class="sxs-lookup"><span data-stu-id="6e288-142">Relationships</span></span>

<span data-ttu-id="6e288-143">Ninguno</span><span class="sxs-lookup"><span data-stu-id="6e288-143">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="6e288-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="6e288-144">JSON representation</span></span>

<span data-ttu-id="6e288-145">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="6e288-145">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.directoryObject",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "countable": false,
        "expandable": false,
        "filterable": false,
        "referenceable": false,
        "selectable": false
      }
    }
  ]
}-->

```json
{
  "id": "string (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "directoryObject resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
