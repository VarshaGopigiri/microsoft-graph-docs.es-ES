---
title: tipo de recurso de notificación
description: La siguiente es una representación JSON del recurso
ms.openlocfilehash: c09927cbe133c945b83a3bfc1b0eb74ef00bce2b
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27089599"
---
# <a name="notification-resource-type"></a><span data-ttu-id="d1801-103">tipo de recurso de notificación</span><span class="sxs-lookup"><span data-stu-id="d1801-103">notification resource type</span></span>

> <span data-ttu-id="d1801-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="d1801-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="d1801-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="d1801-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="properties"></a><span data-ttu-id="d1801-106">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d1801-106">Properties</span></span>
| <span data-ttu-id="d1801-107">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d1801-107">Property</span></span>       | <span data-ttu-id="d1801-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1801-108">Type</span></span>    | <span data-ttu-id="d1801-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1801-109">Description</span></span>                                                |
|:---------------|:--------|:-----------------------------------------------------------|
| <span data-ttu-id="d1801-110">changeType</span><span class="sxs-lookup"><span data-stu-id="d1801-110">changeType</span></span>     | <span data-ttu-id="d1801-111">String</span><span class="sxs-lookup"><span data-stu-id="d1801-111">String</span></span>  | <span data-ttu-id="d1801-112">Los valores posibles son: `created`, `updated` y `deleted`.</span><span class="sxs-lookup"><span data-stu-id="d1801-112">Possible values are: `created`, `updated`, `deleted`.</span></span>      |
| <span data-ttu-id="d1801-113">resource</span><span class="sxs-lookup"><span data-stu-id="d1801-113">resource</span></span>       | <span data-ttu-id="d1801-114">String</span><span class="sxs-lookup"><span data-stu-id="d1801-114">String</span></span>  | <span data-ttu-id="d1801-115">URI del recurso que se ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="d1801-115">URI of the resource that was changed.</span></span>                      |

> <span data-ttu-id="d1801-116">**Nota:** `resourceData` está disponible como datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="d1801-116">**Note:** `resourceData` is available as additional data.</span></span> <span data-ttu-id="d1801-117">Es una entidad o Collection(entity) según el número de empaquetado en la notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="d1801-117">It is an entity or Collection(entity) depending on the number of changes packaged in the notification.</span></span>

## <a name="json-representation"></a><span data-ttu-id="d1801-118">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d1801-118">JSON representation</span></span>

<span data-ttu-id="d1801-119">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d1801-119">The following is a JSON representation of the resource.</span></span>

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
  "description": "notification resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->