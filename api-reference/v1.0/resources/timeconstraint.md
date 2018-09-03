# <a name="timeconstraint-resource-type"></a><span data-ttu-id="67883-101">Tipo de recurso timeConstraint</span><span class="sxs-lookup"><span data-stu-id="67883-101">timeConstraint resource type</span></span>

<span data-ttu-id="67883-102">Restringe las sugerencias de hora de reunión a ciertas horas y días de la semana según la naturaleza de la actividad especificada y las franjas horarias disponibles.</span><span class="sxs-lookup"><span data-stu-id="67883-102">Restricts meeting time suggestions to certain hours and days of the week according to the specified nature of activity and open time slots.</span></span>

## <a name="json-representation"></a><span data-ttu-id="67883-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="67883-103">JSON representation</span></span>

<span data-ttu-id="67883-104">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="67883-104">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeConstraint"
}-->

```json
{
  "activityDomain": "String",
  "timeslots": [{"@odata.type": "microsoft.graph.timeSlot"}]
}

```
## <a name="properties"></a><span data-ttu-id="67883-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="67883-105">Properties</span></span>
| <span data-ttu-id="67883-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="67883-106">Property</span></span>     | <span data-ttu-id="67883-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="67883-107">Type</span></span>   |<span data-ttu-id="67883-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="67883-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="67883-109">activityDomain</span><span class="sxs-lookup"><span data-stu-id="67883-109">activityDomain</span></span>|<span data-ttu-id="67883-110">activityDomain</span><span class="sxs-lookup"><span data-stu-id="67883-110">activityDomain</span></span>|<span data-ttu-id="67883-111">La naturaleza de la actividad, de forma opcional.</span><span class="sxs-lookup"><span data-stu-id="67883-111">The nature of the activity, optional. Possible values are: , , , or .</span></span> <span data-ttu-id="67883-112">Los valores posibles son: `work`, `personal`, `unrestricted` o `unknown`.</span><span class="sxs-lookup"><span data-stu-id="67883-112">The possible values are  `work`,  `personal`,  `unrestricted`, or  `unknown`.</span></span>|
|<span data-ttu-id="67883-113">timeslots</span><span class="sxs-lookup"><span data-stu-id="67883-113">timeslots</span></span>|<span data-ttu-id="67883-114">colección [timeSlot](timeslot.md)</span><span class="sxs-lookup"><span data-stu-id="67883-114">[timeSlot](timeslot.md) collection</span></span>|<span data-ttu-id="67883-115">Una matriz de periodos de tiempo.</span><span class="sxs-lookup"><span data-stu-id="67883-115">An array of time periods.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "timeConstraint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
