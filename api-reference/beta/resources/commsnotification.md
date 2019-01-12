---
title: tipo de recurso commsNotification
description: Comunicaciones base tipo de notificación que se publicará por los servidores de comunicaciones para notificar a los cambios.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: e5b929997cf17d13043264d42421418321aae84e
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27977699"
---
# <a name="commsnotification-resource-type"></a><span data-ttu-id="8a61f-103">tipo de recurso commsNotification</span><span class="sxs-lookup"><span data-stu-id="8a61f-103">commsNotification resource type</span></span>

> <span data-ttu-id="8a61f-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="8a61f-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="8a61f-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="8a61f-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="8a61f-106">Comunicaciones base tipo de notificación que se publicará por los servidores de comunicaciones para notificar a los cambios.</span><span class="sxs-lookup"><span data-stu-id="8a61f-106">Communications notification base type that is published by Communications servers to notify changes.</span></span>

## <a name="properties"></a><span data-ttu-id="8a61f-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8a61f-107">Properties</span></span>
| <span data-ttu-id="8a61f-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="8a61f-108">Property</span></span>       | <span data-ttu-id="8a61f-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="8a61f-109">Type</span></span>    | <span data-ttu-id="8a61f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="8a61f-110">Description</span></span>                                                |
|:---------------|:--------|:-----------------------------------------------------------|
| <span data-ttu-id="8a61f-111">changeType</span><span class="sxs-lookup"><span data-stu-id="8a61f-111">changeType</span></span>     | <span data-ttu-id="8a61f-112">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a61f-112">String</span></span>  | <span data-ttu-id="8a61f-113">Los valores posibles son: `created`, `updated` y `deleted`.</span><span class="sxs-lookup"><span data-stu-id="8a61f-113">Possible values are: `created`, `updated`, `deleted`.</span></span>      |
| <span data-ttu-id="8a61f-114">resource</span><span class="sxs-lookup"><span data-stu-id="8a61f-114">resource</span></span>       | <span data-ttu-id="8a61f-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="8a61f-115">String</span></span>  | <span data-ttu-id="8a61f-116">URI del recurso que se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="8a61f-116">URI of the resource that was changed.</span></span>                      |

> <span data-ttu-id="8a61f-117">**Nota:** `resourceData` está disponible como datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="8a61f-117">**Note:** `resourceData` is available as additional data.</span></span> <span data-ttu-id="8a61f-118">Es una entidad o Collection(entity) según el número de empaquetado en la notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="8a61f-118">It is an entity or Collection(entity) depending on the number of changes packaged in the notification.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8a61f-119">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8a61f-119">JSON representation</span></span>

<span data-ttu-id="8a61f-120">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8a61f-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "resourceData"
  ],
  "@odata.type": "microsoft.graph.commsNotification",
  "openType": true
}-->
```json
{
  "changeType": "created | updated | deleted",
  "resource": "String"
}
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications",
  "truncated": true
}-->
```json
{
  "value": [
    {
      "changeType": "created",
      "resource": "/app/calls/1D6DE2D4-CD51-4309-8DAA-70768651088E",
      "resourceData": {
        "@odata.type": "#microsoft.graph.call",
        "id": "1D6DE2D4-CD51-4309-8DAA-70768651088E",
        "state": "incoming"
      }
    }
  ]
}
```

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.commsNotifications",
  "truncated": true
}-->
```json
{
  "value": [
    {
      "changeType": "created",
      "resource": "/app/calls/1D6DE2D4-CD51-4309-8DAA-70768651088E/participants",
      "resourceData": [
        {
          "@odata.type": "#microsoft.graph.participant",
          "id": "1D6DE2D4-CD51-4309-8DAA-70768651088E"
        },
        {
          "@odata.type": "#microsoft.graph.participant",
          "id": "8fcb5dbc-d5aa-4681-8e31-b001d5168d79"
        }
      ]
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "commsNotification resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
