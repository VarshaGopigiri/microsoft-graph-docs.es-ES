# <a name="followupflag-resource-type"></a><span data-ttu-id="d91db-101">Tipo de recurso followupFlag</span><span class="sxs-lookup"><span data-stu-id="d91db-101">followupFlag resource type</span></span>


<span data-ttu-id="d91db-102">Permite establecer un indicador en un elemento para el usuario realizar el seguimiento más adelante.</span><span class="sxs-lookup"><span data-stu-id="d91db-102">Allows setting a flag in an item for the user to follow up on later.</span></span> 

## <a name="properties"></a><span data-ttu-id="d91db-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d91db-103">Properties</span></span>
| <span data-ttu-id="d91db-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d91db-104">Property</span></span>     | <span data-ttu-id="d91db-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="d91db-105">Type</span></span>   |<span data-ttu-id="d91db-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d91db-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d91db-107">completedDateTime</span><span class="sxs-lookup"><span data-stu-id="d91db-107">completedDateTime</span></span>|[<span data-ttu-id="d91db-108">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="d91db-108">dateTimeTimeZone</span></span>](dateTimeTimeZone.md)|<span data-ttu-id="d91db-109">Fecha y hora en que se finalizó el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="d91db-109">The date and time that the follow-up was finished.</span></span>|
|<span data-ttu-id="d91db-110">dueDateTime</span><span class="sxs-lookup"><span data-stu-id="d91db-110">dueDateTime</span></span>|<span data-ttu-id="d91db-111">**dateTimeTimeZone**</span><span class="sxs-lookup"><span data-stu-id="d91db-111">**dateTimeTimeZone**</span></span>|<span data-ttu-id="d91db-112">Fecha y hora en que se va a finalizar el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="d91db-112">The date and time that the follow-up is to be finished.</span></span>|
|<span data-ttu-id="d91db-113">flagStatus</span><span class="sxs-lookup"><span data-stu-id="d91db-113">flagStatus</span></span>|<span data-ttu-id="d91db-114">followupFlagStatus</span><span class="sxs-lookup"><span data-stu-id="d91db-114">followupFlagStatus</span></span>|<span data-ttu-id="d91db-115">Estado del seguimiento de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d91db-115">The status for follow-up for an item.</span></span> <span data-ttu-id="d91db-116">Los valores posibles son: `notFlagged`, `complete` y `flagged`.</span><span class="sxs-lookup"><span data-stu-id="d91db-116">Possible values are `notFlagged`, `complete`, and `flagged`.</span></span>|
|<span data-ttu-id="d91db-117">startDateTime</span><span class="sxs-lookup"><span data-stu-id="d91db-117">startDateTime</span></span>|<span data-ttu-id="d91db-118">**dateTimeTimeZone**</span><span class="sxs-lookup"><span data-stu-id="d91db-118">**dateTimeTimeZone**</span></span>|<span data-ttu-id="d91db-119">Fecha y hora en que va a iniciarse el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="d91db-119">The date and time that the follow-up is to begin.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d91db-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d91db-120">JSON representation</span></span>

<span data-ttu-id="d91db-121">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d91db-121">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.followupFlag"
}-->

```json
{
  "completedDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "dueDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"},
  "flagStatus": "String",
  "startDateTime": {"@odata.type": "microsoft.graph.dateTimeTimeZone"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "followupFlag resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
