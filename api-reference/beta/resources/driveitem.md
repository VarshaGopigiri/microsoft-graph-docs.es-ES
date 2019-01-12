---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: DriveItem
localization_priority: Normal
ms.prod: sharepoint
ms.openlocfilehash: 98930017f9ca3f70501cd10e4a3029f7a240ce41
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977780"
---
# <a name="driveitem-resource-type"></a><span data-ttu-id="3540f-102">tipo de recurso driveItem</span><span class="sxs-lookup"><span data-stu-id="3540f-102">driveItem resource type</span></span>

> <span data-ttu-id="3540f-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3540f-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3540f-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3540f-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3540f-p102">El recurso **driveItem** representa un archivo, una carpeta u otro elemento almacenado en una unidad. Todos los objetos del sistema de archivos en OneDrive y SharePoint se devuelven como recursos de **driveItem**.</span><span class="sxs-lookup"><span data-stu-id="3540f-p102">The **driveItem** resource represents a file, folder, or other item stored in a drive. All file system objects in OneDrive and SharePoint are returned as **driveItem** resources.</span></span>

<span data-ttu-id="3540f-107">Hay dos maneras principales de abordar un recurso **driveItem**:</span><span class="sxs-lookup"><span data-stu-id="3540f-107">There are two primary ways of addressing a **driveItem** resource:</span></span>

* <span data-ttu-id="3540f-108">Con el identificador único **driveItem** utilizando `drive/items/{item-id}`</span><span class="sxs-lookup"><span data-stu-id="3540f-108">By the **driveItem** unique identifier using `drive/items/{item-id}`</span></span>
* <span data-ttu-id="3540f-109">Con la ruta de acceso del sistema de archivos utilizando `/drive/root:/path/to/file`</span><span class="sxs-lookup"><span data-stu-id="3540f-109">By file system path using `/drive/root:/path/to/file`</span></span>

<span data-ttu-id="3540f-p103">Los recursos **DriveItem** tienen facetas modeladas como propiedades que proporcionan datos sobre las identidades y las capacidades de driveItem. Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="3540f-p103">**DriveItem** resources have facets modeled as properties that provide data about the driveItem's identities and capabilities. For example:</span></span>

* <span data-ttu-id="3540f-112">Las carpetas tienen una [**faceta folder**][folder].</span><span class="sxs-lookup"><span data-stu-id="3540f-112">Folders have a [**folder facet**][folder]</span></span>
* <span data-ttu-id="3540f-113">Los archivos tienen una [**faceta file**][file].</span><span class="sxs-lookup"><span data-stu-id="3540f-113">Files have a [**file facet**][file].</span></span>
* <span data-ttu-id="3540f-114">Las imágenes tienen una [**faceta image**][image], además de su faceta file.</span><span class="sxs-lookup"><span data-stu-id="3540f-114">Images have an [**image facet**][image] in addition to their file facet.</span></span>
* <span data-ttu-id="3540f-115">Las imágenes tomadas con una cámara (fotos) tienen una [**faceta photo**][photo] que identifica el elemento como una foto. Además, facilita las propiedades que indican cuándo se tomó la foto y con qué dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3540f-115">Images taken with a camera (photos) have a [**photo facet**][photo] that identifies the item as a photo and provides the properties of when the photo was taken and with what device.</span></span>

<span data-ttu-id="3540f-116">Los elementos con una faceta **folder** actúan como contenedores de elementos y, por lo tanto, tienen una referencia `children` que indica una colección de **driveItems** dentro de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="3540f-116">Items with the **folder** facet act as containers of items and therefore have a `children` reference pointing to a collection of **driveItems** under the folder.</span></span>

## <a name="json-representation"></a><span data-ttu-id="3540f-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3540f-117">JSON representation</span></span>

<span data-ttu-id="3540f-118">A continuación se incluye una representación JSON del recurso **driveItem**.</span><span class="sxs-lookup"><span data-stu-id="3540f-118">Here is a JSON representation of a **driveItem** resource.</span></span>

<span data-ttu-id="3540f-119">El recurso **driveItem** deriva de [**baseItem**][baseItem] y hereda las propiedades de ese recurso.</span><span class="sxs-lookup"><span data-stu-id="3540f-119">The **driveItem** resource is derived from [**baseItem**][baseItem] and inherits properties from that resource.</span></span>

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
  "activities": [{"@odata.type": "microsoft.graph.itemActivity"}],
  "content": { "@odata.type": "Edm.Stream" },
  "children": [ { "@odata.type": "microsoft.graph.driveItem" }],
  "permissions": [ {"@odata.type": "microsoft.graph.permission"} ],
  "thumbnails": [ {"@odata.type": "microsoft.graph.thumbnailSet"}],
  "versions": [ {"@odata.type": "Collection(microsoft.graph.driveItemVersion)"}],

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

