---
author: daspek
ms.author: dspektor
ms.date: 09/13/2017
title: ContentTypeOrder
ms.openlocfilehash: fe7309373ded16fe2660e0c5a69773c18ffb581a
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="contenttypeorder-resource-type"></a><span data-ttu-id="d4aa0-102">Tipo de recurso ContentTypeOrder</span><span class="sxs-lookup"><span data-stu-id="d4aa0-102">ContentTypeOrder resource type</span></span>

<span data-ttu-id="d4aa0-103">El recurso **contentTypeOrder** especifica el orden en el que aparecerá el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="d4aa0-103">The **contentTypeOrder** resource specifies in which order the Content Type will appear in the selection UI.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d4aa0-104">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d4aa0-104">JSON representation</span></span>

<span data-ttu-id="d4aa0-105">A continuación se incluye una representación JSON de un recurso **contentTypeOrder**.</span><span class="sxs-lookup"><span data-stu-id="d4aa0-105">Here is a JSON representation of a **baseItem** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.contentTypeOrder", "@type.aka": "oneDrive.contentTypeOrderFacet" } -->

```json
{
  "default": true,
  "position": 2
}
```

## <a name="properties"></a><span data-ttu-id="d4aa0-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d4aa0-106">Properties</span></span>

| <span data-ttu-id="d4aa0-107">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="d4aa0-107">Property name</span></span> | <span data-ttu-id="d4aa0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d4aa0-108">Type</span></span>    | <span data-ttu-id="d4aa0-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d4aa0-109">Description</span></span>
|:--------------|:--------|:----------------------------------------------------
| <span data-ttu-id="d4aa0-110">**default**</span><span class="sxs-lookup"><span data-stu-id="d4aa0-110">**default**</span></span>   | <span data-ttu-id="d4aa0-111">boolean</span><span class="sxs-lookup"><span data-stu-id="d4aa0-111">boolean</span></span> | <span data-ttu-id="d4aa0-112">Si este es el tipo de contenido predeterminado</span><span class="sxs-lookup"><span data-stu-id="d4aa0-112">Whether this is the default Content Type</span></span>
| <span data-ttu-id="d4aa0-113">**position**</span><span class="sxs-lookup"><span data-stu-id="d4aa0-113">**position**</span></span>  | <span data-ttu-id="d4aa0-114">Int32</span><span class="sxs-lookup"><span data-stu-id="d4aa0-114">Int32</span></span>   | <span data-ttu-id="d4aa0-115">Especifica la posición en la que aparece el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="d4aa0-115">Specifies the position in which the Content Type appears in the selection UI.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentTypeOrder"
} -->
