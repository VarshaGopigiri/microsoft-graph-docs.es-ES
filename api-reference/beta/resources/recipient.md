---
title: Tipo de recurso recipient
description: 'Representa información sobre un usuario en la finalización del envío o la recepción de un evento, un mensaje o una publicación de grupo. '
ms.openlocfilehash: 2ecf92f314c8b29da529b8dc07cada71dd8571f2
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27088885"
---
# <a name="recipient-resource-type"></a><span data-ttu-id="285a5-103">Tipo de recurso recipient</span><span class="sxs-lookup"><span data-stu-id="285a5-103">recipient resource type</span></span>

> <span data-ttu-id="285a5-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="285a5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="285a5-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="285a5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="285a5-106">Representa información sobre un usuario en la finalización del envío o la recepción de un evento, un mensaje o una publicación de grupo.</span><span class="sxs-lookup"><span data-stu-id="285a5-106">Represents information about a user in the sending or receiving end of an event, message or group post.</span></span> 

## <a name="properties"></a><span data-ttu-id="285a5-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="285a5-107">Properties</span></span>
| <span data-ttu-id="285a5-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="285a5-108">Property</span></span>     | <span data-ttu-id="285a5-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="285a5-109">Type</span></span>   |<span data-ttu-id="285a5-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="285a5-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="285a5-111">emailAddress</span><span class="sxs-lookup"><span data-stu-id="285a5-111">emailAddress</span></span>|[<span data-ttu-id="285a5-112">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="285a5-112">EmailAddress</span></span>](emailaddress.md)|<span data-ttu-id="285a5-113">Dirección de correo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="285a5-113">The recipient's email address.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="285a5-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="285a5-114">JSON representation</span></span>

<span data-ttu-id="285a5-115">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="285a5-115">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recipient"
}-->

```json
{
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recipient resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->