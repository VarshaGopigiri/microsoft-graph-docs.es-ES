# <a name="subscribedsku-resource-type"></a><span data-ttu-id="79ede-101">Tipo de recurso subscribedSku</span><span class="sxs-lookup"><span data-stu-id="79ede-101">subscribedSku resource type</span></span>

<span data-ttu-id="79ede-102">Contiene información acerca de una SKU de servicio a la que la empresa está suscrita.</span><span class="sxs-lookup"><span data-stu-id="79ede-102">Contains information about a service SKU that a company is subscribed to.</span></span>

<span data-ttu-id="79ede-p101">Solo se admite la operación de lectura con las SKU suscritas; no se admiten las operaciones de creación, actualización y eliminación. No se admiten expresiones de filtro de consulta. Se hereda de [DirectoryObject](directoryobject.md).</span><span class="sxs-lookup"><span data-stu-id="79ede-p101">Only the read operation is supported on subscribed SKUs; create, update, and delete are not supported. Query filter expressions are not supported. Inherits from [directoryObject](directoryobject.md).</span></span>

## <a name="methods"></a><span data-ttu-id="79ede-106">Métodos</span><span class="sxs-lookup"><span data-stu-id="79ede-106">Methods</span></span>
| <span data-ttu-id="79ede-107">Método</span><span class="sxs-lookup"><span data-stu-id="79ede-107">Method</span></span>           | <span data-ttu-id="79ede-108">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="79ede-108">Return Type</span></span>    |<span data-ttu-id="79ede-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="79ede-109">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="79ede-110">Obtener subscribedSku</span><span class="sxs-lookup"><span data-stu-id="79ede-110">Get subscribedSku</span></span>](../api/subscribedsku_get.md) | [<span data-ttu-id="79ede-111">subscribedSku</span><span class="sxs-lookup"><span data-stu-id="79ede-111">subscribedSku</span></span>](subscribedsku.md) |<span data-ttu-id="79ede-112">Lee las propiedades y relaciones del objeto subscribedSku.</span><span class="sxs-lookup"><span data-stu-id="79ede-112">Read properties and relationships of subscribedSku object.</span></span>|
|[<span data-ttu-id="79ede-113">Listar subscribedSku</span><span class="sxs-lookup"><span data-stu-id="79ede-113">List subscribedSku</span></span>](../api/subscribedsku_list.md) | <span data-ttu-id="79ede-114">Colección [subscribedSku](subscribedsku.md)</span><span class="sxs-lookup"><span data-stu-id="79ede-114">[subscribedSku](subscribedsku.md) collection</span></span> |<span data-ttu-id="79ede-115">Recupera la lista de suscripciones comerciales que ha adquirido una organización.</span><span class="sxs-lookup"><span data-stu-id="79ede-115">Retrieve the list of commercial subscriptions that an organization has acquired.</span></span>|

