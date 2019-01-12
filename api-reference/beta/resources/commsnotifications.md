---
title: tipo de recurso commsNotifications
description: Lista de notificaciones usado por los servidores de comunicaciones para el envío de varias notificaciones en un único lote.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 83a89e848d0992d253efb532ed078031b6f965d2
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27946304"
---
# <a name="commsnotifications-resource-type"></a><span data-ttu-id="8ba8b-103">tipo de recurso commsNotifications</span><span class="sxs-lookup"><span data-stu-id="8ba8b-103">commsNotifications resource type</span></span>

> <span data-ttu-id="8ba8b-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8ba8b-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8ba8b-106">Lista de notificaciones usado por los servidores de comunicaciones para el envío de varias notificaciones en un único lote.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-106">List of notifications used by the Communications servers for sending multiple notifications in a single batch.</span></span>

## <a name="properties"></a><span data-ttu-id="8ba8b-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8ba8b-107">Properties</span></span>

| <span data-ttu-id="8ba8b-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8ba8b-108">Property</span></span>       | <span data-ttu-id="8ba8b-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8ba8b-109">Type</span></span>                                                 | <span data-ttu-id="8ba8b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ba8b-110">Description</span></span>                                   |
|:---------------|:-----------------------------------------------------|:----------------------------------------------|
| <span data-ttu-id="8ba8b-111">valor</span><span class="sxs-lookup"><span data-stu-id="8ba8b-111">value</span></span>          | <span data-ttu-id="8ba8b-112">colección de [commsNotification](commsnotification.md)</span><span class="sxs-lookup"><span data-stu-id="8ba8b-112">[commsNotification](commsnotification.md) collection</span></span> | <span data-ttu-id="8ba8b-113">La notificación de un cambio en el recurso.</span><span class="sxs-lookup"><span data-stu-id="8ba8b-113">The notification of a change in the resource.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="8ba8b-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8ba8b-114">JSON representation</span></span>

<span data-ttu-id="8ba8b-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8ba8b-115">The following is a JSON representation of the resource.</span></span>

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
