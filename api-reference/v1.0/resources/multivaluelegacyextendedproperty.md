# <a name="multivaluelegacyextendedproperty-resource-type"></a><span data-ttu-id="649bb-101">Tipo de recurso multiValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="649bb-101">multiValueLegacyExtendedProperty resource type</span></span>

<span data-ttu-id="649bb-102">Propiedad extendida que contiene una colección de valores.</span><span class="sxs-lookup"><span data-stu-id="649bb-102">An extended property that contains a collection of values.</span></span>

<span data-ttu-id="649bb-103">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="649bb-103">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span>

## <a name="methods"></a><span data-ttu-id="649bb-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="649bb-104">Methods</span></span>

| <span data-ttu-id="649bb-105">Método</span><span class="sxs-lookup"><span data-stu-id="649bb-105">Method</span></span>           | <span data-ttu-id="649bb-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="649bb-106">Return Type</span></span>    |<span data-ttu-id="649bb-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="649bb-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="649bb-108">Publicar</span><span class="sxs-lookup"><span data-stu-id="649bb-108">Post</span></span>](../api/multivaluelegacyextendedproperty_post_multivalueextendedproperties.md) | <span data-ttu-id="649bb-p101">Instancia de recurso admitida: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md) o [contactFolder](../resources/contactfolder.md). Tenga en cuenta que no se admite [post](../resources/post.md) de grupo.</span><span class="sxs-lookup"><span data-stu-id="649bb-p101">A supported resource instance: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), or [contactFolder](../resources/contactfolder.md). Note that group [post](../resources/post.md) is not supported.</span></span> | <span data-ttu-id="649bb-111">Crea una **multiValueLegacyExtendedProperty** en una instancia nueva o existente de un recurso compatible.</span><span class="sxs-lookup"><span data-stu-id="649bb-111">Create a **multiValueLegacyExtendedProperty** in a new or existing instance of a supported resource.</span></span> |
|[<span data-ttu-id="649bb-112">Get</span><span class="sxs-lookup"><span data-stu-id="649bb-112">Get</span></span>](../api/multivaluelegacyextendedproperty_get.md) |<span data-ttu-id="649bb-113">Instancia de recurso admitida ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md) o [post](../resources/post.md) de grupo) expandida con un objeto [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="649bb-113">A supported resource instance ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md), or group [post](../resources/post.md)) expanded with a [multiValueLegacyExtendedProperty](multivaluelegacyextendedproperty.md) object.</span></span> |<span data-ttu-id="649bb-114">Obtiene una instancia del recurso con una propiedad extendida mediante `$expand`.</span><span class="sxs-lookup"><span data-stu-id="649bb-114">Get a resource instance with an extended property using `$expand`.</span></span>|

## <a name="properties"></a><span data-ttu-id="649bb-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="649bb-115">Properties</span></span>
| <span data-ttu-id="649bb-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="649bb-116">Property</span></span>     | <span data-ttu-id="649bb-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="649bb-117">Type</span></span>   |<span data-ttu-id="649bb-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="649bb-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="649bb-119">id</span><span class="sxs-lookup"><span data-stu-id="649bb-119">id</span></span>|<span data-ttu-id="649bb-120">cadena</span><span class="sxs-lookup"><span data-stu-id="649bb-120">string</span></span>|<span data-ttu-id="649bb-p102">Identificador de la propiedad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="649bb-p102">The property identifier. Read-only.</span></span>|
|<span data-ttu-id="649bb-123">value</span><span class="sxs-lookup"><span data-stu-id="649bb-123">value</span></span>|<span data-ttu-id="649bb-124">colección string</span><span class="sxs-lookup"><span data-stu-id="649bb-124">string collection</span></span>|<span data-ttu-id="649bb-125">Colección de valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="649bb-125">A collection of property values.</span></span>|

## <a name="relationships"></a><span data-ttu-id="649bb-126">Relaciones</span><span class="sxs-lookup"><span data-stu-id="649bb-126">Relationships</span></span>
<span data-ttu-id="649bb-127">Ninguno</span><span class="sxs-lookup"><span data-stu-id="649bb-127">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="649bb-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="649bb-128">JSON representation</span></span>

<span data-ttu-id="649bb-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="649bb-129">Here is a JSON representation of the resource.</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.multiValueLegacyExtendedProperty"
}-->

```json
{
  "id": "string (identifier)",
  "value": ["string"]
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "multiValueLegacyExtendedProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->