# <a name="provisionedplan-resource-type"></a><span data-ttu-id="f7e2b-101">Tipo de recurso provisionedPlan</span><span class="sxs-lookup"><span data-stu-id="f7e2b-101">provisionedPlan resource type</span></span>

<span data-ttu-id="f7e2b-102">La propiedad **provisionedPlans** de la entidad [user](user.md) y la entidad [organization](organization.md) es una colección de **provisionedPlan**.</span><span class="sxs-lookup"><span data-stu-id="f7e2b-102">The **provisionedPlans** property of the [user](user.md) entity and the [organization](organization.md) entity is a collection of **provisionedPlan**.</span></span>


## <a name="properties"></a><span data-ttu-id="f7e2b-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f7e2b-103">Properties</span></span>
| <span data-ttu-id="f7e2b-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="f7e2b-104">Property</span></span>     | <span data-ttu-id="f7e2b-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="f7e2b-105">Type</span></span>   |<span data-ttu-id="f7e2b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="f7e2b-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="f7e2b-107">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="f7e2b-107">capabilityStatus</span></span>|<span data-ttu-id="f7e2b-108">String</span><span class="sxs-lookup"><span data-stu-id="f7e2b-108">String</span></span>|<span data-ttu-id="f7e2b-109">Por ejemplo, "Habilitado".</span><span class="sxs-lookup"><span data-stu-id="f7e2b-109">For example, “Enabled”.</span></span>|
|<span data-ttu-id="f7e2b-110">provisioningStatus</span><span class="sxs-lookup"><span data-stu-id="f7e2b-110">provisioningStatus</span></span>|<span data-ttu-id="f7e2b-111">String</span><span class="sxs-lookup"><span data-stu-id="f7e2b-111">String</span></span>|<span data-ttu-id="f7e2b-112">Por ejemplo, "Correcto".</span><span class="sxs-lookup"><span data-stu-id="f7e2b-112">For example, “Success”.</span></span>|
|<span data-ttu-id="f7e2b-113">service</span><span class="sxs-lookup"><span data-stu-id="f7e2b-113">service</span></span>|<span data-ttu-id="f7e2b-114">String</span><span class="sxs-lookup"><span data-stu-id="f7e2b-114">String</span></span>|<span data-ttu-id="f7e2b-115">Nombre del servicio; por ejemplo, "AccessControlS2S".</span><span class="sxs-lookup"><span data-stu-id="f7e2b-115">The name of the service; for example, “AccessControlS2S”</span></span>|

## <a name="json-representation"></a><span data-ttu-id="f7e2b-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="f7e2b-116">JSON representation</span></span>

<span data-ttu-id="f7e2b-117">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="f7e2b-117">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.provisionedPlan"
}-->

```json
{
  "capabilityStatus": "string",
  "provisioningStatus": "string",
  "service": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "provisionedPlan resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->