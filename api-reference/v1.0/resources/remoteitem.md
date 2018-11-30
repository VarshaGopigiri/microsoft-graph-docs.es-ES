---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: RemoteItem
ms.openlocfilehash: df613c674ab2aed8857112ba01d3a77c15dcd81a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27031539"
---
# <a name="remoteitem-resource-type"></a><span data-ttu-id="917d4-102">Tipo de recurso RemoteItem</span><span class="sxs-lookup"><span data-stu-id="917d4-102">RemoteItem resource type</span></span>

<span data-ttu-id="917d4-p101">El recurso **remoteItem** indica que un objeto [**driveItem**](driveitem.md) hace referencia a un elemento que existe en otra unidad. Este recurso proporciona los identificadores únicos de la unidad de origen y del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="917d4-p101">The **remoteItem** resource indicates that a [**driveItem**](driveitem.md) references an item that exists in another drive. This resource provides the unique IDs of the source drive and target item.</span></span>

<span data-ttu-id="917d4-105">Los objetos [**DriveItem**](driveitem.md) con una faceta **remoteItem** que no sea null son recursos que se comparten, agregan al OneDrive del usuario o que están en elementos devueltos de colecciones heterogéneas de elementos (como los resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="917d4-105">[**DriveItems**](driveitem.md) with a non-null **remoteItem** facet are resources that are shared, added to the user's OneDrive, or on items returned from hetrogenous collections of items (like search results).</span></span>

<span data-ttu-id="917d4-106">**Nota:** A diferencia de las carpetas de la misma unidad, puede que a un objeto **driveItem** que se mueva a un elemento remoto se le cambie el valor `id`.</span><span class="sxs-lookup"><span data-stu-id="917d4-106">**Note:** Unlike with folders in the same drive, a **driveItem** moved into a remote item may have its `id` value changed.</span></span>

## <a name="json-representation"></a><span data-ttu-id="917d4-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="917d4-107">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="917d4-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="917d4-108">Properties</span></span>

| <span data-ttu-id="917d4-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="917d4-109">Property name</span></span>        | <span data-ttu-id="917d4-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="917d4-110">Type</span></span>                                | <span data-ttu-id="917d4-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="917d4-111">Description</span></span>                                                                                                                                                       |
| :------------------- | :---------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="917d4-112">createdBy</span><span class="sxs-lookup"><span data-stu-id="917d4-112">createdBy</span></span>            | [<span data-ttu-id="917d4-113">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="917d4-113">IdentitySet</span></span>](identityset.md)       | <span data-ttu-id="917d4-p102">Identidad del usuario, el dispositivo y la aplicación que ha creado el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p102">Identity of the user, device, and application which created the item. Read-only.</span></span>                                                                                  |
| <span data-ttu-id="917d4-116">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="917d4-116">createdDateTime</span></span>      | <span data-ttu-id="917d4-117">Timestamp</span><span class="sxs-lookup"><span data-stu-id="917d4-117">Timestamp</span></span>                           | <span data-ttu-id="917d4-p103">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p103">Date and time of item creation. Read-only.</span></span>                                                                                                                        |
| <span data-ttu-id="917d4-120">archivo</span><span class="sxs-lookup"><span data-stu-id="917d4-120">file</span></span>                 | [<span data-ttu-id="917d4-121">File</span><span class="sxs-lookup"><span data-stu-id="917d4-121">File</span></span>](file.md)                     | <span data-ttu-id="917d4-p104">Indica que el elemento remoto es un archivo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p104">Indicates that the remote item is a file. Read-only.</span></span>                                                                                                              |
| <span data-ttu-id="917d4-124">fileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="917d4-124">fileSystemInfo</span></span>       | [<span data-ttu-id="917d4-125">FileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="917d4-125">FileSystemInfo</span></span>](filesysteminfo.md) | <span data-ttu-id="917d4-p105">Información sobre el elemento remoto del sistema de archivos local. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p105">Information about the remote item from the local file system. Read-only.</span></span>                                                                                          |
| <span data-ttu-id="917d4-128">folder</span><span class="sxs-lookup"><span data-stu-id="917d4-128">folder</span></span>               | [<span data-ttu-id="917d4-129">Folder</span><span class="sxs-lookup"><span data-stu-id="917d4-129">Folder</span></span>](folder.md)                 | <span data-ttu-id="917d4-p106">Indica que el elemento remoto es una carpeta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p106">Indicates that the remote item is a folder. Read-only.</span></span>                                                                                                            |
| <span data-ttu-id="917d4-132">id</span><span class="sxs-lookup"><span data-stu-id="917d4-132">id</span></span>                   | <span data-ttu-id="917d4-133">String</span><span class="sxs-lookup"><span data-stu-id="917d4-133">String</span></span>                              | <span data-ttu-id="917d4-p107">Identificador único del elemento remoto en su unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p107">Unique identifier for the remote item in its drive. Read-only.</span></span>                                                                                                    |
| <span data-ttu-id="917d4-136">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="917d4-136">lastModifiedBy</span></span>       | [<span data-ttu-id="917d4-137">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="917d4-137">IdentitySet</span></span>](identityset.md)       | <span data-ttu-id="917d4-p108">Identidad del usuario, el dispositivo y la aplicación que ha modificado por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p108">Identity of the user, device, and application which last modified the item. Read-only.</span></span>                                                                            |
| <span data-ttu-id="917d4-140">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="917d4-140">lastModifiedDateTime</span></span> | <span data-ttu-id="917d4-141">Timestamp</span><span class="sxs-lookup"><span data-stu-id="917d4-141">Timestamp</span></span>                           | <span data-ttu-id="917d4-p109">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p109">Date and time the item was last modified. Read-only.</span></span>                                                                                                              |
| <span data-ttu-id="917d4-144">name</span><span class="sxs-lookup"><span data-stu-id="917d4-144">name</span></span>                 | <span data-ttu-id="917d4-145">String</span><span class="sxs-lookup"><span data-stu-id="917d4-145">String</span></span>                              | <span data-ttu-id="917d4-p110">Opcional. Nombre de archivo del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p110">Optional. Filename of the remote item. Read-only.</span></span>                                                                                                                 |
| <span data-ttu-id="917d4-149">paquete</span><span class="sxs-lookup"><span data-stu-id="917d4-149">package</span></span>              | [<span data-ttu-id="917d4-150">Package</span><span class="sxs-lookup"><span data-stu-id="917d4-150">Package</span></span>](package.md)               | <span data-ttu-id="917d4-p111">Si está presente, indica que este elemento es un paquete en lugar de una carpeta o archivo. Los paquetes se tratan como archivos en algunos contextos y como carpetas en otros. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p111">If present, indicates that this item is a package instead of a folder or file. Packages are treated like files in some contexts and folders in others. Read-only.</span></span> |
| <span data-ttu-id="917d4-154">parentReference</span><span class="sxs-lookup"><span data-stu-id="917d4-154">parentReference</span></span>      | [<span data-ttu-id="917d4-155">ItemReference</span><span class="sxs-lookup"><span data-stu-id="917d4-155">ItemReference</span></span>](itemreference.md)   | <span data-ttu-id="917d4-p112">Propiedades del elemento primario del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p112">Properties of the parent of the remote item. Read-only.</span></span>                                                                                                           |
| <span data-ttu-id="917d4-158">shared</span><span class="sxs-lookup"><span data-stu-id="917d4-158">shared</span></span>               | [<span data-ttu-id="917d4-159">shared</span><span class="sxs-lookup"><span data-stu-id="917d4-159">shared</span></span>](shared.md)                 | <span data-ttu-id="917d4-p113">Indica que el elemento se ha compartido con otros usuarios y proporciona información sobre el estado del elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p113">Indicates that the item has been shared with others and provides information about the shared state of the item. Read-only.</span></span>                                       |
| <span data-ttu-id="917d4-162">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="917d4-162">sharepointIds</span></span>        | [<span data-ttu-id="917d4-163">SharepointIds</span><span class="sxs-lookup"><span data-stu-id="917d4-163">SharepointIds</span></span>](sharepointids.md)   | <span data-ttu-id="917d4-p114">Proporciona interoperabilidad entre elementos de OneDrive para la Empresa y SharePoint con el conjunto completo de identificadores de elementos. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p114">Provides interop between items in OneDrive for Business and SharePoint with the full set of item identifiers. Read-only.</span></span>                                          |
| <span data-ttu-id="917d4-166">size</span><span class="sxs-lookup"><span data-stu-id="917d4-166">size</span></span>                 | <span data-ttu-id="917d4-167">Int64</span><span class="sxs-lookup"><span data-stu-id="917d4-167">Int64</span></span>                               | <span data-ttu-id="917d4-p115">Tamaño del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p115">Size of the remote item. Read-only.</span></span>                                                                                                                               |
| <span data-ttu-id="917d4-170">specialFolder</span><span class="sxs-lookup"><span data-stu-id="917d4-170">specialFolder</span></span>        | <span data-ttu-id="917d4-171">[specialFolder][]</span><span class="sxs-lookup"><span data-stu-id="917d4-171">[specialFolder][]</span></span>                   | <span data-ttu-id="917d4-p116">Si el elemento actual también está disponible como una carpeta especial, se devuelve esta faceta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p116">If the current item is also available as a special folder, this facet is returned. Read-only.</span></span>                                                                     |
| <span data-ttu-id="917d4-174">webDavUrl</span><span class="sxs-lookup"><span data-stu-id="917d4-174">webDavUrl</span></span>            | <span data-ttu-id="917d4-175">Url</span><span class="sxs-lookup"><span data-stu-id="917d4-175">Url</span></span>                                 | <span data-ttu-id="917d4-176">Dirección URL compatible con DAV del elemento.</span><span class="sxs-lookup"><span data-stu-id="917d4-176">DAV compatible URL for the item.</span></span>                                                                                                                                  |
| <span data-ttu-id="917d4-177">webUrl</span><span class="sxs-lookup"><span data-stu-id="917d4-177">webUrl</span></span>               | <span data-ttu-id="917d4-178">Url</span><span class="sxs-lookup"><span data-stu-id="917d4-178">Url</span></span>                                 | <span data-ttu-id="917d4-p117">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="917d4-p117">URL that displays the resource in the browser. Read-only.</span></span>                                                                                                         |

[specialFolder]: specialfolder.md

## <a name="remarks"></a><span data-ttu-id="917d4-182">Observaciones</span><span class="sxs-lookup"><span data-stu-id="917d4-182">Remarks</span></span>

<span data-ttu-id="917d4-183">Para obtener más información sobre las facetas de un objeto **driveItem**, consulte [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="917d4-183">For more information about the facets on a **driveItem**, see [driveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The quota facet provides information about how much space the OneDrive has available.",
  "keywords": "quota,available,remaining,used",
  "section": "documentation",
  "tocPath": "Facets/RemoteItem"
} -->