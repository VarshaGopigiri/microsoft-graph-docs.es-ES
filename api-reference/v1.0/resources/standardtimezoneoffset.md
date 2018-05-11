# <a name="standardtimezoneoffset-resource-type"></a><span data-ttu-id="33344-101">Tipo de recurso standardTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="33344-101">standardTimeZoneOffset resource type</span></span>

<span data-ttu-id="33344-102">Especifica cuándo una zona horaria cambia del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="33344-102">Specifies when a time zone switches from daylight saving time to standard time.</span></span>

<span data-ttu-id="33344-103">Por ejemplo, si se especifica una zona horaria con las propiedades siguientes:</span><span class="sxs-lookup"><span data-stu-id="33344-103">For example, if a time zone is specified with the following properties:</span></span>

- <span data-ttu-id="33344-104">**dayOccurrence** es 3.</span><span class="sxs-lookup"><span data-stu-id="33344-104">**dayOccurrence** is 3</span></span>
- <span data-ttu-id="33344-105">**dayOfWeek** es "Domingo".</span><span class="sxs-lookup"><span data-stu-id="33344-105">**dayOfWeek** is "Sunday"</span></span>
- <span data-ttu-id="33344-106">**month** es 10.</span><span class="sxs-lookup"><span data-stu-id="33344-106">**month** is 10</span></span>
- <span data-ttu-id="33344-107">**time** es 02:00:00 y **year** es 0. Eso significa que la transición del horario de verano al estándar se produce todos los años a las 2:00 del tercer domingo de octubre.</span><span class="sxs-lookup"><span data-stu-id="33344-107">**time** is 02:00:00 _ **year** is 0 That means the transition from daylight saving time to standard occurs at 2 AM on the third Sunday of October, every year.</span></span>

## <a name="properties"></a><span data-ttu-id="33344-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33344-108">Properties</span></span>
| <span data-ttu-id="33344-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="33344-109">Property</span></span>     | <span data-ttu-id="33344-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="33344-110">Type</span></span>   |<span data-ttu-id="33344-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="33344-111">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="33344-112">dayOccurrence</span><span class="sxs-lookup"><span data-stu-id="33344-112">dayOccurrence</span></span> | <span data-ttu-id="33344-113">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="33344-113">Edm.Int32</span></span> | <span data-ttu-id="33344-114">Representa la enésima repetición del día de la semana en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="33344-114">Represents the nth occurrence of the day of week that the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="33344-115">dayOfWeek</span><span class="sxs-lookup"><span data-stu-id="33344-115">DAYOFWEEK</span></span> | <span data-ttu-id="33344-116">string</span><span class="sxs-lookup"><span data-stu-id="33344-116">string</span></span> | <span data-ttu-id="33344-117">Representa el día de la semana en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="33344-117">Represents the day of the week when the transition from daylight saving time to standard time.</span></span> |
| <span data-ttu-id="33344-118">month</span><span class="sxs-lookup"><span data-stu-id="33344-118">month</span></span> | <span data-ttu-id="33344-119">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="33344-119">Edm.Int32</span></span> | <span data-ttu-id="33344-120">Representa el mes del año en el que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="33344-120">Represents the month of the year when the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="33344-121">time</span><span class="sxs-lookup"><span data-stu-id="33344-121">time</span></span> | <span data-ttu-id="33344-122">Edm.TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="33344-122">Edm.TimeOfDay</span></span> | <span data-ttu-id="33344-123">Representa la hora del día en la que se produce la transición del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="33344-123">Represents the time of day when the transition from daylight saving time to standard time occurs.</span></span> |
| <span data-ttu-id="33344-124">year</span><span class="sxs-lookup"><span data-stu-id="33344-124">year</span></span> | <span data-ttu-id="33344-125">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="33344-125">Edm.Int32</span></span> | <span data-ttu-id="33344-126">Representa la frecuencia en términos de años con que se produce el cambio del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="33344-126">Represents how frequently in terms of years the change from daylight saving time to standard time occurs.</span></span> <span data-ttu-id="33344-127">Por ejemplo, un valor 0 significa todos los años.</span><span class="sxs-lookup"><span data-stu-id="33344-127">For example, a value of 0 means every year.</span></span>|


## <a name="json-representation"></a><span data-ttu-id="33344-128">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="33344-128">JSON representation</span></span>

<span data-ttu-id="33344-129">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="33344-129">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.standardTimeZoneOffset"
}-->

```json
{
  "dayOccurrence": "Int32",
  "dayOfWeek": "string",
  "month": "Int32",
  "time": "TimeOfDay",
  "year": "Int32"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "standardTimeZoneOffset resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->