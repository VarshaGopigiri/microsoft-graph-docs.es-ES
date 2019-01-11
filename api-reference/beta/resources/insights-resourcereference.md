---
title: tipo de recurso resourceReference
description: Tipo complejo que contiene las propiedades de conocimientos.
author: simonhult
localization_priority: Normal
ms.openlocfilehash: 8ab2a79d66db6a45ecf3df748cf8f5740721ef80
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874329"
---
# <a name="resourcereference-resource-type"></a><span data-ttu-id="eb6c8-103">tipo de recurso resourceReference</span><span class="sxs-lookup"><span data-stu-id="eb6c8-103">resourceReference resource type</span></span>

> <span data-ttu-id="eb6c8-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="eb6c8-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="eb6c8-106">Tipo complejo que contiene las propiedades de [conocimientos](insights.md).</span><span class="sxs-lookup"><span data-stu-id="eb6c8-106">Complex type containing properties of [Insights](insights.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="eb6c8-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="eb6c8-107">JSON representation</span></span>

<span data-ttu-id="eb6c8-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="eb6c8-108">Here is a JSON representation of the resource</span></span>

```json
{
  "webUrl": "string",
  "id": "string",
  "type": "string"
}
```

## <a name="properties"></a><span data-ttu-id="eb6c8-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="eb6c8-109">Properties</span></span>

| <span data-ttu-id="eb6c8-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eb6c8-110">Property</span></span>      | <span data-ttu-id="eb6c8-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="eb6c8-111">Type</span></span>      | <span data-ttu-id="eb6c8-112">Description</span><span class="sxs-lookup"><span data-stu-id="eb6c8-112">Description</span></span>  |
| ------------- |-----------| -------------|
| <span data-ttu-id="eb6c8-113">webUrl</span><span class="sxs-lookup"><span data-stu-id="eb6c8-113">webUrl</span></span>        | <span data-ttu-id="eb6c8-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb6c8-114">String</span></span>    | <span data-ttu-id="eb6c8-115">Una dirección URL conduce al elemento referenciado.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-115">A URL leading to the referenced item.</span></span> |
| <span data-ttu-id="eb6c8-116">id</span><span class="sxs-lookup"><span data-stu-id="eb6c8-116">id</span></span>            | <span data-ttu-id="eb6c8-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb6c8-117">String</span></span>    | <span data-ttu-id="eb6c8-118">Identificador único del elemento.</span><span class="sxs-lookup"><span data-stu-id="eb6c8-118">The item's unique identifier.</span></span>           |
| <span data-ttu-id="eb6c8-119">type</span><span class="sxs-lookup"><span data-stu-id="eb6c8-119">type</span></span>          | <span data-ttu-id="eb6c8-120">Cadena</span><span class="sxs-lookup"><span data-stu-id="eb6c8-120">String</span></span>    | <span data-ttu-id="eb6c8-121">Un valor de tipo string que se puede usar para clasificar el elemento, como "microsoft.graph.driveItem"</span><span class="sxs-lookup"><span data-stu-id="eb6c8-121">A string value that can be used to classify the item, such as "microsoft.graph.driveItem"</span></span> |
