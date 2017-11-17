---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ColumnLink
ms.openlocfilehash: ef7fef6fb6ca35f1117433b452de0841691282a0
ms.sourcegitcommit: 7aea7a97e36e6d146214de3a90fdbc71628aadba
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 09/28/2017
---
# <a name="columnlink-resource-type"></a><span data-ttu-id="4d646-102">Tipo de recurso ColumnLink</span><span class="sxs-lookup"><span data-stu-id="4d646-102">ColumnLink resource type</span></span>

<span data-ttu-id="4d646-103">Un recurso **columnLink** en un recurso [contentType][] adjunta el recurso **columnDefinition** de un sitio a ese tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="4d646-103">A **columnLink** on a [contentType][] attaches a site **columnDefinition** to that content type.</span></span>

[contentType]: contentType.md

## <a name="json-representation"></a><span data-ttu-id="4d646-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4d646-105">JSON representation</span></span>

<span data-ttu-id="4d646-106">A continuación se incluye una representación JSON de un recurso **columnLink**.</span><span class="sxs-lookup"><span data-stu-id="4d646-106">Here is a JSON representation of a **baseItem** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.columnLink" } -->

```json
{
  "id": "string",
  "name": "string"
}
```

## <a name="properties"></a><span data-ttu-id="4d646-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d646-107">Properties</span></span>

| <span data-ttu-id="4d646-108">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="4d646-108">Property name</span></span> | <span data-ttu-id="4d646-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="4d646-109">Type</span></span>   | <span data-ttu-id="4d646-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4d646-110">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="4d646-111">**id**</span><span class="sxs-lookup"><span data-stu-id="4d646-111">**id**</span></span>        | <span data-ttu-id="4d646-112">string</span><span class="sxs-lookup"><span data-stu-id="4d646-112">string</span></span> | <span data-ttu-id="4d646-113">El identificador único de la columna.</span><span class="sxs-lookup"><span data-stu-id="4d646-113">The unique identifier for the column.</span></span>
| <span data-ttu-id="4d646-114">**name**</span><span class="sxs-lookup"><span data-stu-id="4d646-114">**name**</span></span>      | <span data-ttu-id="4d646-115">string</span><span class="sxs-lookup"><span data-stu-id="4d646-115">string</span></span> | <span data-ttu-id="4d646-116">El nombre de la columna de este tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="4d646-116">The name of the column  in this content type.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ColumnLink"
} -->