## <a name="properties"></a><span data-ttu-id="3540f-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3540f-120">Properties</span></span>

| <span data-ttu-id="3540f-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3540f-121">Property</span></span>             | <span data-ttu-id="3540f-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="3540f-122">Type</span></span>               | <span data-ttu-id="3540f-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="3540f-123">Description</span></span>
|:---------------------|:-------------------|:---------------------------------
| <span data-ttu-id="3540f-124">audio</span><span class="sxs-lookup"><span data-stu-id="3540f-124">audio</span></span>                | <span data-ttu-id="3540f-125">[audio][]</span><span class="sxs-lookup"><span data-stu-id="3540f-125">[audio][]</span></span>          | <span data-ttu-id="3540f-p104">Metadatos de audio, si el elemento es un archivo de audio. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p104">Audio metadata, if the item is an audio file. Read-only.</span></span>
| <span data-ttu-id="3540f-128">createdBy</span><span class="sxs-lookup"><span data-stu-id="3540f-128">createdBy</span></span>            | <span data-ttu-id="3540f-129">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="3540f-129">[identitySet][]</span></span>    | <span data-ttu-id="3540f-p105">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p105">Identity of the user, device, and application which created the item. Read-only.</span></span>
| <span data-ttu-id="3540f-132">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="3540f-132">createdDateTime</span></span>      | <span data-ttu-id="3540f-133">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3540f-133">DateTimeOffset</span></span>     | <span data-ttu-id="3540f-p106">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p106">Date and time of item creation. Read-only.</span></span>
| <span data-ttu-id="3540f-136">cTag</span><span class="sxs-lookup"><span data-stu-id="3540f-136">cTag</span></span>                 | <span data-ttu-id="3540f-137">String</span><span class="sxs-lookup"><span data-stu-id="3540f-137">String</span></span>             | <span data-ttu-id="3540f-p107">Un eTag del contenido del elemento. No se cambia este eTag si solo se modifican los metadatos. **Nota** Esta propiedad no se devuelve si el elemento es una carpeta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p107">An eTag for the content of the item. This eTag is not changed if only the metadata is changed. **Note** This property is not returned if the item is a folder. Read-only.</span></span>
| <span data-ttu-id="3540f-142">deleted</span><span class="sxs-lookup"><span data-stu-id="3540f-142">deleted</span></span>              | <span data-ttu-id="3540f-143">[deleted][]</span><span class="sxs-lookup"><span data-stu-id="3540f-143">[deleted][]</span></span>        | <span data-ttu-id="3540f-p108">Información sobre el estado del elemento eliminado. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p108">Information about the deleted state of the item. Read-only.</span></span>
| <span data-ttu-id="3540f-146">description</span><span class="sxs-lookup"><span data-stu-id="3540f-146">description</span></span>          | <span data-ttu-id="3540f-147">Cadena</span><span class="sxs-lookup"><span data-stu-id="3540f-147">String</span></span>             | <span data-ttu-id="3540f-p109">Proporciona una descripción del elemento visible para el usuario. Lectura y escritura. Solo en OneDrive Personal</span><span class="sxs-lookup"><span data-stu-id="3540f-p109">Provides a user-visible description of the item. Read-write. Only on OneDrive Personal</span></span>
| <span data-ttu-id="3540f-151">eTag</span><span class="sxs-lookup"><span data-stu-id="3540f-151">eTag</span></span>                 | <span data-ttu-id="3540f-152">Cadena</span><span class="sxs-lookup"><span data-stu-id="3540f-152">String</span></span>             | <span data-ttu-id="3540f-p110">ETag de todo el elemento (metadatos + contenido). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p110">eTag for the entire item (metadata + content). Read-only.</span></span>
| <span data-ttu-id="3540f-155">file</span><span class="sxs-lookup"><span data-stu-id="3540f-155">file</span></span>                 | <span data-ttu-id="3540f-156">[file][]</span><span class="sxs-lookup"><span data-stu-id="3540f-156">[file][]</span></span>           | <span data-ttu-id="3540f-p111">Metadatos de archivo, si el elemento es un archivo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p111">File metadata, if the item is a file. Read-only.</span></span>
| <span data-ttu-id="3540f-159">fileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="3540f-159">fileSystemInfo</span></span>       | <span data-ttu-id="3540f-160">[fileSystemInfo][]</span><span class="sxs-lookup"><span data-stu-id="3540f-160">[fileSystemInfo][]</span></span> | <span data-ttu-id="3540f-p112">Información del sistema de archivos del cliente. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p112">File system information on client. Read-write.</span></span>
| <span data-ttu-id="3540f-163">folder</span><span class="sxs-lookup"><span data-stu-id="3540f-163">folder</span></span>               | <span data-ttu-id="3540f-164">[folder][]</span><span class="sxs-lookup"><span data-stu-id="3540f-164">[folder][]</span></span>         | <span data-ttu-id="3540f-p113">Metadatos de carpeta, si el elemento es una carpeta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p113">Folder metadata, if the item is a folder. Read-only.</span></span>
| <span data-ttu-id="3540f-167">id</span><span class="sxs-lookup"><span data-stu-id="3540f-167">id</span></span>                   | <span data-ttu-id="3540f-168">Cadena</span><span class="sxs-lookup"><span data-stu-id="3540f-168">String</span></span>             | <span data-ttu-id="3540f-p114">El identificador único del elemento dentro del Drive. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p114">The unique identifier of the item within the Drive. Read-only.</span></span>
| <span data-ttu-id="3540f-171">image</span><span class="sxs-lookup"><span data-stu-id="3540f-171">image</span></span>                | <span data-ttu-id="3540f-172">[image][]</span><span class="sxs-lookup"><span data-stu-id="3540f-172">[image][]</span></span>          | <span data-ttu-id="3540f-p115">Metadatos de imagen, si el elemento es una imagen. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p115">Image metadata, if the item is an image. Read-only.</span></span>
| <span data-ttu-id="3540f-175">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="3540f-175">lastModifiedBy</span></span>       | <span data-ttu-id="3540f-176">[identitySet][]</span><span class="sxs-lookup"><span data-stu-id="3540f-176">[identitySet][]</span></span>    | <span data-ttu-id="3540f-p116">Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p116">Identity of the user, device, and application which last modified the item. Read-only.</span></span>
| <span data-ttu-id="3540f-179">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="3540f-179">lastModifiedDateTime</span></span> | <span data-ttu-id="3540f-180">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3540f-180">DateTimeOffset</span></span>     | <span data-ttu-id="3540f-p117">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p117">Date and time the item was last modified. Read-only.</span></span>
| <span data-ttu-id="3540f-183">location</span><span class="sxs-lookup"><span data-stu-id="3540f-183">location</span></span>             | <span data-ttu-id="3540f-184">[geoCoordinates][]</span><span class="sxs-lookup"><span data-stu-id="3540f-184">[geoCoordinates][]</span></span> | <span data-ttu-id="3540f-p118">Metadatos de ubicación, si el elemento tiene datos de ubicación. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p118">Location metadata, if the item has location data. Read-only.</span></span>
| <span data-ttu-id="3540f-187">name</span><span class="sxs-lookup"><span data-stu-id="3540f-187">name</span></span>                 | <span data-ttu-id="3540f-188">Cadena</span><span class="sxs-lookup"><span data-stu-id="3540f-188">String</span></span>             | <span data-ttu-id="3540f-p119">El nombre del elemento (nombre de archivo y extensión). Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p119">The name of the item (filename and extension). Read-write.</span></span>
| <span data-ttu-id="3540f-191">paquete</span><span class="sxs-lookup"><span data-stu-id="3540f-191">package</span></span>              | <span data-ttu-id="3540f-192">[package][]</span><span class="sxs-lookup"><span data-stu-id="3540f-192">[package][]</span></span>        | <span data-ttu-id="3540f-p120">Si está presente, indica que este elemento es un paquete en lugar de una carpeta o archivo. Los paquetes se tratan como archivos en algunos contextos y como carpetas en otros. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p120">If present, indicates that this item is a package instead of a folder or file. Packages are treated like files in some contexts and folders in others. Read-only.</span></span>
| <span data-ttu-id="3540f-196">parentReference</span><span class="sxs-lookup"><span data-stu-id="3540f-196">parentReference</span></span>      | <span data-ttu-id="3540f-197">[itemReference][]</span><span class="sxs-lookup"><span data-stu-id="3540f-197">[itemReference][]</span></span>  | <span data-ttu-id="3540f-p121">Información primaria, si el elemento tiene un elemento primario. Lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p121">Parent information, if the item has a parent. Read-write.</span></span>
| <span data-ttu-id="3540f-200">photo</span><span class="sxs-lookup"><span data-stu-id="3540f-200">photo</span></span>                | <span data-ttu-id="3540f-201">[photo][]</span><span class="sxs-lookup"><span data-stu-id="3540f-201">[photo][]</span></span>          | <span data-ttu-id="3540f-p122">Metadatos de foto, si el elemento es una foto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p122">Photo metadata, if the item is a photo. Read-only.</span></span>
| <span data-ttu-id="3540f-204">publication</span><span class="sxs-lookup"><span data-stu-id="3540f-204">publication</span></span>          | <span data-ttu-id="3540f-205">[publicationFacet][]</span><span class="sxs-lookup"><span data-stu-id="3540f-205">[publicationFacet][]</span></span> | <span data-ttu-id="3540f-206">Proporciona información sobre el estado publicado o extraído de un elemento, en ubicaciones que admiten esas acciones.</span><span class="sxs-lookup"><span data-stu-id="3540f-206">Provides information about the published or checked-out state of an item, in locations that support such actions.</span></span> <span data-ttu-id="3540f-207">Esta propiedad no se devuelve de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3540f-207">This property is not returned by default.</span></span> <span data-ttu-id="3540f-208">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-208">Read-only.</span></span> |
| <span data-ttu-id="3540f-209">remoteItem</span><span class="sxs-lookup"><span data-stu-id="3540f-209">remoteItem</span></span>           | <span data-ttu-id="3540f-210">[remoteItem][]</span><span class="sxs-lookup"><span data-stu-id="3540f-210">[remoteItem][]</span></span>     | <span data-ttu-id="3540f-p124">Datos de elemento remoto, si el elemento se comparte desde una unidad distinta a la de acceso. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p124">Remote item data, if the item is shared from a drive other than the one being accessed. Read-only.</span></span>
| <span data-ttu-id="3540f-213">root</span><span class="sxs-lookup"><span data-stu-id="3540f-213">root</span></span>                 | <span data-ttu-id="3540f-214">[root][]</span><span class="sxs-lookup"><span data-stu-id="3540f-214">[root][]</span></span>           | <span data-ttu-id="3540f-215">Si esta propiedad no es NULL, indica que el driveItem es el driveItem de nivel superior de la unidad.</span><span class="sxs-lookup"><span data-stu-id="3540f-215">If this property is non-null, it indicates that the driveItem is the top-most driveItem in the drive.</span></span>
| <span data-ttu-id="3540f-216">searchResult</span><span class="sxs-lookup"><span data-stu-id="3540f-216">searchResult</span></span>         | <span data-ttu-id="3540f-217">[searchResult][]</span><span class="sxs-lookup"><span data-stu-id="3540f-217">[searchResult][]</span></span>   | <span data-ttu-id="3540f-p125">Metadatos de búsqueda, si el elemento es un resultado de búsqueda. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p125">Search metadata, if the item is from a search result. Read-only.</span></span>
| <span data-ttu-id="3540f-220">compartido</span><span class="sxs-lookup"><span data-stu-id="3540f-220">shared</span></span>               | <span data-ttu-id="3540f-221">[shared][]</span><span class="sxs-lookup"><span data-stu-id="3540f-221">[shared][]</span></span>         | <span data-ttu-id="3540f-p126">Indica que el elemento se ha compartido con otros usuarios y proporciona información sobre el estado del elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p126">Indicates that the item has been shared with others and provides information about the shared state of the item. Read-only.</span></span>
| <span data-ttu-id="3540f-224">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="3540f-224">sharepointIds</span></span>        | <span data-ttu-id="3540f-225">[sharepointIds][]</span><span class="sxs-lookup"><span data-stu-id="3540f-225">[sharepointIds][]</span></span>  | <span data-ttu-id="3540f-p127">Devuelve los identificadores útiles para la compatibilidad con REST de SharePoint. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p127">Returns identifiers useful for SharePoint REST compatibility. Read-only.</span></span>
| <span data-ttu-id="3540f-228">size</span><span class="sxs-lookup"><span data-stu-id="3540f-228">size</span></span>                 | <span data-ttu-id="3540f-229">Int64</span><span class="sxs-lookup"><span data-stu-id="3540f-229">Int64</span></span>              | <span data-ttu-id="3540f-p128">Tamaño del elemento en bytes. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p128">Size of the item in bytes. Read-only.</span></span>
| <span data-ttu-id="3540f-232">specialFolder</span><span class="sxs-lookup"><span data-stu-id="3540f-232">specialFolder</span></span>        | <span data-ttu-id="3540f-233">[specialFolder][]</span><span class="sxs-lookup"><span data-stu-id="3540f-233">[specialFolder][]</span></span>  | <span data-ttu-id="3540f-p129">Si el elemento actual también está disponible como una carpeta especial, se devuelve esta faceta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p129">If the current item is also available as a special folder, this facet is returned. Read-only.</span></span>
| <span data-ttu-id="3540f-236">video</span><span class="sxs-lookup"><span data-stu-id="3540f-236">video</span></span>                | <span data-ttu-id="3540f-237">[video][]</span><span class="sxs-lookup"><span data-stu-id="3540f-237">[video][]</span></span>          | <span data-ttu-id="3540f-p130">Metadatos de vídeo, si el elemento es un vídeo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p130">Video metadata, if the item is a video. Read-only.</span></span>
| <span data-ttu-id="3540f-240">webDavUrl</span><span class="sxs-lookup"><span data-stu-id="3540f-240">webDavUrl</span></span>            | <span data-ttu-id="3540f-241">Cadena</span><span class="sxs-lookup"><span data-stu-id="3540f-241">String</span></span>             | <span data-ttu-id="3540f-242">Dirección URL compatible con WebDAV del elemento.</span><span class="sxs-lookup"><span data-stu-id="3540f-242">WebDAV compatible URL for the item.</span></span>
| <span data-ttu-id="3540f-243">webUrl</span><span class="sxs-lookup"><span data-stu-id="3540f-243">webUrl</span></span>               | <span data-ttu-id="3540f-244">Cadena</span><span class="sxs-lookup"><span data-stu-id="3540f-244">String</span></span>             | <span data-ttu-id="3540f-p131">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p131">URL that displays the resource in the browser. Read-only.</span></span>

