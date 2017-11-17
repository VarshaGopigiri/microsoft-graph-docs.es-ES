# <a name="assignedlicense-resource-type"></a><span data-ttu-id="5d306-101">Tipo de recurso assignedLicense</span><span class="sxs-lookup"><span data-stu-id="5d306-101">assignedLicense resource type</span></span>

<span data-ttu-id="5d306-p101">Representa una licencia asignada a un usuario. La propiedad **assignedLicenses** de la entidad [user](user.md) es una colección de **assignedLicense**.</span><span class="sxs-lookup"><span data-stu-id="5d306-p101">Represents a license assigned to a user. The **assignedLicenses** property of the [user](user.md) entity is a collection of **assignedLicense**.</span></span>

## <a name="properties"></a><span data-ttu-id="5d306-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5d306-104">Properties</span></span>
| <span data-ttu-id="5d306-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5d306-105">Property</span></span>     | <span data-ttu-id="5d306-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="5d306-106">Type</span></span>   |<span data-ttu-id="5d306-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5d306-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="5d306-108">disabledPlans</span><span class="sxs-lookup"><span data-stu-id="5d306-108">disabledPlans</span></span>|<span data-ttu-id="5d306-109">Colección Guid</span><span class="sxs-lookup"><span data-stu-id="5d306-109">Guid collection</span></span>|<span data-ttu-id="5d306-110">Colección de los identificadores únicos para los planes que se han deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="5d306-110">A collection of the unique identifiers for plans that have been disabled.</span></span>|
|<span data-ttu-id="5d306-111">skuId</span><span class="sxs-lookup"><span data-stu-id="5d306-111">skuId</span></span>|<span data-ttu-id="5d306-112">Guid</span><span class="sxs-lookup"><span data-stu-id="5d306-112">Guid</span></span>|<span data-ttu-id="5d306-113">Identificador único de la SKU.</span><span class="sxs-lookup"><span data-stu-id="5d306-113">The unique identifier for the SKU.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="5d306-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="5d306-114">JSON representation</span></span>

<span data-ttu-id="5d306-115">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="5d306-115">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.assignedLicense"
}-->

```json
{
  "disabledPlans": ["guid"],
  "skuId": "guid"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "assignedLicense resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
