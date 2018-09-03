# <a name="followupflag-resource-type"></a><span data-ttu-id="e9b7e-101">Tipo de recurso followupFlag</span><span class="sxs-lookup"><span data-stu-id="e9b7e-101">followupFlag resource type</span></span>


<span data-ttu-id="e9b7e-102">Permite establecer una marca para que el usuario realice más adelante el seguimiento en un elemento.</span><span class="sxs-lookup"><span data-stu-id="e9b7e-102">Allows setting a flag for the user to follow up on an item later.</span></span> <span data-ttu-id="e9b7e-103">Los elementos admitidos incluyen [message](message.md) y [contact](contact.md).</span><span class="sxs-lookup"><span data-stu-id="e9b7e-103">Supported items include [message](message.md) and [contact](contact.md).</span></span>

## <a name="properties"></a><span data-ttu-id="e9b7e-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e9b7e-104">Properties</span></span>
| <span data-ttu-id="e9b7e-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e9b7e-105">Property</span></span>     | <span data-ttu-id="e9b7e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9b7e-106">Type</span></span>   |<span data-ttu-id="e9b7e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9b7e-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e9b7e-108">completedDateTime</span><span class="sxs-lookup"><span data-stu-id="e9b7e-108">completedDateTime</span></span>|[<span data-ttu-id="e9b7e-109">dateTimeTimeZone</span><span class="sxs-lookup"><span data-stu-id="e9b7e-109">dateTimeTimeZone</span></span>](dateTimeTimeZone.md)|<span data-ttu-id="e9b7e-110">Fecha y hora en que se finalizó el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="e9b7e-110">The date and time that the follow-up was finished.</span></span>|
|<span data-ttu-id="e9b7e-111">dueDateTime</span><span class="sxs-lookup"><span data-stu-id="e9b7e-111">dueDateTime</span></span>|<span data-ttu-id="e9b7e-112">**dateTimeTimeZone**</span><span class="sxs-lookup"><span data-stu-id="e9b7e-112">**dateTimeTimeZone**</span></span>|<span data-ttu-id="e9b7e-113">Fecha y hora en que se va a finalizar el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="e9b7e-113">The date and time that the follow-up is to be finished.</span></span>|
|<span data-ttu-id="e9b7e-114">flagStatus</span><span class="sxs-lookup"><span data-stu-id="e9b7e-114">flagStatus</span></span>|<span data-ttu-id="e9b7e-115">followupFlagStatus</span><span class="sxs-lookup"><span data-stu-id="e9b7e-115">FollowupFlagStatus</span></span>|<span data-ttu-id="e9b7e-116">Estado del seguimiento de un elemento.</span><span class="sxs-lookup"><span data-stu-id="e9b7e-116">The status for follow-up for an item.</span></span> <span data-ttu-id="e9b7e-117">Los valores posibles son: `notFlagged`, `complete` y `flagged`.</span><span class="sxs-lookup"><span data-stu-id="e9b7e-117">Possible values are `notFlagged`, `complete`, and `flagged`.</span></span>|
|<span data-ttu-id="e9b7e-118">startDateTime</span><span class="sxs-lookup"><span data-stu-id="e9b7e-118">startDateTime</span></span>|<span data-ttu-id="e9b7e-119">**dateTimeTimeZone**</span><span class="sxs-lookup"><span data-stu-id="e9b7e-119">**dateTimeTimeZone**</span></span>|<span data-ttu-id="e9b7e-120">Fecha y hora en que va a iniciarse el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="e9b7e-120">The date and time that the follow-up is to begin.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="e9b7e-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="e9b7e-121">JSON representation</span></span>

<span data-ttu-id="e9b7e-122">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="e9b7e-122">Here is a JSON representation of the resource</span></span>

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