<span data-ttu-id="3540f-p132">**Nota:** Las propiedades eTag y cTag funcionan de forma diferente en los contenedores (carpetas). El valor de cTag se modifica cuando se cambia el contenido o los metadatos de cualquier descendiente de la carpeta. El valor de eTag solo se modifica cuando se cambian las propiedades de la carpeta, excepto las propiedades que derivan de descendientes (como **childCount** o **lastModifiedDateTime**).</span><span class="sxs-lookup"><span data-stu-id="3540f-p132">**Note:** The eTag and cTag properties work differently on containers (folders). The cTag value is modified when content or metadata of any descendant of the folder is changed. The eTag value is only modified when the folder's properties are changed, except for properties that are derived from descendants (like **childCount** or **lastModifiedDateTime**).</span></span>

## <a name="relationships"></a><span data-ttu-id="3540f-250">Relaciones</span><span class="sxs-lookup"><span data-stu-id="3540f-250">Relationships</span></span>

| <span data-ttu-id="3540f-251">Relación</span><span class="sxs-lookup"><span data-stu-id="3540f-251">Relationship</span></span>       | <span data-ttu-id="3540f-252">Tipo</span><span class="sxs-lookup"><span data-stu-id="3540f-252">Type</span></span>                            | <span data-ttu-id="3540f-253">Descripción</span><span class="sxs-lookup"><span data-stu-id="3540f-253">Description</span></span>
|:-------------------|:--------------------------------|:--------------------------
| <span data-ttu-id="3540f-254">activities</span><span class="sxs-lookup"><span data-stu-id="3540f-254">activities</span></span>         | <span data-ttu-id="3540f-255">Colección [itemActivity][]</span><span class="sxs-lookup"><span data-stu-id="3540f-255">[itemActivity][] collection</span></span>     | <span data-ttu-id="3540f-256">Lista de actividades recientes que tuvieron lugar en este elemento.</span><span class="sxs-lookup"><span data-stu-id="3540f-256">The list of recent activities that took place on this item.</span></span>
| <span data-ttu-id="3540f-257">análisis</span><span class="sxs-lookup"><span data-stu-id="3540f-257">analytics</span></span>          | <span data-ttu-id="3540f-258">recursos de [itemAnalytics][]</span><span class="sxs-lookup"><span data-stu-id="3540f-258">[itemAnalytics][] resource</span></span>      | <span data-ttu-id="3540f-259">Análisis acerca de las actividades de vista que tuvieron lugar en este elemento.</span><span class="sxs-lookup"><span data-stu-id="3540f-259">Analytics about the view activities that took place on this item.</span></span>
| <span data-ttu-id="3540f-260">content</span><span class="sxs-lookup"><span data-stu-id="3540f-260">content</span></span>            | <span data-ttu-id="3540f-261">Secuencia</span><span class="sxs-lookup"><span data-stu-id="3540f-261">Stream</span></span>                          | <span data-ttu-id="3540f-262">La secuencia de contenido, si el elemento representa un archivo.</span><span class="sxs-lookup"><span data-stu-id="3540f-262">The content stream, if the item represents a file.</span></span>
| <span data-ttu-id="3540f-263">children</span><span class="sxs-lookup"><span data-stu-id="3540f-263">children</span></span>           | <span data-ttu-id="3540f-264">Colección driveItem</span><span class="sxs-lookup"><span data-stu-id="3540f-264">driveitem collection</span></span>            | <span data-ttu-id="3540f-p133">Colección que contiene objetos Item de los elementos secundarios inmediatos del elemento. Solo los elementos que representan carpetas tienen elementos secundarios. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="3540f-p133">Collection containing Item objects for the immediate children of Item. Only items representing folders have children. Read-only. Nullable.</span></span>
| <span data-ttu-id="3540f-269">listItem</span><span class="sxs-lookup"><span data-stu-id="3540f-269">listItem</span></span>           | <span data-ttu-id="3540f-270">[listItem][]</span><span class="sxs-lookup"><span data-stu-id="3540f-270">[listItem][]</span></span>                    | <span data-ttu-id="3540f-271">Para las unidades en SharePoint, el elemento de lista de biblioteca de documentos asociada.</span><span class="sxs-lookup"><span data-stu-id="3540f-271">For drives in SharePoint, the associated document library list item.</span></span> <span data-ttu-id="3540f-272">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-272">Read-only.</span></span> <span data-ttu-id="3540f-273">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="3540f-273">Nullable.</span></span>
| <span data-ttu-id="3540f-274">permissions</span><span class="sxs-lookup"><span data-stu-id="3540f-274">permissions</span></span>        | <span data-ttu-id="3540f-275">Colección [permission][]</span><span class="sxs-lookup"><span data-stu-id="3540f-275">[permission][] collection</span></span>       | <span data-ttu-id="3540f-p135">El conjunto de permisos del elemento. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="3540f-p135">The set of permissions for the item. Read-only. Nullable.</span></span>
| <span data-ttu-id="3540f-279">miniaturas</span><span class="sxs-lookup"><span data-stu-id="3540f-279">thumbnails</span></span>         | <span data-ttu-id="3540f-280">Colección [thumbnailSet][]</span><span class="sxs-lookup"><span data-stu-id="3540f-280">[thumbnailSet][] collection</span></span>     | <span data-ttu-id="3540f-p136">Colección que contiene objetos [ThumbnailSet][] asociados al elemento. Para obtener más información, consulte [obtener miniaturas][]. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="3540f-p136">Collection containing [ThumbnailSet][] objects associated with the item. For more info, see [getting thumbnails][]. Read-only. Nullable.</span></span>
| <span data-ttu-id="3540f-285">versiones</span><span class="sxs-lookup"><span data-stu-id="3540f-285">versions</span></span>           | <span data-ttu-id="3540f-286">colección de [driveItemVersion][]</span><span class="sxs-lookup"><span data-stu-id="3540f-286">[driveItemVersion][] collection</span></span> | <span data-ttu-id="3540f-287">La lista de las versiones anteriores del elemento.</span><span class="sxs-lookup"><span data-stu-id="3540f-287">The list of previous versions of the item.</span></span> <span data-ttu-id="3540f-288">Para obtener más información, vea [Introducción a las versiones anteriores][].</span><span class="sxs-lookup"><span data-stu-id="3540f-288">For more info, see [getting previous versions][].</span></span> <span data-ttu-id="3540f-289">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-289">Read-only.</span></span> <span data-ttu-id="3540f-290">Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="3540f-290">Nullable.</span></span>

