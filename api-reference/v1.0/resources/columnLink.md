---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ColumnLink
ms.openlocfilehash: cdae360afb6e626ee481a7e98ed5f90e657203b2
ms.sourcegitcommit: abf4b739257e3ffd9d045f783ec595d846172590
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2018
ms.locfileid: "23265123"
---
# <a name="columnlink-resource-type"></a><span data-ttu-id="b6489-102">Tipo de recurso ColumnLink</span><span class="sxs-lookup"><span data-stu-id="b6489-102">ColumnLink resource type</span></span>

<span data-ttu-id="b6489-103">Un recurso **columnLink** en un recurso [contentType][] adjunta el recurso **columnDefinition** de un sitio a ese tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="b6489-103">A **columnLink** on a [contentType][] attaches a site **columnDefinition** to that content type.</span></span>

[contentType]: contentType.md

## <a name="json-representation"></a><span data-ttu-id="b6489-105">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b6489-105">JSON representation</span></span>

<span data-ttu-id="b6489-106">A continuación se incluye una representación JSON de un recurso **columnLink**.</span><span class="sxs-lookup"><span data-stu-id="b6489-106">Here is a JSON representation of a **columnLink** resource.</span></span>
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

## <a name="properties"></a><span data-ttu-id="b6489-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6489-107">Properties</span></span>

| <span data-ttu-id="b6489-108">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="b6489-108">Property name</span></span> | <span data-ttu-id="b6489-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="b6489-109">Type</span></span>   | <span data-ttu-id="b6489-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b6489-110">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="b6489-111">**id**</span><span class="sxs-lookup"><span data-stu-id="b6489-111">**id**</span></span>        | <span data-ttu-id="b6489-112">cadena</span><span class="sxs-lookup"><span data-stu-id="b6489-112">string</span></span> | <span data-ttu-id="b6489-113">El identificador único de la columna.</span><span class="sxs-lookup"><span data-stu-id="b6489-113">The unique identifier for the column.</span></span>
| <span data-ttu-id="b6489-114">**name**</span><span class="sxs-lookup"><span data-stu-id="b6489-114">**name**</span></span>      | <span data-ttu-id="b6489-115">string</span><span class="sxs-lookup"><span data-stu-id="b6489-115">string</span></span> | <span data-ttu-id="b6489-116">El nombre de la columna de este tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="b6489-116">The name of the column  in this content type.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ColumnLink"
} -->
