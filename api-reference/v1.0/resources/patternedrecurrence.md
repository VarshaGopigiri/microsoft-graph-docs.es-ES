# <a name="patternedrecurrence-resource-type"></a><span data-ttu-id="90b69-101">Tipo de recurso patternedRecurrence</span><span class="sxs-lookup"><span data-stu-id="90b69-101">patternedRecurrence resource type</span></span>

<span data-ttu-id="90b69-102">Patrón e intervalo de periodicidad.</span><span class="sxs-lookup"><span data-stu-id="90b69-102">The recurrence pattern and range.</span></span>

## <a name="properties"></a><span data-ttu-id="90b69-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="90b69-103">Properties</span></span>
| <span data-ttu-id="90b69-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="90b69-104">Property</span></span>     | <span data-ttu-id="90b69-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="90b69-105">Type</span></span>   |<span data-ttu-id="90b69-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="90b69-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="90b69-107">pattern</span><span class="sxs-lookup"><span data-stu-id="90b69-107">pattern</span></span>|[<span data-ttu-id="90b69-108">RecurrencePattern</span><span class="sxs-lookup"><span data-stu-id="90b69-108">RecurrencePattern</span></span>](recurrencepattern.md)|<span data-ttu-id="90b69-109">Frecuencia de un evento.</span><span class="sxs-lookup"><span data-stu-id="90b69-109">The frequency of an event.</span></span>|
|<span data-ttu-id="90b69-110">range</span><span class="sxs-lookup"><span data-stu-id="90b69-110">range</span></span>|[<span data-ttu-id="90b69-111">RecurrenceRange</span><span class="sxs-lookup"><span data-stu-id="90b69-111">RecurrenceRange</span></span>](recurrencerange.md)|<span data-ttu-id="90b69-112">Duración de un evento.</span><span class="sxs-lookup"><span data-stu-id="90b69-112">The duration of an event.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="90b69-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="90b69-113">JSON representation</span></span>

<span data-ttu-id="90b69-114">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="90b69-114">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.patternedRecurrence"
}-->

```json
{
  "pattern": {"@odata.type": "microsoft.graph.recurrencePattern"},
  "range": {"@odata.type": "microsoft.graph.recurrenceRange"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "patternedRecurrence resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
