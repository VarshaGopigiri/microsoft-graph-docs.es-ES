# <a name="assignedplan-resource-type"></a><span data-ttu-id="9805a-101">Tipo de recurso assignedPlan</span><span class="sxs-lookup"><span data-stu-id="9805a-101">assignedPlan resource type</span></span>

<span data-ttu-id="9805a-102">La propiedad **assignedPlans** de la entidad [user](user.md) y la entidad [organization](organization.md) es una colección de **provisionedPlan**.</span><span class="sxs-lookup"><span data-stu-id="9805a-102">The **assignedPlans** property of both the [user](user.md) entity and the [organization](organization.md) entity is a collection of **assignedPlan**.</span></span>


## <a name="properties"></a><span data-ttu-id="9805a-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9805a-103">Properties</span></span>
| <span data-ttu-id="9805a-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9805a-104">Property</span></span>     | <span data-ttu-id="9805a-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="9805a-105">Type</span></span>   |<span data-ttu-id="9805a-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="9805a-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9805a-107">assignedDateTime</span><span class="sxs-lookup"><span data-stu-id="9805a-107">assignedDateTime</span></span>|<span data-ttu-id="9805a-108">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9805a-108">DateTimeOffset</span></span>|<span data-ttu-id="9805a-p101">Fecha y hora en que se asignó el plan; por ejemplo: 2013-01-02T19:32:30Z. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="9805a-p101">The date and time at which the plan was assigned; for example: 2013-01-02T19:32:30Z. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="9805a-112">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="9805a-112">capabilityStatus</span></span>|<span data-ttu-id="9805a-113">String</span><span class="sxs-lookup"><span data-stu-id="9805a-113">String</span></span>|<span data-ttu-id="9805a-114">Por ejemplo, "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="9805a-114">For example, “Enabled”.</span></span>|
|<span data-ttu-id="9805a-115">service</span><span class="sxs-lookup"><span data-stu-id="9805a-115">service</span></span>|<span data-ttu-id="9805a-116">String</span><span class="sxs-lookup"><span data-stu-id="9805a-116">String</span></span>|<span data-ttu-id="9805a-117">Nombre del servicio; por ejemplo, "Exchange".</span><span class="sxs-lookup"><span data-stu-id="9805a-117">The name of the service; for example, “Exchange”.</span></span>|
|<span data-ttu-id="9805a-118">servicePlanId</span><span class="sxs-lookup"><span data-stu-id="9805a-118">servicePlanId</span></span>|<span data-ttu-id="9805a-119">Guid</span><span class="sxs-lookup"><span data-stu-id="9805a-119">Guid</span></span>|<span data-ttu-id="9805a-120">GUID que identifica el plan de servicio.</span><span class="sxs-lookup"><span data-stu-id="9805a-120">A GUID that identifies the service plan.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9805a-121">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9805a-121">JSON representation</span></span>

<span data-ttu-id="9805a-122">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9805a-122">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.assignedPlan"
}-->

```json
{
  "assignedDateTime": "String (timestamp)",
  "capabilityStatus": "string",
  "service": "string",
  "servicePlanId": "guid"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "assignedPlan resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
