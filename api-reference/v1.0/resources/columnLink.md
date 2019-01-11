---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ColumnLink
localization_priority: Normal
ms.openlocfilehash: 435696cc596f73830104ea8ec0619bf40a462d62
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27834534"
---
# <a name="columnlink-resource-type"></a><span data-ttu-id="c1c68-102">Tipo de recurso ColumnLink</span><span class="sxs-lookup"><span data-stu-id="c1c68-102">ColumnLink resource type</span></span>

<span data-ttu-id="c1c68-103">Un recurso **columnLink** en un recurso [contentType][] adjunta el recurso **columnDefinition** de un sitio a ese tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="c1c68-103">A **columnLink** on a [contentType][] attaches a site **columnDefinition** to that content type.</span></span>

[contentType]: contenttype.md

## <a name="json-representation"></a><span data-ttu-id="c1c68-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c1c68-105">JSON representation</span></span>

<span data-ttu-id="c1c68-106">A continuación se incluye una representación JSON de un recurso **columnLink**.</span><span class="sxs-lookup"><span data-stu-id="c1c68-106">Here is a JSON representation of a **columnLink** resource.</span></span>
<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.columnLink" } -->

```json
{
  "id": "string",
  "name": "string"
}
```

## <a name="properties"></a><span data-ttu-id="c1c68-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c1c68-107">Properties</span></span>

| <span data-ttu-id="c1c68-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="c1c68-108">Property name</span></span> | <span data-ttu-id="c1c68-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="c1c68-109">Type</span></span>   | <span data-ttu-id="c1c68-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1c68-110">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="c1c68-111">**id**</span><span class="sxs-lookup"><span data-stu-id="c1c68-111">**id**</span></span>        | <span data-ttu-id="c1c68-112">string</span><span class="sxs-lookup"><span data-stu-id="c1c68-112">string</span></span> | <span data-ttu-id="c1c68-113">El identificador único de la columna.</span><span class="sxs-lookup"><span data-stu-id="c1c68-113">The unique identifier for the column.</span></span>
| <span data-ttu-id="c1c68-114">**name**</span><span class="sxs-lookup"><span data-stu-id="c1c68-114">**name**</span></span>      | <span data-ttu-id="c1c68-115">string</span><span class="sxs-lookup"><span data-stu-id="c1c68-115">string</span></span> | <span data-ttu-id="c1c68-116">El nombre de la columna de este tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="c1c68-116">The name of the column  in this content type.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ColumnLink"
} -->
