---
title: tipo de recurso synchronizationError
description: Representa un error que se produjo durante el proceso de sincronización.
localization_priority: Normal
ms.openlocfilehash: cc6b58444ac56303bfd2e41f1fcae17658f6aea9
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27847246"
---
# <a name="synchronizationerror-resource-type"></a><span data-ttu-id="50058-103">tipo de recurso synchronizationError</span><span class="sxs-lookup"><span data-stu-id="50058-103">synchronizationError resource type</span></span>

> <span data-ttu-id="50058-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="50058-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="50058-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="50058-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="50058-106">Representa un error que se produjo durante el proceso de sincronización.</span><span class="sxs-lookup"><span data-stu-id="50058-106">Represents an error that occurred during the synchronization process.</span></span>

## <a name="properties"></a><span data-ttu-id="50058-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="50058-107">Properties</span></span>

<!-- Add descriptions for the properties. -->
| <span data-ttu-id="50058-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="50058-108">Property</span></span>     | <span data-ttu-id="50058-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="50058-109">Type</span></span>   |<span data-ttu-id="50058-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="50058-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="50058-111">código</span><span class="sxs-lookup"><span data-stu-id="50058-111">code</span></span>|<span data-ttu-id="50058-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="50058-112">String</span></span>||
|<span data-ttu-id="50058-113">message</span><span class="sxs-lookup"><span data-stu-id="50058-113">message</span></span>|<span data-ttu-id="50058-114">String</span><span class="sxs-lookup"><span data-stu-id="50058-114">String</span></span>||
|<span data-ttu-id="50058-115">tenantActionable</span><span class="sxs-lookup"><span data-stu-id="50058-115">tenantActionable</span></span>|<span data-ttu-id="50058-116">Booleano</span><span class="sxs-lookup"><span data-stu-id="50058-116">Boolean</span></span>||

## <a name="json-representation"></a><span data-ttu-id="50058-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="50058-117">JSON representation</span></span>

<span data-ttu-id="50058-118">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="50058-118">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.synchronizationError"
}-->

```json
{
  "code": "String",
  "message": "String",
  "tenantActionable": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "synchronizationError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
