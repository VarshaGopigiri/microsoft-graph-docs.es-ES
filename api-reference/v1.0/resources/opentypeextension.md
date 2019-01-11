---
title: Tipo de recurso openTypeExtension (extensiones abiertas)
description: Extensiones Open (anteriormente conocidas como extensiones de datos de Office 365) proporcionan una forma sencilla de agregar propiedades sin tipo directamente en un recurso de Microsoft Graph.
localization_priority: Priority
ms.openlocfilehash: e0e7bf992d75ccb8ee04a3cccb90fd42c996d50a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/11/2019
ms.locfileid: "27891689"
---
# <a name="opentypeextension-resource-type-open-extensions"></a><span data-ttu-id="80a4d-103">Tipo de recurso openTypeExtension (extensiones abiertas)</span><span class="sxs-lookup"><span data-stu-id="80a4d-103">openTypeExtension resource type (open extensions)</span></span>

<span data-ttu-id="80a4d-104">Extensiones Open (anteriormente conocidas como extensiones de datos de Office 365) proporcionan una forma sencilla de agregar propiedades sin tipo directamente en un recurso de Microsoft Graph.</span><span class="sxs-lookup"><span data-stu-id="80a4d-104">Open extensions (formerly known as Office 365 data extensions) provide an easy way to directly add untyped properties to a resource in Microsoft Graph.</span></span>

<span data-ttu-id="80a4d-105">El recurso **openTypeExtension** representa las extensiones abiertas.</span><span class="sxs-lookup"><span data-stu-id="80a4d-105">Open extensions are represented by the **openTypeExtension** resource.</span></span> <span data-ttu-id="80a4d-106">Las extensiones abiertas agregadas a un recurso se muestran en la propiedad de navegación **extensions**, que se deriva del tipo abstracto [extension](extension.md).</span><span class="sxs-lookup"><span data-stu-id="80a4d-106">Any open extension added to a resource shows up in the **extensions** navigation property, which is derived from the [extension](extension.md) abstract type.</span></span> <span data-ttu-id="80a4d-107">Cada extensión tiene una propiedad **extensionName** que es la única predefinida y que puede ser escrita para todas las extensiones, junto con los datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="80a4d-107">Each extension has an **extensionName** property which is the only pre-defined, writable property for all extensions, along with your custom data.</span></span>

<span data-ttu-id="80a4d-108">Una forma de asegurarse de que los nombres de extensión son únicos es usar un método inverso del formato de nombres de dominio (DNS) que dependa de _su propio dominio_, por ejemplo, `Com.Contoso.ContactInfo`.</span><span class="sxs-lookup"><span data-stu-id="80a4d-108">One way to help make sure extension names are unique is to use a reverse domain name system (DNS) format that is dependent on _your own domain_, for example, `Com.Contoso.ContactInfo`.</span></span> <span data-ttu-id="80a4d-109">No use el dominio de Microsoft (`Com.Microsoft` o `Com.OnMicrosoft`) en un nombre de extensión.</span><span class="sxs-lookup"><span data-stu-id="80a4d-109">Do not use the Microsoft domain (`Com.Microsoft` or `Com.OnMicrosoft`) in an extension name.</span></span>

<span data-ttu-id="80a4d-110">Ejemplo de extensión abierta: [Agregar datos personalizados a los usuarios mediante extensiones abiertas](/graph/extensibility-open-users)</span><span class="sxs-lookup"><span data-stu-id="80a4d-110">Open extension example: [Add custom data to users using open extensions](/graph/extensibility-open-users)</span></span>

<span data-ttu-id="80a4d-111">Las extensiones abiertas son compatibles con los recursos siguientes en las versiones correspondientes: disponibilidad general (GA: /v1.0 y /beta) o en versión preliminar (/beta).</span><span class="sxs-lookup"><span data-stu-id="80a4d-111">Open extensions are supported by the following resources in the corresponding versions - general availability (GA: /v1.0 and /beta) or preview (/beta).</span></span>

