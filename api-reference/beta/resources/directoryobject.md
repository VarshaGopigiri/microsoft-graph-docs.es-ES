---
title: Tipo de recurso directoryObject
description: Representa un objeto de Azure Active Directory. El tipo **directoryObject** es el tipo base para muchos otros tipos de entidad del directorio.
localization_priority: Priority
ms.openlocfilehash: a03ec966f966df556ab0122958b0b8f5464cf4fc
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27889722"
---
# <a name="directoryobject-resource-type"></a><span data-ttu-id="d0469-104">Tipo de recurso directoryObject</span><span class="sxs-lookup"><span data-stu-id="d0469-104">directoryObject resource type</span></span>

> <span data-ttu-id="d0469-105">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d0469-105">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d0469-106">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d0469-106">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d0469-p103">Representa un objeto de Azure Active Directory. El tipo **directoryObject** es el tipo base para muchos otros tipos de entidad del directorio.</span><span class="sxs-lookup"><span data-stu-id="d0469-p103">Represents an Azure Active Directory object. The **directoryObject** type is the base type for many other directory entity types.</span></span>

<span data-ttu-id="d0469-109">Este recurso admite:</span><span class="sxs-lookup"><span data-stu-id="d0469-109">This resource supports:</span></span>

- <span data-ttu-id="d0469-110">que use una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/directoryobject-delta.md).</span><span class="sxs-lookup"><span data-stu-id="d0469-110">Using [delta query](/graph/delta-query-overview) to track incremental additions, deletions, and updates, by providing a [delta](../api/directoryobject-delta.md) function.</span></span>

## <a name="methods"></a><span data-ttu-id="d0469-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="d0469-111">Methods</span></span>

