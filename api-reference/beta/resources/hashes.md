---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Hashes
ms.openlocfilehash: 2387af83450f667aa4732cc46d7d3cf2111579f0
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27083441"
---
# <a name="hashes-resource-type"></a><span data-ttu-id="5f83d-102">Tipo de recurso Hashes</span><span class="sxs-lookup"><span data-stu-id="5f83d-102">Hashes resource type</span></span>

> <span data-ttu-id="5f83d-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5f83d-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5f83d-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5f83d-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5f83d-105">El recurso **Hashes** agrupa hashes disponibles en una sola estructura de un elemento.</span><span class="sxs-lookup"><span data-stu-id="5f83d-105">The **Hashes** resource groups available hashes into a single structure for an item.</span></span>

<span data-ttu-id="5f83d-106">**Nota:** No todos los servicios proporcionan un valor para todas las propiedades de hash enumeradas.</span><span class="sxs-lookup"><span data-stu-id="5f83d-106">**Note:** Not all services provide a value for all hash properties listed.</span></span>

## <a name="json-representation"></a><span data-ttu-id="5f83d-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5f83d-107">JSON representation</span></span>

<span data-ttu-id="5f83d-108">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="5f83d-108">Here is a JSON representation of the resource.</span></span>

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

## <a name="properties"></a><span data-ttu-id="5f83d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5f83d-109">Properties</span></span>

| <span data-ttu-id="5f83d-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5f83d-110">Property</span></span>         | <span data-ttu-id="5f83d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="5f83d-111">Type</span></span>   | <span data-ttu-id="5f83d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="5f83d-112">Description</span></span>                                                       |
|:-----------------|:-------|:------------------------------------------------------------------|
| <span data-ttu-id="5f83d-113">**sha1Hash**</span><span class="sxs-lookup"><span data-stu-id="5f83d-113">**sha1Hash**</span></span>     | <span data-ttu-id="5f83d-114">String</span><span class="sxs-lookup"><span data-stu-id="5f83d-114">String</span></span> | <span data-ttu-id="5f83d-p102">Hash SHA1 para el contenido del archivo (si está disponible). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5f83d-p102">SHA1 hash for the contents of the file (if available). Read-only.</span></span> |
| <span data-ttu-id="5f83d-117">**crc32Hash**</span><span class="sxs-lookup"><span data-stu-id="5f83d-117">**crc32Hash**</span></span>    | <span data-ttu-id="5f83d-118">String</span><span class="sxs-lookup"><span data-stu-id="5f83d-118">String</span></span> | <span data-ttu-id="5f83d-p103">El valor CRC32 del archivo (si está disponible). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5f83d-p103">The CRC32 value of the file (if available). Read-only.</span></span>            |
| <span data-ttu-id="5f83d-121">**quickXorHash**</span><span class="sxs-lookup"><span data-stu-id="5f83d-121">**quickXorHash**</span></span> | <span data-ttu-id="5f83d-122">String</span><span class="sxs-lookup"><span data-stu-id="5f83d-122">String</span></span> | <span data-ttu-id="5f83d-p104">Un hash de propietario del archivo que se puede usar para determinar si ha cambiado el contenido del archivo (si está disponible). Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5f83d-p104">A proprietary hash of the file that can be used to determine if the contents of the file have changed (if available). Read-only.</span></span> |

<span data-ttu-id="5f83d-p105">**Nota:** En algunos casos, puede que no estén disponibles los valores hash. Si este es el caso, los valores hash de un elemento se actualizarán después de que se descargue el elemento.</span><span class="sxs-lookup"><span data-stu-id="5f83d-p105">**Note:** In some cases hash values may not be available. If this is the case, the hash values on an item will be updated after the item is downloaded.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f83d-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5f83d-127">Remarks</span></span>

<span data-ttu-id="5f83d-128">En OneDrive para la Empresa y SharePoint Server 2016, **sha1Hash** y **crc32Hash** no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="5f83d-128">In OneDrive for Business and SharePoint Server 2016, **sha1Hash** and **crc32Hash** are not available.</span></span>

<span data-ttu-id="5f83d-129">En OneDrive Personal, **quickXorHash** no está disponible.</span><span class="sxs-lookup"><span data-stu-id="5f83d-129">In OneDrive Personal, **quickXorHash** is not available.</span></span>

<span data-ttu-id="5f83d-130">Para calcular **quickXorHash** para un archivo, haga referencia al [fragmento de código QuickXorHash](https://dev.onedrive.com/snippets/quickxorhash.htm).</span><span class="sxs-lookup"><span data-stu-id="5f83d-130">To calculate **quickXorHash** for a file, refer to the [QuickXorHash snippet](https://dev.onedrive.com/snippets/quickxorhash.htm).</span></span>

<span data-ttu-id="5f83d-131">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="5f83d-131">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "The hashes facet provides hash identifiers for a file in OneDrive",
  "keywords": "hash,sha1,crc32,item,facet",
  "section": "documentation",
  "tocPath": "Facets/Hashes"
} -->
