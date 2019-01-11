---
title: Tipo de recurso openTypeExtension (extensiones abiertas)
description: Extensiones Open (anteriormente conocidas como extensiones de datos de Office 365) proporcionan una forma sencilla de agregar propiedades sin tipo directamente en un recurso de Microsoft Graph.
localization_priority: Normal
ms.openlocfilehash: 4bab83766d1fc44e96043689677713cb59084f4f
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27870962"
---
# <a name="opentypeextension-resource-type-open-extensions"></a><span data-ttu-id="5adb4-103">Tipo de recurso openTypeExtension (extensiones abiertas)</span><span class="sxs-lookup"><span data-stu-id="5adb4-103">openTypeExtension resource type (open extensions)</span></span>

> <span data-ttu-id="5adb4-104">**Importante:** Las API de la versión /beta de Microsoft Graph son una versión preliminar y están sujetas a cambios.</span><span class="sxs-lookup"><span data-stu-id="5adb4-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="5adb4-105">No se admite el uso de estas API en aplicaciones de producción.</span><span class="sxs-lookup"><span data-stu-id="5adb4-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="5adb4-106">Extensiones Open (anteriormente conocidas como extensiones de datos de Office 365) proporcionan una forma sencilla de agregar propiedades sin tipo directamente en un recurso de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="5adb4-106">Open extensions (formerly known as Office 365 data extensions) provide an easy way to directly add untyped properties to a resource in Microsoft Graph.</span></span>
<span data-ttu-id="5adb4-107">El recurso **openTypeExtension** representa las extensiones abiertas.</span><span class="sxs-lookup"><span data-stu-id="5adb4-107">Open extensions are represented by the **openTypeExtension** resource.</span></span> <span data-ttu-id="5adb4-108">Las extensiones abiertas agregadas a un recurso se muestran en la propiedad de navegación **extensions**, que se deriva del tipo abstracto [extension](extension.md).</span><span class="sxs-lookup"><span data-stu-id="5adb4-108">Any open extension added to a resource shows up in the **extensions** navigation property, which is derived from the [extension](extension.md) abstract type.</span></span>  <span data-ttu-id="5adb4-109">Cada extensión tiene una propiedad **extensionName** que es la única predefinida y que puede ser escrita para todas las extensiones, junto con los datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="5adb4-109">Each extension has an **extensionName** property which is the only pre-defined, writable property for all extensions, along with your custom data.</span></span> <span data-ttu-id="5adb4-110">Una forma de asegurarse de que los nombres de extensión son únicos es usar un método inverso del formato de nombres de dominio (DNS) que dependa de _su propio dominio_, por ejemplo, `Com.Contoso.ContactInfo`.</span><span class="sxs-lookup"><span data-stu-id="5adb4-110">One way to help make sure extension names are unique is to use a reverse domain name system (DNS) format that is dependent on _your own domain_, for example, `Com.Contoso.ContactInfo`.</span></span> <span data-ttu-id="5adb4-111">No use el dominio de Microsoft (`Com.Microsoft` o `Com.OnMicrosoft`) en un nombre de extensión.</span><span class="sxs-lookup"><span data-stu-id="5adb4-111">Do not use the Microsoft domain (`Com.Microsoft` or `Com.OnMicrosoft`) in an extension name.</span></span>

<span data-ttu-id="5adb4-112">Ejemplo de extensión abierta: [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)</span><span class="sxs-lookup"><span data-stu-id="5adb4-112">Open extension example: [Add custom data to users using open extensions](/graph/extensibility-open-users)</span></span>

<span data-ttu-id="5adb4-113">Las extensiones abiertas son compatibles con los recursos siguientes en las versiones correspondientes: disponibilidad general (GA: /v1.0 y /beta) o en versión preliminar (/beta).</span><span class="sxs-lookup"><span data-stu-id="5adb4-113">Open extensions are supported by the following resources in the corresponding versions - general availability (GA: /v1.0 and /beta) or preview (/beta).</span></span>