| <span data-ttu-id="d0469-112">Método</span><span class="sxs-lookup"><span data-stu-id="d0469-112">Method</span></span>       | <span data-ttu-id="d0469-113">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0469-113">Return Type</span></span>  |<span data-ttu-id="d0469-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0469-114">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d0469-115">Get directoryObject</span><span class="sxs-lookup"><span data-stu-id="d0469-115">Get directoryObject</span></span>](../api/directoryobject-get.md) | [<span data-ttu-id="d0469-116">directoryObject</span><span class="sxs-lookup"><span data-stu-id="d0469-116">directoryObject</span></span>](directoryobject.md) |<span data-ttu-id="d0469-117">Lee las propiedades de un objeto directory.</span><span class="sxs-lookup"><span data-stu-id="d0469-117">Read the properties  of a directory object.</span></span>|
|[<span data-ttu-id="d0469-118">Delete</span><span class="sxs-lookup"><span data-stu-id="d0469-118">Delete</span></span>](../api/directoryobject-delete.md) | <span data-ttu-id="d0469-119">None</span><span class="sxs-lookup"><span data-stu-id="d0469-119">None</span></span> |<span data-ttu-id="d0469-120">Elimina un objeto directory.</span><span class="sxs-lookup"><span data-stu-id="d0469-120">Delete a directory object.</span></span> |
|[<span data-ttu-id="d0469-121">checkMemberGroups</span><span class="sxs-lookup"><span data-stu-id="d0469-121">checkMemberGroups</span></span>](../api/directoryobject-checkmembergroups.md)|<span data-ttu-id="d0469-122">Colección string</span><span class="sxs-lookup"><span data-stu-id="d0469-122">String collection</span></span>|<span data-ttu-id="d0469-p104">Comprueba la pertenencia a una lista de grupos. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="d0469-p104">Check for membership in a list of groups. The check is transitive.</span></span>|
|[<span data-ttu-id="d0469-125">getMemberGroups</span><span class="sxs-lookup"><span data-stu-id="d0469-125">getMemberGroups</span></span>](../api/directoryobject-getmembergroups.md)|<span data-ttu-id="d0469-126">Colección string</span><span class="sxs-lookup"><span data-stu-id="d0469-126">String collection</span></span>|<span data-ttu-id="d0469-p105">Devuelve todos los grupos de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="d0469-p105">Return all the groups that the user, group, or directory object is a member of. The check is transitive.</span></span>|
|[<span data-ttu-id="d0469-129">getMemberObjects</span><span class="sxs-lookup"><span data-stu-id="d0469-129">getMemberObjects</span></span>](../api/directoryobject-getmemberobjects.md)|<span data-ttu-id="d0469-130">Colección string</span><span class="sxs-lookup"><span data-stu-id="d0469-130">String collection</span></span>| <span data-ttu-id="d0469-p106">Devuelve todos los grupos y roles de directorio de los que el usuario, grupo u objeto de directorio sea miembro. La comprobación es transitiva.</span><span class="sxs-lookup"><span data-stu-id="d0469-p106">Return all of the groups and directory roles that the user, group, or directory object is a member of. The check is transitive.</span></span> |
|[<span data-ttu-id="d0469-133">getByIds</span><span class="sxs-lookup"><span data-stu-id="d0469-133">getByIds</span></span>](../api/directoryobject-getbyids.md) | <span data-ttu-id="d0469-134">Colección [directoryObject](directoryobject.md)</span><span class="sxs-lookup"><span data-stu-id="d0469-134">[directoryObject](directoryobject.md) collection</span></span> | <span data-ttu-id="d0469-135">Obtenga un conjunto de objetos de directorio basados en un conjunto de identificadores proporcionados.</span><span class="sxs-lookup"><span data-stu-id="d0469-135">Get a set of directory objects based on a set of supplied ids.</span></span> |
|[<span data-ttu-id="d0469-136">validateProperties</span><span class="sxs-lookup"><span data-stu-id="d0469-136">validateProperties</span></span>](../api/directoryobject-validateproperties.md)|<span data-ttu-id="d0469-137">JSON</span><span class="sxs-lookup"><span data-stu-id="d0469-137">JSON</span></span>| <span data-ttu-id="d0469-138">Validar el nombre para mostrar de un grupo de Office 365 o alias de correo cumplen con las políticas de nomenclatura.</span><span class="sxs-lookup"><span data-stu-id="d0469-138">Validate an Office 365 group's display name or mail nickname complies with naming policies.</span></span> |
|[<span data-ttu-id="d0469-139">delta</span><span class="sxs-lookup"><span data-stu-id="d0469-139">delta</span></span>](../api/directoryobject-delta.md)|<span data-ttu-id="d0469-140">Colección directoryObject</span><span class="sxs-lookup"><span data-stu-id="d0469-140">directoryObject collection</span></span>| <span data-ttu-id="d0469-141">Obtener cambios incrementales para los objetos de Active directory.</span><span class="sxs-lookup"><span data-stu-id="d0469-141">Get incremental changes for directory objects.</span></span> <span data-ttu-id="d0469-142">Admite el filtrado por tipo de derivadas.</span><span class="sxs-lookup"><span data-stu-id="d0469-142">Supports filtering by derrived type.</span></span> |

## <a name="properties"></a><span data-ttu-id="d0469-143">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0469-143">Properties</span></span>

| <span data-ttu-id="d0469-144">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0469-144">Property</span></span>   | <span data-ttu-id="d0469-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="d0469-145">Type</span></span> |<span data-ttu-id="d0469-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0469-146">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d0469-147">id</span><span class="sxs-lookup"><span data-stu-id="d0469-147">id</span></span>|<span data-ttu-id="d0469-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="d0469-148">String</span></span>|<span data-ttu-id="d0469-149">Un Guid que es el identificador único para el objeto; Por ejemplo, 12345678 9abc def0 1234 56789abcde12.</span><span class="sxs-lookup"><span data-stu-id="d0469-149">A Guid that is the unique identifier for the object; for example, 12345678-9abc-def0-1234-56789abcde12.</span></span> <span data-ttu-id="d0469-150">Clave.</span><span class="sxs-lookup"><span data-stu-id="d0469-150">Key.</span></span> <span data-ttu-id="d0469-151">No admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="d0469-151">Not nullable.</span></span> <span data-ttu-id="d0469-152">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d0469-152">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d0469-153">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d0469-153">Relationships</span></span>

<span data-ttu-id="d0469-154">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d0469-154">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="d0469-155">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d0469-155">JSON representation</span></span>

<span data-ttu-id="d0469-156">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d0469-156">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.directoryObject"
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
