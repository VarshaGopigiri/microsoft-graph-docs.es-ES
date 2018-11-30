---
author: daspek
ms.author: dspektor
ms.date: 09/13/2017
title: ContentTypeOrder
ms.openlocfilehash: 8cb47837d8df1c38ed25fc87d3b4d7da450fed1a
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27028804"
---
# <a name="contenttypeorder-resource-type"></a><span data-ttu-id="ace28-102">Tipo de recurso ContentTypeOrder</span><span class="sxs-lookup"><span data-stu-id="ace28-102">ContentTypeOrder resource type</span></span>

<span data-ttu-id="ace28-103">El recurso **contentTypeOrder** especifica el orden en el que aparecerá el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="ace28-103">The **contentTypeOrder** resource specifies in which order the Content Type will appear in the selection UI.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ace28-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ace28-104">JSON representation</span></span>

<span data-ttu-id="ace28-105">A continuación se incluye una representación JSON de un recurso **contentTypeOrder**.</span><span class="sxs-lookup"><span data-stu-id="ace28-105">Here is a JSON representation of a **contentTypeOrder** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.contentTypeOrder", "@type.aka": "oneDrive.contentTypeOrderFacet" } -->

```json
{
  "default": true,
  "position": 2
}
```

## <a name="properties"></a><span data-ttu-id="ace28-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ace28-106">Properties</span></span>

| <span data-ttu-id="ace28-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="ace28-107">Property name</span></span> | <span data-ttu-id="ace28-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="ace28-108">Type</span></span>    | <span data-ttu-id="ace28-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ace28-109">Description</span></span>
|:--------------|:--------|:----------------------------------------------------
| <span data-ttu-id="ace28-110">**default**</span><span class="sxs-lookup"><span data-stu-id="ace28-110">**default**</span></span>   | <span data-ttu-id="ace28-111">boolean</span><span class="sxs-lookup"><span data-stu-id="ace28-111">boolean</span></span> | <span data-ttu-id="ace28-112">Si este es el tipo de contenido predeterminado</span><span class="sxs-lookup"><span data-stu-id="ace28-112">Whether this is the default Content Type</span></span>
| <span data-ttu-id="ace28-113">**position**</span><span class="sxs-lookup"><span data-stu-id="ace28-113">**position**</span></span>  | <span data-ttu-id="ace28-114">Int32</span><span class="sxs-lookup"><span data-stu-id="ace28-114">Int32</span></span>   | <span data-ttu-id="ace28-115">Especifica la posición en la que aparece el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="ace28-115">Specifies the position in which the Content Type appears in the selection UI.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentTypeOrder"
} -->
