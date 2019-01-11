---
title: Tipo de recurso messageRule
description: Regla que se aplica a los mensajes de la Bandeja de entrada de un usuario.
author: angelgolfer-ms
localization_priority: Normal
ms.openlocfilehash: ca26ad271930b83294e472b2d55e71e170722f11
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820961"
---
# <a name="messagerule-resource-type"></a><span data-ttu-id="f130e-103">Tipo de recurso messageRule</span><span class="sxs-lookup"><span data-stu-id="f130e-103">messageRule resource type</span></span>

> <span data-ttu-id="f130e-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="f130e-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="f130e-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="f130e-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="f130e-106">Regla que se aplica a los mensajes de la Bandeja de entrada de un usuario.</span><span class="sxs-lookup"><span data-stu-id="f130e-106">A rule that applies to messages in the Inbox of a user.</span></span>

<span data-ttu-id="f130e-107">En Outlook, puede establecer reglas de los mensajes entrantes en la Bandeja de entrada para llevar a cabo acciones específicas en determinadas condiciones.</span><span class="sxs-lookup"><span data-stu-id="f130e-107">In Outlook, you can set up rules for incoming messages in the Inbox to carry out specific actions upon certain conditions.</span></span> 

<span data-ttu-id="f130e-108">Mediante programación, tiene acceso a las reglas a través de la propiedad de navegación **messageRules** de la [carpeta](mailfolder.md) Bandeja de entrada.</span><span class="sxs-lookup"><span data-stu-id="f130e-108">Programmatically, you can access rules through the **messageRules** navigation property of the Inbox [folder](mailfolder.md).</span></span> <span data-ttu-id="f130e-109">Cada regla se representa mediante este recurso **messageRule**, las acciones de regla disponibles se representan mediante el tipo complejo [messageRuleActions](messageruleactions.md) y las condiciones de regla disponibles se representan mediante el tipo complejo [messageRulePredicates](messagerulepredicates.md).</span><span class="sxs-lookup"><span data-stu-id="f130e-109">Each rule is represented by this **messageRule** resource, available rule actions are represented by the [messageRuleActions](messageruleactions.md) complex type, and available rule conditions and exceptions are represented by the [messageRulePredicates](messagerulepredicates.md) complex type.</span></span>


## <a name="properties"></a><span data-ttu-id="f130e-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f130e-110">Properties</span></span>
| <span data-ttu-id="f130e-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f130e-111">Property</span></span>     | <span data-ttu-id="f130e-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="f130e-112">Type</span></span>   |<span data-ttu-id="f130e-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="f130e-113">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f130e-114">actions</span><span class="sxs-lookup"><span data-stu-id="f130e-114">actions</span></span> | [<span data-ttu-id="f130e-115">messageRuleActions</span><span class="sxs-lookup"><span data-stu-id="f130e-115">messageRuleActions</span></span>](messageruleactions.md) | <span data-ttu-id="f130e-116">Acciones que se van a realizar en un mensaje cuando se cumplan las condiciones correspondientes.</span><span class="sxs-lookup"><span data-stu-id="f130e-116">Actions to be taken on a message when the corresponding conditions are fulfilled.</span></span> |
| <span data-ttu-id="f130e-117">conditions</span><span class="sxs-lookup"><span data-stu-id="f130e-117">conditions</span></span> | [<span data-ttu-id="f130e-118">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="f130e-118">messageRulePredicates</span></span>](messagerulepredicates.md) | <span data-ttu-id="f130e-119">Condiciones que, cuando se cumplan, activarán las acciones correspondientes a esa regla.</span><span class="sxs-lookup"><span data-stu-id="f130e-119">Conditions that when fulfilled, will trigger the corresponding actions for that rule.</span></span> |
| <span data-ttu-id="f130e-120">displayName</span><span class="sxs-lookup"><span data-stu-id="f130e-120">displayName</span></span> | <span data-ttu-id="f130e-121">String</span><span class="sxs-lookup"><span data-stu-id="f130e-121">String</span></span> | <span data-ttu-id="f130e-122">Nombre para mostrar de la regla.</span><span class="sxs-lookup"><span data-stu-id="f130e-122">The display name of the rule.</span></span> |
| <span data-ttu-id="f130e-123">exceptions</span><span class="sxs-lookup"><span data-stu-id="f130e-123">exceptions</span></span> | [<span data-ttu-id="f130e-124">messageRulePredicates</span><span class="sxs-lookup"><span data-stu-id="f130e-124">messageRulePredicates</span></span>](messagerulepredicates.md) | <span data-ttu-id="f130e-125">Condiciones de excepción de la regla.</span><span class="sxs-lookup"><span data-stu-id="f130e-125">Exception conditions for the rule.</span></span> |
| <span data-ttu-id="f130e-126">hasError</span><span class="sxs-lookup"><span data-stu-id="f130e-126">hasError</span></span> | <span data-ttu-id="f130e-127">Boolean</span><span class="sxs-lookup"><span data-stu-id="f130e-127">Boolean</span></span> | <span data-ttu-id="f130e-128">Indica si la regla es una condición de error.</span><span class="sxs-lookup"><span data-stu-id="f130e-128">Indicates whether the rule is in an error condition.</span></span> <span data-ttu-id="f130e-129">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f130e-129">Read-only.</span></span> |
| <span data-ttu-id="f130e-130">id</span><span class="sxs-lookup"><span data-stu-id="f130e-130">id</span></span> |<span data-ttu-id="f130e-131">String</span><span class="sxs-lookup"><span data-stu-id="f130e-131">String</span></span>|<span data-ttu-id="f130e-132">Identificador único de la regla.</span><span class="sxs-lookup"><span data-stu-id="f130e-132">The unique identifier of the rule.</span></span> <span data-ttu-id="f130e-133">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f130e-133">Read-only.</span></span>|
| <span data-ttu-id="f130e-134">isEnabled</span><span class="sxs-lookup"><span data-stu-id="f130e-134">isEnabled</span></span> | <span data-ttu-id="f130e-135">Boolean</span><span class="sxs-lookup"><span data-stu-id="f130e-135">Boolean</span></span> | <span data-ttu-id="f130e-136">Indica si la regla está habilitada para que se aplique a los mensajes.</span><span class="sxs-lookup"><span data-stu-id="f130e-136">Indicates whether the rule is enabled to be applied to messages.</span></span> |
| <span data-ttu-id="f130e-137">isReadOnly</span><span class="sxs-lookup"><span data-stu-id="f130e-137">isReadOnly</span></span> | <span data-ttu-id="f130e-138">Boolean</span><span class="sxs-lookup"><span data-stu-id="f130e-138">Boolean</span></span> | <span data-ttu-id="f130e-139">Indica si la regla es de solo lectura y la API de REST de reglas no la puede modificar ni eliminar.</span><span class="sxs-lookup"><span data-stu-id="f130e-139">Indicates if the rule is read-only and cannot be modified or deleted by the rules REST API.</span></span> |
| <span data-ttu-id="f130e-140">sequence</span><span class="sxs-lookup"><span data-stu-id="f130e-140">sequence</span></span> | <span data-ttu-id="f130e-141">Int32</span><span class="sxs-lookup"><span data-stu-id="f130e-141">Int32</span></span> | <span data-ttu-id="f130e-142">Indica el orden en que se ejecuta la regla entre otras reglas.</span><span class="sxs-lookup"><span data-stu-id="f130e-142">Indicates the order in which the rule is executed, among other rules.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="f130e-143">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f130e-143">JSON representation</span></span>
<span data-ttu-id="f130e-144">Esta es una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="f130e-144">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
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

