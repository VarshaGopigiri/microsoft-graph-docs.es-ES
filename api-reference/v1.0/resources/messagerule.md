---
title: Tipo de recurso messageRule
description: Regla que se aplica a los mensajes de la Bandeja de entrada de un usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: 9336f2e35d6c68d86c3e92b5f94c024eff1e49a5
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27862128"
---
# <a name="messagerule-resource-type"></a><span data-ttu-id="c646e-103">Tipo de recurso messageRule</span><span class="sxs-lookup"><span data-stu-id="c646e-103">messageRule resource type</span></span>


<span data-ttu-id="c646e-104">Regla que se aplica a los mensajes de la Bandeja de entrada de un usuario.</span><span class="sxs-lookup"><span data-stu-id="c646e-104">A rule that applies to messages in the Inbox of a user.</span></span>

<span data-ttu-id="c646e-105">En Outlook, puede establecer reglas de los mensajes entrantes en la Bandeja de entrada para llevar a cabo acciones específicas en determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="c646e-105">In Outlook, you can set up rules for incoming messages in the Inbox to carry out specific actions upon certain conditions.</span></span> 

<span data-ttu-id="c646e-106">Mediante programación, tiene acceso a las reglas a través de la propiedad de navegación **messageRules** de la [carpeta](mailfolder.md) Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="c646e-106">Programmatically, you can access rules through the **messageRules** navigation property of the Inbox [folder](mailfolder.md).</span></span> <span data-ttu-id="c646e-107">Cada regla se representa mediante este recurso **messageRule**, las acciones de regla disponibles se representan mediante el tipo complejo [messageRuleActions](messageruleactions.md) y las condiciones de regla disponibles se representan mediante el tipo complejo [messageRulePredicates](messagerulepredicates.md).</span><span class="sxs-lookup"><span data-stu-id="c646e-107">Each rule is represented by this **messageRule** resource, available rule actions are represented by the [messageRuleActions](messageruleactions.md) complex type, and available rule conditions and exceptions are represented by the [messageRulePredicates](messagerulepredicates.md) complex type.</span></span>


## <a name="properties"></a><span data-ttu-id="c646e-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c646e-108">Properties</span></span>
| <span data-ttu-id="c646e-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c646e-109">Property</span></span>     | <span data-ttu-id="c646e-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="c646e-110">Type</span></span>   |<span data-ttu-id="c646e-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="c646e-111">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c646e-112">actions</span><span class="sxs-lookup"><span data-stu-id="c646e-112">actions</span></span> | [<span data-ttu-id="c646e-113">messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="c646e-113">messageRuleActions</span></span>](messageruleactions.md) | <span data-ttu-id="c646e-114">Acciones que se van a realizar en un mensaje cuando se cumplan las condiciones correspondientes.</span><span class="sxs-lookup"><span data-stu-id="c646e-114">Actions to be taken on a message when the corresponding conditions are fulfilled.</span></span> |
| <span data-ttu-id="c646e-115">conditions</span><span class="sxs-lookup"><span data-stu-id="c646e-115">conditions</span></span> | [<span data-ttu-id="c646e-116">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="c646e-116">messageRulePredicates</span></span>](messagerulepredicates.md) | <span data-ttu-id="c646e-117">Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla.</span><span class="sxs-lookup"><span data-stu-id="c646e-117">Conditions that when fulfilled, will trigger the corresponding actions for that rule.</span></span> |
| <span data-ttu-id="c646e-118">displayName</span><span class="sxs-lookup"><span data-stu-id="c646e-118">displayName</span></span> | <span data-ttu-id="c646e-119">String</span><span class="sxs-lookup"><span data-stu-id="c646e-119">String</span></span> | <span data-ttu-id="c646e-120">Nombre para mostrar de la regla.</span><span class="sxs-lookup"><span data-stu-id="c646e-120">The display name of the rule.</span></span> |
| <span data-ttu-id="c646e-121">exceptions</span><span class="sxs-lookup"><span data-stu-id="c646e-121">exceptions</span></span> | [<span data-ttu-id="c646e-122">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="c646e-122">messageRulePredicates</span></span>](messagerulepredicates.md) | <span data-ttu-id="c646e-123">Condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="c646e-123">Exception conditions for the rule.</span></span> |
| <span data-ttu-id="c646e-124">hasError</span><span class="sxs-lookup"><span data-stu-id="c646e-124">hasError</span></span> | <span data-ttu-id="c646e-125">Boolean</span><span class="sxs-lookup"><span data-stu-id="c646e-125">Boolean</span></span> | <span data-ttu-id="c646e-126">Indica si la regla es una condición de error.</span><span class="sxs-lookup"><span data-stu-id="c646e-126">Indicates whether the rule is in an error condition.</span></span> <span data-ttu-id="c646e-127">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c646e-127">Read-only.</span></span> |
| <span data-ttu-id="c646e-128">id</span><span class="sxs-lookup"><span data-stu-id="c646e-128">id</span></span> |<span data-ttu-id="c646e-129">String</span><span class="sxs-lookup"><span data-stu-id="c646e-129">String</span></span>|<span data-ttu-id="c646e-130">Identificador único de la regla.</span><span class="sxs-lookup"><span data-stu-id="c646e-130">The unique identifier of the rule.</span></span> <span data-ttu-id="c646e-131">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c646e-131">Read-only.</span></span>|
| <span data-ttu-id="c646e-132">isEnabled</span><span class="sxs-lookup"><span data-stu-id="c646e-132">isEnabled</span></span> | <span data-ttu-id="c646e-133">Boolean</span><span class="sxs-lookup"><span data-stu-id="c646e-133">Boolean</span></span> | <span data-ttu-id="c646e-134">Indica si la regla está habilitada para que se aplique a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="c646e-134">Indicates whether the rule is enabled to be applied to messages.</span></span> |
| <span data-ttu-id="c646e-135">isReadOnly</span><span class="sxs-lookup"><span data-stu-id="c646e-135">isReadOnly</span></span> | <span data-ttu-id="c646e-136">Boolean</span><span class="sxs-lookup"><span data-stu-id="c646e-136">Boolean</span></span> | <span data-ttu-id="c646e-137">Indica si la regla es de solo lectura y la API de REST de reglas no la puede modificar ni eliminar.</span><span class="sxs-lookup"><span data-stu-id="c646e-137">Indicates if the rule is read-only and cannot be modified or deleted by the rules REST API.</span></span> |
| <span data-ttu-id="c646e-138">sequence</span><span class="sxs-lookup"><span data-stu-id="c646e-138">sequence</span></span> | <span data-ttu-id="c646e-139">Int32</span><span class="sxs-lookup"><span data-stu-id="c646e-139">Int32</span></span> | <span data-ttu-id="c646e-140">Indica el orden en que se ejecuta la regla entre otras reglas.</span><span class="sxs-lookup"><span data-stu-id="c646e-140">Indicates the order in which the rule is executed, among other rules.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="c646e-141">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c646e-141">JSON representation</span></span>
<span data-ttu-id="c646e-142">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c646e-142">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
   "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.messageRule"
}-->

