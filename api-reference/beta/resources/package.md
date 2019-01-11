---
author: rgregg
ms.author: rgregg
ms.date: 09/10/2017
title: Paquete
localization_priority: Normal
ms.openlocfilehash: ab3d9298b0a03e31a9e33e9c187c1a0af8691cc3
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27833946"
---
# <a name="package-resource-type"></a><span data-ttu-id="2aa2b-102">Tipo de recurso Package</span><span class="sxs-lookup"><span data-stu-id="2aa2b-102">Package resource type</span></span>

> <span data-ttu-id="2aa2b-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="2aa2b-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="2aa2b-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="2aa2b-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="2aa2b-105">El recurso **Package** indica que un objeto DriveItem es el elemento de nivel superior en un "paquete" o una colección de elementos que deben tratarse como una colección en lugar de elementos individuales.</span><span class="sxs-lookup"><span data-stu-id="2aa2b-105">The **Package** resource indicates that a DriveItem is the top level item in a "package" or a collection of items that should be treated as a collection instead of individual items.</span></span>

<span data-ttu-id="2aa2b-106">Un ejemplo de un paquete es un bloc de notas de OneNote.</span><span class="sxs-lookup"><span data-stu-id="2aa2b-106">An example of a package is a OneNote notebook.</span></span> <span data-ttu-id="2aa2b-107">Mientras que el bloc de notas se compone de archivos y carpetas que representan el contenido del bloc de notas, el elemento de nivel superior que representa el bloc de notas tiene una faceta **package** para indicar a los clientes que se trata de una colección de datos que se deberían tratar de forma especial.</span><span class="sxs-lookup"><span data-stu-id="2aa2b-107">While the notebook is made up of files and folders that represent the contents of the notebook, the top level item that represents the notebook has a **package** facet to indicate to clients that this is a collection of data that should be treated special.</span></span>

<span data-ttu-id="2aa2b-108">Los objetos DriveItem con la faceta **package** no incluyen una faceta **folder** o **file**, pero son similares de forma conceptual a un elemento con una faceta **folder**.</span><span class="sxs-lookup"><span data-stu-id="2aa2b-108">DriveItems with the **package** facet do not include a **folder** or **file** facet but are conceptually similar to an item with a **folder** facet.</span></span>

## <a name="json-representation"></a><span data-ttu-id="2aa2b-109">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="2aa2b-109">JSON representation</span></span>

<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.package" } -->
```json
{
  "type": "oneNote"
}
```

| <span data-ttu-id="2aa2b-110">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="2aa2b-110">Property Name</span></span> | <span data-ttu-id="2aa2b-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="2aa2b-111">Type</span></span>   | <span data-ttu-id="2aa2b-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="2aa2b-112">Description</span></span>                                                                                                                                                                      |
|:--------------|:-------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2aa2b-113">**type**</span><span class="sxs-lookup"><span data-stu-id="2aa2b-113">**type**</span></span>      | <span data-ttu-id="2aa2b-114">string</span><span class="sxs-lookup"><span data-stu-id="2aa2b-114">string</span></span> | <span data-ttu-id="2aa2b-p103">Una cadena que indica el tipo de paquete. Mientras que `oneNote` es el único valor definido actualmente, debe esperar que se devuelvan otros tipos de paquetes y debe controlarlos en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="2aa2b-p103">An string indicating the type of package. While `oneNote` is the only currently defined value, you should expect other package types to be returned and handle them accordingly.</span></span> |

## <a name="remarks"></a><span data-ttu-id="2aa2b-117">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2aa2b-117">Remarks</span></span> 

<span data-ttu-id="2aa2b-118">Para obtener más información sobre las facetas de un objeto DriveItem, consulte [DriveItem](driveitem.md).</span><span class="sxs-lookup"><span data-stu-id="2aa2b-118">For more information about the facets on a DriveItem, see [DriveItem](driveitem.md).</span></span>


<!-- {
  "type": "#page.annotation",
  "description": "The Package facet indicates that an item is the root of a special collection of items that should be treated as a single unit.",
  "keywords": "package, facet, onenote",
  "section": "documentation"
} -->