## <a name="methods"></a><span data-ttu-id="f130e-145">Métodos</span><span class="sxs-lookup"><span data-stu-id="f130e-145">Methods</span></span>
| <span data-ttu-id="f130e-146">Método</span><span class="sxs-lookup"><span data-stu-id="f130e-146">Method</span></span>           | <span data-ttu-id="f130e-147">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f130e-147">Return Type</span></span>    |<span data-ttu-id="f130e-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="f130e-148">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="f130e-149">Enumerar reglas</span><span class="sxs-lookup"><span data-stu-id="f130e-149">List rules</span></span>](../api/mailfolder-list-messagerules.md) | <span data-ttu-id="f130e-150">Colección [messageRule](messagerule.md)</span><span class="sxs-lookup"><span data-stu-id="f130e-150">[messageRule](messagerule.md) collection</span></span> |<span data-ttu-id="f130e-151">Obtener todos los objetos **messageRule** definidos para la Bandeja de entrada del usuario.</span><span class="sxs-lookup"><span data-stu-id="f130e-151">Get all the **messageRule** objects defined for the user's Inbox.</span></span>|
|[<span data-ttu-id="f130e-152">Obtener regla</span><span class="sxs-lookup"><span data-stu-id="f130e-152">Get rule</span></span>](../api/messagerule-get.md) | [<span data-ttu-id="f130e-153">messageRule</span><span class="sxs-lookup"><span data-stu-id="f130e-153">messageRule</span></span>](messagerule.md) |<span data-ttu-id="f130e-154">Leer las propiedades y relaciones de un objeto **messageRule**.</span><span class="sxs-lookup"><span data-stu-id="f130e-154">Read the properties and relationships of a **messageRule** object.</span></span>|
|[<span data-ttu-id="f130e-155">Crear</span><span class="sxs-lookup"><span data-stu-id="f130e-155">Create</span></span>](../api/mailfolder-post-messagerules.md) | [<span data-ttu-id="f130e-156">messageRule</span><span class="sxs-lookup"><span data-stu-id="f130e-156">messageRule</span></span>](messagerule.md) |<span data-ttu-id="f130e-157">Crear un objeto **messageRule** especificando un conjunto de condiciones y acciones.</span><span class="sxs-lookup"><span data-stu-id="f130e-157">Create a **messageRule** object by specifying a set of conditions and actions.</span></span>|
|[<span data-ttu-id="f130e-158">Actualizar</span><span class="sxs-lookup"><span data-stu-id="f130e-158">Update</span></span>](../api/messagerule-update.md) | [<span data-ttu-id="f130e-159">messageRule</span><span class="sxs-lookup"><span data-stu-id="f130e-159">messageRule</span></span>](messagerule.md) |<span data-ttu-id="f130e-160">Cambie las propiedades modificables en un objeto **messageRule** y guarde los cambios.</span><span class="sxs-lookup"><span data-stu-id="f130e-160">Change writable properties on a **messageRule** object and save the changes.</span></span> |
|[<span data-ttu-id="f130e-161">Eliminar</span><span class="sxs-lookup"><span data-stu-id="f130e-161">Delete</span></span>](../api/messagerule-delete.md) | <span data-ttu-id="f130e-162">Ninguno</span><span class="sxs-lookup"><span data-stu-id="f130e-162">None</span></span> |<span data-ttu-id="f130e-163">Eliminar el objeto **messageRule** especificado.</span><span class="sxs-lookup"><span data-stu-id="f130e-163">Delete the specified **messageRule** object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "messageRule resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
