---
title: Tipo de recurso messageRuleActions
description: Representa el conjunto de acciones que están disponibles para una regla.
author: angelgolfer-ms
ms.openlocfilehash: c65e950fbe440ba6e453856b034036fada657f0b
ms.sourcegitcommit: 6a82bf240a3cfc0baabd227349e08a08311e3d44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/18/2018
ms.locfileid: "27347351"
---
# <a name="messageruleactions-resource-type"></a><span data-ttu-id="100d2-103">Tipo de recurso messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="100d2-103">messageRuleActions resource type</span></span>


<span data-ttu-id="100d2-104">Representa el conjunto de acciones que están disponibles para una regla.</span><span class="sxs-lookup"><span data-stu-id="100d2-104">Represents the set of actions that are available to a rule.</span></span>

## <a name="properties"></a><span data-ttu-id="100d2-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="100d2-105">Properties</span></span>
| <span data-ttu-id="100d2-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="100d2-106">Property</span></span>     | <span data-ttu-id="100d2-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="100d2-107">Type</span></span>   |<span data-ttu-id="100d2-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="100d2-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="100d2-109">assignCategories</span><span class="sxs-lookup"><span data-stu-id="100d2-109">assignCategories</span></span> | <span data-ttu-id="100d2-110">Colección String</span><span class="sxs-lookup"><span data-stu-id="100d2-110">String collection</span></span> | <span data-ttu-id="100d2-111">Lista de categorías que se asignarán a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="100d2-111">A list of categories to be assigned to a message.</span></span> |
| <span data-ttu-id="100d2-112">copyToFolder</span><span class="sxs-lookup"><span data-stu-id="100d2-112">copyToFolder</span></span> | <span data-ttu-id="100d2-113">String</span><span class="sxs-lookup"><span data-stu-id="100d2-113">String</span></span> | <span data-ttu-id="100d2-114">Identificador de la carpeta donde se va a copiar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="100d2-114">The ID of a folder that a message is to be copied to.</span></span> |
| <span data-ttu-id="100d2-115">delete</span><span class="sxs-lookup"><span data-stu-id="100d2-115">delete</span></span> | <span data-ttu-id="100d2-116">Boolean</span><span class="sxs-lookup"><span data-stu-id="100d2-116">Boolean</span></span> | <span data-ttu-id="100d2-117">Indica si un mensaje se debe mover a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="100d2-117">Indicates whether a message should be moved to the Deleted Items folder.</span></span> |
| <span data-ttu-id="100d2-118">forwardAsAttachmentTo</span><span class="sxs-lookup"><span data-stu-id="100d2-118">forwardAsAttachmentTo</span></span> | <span data-ttu-id="100d2-119">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="100d2-119">[recipient](recipient.md) collection</span></span> | <span data-ttu-id="100d2-120">Direcciones de correo electrónico de los destinatarios a los que se debe reenviar un mensaje como datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="100d2-120">The email addresses of the recipients to which a message should be forwarded as an attachment.</span></span> |
| <span data-ttu-id="100d2-121">forwardTo</span><span class="sxs-lookup"><span data-stu-id="100d2-121">forwardTo</span></span> | <span data-ttu-id="100d2-122">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="100d2-122">[recipient](recipient.md) collection</span></span> | <span data-ttu-id="100d2-123">Direcciones de correo electrónico de los destinatarios a los que se debe reenviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="100d2-123">The email addresses of the recipients to which a message should be forwarded.</span></span> |
| <span data-ttu-id="100d2-124">markAsRead</span><span class="sxs-lookup"><span data-stu-id="100d2-124">markAsRead</span></span> | <span data-ttu-id="100d2-125">Boolean</span><span class="sxs-lookup"><span data-stu-id="100d2-125">Boolean</span></span> | <span data-ttu-id="100d2-126">Indica si un mensaje debe marcarse como leído.</span><span class="sxs-lookup"><span data-stu-id="100d2-126">Indicates whether a message should be marked as read.</span></span> |
| <span data-ttu-id="100d2-127">markImportance</span><span class="sxs-lookup"><span data-stu-id="100d2-127">markImportance</span></span> | <span data-ttu-id="100d2-128">importance</span><span class="sxs-lookup"><span data-stu-id="100d2-128">importance</span></span> | <span data-ttu-id="100d2-129">Establece la importancia del mensaje, que puede ser: `low`, `normal` o `high`.</span><span class="sxs-lookup"><span data-stu-id="100d2-129">Sets the importance of the message, which can be: `low`, `normal`, `high`.</span></span> |
| <span data-ttu-id="100d2-130">moveToFolder</span><span class="sxs-lookup"><span data-stu-id="100d2-130">moveToFolder</span></span> |  <span data-ttu-id="100d2-131">String</span><span class="sxs-lookup"><span data-stu-id="100d2-131">String</span></span>| <span data-ttu-id="100d2-132">Identificador de la carpeta a la que se moverá un mensaje.</span><span class="sxs-lookup"><span data-stu-id="100d2-132">The ID of the folder that a message will be moved to.</span></span> |
| <span data-ttu-id="100d2-133">permanentDelete</span><span class="sxs-lookup"><span data-stu-id="100d2-133">permanentDelete</span></span> | <span data-ttu-id="100d2-134">Boolean</span><span class="sxs-lookup"><span data-stu-id="100d2-134">Boolean</span></span> | <span data-ttu-id="100d2-135">Indica si un mensaje se debe eliminar permanentemente sin guardarse en la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="100d2-135">Indicates whether a message should be permanently deleted and not saved to the Deleted Items folder.</span></span> |
| <span data-ttu-id="100d2-136">redirectTo</span><span class="sxs-lookup"><span data-stu-id="100d2-136">redirectTo</span></span> | <span data-ttu-id="100d2-137">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="100d2-137">[recipient](recipient.md) collection</span></span> | <span data-ttu-id="100d2-138">Las direcciones de correo electrónico a la que se debe redirigir un mensaje.</span><span class="sxs-lookup"><span data-stu-id="100d2-138">The email addresses to which a message should be redirected.</span></span> |
| <span data-ttu-id="100d2-139">stopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="100d2-139">stopProcessingRules</span></span> | <span data-ttu-id="100d2-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="100d2-140">Boolean</span></span> | <span data-ttu-id="100d2-141">Indica si se deben evaluar las reglas siguientes.</span><span class="sxs-lookup"><span data-stu-id="100d2-141">Indicates whether subsequent rules should be evaluated.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="100d2-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="100d2-142">JSON representation</span></span>
<span data-ttu-id="100d2-143">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="100d2-143">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.messageRuleActions"
}-->

```json
{
  "assignCategories": ["String"],
  "copyToFolder": "String",
  "delete": "Boolean",
  "forwardAsAttachmentTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "forwardTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "markAsRead": "Boolean",
  "markImportance": "String",
  "moveToFolder": "String",
  "permanentDelete": "Boolean",
  "redirectTo": [{"@odata.type": "microsoft.graph.recipient"}],
  "stopProcessingRules": "Boolean"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRuleActions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->