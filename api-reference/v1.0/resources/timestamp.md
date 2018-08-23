# <a name="timestamp-resource-type"></a><span data-ttu-id="17da8-101">tipo de recurso timeStamp</span><span class="sxs-lookup"><span data-stu-id="17da8-101">timeStamp resource type</span></span>

<span data-ttu-id="17da8-102">Información sobre la fecha y la hora de un momento dado.</span><span class="sxs-lookup"><span data-stu-id="17da8-102">Date and time information for a point in time.</span></span>

## <a name="json-representation"></a><span data-ttu-id="17da8-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="17da8-103">JSON representation</span></span>

<span data-ttu-id="17da8-104">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="17da8-104">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeStamp"
}-->

```json
{
  "date": "String (timestamp)",
  "time": "String (timestamp)",
  "timeZone": "string"
}

```
## <a name="properties"></a><span data-ttu-id="17da8-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="17da8-105">Properties</span></span>
| <span data-ttu-id="17da8-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="17da8-106">Property</span></span>       | <span data-ttu-id="17da8-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="17da8-107">Type</span></span>    |<span data-ttu-id="17da8-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="17da8-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="17da8-109">date</span><span class="sxs-lookup"><span data-stu-id="17da8-109">date</span></span>|<span data-ttu-id="17da8-110">Date</span><span class="sxs-lookup"><span data-stu-id="17da8-110">Date</span></span>|<span data-ttu-id="17da8-111">La fecha de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="17da8-111">The date portion of the timestamp.</span></span>|
|<span data-ttu-id="17da8-112">time</span><span class="sxs-lookup"><span data-stu-id="17da8-112">time</span></span>|<span data-ttu-id="17da8-113">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="17da8-113">TimeOfDay</span></span>|<span data-ttu-id="17da8-114">La hora de la marca de tiempo.</span><span class="sxs-lookup"><span data-stu-id="17da8-114">The time portion of the timestamp.</span></span>|
|<span data-ttu-id="17da8-115">timeZone</span><span class="sxs-lookup"><span data-stu-id="17da8-115">timeZone</span></span>|<span data-ttu-id="17da8-116">Cadena</span><span class="sxs-lookup"><span data-stu-id="17da8-116">String</span></span>|<span data-ttu-id="17da8-117">La zona horaria de la marca de tiempo, que se corresponde con una de las 24 áreas longitudinales del mundo.</span><span class="sxs-lookup"><span data-stu-id="17da8-117">The timezone portion of the timestamp, which is one of the 24 longitudinal areas in the world.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeStamp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->