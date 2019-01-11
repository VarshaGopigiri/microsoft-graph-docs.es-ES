---
author: daspek
ms.author: dspektor
ms.date: 09/13/2017
title: ContentTypeOrder
localization_priority: Normal
ms.openlocfilehash: ccea5804c3f4eddb02b5d4163302362f29b5fbc8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27890499"
---
# <a name="contenttypeorder-resource-type"></a><span data-ttu-id="1e300-102">Tipo de recurso ContentTypeOrder</span><span class="sxs-lookup"><span data-stu-id="1e300-102">ContentTypeOrder resource type</span></span>

<span data-ttu-id="1e300-103">El recurso **contentTypeOrder** especifica el orden en el que aparecerá el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="1e300-103">The **contentTypeOrder** resource specifies in which order the Content Type will appear in the selection UI.</span></span>

## <a name="json-representation"></a><span data-ttu-id="1e300-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1e300-104">JSON representation</span></span>

<span data-ttu-id="1e300-105">A continuación se incluye una representación JSON de un recurso **contentTypeOrder**.</span><span class="sxs-lookup"><span data-stu-id="1e300-105">Here is a JSON representation of a **contentTypeOrder** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.contentTypeOrder", "@type.aka": "oneDrive.contentTypeOrderFacet" } -->

```json
{
  "default": true,
  "position": 2
}
```

## <a name="properties"></a><span data-ttu-id="1e300-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e300-106">Properties</span></span>

| <span data-ttu-id="1e300-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="1e300-107">Property name</span></span> | <span data-ttu-id="1e300-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e300-108">Type</span></span>    | <span data-ttu-id="1e300-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e300-109">Description</span></span>
|:--------------|:--------|:----------------------------------------------------
| <span data-ttu-id="1e300-110">**default**</span><span class="sxs-lookup"><span data-stu-id="1e300-110">**default**</span></span>   | <span data-ttu-id="1e300-111">boolean</span><span class="sxs-lookup"><span data-stu-id="1e300-111">boolean</span></span> | <span data-ttu-id="1e300-112">Si este es el tipo de contenido predeterminado</span><span class="sxs-lookup"><span data-stu-id="1e300-112">Whether this is the default Content Type</span></span>
| <span data-ttu-id="1e300-113">**position**</span><span class="sxs-lookup"><span data-stu-id="1e300-113">**position**</span></span>  | <span data-ttu-id="1e300-114">Int32</span><span class="sxs-lookup"><span data-stu-id="1e300-114">Int32</span></span>   | <span data-ttu-id="1e300-115">Especifica la posición en la que aparece el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="1e300-115">Specifies the position in which the Content Type appears in the selection UI.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentTypeOrder"
} -->
