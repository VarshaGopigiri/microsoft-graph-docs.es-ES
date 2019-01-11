---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ColumnLink
localization_priority: Normal
ms.openlocfilehash: 226666875b9364f33954e7f932227562a9734267
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27888574"
---
# <a name="columnlink-resource-type"></a><span data-ttu-id="054f7-102">Tipo de recurso ColumnLink</span><span class="sxs-lookup"><span data-stu-id="054f7-102">ColumnLink resource type</span></span>

> <span data-ttu-id="054f7-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="054f7-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="054f7-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="054f7-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="054f7-105">Un recurso **columnLink** en un recurso [contentType][] adjunta el recurso **columnDefinition** de un sitio a ese tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="054f7-105">A **columnLink** on a [contentType][] attaches a site **columnDefinition** to that content type.</span></span>

[contentType]: contenttype.md

## <a name="json-representation"></a><span data-ttu-id="054f7-107">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="054f7-107">JSON representation</span></span>

<span data-ttu-id="054f7-108">A continuación se incluye una representación JSON de un recurso **columnLink**.</span><span class="sxs-lookup"><span data-stu-id="054f7-108">Here is a JSON representation of a **columnLink** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.columnLink" } -->

```json
{
  "id": "string",
  "name": "string"
}
```

## <a name="properties"></a><span data-ttu-id="054f7-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="054f7-109">Properties</span></span>

| <span data-ttu-id="054f7-110">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="054f7-110">Property name</span></span> | <span data-ttu-id="054f7-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="054f7-111">Type</span></span>   | <span data-ttu-id="054f7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="054f7-112">Description</span></span>
|:--------------|:-------|:----------------------------------------------------
| <span data-ttu-id="054f7-113">**id**</span><span class="sxs-lookup"><span data-stu-id="054f7-113">**id**</span></span>        | <span data-ttu-id="054f7-114">string</span><span class="sxs-lookup"><span data-stu-id="054f7-114">string</span></span> | <span data-ttu-id="054f7-115">El identificador único de la columna.</span><span class="sxs-lookup"><span data-stu-id="054f7-115">The unique identifier for the column.</span></span>
| <span data-ttu-id="054f7-116">**name**</span><span class="sxs-lookup"><span data-stu-id="054f7-116">**name**</span></span>      | <span data-ttu-id="054f7-117">string</span><span class="sxs-lookup"><span data-stu-id="054f7-117">string</span></span> | <span data-ttu-id="054f7-118">El nombre de la columna de este tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="054f7-118">The name of the column  in this content type.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ColumnLink"
} -->
