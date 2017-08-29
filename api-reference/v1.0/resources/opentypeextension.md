# <a name="opentypeextension-resource-type-open-extensions"></a><span data-ttu-id="0e693-101">Tipo de recurso openTypeExtension (extensiones abiertas)</span><span class="sxs-lookup"><span data-stu-id="0e693-101">openTypeExtension resource type (open extensions)</span></span>

<span data-ttu-id="0e693-p101">Las extensiones abiertas (anteriormente conocidas como extensiones de datos de Office 365) ofrecen una manera fácil de agregar propiedades sin tipo directamente a un recurso en Microsoft Graph. El recurso **openTypeExtension** representa las extensiones abiertas. Las extensiones abiertas agregadas a un recurso se muestran en la propiedad de navegación **extensions**, que se deriva del tipo abstracto [extension](extension.md).  Cada extensión tiene una propiedad **extensionName** que es la única predefinida y que puede ser escrita para todas las extensiones, junto con los datos personalizados. Una forma de asegurarse de que los nombres de extensión son únicos es usar un método inverso del formato de nombres de dominio (DNS) que dependa de _su propio dominio_, por ejemplo, `Com.Contoso.ContactInfo`. No use el dominio de Microsoft (`Com.Microsoft` o `Com.OnMicrosoft`) en un nombre de extensión.</span><span class="sxs-lookup"><span data-stu-id="0e693-p101">Open extensions (formerly known as Office 365 data extensions) gives you an easy way to directly add untyped properties to a resource in Microsoft Graph. Open extensions are represented by the **openTypeExtension** resource. Any open extension added to a resource shows up in the **extensions** navigation property, which is derived from the [extension](extension.md) abstract type.  Each extension has an **extensionName** property which is the only pre-defined, writable property for all extensions, along with your custom data. One way to help make sure extension names are unique is to use a reverse domain name system (DNS) format that is dependent on _your own domain_, for example, `Com.Contoso.ContactInfo`. Do not use the Microsoft domain (`Com.Microsoft` or `Com.OnMicrosoft`) in an extension name.</span></span>

<span data-ttu-id="0e693-108">Ejemplo de extensión abierta: [Agregar datos personalizados a los usuarios mediante extensiones abiertas](../../../concepts/extensibility_open_users.md)</span><span class="sxs-lookup"><span data-stu-id="0e693-108">Open extension example: [Add custom data to users using open extensions](../../../concepts/extensibility_open_users.md)</span></span>

<span data-ttu-id="0e693-109">Las extensiones abiertas son compatibles con los recursos siguientes en las versiones correspondientes: disponibilidad general (GA: /v1.0 y /beta) o en versión preliminar (/beta).</span><span class="sxs-lookup"><span data-stu-id="0e693-109">Open extensions are supported by the following resources in the corresponding versions - general availability (GA: /v1.0 and /beta) or preview (/beta).</span></span>

