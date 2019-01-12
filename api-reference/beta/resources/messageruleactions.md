---
title: Tipo de recurso messageRuleActions
description: Representa el conjunto de acciones que están disponibles para una regla.
author: angelgolfer-ms
localization_priority: Normal
ms.prod: outlook
ms.openlocfilehash: 58cae7f777d0ac9ee03b102b22325e63acf55358
ms.sourcegitcommit: 36be044c89a19af84c93e586e22200ec919e4c9f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/12/2019
ms.locfileid: "27938891"
---
# <a name="messageruleactions-resource-type"></a><span data-ttu-id="96fe4-103">Tipo de recurso messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="96fe4-103">messageRuleActions resource type</span></span>

> <span data-ttu-id="96fe4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="96fe4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="96fe4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="96fe4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="96fe4-106">Representa el conjunto de acciones que están disponibles para una regla.</span><span class="sxs-lookup"><span data-stu-id="96fe4-106">Represents the set of actions that are available to a rule.</span></span>

## <a name="properties"></a><span data-ttu-id="96fe4-107">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96fe4-107">Properties</span></span>
| <span data-ttu-id="96fe4-108">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96fe4-108">Property</span></span>     | <span data-ttu-id="96fe4-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="96fe4-109">Type</span></span>   |<span data-ttu-id="96fe4-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="96fe4-110">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="96fe4-111">assignCategories</span><span class="sxs-lookup"><span data-stu-id="96fe4-111">assignCategories</span></span> | <span data-ttu-id="96fe4-112">Colección String</span><span class="sxs-lookup"><span data-stu-id="96fe4-112">String collection</span></span> | <span data-ttu-id="96fe4-113">Lista de categorías que se asignarán a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="96fe4-113">A list of categories to be assigned to a message.</span></span> |
| <span data-ttu-id="96fe4-114">copyToFolder</span><span class="sxs-lookup"><span data-stu-id="96fe4-114">copyToFolder</span></span> | <span data-ttu-id="96fe4-115">String</span><span class="sxs-lookup"><span data-stu-id="96fe4-115">String</span></span> | <span data-ttu-id="96fe4-116">Identificador de la carpeta donde se va a copiar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="96fe4-116">The ID of a folder that a message is to be copied to.</span></span> |
| <span data-ttu-id="96fe4-117">delete</span><span class="sxs-lookup"><span data-stu-id="96fe4-117">delete</span></span> | <span data-ttu-id="96fe4-118">Boolean</span><span class="sxs-lookup"><span data-stu-id="96fe4-118">Boolean</span></span> | <span data-ttu-id="96fe4-119">Indica si un mensaje se debe mover a la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="96fe4-119">Indicates whether a message should be moved to the Deleted Items folder.</span></span> |
| <span data-ttu-id="96fe4-120">forwardAsAttachmentTo</span><span class="sxs-lookup"><span data-stu-id="96fe4-120">forwardAsAttachmentTo</span></span> | <span data-ttu-id="96fe4-121">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="96fe4-121">[recipient](recipient.md) collection</span></span> | <span data-ttu-id="96fe4-122">Direcciones de correo electrónico de los destinatarios a los que se debe reenviar un mensaje como datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="96fe4-122">The email addresses of the recipients to which a message should be forwarded as an attachment.</span></span> |
| <span data-ttu-id="96fe4-123">forwardTo</span><span class="sxs-lookup"><span data-stu-id="96fe4-123">forwardTo</span></span> | <span data-ttu-id="96fe4-124">Colección [recipient](recipient.md)</span><span class="sxs-lookup"><span data-stu-id="96fe4-124">[recipient](recipient.md) collection</span></span> | <span data-ttu-id="96fe4-125">Direcciones de correo electrónico de los destinatarios a los que se debe reenviar un mensaje.</span><span class="sxs-lookup"><span data-stu-id="96fe4-125">The email addresses of the recipients to which a message should be forwarded.</span></span> |
| <span data-ttu-id="96fe4-126">markAsRead</span><span class="sxs-lookup"><span data-stu-id="96fe4-126">markAsRead</span></span> | <span data-ttu-id="96fe4-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="96fe4-127">Boolean</span></span> | <span data-ttu-id="96fe4-128">Indica si un mensaje debe marcarse como leído.</span><span class="sxs-lookup"><span data-stu-id="96fe4-128">Indicates whether a message should be marked as read.</span></span> |
| <span data-ttu-id="96fe4-129">markImportance</span><span class="sxs-lookup"><span data-stu-id="96fe4-129">markImportance</span></span> | <span data-ttu-id="96fe4-130">String</span><span class="sxs-lookup"><span data-stu-id="96fe4-130">String</span></span> | <span data-ttu-id="96fe4-131">Establece la importancia del mensaje, que puede ser: `low`, `normal` o `high`.</span><span class="sxs-lookup"><span data-stu-id="96fe4-131">Sets the importance of the message, which can be: `low`, `normal`, `high`.</span></span> |
| <span data-ttu-id="96fe4-132">moveToFolder</span><span class="sxs-lookup"><span data-stu-id="96fe4-132">moveToFolder</span></span> |  <span data-ttu-id="96fe4-133">String</span><span class="sxs-lookup"><span data-stu-id="96fe4-133">String</span></span>| <span data-ttu-id="96fe4-134">Identificador de la carpeta a la que se moverá un mensaje.</span><span class="sxs-lookup"><span data-stu-id="96fe4-134">The ID of the folder that a message will be moved to.</span></span> |
| <span data-ttu-id="96fe4-135">permanentDelete</span><span class="sxs-lookup"><span data-stu-id="96fe4-135">permanentDelete</span></span> | <span data-ttu-id="96fe4-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="96fe4-136">Boolean</span></span> | <span data-ttu-id="96fe4-137">Indica si un mensaje se debe eliminar permanentemente sin guardarse en la carpeta Elementos eliminados.</span><span class="sxs-lookup"><span data-stu-id="96fe4-137">Indicates whether a message should be permanently deleted and not saved to the Deleted Items folder.</span></span> |
| <span data-ttu-id="96fe4-138">redirectTo</span><span class="sxs-lookup"><span data-stu-id="96fe4-138">redirectTo</span></span> | [<span data-ttu-id="96fe4-139">recipient</span><span class="sxs-lookup"><span data-stu-id="96fe4-139">recipient</span></span>](recipient.md) | <span data-ttu-id="96fe4-140">Dirección de correo electrónico a la que se debe redirigir un mensaje.</span><span class="sxs-lookup"><span data-stu-id="96fe4-140">The email address to which a message should be redirected.</span></span> |
| <span data-ttu-id="96fe4-141">stopProcessingRules</span><span class="sxs-lookup"><span data-stu-id="96fe4-141">stopProcessingRules</span></span> | <span data-ttu-id="96fe4-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="96fe4-142">Boolean</span></span> | <span data-ttu-id="96fe4-143">Indica si se deben evaluar las reglas siguientes.</span><span class="sxs-lookup"><span data-stu-id="96fe4-143">Indicates whether subsequent rules should be evaluated.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="96fe4-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="96fe4-144">JSON representation</span></span>
<span data-ttu-id="96fe4-145">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="96fe4-145">Here is a JSON representation of the resource.</span></span>

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
  "redirectTo": {"@odata.type": "microsoft.graph.recipient"},
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
