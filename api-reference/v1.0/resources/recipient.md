---
title: Tipo de recurso recipient
description: 'Representa información sobre un usuario en la finalización del envío o la recepción de un evento, un mensaje o una publicación de grupo. '
ms.openlocfilehash: 7ae272d239f44c3d2f709a03438facb2f0247e49
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/29/2018
ms.locfileid: "27029165"
---
# <a name="recipient-resource-type"></a><span data-ttu-id="0c243-103">Tipo de recurso recipient</span><span class="sxs-lookup"><span data-stu-id="0c243-103">recipient resource type</span></span>

<span data-ttu-id="0c243-104">Representa información sobre un usuario en la finalización del envío o la recepción de un evento, un mensaje o una publicación de grupo.</span><span class="sxs-lookup"><span data-stu-id="0c243-104">Represents information about a user in the sending or receiving end of an event, message or group post.</span></span> 

## <a name="properties"></a><span data-ttu-id="0c243-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c243-105">Properties</span></span>
| <span data-ttu-id="0c243-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0c243-106">Property</span></span>     | <span data-ttu-id="0c243-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c243-107">Type</span></span>   |<span data-ttu-id="0c243-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c243-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0c243-109">emailAddress</span><span class="sxs-lookup"><span data-stu-id="0c243-109">emailAddress</span></span>|[<span data-ttu-id="0c243-110">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="0c243-110">EmailAddress</span></span>](emailaddress.md)|<span data-ttu-id="0c243-111">Dirección de correo del destinatario.</span><span class="sxs-lookup"><span data-stu-id="0c243-111">The recipient's email address.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="0c243-112">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0c243-112">JSON representation</span></span>

<span data-ttu-id="0c243-113">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0c243-113">Here is a JSON representation of the resource</span></span>

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