| <span data-ttu-id="5adb4-114">Recurso</span><span class="sxs-lookup"><span data-stu-id="5adb4-114">Resource</span></span> | <span data-ttu-id="5adb4-115">Versión</span><span class="sxs-lookup"><span data-stu-id="5adb4-115">Version</span></span> |
|---------------|-------|
| [<span data-ttu-id="5adb4-116">Unidad administrativa</span><span class="sxs-lookup"><span data-stu-id="5adb4-116">Administrative unit</span></span>](administrativeunit.md)  | <span data-ttu-id="5adb4-117">Solo versión preliminar</span><span class="sxs-lookup"><span data-stu-id="5adb4-117">Preview only</span></span> |
| [<span data-ttu-id="5adb4-118">Evento de calendario</span><span class="sxs-lookup"><span data-stu-id="5adb4-118">Calendar event</span></span>](event.md) | <span data-ttu-id="5adb4-119">GA</span><span class="sxs-lookup"><span data-stu-id="5adb4-119">GA</span></span> |
| <span data-ttu-id="5adb4-120">[Evento de calendario](event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="5adb4-120">Group [calendar event](event.md)</span></span> | <span data-ttu-id="5adb4-121">GA</span><span class="sxs-lookup"><span data-stu-id="5adb4-121">GA</span></span> |
| <span data-ttu-id="5adb4-122">[Publicación](post.md) de subproceso de conversación de grupo</span><span class="sxs-lookup"><span data-stu-id="5adb4-122">Group conversation thread [post](post.md)</span></span> | <span data-ttu-id="5adb4-123">GA</span><span class="sxs-lookup"><span data-stu-id="5adb4-123">GA</span></span> |
| [<span data-ttu-id="5adb4-124">device</span><span class="sxs-lookup"><span data-stu-id="5adb4-124">device</span></span>](device.md) | <span data-ttu-id="5adb4-125">GA</span><span class="sxs-lookup"><span data-stu-id="5adb4-125">GA</span></span> |
| [<span data-ttu-id="5adb4-126">group</span><span class="sxs-lookup"><span data-stu-id="5adb4-126">group</span></span>](group.md) | <span data-ttu-id="5adb4-127">GA</span><span class="sxs-lookup"><span data-stu-id="5adb4-127">GA</span></span> |
| [<span data-ttu-id="5adb4-128">message</span><span class="sxs-lookup"><span data-stu-id="5adb4-128">message</span></span>](message.md) | <span data-ttu-id="5adb4-129">GA</span><span class="sxs-lookup"><span data-stu-id="5adb4-129">GA</span></span> |
| [<span data-ttu-id="5adb4-130">organization</span><span class="sxs-lookup"><span data-stu-id="5adb4-130">organization</span></span>](organization.md) | <span data-ttu-id="5adb4-131">GA</span><span class="sxs-lookup"><span data-stu-id="5adb4-131">GA</span></span> |
| [<span data-ttu-id="5adb4-132">Contacto personal</span><span class="sxs-lookup"><span data-stu-id="5adb4-132">Personal contact</span></span>](contact.md) | <span data-ttu-id="5adb4-133">GA</span><span class="sxs-lookup"><span data-stu-id="5adb4-133">GA</span></span> |
| [<span data-ttu-id="5adb4-134">user</span><span class="sxs-lookup"><span data-stu-id="5adb4-134">user</span></span>](user.md) | <span data-ttu-id="5adb4-135">GA</span><span class="sxs-lookup"><span data-stu-id="5adb4-135">GA</span></span> |

## <a name="outlook-specific-considerations"></a><span data-ttu-id="5adb4-136">Consideraciones sobre específica de Outlook</span><span class="sxs-lookup"><span data-stu-id="5adb4-136">Outlook-specific considerations</span></span>

<span data-ttu-id="5adb4-137">Cada extensión open presente en un recurso de Outlook (evento, mensaje o contacto personal) se almacena en una [propiedad con nombre de MAPI](https://msdn.microsoft.com/library/cc765864(v=office.15).aspx).</span><span class="sxs-lookup"><span data-stu-id="5adb4-137">Each open extension present on an Outlook resource (event, message, or personal contact) is stored in a [MAPI named property](https://msdn.microsoft.com/library/cc765864(v=office.15).aspx).</span></span> <span data-ttu-id="5adb4-138">Al crear extensiones open para Outlook, tenga en cuenta que con el nombre de las propiedades de MAPI son un recurso finito en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="5adb4-138">When you create open extensions for Outlook, consider that MAPI named properties are a finite resource in a user's mailbox.</span></span> <span data-ttu-id="5adb4-139">Cuando se agota la cuota de la propiedad con nombre de un usuario, no se puede crear las propiedades más con nombre de dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="5adb4-139">When a user's named property quota is exhausted, you can't create any more named properties for that user.</span></span> <span data-ttu-id="5adb4-140">Esto se puede producir un comportamiento inesperado de clientes que se basan en las propiedades con nombre para la función.</span><span class="sxs-lookup"><span data-stu-id="5adb4-140">This can result in unexpected behavior from clients that rely on named properties to function.</span></span>

<span data-ttu-id="5adb4-141">Aplique las siguientes directrices al crear extensiones open en recursos de Outlook:</span><span class="sxs-lookup"><span data-stu-id="5adb4-141">Apply the following guidelines when you create open extensions on Outlook resources:</span></span>

- <span data-ttu-id="5adb4-142">Cree el número mínimo de extensiones necesarias.</span><span class="sxs-lookup"><span data-stu-id="5adb4-142">Create the minimum number of extensions required.</span></span> <span data-ttu-id="5adb4-143">La mayoría de las aplicaciones deben requerir no más de una extensión.</span><span class="sxs-lookup"><span data-stu-id="5adb4-143">Most applications should require no more than one extension.</span></span> <span data-ttu-id="5adb4-144">Las extensiones no tienen propiedades de conjunto definido ni estructura, por lo que puede almacenar varios valores en una única extensión.</span><span class="sxs-lookup"><span data-stu-id="5adb4-144">Extensions have no set defined properties or structure, so you can store multiple values in a single extension.</span></span>
- <span data-ttu-id="5adb4-145">Evitar extensiones de nombres de una forma variable (por ejemplo, basándose en la entrada del usuario, etcetera.).</span><span class="sxs-lookup"><span data-stu-id="5adb4-145">Avoid naming extensions in a variable manner (such as based on user input, etc.).</span></span> <span data-ttu-id="5adb4-146">Cada vez que se crea una extensión abierta con un nombre nuevo que no se ha usado en el buzón de un usuario antes, se crea un nuevo MAPI con nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="5adb4-146">Each time an open extension is created with a new name that has not been used in a user's mailbox before, a new MAPI named property is created.</span></span> <span data-ttu-id="5adb4-147">Quitar la extensión no quita la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="5adb4-147">Removing the extension does not remove the named property.</span></span>

### <a name="use-open-extensions-for-outlook-resources-or-extended-properties"></a><span data-ttu-id="5adb4-148">Utilizar extensiones open (para recursos de Outlook) o las propiedades extendidas</span><span class="sxs-lookup"><span data-stu-id="5adb4-148">Use open extensions (for Outlook resources) or extended properties</span></span>

<span data-ttu-id="5adb4-149">Extensiones de Open es la solución recomendada para la mayoría de los escenarios que implican almacenar y obtener acceso a datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="5adb4-149">Open extensions is the recommended solution for most scenarios involving storing and accessing custom data.</span></span> <span data-ttu-id="5adb4-150">Si, sin embargo, necesita tener acceso a datos personalizados para las propiedades de MAPI de Outlook que ya no están expuestas a través de los [metadatos de la API de Microsoft Graph](https://developer.microsoft.com/graph/docs/overview/call_api), puede usar [las propiedades extendidas y su API de REST](extended-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5adb4-150">If, however, you need to access custom data for Outlook MAPI properties that are not already exposed through the [Microsoft Graph API metadata](https://developer.microsoft.com/graph/docs/overview/call_api), you can use [extended properties and its REST API](extended-properties-overview.md).</span></span> <span data-ttu-id="5adb4-151">Puede comprobar qué propiedades expone los metadatos en [ https://graph.microsoft.com/v1.0/$metadata](https://graph.microsoft.com/v1.0/$metadata).</span><span class="sxs-lookup"><span data-stu-id="5adb4-151">You can verify which properties the metadata exposes at [https://graph.microsoft.com/v1.0/$metadata](https://graph.microsoft.com/v1.0/$metadata).</span></span>

## <a name="json-representation"></a><span data-ttu-id="5adb4-152">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5adb4-152">JSON representation</span></span>

<span data-ttu-id="5adb4-153">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5adb4-153">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.opentypeextension"
}-->

```json
{
  "extensionName": "string",
  "id": "string (identifier)"
}

```

## <a name="properties"></a><span data-ttu-id="5adb4-154">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5adb4-154">Properties</span></span>

| <span data-ttu-id="5adb4-155">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5adb4-155">Property</span></span> | <span data-ttu-id="5adb4-156">Tipo</span><span class="sxs-lookup"><span data-stu-id="5adb4-156">Type</span></span> | <span data-ttu-id="5adb4-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="5adb4-157">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="5adb4-158">extensionName</span><span class="sxs-lookup"><span data-stu-id="5adb4-158">extensionName</span></span>|<span data-ttu-id="5adb4-159">String</span><span class="sxs-lookup"><span data-stu-id="5adb4-159">String</span></span>|<span data-ttu-id="5adb4-p107">Un identificador de texto único para una extensión de datos de tipo abierto. Necesario.</span><span class="sxs-lookup"><span data-stu-id="5adb4-p107">A unique text identifier for an open type data extension. Required.</span></span>|
|<span data-ttu-id="5adb4-162">id</span><span class="sxs-lookup"><span data-stu-id="5adb4-162">id</span></span>|<span data-ttu-id="5adb4-163">String</span><span class="sxs-lookup"><span data-stu-id="5adb4-163">String</span></span>| <span data-ttu-id="5adb4-p108">Un identificador completo que concatena el tipo de extensión con el **extensionName**. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5adb4-p108">A fully qualified identifier that concatenates the extension type with the **extensionName**. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="5adb4-166">Relaciones</span><span class="sxs-lookup"><span data-stu-id="5adb4-166">Relationships</span></span>

<span data-ttu-id="5adb4-167">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5adb4-167">None</span></span>

## <a name="methods"></a><span data-ttu-id="5adb4-168">Métodos</span><span class="sxs-lookup"><span data-stu-id="5adb4-168">Methods</span></span>

| <span data-ttu-id="5adb4-169">Método</span><span class="sxs-lookup"><span data-stu-id="5adb4-169">Method</span></span> | <span data-ttu-id="5adb4-170">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5adb4-170">Return Type</span></span> | <span data-ttu-id="5adb4-171">Descripción</span><span class="sxs-lookup"><span data-stu-id="5adb4-171">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="5adb4-172">Post</span><span class="sxs-lookup"><span data-stu-id="5adb4-172">Post</span></span>](../api/opentypeextension-post-opentypeextension.md) | <span data-ttu-id="5adb4-173">[openTypeExtension](opentypeextension.md) (en una instancia recurso existente), o un nuevo [contacto](../resources/contact.md), [evento](../resources/event.md)o [mensaje](../resources/message.md) que contiene un objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="5adb4-173">[openTypeExtension](opentypeextension.md)(in an existing resource instance), or a new [contact](../resources/contact.md), [event](../resources/event.md), or [message](../resources/message.md) that contains an openTypeExtension object.</span></span> | <span data-ttu-id="5adb4-174">Cree un objeto openTypeExtension en una instancia de recursos nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="5adb4-174">Create an openTypeExtension object in an existing or new resource instance.</span></span>|
|[<span data-ttu-id="5adb4-175">Get</span><span class="sxs-lookup"><span data-stu-id="5adb4-175">Get</span></span>](../api/opentypeextension-get.md) | [<span data-ttu-id="5adb4-176">openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="5adb4-176">openTypeExtension</span></span>](opentypeextension.md) |<span data-ttu-id="5adb4-177">Lea las propiedades y las relaciones del objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="5adb4-177">Read properties and relationships of openTypeExtension object.</span></span>|
|[<span data-ttu-id="5adb4-178">Actualizar</span><span class="sxs-lookup"><span data-stu-id="5adb4-178">Update</span></span>](../api/opentypeextension-update.md) | [<span data-ttu-id="5adb4-179">openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="5adb4-179">openTypeExtension</span></span>](opentypeextension.md) |<span data-ttu-id="5adb4-180">Actualice el objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="5adb4-180">Update openTypeExtension object.</span></span> |
|[<span data-ttu-id="5adb4-181">Eliminar</span><span class="sxs-lookup"><span data-stu-id="5adb4-181">Delete</span></span>](../api/opentypeextension-delete.md) | <span data-ttu-id="5adb4-182">Ninguno</span><span class="sxs-lookup"><span data-stu-id="5adb4-182">None</span></span> |<span data-ttu-id="5adb4-183">Elimine el objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="5adb4-183">Delete openTypeExtension object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "openTypeExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
