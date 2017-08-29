# <a name="recurrencerange-resource-type"></a><span data-ttu-id="15ff9-101">Tipo de recurso recurrenceRange</span><span class="sxs-lookup"><span data-stu-id="15ff9-101">recurrenceRange resource type</span></span>

<span data-ttu-id="15ff9-102">Duración de un evento.</span><span class="sxs-lookup"><span data-stu-id="15ff9-102">The duration of an event.</span></span>

## <a name="properties"></a><span data-ttu-id="15ff9-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="15ff9-103">Properties</span></span>

| <span data-ttu-id="15ff9-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="15ff9-104">Property</span></span>     | <span data-ttu-id="15ff9-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="15ff9-105">Type</span></span>   |<span data-ttu-id="15ff9-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="15ff9-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="15ff9-107">endDate</span><span class="sxs-lookup"><span data-stu-id="15ff9-107">endDate</span></span>|<span data-ttu-id="15ff9-108">Date</span><span class="sxs-lookup"><span data-stu-id="15ff9-108">Date</span></span>|<span data-ttu-id="15ff9-109">Fecha de finalización de la serie.</span><span class="sxs-lookup"><span data-stu-id="15ff9-109">The end date of the series.</span></span>|
|<span data-ttu-id="15ff9-110">numberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="15ff9-110">numberOfOccurrences</span></span>|<span data-ttu-id="15ff9-111">Int32</span><span class="sxs-lookup"><span data-stu-id="15ff9-111">Int32</span></span>|<span data-ttu-id="15ff9-112">Número de veces que se repite el evento.</span><span class="sxs-lookup"><span data-stu-id="15ff9-112">How many times to repeat the event.</span></span>|
|<span data-ttu-id="15ff9-113">recurrenceTimeZone</span><span class="sxs-lookup"><span data-stu-id="15ff9-113">recurrenceTimeZone</span></span>|<span data-ttu-id="15ff9-114">String</span><span class="sxs-lookup"><span data-stu-id="15ff9-114">String</span></span> |<span data-ttu-id="15ff9-115">Zona horaria de las propiedades **startDate** y **endDate**.</span><span class="sxs-lookup"><span data-stu-id="15ff9-115">Time zone for the **startDate** and **endDate** properties.</span></span> |
|<span data-ttu-id="15ff9-116">startDate</span><span class="sxs-lookup"><span data-stu-id="15ff9-116">startDate</span></span>|<span data-ttu-id="15ff9-117">Date</span><span class="sxs-lookup"><span data-stu-id="15ff9-117">Date</span></span>|<span data-ttu-id="15ff9-118">Fecha de inicio de la tarea.</span><span class="sxs-lookup"><span data-stu-id="15ff9-118">The start date of the series.</span></span>|
|<span data-ttu-id="15ff9-119">type</span><span class="sxs-lookup"><span data-stu-id="15ff9-119">type</span></span>|<span data-ttu-id="15ff9-120">String</span><span class="sxs-lookup"><span data-stu-id="15ff9-120">String</span></span>|<span data-ttu-id="15ff9-p101">Intervalo de periodicidad: EndDate = 0, NoEnd = 1, Numbered = 2. Valores posibles: `EndDate`, `NoEnd`, `Numbered`.</span><span class="sxs-lookup"><span data-stu-id="15ff9-p101">The recurrence range: EndDate = 0, NoEnd = 1, Numbered = 2. Possible values are: `EndDate`, `NoEnd`, `Numbered`.</span></span>||

## <a name="json-representation"></a><span data-ttu-id="15ff9-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="15ff9-123">JSON representation</span></span>

<span data-ttu-id="15ff9-124">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="15ff9-124">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recurrencerange"
}-->

```json
{
  "endDate": "String (timestamp)",
  "numberOfOccurrences": 1024,
  "recurrenceTimeZone": "string",
  "startDate": "String (timestamp)",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "recurrenceRange resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
