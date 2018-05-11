# <a name="customtimezone-resource-type"></a><span data-ttu-id="1f511-101">Tipo de recurso customTimeZone</span><span class="sxs-lookup"><span data-stu-id="1f511-101">customTimeZone resource type</span></span>

<span data-ttu-id="1f511-102">Representa una zona horaria en la que la transición del horario de verano a la hora estándar, o viceversa, no es estándar.</span><span class="sxs-lookup"><span data-stu-id="1f511-102">Represents a time zone where the transition from standard to daylight saving time, or vice versa is not standard.</span></span>


## <a name="properties"></a><span data-ttu-id="1f511-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1f511-103">Properties</span></span>
| <span data-ttu-id="1f511-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="1f511-104">Property</span></span>     | <span data-ttu-id="1f511-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="1f511-105">Type</span></span>   |<span data-ttu-id="1f511-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="1f511-106">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="1f511-107">bias</span><span class="sxs-lookup"><span data-stu-id="1f511-107">Bias</span></span> | <span data-ttu-id="1f511-108">Edm.Int32</span><span class="sxs-lookup"><span data-stu-id="1f511-108">Edm.Int32</span></span> | <span data-ttu-id="1f511-109">Diferencia horaria de la zona horaria con respecto a la hora universal coordinada (UTC).</span><span class="sxs-lookup"><span data-stu-id="1f511-109">The time offset of the time zone from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1f511-110">Este valor está en minutos.</span><span class="sxs-lookup"><span data-stu-id="1f511-110">This value is in points.</span></span> <span data-ttu-id="1f511-111">Las zonas horarias que son anteriores a UTC tienen una diferencia positiva; las zonas horarias que son posteriores a UTC tienen una diferencia negativa.</span><span class="sxs-lookup"><span data-stu-id="1f511-111">Time zones that are ahead of UTC have a positive offset; time zones that are behind UTC have a negative offset.</span></span>|
| <span data-ttu-id="1f511-112">daylightOffset</span><span class="sxs-lookup"><span data-stu-id="1f511-112">daylightOffset</span></span> | [<span data-ttu-id="1f511-113">daylightTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="1f511-113">daylightTimeZoneOffset</span></span>](daylighttimezoneoffset.md) | <span data-ttu-id="1f511-114">Especifica cuándo la zona horaria cambia de la hora estándar al horario de verano.</span><span class="sxs-lookup"><span data-stu-id="1f511-114">Specifies when the time zone switches from standard time to daylight saving time.</span></span> |
| <span data-ttu-id="1f511-115">name</span><span class="sxs-lookup"><span data-stu-id="1f511-115">name</span></span> | <span data-ttu-id="1f511-116">string</span><span class="sxs-lookup"><span data-stu-id="1f511-116">string</span></span> | <span data-ttu-id="1f511-117">Nombre de la zona horaria personalizada.</span><span class="sxs-lookup"><span data-stu-id="1f511-117">The name of the custom time zone.</span></span> |
| <span data-ttu-id="1f511-118">standardOffset</span><span class="sxs-lookup"><span data-stu-id="1f511-118">standardOffset</span></span> | [<span data-ttu-id="1f511-119">standardTimeZoneOffset</span><span class="sxs-lookup"><span data-stu-id="1f511-119">standardTimeZoneOffset</span></span>](standardtimezoneoffset.md) | <span data-ttu-id="1f511-120">Especifica cuándo la zona horaria cambia del horario de verano a la hora estándar.</span><span class="sxs-lookup"><span data-stu-id="1f511-120">Specifies when the time zone switches from daylight saving time to standard time.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="1f511-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="1f511-121">JSON representation</span></span>

<span data-ttu-id="1f511-122">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="1f511-122">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.customTimeZone"
}-->

```json
{
  "bias": "Int32",
  "daylightOffset": {"@odata.type": "microsoft.graph.daylightTimeZoneOffset"},
  "name": "string",
  "standardOffset": {"@odata.type": "microsoft.graph.standardTimeZoneOffset"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "customTimeZone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->