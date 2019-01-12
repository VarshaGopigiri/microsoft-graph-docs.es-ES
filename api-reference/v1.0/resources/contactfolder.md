---
title: Tipo de recurso contactFolder
description: Una carpeta que contiene contactos.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 6cf4d6ed75427dce527ced6cb64d0cdcb9afed99
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27949048"
---
# <a name="contactfolder-resource-type"></a><span data-ttu-id="d1618-103">Tipo de recurso contactFolder</span><span class="sxs-lookup"><span data-stu-id="d1618-103">contactFolder resource type</span></span>

<span data-ttu-id="d1618-104">Una carpeta que contiene contactos.</span><span class="sxs-lookup"><span data-stu-id="d1618-104">A folder that contains contacts.</span></span>

<span data-ttu-id="d1618-105">Este recurso es compatible con el uso de una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/contactfolder-delta.md).</span><span class="sxs-lookup"><span data-stu-id="d1618-105">This resource supports using [delta query](/graph/delta-query-overview) to track incremental additions, deletions, and updates, by providing a [delta](../api/contactfolder-delta.md) function.</span></span>


## <a name="methods"></a><span data-ttu-id="d1618-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="d1618-106">Methods</span></span>

| <span data-ttu-id="d1618-107">Método</span><span class="sxs-lookup"><span data-stu-id="d1618-107">Method</span></span>       | <span data-ttu-id="d1618-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d1618-108">Return Type</span></span>  |<span data-ttu-id="d1618-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1618-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d1618-110">Obtener contactFolder</span><span class="sxs-lookup"><span data-stu-id="d1618-110">Get contactFolder</span></span>](../api/contactfolder-get.md) | [<span data-ttu-id="d1618-111">contactFolder</span><span class="sxs-lookup"><span data-stu-id="d1618-111">contactFolder</span></span>](contactfolder.md) |<span data-ttu-id="d1618-112">Obtenga una carpeta de contactos mediante el identificador de carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="d1618-112">Get a contact folder by using the contact folder ID.</span></span>|
|[<span data-ttu-id="d1618-113">Actualizar</span><span class="sxs-lookup"><span data-stu-id="d1618-113">Update</span></span>](../api/contactfolder-update.md) | [<span data-ttu-id="d1618-114">contactFolder</span><span class="sxs-lookup"><span data-stu-id="d1618-114">contactFolder</span></span>](contactfolder.md) |<span data-ttu-id="d1618-115">Actualice el objeto contactFolder.</span><span class="sxs-lookup"><span data-stu-id="d1618-115">Update contactFolder object.</span></span> |
|[<span data-ttu-id="d1618-116">Eliminar</span><span class="sxs-lookup"><span data-stu-id="d1618-116">Delete</span></span>](../api/contactfolder-delete.md) | <span data-ttu-id="d1618-117">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d1618-117">None</span></span> |<span data-ttu-id="d1618-118">Elimine el objeto contactFolder.</span><span class="sxs-lookup"><span data-stu-id="d1618-118">Delete contactFolder object.</span></span> |
|[<span data-ttu-id="d1618-119">Enumerar childFolders</span><span class="sxs-lookup"><span data-stu-id="d1618-119">List childFolders</span></span>](../api/contactfolder-list-childfolders.md) |<span data-ttu-id="d1618-120">Colección [ContactFolder](contactfolder.md)</span><span class="sxs-lookup"><span data-stu-id="d1618-120">[ContactFolder](contactfolder.md) collection</span></span>| <span data-ttu-id="d1618-121">Obtenga una colección de carpetas secundarias en la carpeta de contactos especificada.</span><span class="sxs-lookup"><span data-stu-id="d1618-121">Get a collection of child folders under the specified contact folder.</span></span>|
|[<span data-ttu-id="d1618-122">Crear contactFolder secundario</span><span class="sxs-lookup"><span data-stu-id="d1618-122">Create child contactFolder</span></span>](../api/contactfolder-post-childfolders.md) |[<span data-ttu-id="d1618-123">ContactFolder</span><span class="sxs-lookup"><span data-stu-id="d1618-123">ContactFolder</span></span>](contactfolder.md)| <span data-ttu-id="d1618-124">Cree una contactFolder como elemento secundario de una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="d1618-124">Create a new contactFolder as a child of a specified folder.</span></span>|
|[<span data-ttu-id="d1618-125">delta</span><span class="sxs-lookup"><span data-stu-id="d1618-125">delta</span></span>](../api/contact-delta.md)|<span data-ttu-id="d1618-126">Colección [contact](contact.md)</span><span class="sxs-lookup"><span data-stu-id="d1618-126">[contact](contact.md) collection</span></span>| <span data-ttu-id="d1618-127">Obtenga un conjunto de carpetas de contactos que se hayan agregado, eliminado o quitado del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="d1618-127">Get a set of contact folders that have been added, deleted, or removed from the user's mailbox.</span></span>|
|[<span data-ttu-id="d1618-128">Enumerar contactos en la carpeta</span><span class="sxs-lookup"><span data-stu-id="d1618-128">List contacts in folder</span></span>](../api/contactfolder-list-contacts.md) |<span data-ttu-id="d1618-129">Colección [contact](contact.md)</span><span class="sxs-lookup"><span data-stu-id="d1618-129">[Contact](contact.md) collection</span></span>| <span data-ttu-id="d1618-130">Obtenga una colección de contactos de la carpeta de contactos predeterminada del usuario que ha iniciado sesión (`.../me/contacts`) o de la carpeta de contactos especificada.</span><span class="sxs-lookup"><span data-stu-id="d1618-130">Get a contact collection from the default Contacts folder of the signed-in user (`.../me/contacts`), or from the specified contact folder.</span></span>|
|[<span data-ttu-id="d1618-131">Crear contacto en la carpeta</span><span class="sxs-lookup"><span data-stu-id="d1618-131">Create contact in folder</span></span>](../api/contactfolder-post-contacts.md) |[<span data-ttu-id="d1618-132">Contact</span><span class="sxs-lookup"><span data-stu-id="d1618-132">Contact</span></span>](contact.md)| <span data-ttu-id="d1618-133">Agregue un contacto a la carpeta de contactos raíz o al extremo de `contacts` de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="d1618-133">Add a contact to the root Contacts folder or to the `contacts` endpoint of another contact folder.</span></span>|
|[<span data-ttu-id="d1618-134">Crear propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="d1618-134">Create single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[<span data-ttu-id="d1618-135">contactFolder</span><span class="sxs-lookup"><span data-stu-id="d1618-135">contactFolder</span></span>](contactfolder.md)  |<span data-ttu-id="d1618-136">Cree una o varias propiedades extendidas de valor único en un objeto contactFolder nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="d1618-136">Create one or more single-value extended properties in a new or existing contactFolder.</span></span>   |
|[<span data-ttu-id="d1618-137">Obtener contactFolder con propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="d1618-137">Get contactFolder with single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="d1618-138">contactFolder</span><span class="sxs-lookup"><span data-stu-id="d1618-138">contactFolder</span></span>](contactfolder.md) | <span data-ttu-id="d1618-139">Obtenga objetos contactFolder que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="d1618-139">Get contactFolders that contain a single-value extended property by using `$expand` or `$filter`.</span></span> |
|[<span data-ttu-id="d1618-140">Crear propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="d1618-140">Create multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [<span data-ttu-id="d1618-141">contactFolder</span><span class="sxs-lookup"><span data-stu-id="d1618-141">contactFolder</span></span>](contactfolder.md) | <span data-ttu-id="d1618-142">Cree una o varias propiedades extendidas de varios valores en un objeto contactFolder nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="d1618-142">Create one or more multi-value extended properties in a new or existing contactFolder.</span></span>  |
|[<span data-ttu-id="d1618-143">Obtener contactFolder con propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="d1618-143">Get contactFolder with multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="d1618-144">contactFolder</span><span class="sxs-lookup"><span data-stu-id="d1618-144">contactFolder</span></span>](contactfolder.md) | <span data-ttu-id="d1618-145">Obtenga un objeto contactFolder que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="d1618-145">Get a contactFolder that contains a multi-value extended property by using `$expand`.</span></span> |

## <a name="properties"></a><span data-ttu-id="d1618-146">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1618-146">Properties</span></span>
| <span data-ttu-id="d1618-147">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d1618-147">Property</span></span>     | <span data-ttu-id="d1618-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1618-148">Type</span></span>   |<span data-ttu-id="d1618-149">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1618-149">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d1618-150">displayName</span><span class="sxs-lookup"><span data-stu-id="d1618-150">displayName</span></span>|<span data-ttu-id="d1618-151">String</span><span class="sxs-lookup"><span data-stu-id="d1618-151">String</span></span>|<span data-ttu-id="d1618-152">El nombre para mostrar de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1618-152">The folder's display name.</span></span>|
|<span data-ttu-id="d1618-153">id</span><span class="sxs-lookup"><span data-stu-id="d1618-153">id</span></span>|<span data-ttu-id="d1618-154">String</span><span class="sxs-lookup"><span data-stu-id="d1618-154">String</span></span>|<span data-ttu-id="d1618-p101">Identificador único de la carpeta de contactos. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d1618-p101">Unique identifier of the contact folder. Read-only.</span></span>|
|<span data-ttu-id="d1618-157">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="d1618-157">parentFolderId</span></span>|<span data-ttu-id="d1618-158">String</span><span class="sxs-lookup"><span data-stu-id="d1618-158">String</span></span>|<span data-ttu-id="d1618-159">El identificador de la carpeta principal de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d1618-159">The ID of the folder's parent folder.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d1618-160">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d1618-160">Relationships</span></span>
| <span data-ttu-id="d1618-161">Relación</span><span class="sxs-lookup"><span data-stu-id="d1618-161">Relationship</span></span> | <span data-ttu-id="d1618-162">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1618-162">Type</span></span>   |<span data-ttu-id="d1618-163">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1618-163">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d1618-164">childFolders</span><span class="sxs-lookup"><span data-stu-id="d1618-164">childFolders</span></span>|<span data-ttu-id="d1618-165">Colección [ContactFolder](contactfolder.md)</span><span class="sxs-lookup"><span data-stu-id="d1618-165">[ContactFolder](contactfolder.md) collection</span></span>|<span data-ttu-id="d1618-p102">La colección de carpetas secundarias de la carpeta. Propiedad Navigation. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="d1618-p102">The collection of child folders in the folder. Navigation property. Read-only. Nullable.</span></span>|
|<span data-ttu-id="d1618-170">contactos</span><span class="sxs-lookup"><span data-stu-id="d1618-170">contacts</span></span>|<span data-ttu-id="d1618-171">Colección [contact](contact.md)</span><span class="sxs-lookup"><span data-stu-id="d1618-171">[Contact](contact.md) collection</span></span>|<span data-ttu-id="d1618-p103">Los contactos de la carpeta. Propiedad Navigation. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="d1618-p103">The contacts in the folder. Navigation property. Read-only. Nullable.</span></span>|
|<span data-ttu-id="d1618-176">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="d1618-176">multiValueExtendedProperties</span></span>|<span data-ttu-id="d1618-177">Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="d1618-177">[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="d1618-p104">La colección de propiedades extendidas de varios valores definidas para el objeto contactFolder. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="d1618-p104">The collection of multi-value extended properties defined for the contactFolder. Read-only. Nullable.</span></span>|
|<span data-ttu-id="d1618-181">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="d1618-181">singleValueExtendedProperties</span></span>|<span data-ttu-id="d1618-182">Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="d1618-182">[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="d1618-p105">La colección de propiedades extendidas de valor único definidas para el objeto contactFolder. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="d1618-p105">The collection of single-value extended properties defined for the contactFolder. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d1618-186">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d1618-186">JSON representation</span></span>

<span data-ttu-id="d1618-187">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d1618-187">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "childFolders",
    "contacts",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.contactFolder",
  "@odata.annotations": [
    {
      "property": "childFolders",
      "capabilities": {
        "navigability": "single",
        "changeTracking": false,
        "searchable": false
      }
    },
    {
      "property": "contacts",
      "capabilities": {
        "changeTracking": true,
        "navigability": "single",
        "searchable": false
      }
    }
  ]
}-->

```json
{
  "displayName": "string",
  "id": "string (identifier)",
  "parentFolderId": "string"
}

```

## <a name="see-also"></a><span data-ttu-id="d1618-188">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d1618-188">See also</span></span>

- [<span data-ttu-id="d1618-189">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="d1618-189">Use delta query to track changes in Microsoft Graph data</span></span>](/graph/delta-query-overview)
- [<span data-ttu-id="d1618-190">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="d1618-190">Get incremental changes to messages in a folder</span></span>](/graph/delta-query-messages)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contactFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
