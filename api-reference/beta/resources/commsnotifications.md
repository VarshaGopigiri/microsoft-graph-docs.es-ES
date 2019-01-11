---
title: tipo de recurso commsNotifications
description: Lista de notificaciones usado por los servidores de comunicaciones para el envío de varias notificaciones en un único lote.
author: VinodRavichandran
localization_priority: Normal
ms.openlocfilehash: 9ce629e17c85806d7e05bce99d6a62f9fa9cbff8
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27851502"
---
# <a name="commsnotifications-resource-type"></a><span data-ttu-id="ccef3-103">tipo de recurso commsNotifications</span><span class="sxs-lookup"><span data-stu-id="ccef3-103">commsNotifications resource type</span></span>

> <span data-ttu-id="ccef3-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="ccef3-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="ccef3-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="ccef3-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="ccef3-106">Lista de notificaciones usado por los servidores de comunicaciones para el envío de varias notificaciones en un único lote.</span><span class="sxs-lookup"><span data-stu-id="ccef3-106">List of notifications used by the Communications servers for sending multiple notifications in a single batch.</span></span>

## <a name="properties"></a><span data-ttu-id="ccef3-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ccef3-107">Properties</span></span>

| <span data-ttu-id="ccef3-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ccef3-108">Property</span></span>       | <span data-ttu-id="ccef3-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccef3-109">Type</span></span>                                                 | <span data-ttu-id="ccef3-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccef3-110">Description</span></span>                                   |
|:---------------|:-----------------------------------------------------|:----------------------------------------------|
| <span data-ttu-id="ccef3-111">valor</span><span class="sxs-lookup"><span data-stu-id="ccef3-111">value</span></span>          | <span data-ttu-id="ccef3-112">colección de [commsNotification](commsnotification.md)</span><span class="sxs-lookup"><span data-stu-id="ccef3-112">[commsNotification](commsnotification.md) collection</span></span> | <span data-ttu-id="ccef3-113">La notificación de un cambio en el recurso.</span><span class="sxs-lookup"><span data-stu-id="ccef3-113">The notification of a change in the resource.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="ccef3-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ccef3-114">JSON representation</span></span>

<span data-ttu-id="ccef3-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ccef3-115">The following is a JSON representation of the resource.</span></span>

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
  "description": "commsNotifications resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
