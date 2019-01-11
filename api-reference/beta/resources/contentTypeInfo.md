---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ContentTypeInfo
localization_priority: Normal
ms.openlocfilehash: e394d52a5f7ed5e8dce1c61d31d787d62bd36e56
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27892340"
---
# <a name="contenttypeinfo-resource-type"></a><span data-ttu-id="706cb-102">Tipo de recurso ContentTypeInfo</span><span class="sxs-lookup"><span data-stu-id="706cb-102">ContentTypeInfo resource type</span></span>

> <span data-ttu-id="706cb-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="706cb-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="706cb-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="706cb-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="706cb-105">El recurso **contentTypeInfo** indica el tipo de contenido de SharePoint de un elemento.</span><span class="sxs-lookup"><span data-stu-id="706cb-105">The **contentTypeInfo** resource indicates the SharePoint content type of an item.</span></span>

## <a name="json-representation"></a><span data-ttu-id="706cb-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="706cb-106">JSON representation</span></span>

<span data-ttu-id="706cb-107">A continuación se incluye una representación JSON de un recurso **ContentTypeInfo**.</span><span class="sxs-lookup"><span data-stu-id="706cb-107">Here is a JSON representation of a **contentTypeInfo** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.contentTypeInfo", "@type.aka": "oneDrive.contentTypeFacet" } -->

```json
{
  "id": "string",
  "name": "string"
}
```

## <a name="properties"></a><span data-ttu-id="706cb-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="706cb-108">Properties</span></span>

| <span data-ttu-id="706cb-109">Nombre de la propiedad</span><span class="sxs-lookup"><span data-stu-id="706cb-109">Property name</span></span>  | <span data-ttu-id="706cb-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="706cb-110">Type</span></span>    | <span data-ttu-id="706cb-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="706cb-111">Description</span></span>
|:---------------|:--------|:--------------------------------------------------
| <span data-ttu-id="706cb-112">**id**</span><span class="sxs-lookup"><span data-stu-id="706cb-112">**id**</span></span>         | <span data-ttu-id="706cb-113">string</span><span class="sxs-lookup"><span data-stu-id="706cb-113">string</span></span>  | <span data-ttu-id="706cb-114">El identificador del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="706cb-114">The id of the content type.</span></span>
| <span data-ttu-id="706cb-115">**name**</span><span class="sxs-lookup"><span data-stu-id="706cb-115">**name**</span></span>       | <span data-ttu-id="706cb-116">string</span><span class="sxs-lookup"><span data-stu-id="706cb-116">string</span></span>  | <span data-ttu-id="706cb-117">El nombre del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="706cb-117">The name of the content type.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentTypeInfo"
} -->