## <a name="properties"></a><span data-ttu-id="79ede-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="79ede-116">Properties</span></span>
| <span data-ttu-id="79ede-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="79ede-117">Property</span></span>     | <span data-ttu-id="79ede-118">Tipo</span><span class="sxs-lookup"><span data-stu-id="79ede-118">Type</span></span>   |<span data-ttu-id="79ede-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="79ede-119">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="79ede-120">appliesTo</span><span class="sxs-lookup"><span data-stu-id="79ede-120">appliesTo</span></span>|<span data-ttu-id="79ede-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="79ede-121">String</span></span>| <span data-ttu-id="79ede-122">Por ejemplo, "usuario" o "empresa".</span><span class="sxs-lookup"><span data-stu-id="79ede-122">For example, "User" or "Company".</span></span> |
|<span data-ttu-id="79ede-123">capabilityStatus</span><span class="sxs-lookup"><span data-stu-id="79ede-123">capabilityStatus</span></span>|<span data-ttu-id="79ede-124">Cadena</span><span class="sxs-lookup"><span data-stu-id="79ede-124">String</span></span>| <span data-ttu-id="79ede-125">Por ejemplo, "habilitado".</span><span class="sxs-lookup"><span data-stu-id="79ede-125">For example, "Enabled".</span></span> |
|<span data-ttu-id="79ede-126">consumedUnits</span><span class="sxs-lookup"><span data-stu-id="79ede-126">consumedUnits</span></span>|<span data-ttu-id="79ede-127">Int32</span><span class="sxs-lookup"><span data-stu-id="79ede-127">Int32</span></span>| <span data-ttu-id="79ede-128">El número de licencias asignadas.</span><span class="sxs-lookup"><span data-stu-id="79ede-128">The number of licenses that have been assigned.</span></span> |
|<span data-ttu-id="79ede-129">id</span><span class="sxs-lookup"><span data-stu-id="79ede-129">id</span></span>|<span data-ttu-id="79ede-130">Cadena</span><span class="sxs-lookup"><span data-stu-id="79ede-130">String</span></span>| <span data-ttu-id="79ede-p102">El identificador único del recurso del objeto sku suscrito. Clave, no admite valores NULL.</span><span class="sxs-lookup"><span data-stu-id="79ede-p102">The unique identifier for the subscribed sku object. Key, not nullable.</span></span> |
|<span data-ttu-id="79ede-133">prepaidUnits</span><span class="sxs-lookup"><span data-stu-id="79ede-133">prepaidUnits</span></span>|[<span data-ttu-id="79ede-134">licenseUnitsDetail</span><span class="sxs-lookup"><span data-stu-id="79ede-134">licenseUnitsDetail</span></span>](licenseunitsdetail.md)| <span data-ttu-id="79ede-135">Información sobre el número y el estado de las licencias prepagadas.</span><span class="sxs-lookup"><span data-stu-id="79ede-135">Information about the number and status of prepaid licenses.</span></span> |
|<span data-ttu-id="79ede-136">servicePlans</span><span class="sxs-lookup"><span data-stu-id="79ede-136">servicePlans</span></span>|<span data-ttu-id="79ede-137">Colección [servicePlanInfo](serviceplaninfo.md)</span><span class="sxs-lookup"><span data-stu-id="79ede-137">[servicePlanInfo](serviceplaninfo.md) collection</span></span>| <span data-ttu-id="79ede-p103">Información acerca de los planes de servicio que están disponibles con el SKU. No admite valores NULL</span><span class="sxs-lookup"><span data-stu-id="79ede-p103">Information about the service plans that are available with the SKU. Not nullable</span></span> |
|<span data-ttu-id="79ede-140">skuId</span><span class="sxs-lookup"><span data-stu-id="79ede-140">skuId</span></span>|<span data-ttu-id="79ede-141">Guid</span><span class="sxs-lookup"><span data-stu-id="79ede-141">Guid</span></span>| <span data-ttu-id="79ede-142">El identificador único (GUID) para el SKU de servicio.</span><span class="sxs-lookup"><span data-stu-id="79ede-142">The unique identifier (GUID) for the service SKU.</span></span> |
|<span data-ttu-id="79ede-143">skuPartNumber</span><span class="sxs-lookup"><span data-stu-id="79ede-143">skuPartNumber</span></span>|<span data-ttu-id="79ede-144">Cadena</span><span class="sxs-lookup"><span data-stu-id="79ede-144">String</span></span>| <span data-ttu-id="79ede-145">La parte numérica del SKU, por ejemplo: "AAD_PREMIUM" o "RMSBASIC".</span><span class="sxs-lookup"><span data-stu-id="79ede-145">The SKU part number; for example: "AAD_PREMIUM" or "RMSBASIC".</span></span> |

## <a name="relationships"></a><span data-ttu-id="79ede-146">Relaciones</span><span class="sxs-lookup"><span data-stu-id="79ede-146">Relationships</span></span>
<span data-ttu-id="79ede-147">Ninguno</span><span class="sxs-lookup"><span data-stu-id="79ede-147">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="79ede-148">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="79ede-148">JSON representation</span></span>

<span data-ttu-id="79ede-149">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="79ede-149">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.subscribedSku",
  "@odata.annotations": [
    {
      "capabilities": {
        "skippable": false,
        "toppable": false,
        "countable": false,
        "expandable": false,
        "filterable": false,
        "referenceable": false,
        "selectable": false
      }
    }
  ]
}-->

```json
{
  "appliesTo": "string",
  "capabilityStatus": "string",
  "consumedUnits": 1024,
  "id": "string (identifier)",
  "prepaidUnits": {"@odata.type": "microsoft.graph.licenseUnitsDetail"},
  "servicePlans": [{"@odata.type": "microsoft.graph.servicePlanInfo"}],
  "skuId": "guid",
  "skuPartNumber": "string"
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "subscribedSku resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
