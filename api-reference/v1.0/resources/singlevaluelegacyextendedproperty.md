# <a name="singlevaluelegacyextendedproperty-resource-type"></a><span data-ttu-id="4bdb1-101">Tipo de recurso singleValueLegacyExtendedProperty</span><span class="sxs-lookup"><span data-stu-id="4bdb1-101">singleValueLegacyExtendedProperty resource type</span></span>

<span data-ttu-id="4bdb1-102">Propiedad extendida que contiene un solo valor.</span><span class="sxs-lookup"><span data-stu-id="4bdb1-102">An extended property that contains a single value.</span></span> 

<span data-ttu-id="4bdb1-103">Consulte el artículo de [información general sobre las propiedades extendidas](../resources/extended-properties-overview.md) para obtener más información sobre cuándo usar las extensiones abiertas o las propiedades extendidas y cómo especificar las propiedades extendidas.</span><span class="sxs-lookup"><span data-stu-id="4bdb1-103">See [Extended properties overview](../resources/extended-properties-overview.md) for more information about when to use open extensions or extended properties, and how to specify extended properties.</span></span> 


## <a name="methods"></a><span data-ttu-id="4bdb1-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="4bdb1-104">Methods</span></span>

| <span data-ttu-id="4bdb1-105">Método</span><span class="sxs-lookup"><span data-stu-id="4bdb1-105">Method</span></span>           | <span data-ttu-id="4bdb1-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4bdb1-106">Return Type</span></span>    |<span data-ttu-id="4bdb1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bdb1-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="4bdb1-108">Post</span><span class="sxs-lookup"><span data-stu-id="4bdb1-108">Post</span></span>](../api/singlevaluelegacyextendedproperty_post_singlevalueextendedproperties.md) | <span data-ttu-id="4bdb1-109">Instancia de recurso admitida: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md) o [contactFolder](../resources/contactfolder.md), pero no [post](../resources/post.md) de grupo.</span><span class="sxs-lookup"><span data-stu-id="4bdb1-109">A supported resource instance: [message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), or [contactFolder](../resources/contactfolder.md), but not group [post](../resources/post.md).</span></span> | <span data-ttu-id="4bdb1-110">Crea una **singleValueLegacyExtendedProperty** en una instancia nueva o existente de un recurso compatible.</span><span class="sxs-lookup"><span data-stu-id="4bdb1-110">Create a **singleValueLegacyExtendedProperty** in a new or existing instance of a supported resource.</span></span> |
|[<span data-ttu-id="4bdb1-111">Get</span><span class="sxs-lookup"><span data-stu-id="4bdb1-111">Get</span></span>](../api/singlevaluelegacyextendedproperty_get.md) |<span data-ttu-id="4bdb1-112">Instancia o colección de instancias de recurso admitidas: ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md) o [post](../resources/post.md) de grupo), o una instancia de este tipo expandida con un objeto [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md).</span><span class="sxs-lookup"><span data-stu-id="4bdb1-112">One or a collection of supported resource instance ([message](../resources/message.md), [mailFolder](../resources/mailfolder.md), [event](../resources/event.md), [calendar](../resources/calendar.md), [contact](../resources/contact.md), [contactFolder](../resources/contactfolder.md), or group [post](../resources/post.md)), or one such instance expanded with a [singleValueLegacyExtendedProperty](singlevaluelegacyextendedproperty.md) object.</span></span> |<span data-ttu-id="4bdb1-113">Obtiene una instancia del recurso con una propiedad extendida mediante `$expand` o `$filter`.</span><span class="sxs-lookup"><span data-stu-id="4bdb1-113">Get a resource instance with an extended property using `$expand` or `$filter`.</span></span>|

## <a name="properties"></a><span data-ttu-id="4bdb1-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4bdb1-114">Properties</span></span>
| <span data-ttu-id="4bdb1-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4bdb1-115">Property</span></span>     | <span data-ttu-id="4bdb1-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="4bdb1-116">Type</span></span>   |<span data-ttu-id="4bdb1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="4bdb1-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="4bdb1-118">id</span><span class="sxs-lookup"><span data-stu-id="4bdb1-118">id</span></span>|<span data-ttu-id="4bdb1-119">string</span><span class="sxs-lookup"><span data-stu-id="4bdb1-119">string</span></span>|<span data-ttu-id="4bdb1-p101">Identificador de propiedad que se usa para identificar la propiedad. Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4bdb1-p101">The property ID used to identify the property. Read-only.</span></span>|
|<span data-ttu-id="4bdb1-122">value</span><span class="sxs-lookup"><span data-stu-id="4bdb1-122">value</span></span>|<span data-ttu-id="4bdb1-123">string</span><span class="sxs-lookup"><span data-stu-id="4bdb1-123">string</span></span>|<span data-ttu-id="4bdb1-124">Valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="4bdb1-124">A property value.</span></span>|

## <a name="relationships"></a><span data-ttu-id="4bdb1-125">Relaciones</span><span class="sxs-lookup"><span data-stu-id="4bdb1-125">Relationships</span></span>
<span data-ttu-id="4bdb1-126">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4bdb1-126">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="4bdb1-127">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="4bdb1-127">JSON representation</span></span>

<span data-ttu-id="4bdb1-128">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="4bdb1-128">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.singleValueLegacyExtendedProperty"
}-->

```json
{
  "id": "string (identifier)",
  "value": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "singleValueLegacyExtendedProperty resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->