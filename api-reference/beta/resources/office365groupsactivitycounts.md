---
title: tipo de recurso office365GroupsActivityCounts
description: La siguiente es una representación JSON del recurso
localization_priority: Normal
ms.openlocfilehash: 87867071545a36f7aca1833a369f919317153bc6
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27874112"
---
# <a name="office365groupsactivitycounts-resource-type"></a><span data-ttu-id="74d46-103">tipo de recurso office365GroupsActivityCounts</span><span class="sxs-lookup"><span data-stu-id="74d46-103">office365GroupsActivityCounts resource type</span></span>

## <a name="properties"></a><span data-ttu-id="74d46-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="74d46-104">Properties</span></span>

| <span data-ttu-id="74d46-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="74d46-105">Property</span></span>               | <span data-ttu-id="74d46-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="74d46-106">Type</span></span>   | <span data-ttu-id="74d46-107">Description</span><span class="sxs-lookup"><span data-stu-id="74d46-107">Description</span></span>                              |
| :--------------------- | :----- | ---------------------------------------- |
| <span data-ttu-id="74d46-108">reportRefreshDate</span><span class="sxs-lookup"><span data-stu-id="74d46-108">reportRefreshDate</span></span>      | <span data-ttu-id="74d46-109">Fecha</span><span class="sxs-lookup"><span data-stu-id="74d46-109">Date</span></span>   | <span data-ttu-id="74d46-110">La fecha más reciente del contenido.</span><span class="sxs-lookup"><span data-stu-id="74d46-110">The latest date of the content.</span></span>          |
| <span data-ttu-id="74d46-111">exchangeEmailsReceived</span><span class="sxs-lookup"><span data-stu-id="74d46-111">exchangeEmailsReceived</span></span> | <span data-ttu-id="74d46-112">Int64</span><span class="sxs-lookup"><span data-stu-id="74d46-112">Int64</span></span>  | <span data-ttu-id="74d46-113">El número de mensajes de correo electrónico recibidos por los buzones de grupo.</span><span class="sxs-lookup"><span data-stu-id="74d46-113">The number of emails received by Group mailboxes.</span></span> |
| <span data-ttu-id="74d46-114">yammerMessagesPosted</span><span class="sxs-lookup"><span data-stu-id="74d46-114">yammerMessagesPosted</span></span>   | <span data-ttu-id="74d46-115">Int64</span><span class="sxs-lookup"><span data-stu-id="74d46-115">Int64</span></span>  | <span data-ttu-id="74d46-116">El número de los mensajes enviados a grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="74d46-116">The number of messages posted to Yammer groups.</span></span> |
| <span data-ttu-id="74d46-117">yammerMessagesRead</span><span class="sxs-lookup"><span data-stu-id="74d46-117">yammerMessagesRead</span></span>     | <span data-ttu-id="74d46-118">Int64</span><span class="sxs-lookup"><span data-stu-id="74d46-118">Int64</span></span>  | <span data-ttu-id="74d46-119">El número de mensajes leídos en grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="74d46-119">The number of messages read in Yammer groups.</span></span> |
| <span data-ttu-id="74d46-120">yammerMessagesLiked</span><span class="sxs-lookup"><span data-stu-id="74d46-120">yammerMessagesLiked</span></span>    | <span data-ttu-id="74d46-121">Int64</span><span class="sxs-lookup"><span data-stu-id="74d46-121">Int64</span></span>  | <span data-ttu-id="74d46-122">El número de mensajes en grupos de Yammer.</span><span class="sxs-lookup"><span data-stu-id="74d46-122">The number of messages liked in Yammer groups.</span></span> |
| <span data-ttu-id="74d46-123">reportDate</span><span class="sxs-lookup"><span data-stu-id="74d46-123">reportDate</span></span>             | <span data-ttu-id="74d46-124">Fecha</span><span class="sxs-lookup"><span data-stu-id="74d46-124">Date</span></span>   | <span data-ttu-id="74d46-125">La fecha en la que un número de mensajes de correo electrónico se han enviado a un buzón de grupo o un número de mensajes se contabilizaron, leer o gustado en un grupo de Yammer</span><span class="sxs-lookup"><span data-stu-id="74d46-125">The date on which a number of emails were sent to a group mailbox or a number of messages were posted, read, or liked in a Yammer group</span></span> |
| <span data-ttu-id="74d46-126">reportPeriod</span><span class="sxs-lookup"><span data-stu-id="74d46-126">reportPeriod</span></span>           | <span data-ttu-id="74d46-127">Cadena</span><span class="sxs-lookup"><span data-stu-id="74d46-127">String</span></span> | <span data-ttu-id="74d46-128">El número de días que cubre el informe.</span><span class="sxs-lookup"><span data-stu-id="74d46-128">The number of days the report covers.</span></span>    |

## <a name="json-representation"></a><span data-ttu-id="74d46-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="74d46-129">JSON representation</span></span>

<span data-ttu-id="74d46-130">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="74d46-130">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.office365GroupsActivityCounts"
} -->

```json
{
  "reportRefreshDate": "Date", 
  "exchangeEmailsReceived": 1024, 
  "yammerMessagesPosted": 1024, 
  "yammerMessagesRead": 1024, 
  "yammerMessagesLiked": 1024, 
  "reportDate": "Date", 
  "reportPeriod": "String"
}
```
