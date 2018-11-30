---
title: tipo de recurso de los destinatarios
description: Aquí tiene una representación JSON del recurso
ms.openlocfilehash: aa620fa920b4f91b2b2214f02c2e75d7a8cbcc4f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089870"
---
# <a name="recipients-resource-type"></a><span data-ttu-id="b5c6b-103">tipo de recurso de los destinatarios</span><span class="sxs-lookup"><span data-stu-id="b5c6b-103">recipients resource type</span></span>

> <span data-ttu-id="b5c6b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b5c6b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b5c6b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b5c6b-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b5c6b-106">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b5c6b-106">JSON representation</span></span>

<span data-ttu-id="b5c6b-107">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b5c6b-107">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recipients"
}-->

```json
{
  "alias": "string",
  "email": "string",
  "objectId": "string",
  "permissionIdentityType": "string"
}

```
## <a name="properties"></a><span data-ttu-id="b5c6b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b5c6b-108">Properties</span></span>
| <span data-ttu-id="b5c6b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b5c6b-109">Property</span></span>     | <span data-ttu-id="b5c6b-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="b5c6b-110">Type</span></span>   |<span data-ttu-id="b5c6b-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="b5c6b-111">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="b5c6b-112">alias</span><span class="sxs-lookup"><span data-stu-id="b5c6b-112">alias</span></span>|<span data-ttu-id="b5c6b-113">String</span><span class="sxs-lookup"><span data-stu-id="b5c6b-113">String</span></span>||
|<span data-ttu-id="b5c6b-114">email</span><span class="sxs-lookup"><span data-stu-id="b5c6b-114">email</span></span>|<span data-ttu-id="b5c6b-115">String</span><span class="sxs-lookup"><span data-stu-id="b5c6b-115">String</span></span>||
|<span data-ttu-id="b5c6b-116">objectId</span><span class="sxs-lookup"><span data-stu-id="b5c6b-116">objectId</span></span>|<span data-ttu-id="b5c6b-117">String</span><span class="sxs-lookup"><span data-stu-id="b5c6b-117">String</span></span>||
|<span data-ttu-id="b5c6b-118">permissionIdentityType</span><span class="sxs-lookup"><span data-stu-id="b5c6b-118">permissionIdentityType</span></span>|<span data-ttu-id="b5c6b-119">String</span><span class="sxs-lookup"><span data-stu-id="b5c6b-119">String</span></span>||

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recipients resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->