## <a name="instance-attributes"></a><span data-ttu-id="3540f-291">Atributos de instancia</span><span class="sxs-lookup"><span data-stu-id="3540f-291">Instance Attributes</span></span>

<span data-ttu-id="3540f-p138">Los atributos de instancia son propiedades con comportamientos especiales. Estas propiedades son temporales y o bien a) definen el comportamiento que debería tener el servicio o b) proporcionan valores de propiedad a corto plazo, como una dirección URL de descarga de un elemento que expira.</span><span class="sxs-lookup"><span data-stu-id="3540f-p138">Instance attributes are properties with special behaviors. These properties are temporary and either a) define behavior the service should perform or b) provide short-term property values, like a download URL for an item that expires.</span></span>

| <span data-ttu-id="3540f-294">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="3540f-294">Property name</span></span>                     | <span data-ttu-id="3540f-295">Tipo</span><span class="sxs-lookup"><span data-stu-id="3540f-295">Type</span></span>   | <span data-ttu-id="3540f-296">Descripción</span><span class="sxs-lookup"><span data-stu-id="3540f-296">Description</span></span>
|:----------------------------------|:-------|:--------------------------------
| <span data-ttu-id="3540f-297">@microsoft.graph.conflictBehavior</span><span class="sxs-lookup"><span data-stu-id="3540f-297">@microsoft.graph.conflictBehavior</span></span> | <span data-ttu-id="3540f-298">string</span><span class="sxs-lookup"><span data-stu-id="3540f-298">string</span></span> | <span data-ttu-id="3540f-p139">El comportamiento de resolución de conflictos para las acciones que crean un nuevo elemento. Puede utilizar los valores de *fail*, *replace*, o *rename*. El valor predeterminado de PUT es *replace*. Nunca se devuelve un elemento con esta anotación. Solo escritura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p139">The conflict resolution behavior for actions that create a new item. You can use the values *fail*, *replace*, or *rename*. The default for PUT is *replace*. An item will never be returned with this annotation. Write-only.</span></span>
| <span data-ttu-id="3540f-304">@microsoft.graph.downloadUrl</span><span class="sxs-lookup"><span data-stu-id="3540f-304">@microsoft.graph.downloadUrl</span></span>      | <span data-ttu-id="3540f-305">string</span><span class="sxs-lookup"><span data-stu-id="3540f-305">string</span></span> | <span data-ttu-id="3540f-p140">Una dirección URL que puede utilizarse para descargar el contenido de este archivo. No es necesaria la autenticación con esta dirección URL. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p140">A URL that can be used to download this file's content. Authentication is not required with this URL. Read-only.</span></span>
| <span data-ttu-id="3540f-309">@microsoft.graph.sourceUrl</span><span class="sxs-lookup"><span data-stu-id="3540f-309">@microsoft.graph.sourceUrl</span></span>        | <span data-ttu-id="3540f-310">string</span><span class="sxs-lookup"><span data-stu-id="3540f-310">string</span></span> | <span data-ttu-id="3540f-p141">Al emitir una solicitud PUT, esta anotación de instancia puede utilizarse para indicar al servicio que descargue el contenido de la dirección URL y lo guarde como el archivo. Solo escritura.</span><span class="sxs-lookup"><span data-stu-id="3540f-p141">When issuing a PUT request, this instance annotation can be used to instruct the service to download the contents of the URL, and store it as the file. Write-only.</span></span>