|<span data-ttu-id="80a4d-112">Recurso</span><span class="sxs-lookup"><span data-stu-id="80a4d-112">Resource</span></span> |<span data-ttu-id="80a4d-113">Versión</span><span class="sxs-lookup"><span data-stu-id="80a4d-113">Version</span></span> |
|:---------------|:-------|
| [<span data-ttu-id="80a4d-114">Unidad administrativa</span><span class="sxs-lookup"><span data-stu-id="80a4d-114">Administrative unit</span></span>](/graph/api/resources/administrativeunit?view=graph-rest-beta)  | <span data-ttu-id="80a4d-115">Solo versión preliminar</span><span class="sxs-lookup"><span data-stu-id="80a4d-115">Preview only</span></span> |
| [<span data-ttu-id="80a4d-116">Evento de calendario</span><span class="sxs-lookup"><span data-stu-id="80a4d-116">Calendar event</span></span>](event.md) | <span data-ttu-id="80a4d-117">GA</span><span class="sxs-lookup"><span data-stu-id="80a4d-117">GA</span></span> |
| <span data-ttu-id="80a4d-118">[Evento de calendario](event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="80a4d-118">Group [calendar event](event.md)</span></span> | <span data-ttu-id="80a4d-119">GA</span><span class="sxs-lookup"><span data-stu-id="80a4d-119">GA</span></span> |
| <span data-ttu-id="80a4d-120">[Publicación](post.md) de subproceso de conversación de grupo</span><span class="sxs-lookup"><span data-stu-id="80a4d-120">Group conversation thread [post](post.md)</span></span> | <span data-ttu-id="80a4d-121">GA</span><span class="sxs-lookup"><span data-stu-id="80a4d-121">GA</span></span> |
| [<span data-ttu-id="80a4d-122">device</span><span class="sxs-lookup"><span data-stu-id="80a4d-122">device</span></span>](device.md) | <span data-ttu-id="80a4d-123">GA</span><span class="sxs-lookup"><span data-stu-id="80a4d-123">GA</span></span> |
| [<span data-ttu-id="80a4d-124">group</span><span class="sxs-lookup"><span data-stu-id="80a4d-124">group</span></span>](group.md) | <span data-ttu-id="80a4d-125">GA</span><span class="sxs-lookup"><span data-stu-id="80a4d-125">GA</span></span> |
| [<span data-ttu-id="80a4d-126">message</span><span class="sxs-lookup"><span data-stu-id="80a4d-126">message</span></span>](message.md) | <span data-ttu-id="80a4d-127">GA</span><span class="sxs-lookup"><span data-stu-id="80a4d-127">GA</span></span> |
| [<span data-ttu-id="80a4d-128">organization</span><span class="sxs-lookup"><span data-stu-id="80a4d-128">organization</span></span>](organization.md) | <span data-ttu-id="80a4d-129">GA</span><span class="sxs-lookup"><span data-stu-id="80a4d-129">GA</span></span> |
| [<span data-ttu-id="80a4d-130">Contacto personal</span><span class="sxs-lookup"><span data-stu-id="80a4d-130">Personal contact</span></span>](contact.md) | <span data-ttu-id="80a4d-131">GA</span><span class="sxs-lookup"><span data-stu-id="80a4d-131">GA</span></span> |
| [<span data-ttu-id="80a4d-132">user</span><span class="sxs-lookup"><span data-stu-id="80a4d-132">user</span></span>](user.md) | <span data-ttu-id="80a4d-133">GA</span><span class="sxs-lookup"><span data-stu-id="80a4d-133">GA</span></span> |

## <a name="outlook-specific-considerations"></a><span data-ttu-id="80a4d-134">Consideraciones sobre específica de Outlook</span><span class="sxs-lookup"><span data-stu-id="80a4d-134">Outlook-specific considerations</span></span>

<span data-ttu-id="80a4d-135">Cada extensión open presente en un recurso de Outlook (evento, mensaje o contacto personal) se almacena en una [propiedad con nombre de MAPI](https://msdn.microsoft.com/library/cc765864(v=office.15).aspx).</span><span class="sxs-lookup"><span data-stu-id="80a4d-135">Each open extension present on an Outlook resource (event, message, or personal contact) is stored in a [MAPI named property](https://msdn.microsoft.com/library/cc765864(v=office.15).aspx).</span></span> <span data-ttu-id="80a4d-136">Al crear extensiones open para Outlook, tenga en cuenta que con el nombre de las propiedades de MAPI son un recurso finito en el buzón del usuario.</span><span class="sxs-lookup"><span data-stu-id="80a4d-136">When you create open extensions for Outlook, consider that MAPI named properties are a finite resource in a user's mailbox.</span></span> <span data-ttu-id="80a4d-137">Cuando se agota la cuota de la propiedad con nombre de un usuario, no se puede crear las propiedades más con nombre de dicho usuario.</span><span class="sxs-lookup"><span data-stu-id="80a4d-137">When a user's named property quota is exhausted, you can't create any more named properties for that user.</span></span> <span data-ttu-id="80a4d-138">Esto se puede producir un comportamiento inesperado de clientes que se basan en las propiedades con nombre para la función.</span><span class="sxs-lookup"><span data-stu-id="80a4d-138">This can result in unexpected behavior from clients that rely on named properties to function.</span></span>

<span data-ttu-id="80a4d-139">Aplique las siguientes directrices al crear extensiones open en recursos de Outlook:</span><span class="sxs-lookup"><span data-stu-id="80a4d-139">Apply the following guidelines when you create open extensions on Outlook resources:</span></span>

- <span data-ttu-id="80a4d-140">Cree el número mínimo de extensiones necesarias.</span><span class="sxs-lookup"><span data-stu-id="80a4d-140">Create the minimum number of extensions required.</span></span> <span data-ttu-id="80a4d-141">La mayoría de las aplicaciones deben requerir no más de una extensión.</span><span class="sxs-lookup"><span data-stu-id="80a4d-141">Most applications should require no more than one extension.</span></span> <span data-ttu-id="80a4d-142">Las extensiones no tienen propiedades de conjunto definido ni estructura, por lo que puede almacenar varios valores en una única extensión.</span><span class="sxs-lookup"><span data-stu-id="80a4d-142">Extensions have no set defined properties or structure, so you can store multiple values in a single extension.</span></span>
- <span data-ttu-id="80a4d-143">Evitar extensiones de nombres de una forma variable (por ejemplo, basándose en la entrada del usuario, etcetera.).</span><span class="sxs-lookup"><span data-stu-id="80a4d-143">Avoid naming extensions in a variable manner (such as based on user input, etc.).</span></span> <span data-ttu-id="80a4d-144">Cada vez que se crea una extensión abierta con un nombre nuevo que no se ha usado en el buzón de un usuario antes, se crea un nuevo MAPI con nombre de propiedad.</span><span class="sxs-lookup"><span data-stu-id="80a4d-144">Each time an open extension is created with a new name that has not been used in a user's mailbox before, a new MAPI named property is created.</span></span> <span data-ttu-id="80a4d-145">Quitar la extensión no quita la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="80a4d-145">Removing the extension does not remove the named property.</span></span>

### <a name="use-open-extensions-for-outlook-resources-or-extended-properties"></a><span data-ttu-id="80a4d-146">Utilizar extensiones open (para recursos de Outlook) o las propiedades extendidas</span><span class="sxs-lookup"><span data-stu-id="80a4d-146">Use open extensions (for Outlook resources) or extended properties</span></span>

<span data-ttu-id="80a4d-147">Extensiones de Open son la solución recomendada para la mayoría de los escenarios que implican almacenar y obtener acceso a datos personalizados.</span><span class="sxs-lookup"><span data-stu-id="80a4d-147">Open extensions are the recommended solution for most scenarios involving storing and accessing custom data.</span></span> <span data-ttu-id="80a4d-148">Si, sin embargo, necesita tener acceso a datos personalizados para las propiedades de MAPI de Outlook que ya no están expuestas a través de los [metadatos de la API de Microsoft Graph](https://developer.microsoft.com/graph/docs/overview/call_api), puede usar [las propiedades extendidas y su API de REST](extended-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="80a4d-148">If, however, you need to access custom data for Outlook MAPI properties that are not already exposed through the [Microsoft Graph API metadata](https://developer.microsoft.com/graph/docs/overview/call_api), you can use [extended properties and its REST API](extended-properties-overview.md).</span></span> <span data-ttu-id="80a4d-149">Puede comprobar qué propiedades expone los metadatos en [ https://graph.microsoft.com/v1.0/$metadata](https://graph.microsoft.com/v1.0/$metadata).</span><span class="sxs-lookup"><span data-stu-id="80a4d-149">You can verify which properties the metadata exposes at [https://graph.microsoft.com/v1.0/$metadata](https://graph.microsoft.com/v1.0/$metadata).</span></span>

## <a name="json-representation"></a><span data-ttu-id="80a4d-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="80a4d-150">JSON representation</span></span>

<span data-ttu-id="80a4d-151">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="80a4d-151">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "openType": true,
  "optionalProperties": [],
  "baseType": "microsoft.graph.extension",
  "@odata.type": "microsoft.graph.openTypeExtension"
}-->

```json
{
  "extensionName": "string",
  "id": "string (identifier)"
}

```

## <a name="properties"></a><span data-ttu-id="80a4d-152">Propiedades</span><span class="sxs-lookup"><span data-stu-id="80a4d-152">Properties</span></span>

|<span data-ttu-id="80a4d-153">Propiedad</span><span class="sxs-lookup"><span data-stu-id="80a4d-153">Property</span></span> | <span data-ttu-id="80a4d-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="80a4d-154">Type</span></span> | <span data-ttu-id="80a4d-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="80a4d-155">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="80a4d-156">extensionName</span><span class="sxs-lookup"><span data-stu-id="80a4d-156">extensionName</span></span>|<span data-ttu-id="80a4d-157">Cadena</span><span class="sxs-lookup"><span data-stu-id="80a4d-157">String</span></span>|<span data-ttu-id="80a4d-p107">Un identificador de texto único para una extensión abierta de tipo abierto. Necesario.</span><span class="sxs-lookup"><span data-stu-id="80a4d-p107">A unique text identifier for an open type open extension. Required.</span></span>|
|<span data-ttu-id="80a4d-160">id</span><span class="sxs-lookup"><span data-stu-id="80a4d-160">id</span></span>|<span data-ttu-id="80a4d-161">String</span><span class="sxs-lookup"><span data-stu-id="80a4d-161">String</span></span>| <span data-ttu-id="80a4d-p108">Un identificador completo que concatena el tipo de extensión con el **extensionName**. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="80a4d-p108">A fully qualified identifier that concatenates the extension type with the **extensionName**. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="80a4d-164">Relaciones</span><span class="sxs-lookup"><span data-stu-id="80a4d-164">Relationships</span></span>

<span data-ttu-id="80a4d-165">Ninguno</span><span class="sxs-lookup"><span data-stu-id="80a4d-165">None</span></span>

## <a name="methods"></a><span data-ttu-id="80a4d-166">Métodos</span><span class="sxs-lookup"><span data-stu-id="80a4d-166">Methods</span></span>

|<span data-ttu-id="80a4d-167">Método</span><span class="sxs-lookup"><span data-stu-id="80a4d-167">Method</span></span> | <span data-ttu-id="80a4d-168">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80a4d-168">Return Type</span></span> | <span data-ttu-id="80a4d-169">Descripción</span><span class="sxs-lookup"><span data-stu-id="80a4d-169">Description</span></span> |
|:---------------|:--------|:----------|
|[<span data-ttu-id="80a4d-170">Post</span><span class="sxs-lookup"><span data-stu-id="80a4d-170">Post</span></span>](../api/opentypeextension-post-opentypeextension.md) | <span data-ttu-id="80a4d-171">[openTypeExtension](opentypeextension.md) (en una instancia de recurso existente) o un [contacto](../resources/contact.md), [evento](../resources/event.md) o [mensaje](../resources/message.md) nuevo que contenga un objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="80a4d-171">[openTypeExtension](opentypeextension.md) (in an existing resource instance), or a new [contact](../resources/contact.md), [event](../resources/event.md), or [message](../resources/message.md) that contains an openTypeExtension object</span></span> | <span data-ttu-id="80a4d-172">Cree un objeto openTypeExtension en una instancia de recursos nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="80a4d-172">Create an openTypeExtension object in an existing or new resource instance.</span></span>|
|[<span data-ttu-id="80a4d-173">Get</span><span class="sxs-lookup"><span data-stu-id="80a4d-173">Get</span></span>](../api/opentypeextension-get.md) | [<span data-ttu-id="80a4d-174">openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="80a4d-174">openTypeExtension</span></span>](opentypeextension.md) |<span data-ttu-id="80a4d-175">Lea las propiedades y las relaciones del objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="80a4d-175">Read properties and relationships of openTypeExtension object.</span></span>|
|[<span data-ttu-id="80a4d-176">Actualizar</span><span class="sxs-lookup"><span data-stu-id="80a4d-176">Update</span></span>](../api/opentypeextension-update.md) | [<span data-ttu-id="80a4d-177">openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="80a4d-177">openTypeExtension</span></span>](opentypeextension.md) |<span data-ttu-id="80a4d-178">Actualice el objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="80a4d-178">Update openTypeExtension object.</span></span> |
|[<span data-ttu-id="80a4d-179">Eliminar</span><span class="sxs-lookup"><span data-stu-id="80a4d-179">Delete</span></span>](../api/opentypeextension-delete.md) | <span data-ttu-id="80a4d-180">Ninguno</span><span class="sxs-lookup"><span data-stu-id="80a4d-180">None</span></span> |<span data-ttu-id="80a4d-181">Elimine el objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="80a4d-181">Delete openTypeExtension object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "openTypeExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
