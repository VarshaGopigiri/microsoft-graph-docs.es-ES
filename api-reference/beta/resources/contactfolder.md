---
title: Tipo de recurso contactFolder
description: Una carpeta que contiene contactos.
ms.openlocfilehash: 3e9916d70a23c8acd4b1da2ee8f7e2df4c408e41
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087498"
---
# <a name="contactfolder-resource-type"></a><span data-ttu-id="194d1-103">Tipo de recurso contactFolder</span><span class="sxs-lookup"><span data-stu-id="194d1-103">contactFolder resource type</span></span>

> <span data-ttu-id="194d1-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="194d1-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="194d1-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="194d1-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="194d1-106">Una carpeta que contiene contactos.</span><span class="sxs-lookup"><span data-stu-id="194d1-106">A folder that contains contacts.</span></span>

<span data-ttu-id="194d1-107">Este recurso es compatible con el uso de una [consulta delta](/graph/delta-query-overview) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/contactfolder-delta.md).</span><span class="sxs-lookup"><span data-stu-id="194d1-107">This resource supports using [delta query](/graph/delta-query-overview) to track incremental additions, deletions, and updates, by providing a [delta](../api/contactfolder-delta.md) function.</span></span>


## <a name="methods"></a><span data-ttu-id="194d1-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="194d1-108">Methods</span></span>

