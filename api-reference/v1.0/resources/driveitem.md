---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: DriveItem
localization_priority: Priority
ms.openlocfilehash: 9de5de7f945177b1ab5c9f9107a32129f0f38c10
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27894561"
---
# <a name="driveitem-resource-type"></a><span data-ttu-id="af990-102">Tipo de recurso DriveItem</span><span class="sxs-lookup"><span data-stu-id="af990-102">DriveItem resource type</span></span>

<span data-ttu-id="af990-p101">El recurso **driveItem** representa un archivo, una carpeta u otro elemento almacenado en una unidad. Todos los objetos del sistema de archivos en OneDrive y SharePoint se devuelven como recursos de **driveItem**.</span><span class="sxs-lookup"><span data-stu-id="af990-p101">The **driveItem** resource represents a file, folder, or other item stored in a drive. All file system objects in OneDrive and SharePoint are returned as **driveItem** resources.</span></span>

<span data-ttu-id="af990-105">Hay dos maneras principales de abordar un recurso **driveItem**:</span><span class="sxs-lookup"><span data-stu-id="af990-105">There are two primary ways of addressing a **driveItem** resource:</span></span>

* <span data-ttu-id="af990-106">Con el identificador único **driveItem** utilizando `drive/items/{item-id}`</span><span class="sxs-lookup"><span data-stu-id="af990-106">By the **driveItem** unique identifier using `drive/items/{item-id}`</span></span>
* <span data-ttu-id="af990-107">Con la ruta de acceso del sistema de archivos utilizando `/drive/root:/path/to/file`</span><span class="sxs-lookup"><span data-stu-id="af990-107">By file system path using `/drive/root:/path/to/file`</span></span>

<span data-ttu-id="af990-p102">Los recursos **DriveItem** tienen facetas modeladas como propiedades que proporcionan datos sobre las identidades y las capacidades de driveItem. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="af990-p102">**DriveItem** resources have facets modeled as properties that provide data about the driveItem's identities and capabilities. For example:</span></span>

* <span data-ttu-id="af990-110">Las carpetas tienen una [**faceta folder**][folder].</span><span class="sxs-lookup"><span data-stu-id="af990-110">Folders have a [**folder facet**][folder]</span></span>
* <span data-ttu-id="af990-111">Los archivos tienen una [**faceta file**][file].</span><span class="sxs-lookup"><span data-stu-id="af990-111">Files have a [**file facet**][file].</span></span>
* <span data-ttu-id="af990-112">Las imágenes tienen una [**faceta image**][image], además de su faceta file.</span><span class="sxs-lookup"><span data-stu-id="af990-112">Images have an [**image facet**][image] in addition to their file facet.</span></span>
* <span data-ttu-id="af990-113">Las imágenes tomadas con una cámara (fotos) tienen una [**faceta photo**][photo] que identifica el elemento como una foto. Además, facilita las propiedades que indican cuándo se tomó la foto y con qué dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af990-113">Images taken with a camera (photos) have a [**photo facet**][photo] that identifies the item as a photo and provides the properties of when the photo was taken and with what device.</span></span>

<span data-ttu-id="af990-114">Los elementos con una faceta **folder** actúan como contenedores de elementos y, por lo tanto, tienen una referencia `children` que indica una colección de **driveItems** dentro de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="af990-114">Items with the **folder** facet act as containers of items and therefore have a `children` reference pointing to a collection of **driveItems** under the folder.</span></span>

## <a name="json-representation"></a><span data-ttu-id="af990-115">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="af990-115">JSON representation</span></span>

<span data-ttu-id="af990-116">A continuación se incluye una representación JSON del recurso **driveItem**.</span><span class="sxs-lookup"><span data-stu-id="af990-116">Here is a JSON representation of a **driveItem** resource.</span></span>

<span data-ttu-id="af990-117">El recurso **driveItem** deriva de [**baseItem**][baseItem] y hereda las propiedades de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="af990-117">The **driveItem** resource is derived from [**baseItem**][baseItem] and inherits properties from that resource.</span></span>

<!-- { "blockType": "resource", "@type": "microsoft.graph.driveItem", "@type.aka": "oneDrive.item",
       "baseType": "microsoft.graph.baseItem",
       "optionalProperties": ["cTag", "children", "folder", "file", "image", "audio", "video",
       "location", "deleted", "specialFolder", "photo", "thumbnails", "searchResult", "remoteItem",
       "shared", "content", "@microsoft.graph.conflictBehavior", "@microsoft.graph.downloadUrl", "@content.sourceUrl",
       "sharepointIds"],
       "keyProperty": "id", "openType": true } -->

