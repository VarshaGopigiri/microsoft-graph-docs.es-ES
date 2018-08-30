# <a name="inferenceclassification-resource-type"></a><span data-ttu-id="bf1f7-101">Tipo de recurso inferenceClassification</span><span class="sxs-lookup"><span data-stu-id="bf1f7-101">inferenceClassification resource type</span></span>

<span data-ttu-id="bf1f7-102">Clasificación de mensajes de un usuario que permite poner el foco en los que son más relevantes o importantes para el usuario.</span><span class="sxs-lookup"><span data-stu-id="bf1f7-102">Classification of a user's messages to enable focus on those that are more relevant or important to the user.</span></span> 

<span data-ttu-id="bf1f7-103">Para obtener más información, consulte [Administrar Bandeja de entrada Prioritarios](manage_focused_inbox.md).</span><span class="sxs-lookup"><span data-stu-id="bf1f7-103">For more information, see [Manage Focused Inbox](manage_focused_inbox.md).</span></span>


## <a name="methods"></a><span data-ttu-id="bf1f7-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="bf1f7-104">Methods</span></span>

| <span data-ttu-id="bf1f7-105">Método</span><span class="sxs-lookup"><span data-stu-id="bf1f7-105">Method</span></span>           | <span data-ttu-id="bf1f7-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bf1f7-106">Return Type</span></span>    |<span data-ttu-id="bf1f7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf1f7-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="bf1f7-108">Create inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="bf1f7-108">Create inferenceClassificationOverride</span></span>](../api/inferenceclassification_post_overrides.md) |[<span data-ttu-id="bf1f7-109">inferenceClassificationOverride</span><span class="sxs-lookup"><span data-stu-id="bf1f7-109">inferenceClassificationOverride</span></span>](inferenceclassificationoverride.md)| <span data-ttu-id="bf1f7-p101">Cree una invalidación para un remitente que se ha identificado mediante una dirección SMTP. Los mensajes futuros de esa dirección SMTP se clasificarán sistemáticamente como se especifica en la invalidación.</span><span class="sxs-lookup"><span data-stu-id="bf1f7-p101">Create an override for a sender identified by an SMTP address. Future messages from that SMTP address will be consistently classified as specified in the override.</span></span>|
|[<span data-ttu-id="bf1f7-112">List overrides</span><span class="sxs-lookup"><span data-stu-id="bf1f7-112">List overrides</span></span>](../api/inferenceclassification_list_overrides.md) |<span data-ttu-id="bf1f7-113">Colección [inferenceClassificationOverride](inferenceclassificationoverride.md)</span><span class="sxs-lookup"><span data-stu-id="bf1f7-113">[inferenceClassificationOverride](inferenceclassificationoverride.md) collection</span></span>| <span data-ttu-id="bf1f7-114">Obtiene los reemplazos que un usuario ha configurado para clasificar siempre los mensajes de determinados remitentes de forma específica.</span><span class="sxs-lookup"><span data-stu-id="bf1f7-114">Get the overrides that a user has set up to always classify messages from certain senders in specific ways.</span></span>|

## <a name="properties"></a><span data-ttu-id="bf1f7-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bf1f7-115">Properties</span></span>
| <span data-ttu-id="bf1f7-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bf1f7-116">Property</span></span>     | <span data-ttu-id="bf1f7-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf1f7-117">Type</span></span>   |<span data-ttu-id="bf1f7-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf1f7-118">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bf1f7-119">id</span><span class="sxs-lookup"><span data-stu-id="bf1f7-119">id</span></span>|<span data-ttu-id="bf1f7-120">cadena</span><span class="sxs-lookup"><span data-stu-id="bf1f7-120">string</span></span>| <span data-ttu-id="bf1f7-121">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="bf1f7-121">Read-only.</span></span>|

## <a name="relationships"></a><span data-ttu-id="bf1f7-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="bf1f7-122">Relationships</span></span>
| <span data-ttu-id="bf1f7-123">Relación</span><span class="sxs-lookup"><span data-stu-id="bf1f7-123">Relationship</span></span> | <span data-ttu-id="bf1f7-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="bf1f7-124">Type</span></span>   |<span data-ttu-id="bf1f7-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf1f7-125">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="bf1f7-126">overrides</span><span class="sxs-lookup"><span data-stu-id="bf1f7-126">overrides</span></span>|<span data-ttu-id="bf1f7-127">Colección [inferenceClassificationOverride](inferenceclassificationoverride.md)</span><span class="sxs-lookup"><span data-stu-id="bf1f7-127">[inferenceClassificationOverride](inferenceclassificationoverride.md) collection</span></span>| <span data-ttu-id="bf1f7-p102">Conjunto de valores de reemplazo de un usuario para clasificar siempre los mensajes de remitentes concretos de determinada manera: `focused`, o `other`. Solo lectura. Admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="bf1f7-p102">A set of overrides for a user to always classify messages from specific senders in certain ways: `focused`, or `other`. Read-only. Nullable.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="bf1f7-131">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="bf1f7-131">JSON representation</span></span>

<span data-ttu-id="bf1f7-132">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="bf1f7-132">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.inferenceClassification",
  "@odata.annotations": [
    {
      "property": "overrides",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "searchable": false
      }
    }
  ]
}-->

```json
{
  "id": "string (identifier)"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "inferenceClassification resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->