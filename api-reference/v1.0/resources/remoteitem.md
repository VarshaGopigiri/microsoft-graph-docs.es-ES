---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: RemoteItem
localization_priority: Normal
ms.openlocfilehash: 0b29ba14273bad7306518c290029a9ebc444f07d
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888091"
---
# <a name="remoteitem-resource-type"></a><span data-ttu-id="8e0ea-102">Tipo de recurso RemoteItem</span><span class="sxs-lookup"><span data-stu-id="8e0ea-102">RemoteItem resource type</span></span>

<span data-ttu-id="8e0ea-p101">El recurso **remoteItem** indica que un objeto [**driveItem**](driveitem.md) hace referencia a un elemento que existe en otra unidad. Este recurso proporciona los identificadores únicos de la unidad de origen y del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p101">The **remoteItem** resource indicates that a [**driveItem**](driveitem.md) references an item that exists in another drive. This resource provides the unique IDs of the source drive and target item.</span></span>

<span data-ttu-id="8e0ea-105">Los objetos [**DriveItem**](driveitem.md) con una faceta **remoteItem** que no sea null son recursos que se comparten, agregan al OneDrive del usuario o que están en elementos devueltos de colecciones heterogéneas de elementos (como los resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="8e0ea-105">[**DriveItems**](driveitem.md) with a non-null **remoteItem** facet are resources that are shared, added to the user's OneDrive, or on items returned from hetrogenous collections of items (like search results).</span></span>

<span data-ttu-id="8e0ea-106">**Nota:** A diferencia de las carpetas de la misma unidad, puede que a un objeto **driveItem** que se mueva a un elemento remoto se le cambie el valor `id`.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-106">**Note:** Unlike with folders in the same drive, a **driveItem** moved into a remote item may have its `id` value changed.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8e0ea-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8e0ea-107">JSON representation</span></span>

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
  "specialFolder": { "@odata.type": "microsoft.graph.specialFolder" },
  "size": 1024,
  "webDavUrl": "url",
  "webUrl": "url"
}
```

## <a name="properties"></a><span data-ttu-id="8e0ea-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8e0ea-108">Properties</span></span>

| <span data-ttu-id="8e0ea-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="8e0ea-109">Property name</span></span>        | <span data-ttu-id="8e0ea-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="8e0ea-110">Type</span></span>                                | <span data-ttu-id="8e0ea-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="8e0ea-111">Description</span></span>                                                                                                                                                       |
| :------------------- | :---------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="8e0ea-112">createdBy</span><span class="sxs-lookup"><span data-stu-id="8e0ea-112">createdBy</span></span>            | [<span data-ttu-id="8e0ea-113">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="8e0ea-113">IdentitySet</span></span>](identityset.md)       | <span data-ttu-id="8e0ea-p102">Identidad del usuario, el dispositivo y la aplicación que ha creado el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p102">Identity of the user, device, and application which created the item. Read-only.</span></span>                                                                                  |
| <span data-ttu-id="8e0ea-116">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="8e0ea-116">createdDateTime</span></span>      | <span data-ttu-id="8e0ea-117">Timestamp</span><span class="sxs-lookup"><span data-stu-id="8e0ea-117">Timestamp</span></span>                           | <span data-ttu-id="8e0ea-p103">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p103">Date and time of item creation. Read-only.</span></span>                                                                                                                        |
| <span data-ttu-id="8e0ea-120">archivo</span><span class="sxs-lookup"><span data-stu-id="8e0ea-120">file</span></span>                 | [<span data-ttu-id="8e0ea-121">File</span><span class="sxs-lookup"><span data-stu-id="8e0ea-121">File</span></span>](file.md)                     | <span data-ttu-id="8e0ea-p104">Indica que el elemento remoto es un archivo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p104">Indicates that the remote item is a file. Read-only.</span></span>                                                                                                              |
| <span data-ttu-id="8e0ea-124">fileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="8e0ea-124">fileSystemInfo</span></span>       | [<span data-ttu-id="8e0ea-125">FileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="8e0ea-125">FileSystemInfo</span></span>](filesysteminfo.md) | <span data-ttu-id="8e0ea-p105">Información sobre el elemento remoto del sistema de archivos local. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p105">Information about the remote item from the local file system. Read-only.</span></span>                                                                                          |
| <span data-ttu-id="8e0ea-128">folder</span><span class="sxs-lookup"><span data-stu-id="8e0ea-128">folder</span></span>               | [<span data-ttu-id="8e0ea-129">Folder</span><span class="sxs-lookup"><span data-stu-id="8e0ea-129">Folder</span></span>](folder.md)                 | <span data-ttu-id="8e0ea-p106">Indica que el elemento remoto es una carpeta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p106">Indicates that the remote item is a folder. Read-only.</span></span>                                                                                                            |
| <span data-ttu-id="8e0ea-132">id</span><span class="sxs-lookup"><span data-stu-id="8e0ea-132">id</span></span>                   | <span data-ttu-id="8e0ea-133">String</span><span class="sxs-lookup"><span data-stu-id="8e0ea-133">String</span></span>                              | <span data-ttu-id="8e0ea-p107">Identificador único del elemento remoto en su unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p107">Unique identifier for the remote item in its drive. Read-only.</span></span>                                                                                                    |
| <span data-ttu-id="8e0ea-136">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="8e0ea-136">lastModifiedBy</span></span>       | [<span data-ttu-id="8e0ea-137">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="8e0ea-137">IdentitySet</span></span>](identityset.md)       | <span data-ttu-id="8e0ea-p108">Identidad del usuario, el dispositivo y la aplicación que ha modificado por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p108">Identity of the user, device, and application which last modified the item. Read-only.</span></span>                                                                            |
| <span data-ttu-id="8e0ea-140">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="8e0ea-140">lastModifiedDateTime</span></span> | <span data-ttu-id="8e0ea-141">Timestamp</span><span class="sxs-lookup"><span data-stu-id="8e0ea-141">Timestamp</span></span>                           | <span data-ttu-id="8e0ea-p109">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p109">Date and time the item was last modified. Read-only.</span></span>                                                                                                              |
| <span data-ttu-id="8e0ea-144">name</span><span class="sxs-lookup"><span data-stu-id="8e0ea-144">name</span></span>                 | <span data-ttu-id="8e0ea-145">String</span><span class="sxs-lookup"><span data-stu-id="8e0ea-145">String</span></span>                              | <span data-ttu-id="8e0ea-p110">Opcional. Nombre de archivo del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p110">Optional. Filename of the remote item. Read-only.</span></span>                                                                                                                 |
| <span data-ttu-id="8e0ea-149">paquete</span><span class="sxs-lookup"><span data-stu-id="8e0ea-149">package</span></span>              | [<span data-ttu-id="8e0ea-150">Package</span><span class="sxs-lookup"><span data-stu-id="8e0ea-150">Package</span></span>](package.md)               | <span data-ttu-id="8e0ea-p111">Si está presente, indica que este elemento es un paquete en lugar de una carpeta o archivo. Los paquetes se tratan como archivos en algunos contextos y como carpetas en otros. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p111">If present, indicates that this item is a package instead of a folder or file. Packages are treated like files in some contexts and folders in others. Read-only.</span></span> |
| <span data-ttu-id="8e0ea-154">parentReference</span><span class="sxs-lookup"><span data-stu-id="8e0ea-154">parentReference</span></span>      | [<span data-ttu-id="8e0ea-155">ItemReference</span><span class="sxs-lookup"><span data-stu-id="8e0ea-155">ItemReference</span></span>](itemreference.md)   | <span data-ttu-id="8e0ea-p112">Propiedades del elemento primario del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p112">Properties of the parent of the remote item. Read-only.</span></span>                                                                                                           |
| <span data-ttu-id="8e0ea-158">shared</span><span class="sxs-lookup"><span data-stu-id="8e0ea-158">shared</span></span>               | [<span data-ttu-id="8e0ea-159">shared</span><span class="sxs-lookup"><span data-stu-id="8e0ea-159">shared</span></span>](shared.md)                 | <span data-ttu-id="8e0ea-p113">Indica que el elemento se ha compartido con otros usuarios y proporciona información sobre el estado del elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p113">Indicates that the item has been shared with others and provides information about the shared state of the item. Read-only.</span></span>                                       |
| <span data-ttu-id="8e0ea-162">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="8e0ea-162">sharepointIds</span></span>        | [<span data-ttu-id="8e0ea-163">SharepointIds</span><span class="sxs-lookup"><span data-stu-id="8e0ea-163">SharepointIds</span></span>](sharepointids.md)   | <span data-ttu-id="8e0ea-p114">Proporciona interoperabilidad entre elementos de OneDrive para la Empresa y SharePoint con el conjunto completo de identificadores de elementos. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p114">Provides interop between items in OneDrive for Business and SharePoint with the full set of item identifiers. Read-only.</span></span>                                          |
| <span data-ttu-id="8e0ea-166">size</span><span class="sxs-lookup"><span data-stu-id="8e0ea-166">size</span></span>                 | <span data-ttu-id="8e0ea-167">Int64</span><span class="sxs-lookup"><span data-stu-id="8e0ea-167">Int64</span></span>                               | <span data-ttu-id="8e0ea-p115">Tamaño del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p115">Size of the remote item. Read-only.</span></span>                                                                                                                               |
| <span data-ttu-id="8e0ea-170">specialFolder</span><span class="sxs-lookup"><span data-stu-id="8e0ea-170">specialFolder</span></span>        | <span data-ttu-id="8e0ea-171">[specialFolder][]</span><span class="sxs-lookup"><span data-stu-id="8e0ea-171">[specialFolder][]</span></span>                   | <span data-ttu-id="8e0ea-p116">Si el elemento actual también está disponible como una carpeta especial, se devuelve esta faceta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p116">If the current item is also available as a special folder, this facet is returned. Read-only.</span></span>                                                                     |
| <span data-ttu-id="8e0ea-174">webDavUrl</span><span class="sxs-lookup"><span data-stu-id="8e0ea-174">webDavUrl</span></span>            | <span data-ttu-id="8e0ea-175">Url</span><span class="sxs-lookup"><span data-stu-id="8e0ea-175">Url</span></span>                                 | <span data-ttu-id="8e0ea-176">Dirección URL compatible con DAV del elemento.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-176">DAV compatible URL for the item.</span></span>                                                                                                                                  |
| <span data-ttu-id="8e0ea-177">webUrl</span><span class="sxs-lookup"><span data-stu-id="8e0ea-177">webUrl</span></span>               | <span data-ttu-id="8e0ea-178">Url</span><span class="sxs-lookup"><span data-stu-id="8e0ea-178">Url</span></span>                                 | <span data-ttu-id="8e0ea-p117">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8e0ea-p117">URL that displays the resource in the browser. Read-only.</span></span>                                                                                                         |

[specialFolder]: specialfolder.md

## <a name="remarks"></a><span data-ttu-id="8e0ea-182">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8e0ea-182">Remarks</span></span>

<span data-ttu-id="8e0ea-183">Para obtener más información sobre las facetas de un objeto **driveItem**, consulte [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="8e0ea-183">For more information about the facets on a **driveItem**, see [driveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The quota facet provides information about how much space the OneDrive has available.",
  "keywords": "quota,available,remaining,used",
  "section": "documentation",
  "tocPath": "Facets/RemoteItem"
} -->