| <span data-ttu-id="0e693-110">Recurso</span><span class="sxs-lookup"><span data-stu-id="0e693-110">Resource</span></span> | <span data-ttu-id="0e693-111">Versión</span><span class="sxs-lookup"><span data-stu-id="0e693-111">Version</span></span> |
|---------------|-------|
| [<span data-ttu-id="0e693-112">Unidad administrativa</span><span class="sxs-lookup"><span data-stu-id="0e693-112">Administrative unit</span></span>](../../beta/resources/administrativeunit.md)  | <span data-ttu-id="0e693-113">Solo versión preliminar</span><span class="sxs-lookup"><span data-stu-id="0e693-113">Preview only</span></span> |
| [<span data-ttu-id="0e693-114">Evento de calendario</span><span class="sxs-lookup"><span data-stu-id="0e693-114">Calendar event</span></span>](event.md) | <span data-ttu-id="0e693-115">GA</span><span class="sxs-lookup"><span data-stu-id="0e693-115">GA</span></span> |
| <span data-ttu-id="0e693-116">[Evento de calendario](event.md) de grupo</span><span class="sxs-lookup"><span data-stu-id="0e693-116">[Group calendar event](event.md)</span></span> | <span data-ttu-id="0e693-117">GA</span><span class="sxs-lookup"><span data-stu-id="0e693-117">GA</span></span> |
| <span data-ttu-id="0e693-118">[Publicación](post.md) de subproceso de conversación de grupo</span><span class="sxs-lookup"><span data-stu-id="0e693-118">Group conversation thread [post](post.md)</span></span> | <span data-ttu-id="0e693-119">GA</span><span class="sxs-lookup"><span data-stu-id="0e693-119">GA</span></span> |
| [<span data-ttu-id="0e693-120">device</span><span class="sxs-lookup"><span data-stu-id="0e693-120">device</span></span>](device.md) | <span data-ttu-id="0e693-121">GA</span><span class="sxs-lookup"><span data-stu-id="0e693-121">GA</span></span> |
| [<span data-ttu-id="0e693-122">group</span><span class="sxs-lookup"><span data-stu-id="0e693-122">group</span></span>](group.md) | <span data-ttu-id="0e693-123">GA</span><span class="sxs-lookup"><span data-stu-id="0e693-123">GA</span></span> |
| [<span data-ttu-id="0e693-124">message</span><span class="sxs-lookup"><span data-stu-id="0e693-124">message</span></span>](message.md) | <span data-ttu-id="0e693-125">GA</span><span class="sxs-lookup"><span data-stu-id="0e693-125">GA</span></span> |
| [<span data-ttu-id="0e693-126">organization</span><span class="sxs-lookup"><span data-stu-id="0e693-126">organization</span></span>](organization.md) | <span data-ttu-id="0e693-127">GA</span><span class="sxs-lookup"><span data-stu-id="0e693-127">GA</span></span> |
| [<span data-ttu-id="0e693-128">Contacto personal</span><span class="sxs-lookup"><span data-stu-id="0e693-128">Personal contact</span></span>](contact.md) | <span data-ttu-id="0e693-129">GA</span><span class="sxs-lookup"><span data-stu-id="0e693-129">GA</span></span> |
| [<span data-ttu-id="0e693-130">user</span><span class="sxs-lookup"><span data-stu-id="0e693-130">user</span></span>](user.md) | <span data-ttu-id="0e693-131">GA</span><span class="sxs-lookup"><span data-stu-id="0e693-131">GA</span></span> |

### <a name="use-open-extensions-for-outlook-resources-or-extended-properties"></a><span data-ttu-id="0e693-132">¿Se deben utilizar extensiones abiertas (para recursos de Outlook) o propiedades extendidas?</span><span class="sxs-lookup"><span data-stu-id="0e693-132">Use open extensions (for Outlook resources) or extended properties?</span></span>

