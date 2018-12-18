---
title: tipo de recurso resourceReference
description: Tipo complejo que contiene las propiedades de conocimientos.
author: simonhult
ms.openlocfilehash: 2f1a44412eebbb7a74895c12db9a07696d6ee409
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27363623"
---
# <a name="resourcereference-resource-type"></a><span data-ttu-id="3ff9d-103">tipo de recurso resourceReference</span><span class="sxs-lookup"><span data-stu-id="3ff9d-103">resourceReference resource type</span></span>

> <span data-ttu-id="3ff9d-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="3ff9d-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3ff9d-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="3ff9d-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="3ff9d-106">Tipo complejo que contiene las propiedades de [conocimientos](insights.md).</span><span class="sxs-lookup"><span data-stu-id="3ff9d-106">Complex type containing properties of [Insights](insights.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="3ff9d-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3ff9d-107">JSON representation</span></span>

<span data-ttu-id="3ff9d-108">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3ff9d-108">Here is a JSON representation of the resource</span></span>

```json
{
  "webUrl": "string",
  "id": "string",
  "type": "string"
}
```

## <a name="properties"></a><span data-ttu-id="3ff9d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ff9d-109">Properties</span></span>

| <span data-ttu-id="3ff9d-110">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3ff9d-110">Property</span></span>      | <span data-ttu-id="3ff9d-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ff9d-111">Type</span></span>      | <span data-ttu-id="3ff9d-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ff9d-112">Description</span></span>  |
| ------------- |-----------| -------------|
| <span data-ttu-id="3ff9d-113">webUrl</span><span class="sxs-lookup"><span data-stu-id="3ff9d-113">webUrl</span></span>        | <span data-ttu-id="3ff9d-114">String</span><span class="sxs-lookup"><span data-stu-id="3ff9d-114">String</span></span>    | <span data-ttu-id="3ff9d-115">Una dirección URL conduce al elemento referenciado.</span><span class="sxs-lookup"><span data-stu-id="3ff9d-115">A URL leading to the referenced item.</span></span> |
| <span data-ttu-id="3ff9d-116">id</span><span class="sxs-lookup"><span data-stu-id="3ff9d-116">id</span></span>            | <span data-ttu-id="3ff9d-117">String</span><span class="sxs-lookup"><span data-stu-id="3ff9d-117">String</span></span>    | <span data-ttu-id="3ff9d-118">Identificador único del elemento.</span><span class="sxs-lookup"><span data-stu-id="3ff9d-118">The item's unique identifier.</span></span>           |
| <span data-ttu-id="3ff9d-119">type</span><span class="sxs-lookup"><span data-stu-id="3ff9d-119">type</span></span>          | <span data-ttu-id="3ff9d-120">String</span><span class="sxs-lookup"><span data-stu-id="3ff9d-120">String</span></span>    | <span data-ttu-id="3ff9d-121">Un valor de tipo string que se puede usar para clasificar el elemento, como "microsoft.graph.driveItem"</span><span class="sxs-lookup"><span data-stu-id="3ff9d-121">A string value that can be used to classify the item, such as "microsoft.graph.driveItem"</span></span> |