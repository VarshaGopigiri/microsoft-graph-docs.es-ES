# <a name="onpremisesprovisioningerror-resource-type"></a><span data-ttu-id="3c287-101">tipo de recurso onPremisesProvisioningError</span><span class="sxs-lookup"><span data-stu-id="3c287-101">onPremisesProvisioningError resource type</span></span>

<span data-ttu-id="3c287-102">Representa los errores de sincronización de directorio de las entidades [user](user.md) y [group](group.md) cuando se sincronizan los directorios locales a Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3c287-102">Represents directory synchronization errors for the [user](user.md) and [group](group.md) entities when synchronizing on-premises directories to Azure Active Directory.</span></span>

## <a name="properties"></a><span data-ttu-id="3c287-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3c287-103">Properties</span></span>

| <span data-ttu-id="3c287-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3c287-104">Property</span></span> | <span data-ttu-id="3c287-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="3c287-105">Type</span></span> | <span data-ttu-id="3c287-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="3c287-106">Description</span></span> |
|:---------------|:--------|:----------|
|<span data-ttu-id="3c287-107">categoría</span><span class="sxs-lookup"><span data-stu-id="3c287-107">category</span></span>|<span data-ttu-id="3c287-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="3c287-108">String</span></span>| <span data-ttu-id="3c287-109">Categoría del error de aprovisionamiento.</span><span class="sxs-lookup"><span data-stu-id="3c287-109">Category of the provisioning error.</span></span> <span data-ttu-id="3c287-110">Nota: Actualmente, hay un único valor posible.</span><span class="sxs-lookup"><span data-stu-id="3c287-110">Note: Currently, there is only one possible value.</span></span> <span data-ttu-id="3c287-111">Valor posible: *PropertyConflict* (indica que un valor de propiedad no es único).</span><span class="sxs-lookup"><span data-stu-id="3c287-111">Possible value: *PropertyConflict* - indicates a property value is not unique.</span></span> <span data-ttu-id="3c287-112">Otros objetos contienen el mismo valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="3c287-112">Other objects contain the same value for the property.</span></span> |
|<span data-ttu-id="3c287-113">occurredDateTime</span><span class="sxs-lookup"><span data-stu-id="3c287-113">occurredDateTime</span></span>|<span data-ttu-id="3c287-114">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="3c287-114">DateTimeOffset</span></span>| <span data-ttu-id="3c287-115">Fecha y hora en que ocurrió el error.</span><span class="sxs-lookup"><span data-stu-id="3c287-115">The time at which the error occurred.</span></span> |
|<span data-ttu-id="3c287-116">propertyCausingError</span><span class="sxs-lookup"><span data-stu-id="3c287-116">propertyCausingError</span></span>|<span data-ttu-id="3c287-117">Cadena</span><span class="sxs-lookup"><span data-stu-id="3c287-117">String</span></span>| <span data-ttu-id="3c287-118">Nombre de la propiedad del directorio que provoca el error.</span><span class="sxs-lookup"><span data-stu-id="3c287-118">Name of the directory property causing the error.</span></span> <span data-ttu-id="3c287-119">Valores posibles actuales: *UserPrincipalName* o *ProxyAddress*</span><span class="sxs-lookup"><span data-stu-id="3c287-119">Current possible values: *UserPrincipalName* or *ProxyAddress*</span></span> |
|<span data-ttu-id="3c287-120">value</span><span class="sxs-lookup"><span data-stu-id="3c287-120">value</span></span>|<span data-ttu-id="3c287-121">Cadena</span><span class="sxs-lookup"><span data-stu-id="3c287-121">String</span></span>| <span data-ttu-id="3c287-122">Valor de la propiedad que provoca el error.</span><span class="sxs-lookup"><span data-stu-id="3c287-122">Value of the property causing the error.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="3c287-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3c287-123">JSON representation</span></span>
<span data-ttu-id="3c287-124">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="3c287-124">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onPremisesProvisioningError"
}-->

```json
{
  "category": "String",
  "occurredDateTime": "String (timestamp)",
  "propertyCausingError": "String",
  "value": "String"
}

```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "onPremisesProvisioningError resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->