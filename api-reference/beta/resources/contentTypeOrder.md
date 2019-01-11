---
author: daspek
ms.author: dspektor
ms.date: 09/13/2017
title: ContentTypeOrder
localization_priority: Normal
ms.openlocfilehash: ad25ececa9a32a1aaab7f25bf909f7e1ef640dec
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27825756"
---
# <a name="contenttypeorder-resource-type"></a><span data-ttu-id="30f78-102">Tipo de recurso ContentTypeOrder</span><span class="sxs-lookup"><span data-stu-id="30f78-102">ContentTypeOrder resource type</span></span>

> <span data-ttu-id="30f78-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="30f78-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="30f78-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="30f78-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="30f78-105">El recurso **contentTypeOrder** especifica el orden en el que aparecerá el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="30f78-105">The **contentTypeOrder** resource specifies in which order the Content Type will appear in the selection UI.</span></span>

## <a name="json-representation"></a><span data-ttu-id="30f78-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="30f78-106">JSON representation</span></span>

<span data-ttu-id="30f78-107">A continuación se incluye una representación JSON de un recurso **contentTypeOrder**.</span><span class="sxs-lookup"><span data-stu-id="30f78-107">Here is a JSON representation of a **contentTypeOrder** resource.</span></span>
<!-- { "blockType": "resource", "@type": "microsoft.graph.contentTypeOrder", "@type.aka": "oneDrive.contentTypeOrderFacet" } -->

```json
{
  "default": true,
  "position": 2
}
```

## <a name="properties"></a><span data-ttu-id="30f78-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="30f78-108">Properties</span></span>

| <span data-ttu-id="30f78-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="30f78-109">Property name</span></span> | <span data-ttu-id="30f78-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="30f78-110">Type</span></span>    | <span data-ttu-id="30f78-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="30f78-111">Description</span></span>
|:--------------|:--------|:----------------------------------------------------
| <span data-ttu-id="30f78-112">**default**</span><span class="sxs-lookup"><span data-stu-id="30f78-112">**default**</span></span>   | <span data-ttu-id="30f78-113">boolean</span><span class="sxs-lookup"><span data-stu-id="30f78-113">boolean</span></span> | <span data-ttu-id="30f78-114">Si este es el tipo de contenido predeterminado</span><span class="sxs-lookup"><span data-stu-id="30f78-114">Whether this is the default Content Type</span></span>
| <span data-ttu-id="30f78-115">**position**</span><span class="sxs-lookup"><span data-stu-id="30f78-115">**position**</span></span>  | <span data-ttu-id="30f78-116">Int32</span><span class="sxs-lookup"><span data-stu-id="30f78-116">Int32</span></span>   | <span data-ttu-id="30f78-117">Especifica la posición en la que aparece el tipo de contenido en la interfaz de usuario de selección.</span><span class="sxs-lookup"><span data-stu-id="30f78-117">Specifies the position in which the Content Type appears in the selection UI.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentTypeOrder"
} -->
