# <a name="serviceplaninfo-resource-type"></a><span data-ttu-id="28497-101">Tipo de recurso servicePlanInfo</span><span class="sxs-lookup"><span data-stu-id="28497-101">servicePlanInfo resource type</span></span>

<span data-ttu-id="28497-p101">Contiene información sobre un plan de servicio asociado a una SKU suscrita. La propiedad **servicePlans** de la entidad [subscribedSku](subscribedsku.md) es una colección de **servicePlanInfo**.</span><span class="sxs-lookup"><span data-stu-id="28497-p101">Contains information about a service plan associated with a subscribed SKU. The **servicePlans** property of the [subscribedSku](subscribedsku.md) entity is a collection of **servicePlanInfo**.</span></span>


## <a name="properties"></a><span data-ttu-id="28497-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="28497-104">Properties</span></span>
| <span data-ttu-id="28497-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="28497-105">Property</span></span>     | <span data-ttu-id="28497-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="28497-106">Type</span></span>   |<span data-ttu-id="28497-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="28497-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="28497-108">servicePlanId</span><span class="sxs-lookup"><span data-stu-id="28497-108">servicePlanId</span></span>|<span data-ttu-id="28497-109">Guid</span><span class="sxs-lookup"><span data-stu-id="28497-109">Guid</span></span>|<span data-ttu-id="28497-110">Identificador único del plan de servicio.</span><span class="sxs-lookup"><span data-stu-id="28497-110">The unique identifier of the service plan.</span></span>|
|<span data-ttu-id="28497-111">servicePlanName</span><span class="sxs-lookup"><span data-stu-id="28497-111">servicePlanName</span></span>|<span data-ttu-id="28497-112">String</span><span class="sxs-lookup"><span data-stu-id="28497-112">String</span></span>|<span data-ttu-id="28497-113">Nombre del plan de servicio.</span><span class="sxs-lookup"><span data-stu-id="28497-113">The name of the service plan.</span></span>|
|<span data-ttu-id="28497-114">provisioningStatus</span><span class="sxs-lookup"><span data-stu-id="28497-114">provisioningStatus</span></span>|<span data-ttu-id="28497-115">String</span><span class="sxs-lookup"><span data-stu-id="28497-115">String</span></span>|<span data-ttu-id="28497-p102">El estado de aprovisionamiento del plan de servicio. Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="28497-p102">The provisioning status of the service plan. Possible values:</span></span><br/><span data-ttu-id="28497-118">“Success”: el servicio está completamente aprovisionado.</span><span class="sxs-lookup"><span data-stu-id="28497-118">"Success" - Service is fully provisioned.</span></span><br/><span data-ttu-id="28497-119">“Disabled”: se deshabilitó el servicio.</span><span class="sxs-lookup"><span data-stu-id="28497-119">"Disabled" - Service has been disabled.</span></span><br/><span data-ttu-id="28497-120">“PendingInput”: aún no se aprovisionó el servicio; esperando la confirmación del servicio.</span><span class="sxs-lookup"><span data-stu-id="28497-120">"PendingInput" - Service is not yet provisioned; awaiting service confirmation.</span></span><br/><span data-ttu-id="28497-121">“PendingActivation”: el servicio está aprovisionado, pero necesita una activación explícita por el administrador (por ejemplo, plan de servicio de Intune_O365).</span><span class="sxs-lookup"><span data-stu-id="28497-121">"PendingActivation" - Service is provisioned but requires explicit activation by administrator (for example, Intune_O365 service plan)</span></span><br/><span data-ttu-id="28497-122">“PendingProvisioning”: Microsoft agregó un nuevo servicio al SKU del producto y aún no se activó en el inquilino.</span><span class="sxs-lookup"><span data-stu-id="28497-122">"PendingProvisioning" - Microsoft has added a new service to the product SKU and it has not been activated in the tenant, yet.</span></span>|
|<span data-ttu-id="28497-123">appliesTo</span><span class="sxs-lookup"><span data-stu-id="28497-123">appliesTo</span></span>|<span data-ttu-id="28497-124">String</span><span class="sxs-lookup"><span data-stu-id="28497-124">String</span></span>|<span data-ttu-id="28497-p103">El objeto al que se puede asignar el plan de servicio. Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="28497-p103">The object the service plan can be assigned to. Possible values:</span></span><br/><span data-ttu-id="28497-127">“User”: el plan de servicio se puede asignar a usuarios individuales.</span><span class="sxs-lookup"><span data-stu-id="28497-127">"User" - service plan can be assigned to individual users.</span></span><br/><span data-ttu-id="28497-128">“Company”: el plan de servicio se puede asignar a todo el inquilino.</span><span class="sxs-lookup"><span data-stu-id="28497-128">"Company" - service plan can be assigned to the entire tenant.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="28497-129">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="28497-129">JSON representation</span></span>

<span data-ttu-id="28497-130">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="28497-130">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.servicePlanInfo"
}-->

```json
{
  "appliesTo": "string",
  "provisioningStatus": "string",
  "servicePlanId": "guid",
  "servicePlanName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "servicePlanInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