```json
{
  "audio": { "@odata.type": "microsoft.graph.audio" },
  "content": { "@odata.type": "Edm.Stream" },
  "cTag": "string (etag)",
  "deleted": { "@odata.type": "microsoft.graph.deleted"},
  "description": "string",
  "file": { "@odata.type": "microsoft.graph.file" },
  "fileSystemInfo": { "@odata.type": "microsoft.graph.fileSystemInfo" },
  "folder": { "@odata.type": "microsoft.graph.folder" },
  "image": { "@odata.type": "microsoft.graph.image" },
  "location": { "@odata.type": "microsoft.graph.geoCoordinates" },
  "package": { "@odata.type": "microsoft.graph.package" },
  "photo": { "@odata.type": "microsoft.graph.photo" },
  "publication": {"@odata.type": "microsoft.graph.publicationFacet"},
  "remoteItem": { "@odata.type": "microsoft.graph.remoteItem" },
  "root": { "@odata.type": "microsoft.graph.root" },
  "searchResult": { "@odata.type": "microsoft.graph.searchResult" },
  "shared": { "@odata.type": "microsoft.graph.shared" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "size": 1024,
  "specialFolder": { "@odata.type": "microsoft.graph.specialFolder" },
  "video": { "@odata.type": "microsoft.graph.video" },
  "webDavUrl": "string",

  /* relationships */
  "children": [{ "@odata.type": "microsoft.graph.driveItem" }],
  "createdByUser": { "@odata.type": "microsoft.graph.user" },
  "lastModifiedByUser": { "@odata.type": "microsoft.graph.user" },
  "permissions": [ {"@odata.type": "microsoft.graph.permission"} ],
  "thumbnails": [ {"@odata.type": "microsoft.graph.thumbnailSet"}],
  "versions": [ {"@odata.type": "microsoft.graph.driveItemVersion"}],

  /* inherited from baseItem */
  "id": "string (identifier)",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "eTag": "string",
  "lastModifiedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "parentReference": {"@odata.type": "microsoft.graph.itemReference"},
  "webUrl": "string",

  /* instance annotations */
  "@microsoft.graph.conflictBehavior": "string",
  "@microsoft.graph.downloadUrl": "url",
  "@microsoft.graph.sourceUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="af990-118">Propiedades</span><span class="sxs-lookup"><span data-stu-id="af990-118">Properties</span></span>

| <span data-ttu-id="af990-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="af990-119">Property</span></span>             | <span data-ttu-id="af990-120">Tipo</span><span class="sxs-lookup"><span data-stu-id="af990-120">Type</span></span>               | <span data-ttu-id="af990-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="af990-121">Description</span></span>
|:---------------------|:-------------------|:---------------------------------
| <span data-ttu-id="af990-122">audio</span><span class="sxs-lookup"><span data-stu-id="af990-122">audio</span></span>                | <span data-ttu-id="af990-123">[audio][]</span><span class="sxs-lookup"><span data-stu-id="af990-123">[audio][]</span></span>          | <span data-ttu-id="af990-p103">Metadatos de audio, si el elemento es un archivo de audio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p103">Audio metadata, if the item is an audio file. Read-only.</span></span>
| <span data-ttu-id="af990-126">content</span><span class="sxs-lookup"><span data-stu-id="af990-126">content</span></span>              | <span data-ttu-id="af990-127">Secuencia</span><span class="sxs-lookup"><span data-stu-id="af990-127">Stream</span></span>             | <span data-ttu-id="af990-128">La secuencia de contenido, si el elemento representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="af990-128">The content stream, if the item represents a file.</span></span>
| <span data-ttu-id="af990-129">createdBy</span><span class="sxs-lookup"><span data-stu-id="af990-129">createdBy</span></span>            | <span data-ttu-id="af990-130">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="af990-130">[identitySet][]</span></span>    | <span data-ttu-id="af990-p104">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p104">Identity of the user, device, and application which created the item. Read-only.</span></span>
| <span data-ttu-id="af990-133">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="af990-133">createdDateTime</span></span>      | <span data-ttu-id="af990-134">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="af990-134">DateTimeOffset</span></span>     | <span data-ttu-id="af990-p105">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p105">Date and time of item creation. Read-only.</span></span>
| <span data-ttu-id="af990-137">cTag</span><span class="sxs-lookup"><span data-stu-id="af990-137">cTag</span></span>                 | <span data-ttu-id="af990-138">String</span><span class="sxs-lookup"><span data-stu-id="af990-138">String</span></span>             | <span data-ttu-id="af990-p106">Un eTag del contenido del elemento. No se cambia este eTag si solo se modifican los metadatos. **Nota** Esta propiedad no se devuelve si el elemento es una carpeta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p106">An eTag for the content of the item. This eTag is not changed if only the metadata is changed. **Note** This property is not returned if the item is a folder. Read-only.</span></span>
| <span data-ttu-id="af990-143">deleted</span><span class="sxs-lookup"><span data-stu-id="af990-143">deleted</span></span>              | <span data-ttu-id="af990-144">[deleted][]</span><span class="sxs-lookup"><span data-stu-id="af990-144">[deleted][]</span></span>        | <span data-ttu-id="af990-p107">Información sobre el estado del elemento eliminado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p107">Information about the deleted state of the item. Read-only.</span></span>
| <span data-ttu-id="af990-147">description</span><span class="sxs-lookup"><span data-stu-id="af990-147">description</span></span>          | <span data-ttu-id="af990-148">Cadena</span><span class="sxs-lookup"><span data-stu-id="af990-148">String</span></span>             | <span data-ttu-id="af990-p108">Proporciona una descripción del elemento visible para el usuario. Lectura y escritura. Solo en OneDrive Personal</span><span class="sxs-lookup"><span data-stu-id="af990-p108">Provides a user-visible description of the item. Read-write. Only on OneDrive Personal</span></span>
| <span data-ttu-id="af990-152">eTag</span><span class="sxs-lookup"><span data-stu-id="af990-152">eTag</span></span>                 | <span data-ttu-id="af990-153">Cadena</span><span class="sxs-lookup"><span data-stu-id="af990-153">String</span></span>             | <span data-ttu-id="af990-p109">ETag de todo el elemento (metadatos + contenido). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p109">eTag for the entire item (metadata + content). Read-only.</span></span>
| <span data-ttu-id="af990-156">file</span><span class="sxs-lookup"><span data-stu-id="af990-156">file</span></span>                 | <span data-ttu-id="af990-157">[file][]</span><span class="sxs-lookup"><span data-stu-id="af990-157">[file][]</span></span>           | <span data-ttu-id="af990-p110">Metadatos de archivo, si el elemento es un archivo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p110">File metadata, if the item is a file. Read-only.</span></span>
| <span data-ttu-id="af990-160">fileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="af990-160">fileSystemInfo</span></span>       | <span data-ttu-id="af990-161">[fileSystemInfo][]</span><span class="sxs-lookup"><span data-stu-id="af990-161">[fileSystemInfo][]</span></span> | <span data-ttu-id="af990-p111">Información del sistema de archivos del cliente. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="af990-p111">File system information on client. Read-write.</span></span>
| <span data-ttu-id="af990-164">folder</span><span class="sxs-lookup"><span data-stu-id="af990-164">folder</span></span>               | <span data-ttu-id="af990-165">[folder][]</span><span class="sxs-lookup"><span data-stu-id="af990-165">[folder][]</span></span>         | <span data-ttu-id="af990-p112">Metadatos de carpeta, si el elemento es una carpeta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p112">Folder metadata, if the item is a folder. Read-only.</span></span>
| <span data-ttu-id="af990-168">id</span><span class="sxs-lookup"><span data-stu-id="af990-168">id</span></span>                   | <span data-ttu-id="af990-169">Cadena</span><span class="sxs-lookup"><span data-stu-id="af990-169">String</span></span>             | <span data-ttu-id="af990-p113">El identificador único del elemento dentro del Drive. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p113">The unique identifier of the item within the Drive. Read-only.</span></span>
| <span data-ttu-id="af990-172">image</span><span class="sxs-lookup"><span data-stu-id="af990-172">image</span></span>                | <span data-ttu-id="af990-173">[image][]</span><span class="sxs-lookup"><span data-stu-id="af990-173">[image][]</span></span>          | <span data-ttu-id="af990-p114">Metadatos de imagen, si el elemento es una imagen. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p114">Image metadata, if the item is an image. Read-only.</span></span>
| <span data-ttu-id="af990-176">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="af990-176">lastModifiedBy</span></span>       | <span data-ttu-id="af990-177">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="af990-177">[identitySet][]</span></span>    | <span data-ttu-id="af990-p115">Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p115">Identity of the user, device, and application which last modified the item. Read-only.</span></span>
| <span data-ttu-id="af990-180">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="af990-180">lastModifiedDateTime</span></span> | <span data-ttu-id="af990-181">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="af990-181">DateTimeOffset</span></span>     | <span data-ttu-id="af990-p116">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p116">Date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="af990-184">location</span><span class="sxs-lookup"><span data-stu-id="af990-184">location</span></span>             | <span data-ttu-id="af990-185">[geoCoordinates][]</span><span class="sxs-lookup"><span data-stu-id="af990-185">[geoCoordinates][]</span></span> | <span data-ttu-id="af990-p117">Metadatos de ubicación, si el elemento tiene datos de ubicación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p117">Location metadata, if the item has location data. Read-only.</span></span>
| <span data-ttu-id="af990-188">name</span><span class="sxs-lookup"><span data-stu-id="af990-188">name</span></span>                 | <span data-ttu-id="af990-189">Cadena</span><span class="sxs-lookup"><span data-stu-id="af990-189">String</span></span>             | <span data-ttu-id="af990-p118">El nombre del elemento (nombre de archivo y extensión). Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="af990-p118">The name of the item (filename and extension). Read-write.</span></span>
| <span data-ttu-id="af990-192">paquete</span><span class="sxs-lookup"><span data-stu-id="af990-192">package</span></span>              | <span data-ttu-id="af990-193">[package][]</span><span class="sxs-lookup"><span data-stu-id="af990-193">[package][]</span></span>        | <span data-ttu-id="af990-p119">Si está presente, indica que este elemento es un paquete en lugar de una carpeta o archivo. Los paquetes se tratan como archivos en algunos contextos y como carpetas en otros. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p119">If present, indicates that this item is a package instead of a folder or file. Packages are treated like files in some contexts and folders in others. Read-only.</span></span>
| <span data-ttu-id="af990-197">parentReference</span><span class="sxs-lookup"><span data-stu-id="af990-197">parentReference</span></span>      | <span data-ttu-id="af990-198">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="af990-198">[itemReference][]</span></span>  | <span data-ttu-id="af990-p120">Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="af990-p120">Parent information, if the item has a parent. Read-write.</span></span>
| <span data-ttu-id="af990-201">photo</span><span class="sxs-lookup"><span data-stu-id="af990-201">photo</span></span>                | <span data-ttu-id="af990-202">[photo][]</span><span class="sxs-lookup"><span data-stu-id="af990-202">[photo][]</span></span>          | <span data-ttu-id="af990-p121">Metadatos de foto, si el elemento es una foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p121">Photo metadata, if the item is a photo. Read-only.</span></span>
| <span data-ttu-id="af990-205">publication</span><span class="sxs-lookup"><span data-stu-id="af990-205">publication</span></span>          | <span data-ttu-id="af990-206">[publicationFacet][]</span><span class="sxs-lookup"><span data-stu-id="af990-206">[publicationFacet][]</span></span> | <span data-ttu-id="af990-207">Proporciona información sobre el estado publicado o extraído de un elemento, en ubicaciones que admiten esas acciones.</span><span class="sxs-lookup"><span data-stu-id="af990-207">Provides information about the published or checked-out state of an item, in locations that support such actions.</span></span> <span data-ttu-id="af990-208">Esta propiedad no se devuelve de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="af990-208">This property is not returned by default.</span></span> <span data-ttu-id="af990-209">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-209">Read-only.</span></span> |
| <span data-ttu-id="af990-210">remoteItem</span><span class="sxs-lookup"><span data-stu-id="af990-210">remoteItem</span></span>           | <span data-ttu-id="af990-211">[remoteItem][]</span><span class="sxs-lookup"><span data-stu-id="af990-211">[remoteItem][]</span></span>     | <span data-ttu-id="af990-p123">Datos de elemento remoto, si el elemento se comparte desde una unidad distinta a la de acceso. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p123">Remote item data, if the item is shared from a drive other than the one being accessed. Read-only.</span></span>
| <span data-ttu-id="af990-214">root</span><span class="sxs-lookup"><span data-stu-id="af990-214">root</span></span>                 | <span data-ttu-id="af990-215">[root][]</span><span class="sxs-lookup"><span data-stu-id="af990-215">[root][]</span></span>           | <span data-ttu-id="af990-216">Si esta propiedad no es NULL, indica que el driveItem es el driveItem de nivel superior de la unidad.</span><span class="sxs-lookup"><span data-stu-id="af990-216">If this property is non-null, it indicates that the driveItem is the top-most driveItem in the drive.</span></span>
| <span data-ttu-id="af990-217">searchResult</span><span class="sxs-lookup"><span data-stu-id="af990-217">searchResult</span></span>         | <span data-ttu-id="af990-218">[searchResult][]</span><span class="sxs-lookup"><span data-stu-id="af990-218">[searchResult][]</span></span>   | <span data-ttu-id="af990-p124">Metadatos de búsqueda, si el elemento es un resultado de búsqueda. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p124">Search metadata, if the item is from a search result. Read-only.</span></span>
| <span data-ttu-id="af990-221">compartido</span><span class="sxs-lookup"><span data-stu-id="af990-221">shared</span></span>               | <span data-ttu-id="af990-222">[shared][]</span><span class="sxs-lookup"><span data-stu-id="af990-222">[shared][]</span></span>         | <span data-ttu-id="af990-p125">Indica que el elemento se ha compartido con otros usuarios y proporciona información sobre el estado del elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p125">Indicates that the item has been shared with others and provides information about the shared state of the item. Read-only.</span></span>
| <span data-ttu-id="af990-225">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="af990-225">sharepointIds</span></span>        | <span data-ttu-id="af990-226">[sharepointIds][]</span><span class="sxs-lookup"><span data-stu-id="af990-226">[sharepointIds][]</span></span>  | <span data-ttu-id="af990-p126">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p126">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>
| <span data-ttu-id="af990-229">size</span><span class="sxs-lookup"><span data-stu-id="af990-229">size</span></span>                 | <span data-ttu-id="af990-230">Int64</span><span class="sxs-lookup"><span data-stu-id="af990-230">Int64</span></span>              | <span data-ttu-id="af990-p127">Tamaño del elemento en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p127">Size of the item in bytes. Read-only.</span></span>
| <span data-ttu-id="af990-233">specialFolder</span><span class="sxs-lookup"><span data-stu-id="af990-233">specialFolder</span></span>        | <span data-ttu-id="af990-234">[specialFolder][]</span><span class="sxs-lookup"><span data-stu-id="af990-234">[specialFolder][]</span></span>  | <span data-ttu-id="af990-p128">Si el elemento actual también está disponible como una carpeta especial, se devuelve esta faceta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p128">If the current item is also available as a special folder, this facet is returned. Read-only.</span></span>
| <span data-ttu-id="af990-237">video</span><span class="sxs-lookup"><span data-stu-id="af990-237">video</span></span>                | <span data-ttu-id="af990-238">[video][]</span><span class="sxs-lookup"><span data-stu-id="af990-238">[video][]</span></span>          | <span data-ttu-id="af990-p129">Metadatos de vídeo, si el elemento es un vídeo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p129">Video metadata, if the item is a video. Read-only.</span></span>
| <span data-ttu-id="af990-241">webDavUrl</span><span class="sxs-lookup"><span data-stu-id="af990-241">webDavUrl</span></span>            | <span data-ttu-id="af990-242">String</span><span class="sxs-lookup"><span data-stu-id="af990-242">String</span></span>             | <span data-ttu-id="af990-243">Dirección URL compatible con WebDAV del elemento.</span><span class="sxs-lookup"><span data-stu-id="af990-243">WebDAV compatible URL for the item.</span></span>
| <span data-ttu-id="af990-244">webUrl</span><span class="sxs-lookup"><span data-stu-id="af990-244">webUrl</span></span>               | <span data-ttu-id="af990-245">Cadena</span><span class="sxs-lookup"><span data-stu-id="af990-245">String</span></span>             | <span data-ttu-id="af990-p130">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p130">URL that displays the resource in the browser. Read-only.</span></span>

<span data-ttu-id="af990-p131">**Nota:** Las propiedades eTag y cTag funcionan de forma diferente en los contenedores (carpetas). El valor de cTag se modifica cuando se cambia el contenido o los metadatos de cualquier descendiente de la carpeta. El valor de eTag solo se modifica cuando se cambian las propiedades de la carpeta, excepto las propiedades que derivan de descendientes (como **childCount** o **lastModifiedDateTime**).</span><span class="sxs-lookup"><span data-stu-id="af990-p131">**Note:** The eTag and cTag properties work differently on containers (folders). The cTag value is modified when content or metadata of any descendant of the folder is changed. The eTag value is only modified when the folder's properties are changed, except for properties that are derived from descendants (like **childCount** or **lastModifiedDateTime**).</span></span>

## <a name="relationships"></a><span data-ttu-id="af990-251">Relaciones</span><span class="sxs-lookup"><span data-stu-id="af990-251">Relationships</span></span>

| <span data-ttu-id="af990-252">Relación</span><span class="sxs-lookup"><span data-stu-id="af990-252">Relationship</span></span>       | <span data-ttu-id="af990-253">Tipo</span><span class="sxs-lookup"><span data-stu-id="af990-253">Type</span></span>                        | <span data-ttu-id="af990-254">Descripción</span><span class="sxs-lookup"><span data-stu-id="af990-254">Description</span></span>
|:-------------------|:----------------------------|:--------------------------
| <span data-ttu-id="af990-255">children</span><span class="sxs-lookup"><span data-stu-id="af990-255">children</span></span>           | <span data-ttu-id="af990-256">colección de driveItem</span><span class="sxs-lookup"><span data-stu-id="af990-256">driveItem collection</span></span>        | <span data-ttu-id="af990-p132">Colección que contiene objetos Item de los elementos secundarios inmediatos del elemento. Solo los elementos que representan carpetas tienen elementos secundarios. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="af990-p132">Collection containing Item objects for the immediate children of Item. Only items representing folders have children. Read-only. Nullable.</span></span>
| <span data-ttu-id="af990-261">createdByUser</span><span class="sxs-lookup"><span data-stu-id="af990-261">createdByUser</span></span>      | <span data-ttu-id="af990-262">[user][]</span><span class="sxs-lookup"><span data-stu-id="af990-262">[user][]</span></span>                    | <span data-ttu-id="af990-263">Identidad del usuario que ha creado el elemento.</span><span class="sxs-lookup"><span data-stu-id="af990-263">Identity of the user who created the item.</span></span> <span data-ttu-id="af990-264">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-264">Read-only.</span></span>
| <span data-ttu-id="af990-265">lastModifiedByUser</span><span class="sxs-lookup"><span data-stu-id="af990-265">lastModifiedByUser</span></span> | <span data-ttu-id="af990-266">[user][]</span><span class="sxs-lookup"><span data-stu-id="af990-266">[user][]</span></span>                    | <span data-ttu-id="af990-267">Identidad del usuario que ha modificado por última vez el elemento.</span><span class="sxs-lookup"><span data-stu-id="af990-267">Identity of the user who last modified the item.</span></span> <span data-ttu-id="af990-268">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-268">Read-only.</span></span>
| <span data-ttu-id="af990-269">listItem</span><span class="sxs-lookup"><span data-stu-id="af990-269">listItem</span></span>           | <span data-ttu-id="af990-270">[listItem][]</span><span class="sxs-lookup"><span data-stu-id="af990-270">[listItem][]</span></span>                | <span data-ttu-id="af990-271">Para las unidades en SharePoint, el elemento de lista de biblioteca de documentos asociada.</span><span class="sxs-lookup"><span data-stu-id="af990-271">For drives in SharePoint, the associated document library list item.</span></span> <span data-ttu-id="af990-272">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-272">Read-only.</span></span> <span data-ttu-id="af990-273">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="af990-273">Nullable.</span></span>
| <span data-ttu-id="af990-274">permissions</span><span class="sxs-lookup"><span data-stu-id="af990-274">permissions</span></span>        | <span data-ttu-id="af990-275">Colección [permission][]</span><span class="sxs-lookup"><span data-stu-id="af990-275">[permission][] collection</span></span>   | <span data-ttu-id="af990-p136">El conjunto de permisos del elemento. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="af990-p136">The set of permissions for the item. Read-only. Nullable.</span></span>
| <span data-ttu-id="af990-279">miniaturas</span><span class="sxs-lookup"><span data-stu-id="af990-279">thumbnails</span></span>         | <span data-ttu-id="af990-280">Colección [thumbnailSet][]</span><span class="sxs-lookup"><span data-stu-id="af990-280">[thumbnailSet][] collection</span></span> | <span data-ttu-id="af990-p137">Colección que contiene objetos [ThumbnailSet][] asociados al elemento. Para obtener más información, consulte [obtener miniaturas][]. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="af990-p137">Collection containing [ThumbnailSet][] objects associated with the item. For more info, see [getting thumbnails][]. Read-only. Nullable.</span></span>
| <span data-ttu-id="af990-285">versiones</span><span class="sxs-lookup"><span data-stu-id="af990-285">versions</span></span>           | <span data-ttu-id="af990-286">colección de [driveItemVersion][]</span><span class="sxs-lookup"><span data-stu-id="af990-286">[driveItemVersion][] collection</span></span> | <span data-ttu-id="af990-287">La lista de las versiones anteriores del elemento.</span><span class="sxs-lookup"><span data-stu-id="af990-287">The list of previous versions of the item.</span></span> <span data-ttu-id="af990-288">Para obtener más información, vea [Introducción a las versiones anteriores][].</span><span class="sxs-lookup"><span data-stu-id="af990-288">For more info, see [getting previous versions][].</span></span> <span data-ttu-id="af990-289">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-289">Read-only.</span></span> <span data-ttu-id="af990-290">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="af990-290">Nullable.</span></span>
| <span data-ttu-id="af990-291">libro de trabajo</span><span class="sxs-lookup"><span data-stu-id="af990-291">workbook</span></span>           | <span data-ttu-id="af990-292">[workbook][]</span><span class="sxs-lookup"><span data-stu-id="af990-292">[workbook][]</span></span>                | <span data-ttu-id="af990-293">Para los archivos que son hojas de cálculo de Excel, tiene acceso a la API para trabajar con contenido de la hoja de cálculo del libro.</span><span class="sxs-lookup"><span data-stu-id="af990-293">For files that are Excel spreadsheets, accesses the workbook API to work with the spreadsheet's contents.</span></span> <span data-ttu-id="af990-294">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="af990-294">Nullable.</span></span>

## <a name="instance-attributes"></a><span data-ttu-id="af990-295">Atributos de instancia</span><span class="sxs-lookup"><span data-stu-id="af990-295">Instance Attributes</span></span>

<span data-ttu-id="af990-p140">Los atributos de instancia son propiedades con comportamientos especiales. Estas propiedades son temporales y o bien a) definen el comportamiento que debería tener el servicio o b) proporcionan valores de propiedad a corto plazo, como una dirección URL de descarga de un elemento que expira.</span><span class="sxs-lookup"><span data-stu-id="af990-p140">Instance attributes are properties with special behaviors. These properties are temporary and either a) define behavior the service should perform or b) provide short-term property values, like a download URL for an item that expires.</span></span>

| <span data-ttu-id="af990-298">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="af990-298">Property name</span></span>                     | <span data-ttu-id="af990-299">Tipo</span><span class="sxs-lookup"><span data-stu-id="af990-299">Type</span></span>   | <span data-ttu-id="af990-300">Descripción</span><span class="sxs-lookup"><span data-stu-id="af990-300">Description</span></span>
|:----------------------------------|:-------|:--------------------------------
| <span data-ttu-id="af990-301">@microsoft.graph.conflictBehavior</span><span class="sxs-lookup"><span data-stu-id="af990-301">@microsoft.graph.conflictBehavior</span></span> | <span data-ttu-id="af990-302">string</span><span class="sxs-lookup"><span data-stu-id="af990-302">string</span></span> | <span data-ttu-id="af990-p141">El comportamiento de resolución de conflictos para las acciones que crean un nuevo elemento. Puede utilizar los valores de *fail*, *replace*, o *rename*. El valor predeterminado de PUT es *replace*. Nunca se devuelve un elemento con esta anotación. Solo escritura.</span><span class="sxs-lookup"><span data-stu-id="af990-p141">The conflict resolution behavior for actions that create a new item. You can use the values *fail*, *replace*, or *rename*. The default for PUT is *replace*. An item will never be returned with this annotation. Write-only.</span></span>
| <span data-ttu-id="af990-308">@microsoft.graph.downloadUrl</span><span class="sxs-lookup"><span data-stu-id="af990-308">@microsoft.graph.downloadUrl</span></span>      | <span data-ttu-id="af990-309">string</span><span class="sxs-lookup"><span data-stu-id="af990-309">string</span></span> | <span data-ttu-id="af990-p142">Una dirección URL que puede utilizarse para descargar el contenido de este archivo. No es necesaria la autenticación con esta dirección URL. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="af990-p142">A URL that can be used to download this file's content. Authentication is not required with this URL. Read-only.</span></span>
| <span data-ttu-id="af990-313">@microsoft.graph.sourceUrl</span><span class="sxs-lookup"><span data-stu-id="af990-313">@microsoft.graph.sourceUrl</span></span>        | <span data-ttu-id="af990-314">string</span><span class="sxs-lookup"><span data-stu-id="af990-314">string</span></span> | <span data-ttu-id="af990-p143">Al emitir una solicitud PUT, esta anotación de instancia puede utilizarse para indicar al servicio que descargue el contenido de la dirección URL y lo guarde como el archivo. Solo escritura.</span><span class="sxs-lookup"><span data-stu-id="af990-p143">When issuing a PUT request, this instance annotation can be used to instruct the service to download the contents of the URL, and store it as the file. Write-only.</span></span>

<span data-ttu-id="af990-p144">**Nota:** El valor @microsoft.graph.downloadUrl es una dirección URL de corta duración y no puede almacenarse en caché. La dirección URL solo estará disponible durante un breve período de tiempo (1 hora) antes de ser invalidada.</span><span class="sxs-lookup"><span data-stu-id="af990-p144">**Note:** The @microsoft.graph.downloadUrl value is a short-lived URL and can't be cached. The URL will only be available for a short period of time (1 hour) before it is invalidated.</span></span>

## <a name="methods"></a><span data-ttu-id="af990-319">Métodos</span><span class="sxs-lookup"><span data-stu-id="af990-319">Methods</span></span>

| <span data-ttu-id="af990-320">Método</span><span class="sxs-lookup"><span data-stu-id="af990-320">Method</span></span>                                                   | <span data-ttu-id="af990-321">Ruta de acceso a REST</span><span class="sxs-lookup"><span data-stu-id="af990-321">REST Path</span></span>
|:---------------------------------------------------------|:------------------
| [<span data-ttu-id="af990-322">Obtener elemento</span><span class="sxs-lookup"><span data-stu-id="af990-322">Get item</span></span>](../api/driveitem-get.md)                      | `GET /drive/items/{item-id}`
| [<span data-ttu-id="af990-323">Enumerar elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="af990-323">List children</span></span>](../api/driveitem-list-children.md)       | `GET /drive/items/{item-id}/children`
| [<span data-ttu-id="af990-324">Enumerar versiones</span><span class="sxs-lookup"><span data-stu-id="af990-324">List versions</span></span>](../api/driveitem-list-versions.md)       | `GET /drive/items/{item-id}/versions`
| [<span data-ttu-id="af990-325">Crear elemento</span><span class="sxs-lookup"><span data-stu-id="af990-325">Create item</span></span>](../api/driveitem-post-children.md)         | `POST /drive/items/{item-id}/children`
| [<span data-ttu-id="af990-326">Actualizar elemento</span><span class="sxs-lookup"><span data-stu-id="af990-326">Update item</span></span>](../api/driveitem-update.md)                | `PATCH /drive/items/{item-id}`
| [<span data-ttu-id="af990-327">Cargar contenido</span><span class="sxs-lookup"><span data-stu-id="af990-327">Upload content</span></span>](../api/driveitem-put-content.md)        | `PUT /drive/items/{item-id}/content`
| [<span data-ttu-id="af990-328">Descargar contenido</span><span class="sxs-lookup"><span data-stu-id="af990-328">Download content</span></span>](../api/driveitem-get-content.md)      | `GET /drive/items/{item-id}/content`
| <span data-ttu-id="af990-329">[Descargar el formato de archivo específico][download-format]</span><span class="sxs-lookup"><span data-stu-id="af990-329">[Download specific file format][download-format]</span></span>         | `GET /drive/items/{item-id}/content?format={format}`
| [<span data-ttu-id="af990-330">Eliminar elemento</span><span class="sxs-lookup"><span data-stu-id="af990-330">Delete item</span></span>](../api/driveitem-delete.md)                | `DELETE /drive/items/{item-id}`
| [<span data-ttu-id="af990-331">Mover elemento</span><span class="sxs-lookup"><span data-stu-id="af990-331">Move item</span></span>](../api/driveitem-move.md)                    | `PATCH /drive/items/{item-id}`
| [<span data-ttu-id="af990-332">Copiar elemento</span><span class="sxs-lookup"><span data-stu-id="af990-332">Copy item</span></span>](../api/driveitem-copy.md)                    | `POST /drive/items/{item-id}/copy`
| [<span data-ttu-id="af990-333">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="af990-333">Search items</span></span>](../api/driveitem-search.md)               | `GET /drive/items/{item-id}/search(q='text')`
| [<span data-ttu-id="af990-334">Enumerar cambios en una unidad</span><span class="sxs-lookup"><span data-stu-id="af990-334">List changes in a drive</span></span>](../api/driveitem-delta.md)     | `GET /drive/root/delta`
| [<span data-ttu-id="af990-335">Enumerar miniaturas</span><span class="sxs-lookup"><span data-stu-id="af990-335">List thumbnails</span></span>](../api/driveitem-list-thumbnails.md)   | `GET /drive/items/{item-id}/thumbnails`
| [<span data-ttu-id="af990-336">Crear vínculo para compartir</span><span class="sxs-lookup"><span data-stu-id="af990-336">Create sharing link</span></span>](../api/driveitem-createlink.md)    | `POST /drive/items/{item-id}/createLink`
| [<span data-ttu-id="af990-337">Agregar permisos</span><span class="sxs-lookup"><span data-stu-id="af990-337">Add permissions</span></span>](../api/driveitem-invite.md)            | `POST /drive/items/{item-id}/invite`
| [<span data-ttu-id="af990-338">Enumerar permisos</span><span class="sxs-lookup"><span data-stu-id="af990-338">List permissions</span></span>](../api/driveitem-list-permissions.md) | `GET /drive/items/{item-id}/permissions`
| [<span data-ttu-id="af990-339">Eliminar permiso</span><span class="sxs-lookup"><span data-stu-id="af990-339">Delete permission</span></span>](../api/permission-delete.md)         | `DELETE /drive/items/{item-id}/permissions/{perm-id}`
| <span data-ttu-id="af990-340">[Vista previa del artículo][item-preview]</span><span class="sxs-lookup"><span data-stu-id="af990-340">[Preview item][item-preview]</span></span>                             | `POST /drive/items/{item-id}/preview`

[item-preview]: ../api/driveitem-preview.md

## <a name="remarks"></a><span data-ttu-id="af990-341">Observaciones</span><span class="sxs-lookup"><span data-stu-id="af990-341">Remarks</span></span>

<span data-ttu-id="af990-342">En las bibliotecas de documentos de OneDrive para la Empresa o SharePoint, no se devuelve la propiedad **cTag** si **driveItem** tiene una faceta [folder][].</span><span class="sxs-lookup"><span data-stu-id="af990-342">In OneDrive for Business or SharePoint document libraries, the **cTag** property is not returned, if the **driveItem** has a [folder][] facet.</span></span>

[audio]: audio.md
[baseItem]: baseitem.md
[deleted]: deleted.md
[download-format]: ../api/driveitem-get-content-format.md
[driveItemVersion]: driveitemversion.md
[file]: file.md
[fileSystemInfo]: filesysteminfo.md
[folder]: folder.md
[Introducción a las versiones anteriores]: ../api/driveitem-list-versions.md
[getting previous versions]: ../api/driveitem-list-versions.md
[obtener miniaturas]: ../api/driveitem-list-thumbnails.md
[getting thumbnails]: ../api/driveitem-list-thumbnails.md
[identitySet]: identityset.md
[image]: image.md
[itemReference]: itemreference.md
[geoCoordinates]: geocoordinates.md
[listItem]: listitem.md
[package]: package.md
[permission]: permission.md
[photo]: photo.md
[remoteItem]: remoteitem.md
[root]: root.md
[searchResult]: searchresult.md
[shared]: shared.md
[sharepointIds]: sharepointids.md
[specialFolder]: specialfolder.md
[thumbnailSet]: thumbnailset.md
[video]: video.md
[workbook]: workbook.md
[user]: https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/users
[publicationFacet]: publicationfacet.md

<!-- {
  "type": "#page.annotation",
  "description": "Item is the main data model in the OneDrive API. Everything is an item.",
  "keywords": "item,facet,resource",
  "section": "documentation",
  "tocPath": "Items",
  "tocBookmarks": { "Resources/Item": "#" }
} -->