<span data-ttu-id="0e693-p102">Las extensiones abiertas son la solución recomendada en la mayoría de escenarios relacionados con el almacenamiento y el acceso de datos personalizados. Sin embargo, si necesita acceder a datos personalizados para las propiedades MAPI de Outlook que no están ya expuestas en los [metadatos API de Microsoft Graph](http://developer.microsoft.com/en-us/graph/docs/overview/call_api), puede usar [propiedades extendidas y su API REST](extended-properties-overview.md). Puede comprobar las propiedades que exponen los metadatos en: https://graph.microsoft.com/v1.0/$metadata.</span><span class="sxs-lookup"><span data-stu-id="0e693-p102">Open extensions is the recommended solution for most scenarios involving storing and accessing custom data. If, however, you need to access custom data for Outlook MAPI properties that are not already exposed through the [Microsoft Graph API metadata](http://developer.microsoft.com/en-us/graph/docs/overview/call_api), you can use [extended properties and its REST API](extended-properties-overview.md). You can verify which properties the metadata exposes at https://graph.microsoft.com/v1.0/$metadata.</span></span>


## <a name="json-representation"></a><span data-ttu-id="0e693-136">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0e693-136">JSON representation</span></span>

<span data-ttu-id="0e693-137">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0e693-137">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="0e693-138">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0e693-138">Properties</span></span>
| <span data-ttu-id="0e693-139">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0e693-139">Property</span></span>     | <span data-ttu-id="0e693-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="0e693-140">Type</span></span>   |<span data-ttu-id="0e693-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e693-141">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0e693-142">extensionName</span><span class="sxs-lookup"><span data-stu-id="0e693-142">extensionName</span></span>|<span data-ttu-id="0e693-143">String</span><span class="sxs-lookup"><span data-stu-id="0e693-143">String</span></span>|<span data-ttu-id="0e693-p103">Un identificador de texto único para una extensión abierta de tipo abierto. Necesario.</span><span class="sxs-lookup"><span data-stu-id="0e693-p103">A unique text identifier for an open type open extension. Required.</span></span>|
|<span data-ttu-id="0e693-146">id</span><span class="sxs-lookup"><span data-stu-id="0e693-146">id</span></span>|<span data-ttu-id="0e693-147">String</span><span class="sxs-lookup"><span data-stu-id="0e693-147">String</span></span>| <span data-ttu-id="0e693-p104">Un identificador completo que concatena el tipo de extensión con el **extensionName**. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0e693-p104">A fully qualified identifier that concatenates the extension type with the **extensionName**. Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="0e693-150">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0e693-150">Relationships</span></span>
<span data-ttu-id="0e693-151">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0e693-151">None</span></span>


## <a name="methods"></a><span data-ttu-id="0e693-152">Métodos</span><span class="sxs-lookup"><span data-stu-id="0e693-152">Methods</span></span>

| <span data-ttu-id="0e693-153">Método</span><span class="sxs-lookup"><span data-stu-id="0e693-153">Method</span></span>           | <span data-ttu-id="0e693-154">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0e693-154">Return Type</span></span>    |<span data-ttu-id="0e693-155">Descripción</span><span class="sxs-lookup"><span data-stu-id="0e693-155">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="0e693-156">Post</span><span class="sxs-lookup"><span data-stu-id="0e693-156">Post</span></span>](../api/opentypeextension_post_opentypeextension.md) | <span data-ttu-id="0e693-157">[openTypeExtension](opentypeextension.md) (en una instancia de recurso existente) o un [contacto](../resources/contact.md), [evento](../resources/event.md) o [mensaje](../resources/message.md) nuevo que contenga un objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="0e693-157">[openTypeExtension](opentypeextension.md) (in an existing resource instance), or a new [contact](../resources/contact.md), [event](../resources/event.md), or [message](../resources/message.md) that contains an openTypeExtension object.</span></span> | <span data-ttu-id="0e693-158">Cree un objeto openTypeExtension en una instancia de recursos nueva o existente.</span><span class="sxs-lookup"><span data-stu-id="0e693-158">Create an openTypeExtension object in an existing or new resource instance.</span></span>|
|[<span data-ttu-id="0e693-159">Get</span><span class="sxs-lookup"><span data-stu-id="0e693-159">Get</span></span>](../api/opentypeextension_get.md) | [<span data-ttu-id="0e693-160">openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="0e693-160">openTypeExtension</span></span>](opentypeextension.md) |<span data-ttu-id="0e693-161">Lea las propiedades y las relaciones del objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="0e693-161">Read properties and relationships of openTypeExtension object.</span></span>|
|[<span data-ttu-id="0e693-162">Actualizar</span><span class="sxs-lookup"><span data-stu-id="0e693-162">Update</span></span>](../api/opentypeextension_update.md) | [<span data-ttu-id="0e693-163">openTypeExtension</span><span class="sxs-lookup"><span data-stu-id="0e693-163">openTypeExtension</span></span>](opentypeextension.md)   |<span data-ttu-id="0e693-164">Actualice el objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="0e693-164">Update openTypeExtension object.</span></span> |
|[<span data-ttu-id="0e693-165">Eliminar</span><span class="sxs-lookup"><span data-stu-id="0e693-165">Delete</span></span>](../api/opentypeextension_delete.md) | <span data-ttu-id="0e693-166">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0e693-166">None</span></span> |<span data-ttu-id="0e693-167">Elimine el objeto openTypeExtension.</span><span class="sxs-lookup"><span data-stu-id="0e693-167">Delete openTypeExtension object.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "openTypeExtension resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->