| <span data-ttu-id="194d1-109">Método</span><span class="sxs-lookup"><span data-stu-id="194d1-109">Method</span></span>       | <span data-ttu-id="194d1-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="194d1-110">Return Type</span></span>  |<span data-ttu-id="194d1-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="194d1-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="194d1-112">Obtener contactFolder</span><span class="sxs-lookup"><span data-stu-id="194d1-112">Get contactFolder</span></span>](../api/contactfolder-get.md) | [<span data-ttu-id="194d1-113">contactFolder</span><span class="sxs-lookup"><span data-stu-id="194d1-113">contactFolder</span></span>](contactfolder.md) |<span data-ttu-id="194d1-114">Obtenga una carpeta de contactos mediante el identificador de carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="194d1-114">Get a contact folder by using the contact folder ID.</span></span>|
|[<span data-ttu-id="194d1-115">Actualizar</span><span class="sxs-lookup"><span data-stu-id="194d1-115">Update</span></span>](../api/contactfolder-update.md) | [<span data-ttu-id="194d1-116">contactFolder</span><span class="sxs-lookup"><span data-stu-id="194d1-116">contactFolder</span></span>](contactfolder.md) |<span data-ttu-id="194d1-117">Actualice el objeto contactFolder.</span><span class="sxs-lookup"><span data-stu-id="194d1-117">Update contactFolder object.</span></span> |
|[<span data-ttu-id="194d1-118">Eliminar</span><span class="sxs-lookup"><span data-stu-id="194d1-118">Delete</span></span>](../api/contactfolder-delete.md) | <span data-ttu-id="194d1-119">Ninguno</span><span class="sxs-lookup"><span data-stu-id="194d1-119">None</span></span> |<span data-ttu-id="194d1-120">Elimine el objeto contactFolder.</span><span class="sxs-lookup"><span data-stu-id="194d1-120">Delete contactFolder object.</span></span> |
|[<span data-ttu-id="194d1-121">Enumerar childFolders</span><span class="sxs-lookup"><span data-stu-id="194d1-121">List childFolders</span></span>](../api/contactfolder-list-childfolders.md) |<span data-ttu-id="194d1-122">colección de [contactFolder](contactfolder.md)</span><span class="sxs-lookup"><span data-stu-id="194d1-122">[contactFolder](contactfolder.md) collection</span></span>| <span data-ttu-id="194d1-123">Obtenga una colección de carpetas secundarias en la carpeta de contactos especificada.</span><span class="sxs-lookup"><span data-stu-id="194d1-123">Get a collection of child folders under the specified contact folder.</span></span>|
|[<span data-ttu-id="194d1-124">Crear contactFolder secundario</span><span class="sxs-lookup"><span data-stu-id="194d1-124">Create child contactFolder</span></span>](../api/contactfolder-post-childfolders.md) |[<span data-ttu-id="194d1-125">contactFolder</span><span class="sxs-lookup"><span data-stu-id="194d1-125">contactFolder</span></span>](contactfolder.md)| <span data-ttu-id="194d1-126">Cree una contactFolder como elemento secundario de una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="194d1-126">Create a new contactFolder as a child of a specified folder.</span></span>|
|[<span data-ttu-id="194d1-127">delta</span><span class="sxs-lookup"><span data-stu-id="194d1-127">delta</span></span>](../api/contact-delta.md)|<span data-ttu-id="194d1-128">Colección [contact](contact.md)</span><span class="sxs-lookup"><span data-stu-id="194d1-128">[contact](contact.md) collection</span></span>| <span data-ttu-id="194d1-129">Obtenga un conjunto de carpetas de contactos que se hayan agregado, eliminado o quitado del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="194d1-129">Get a set of contact folders that have been added, deleted, or removed from the user's mailbox.</span></span>|
|[<span data-ttu-id="194d1-130">Enumerar contactos en la carpeta</span><span class="sxs-lookup"><span data-stu-id="194d1-130">List contacts in folder</span></span>](../api/contactfolder-list-contacts.md) |<span data-ttu-id="194d1-131">Colección [contact](contact.md)</span><span class="sxs-lookup"><span data-stu-id="194d1-131">[contact](contact.md) collection</span></span>| <span data-ttu-id="194d1-132">Obtenga una colección de contactos de la carpeta de contactos predeterminada del usuario que ha iniciado sesión (`.../me/contacts`) o de la carpeta de contactos especificada.</span><span class="sxs-lookup"><span data-stu-id="194d1-132">Get a contact collection from the default Contacts folder of the signed-in user (`.../me/contacts`), or from the specified contact folder.</span></span>|
|[<span data-ttu-id="194d1-133">Crear contacto en la carpeta</span><span class="sxs-lookup"><span data-stu-id="194d1-133">Create contact in folder</span></span>](../api/contactfolder-post-contacts.md) |[<span data-ttu-id="194d1-134">contact</span><span class="sxs-lookup"><span data-stu-id="194d1-134">contact</span></span>](contact.md)| <span data-ttu-id="194d1-135">Agregue un contacto a la carpeta de contactos raíz o al punto de conexión de `contacts` de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="194d1-135">Add a contact to the root Contacts folder or to the `contacts` endpoint of another contact folder.</span></span>|
|<span data-ttu-id="194d1-136">**Propiedades extendidas**</span><span class="sxs-lookup"><span data-stu-id="194d1-136">**Extended properties**</span></span>| | |
|[<span data-ttu-id="194d1-137">Crear propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="194d1-137">Create single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-post-singlevalueextendedproperties.md) |[<span data-ttu-id="194d1-138">contactFolder</span><span class="sxs-lookup"><span data-stu-id="194d1-138">contactFolder</span></span>](contactfolder.md)  |<span data-ttu-id="194d1-139">Cree una o varias propiedades extendidas de valor único en un objeto contactFolder nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="194d1-139">Create one or more single-value extended properties in a new or existing contactFolder.</span></span>   |
|[<span data-ttu-id="194d1-140">Obtener contactFolder con propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="194d1-140">Get contactFolder with single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="194d1-141">contactFolder</span><span class="sxs-lookup"><span data-stu-id="194d1-141">contactFolder</span></span>](contactfolder.md) | <span data-ttu-id="194d1-142">Obtenga objetos contactFolder que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="194d1-142">Get contactFolders that contain a single-value extended property by using `$expand` or `$filter`.</span></span> |
|[<span data-ttu-id="194d1-143">Crear propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="194d1-143">Create multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-post-multivalueextendedproperties.md) | [<span data-ttu-id="194d1-144">contactFolder</span><span class="sxs-lookup"><span data-stu-id="194d1-144">contactFolder</span></span>](contactfolder.md) | <span data-ttu-id="194d1-145">Cree una o varias propiedades extendidas de varios valores en un objeto contactFolder nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="194d1-145">Create one or more multi-value extended properties in a new or existing contactFolder.</span></span>  |
|[<span data-ttu-id="194d1-146">Obtener contactFolder con propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="194d1-146">Get contactFolder with multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty-get.md)  | [<span data-ttu-id="194d1-147">contactFolder</span><span class="sxs-lookup"><span data-stu-id="194d1-147">contactFolder</span></span>](contactfolder.md) | <span data-ttu-id="194d1-148">Obtenga un objeto contactFolder que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="194d1-148">Get a contactFolder that contains a multi-value extended property by using `$expand`.</span></span> |

