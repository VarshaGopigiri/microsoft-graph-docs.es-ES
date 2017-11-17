---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Unidad de disco
ms.openlocfilehash: 0b178967f7eb8da8bdf8584bb13a7d4f9950392b
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="drive-resource-type"></a><span data-ttu-id="d9519-102">Tipo de recurso Drive</span><span class="sxs-lookup"><span data-stu-id="d9519-102">Drive resource type</span></span>

<span data-ttu-id="d9519-103">El recurso de unidad es el objeto de nivel superior que representa el OneDrive de un usuario o una biblioteca de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d9519-103">The drive resource is the top level object representing a user's OneDrive or a document library in SharePoint.</span></span>

<span data-ttu-id="d9519-p101">Los usuarios de OneDrive siempre tendrán al menos una unidad disponible, la unidad predeterminada. Es posible que los usuarios sin licencia de OneDrive no tengan una unidad predeterminada disponible.</span><span class="sxs-lookup"><span data-stu-id="d9519-p101">OneDrive users will always have at least one drive available, their default drive. Users without a OneDrive license may not have a default drive available.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d9519-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d9519-106">JSON representation</span></span>

<span data-ttu-id="d9519-107">A continuación se muestra una representación JSON de un recurso Drive.</span><span class="sxs-lookup"><span data-stu-id="d9519-107">Here is a JSON representation of a Drive resource.</span></span>

<span data-ttu-id="d9519-108">El recurso **drive** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="d9519-108">The **drive** resource is derived from [**baseItem**](baseitem.md) and inherits properties from that resource.</span></span>

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.drive",
       "keyProperty": "id", 
       "optionalProperties": [ "activities", "createdBy", "createdDateTime", "description", "lastModifiedBy", "lastModifiedDateTime", "name", "webUrl", "items", "root", "special", "system"] } -->

