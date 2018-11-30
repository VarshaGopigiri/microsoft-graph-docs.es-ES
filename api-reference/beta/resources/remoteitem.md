---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: RemoteItem
ms.openlocfilehash: 0eb418d5a3f1fb65f6f59bd7babf87bed1d440dc
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083835"
---
# <a name="remoteitem-resource-type"></a><span data-ttu-id="19577-102">Tipo de recurso RemoteItem</span><span class="sxs-lookup"><span data-stu-id="19577-102">RemoteItem resource type</span></span>

> <span data-ttu-id="19577-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="19577-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="19577-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="19577-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="19577-p102">El recurso **remoteItem** indica que un objeto [**driveItem**](driveitem.md) hace referencia a un elemento que existe en otra unidad. Este recurso proporciona los identificadores únicos de la unidad de origen y del elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="19577-p102">The **remoteItem** resource indicates that a [**driveItem**](driveitem.md) references an item that exists in another drive. This resource provides the unique IDs of the source drive and target item.</span></span>

<span data-ttu-id="19577-107">Los objetos [**DriveItem**](driveitem.md) con una faceta **remoteItem** que no sea null son recursos que se comparten, agregan al OneDrive del usuario o que están en elementos devueltos de colecciones heterogéneas de elementos (como los resultados de la búsqueda).</span><span class="sxs-lookup"><span data-stu-id="19577-107">[**DriveItems**](driveitem.md) with a non-null **remoteItem** facet are resources that are shared, added to the user's OneDrive, or on items returned from hetrogenous collections of items (like search results).</span></span>

<span data-ttu-id="19577-108">**Nota:** A diferencia de las carpetas de la misma unidad, puede que a un objeto **driveItem** que se mueva a un elemento remoto se le cambie el valor `id`.</span><span class="sxs-lookup"><span data-stu-id="19577-108">**Note:** Unlike with folders in the same drive, a **driveItem** moved into a remote item may have its `id` value changed.</span></span>

## <a name="json-representation"></a><span data-ttu-id="19577-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="19577-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="19577-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="19577-110">Properties</span></span>

