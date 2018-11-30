---
author: daspek
ms.author: dspektor
ms.date: 09/13/2017
title: ContentTypeOrder
ms.openlocfilehash: a6b83627d86bbb35357f03dbee3605c6fb1df7a1
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090118"
---
# <a name="contenttypeorder-resource-type"></a><span data-ttu-id="a4adf-102">Tipo de recurso ContentTypeOrder</span><span class="sxs-lookup"><span data-stu-id="a4adf-102">ContentTypeOrder resource type</span></span>

> <span data-ttu-id="a4adf-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="a4adf-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a4adf-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="a4adf-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a4adf-105">El recurso **contentTypeOrder** especifica el orden en el que aparecerá el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="a4adf-105">The **contentTypeOrder** resource specifies in which order the Content Type will appear in the selection UI.</span></span>

## <a name="json-representation"></a><span data-ttu-id="a4adf-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="a4adf-106">JSON representation</span></span>

<span data-ttu-id="a4adf-107">A continuación se incluye una representación JSON de un recurso **contentTypeOrder**.</span><span class="sxs-lookup"><span data-stu-id="a4adf-107">Here is a JSON representation of a **contentTypeOrder** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.contentTypeOrder", "@type.aka": "oneDrive.contentTypeOrderFacet" } -->

```json
{
  "default": true,
  "position": 2
}
```

## <a name="properties"></a><span data-ttu-id="a4adf-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a4adf-108">Properties</span></span>

| <span data-ttu-id="a4adf-109">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="a4adf-109">Property name</span></span> | <span data-ttu-id="a4adf-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="a4adf-110">Type</span></span>    | <span data-ttu-id="a4adf-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="a4adf-111">Description</span></span>
|:--------------|:--------|:----------------------------------------------------
| <span data-ttu-id="a4adf-112">**default**</span><span class="sxs-lookup"><span data-stu-id="a4adf-112">**default**</span></span>   | <span data-ttu-id="a4adf-113">boolean</span><span class="sxs-lookup"><span data-stu-id="a4adf-113">boolean</span></span> | <span data-ttu-id="a4adf-114">Si este es el tipo de contenido predeterminado</span><span class="sxs-lookup"><span data-stu-id="a4adf-114">Whether this is the default Content Type</span></span>
| <span data-ttu-id="a4adf-115">**position**</span><span class="sxs-lookup"><span data-stu-id="a4adf-115">**position**</span></span>  | <span data-ttu-id="a4adf-116">Int32</span><span class="sxs-lookup"><span data-stu-id="a4adf-116">Int32</span></span>   | <span data-ttu-id="a4adf-117">Especifica la posición en la que aparece el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="a4adf-117">Specifies the position in which the Content Type appears in the selection UI.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentTypeOrder"
} -->
