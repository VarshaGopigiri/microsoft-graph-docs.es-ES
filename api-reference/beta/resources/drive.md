---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Unidad de disco
ms.openlocfilehash: c9926d0245b63a8d4545c4864b396624b82bf57a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090881"
---
# <a name="drive-resource-type"></a><span data-ttu-id="d7195-102">tipo de recurso de unidad</span><span class="sxs-lookup"><span data-stu-id="d7195-102">drive resource type</span></span>

> <span data-ttu-id="d7195-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d7195-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d7195-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d7195-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d7195-105">El recurso de unidad es el objeto de nivel superior que representa el OneDrive de un usuario o una biblioteca de documentos de SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d7195-105">The drive resource is the top level object representing a user's OneDrive or a document library in SharePoint.</span></span>

<span data-ttu-id="d7195-p102">Los usuarios de OneDrive siempre tendrán al menos una unidad disponible, la unidad predeterminada. Es posible que los usuarios sin licencia de OneDrive no tengan una unidad predeterminada disponible.</span><span class="sxs-lookup"><span data-stu-id="d7195-p102">OneDrive users will always have at least one drive available, their default drive. Users without a OneDrive license may not have a default drive available.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d7195-108">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d7195-108">JSON representation</span></span>

<span data-ttu-id="d7195-109">A continuación se muestra una representación JSON de un recurso Drive.</span><span class="sxs-lookup"><span data-stu-id="d7195-109">Here is a JSON representation of a Drive resource.</span></span>

<span data-ttu-id="d7195-110">El recurso **drive** deriva de [**baseItem**](baseitem.md) y hereda las propiedades de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="d7195-110">The **drive** resource is derived from [**baseItem**](baseitem.md) and inherits properties from that resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "activities",
    "createdBy",
    "createdDateTime",
    "description",
    "lastModifiedBy",
    "lastModifiedDateTime",
    "name",
    "webUrl",
    "items",
    "root",
    "special",
    "system"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.baseItem",
  "@odata.type": "microsoft.graph.drive"
}-->