```json
{
  "id": "string",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "string (timestamp)",
  "description": "string",
  "driveType": "personal | business | documentLibrary",
  "items": [ { "@odata.type": "microsoft.graph.driveItem" } ],
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "string (timestamp)",
  "name": "string",
  "owner": { "@odata.type": "microsoft.graph.identitySet" },
  "quota": { "@odata.type": "microsoft.graph.quota" },
  "root": { "@odata.type": "microsoft.graph.driveItem" },
  "special": [ { "@odata.type": "microsoft.graph.driveItem" }],
  "system": { "@odata.type": "microsoft.graph.systemFacet" },
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="d9519-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9519-109">Properties</span></span>

| <span data-ttu-id="d9519-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9519-110">Property</span></span>             | <span data-ttu-id="d9519-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9519-111">Type</span></span>                          | <span data-ttu-id="d9519-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9519-112">Description</span></span>                                                                                                                                                                                                                      |
| :------------------- | :---------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="d9519-113">createdBy</span><span class="sxs-lookup"><span data-stu-id="d9519-113">createdBy</span></span>            | <span data-ttu-id="d9519-114">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="d9519-114">[identitySet][]</span></span>               | <span data-ttu-id="d9519-p102">Identidad del usuario, del dispositivo o de la aplicación que ha creado el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p102">Identity of the user, device, or application which created the item. Read-only.</span></span>                                                                                                                                                  |
| <span data-ttu-id="d9519-117">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d9519-117">createdDateTime</span></span>      | <span data-ttu-id="d9519-118">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d9519-118">dateTimeOffset</span></span>                | <span data-ttu-id="d9519-p103">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p103">Date and time of item creation. Read-only.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="d9519-121">description</span><span class="sxs-lookup"><span data-stu-id="d9519-121">description</span></span>          | <span data-ttu-id="d9519-122">String</span><span class="sxs-lookup"><span data-stu-id="d9519-122">String</span></span>                        | <span data-ttu-id="d9519-123">Proporciona una descripción de la unidad visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="d9519-123">Provide a user-visible description of the drive.</span></span> <span data-ttu-id="d9519-124">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d9519-124">Read-write.</span></span>
| <span data-ttu-id="d9519-125">driveType</span><span class="sxs-lookup"><span data-stu-id="d9519-125">driveType</span></span>            | <span data-ttu-id="d9519-126">String</span><span class="sxs-lookup"><span data-stu-id="d9519-126">String</span></span>                        | <span data-ttu-id="d9519-p105">Describe el tipo de unidad que representa este recurso. Las unidades personales de OneDrive devolverán `personal`. OneDrive para la Empresa devolverá `business`. Las bibliotecas de documentos de SharePoint devolverán `documentLibrary`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p105">Describes the type of drive represented by this resource. OneDrive personal drives will return `personal`. OneDrive for Business will return `business`. SharePoint document libraries will return `documentLibrary`. Read-only.</span></span> |
| <span data-ttu-id="d9519-132">id</span><span class="sxs-lookup"><span data-stu-id="d9519-132">id</span></span>                   | <span data-ttu-id="d9519-133">String</span><span class="sxs-lookup"><span data-stu-id="d9519-133">String</span></span>                        | <span data-ttu-id="d9519-p106">El identificador único de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p106">The unique identifier of the drive. Read-only.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="d9519-136">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="d9519-136">lastModifiedBy</span></span>       | <span data-ttu-id="d9519-137">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="d9519-137">[identitySet][]</span></span>               | <span data-ttu-id="d9519-p107">Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p107">Identity of the user, device, and application which last modified the item. Read-only.</span></span>                                                                                                                                           |
| <span data-ttu-id="d9519-140">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d9519-140">lastModifiedDateTime</span></span> | <span data-ttu-id="d9519-141">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d9519-141">dateTimeOffset</span></span>                | <span data-ttu-id="d9519-p108">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p108">Date and time the item was last modified. Read-only.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="d9519-144">name</span><span class="sxs-lookup"><span data-stu-id="d9519-144">name</span></span>                 | <span data-ttu-id="d9519-145">string</span><span class="sxs-lookup"><span data-stu-id="d9519-145">string</span></span>                        | <span data-ttu-id="d9519-p109">Nombre del elemento. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p109">The name of the item. Read-write.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="d9519-148">owner</span><span class="sxs-lookup"><span data-stu-id="d9519-148">owner</span></span>                | [<span data-ttu-id="d9519-149">identitySet</span><span class="sxs-lookup"><span data-stu-id="d9519-149">identitySet</span></span>](identityset.md) | <span data-ttu-id="d9519-p110">Opcional. La cuenta de usuario propietaria de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p110">Optional. The user account that owns the drive. Read-only.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="d9519-153">quota</span><span class="sxs-lookup"><span data-stu-id="d9519-153">quota</span></span>                | [<span data-ttu-id="d9519-154">quota</span><span class="sxs-lookup"><span data-stu-id="d9519-154">quota</span></span>](quota.md)             | <span data-ttu-id="d9519-p111">Opcional. Información sobre la cuota de espacio de almacenamiento de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p111">Optional. Information about the drive's storage space quota. Read-only.</span></span>                                                                                                                                                          |
| <span data-ttu-id="d9519-158">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="d9519-158">sharepointIds</span></span>        | <span data-ttu-id="d9519-159">[sharepointIds][]</span><span class="sxs-lookup"><span data-stu-id="d9519-159">[sharepointIds][]</span></span>             | <span data-ttu-id="d9519-p112">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p112">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>                                                                                                                                                         |
| <span data-ttu-id="d9519-162">sistema</span><span class="sxs-lookup"><span data-stu-id="d9519-162">System</span></span>               | <span data-ttu-id="d9519-163">[systemFacet][]</span><span class="sxs-lookup"><span data-stu-id="d9519-163">[systemFacet][]</span></span>               | <span data-ttu-id="d9519-164">Si está presente, indica que se trata de una unidad administrada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="d9519-164">If present, indicates that this is a system-managed drive.</span></span> <span data-ttu-id="d9519-165">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-165">Read-only.</span></span>
| <span data-ttu-id="d9519-166">webUrl</span><span class="sxs-lookup"><span data-stu-id="d9519-166">webUrl</span></span>               | <span data-ttu-id="d9519-167">string (url)</span><span class="sxs-lookup"><span data-stu-id="d9519-167">string (url)</span></span>                  | <span data-ttu-id="d9519-p114">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p114">URL that displays the resource in the browser. Read-only.</span></span>                                                                                                                                                                        |

[identitySet]: identityset.md
[sharepointIds]: sharepointids.md
[systemFacet]: systemfacet.md

## <a name="relationships"></a><span data-ttu-id="d9519-173">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d9519-173">Relationships</span></span>

| <span data-ttu-id="d9519-174">Relación</span><span class="sxs-lookup"><span data-stu-id="d9519-174">Relationship</span></span> | <span data-ttu-id="d9519-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9519-175">Type</span></span>                                 | <span data-ttu-id="d9519-176">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9519-176">Description</span></span>
|:-------------|:-------------------------------------|:-----------------------
| <span data-ttu-id="d9519-177">items</span><span class="sxs-lookup"><span data-stu-id="d9519-177">items</span></span>        | <span data-ttu-id="d9519-178">Colección [driveitem](driveitem.md)</span><span class="sxs-lookup"><span data-stu-id="d9519-178">[driveitem](driveitem.md) collection</span></span> | <span data-ttu-id="d9519-p115">Todos los elementos contenidos en la unidad. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="d9519-p115">All items contained in the drive. Read-only. Nullable.</span></span>
| <span data-ttu-id="d9519-182">root</span><span class="sxs-lookup"><span data-stu-id="d9519-182">root</span></span>         | [<span data-ttu-id="d9519-183">driveitem</span><span class="sxs-lookup"><span data-stu-id="d9519-183">driveitem</span></span>](driveitem.md)            | <span data-ttu-id="d9519-p116">La carpeta raíz de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9519-p116">The root folder of the drive. Read-only.</span></span>
| <span data-ttu-id="d9519-186">special</span><span class="sxs-lookup"><span data-stu-id="d9519-186">special</span></span>      | <span data-ttu-id="d9519-187">Colección [driveitem](driveitem.md)</span><span class="sxs-lookup"><span data-stu-id="d9519-187">[driveitem](driveitem.md) collection</span></span> | <span data-ttu-id="d9519-p117">Colección de carpetas comunes disponibles en OneDrive. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="d9519-p117">Collection of common folders available in OneDrive. Read-only. Nullable.</span></span>

## <a name="methods"></a><span data-ttu-id="d9519-191">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9519-191">Methods</span></span>

|                        <span data-ttu-id="d9519-192">Tarea común</span><span class="sxs-lookup"><span data-stu-id="d9519-192">Common task</span></span>                         |         <span data-ttu-id="d9519-193">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="d9519-193">HTTP method</span></span>         |
| :--------------------------------------------------------- | :-------------------------- |
| <span data-ttu-id="d9519-194">[Obtener los metadatos de la unidad de otra unidad][drive-get]</span><span class="sxs-lookup"><span data-stu-id="d9519-194">[Get Drive metadata of another Drive][drive-get]</span></span>           | `GET /drives/{drive-id}`    |
| <span data-ttu-id="d9519-195">[Obtener la carpeta raíz de la unidad predeterminada del usuario][item-get]</span><span class="sxs-lookup"><span data-stu-id="d9519-195">[Get root folder for user's default Drive][item-get]</span></span>       | `GET /drive/root`           |
| <span data-ttu-id="d9519-196">[Mostrar los elementos secundarios en la unidad][item-children]</span><span class="sxs-lookup"><span data-stu-id="d9519-196">[List children under the Drive][item-children]</span></span>             | `GET /drive/root/children`  |
| <span data-ttu-id="d9519-197">[Mostrar los cambios para todos los elementos de la unidad][item-changes]</span><span class="sxs-lookup"><span data-stu-id="d9519-197">[List changes for all Items in the Drive][item-changes]</span></span>    | `GET /drive/root/delta`     |
| <span data-ttu-id="d9519-198">[Buscar los elementos en la unidad][item-search]</span><span class="sxs-lookup"><span data-stu-id="d9519-198">[Search for Items in the Drive][item-search]</span></span>               | `GET /drive/root/search`    |
| [<span data-ttu-id="d9519-199">Acceso a la carpeta especial</span><span class="sxs-lookup"><span data-stu-id="d9519-199">Access special folder</span></span>](../api/drive_get_specialfolder.md) | `GET /drive/special/{name}` |

<span data-ttu-id="d9519-200">En la tabla anterior, los ejemplos usan `/drive` pero también son válidas otras rutas.</span><span class="sxs-lookup"><span data-stu-id="d9519-200">In the previous table, the examples use , but  is valid too.</span></span>

[item-resource]: driveitem.md
[identity-set]: identityset.md
[quota-facet]: quota.md
[drive-resource]: drive.md
[drive-get]: ../api/drive_get.md
[item-get]: ../api/driveitem_get.md
[item-changes]: ../api/driveitem_delta.md
[item-search]: ../api/driveitem_search.md
[item-children]: ../api/driveitem_list_children.md


<!-- {
  "type": "#page.annotation",
  "description": "Drive is a top level object for OneDrive API that provides access to the contents of a drive. ",
  "keywords": "drive,objects,resources",
  "section": "documentation",
  "tocPath": "Drives",
  "tocBookmarks": { "Resources/Drive": "#" }
} -->
