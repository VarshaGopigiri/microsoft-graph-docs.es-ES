# <a name="contactfolder-resource-type"></a><span data-ttu-id="155c0-101">Tipo de recurso contactFolder</span><span class="sxs-lookup"><span data-stu-id="155c0-101">contactFolder resource type</span></span>

<span data-ttu-id="155c0-102">Una carpeta que contiene contactos.</span><span class="sxs-lookup"><span data-stu-id="155c0-102">A folder that contains contacts.</span></span>

<span data-ttu-id="155c0-103">Este recurso es compatible con el uso de una [consulta delta](../../../concepts/delta_query_overview.md) para realizar un seguimiento de los aumentos incrementales, las eliminaciones y las actualizaciones proporcionando una función [delta](../api/contactfolder_delta.md).</span><span class="sxs-lookup"><span data-stu-id="155c0-103">This resource supports using [delta query](../../../concepts/delta_query_overview.md) to track incremental additions, deletions, and updates, by providing a [delta](../api/contactfolder_delta.md) function.</span></span>


## <a name="methods"></a><span data-ttu-id="155c0-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="155c0-104">Methods</span></span>

| <span data-ttu-id="155c0-105">Método</span><span class="sxs-lookup"><span data-stu-id="155c0-105">Method</span></span>       | <span data-ttu-id="155c0-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="155c0-106">Return Type</span></span>  |<span data-ttu-id="155c0-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="155c0-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="155c0-108">Obtener contactFolder</span><span class="sxs-lookup"><span data-stu-id="155c0-108">Get contactFolder</span></span>](../api/contactfolder_get.md) | [<span data-ttu-id="155c0-109">contactFolder</span><span class="sxs-lookup"><span data-stu-id="155c0-109">contactFolder</span></span>](contactfolder.md) |<span data-ttu-id="155c0-110">Obtenga una carpeta de contactos mediante el identificador de carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="155c0-110">Get a contact folder by using the contact folder ID.</span></span>|
|[<span data-ttu-id="155c0-111">Actualizar</span><span class="sxs-lookup"><span data-stu-id="155c0-111">Update</span></span>](../api/contactfolder_update.md) | [<span data-ttu-id="155c0-112">contactFolder</span><span class="sxs-lookup"><span data-stu-id="155c0-112">contactFolder</span></span>](contactfolder.md) |<span data-ttu-id="155c0-113">Actualice el objeto contactFolder.</span><span class="sxs-lookup"><span data-stu-id="155c0-113">Update contactFolder object.</span></span> |
|[<span data-ttu-id="155c0-114">Eliminar</span><span class="sxs-lookup"><span data-stu-id="155c0-114">Delete</span></span>](../api/contactfolder_delete.md) | <span data-ttu-id="155c0-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="155c0-115">None</span></span> |<span data-ttu-id="155c0-116">Elimine el objeto contactFolder.</span><span class="sxs-lookup"><span data-stu-id="155c0-116">Delete contactFolder object.</span></span> |
|[<span data-ttu-id="155c0-117">Enumerar childFolders</span><span class="sxs-lookup"><span data-stu-id="155c0-117">List childFolders</span></span>](../api/contactfolder_list_childfolders.md) |<span data-ttu-id="155c0-118">Colección [ContactFolder](contactfolder.md)</span><span class="sxs-lookup"><span data-stu-id="155c0-118">[ContactFolder](contactfolder.md) collection</span></span>| <span data-ttu-id="155c0-119">Obtenga una colección de carpetas secundarias en la carpeta de contactos especificada.</span><span class="sxs-lookup"><span data-stu-id="155c0-119">Get a collection of child folders under the specified contact folder.</span></span>|
|[<span data-ttu-id="155c0-120">Crear contactFolder secundario</span><span class="sxs-lookup"><span data-stu-id="155c0-120">Create child contactFolder</span></span>](../api/contactfolder_post_childfolders.md) |[<span data-ttu-id="155c0-121">ContactFolder</span><span class="sxs-lookup"><span data-stu-id="155c0-121">ContactFolder</span></span>](contactfolder.md)| <span data-ttu-id="155c0-122">Cree una contactFolder como elemento secundario de una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="155c0-122">Create a new contactFolder as a child of a specified folder.</span></span>|
|[<span data-ttu-id="155c0-123">delta</span><span class="sxs-lookup"><span data-stu-id="155c0-123">delta</span></span>](../api/contact_delta.md)|<span data-ttu-id="155c0-124">Colección [contact](contact.md)</span><span class="sxs-lookup"><span data-stu-id="155c0-124">[contact](contact.md) collection</span></span>| <span data-ttu-id="155c0-125">Obtenga un conjunto de carpetas de contactos que se hayan agregado, eliminado o quitado del buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="155c0-125">Get a set of contact folders that have been added, deleted, or removed from the user's mailbox.</span></span>|
|[<span data-ttu-id="155c0-126">Enumerar contactos en la carpeta</span><span class="sxs-lookup"><span data-stu-id="155c0-126">List contacts in folder</span></span>](../api/contactfolder_list_contacts.md) |<span data-ttu-id="155c0-127">Colección [contact](contact.md)</span><span class="sxs-lookup"><span data-stu-id="155c0-127">[Contact](contact.md) collection</span></span>| <span data-ttu-id="155c0-128">Obtenga una colección de contactos de la carpeta de contactos predeterminada del usuario que ha iniciado sesión (`.../me/contacts`) o de la carpeta de contactos especificada.</span><span class="sxs-lookup"><span data-stu-id="155c0-128">Get a contact collection from the default Contacts folder of the signed-in user (`.../me/contacts`), or from the specified contact folder.</span></span>|
|[<span data-ttu-id="155c0-129">Crear contacto en la carpeta</span><span class="sxs-lookup"><span data-stu-id="155c0-129">Create contact in folder</span></span>](../api/contactfolder_post_contacts.md) |[<span data-ttu-id="155c0-130">Contact</span><span class="sxs-lookup"><span data-stu-id="155c0-130">Contact</span></span>](contact.md)| <span data-ttu-id="155c0-131">Agregue un contacto a la carpeta de contactos raíz o al extremo de `contacts` de otra carpeta de contactos.</span><span class="sxs-lookup"><span data-stu-id="155c0-131">Add a contact to the root Contacts folder or to the `contacts` endpoint of another contact folder.</span></span>|
|[<span data-ttu-id="155c0-132">Crear propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="155c0-132">Create single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) |[<span data-ttu-id="155c0-133">contactFolder</span><span class="sxs-lookup"><span data-stu-id="155c0-133">contactFolder</span></span>](contactFolder.md)  |<span data-ttu-id="155c0-134">Cree una o varias propiedades extendidas de valor único en un objeto contactFolder nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="155c0-134">Create one or more single-value extended properties in a new or existing contactFolder.</span></span>   |
|[<span data-ttu-id="155c0-135">Obtener contactFolder con propiedad extendida de valor único</span><span class="sxs-lookup"><span data-stu-id="155c0-135">Get contactFolder with single-value extended property</span></span>](../api/singlevaluelegacyextendedproperty_get.md)  | [<span data-ttu-id="155c0-136">contactFolder</span><span class="sxs-lookup"><span data-stu-id="155c0-136">contactFolder</span></span>](contactFolder.md) | <span data-ttu-id="155c0-137">Obtenga objetos contactFolder que contienen una propiedad extendida de valor único mediante el uso de `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="155c0-137">Get contactFolders that contain a single-value extended property by using `$expand` or `$filter`.</span></span> |
|[<span data-ttu-id="155c0-138">Crear propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="155c0-138">Create multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | [<span data-ttu-id="155c0-139">contactFolder</span><span class="sxs-lookup"><span data-stu-id="155c0-139">contactFolder</span></span>](contactFolder.md) | <span data-ttu-id="155c0-140">Cree una o varias propiedades extendidas de varios valores en un objeto contactFolder nuevo o existente.</span><span class="sxs-lookup"><span data-stu-id="155c0-140">Create one or more multi-value extended properties in a new or existing contactFolder.</span></span>  |
|[<span data-ttu-id="155c0-141">Obtener contactFolder con propiedad extendida de varios valores</span><span class="sxs-lookup"><span data-stu-id="155c0-141">Get contactFolder with multi-value extended property</span></span>](../api/multivaluelegacyextendedproperty_get.md)  | [<span data-ttu-id="155c0-142">contactFolder</span><span class="sxs-lookup"><span data-stu-id="155c0-142">contactFolder</span></span>](contactFolder.md) | <span data-ttu-id="155c0-143">Obtenga un objeto contactFolder que contiene una propiedad extendida de varios valores mediante el uso de `$expand`.</span><span class="sxs-lookup"><span data-stu-id="155c0-143">Get a contactFolder that contains a multi-value extended property by using `$expand`.</span></span> |

## <a name="properties"></a><span data-ttu-id="155c0-144">Propiedades</span><span class="sxs-lookup"><span data-stu-id="155c0-144">Properties</span></span>
| <span data-ttu-id="155c0-145">Propiedad</span><span class="sxs-lookup"><span data-stu-id="155c0-145">Property</span></span>     | <span data-ttu-id="155c0-146">Tipo</span><span class="sxs-lookup"><span data-stu-id="155c0-146">Type</span></span>   |<span data-ttu-id="155c0-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="155c0-147">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="155c0-148">displayName</span><span class="sxs-lookup"><span data-stu-id="155c0-148">displayName</span></span>|<span data-ttu-id="155c0-149">String</span><span class="sxs-lookup"><span data-stu-id="155c0-149">String</span></span>|<span data-ttu-id="155c0-150">El nombre para mostrar de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="155c0-150">The folder's display name.</span></span>|
|<span data-ttu-id="155c0-151">id</span><span class="sxs-lookup"><span data-stu-id="155c0-151">id</span></span>|<span data-ttu-id="155c0-152">String</span><span class="sxs-lookup"><span data-stu-id="155c0-152">String</span></span>|<span data-ttu-id="155c0-p101">Identificador único de la carpeta de contactos. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="155c0-p101">Unique identifier of the contact folder. Read-only.</span></span>|
|<span data-ttu-id="155c0-155">parentFolderId</span><span class="sxs-lookup"><span data-stu-id="155c0-155">parentFolderId</span></span>|<span data-ttu-id="155c0-156">String</span><span class="sxs-lookup"><span data-stu-id="155c0-156">String</span></span>|<span data-ttu-id="155c0-157">El identificador de la carpeta principal de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="155c0-157">The ID of the folder's parent folder.</span></span>|

## <a name="relationships"></a><span data-ttu-id="155c0-158">Relaciones</span><span class="sxs-lookup"><span data-stu-id="155c0-158">Relationships</span></span>
| <span data-ttu-id="155c0-159">Relación</span><span class="sxs-lookup"><span data-stu-id="155c0-159">Relationship</span></span> | <span data-ttu-id="155c0-160">Tipo</span><span class="sxs-lookup"><span data-stu-id="155c0-160">Type</span></span>   |<span data-ttu-id="155c0-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="155c0-161">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="155c0-162">childFolders</span><span class="sxs-lookup"><span data-stu-id="155c0-162">childFolders</span></span>|<span data-ttu-id="155c0-163">Colección [ContactFolder](contactfolder.md)</span><span class="sxs-lookup"><span data-stu-id="155c0-163">[ContactFolder](contactfolder.md) collection</span></span>|<span data-ttu-id="155c0-p102">La colección de carpetas secundarias de la carpeta. Propiedad Navigation. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="155c0-p102">The collection of child folders in the folder. Navigation property. Read-only. Nullable.</span></span>|
|<span data-ttu-id="155c0-168">contactos</span><span class="sxs-lookup"><span data-stu-id="155c0-168">contacts</span></span>|<span data-ttu-id="155c0-169">Colección [contact](contact.md)</span><span class="sxs-lookup"><span data-stu-id="155c0-169">[Contact](contact.md) collection</span></span>|<span data-ttu-id="155c0-p103">Los contactos de la carpeta. Propiedad Navigation. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="155c0-p103">The contacts in the folder. Navigation property. Read-only. Nullable.</span></span>|
|<span data-ttu-id="155c0-174">multiValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="155c0-174">multiValueExtendedProperties</span></span>|<span data-ttu-id="155c0-175">Colección [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="155c0-175">[multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="155c0-p104">La colección de propiedades extendidas de varios valores definidas para el objeto contactFolder. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="155c0-p104">The collection of multi-value extended properties defined for the contactFolder. Read-only. Nullable.</span></span>|
|<span data-ttu-id="155c0-179">singleValueExtendedProperties</span><span class="sxs-lookup"><span data-stu-id="155c0-179">singleValueExtendedProperties</span></span>|<span data-ttu-id="155c0-180">Colección [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md)</span><span class="sxs-lookup"><span data-stu-id="155c0-180">[singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) collection</span></span>| <span data-ttu-id="155c0-p105">La colección de propiedades extendidas de valor único definidas para el objeto contactFolder. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="155c0-p105">The collection of single-value extended properties defined for the contactFolder. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="155c0-184">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="155c0-184">JSON representation</span></span>

<span data-ttu-id="155c0-185">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="155c0-185">Here is a JSON representation of the resource</span></span>

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

## <a name="see-also"></a><span data-ttu-id="155c0-186">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="155c0-186">See also</span></span>

- [<span data-ttu-id="155c0-187">Usar la consulta delta para realizar el seguimiento de los cambios en datos de Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="155c0-187">Use delta query to track changes in Microsoft Graph data</span></span>](../../../concepts/delta_query_overview.md)
- [<span data-ttu-id="155c0-188">Obtener los cambios incrementales en los mensajes de una carpeta</span><span class="sxs-lookup"><span data-stu-id="155c0-188">Get incremental changes to messages in a folder</span></span>](../../../concepts/delta_query_messages.md)


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "contactFolder resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