```json
{
  "activities": [{"@odata.type": "microsoft.graph.itemActivity"}],
  "id": "string",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "string (timestamp)",
  "description": "string",
  "driveType": "personal | business | documentLibrary",
  "following": [ { "@odata.type": "microsoft.graph.driveItem" } ],
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

## <a name="properties"></a><span data-ttu-id="d7195-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d7195-111">Properties</span></span>

| <span data-ttu-id="d7195-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7195-112">Property</span></span>             | <span data-ttu-id="d7195-113">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7195-113">Type</span></span>                          | <span data-ttu-id="d7195-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7195-114">Description</span></span>                                                                                                                                                                                                                      |
| :------------------- | :---------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="d7195-115">createdBy</span><span class="sxs-lookup"><span data-stu-id="d7195-115">createdBy</span></span>            | <span data-ttu-id="d7195-116">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="d7195-116">[identitySet][]</span></span>               | <span data-ttu-id="d7195-p103">Identidad del usuario, del dispositivo o de la aplicación que ha creado el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p103">Identity of the user, device, or application which created the item. Read-only.</span></span>                                                                                                                                                  |
| <span data-ttu-id="d7195-119">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="d7195-119">createdDateTime</span></span>      | <span data-ttu-id="d7195-120">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d7195-120">dateTimeOffset</span></span>                | <span data-ttu-id="d7195-p104">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p104">Date and time of item creation. Read-only.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="d7195-123">description</span><span class="sxs-lookup"><span data-stu-id="d7195-123">description</span></span>          | <span data-ttu-id="d7195-124">String</span><span class="sxs-lookup"><span data-stu-id="d7195-124">String</span></span>                        | <span data-ttu-id="d7195-125">Proporciona una descripción de la unidad visible para el usuario.</span><span class="sxs-lookup"><span data-stu-id="d7195-125">Provide a user-visible description of the drive.</span></span> <span data-ttu-id="d7195-126">Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d7195-126">Read-write.</span></span>
| <span data-ttu-id="d7195-127">driveType</span><span class="sxs-lookup"><span data-stu-id="d7195-127">driveType</span></span>            | <span data-ttu-id="d7195-128">String</span><span class="sxs-lookup"><span data-stu-id="d7195-128">String</span></span>                        | <span data-ttu-id="d7195-p106">Describe el tipo de unidad que representa este recurso. Las unidades personales de OneDrive devolverán `personal`. OneDrive para la Empresa devolverá `business`. Las bibliotecas de documentos de SharePoint devolverán `documentLibrary`. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p106">Describes the type of drive represented by this resource. OneDrive personal drives will return `personal`. OneDrive for Business will return `business`. SharePoint document libraries will return `documentLibrary`. Read-only.</span></span> |
| <span data-ttu-id="d7195-134">id</span><span class="sxs-lookup"><span data-stu-id="d7195-134">id</span></span>                   | <span data-ttu-id="d7195-135">String</span><span class="sxs-lookup"><span data-stu-id="d7195-135">String</span></span>                        | <span data-ttu-id="d7195-p107">El identificador único de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p107">The unique identifier of the drive. Read-only.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="d7195-138">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="d7195-138">lastModifiedBy</span></span>       | <span data-ttu-id="d7195-139">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="d7195-139">[identitySet][]</span></span>               | <span data-ttu-id="d7195-p108">Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p108">Identity of the user, device, and application which last modified the item. Read-only.</span></span>                                                                                                                                           |
| <span data-ttu-id="d7195-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d7195-142">lastModifiedDateTime</span></span> | <span data-ttu-id="d7195-143">dateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d7195-143">dateTimeOffset</span></span>                | <span data-ttu-id="d7195-p109">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p109">Date and time the item was last modified. Read-only.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="d7195-146">name</span><span class="sxs-lookup"><span data-stu-id="d7195-146">name</span></span>                 | <span data-ttu-id="d7195-147">string</span><span class="sxs-lookup"><span data-stu-id="d7195-147">string</span></span>                        | <span data-ttu-id="d7195-p110">Nombre del elemento. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p110">The name of the item. Read-write.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="d7195-150">owner</span><span class="sxs-lookup"><span data-stu-id="d7195-150">owner</span></span>                | [<span data-ttu-id="d7195-151">identitySet</span><span class="sxs-lookup"><span data-stu-id="d7195-151">identitySet</span></span>](identityset.md) | <span data-ttu-id="d7195-p111">Opcional. La cuenta de usuario propietaria de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p111">Optional. The user account that owns the drive. Read-only.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="d7195-155">quota</span><span class="sxs-lookup"><span data-stu-id="d7195-155">quota</span></span>                | [<span data-ttu-id="d7195-156">quota</span><span class="sxs-lookup"><span data-stu-id="d7195-156">quota</span></span>](quota.md)             | <span data-ttu-id="d7195-p112">Opcional. Información sobre la cuota de espacio de almacenamiento de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p112">Optional. Information about the drive's storage space quota. Read-only.</span></span>                                                                                                                                                          |
| <span data-ttu-id="d7195-160">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="d7195-160">sharepointIds</span></span>        | <span data-ttu-id="d7195-161">[sharepointIds][]</span><span class="sxs-lookup"><span data-stu-id="d7195-161">[sharepointIds][]</span></span>             | <span data-ttu-id="d7195-p113">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p113">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>                                                                                                                                                         |
| <span data-ttu-id="d7195-164">system</span><span class="sxs-lookup"><span data-stu-id="d7195-164">system</span></span>               | <span data-ttu-id="d7195-165">[systemFacet][]</span><span class="sxs-lookup"><span data-stu-id="d7195-165">[systemFacet][]</span></span>               | <span data-ttu-id="d7195-166">Si está presente, indica que se trata de una unidad administrada por el sistema.</span><span class="sxs-lookup"><span data-stu-id="d7195-166">If present, indicates that this is a system-managed drive.</span></span> <span data-ttu-id="d7195-167">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-167">Read-only.</span></span>
| <span data-ttu-id="d7195-168">webUrl</span><span class="sxs-lookup"><span data-stu-id="d7195-168">webUrl</span></span>               | <span data-ttu-id="d7195-169">string (url)</span><span class="sxs-lookup"><span data-stu-id="d7195-169">string (url)</span></span>                  | <span data-ttu-id="d7195-p115">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p115">URL that displays the resource in the browser. Read-only.</span></span>                                                                                                                                                                        |

[identitySet]: identityset.md
[sharepointIds]: sharepointids.md
[systemFacet]: systemfacet.md

## <a name="relationships"></a><span data-ttu-id="d7195-175">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d7195-175">Relationships</span></span>

| <span data-ttu-id="d7195-176">Relación</span><span class="sxs-lookup"><span data-stu-id="d7195-176">Relationship</span></span> | <span data-ttu-id="d7195-177">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7195-177">Type</span></span>                                 | <span data-ttu-id="d7195-178">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7195-178">Description</span></span>
|:-------------|:-------------------------------------|:-----------------------
| <span data-ttu-id="d7195-179">activities</span><span class="sxs-lookup"><span data-stu-id="d7195-179">activities</span></span>   | <span data-ttu-id="d7195-180">Colección [itemActivity][]</span><span class="sxs-lookup"><span data-stu-id="d7195-180">[itemActivity][] collection</span></span>          | <span data-ttu-id="d7195-181">Lista de actividades recientes que tuvieron lugar en esta unidad.</span><span class="sxs-lookup"><span data-stu-id="d7195-181">The list of recent activities that took place under this drive.</span></span>
| <span data-ttu-id="d7195-182">items</span><span class="sxs-lookup"><span data-stu-id="d7195-182">items</span></span>        | <span data-ttu-id="d7195-183">Colección [driveitem](driveitem.md)</span><span class="sxs-lookup"><span data-stu-id="d7195-183">[driveitem](driveitem.md) collection</span></span> | <span data-ttu-id="d7195-p116">Todos los elementos contenidos en la unidad. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="d7195-p116">All items contained in the drive. Read-only. Nullable.</span></span>
| <span data-ttu-id="d7195-187">root</span><span class="sxs-lookup"><span data-stu-id="d7195-187">root</span></span>         | [<span data-ttu-id="d7195-188">driveitem</span><span class="sxs-lookup"><span data-stu-id="d7195-188">driveitem</span></span>](driveitem.md)            | <span data-ttu-id="d7195-p117">La carpeta raíz de la unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d7195-p117">The root folder of the drive. Read-only.</span></span>
| <span data-ttu-id="d7195-191">special</span><span class="sxs-lookup"><span data-stu-id="d7195-191">special</span></span>      | <span data-ttu-id="d7195-192">Colección [driveitem](driveitem.md)</span><span class="sxs-lookup"><span data-stu-id="d7195-192">[driveitem](driveitem.md) collection</span></span> | <span data-ttu-id="d7195-p118">Colección de carpetas comunes disponibles en OneDrive. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="d7195-p118">Collection of common folders available in OneDrive. Read-only. Nullable.</span></span>
| <span data-ttu-id="d7195-196">siguiente</span><span class="sxs-lookup"><span data-stu-id="d7195-196">following</span></span>    | <span data-ttu-id="d7195-197">Colección de [DriveItem](driveitem.md)</span><span class="sxs-lookup"><span data-stu-id="d7195-197">[DriveItem](driveitem.md) collection</span></span> | <span data-ttu-id="d7195-198">La lista de elementos que está siguiendo el usuario.</span><span class="sxs-lookup"><span data-stu-id="d7195-198">The list of items the user is following.</span></span> <span data-ttu-id="d7195-199">Sólo en OneDrive para la empresa.</span><span class="sxs-lookup"><span data-stu-id="d7195-199">Only in OneDrive for Business.</span></span>

## <a name="methods"></a><span data-ttu-id="d7195-200">Métodos</span><span class="sxs-lookup"><span data-stu-id="d7195-200">Methods</span></span>

|                        <span data-ttu-id="d7195-201">Tarea común</span><span class="sxs-lookup"><span data-stu-id="d7195-201">Common task</span></span>                         |         <span data-ttu-id="d7195-202">Método HTTP</span><span class="sxs-lookup"><span data-stu-id="d7195-202">HTTP method</span></span>         |
| :--------------------------------------------------------- | :-------------------------- |
| <span data-ttu-id="d7195-203">[Obtener los metadatos de la unidad de otra unidad][drive-get]</span><span class="sxs-lookup"><span data-stu-id="d7195-203">[Get Drive metadata of another Drive][drive-get]</span></span>           | `GET /drives/{drive-id}`    |
| <span data-ttu-id="d7195-204">[Obtener la carpeta raíz de la unidad predeterminada del usuario][item-get]</span><span class="sxs-lookup"><span data-stu-id="d7195-204">[Get root folder for user's default Drive][item-get]</span></span>       | `GET /drive/root`           |
| <span data-ttu-id="d7195-205">[Enumerar las actividades en la unidad][drive-activities]</span><span class="sxs-lookup"><span data-stu-id="d7195-205">[List activities under the Drive][drive-activities]</span></span>        | `GET /drive/activities`     |
| <span data-ttu-id="d7195-206">[Lista seguido elementos][drive-following]</span><span class="sxs-lookup"><span data-stu-id="d7195-206">[List followed Items][drive-following]</span></span>                     | `GET /drive/following`      |
| <span data-ttu-id="d7195-207">[Mostrar los elementos secundarios en la unidad][item-children]</span><span class="sxs-lookup"><span data-stu-id="d7195-207">[List children under the Drive][item-children]</span></span>             | `GET /drive/root/children`  |
| <span data-ttu-id="d7195-208">[Mostrar los cambios para todos los elementos de la unidad][item-changes]</span><span class="sxs-lookup"><span data-stu-id="d7195-208">[List changes for all Items in the Drive][item-changes]</span></span>    | `GET /drive/root/delta`     |
| <span data-ttu-id="d7195-209">[Buscar los elementos en la unidad][item-search]</span><span class="sxs-lookup"><span data-stu-id="d7195-209">[Search for Items in the Drive][item-search]</span></span>               | `GET /drive/root/search`    |
| [<span data-ttu-id="d7195-210">Acceso a la carpeta especial</span><span class="sxs-lookup"><span data-stu-id="d7195-210">Access special folder</span></span>](../api/drive-get-specialfolder.md) | `GET /drive/special/{name}` |

<span data-ttu-id="d7195-211">En la tabla anterior, los ejemplos utilizan `/drive`, pero otras rutas de acceso son válidos demasiado.</span><span class="sxs-lookup"><span data-stu-id="d7195-211">In the previous table, the examples use `/drive`, but other paths are valid too.</span></span>

[itemActivity]: itemactivity.md
[item-resource]: driveitem.md
[identity-set]: identityset.md
[quota-facet]: quota.md
[drive-resource]: drive.md
[drive-activities]: ../api/activities-list.md
[drive-following]: ../api/drive-list-following.md
[drive-get]: ../api/drive-get.md
[item-get]: ../api/driveitem-get.md
[item-changes]: ../api/driveitem-delta.md
[item-search]: ../api/driveitem-search.md
[item-children]: ../api/driveitem-list-children.md


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Drive is a top level object for OneDrive API that provides access to the contents of a drive. ",
  "keywords": "drive,objects,resources",
  "section": "documentation",
  "tocPath": "Drives",
  "tocBookmarks": { "Resources/Drive": "#" }
} -->