| <span data-ttu-id="19577-111">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="19577-111">Property name</span></span>        | <span data-ttu-id="19577-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="19577-112">Type</span></span>                                | <span data-ttu-id="19577-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="19577-113">Description</span></span>                                                                                                                                                       |
| :------------------- | :---------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="19577-114">createdBy</span><span class="sxs-lookup"><span data-stu-id="19577-114">createdBy</span></span>            | [<span data-ttu-id="19577-115">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="19577-115">IdentitySet</span></span>](identityset.md)       | <span data-ttu-id="19577-p103">Identidad del usuario, el dispositivo y la aplicación que creó el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p103">Identity of the user, device, and application which created the item. Read-only.</span></span>                                                                                  |
| <span data-ttu-id="19577-118">createdDateTime</span><span class="sxs-lookup"><span data-stu-id="19577-118">createdDateTime</span></span>      | <span data-ttu-id="19577-119">Timestamp</span><span class="sxs-lookup"><span data-stu-id="19577-119">Timestamp</span></span>                           | <span data-ttu-id="19577-p104">Fecha y hora de creación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p104">Date and time of item creation. Read-only.</span></span>                                                                                                                        |
| <span data-ttu-id="19577-122">file</span><span class="sxs-lookup"><span data-stu-id="19577-122">file</span></span>                 | [<span data-ttu-id="19577-123">File</span><span class="sxs-lookup"><span data-stu-id="19577-123">File</span></span>](file.md)                     | <span data-ttu-id="19577-p105">Indica que el elemento remoto es un archivo. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p105">Indicates that the remote item is a file. Read-only.</span></span>                                                                                                              |
| <span data-ttu-id="19577-126">fileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="19577-126">fileSystemInfo</span></span>       | [<span data-ttu-id="19577-127">FileSystemInfo</span><span class="sxs-lookup"><span data-stu-id="19577-127">FileSystemInfo</span></span>](filesysteminfo.md) | <span data-ttu-id="19577-p106">Información sobre el elemento remoto del sistema de archivos local. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p106">Information about the remote item from the local file system. Read-only.</span></span>                                                                                          |
| <span data-ttu-id="19577-130">folder</span><span class="sxs-lookup"><span data-stu-id="19577-130">folder</span></span>               | [<span data-ttu-id="19577-131">Folder</span><span class="sxs-lookup"><span data-stu-id="19577-131">Folder</span></span>](folder.md)                 | <span data-ttu-id="19577-p107">Indica que el elemento remoto es una carpeta. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p107">Indicates that the remote item is a folder. Read-only.</span></span>                                                                                                            |
| <span data-ttu-id="19577-134">id</span><span class="sxs-lookup"><span data-stu-id="19577-134">id</span></span>                   | <span data-ttu-id="19577-135">String</span><span class="sxs-lookup"><span data-stu-id="19577-135">String</span></span>                              | <span data-ttu-id="19577-p108">Identificador único del elemento remoto en su unidad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p108">Unique identifier for the remote item in its drive. Read-only.</span></span>                                                                                                    |
| <span data-ttu-id="19577-138">lastModifiedBy</span><span class="sxs-lookup"><span data-stu-id="19577-138">lastModifiedBy</span></span>       | [<span data-ttu-id="19577-139">IdentitySet</span><span class="sxs-lookup"><span data-stu-id="19577-139">IdentitySet</span></span>](identityset.md)       | <span data-ttu-id="19577-p109">Identidad del usuario, el dispositivo y la aplicación que modificó por última vez el elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p109">Identity of the user, device, and application which last modified the item. Read-only.</span></span>                                                                            |
| <span data-ttu-id="19577-142">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="19577-142">lastModifiedDateTime</span></span> | <span data-ttu-id="19577-143">Timestamp</span><span class="sxs-lookup"><span data-stu-id="19577-143">Timestamp</span></span>                           | <span data-ttu-id="19577-p110">Fecha y hora de la última modificación del elemento. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p110">Date and time the item was last modified. Read-only.</span></span>                                                                                                              |
| <span data-ttu-id="19577-146">name</span><span class="sxs-lookup"><span data-stu-id="19577-146">name</span></span>                 | <span data-ttu-id="19577-147">String</span><span class="sxs-lookup"><span data-stu-id="19577-147">String</span></span>                              | <span data-ttu-id="19577-p111">Opcional. Nombre de archivo del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p111">Optional. Filename of the remote item. Read-only.</span></span>                                                                                                                 |
| <span data-ttu-id="19577-151">paquete</span><span class="sxs-lookup"><span data-stu-id="19577-151">package</span></span>              | [<span data-ttu-id="19577-152">Package</span><span class="sxs-lookup"><span data-stu-id="19577-152">Package</span></span>](package.md)               | <span data-ttu-id="19577-p112">Si está presente, indica que este elemento es un paquete en lugar de una carpeta o archivo. Los paquetes se tratan como archivos en algunos contextos y como carpetas en otros. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p112">If present, indicates that this item is a package instead of a folder or file. Packages are treated like files in some contexts and folders in others. Read-only.</span></span> |
| <span data-ttu-id="19577-156">parentReference</span><span class="sxs-lookup"><span data-stu-id="19577-156">parentReference</span></span>      | [<span data-ttu-id="19577-157">ItemReference</span><span class="sxs-lookup"><span data-stu-id="19577-157">ItemReference</span></span>](itemreference.md)   | <span data-ttu-id="19577-p113">Propiedades del elemento primario del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p113">Properties of the parent of the remote item. Read-only.</span></span>                                                                                                           |
| <span data-ttu-id="19577-160">shared</span><span class="sxs-lookup"><span data-stu-id="19577-160">shared</span></span>               | [<span data-ttu-id="19577-161">shared</span><span class="sxs-lookup"><span data-stu-id="19577-161">shared</span></span>](shared.md)                 | <span data-ttu-id="19577-p114">Indica que el elemento se ha compartido con otros usuarios y proporciona información sobre el estado del elemento compartido. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p114">Indicates that the item has been shared with others and provides information about the shared state of the item. Read-only.</span></span>                                       |
| <span data-ttu-id="19577-164">sharepointIds</span><span class="sxs-lookup"><span data-stu-id="19577-164">sharepointIds</span></span>        | [<span data-ttu-id="19577-165">SharepointIds</span><span class="sxs-lookup"><span data-stu-id="19577-165">SharepointIds</span></span>](sharepointids.md)   | <span data-ttu-id="19577-p115">Proporciona interoperabilidad entre elementos de OneDrive para la Empresa y SharePoint con el conjunto completo de identificadores de elementos. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p115">Provides interop between items in OneDrive for Business and SharePoint with the full set of item identifiers. Read-only.</span></span>                                          |
| <span data-ttu-id="19577-168">size</span><span class="sxs-lookup"><span data-stu-id="19577-168">size</span></span>                 | <span data-ttu-id="19577-169">Int64</span><span class="sxs-lookup"><span data-stu-id="19577-169">Int64</span></span>                               | <span data-ttu-id="19577-p116">Tamaño del elemento remoto. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p116">Size of the remote item. Read-only.</span></span>                                                                                                                               |
| <span data-ttu-id="19577-172">webDavUrl</span><span class="sxs-lookup"><span data-stu-id="19577-172">webDavUrl</span></span>            | <span data-ttu-id="19577-173">Url</span><span class="sxs-lookup"><span data-stu-id="19577-173">Url</span></span>                                 | <span data-ttu-id="19577-174">Dirección URL compatible con DAV del elemento.</span><span class="sxs-lookup"><span data-stu-id="19577-174">DAV compatible URL for the item.</span></span>                                                                                                                                  |
| <span data-ttu-id="19577-175">webUrl</span><span class="sxs-lookup"><span data-stu-id="19577-175">webUrl</span></span>               | <span data-ttu-id="19577-176">Url</span><span class="sxs-lookup"><span data-stu-id="19577-176">Url</span></span>                                 | <span data-ttu-id="19577-p117">Dirección URL que muestra el recurso en el explorador. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="19577-p117">URL that displays the resource in the browser. Read-only.</span></span>                                                                                                         |

## <a name="remarks"></a><span data-ttu-id="19577-179">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19577-179">Remarks</span></span>

<span data-ttu-id="19577-180">Para obtener más información sobre las facetas de un objeto **driveItem**, consulte [driveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="19577-180">For more information about the facets on a **driveItem**, see [driveItem](driveitem.md).</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "The quota facet provides information about how much space the OneDrive has available.",
  "keywords": "quota,available,remaining,used",
  "section": "documentation",
  "tocPath": "Facets/RemoteItem"
} -->