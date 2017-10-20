---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
ms.openlocfilehash: 9de6923146b915207fc771721d7aeb6767e9f99e
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="hashes-resource-type"></a><span data-ttu-id="e535b-101">Tipo de recurso Hashes</span><span class="sxs-lookup"><span data-stu-id="e535b-101">Hashes resource type</span></span>

<span data-ttu-id="e535b-102">El recurso **Hashes** agrupa hashes disponibles en una sola estructura de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e535b-102">The **Hashes** resource groups available hashes into a single structure for an item.</span></span>

<span data-ttu-id="e535b-103">**Nota:** No todos los servicios proporcionan un valor para todas las propiedades de hash enumeradas.</span><span class="sxs-lookup"><span data-stu-id="e535b-103">**Note:** Not all services provide a value for all hash properties listed.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e535b-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e535b-104">JSON representation</span></span>

<span data-ttu-id="e535b-105">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="e535b-105">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [ "sha1Hash", "crc32Hash", "quickXorHash" ],
  "@odata.type": "microsoft.graph.hashes"
}-->

```json
{
  "crc32Hash": "string (hex)",
  "sha1Hash": "string (hex)",
  "quickXorHash": "string (base64)"
}
```

## <a name="properties"></a><span data-ttu-id="e535b-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e535b-106">Properties</span></span>

| <span data-ttu-id="e535b-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e535b-107">Property</span></span>         | <span data-ttu-id="e535b-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="e535b-108">Type</span></span>   | <span data-ttu-id="e535b-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e535b-109">Description</span></span>                                                       |
|:-----------------|:-------|:------------------------------------------------------------------|
| <span data-ttu-id="e535b-110">**sha1Hash**</span><span class="sxs-lookup"><span data-stu-id="e535b-110">**sha1Hash**</span></span>     | <span data-ttu-id="e535b-111">String</span><span class="sxs-lookup"><span data-stu-id="e535b-111">String</span></span> | <span data-ttu-id="e535b-p101">Hash SHA1 para el contenido del archivo (si está disponible). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e535b-p101">SHA1 hash for the contents of the file (if available). Read-only.</span></span> |
| <span data-ttu-id="e535b-114">**crc32Hash**</span><span class="sxs-lookup"><span data-stu-id="e535b-114">**crc32Hash**</span></span>    | <span data-ttu-id="e535b-115">String</span><span class="sxs-lookup"><span data-stu-id="e535b-115">String</span></span> | <span data-ttu-id="e535b-p102">El valor CRC32 del archivo (si está disponible). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e535b-p102">The CRC32 value of the file (if available). Read-only.</span></span>            |
| <span data-ttu-id="e535b-118">**quickXorHash**</span><span class="sxs-lookup"><span data-stu-id="e535b-118">**quickXorHash**</span></span> | <span data-ttu-id="e535b-119">String</span><span class="sxs-lookup"><span data-stu-id="e535b-119">String</span></span> | <span data-ttu-id="e535b-p103">Un hash de propietario del archivo que se puede usar para determinar si ha cambiado el contenido del archivo (si está disponible). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e535b-p103">A proprietary hash of the file that can be used to determine if the contents of the file have changed (if available). Read-only.</span></span> |

<span data-ttu-id="e535b-p104">**Nota:** En algunos casos, puede que no estén disponibles los valores hash. Si este es el caso, los valores hash de un elemento se actualizarán después de que se descargue el elemento.</span><span class="sxs-lookup"><span data-stu-id="e535b-p104">**Note:** In some cases hash values may not be available. If this is the case, the hash values on an item will be updated after the item is downloaded.</span></span>

## <a name="remarks"></a><span data-ttu-id="e535b-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="e535b-124">Remarks</span></span>

<span data-ttu-id="e535b-125">En OneDrive para la Empresa y SharePoint Server 2016, **sha1Hash** y **crc32Hash** no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="e535b-125">In OneDrive for Business and SharePoint Server 2016, **sha1Hash** and **crc32Hash** are not available.</span></span>

<span data-ttu-id="e535b-126">En OneDrive Personal, **quickXorHash** no está disponible.</span><span class="sxs-lookup"><span data-stu-id="e535b-126">In OneDrive Personal, **quickXorHash** is not available.</span></span>

<span data-ttu-id="e535b-127">Para calcular **quickXorHash** para un archivo, haga referencia al [fragmento de código QuickXorHash](https://dev.onedrive.com/snippets/quickxorhash.htm).</span><span class="sxs-lookup"><span data-stu-id="e535b-127">To calculate **quickXorHash** for a file, refer to the [QuickXorHash snippet](https://dev.onedrive.com/snippets/quickxorhash.htm).</span></span>
<span data-ttu-id="e535b-128">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="e535b-128">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "The hashes facet provides hash identifiers for a file in OneDrive",
  "keywords": "hash,sha1,crc32,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Hashes"
} -->
