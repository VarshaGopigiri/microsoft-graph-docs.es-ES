---
title: tipo de recurso de notificaciones
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: 96246491c386971fe18184f26269d4abe3af6e6e
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27090834"
---
# <a name="notifications-resource-type"></a><span data-ttu-id="b4759-103">tipo de recurso de notificaciones</span><span class="sxs-lookup"><span data-stu-id="b4759-103">notifications resource type</span></span>

> <span data-ttu-id="b4759-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="b4759-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="b4759-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="b4759-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="properties"></a><span data-ttu-id="b4759-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b4759-106">Properties</span></span>

| <span data-ttu-id="b4759-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b4759-107">Property</span></span>       | <span data-ttu-id="b4759-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="b4759-108">Type</span></span>                                       | <span data-ttu-id="b4759-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4759-109">Description</span></span> |
|:---------------|:-------------------------------------------|:------------|
| <span data-ttu-id="b4759-110">valor</span><span class="sxs-lookup"><span data-stu-id="b4759-110">value</span></span>          | <span data-ttu-id="b4759-111">colección de [notificación](commsnotification.md)</span><span class="sxs-lookup"><span data-stu-id="b4759-111">[notification](commsnotification.md) collection</span></span> | <span data-ttu-id="b4759-112">La notificación de un cambio en el recurso.</span><span class="sxs-lookup"><span data-stu-id="b4759-112">The notification of a change in the resource.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="b4759-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="b4759-113">JSON representation</span></span>

<span data-ttu-id="b4759-114">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="b4759-114">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.commsNotifications"
}-->
```json
{
  "value": [ { "@odata.type": "#microsoft.graph.commsNotification" } ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notifications resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->