<span data-ttu-id="3540f-313">**Nota:** El valor de @microsoft.graph.downloadUrl es una dirección URL de corta duración y no se puede almacenar en caché.</span><span class="sxs-lookup"><span data-stu-id="3540f-313">**Note:** The @microsoft.graph.downloadUrl value is a short-lived URL and can't be cached.</span></span>
<span data-ttu-id="3540f-314">La dirección URL sólo estará disponible durante un breve período de tiempo (1 hora) antes de se haya invalidado.</span><span class="sxs-lookup"><span data-stu-id="3540f-314">The URL will only be available for a short period of time (1 hour) before it is invalidated.</span></span> <span data-ttu-id="3540f-315">Quitar permisos de archivo para un usuario no puede invalidar inmediatamente la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="3540f-315">Removing file permissions for a user may not immediately invalidate the URL.</span></span>

## <a name="methods"></a><span data-ttu-id="3540f-316">Métodos</span><span class="sxs-lookup"><span data-stu-id="3540f-316">Methods</span></span>

| <span data-ttu-id="3540f-317">Método</span><span class="sxs-lookup"><span data-stu-id="3540f-317">Method</span></span>                                                   | <span data-ttu-id="3540f-318">Ruta de acceso a REST</span><span class="sxs-lookup"><span data-stu-id="3540f-318">REST Path</span></span>
|:---------------------------------------------------------|:------------------
| [<span data-ttu-id="3540f-319">Obtener elemento</span><span class="sxs-lookup"><span data-stu-id="3540f-319">Get item</span></span>](../api/driveitem-get.md)                      | `GET /drive/items/{item-id}`
| [<span data-ttu-id="3540f-320">Enumerar actividades</span><span class="sxs-lookup"><span data-stu-id="3540f-320">List activities</span></span>](../api/activities-list.md)             | `GET /drive/items/{item-id}/activities`
| <span data-ttu-id="3540f-321">[Obtener análisis][]</span><span class="sxs-lookup"><span data-stu-id="3540f-321">[Get analytics][]</span></span>                                        | `GET /drive/items/{item-id}/analytics`
| <span data-ttu-id="3540f-322">[Obtener las actividades por intervalo][]</span><span class="sxs-lookup"><span data-stu-id="3540f-322">[Get activities by interval][]</span></span>                           | `GET /drive/items/{item-id}/getActivitiesByInterval`
| [<span data-ttu-id="3540f-323">Enumerar elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3540f-323">List children</span></span>](../api/driveitem-list-children.md)       | `GET /drive/items/{item-id}/children`
| [<span data-ttu-id="3540f-324">Enumerar versiones</span><span class="sxs-lookup"><span data-stu-id="3540f-324">List versions</span></span>](../api/driveitem-list-versions.md)       | `GET /drive/items/{item-id}/versions`
| [<span data-ttu-id="3540f-325">Crear elemento</span><span class="sxs-lookup"><span data-stu-id="3540f-325">Create item</span></span>](../api/driveitem-post-children.md)         | `POST /drive/items/{item-id}/children`
| [<span data-ttu-id="3540f-326">Actualizar elemento</span><span class="sxs-lookup"><span data-stu-id="3540f-326">Update item</span></span>](../api/driveitem-update.md)                | `PATCH /drive/items/{item-id}`
| [<span data-ttu-id="3540f-327">Cargar contenido</span><span class="sxs-lookup"><span data-stu-id="3540f-327">Upload content</span></span>](../api/driveitem-put-content.md)        | `PUT /drive/items/{item-id}/content`
| [<span data-ttu-id="3540f-328">Descargar contenido</span><span class="sxs-lookup"><span data-stu-id="3540f-328">Download content</span></span>](../api/driveitem-get-content.md)      | `GET /drive/items/{item-id}/content`
| <span data-ttu-id="3540f-329">[Descargar el formato de archivo específico][download-format]</span><span class="sxs-lookup"><span data-stu-id="3540f-329">[Download specific file format][download-format]</span></span>         | `GET /drive/items/{item-id}/content?format={format}`
| [<span data-ttu-id="3540f-330">Eliminar elemento</span><span class="sxs-lookup"><span data-stu-id="3540f-330">Delete item</span></span>](../api/driveitem-delete.md)                | `DELETE /drive/items/{item-id}`
| [<span data-ttu-id="3540f-331">Mover elemento</span><span class="sxs-lookup"><span data-stu-id="3540f-331">Move item</span></span>](../api/driveitem-move.md)                    | `PATCH /drive/items/{item-id}`
| [<span data-ttu-id="3540f-332">Copiar elemento</span><span class="sxs-lookup"><span data-stu-id="3540f-332">Copy item</span></span>](../api/driveitem-copy.md)                    | `POST /drive/items/{item-id}/copy`
| [<span data-ttu-id="3540f-333">Buscar elementos</span><span class="sxs-lookup"><span data-stu-id="3540f-333">Search items</span></span>](../api/driveitem-search.md)               | `GET /drive/items/{item-id}/search(q='text')`
| [<span data-ttu-id="3540f-334">Enumerar cambios en una unidad</span><span class="sxs-lookup"><span data-stu-id="3540f-334">List changes in a drive</span></span>](../api/driveitem-delta.md)     | `GET /drive/root/delta`
| [<span data-ttu-id="3540f-335">Enumerar miniaturas</span><span class="sxs-lookup"><span data-stu-id="3540f-335">List thumbnails</span></span>](../api/driveitem-list-thumbnails.md)   | `GET /drive/items/{item-id}/thumbnails`
| [<span data-ttu-id="3540f-336">Crear vínculo para compartir</span><span class="sxs-lookup"><span data-stu-id="3540f-336">Create sharing link</span></span>](../api/driveitem-createlink.md)    | `POST /drive/items/{item-id}/createLink`
| [<span data-ttu-id="3540f-337">Agregar permisos</span><span class="sxs-lookup"><span data-stu-id="3540f-337">Add permissions</span></span>](../api/driveitem-invite.md)            | `POST /drive/items/{item-id}/invite`
| [<span data-ttu-id="3540f-338">Enumerar permisos</span><span class="sxs-lookup"><span data-stu-id="3540f-338">List permissions</span></span>](../api/driveitem-list-permissions.md) | `GET /drive/items/{item-id}/permissions`
| [<span data-ttu-id="3540f-339">Eliminar permiso</span><span class="sxs-lookup"><span data-stu-id="3540f-339">Delete permission</span></span>](../api/permission-delete.md)         | `DELETE /drive/items/{item-id}/permissions/{perm-id}`
| <span data-ttu-id="3540f-340">[Obtener WebSocket canal][getWebSocket]</span><span class="sxs-lookup"><span data-stu-id="3540f-340">[Get WebSocket channel][getWebSocket]</span></span>                    | `GET /drive/root/subscriptions/socketIo`
| <span data-ttu-id="3540f-341">[Vista previa del artículo][item-preview]</span><span class="sxs-lookup"><span data-stu-id="3540f-341">[Preview item][item-preview]</span></span>                             | `POST /drive/items/{item-id}/preview`

[item-preview]: ../api/driveitem-preview.md
[Obtener análisis]: ../api/itemanalytics-get.md
[Get analytics]: ../api/itemanalytics-get.md
[Obtener las actividades por intervalo]: ../api/itemactivity-getbyinterval.md
[Get activities by interval]: ../api/itemactivity-getbyinterval.md

## <a name="remarks"></a><span data-ttu-id="3540f-344">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3540f-344">Remarks</span></span>

<span data-ttu-id="3540f-345">En las bibliotecas de documentos de OneDrive para la Empresa o SharePoint, no se devuelve la propiedad **cTag** si **driveItem** tiene una faceta [folder][].</span><span class="sxs-lookup"><span data-stu-id="3540f-345">In OneDrive for Business or SharePoint document libraries, the **cTag** property is not returned, if the **driveItem** has a [folder][] facet.</span></span>

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
[getWebSocket]: ../api/driveitem-subscriptions-socketio.md
[identitySet]: identityset.md
[image]: image.md
[itemActivity]: itemactivity.md
[itemAnalytics]: itemanalytics.md
[itemReference]: itemreference.md
[geoCoordinates]: geocoordinates.md
[List activities]: ../api/activities-list.md
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
[user]: https://developer.microsoft.com/graph/docs/api-reference/v1.0/resources/users
[publicationFacet]: publicationfacet.md

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Item is the main data model in the OneDrive API. Everything is an item.",
  "keywords": "item,facet,resource",
  "section": "documentation",
  "tocPath": "Items",
  "tocBookmarks": { "Resources/Item": "#" }
} -->
