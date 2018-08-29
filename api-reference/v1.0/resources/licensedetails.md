# <a name="licensedetails-resource-type"></a><span data-ttu-id="96a7b-101">Tipo de recurso licenseDetails</span><span class="sxs-lookup"><span data-stu-id="96a7b-101">licenseDetails resource type</span></span>

<span data-ttu-id="96a7b-102">Contiene información sobre una licencia asignada a un usuario.</span><span class="sxs-lookup"><span data-stu-id="96a7b-102">Contains information about a license assigned to a user.</span></span>

## <a name="methods"></a><span data-ttu-id="96a7b-103">Métodos</span><span class="sxs-lookup"><span data-stu-id="96a7b-103">Methods</span></span>

| <span data-ttu-id="96a7b-104">Método</span><span class="sxs-lookup"><span data-stu-id="96a7b-104">Method</span></span>           | <span data-ttu-id="96a7b-105">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="96a7b-105">Return Type</span></span>    |<span data-ttu-id="96a7b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="96a7b-106">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="96a7b-107">Enumerar licenseDetails</span><span class="sxs-lookup"><span data-stu-id="96a7b-107">List licenseDetails</span></span>](../api/user_list_licensedetails.md) | <span data-ttu-id="96a7b-108">Colección licenseDetails</span><span class="sxs-lookup"><span data-stu-id="96a7b-108">licenseDetails collection</span></span> |<span data-ttu-id="96a7b-109">Recupere una lista de objetos licenseDetails para un usuario.</span><span class="sxs-lookup"><span data-stu-id="96a7b-109">Retrieve a list of licenseDetails objects for a user.</span></span>|

<!--|[Get licenseDetails](../api/licensedetails_get.md) | licenseDetails |Read properties and relationships of a licenseDetails object.|-->

## <a name="properties"></a><span data-ttu-id="96a7b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="96a7b-110">Properties</span></span>
| <span data-ttu-id="96a7b-111">Propiedad</span><span class="sxs-lookup"><span data-stu-id="96a7b-111">Property</span></span>     | <span data-ttu-id="96a7b-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="96a7b-112">Type</span></span>   |<span data-ttu-id="96a7b-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="96a7b-113">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="96a7b-114">id</span><span class="sxs-lookup"><span data-stu-id="96a7b-114">id</span></span>|<span data-ttu-id="96a7b-115">String</span><span class="sxs-lookup"><span data-stu-id="96a7b-115">String</span></span>| <span data-ttu-id="96a7b-p101">Identificador único del objeto licenseDetails. Solo lectura, no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="96a7b-p101">The unique identifier for the license detail object. Read-only, Key, Not nullable</span></span> |
|<span data-ttu-id="96a7b-118">servicePlans</span><span class="sxs-lookup"><span data-stu-id="96a7b-118">servicePlans</span></span>|<span data-ttu-id="96a7b-119">Colección [servicePlanInfo](serviceplaninfo.md)</span><span class="sxs-lookup"><span data-stu-id="96a7b-119">[servicePlanInfo](serviceplaninfo.md) collection</span></span>| <span data-ttu-id="96a7b-p102">Información sobre los planes de servicio asignados a la licencia. Solo lectura, no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="96a7b-p102">Information about the service plans assigned with the license. Read-only, Not nullable</span></span> |
|<span data-ttu-id="96a7b-122">skuId</span><span class="sxs-lookup"><span data-stu-id="96a7b-122">skuId</span></span>|<span data-ttu-id="96a7b-123">Guid</span><span class="sxs-lookup"><span data-stu-id="96a7b-123">Guid</span></span>| <span data-ttu-id="96a7b-p103">Identificador único (GUID) del SKU de servicio. Es igual a la propiedad skuId en el objeto [SubscribedSku](subscribedsku.md) relacionado. Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96a7b-p103">Unique identifier (GUID) for the service SKU. Equal to the skuId property on the related [SubscribedSku](subscribedsku.md) object. Read-only</span></span> |
|<span data-ttu-id="96a7b-127">skuPartNumber</span><span class="sxs-lookup"><span data-stu-id="96a7b-127">skuPartNumber</span></span>|<span data-ttu-id="96a7b-128">Cadena</span><span class="sxs-lookup"><span data-stu-id="96a7b-128">String</span></span>| <span data-ttu-id="96a7b-p104">Nombre para mostrar de SKU único. Es igual al skuPartNumber en el objeto [SubscribedSku](subscribedsku.md) relacionado; por ejemplo: "AAD_Premium". Solo lectura</span><span class="sxs-lookup"><span data-stu-id="96a7b-p104">Unique SKU display name. Equal to the skuPartNumber on the related [SubscribedSku](subscribedsku.md) object; for example: "AAD_Premium". Read-only</span></span> |

## <a name="relationships"></a><span data-ttu-id="96a7b-132">Relaciones</span><span class="sxs-lookup"><span data-stu-id="96a7b-132">Relationships</span></span>
<span data-ttu-id="96a7b-133">Ninguno</span><span class="sxs-lookup"><span data-stu-id="96a7b-133">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="96a7b-134">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="96a7b-134">JSON representation</span></span>
<span data-ttu-id="96a7b-135">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="96a7b-135">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.licenseDetails"
}-->

```json
{
  "id": "String (identifier)",
  "servicePlans": [{"@odata.type": "microsoft.graph.servicePlanInfo"}],
  "skuId": "Guid",
  "skuPartNumber": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "licenseDetails resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->