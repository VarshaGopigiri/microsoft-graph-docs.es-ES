---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: RemoteItem
ms.openlocfilehash: fd324460b3486f90c342feb1c782c0cf74d77416
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="remoteitem-resource-type"></a><span data-ttu-id="09df7-102">Tipo de recurso RemoteItem</span><span class="sxs-lookup"><span data-stu-id="09df7-102">RemoteItem resource type</span></span>

<span data-ttu-id="09df7-103">El recurso **remoteItem** indica que un objeto [**driveItem**](driveitem.md) hace referencia a un elemento que existe en otra unidad.</span><span class="sxs-lookup"><span data-stu-id="09df7-103">The **remoteItem** resource indicates that a [**driveItem**](driveitem.md) references an item that exists in another drive. This resource provides the unique IDs of the source drive and target item.</span></span>
<span data-ttu-id="09df7-104">Este recurso proporciona los identificadores únicos de la unidad de origen y del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="09df7-104">The remoteItem resource indicates that a driveItem references an item that exists in another drive. This resource provides the unique IDs of the source drive and target item.</span></span>

<span data-ttu-id="09df7-105">Los objetos [**DriveItem**](driveitem.md) con una faceta **remoteItem** que no sea null son recursos que se comparten, agregan al OneDrive del usuario o que están en elementos devueltos de colecciones heterogéneas de elementos (como los resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="09df7-105">[**DriveItems**](driveitem.md) with a non-null **remoteItem** facet are resources that are shared, added to the user's OneDrive, or on items returned from hetrogenous collections of items (like search results).</span></span>

<span data-ttu-id="09df7-106">**Nota:** A diferencia de las carpetas de la misma unidad, puede que a un objeto **driveItem** que se mueva a un elemento remoto se le cambie el valor `id`.</span><span class="sxs-lookup"><span data-stu-id="09df7-106">**Note:** Unlike with folders in the same drive, a **driveItem** moved into a remote item may have its `id` value changed.</span></span>

## <a name="json-representation"></a><span data-ttu-id="09df7-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="09df7-107">JSON representation</span></span>

<!-- { "blockType": "resource", 
       "@odata.type": "microsoft.graph.remoteItem", 
       "optionalProperties": ["name", "fileSystemInfo", "file", "folder"] } -->

```json
{
  "id": "string",
  "createdBy": { "@odata.type": "microsoft.graph.identitySet" },
  "createdDateTime": "timestamp",
  "file": { "@odata.type": "microsoft.graph.file" },
  "fileSystemInfo": { "@odata.type": "microsoft.graph.fileSystemInfo" },
  "folder": { "@odata.type": "microsoft.graph.folder" },
  "lastModifiedBy": { "@odata.type": "microsoft.graph.identitySet" },
  "lastModifiedDateTime": "timestamp",
  "name": "string",
  "package": { "@odata.type": "microsoft.graph.package" },
  "parentReference": { "@odata.type": "microsoft.graph.itemReference" },
  "shared": { "@odata.type": "microsoft.graph.shared" },
  "sharepointIds": { "@odata.type": "microsoft.graph.sharepointIds" },
  "size": 1024,
  "webDavUrl": "url",
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="09df7-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09df7-108">Properties</span></span>

| <span data-ttu-id="09df7-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="09df7-109">Property name</span></span>        | <span data-ttu-id="09df7-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="09df7-110">Type</span></span>                                | <span data-ttu-id="09df7-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="09df7-111">Description</span></span>                                                                                                                                                       |
| :------------------- | :---------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="09df7-112">createdBy</span><span class="sxs-lookup"><span data-stu-id="09df7-112">createdBy</span></span>            | [<span data-ttu-id="09df7-113">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="09df7-113">identitySet</span></span>](identityset.md)       | <span data-ttu-id="09df7-p102">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p102">Identity of the user, device, and application which created the item. Read-only.</span></span>                                                                                  |
| <span data-ttu-id="09df7-116">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="09df7-116">createdDateTime</span></span>      | <span data-ttu-id="09df7-117">Timestamp</span><span class="sxs-lookup"><span data-stu-id="09df7-117">Timestamp</span></span>                           | <span data-ttu-id="09df7-p103">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p103">Date and time of item creation. Read-only.</span></span>                                                                                                                        |
| <span data-ttu-id="09df7-120">file</span><span class="sxs-lookup"><span data-stu-id="09df7-120">file</span></span>                 | [<span data-ttu-id="09df7-121">File</span><span class="sxs-lookup"><span data-stu-id="09df7-121">File</span></span>](file.md)                     | <span data-ttu-id="09df7-p104">Indica que el elemento remoto es un archivo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p104">Indicates that the remote item is a file. Read-only.</span></span>                                                                                                              |
| <span data-ttu-id="09df7-124">fileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="09df7-124">fileSystemInfo</span></span>       | [<span data-ttu-id="09df7-125">FileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="09df7-125">FileSystemInfo</span></span>](filesysteminfo.md) | <span data-ttu-id="09df7-p105">Información sobre el elemento remoto del sistema de archivos local. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p105">Information about the remote item from the local file system. Read-only.</span></span>                                                                                          |
| <span data-ttu-id="09df7-128">folder</span><span class="sxs-lookup"><span data-stu-id="09df7-128">folder</span></span>               | [<span data-ttu-id="09df7-129">Folder</span><span class="sxs-lookup"><span data-stu-id="09df7-129">Folder</span></span>](folder.md)                 | <span data-ttu-id="09df7-p106">Indica que el elemento remoto es una carpeta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p106">Indicates that the remote item is a folder. Read-only.</span></span>                                                                                                            |
| <span data-ttu-id="09df7-132">id</span><span class="sxs-lookup"><span data-stu-id="09df7-132">id</span></span>                   | <span data-ttu-id="09df7-133">String</span><span class="sxs-lookup"><span data-stu-id="09df7-133">String</span></span>                              | <span data-ttu-id="09df7-p107">Identificador único del elemento remoto en su unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p107">Unique identifier for the remote item in its drive. Read-only.</span></span>                                                                                                    |
| <span data-ttu-id="09df7-136">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="09df7-136">lastModifiedBy</span></span>       | [<span data-ttu-id="09df7-137">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="09df7-137">identitySet</span></span>](identityset.md)       | <span data-ttu-id="09df7-p108">Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p108">Identity of the user, device, and application which last modified the item. Read-only.</span></span>                                                                            |
| <span data-ttu-id="09df7-140">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="09df7-140">lastModifiedDateTime</span></span> | <span data-ttu-id="09df7-141">Timestamp</span><span class="sxs-lookup"><span data-stu-id="09df7-141">Timestamp</span></span>                           | <span data-ttu-id="09df7-p109">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p109">Date and time the item was last modified. Read-only.</span></span>                                                                                                              |
| <span data-ttu-id="09df7-144">name</span><span class="sxs-lookup"><span data-stu-id="09df7-144">name</span></span>                 | <span data-ttu-id="09df7-145">String</span><span class="sxs-lookup"><span data-stu-id="09df7-145">String</span></span>                              | <span data-ttu-id="09df7-p110">Opcional. Nombre de archivo del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p110">Optional. Filename of the remote item. Read-only.</span></span>                                                                                                                 |
| <span data-ttu-id="09df7-149">package</span><span class="sxs-lookup"><span data-stu-id="09df7-149">package</span></span>              | [<span data-ttu-id="09df7-150">Package</span><span class="sxs-lookup"><span data-stu-id="09df7-150">package</span></span>](package.md)               | <span data-ttu-id="09df7-p111">Si está presente, indica que este elemento es un paquete en lugar de una carpeta o archivo. Los paquetes se tratan como archivos en algunos contextos y como carpetas en otros. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p111">If present, indicates that this item is a package instead of a folder or file. Packages are treated like files in some contexts and folders in others. Read-only.</span></span> |
| <span data-ttu-id="09df7-154">parentReference</span><span class="sxs-lookup"><span data-stu-id="09df7-154">parentReference</span></span>      | [<span data-ttu-id="09df7-155">ItemReference</span><span class="sxs-lookup"><span data-stu-id="09df7-155">ItemReference</span></span>](itemreference.md)   | <span data-ttu-id="09df7-p112">Propiedades del elemento primario del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p112">Properties of the parent of the remote item. Read-only.</span></span>                                                                                                           |
| <span data-ttu-id="09df7-158">shared</span><span class="sxs-lookup"><span data-stu-id="09df7-158">shared</span></span>               | [<span data-ttu-id="09df7-159">shared</span><span class="sxs-lookup"><span data-stu-id="09df7-159">shared</span></span>](shared.md)                 | <span data-ttu-id="09df7-p113">Indica que el elemento se ha compartido con otros usuarios y proporciona información sobre el estado del elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p113">Indicates that the item has been shared with others and provides information about the shared state of the item. Read-only.</span></span>                                       |
| <span data-ttu-id="09df7-162">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="09df7-162">sharepointIds</span></span>        | [<span data-ttu-id="09df7-163">SharepointIds</span><span class="sxs-lookup"><span data-stu-id="09df7-163">SharepointIds</span></span>](sharepointids.md)   | <span data-ttu-id="09df7-p114">Proporciona interoperabilidad entre elementos de OneDrive para la Empresa y SharePoint con el conjunto completo de identificadores de elementos. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p114">Provides interop between items in OneDrive for Business and SharePoint with the full set of item identifiers. Read-only.</span></span>                                          |
| <span data-ttu-id="09df7-166">size</span><span class="sxs-lookup"><span data-stu-id="09df7-166">size</span></span>                 | <span data-ttu-id="09df7-167">Int64</span><span class="sxs-lookup"><span data-stu-id="09df7-167">Int64</span></span>                               | <span data-ttu-id="09df7-p115">Tamaño del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p115">Size of the remote item. Read-only.</span></span>                                                                                                                               |
| <span data-ttu-id="09df7-170">webDavUrl</span><span class="sxs-lookup"><span data-stu-id="09df7-170">webDavUrl</span></span>            | <span data-ttu-id="09df7-171">Url</span><span class="sxs-lookup"><span data-stu-id="09df7-171">Url</span></span>                                 | <span data-ttu-id="09df7-172">Dirección URL compatible con DAV del elemento.</span><span class="sxs-lookup"><span data-stu-id="09df7-172">DAV compatible URL for the item.</span></span>                                                                                                                                  |
| <span data-ttu-id="09df7-173">webUrl</span><span class="sxs-lookup"><span data-stu-id="09df7-173">webUrl</span></span>               | <span data-ttu-id="09df7-174">Url</span><span class="sxs-lookup"><span data-stu-id="09df7-174">Url</span></span>                                 | <span data-ttu-id="09df7-p116">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="09df7-p116">URL that displays the resource in the browser. Read-only.</span></span>                                                                                                         |

## <a name="remarks"></a><span data-ttu-id="09df7-177">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09df7-177">Remarks</span></span>

<span data-ttu-id="09df7-178">Para obtener más información sobre las facetas de un objeto **driveItem**, consulte [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="09df7-178">For more information about the facets on a DriveItem, see **DriveItem**.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The quota facet provides information about how much space the OneDrive has available.",
  "keywords": "quota,available,remaining,used",
  "section": "documentation",
  "tocPath": "Facets/RemoteItem"
} -->