---
title: tipo de recurso commsNotifications
description: Lista de notificaciones usado por los servidores de comunicaciones para el envío de varias notificaciones en un único lote.
author: VinodRavichandran
ms.openlocfilehash: 052520a99081e5c09cd6e3ec3b74f74e9527d38d
ms.sourcegitcommit: 0b3a57ac8b99871e56389f9be15e4f96e219f635
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/20/2018
ms.locfileid: "27380453"
---
# <a name="commsnotifications-resource-type"></a><span data-ttu-id="168c0-103">tipo de recurso commsNotifications</span><span class="sxs-lookup"><span data-stu-id="168c0-103">commsNotifications resource type</span></span>

> <span data-ttu-id="168c0-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="168c0-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="168c0-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="168c0-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="168c0-106">Lista de notificaciones usado por los servidores de comunicaciones para el envío de varias notificaciones en un único lote.</span><span class="sxs-lookup"><span data-stu-id="168c0-106">List of notifications used by the Communications servers for sending multiple notifications in a single batch.</span></span>

## <a name="properties"></a><span data-ttu-id="168c0-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="168c0-107">Properties</span></span>

| <span data-ttu-id="168c0-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="168c0-108">Property</span></span>       | <span data-ttu-id="168c0-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="168c0-109">Type</span></span>                                                 | <span data-ttu-id="168c0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="168c0-110">Description</span></span>                                   |
|:---------------|:-----------------------------------------------------|:----------------------------------------------|
| <span data-ttu-id="168c0-111">valor</span><span class="sxs-lookup"><span data-stu-id="168c0-111">value</span></span>          | <span data-ttu-id="168c0-112">colección de [commsNotification](commsnotification.md)</span><span class="sxs-lookup"><span data-stu-id="168c0-112">[commsNotification](commsnotification.md) collection</span></span> | <span data-ttu-id="168c0-113">La notificación de un cambio en el recurso.</span><span class="sxs-lookup"><span data-stu-id="168c0-113">The notification of a change in the resource.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="168c0-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="168c0-114">JSON representation</span></span>

<span data-ttu-id="168c0-115">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="168c0-115">The following is a JSON representation of the resource.</span></span>

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