## <a name="properties"></a><span data-ttu-id="194d1-149">Propiedades</span><span class="sxs-lookup"><span data-stu-id="194d1-149">Properties</span></span>
| <span data-ttu-id="194d1-150">Propiedad</span><span class="sxs-lookup"><span data-stu-id="194d1-150">Property</span></span>     | <span data-ttu-id="194d1-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="194d1-151">Type</span></span>   |<span data-ttu-id="194d1-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="194d1-152">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="194d1-153">displayName</span><span class="sxs-lookup"><span data-stu-id="194d1-153">displayName</span></span>|<span data-ttu-id="194d1-154">String</span><span class="sxs-lookup"><span data-stu-id="194d1-154">String</span></span>|<span data-ttu-id="194d1-155">El nombre para mostrar de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="194d1-155">The folder's display name.</span></span>|
|<span data-ttu-id="194d1-156">id</span><span class="sxs-lookup"><span data-stu-id="194d1-156">id</span></span>|<span data-ttu-id="194d1-157">String</span><span class="sxs-lookup"><span data-stu-id="194d1-157">String</span></span>|<span data-ttu-id="194d1-p102">Identificador único de la carpeta de contactos. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="194d1-p102">Unique identifier of the contact folder. Read-only.</span></span>|
|<span data-ttu-id="194d1-160">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="194d1-160">parentFolderId</span></span>|<span data-ttu-id="194d1-161">String</span><span class="sxs-lookup"><span data-stu-id="194d1-161">String</span></span>|<span data-ttu-id="194d1-162">El identificador de la carpeta principal de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="194d1-162">The ID of the folder's parent folder.</span></span>|
|<span data-ttu-id="194d1-163">wellKnownName</span><span class="sxs-lookup"><span data-stu-id="194d1-163">wellKnownName</span></span>|<span data-ttu-id="194d1-164">string</span><span class="sxs-lookup"><span data-stu-id="194d1-164">string</span></span>|<span data-ttu-id="194d1-165">El nombre de la carpeta si la carpeta es una carpeta reconocida.</span><span class="sxs-lookup"><span data-stu-id="194d1-165">The name of the folder if the folder is a recognized folder.</span></span> <span data-ttu-id="194d1-166">Actualmente `contacts` es la única carpeta Contactos reconocida.</span><span class="sxs-lookup"><span data-stu-id="194d1-166">Currently `contacts` is the only recognized contacts folder.</span></span>|

## <a name="relationships"></a><span data-ttu-id="194d1-167">Relaciones</span><span class="sxs-lookup"><span data-stu-id="194d1-167">Relationships</span></span>
| <span data-ttu-id="194d1-168">Relación</span><span class="sxs-lookup"><span data-stu-id="194d1-168">Relationship</span></span> | <span data-ttu-id="194d1-169">Tipo</span><span class="sxs-lookup"><span data-stu-id="194d1-169">Type</span></span>   |<span data-ttu-id="194d1-170">Descripción</span><span class="sxs-lookup"><span data-stu-id="194d1-170">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="194d1-171">childFolders</span><span class="sxs-lookup"><span data-stu-id="194d1-171">childFolders</span></span>|<span data-ttu-id="194d1-172">Colección [ContactFolder](contactfolder.md)</span><span class="sxs-lookup"><span data-stu-id="194d1-172">[ContactFolder](contactfolder.md) collection</span></span>|<span data-ttu-id="194d1-p104">La colección de carpetas secundarias de la carpeta. Propiedad Navigation. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="194d1-p104">The collection of child folders in the folder. Navigation property. Read-only. Nullable.</span></span>|
|<span data-ttu-id="194d1-177">contactos</span><span class="sxs-lookup"><span data-stu-id="194d1-177">contacts</span></span>|<span data-ttu-id="194d1-178">Colección [contact](contact.md)</span><span class="sxs-lookup"><span data-stu-id="194d1-178">[Contact](contact.md) collection</span></span>|<span data-ttu-id="194d1-p105">Los contactos de la carpeta. Propiedad Navigation. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="194d1-p105">The contacts in the folder. Navigation property. Read-only. Nullable.</span></span>|
|<span data-ttu-id="194d1-183">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="194d1-183">multiValueExtendedProperties</span></span>|<span data-ttu-id="194d1-184">Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="194d1-184">[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="194d1-p106">La colección de propiedades extendidas de varios valores definidas para el objeto contactFolder. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="194d1-p106">The collection of multi-value extended properties defined for the contactFolder. Read-only. Nullable.</span></span>|
|<span data-ttu-id="194d1-188">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="194d1-188">singleValueExtendedProperties</span></span>|<span data-ttu-id="194d1-189">Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="194d1-189">[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="194d1-p107">La colección de propiedades extendidas de valor único definidas para el objeto contactFolder. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="194d1-p107">The collection of single-value extended properties defined for the contactFolder. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="194d1-193">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="194d1-193">JSON representation</span></span>

<span data-ttu-id="194d1-194">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="194d1-194">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "childFolders",
    "contacts",
    "multiValueExtendedProperties",
    "singleValueExtendedProperties"
  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.contactFolder"
}-->

```json
{
  "displayName": "string",
  "id": "string (identifier)",
  "parentFolderId": "string",
  "wellKnownName": "string"
}

```

## <a name="see-also"></a><span data-ttu-id="194d1-195">Consulte también</span><span class="sxs-lookup"><span data-stu-id="194d1-195">See also</span></span>

- [<span data-ttu-id="194d1-196">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="194d1-196">Use delta query to track changes in Microsoft Graph data</span></span>](/graph/delta-query-overview)
- [<span data-ttu-id="194d1-197">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="194d1-197">Get incremental changes to messages in a folder</span></span>](/graph/delta-query-messages)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contactFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
