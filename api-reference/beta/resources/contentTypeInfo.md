---
author: daspek
ms.author: dspektor
ms.date: 09/12/2017
title: ContentTypeInfo
ms.openlocfilehash: 922f87c77280627efb956e4558e1ff269daa9311
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27087459"
---
# <a name="contenttypeinfo-resource-type"></a><span data-ttu-id="dbb05-102">Tipo de recurso ContentTypeInfo</span><span class="sxs-lookup"><span data-stu-id="dbb05-102">ContentTypeInfo resource type</span></span>

> <span data-ttu-id="dbb05-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="dbb05-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="dbb05-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="dbb05-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="dbb05-105">El recurso **contentTypeInfo** indica el tipo de contenido de SharePoint de un elemento.</span><span class="sxs-lookup"><span data-stu-id="dbb05-105">The **contentTypeInfo** resource indicates the SharePoint content type of an item.</span></span>

## <a name="json-representation"></a><span data-ttu-id="dbb05-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dbb05-106">JSON representation</span></span>

<span data-ttu-id="dbb05-107">A continuación se incluye una representación JSON de un recurso **ContentTypeInfo**.</span><span class="sxs-lookup"><span data-stu-id="dbb05-107">Here is a JSON representation of a **contentTypeInfo** resource.</span></span>
<!-- { "blockType": "resource", "@odata.type": "microsoft.graph.contentTypeInfo", "@type.aka": "oneDrive.contentTypeFacet" } -->

```json
{
  "id": "string",
  "name": "string"
}
```

## <a name="properties"></a><span data-ttu-id="dbb05-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dbb05-108">Properties</span></span>

| <span data-ttu-id="dbb05-109">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="dbb05-109">Property name</span></span>  | <span data-ttu-id="dbb05-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="dbb05-110">Type</span></span>    | <span data-ttu-id="dbb05-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbb05-111">Description</span></span>
|:---------------|:--------|:--------------------------------------------------
| <span data-ttu-id="dbb05-112">**id**</span><span class="sxs-lookup"><span data-stu-id="dbb05-112">**id**</span></span>         | <span data-ttu-id="dbb05-113">string</span><span class="sxs-lookup"><span data-stu-id="dbb05-113">string</span></span>  | <span data-ttu-id="dbb05-114">El identificador del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="dbb05-114">The id of the content type.</span></span>
| <span data-ttu-id="dbb05-115">**name**</span><span class="sxs-lookup"><span data-stu-id="dbb05-115">**name**</span></span>       | <span data-ttu-id="dbb05-116">string</span><span class="sxs-lookup"><span data-stu-id="dbb05-116">string</span></span>  | <span data-ttu-id="dbb05-117">El nombre del tipo de contenido.</span><span class="sxs-lookup"><span data-stu-id="dbb05-117">The name of the content type.</span></span>

<!-- {
  "type": "#page.annotation",
  "description": "",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Resources/ContentTypeInfo"
} -->