```json
{
  "actions": {"@odata.type": "microsoft.graph.messageRuleActions"},
  "conditions": {"@odata.type": "microsoft.graph.messageRulePredicates"},
  "displayName": "String",
  "exceptions": {"@odata.type": "microsoft.graph.messageRulePredicates"},
  "hasError": "Boolean",
  "id": "String",
  "isEnabled": "Boolean",
  "isReadOnly": "Boolean",
  "sequence": "Int32"
}

```

## <a name="methods"></a><span data-ttu-id="c646e-143">Métodos</span><span class="sxs-lookup"><span data-stu-id="c646e-143">Methods</span></span>
| <span data-ttu-id="c646e-144">Método</span><span class="sxs-lookup"><span data-stu-id="c646e-144">Method</span></span>           | <span data-ttu-id="c646e-145">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c646e-145">Return Type</span></span>    |<span data-ttu-id="c646e-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="c646e-146">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="c646e-147">Enumerar reglas</span><span class="sxs-lookup"><span data-stu-id="c646e-147">List rules</span></span>](../api/mailfolder-list-messagerules.md) | <span data-ttu-id="c646e-148">Colección [messageRule](messagerule.md)</span><span class="sxs-lookup"><span data-stu-id="c646e-148">[messageRule](messagerule.md) collection</span></span> |<span data-ttu-id="c646e-149">Obtener todos los objetos **messageRule** definidos para la Bandeja de entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="c646e-149">Get all the **messageRule** objects defined for the user's Inbox.</span></span>|
|[<span data-ttu-id="c646e-150">Obtener regla</span><span class="sxs-lookup"><span data-stu-id="c646e-150">Get rule</span></span>](../api/messagerule-get.md) | [<span data-ttu-id="c646e-151">messageRule</span><span class="sxs-lookup"><span data-stu-id="c646e-151">messageRule</span></span>](messagerule.md) |<span data-ttu-id="c646e-152">Leer las propiedades y relaciones de un objeto **messageRule**.</span><span class="sxs-lookup"><span data-stu-id="c646e-152">Read the properties and relationships of a **messageRule** object.</span></span>|
|[<span data-ttu-id="c646e-153">Crear</span><span class="sxs-lookup"><span data-stu-id="c646e-153">Create</span></span>](../api/mailfolder-post-messagerules.md) | [<span data-ttu-id="c646e-154">messageRule</span><span class="sxs-lookup"><span data-stu-id="c646e-154">messageRule</span></span>](messagerule.md) |<span data-ttu-id="c646e-155">Crear un objeto **messageRule** especificando un conjunto de condiciones y acciones.</span><span class="sxs-lookup"><span data-stu-id="c646e-155">Create a **messageRule** object by specifying a set of conditions and actions.</span></span>|
|[<span data-ttu-id="c646e-156">Actualizar</span><span class="sxs-lookup"><span data-stu-id="c646e-156">Update</span></span>](../api/messagerule-update.md) | [<span data-ttu-id="c646e-157">messageRule</span><span class="sxs-lookup"><span data-stu-id="c646e-157">messageRule</span></span>](messagerule.md) |<span data-ttu-id="c646e-158">Cambie las propiedades modificables en un objeto **messageRule** y guarde los cambios.</span><span class="sxs-lookup"><span data-stu-id="c646e-158">Change writable properties on a **messageRule** object and save the changes.</span></span> |
|[<span data-ttu-id="c646e-159">Eliminar</span><span class="sxs-lookup"><span data-stu-id="c646e-159">Delete</span></span>](../api/messagerule-delete.md) | <span data-ttu-id="c646e-160">Ninguno</span><span class="sxs-lookup"><span data-stu-id="c646e-160">None</span></span> |<span data-ttu-id="c646e-161">Eliminar el objeto **messageRule** especificado.</span><span class="sxs-lookup"><span data-stu-id="c646e-161">Delete the specified **messageRule** object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
