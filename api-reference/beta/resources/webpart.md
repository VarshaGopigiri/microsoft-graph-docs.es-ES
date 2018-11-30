---
author: rahmit
ms.author: rahmit
ms.date: 09/01/2018
title: WebPart
ms.openlocfilehash: e9bb612e20bc3d2416503f571f5abf364215efb2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27086144"
---
# <a name="webpart-resource"></a><span data-ttu-id="d8dbb-102">recursos de webPart</span><span class="sxs-lookup"><span data-stu-id="d8dbb-102">webPart resource</span></span>

> <span data-ttu-id="d8dbb-103">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d8dbb-103">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d8dbb-104">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d8dbb-104">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="d8dbb-105">El recurso de **webPart** representa el tipo y la información de representación de un elemento web en un [sitePage](sitepage.md).</span><span class="sxs-lookup"><span data-stu-id="d8dbb-105">The **webPart** resource represents type and rendering information for a web part on a [sitePage](sitepage.md).</span></span>

## <a name="json-representation"></a><span data-ttu-id="d8dbb-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d8dbb-106">JSON representation</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [  ],
  "@odata.type": "microsoft.graph.webPart"
}-->

```json
{
  "type": "string (guid)",
  "data": {
    "instanceId": "string (guid) (optional)"
  }
}
```

## <a name="properties"></a><span data-ttu-id="d8dbb-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d8dbb-107">Properties</span></span>

| <span data-ttu-id="d8dbb-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d8dbb-108">Property</span></span>                | <span data-ttu-id="d8dbb-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="d8dbb-109">Type</span></span>             | <span data-ttu-id="d8dbb-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d8dbb-110">Description</span></span>
|:------------------------|:-----------------|:----------------------------------
| <span data-ttu-id="d8dbb-111">**type**</span><span class="sxs-lookup"><span data-stu-id="d8dbb-111">**type**</span></span>                | <span data-ttu-id="d8dbb-112">String</span><span class="sxs-lookup"><span data-stu-id="d8dbb-112">String</span></span>           | <span data-ttu-id="d8dbb-113">Un identificador único que especifica el tipo de elemento Web.</span><span class="sxs-lookup"><span data-stu-id="d8dbb-113">A unique identifier specifying the webPart type.</span></span> <span data-ttu-id="d8dbb-114">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d8dbb-114">Read-only.</span></span>
| <span data-ttu-id="d8dbb-115">**data**</span><span class="sxs-lookup"><span data-stu-id="d8dbb-115">**data**</span></span>                | <span data-ttu-id="d8dbb-116">[sitePageData][]</span><span class="sxs-lookup"><span data-stu-id="d8dbb-116">[sitePageData][]</span></span> | <span data-ttu-id="d8dbb-117">Las propiedades necesarias para el elemento Web (varía según el elemento Web)</span><span class="sxs-lookup"><span data-stu-id="d8dbb-117">The required properties for the webPart (varies by webPart)</span></span>

[sitePageData]: sitepagedata.md

## <a name="remarks"></a><span data-ttu-id="d8dbb-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d8dbb-119">Remarks</span></span>

<span data-ttu-id="d8dbb-120">Elementos Web pueden definir sus propias propiedades necesarias en los **datos**.</span><span class="sxs-lookup"><span data-stu-id="d8dbb-120">Web parts can define their own required properties under **data**.</span></span>

<span data-ttu-id="d8dbb-121">Para obtener más información acerca de las páginas, vea [sitePage](sitepage.md).</span><span class="sxs-lookup"><span data-stu-id="d8dbb-121">For more information about pages, see [sitePage](sitepage.md).</span></span>
<!-- {
  "type": "#page.annotation",
  "description": "Defines a control resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "Control"
} -->
