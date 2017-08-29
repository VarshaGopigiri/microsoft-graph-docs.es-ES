# <a name="verifieddomain-resource-type"></a><span data-ttu-id="9f1c3-101">Tipo de recurso verifiedDomain</span><span class="sxs-lookup"><span data-stu-id="9f1c3-101">verifiedDomain resource type</span></span>

<span data-ttu-id="9f1c3-p101">Especifica un dominio para un inquilino. La propiedad **verifiedDomains** de la entidad [organization](organization.md) es una colección de **VerifiedDomain**.</span><span class="sxs-lookup"><span data-stu-id="9f1c3-p101">Specifies a domain for a tenant. The **verifiedDomains** property of the [organization](organization.md) entity is a collection of **VerifiedDomain**.</span></span>


## <a name="properties"></a><span data-ttu-id="9f1c3-104">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9f1c3-104">Properties</span></span>
| <span data-ttu-id="9f1c3-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9f1c3-105">Property</span></span>     | <span data-ttu-id="9f1c3-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="9f1c3-106">Type</span></span>   |<span data-ttu-id="9f1c3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9f1c3-107">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9f1c3-108">capabilities</span><span class="sxs-lookup"><span data-stu-id="9f1c3-108">capabilities</span></span>|<span data-ttu-id="9f1c3-109">String</span><span class="sxs-lookup"><span data-stu-id="9f1c3-109">String</span></span>|<span data-ttu-id="9f1c3-110">Por ejemplo, "Email", "OfficeCommunicationsOnline".</span><span class="sxs-lookup"><span data-stu-id="9f1c3-110">For example, “Email”, “OfficeCommunicationsOnline”.</span></span>|
|<span data-ttu-id="9f1c3-111">isDefault</span><span class="sxs-lookup"><span data-stu-id="9f1c3-111">isDefault</span></span>|<span data-ttu-id="9f1c3-112">Boolean</span><span class="sxs-lookup"><span data-stu-id="9f1c3-112">Boolean</span></span>|                <span data-ttu-id="9f1c3-113">**true** si se trata del dominio predeterminado asociado al inquilino; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9f1c3-113">**true** if this is the default domain associated with the tenant; otherwise, **false**.</span></span>            |
|<span data-ttu-id="9f1c3-114">isInitial</span><span class="sxs-lookup"><span data-stu-id="9f1c3-114">isInitial</span></span>|<span data-ttu-id="9f1c3-115">Boolean</span><span class="sxs-lookup"><span data-stu-id="9f1c3-115">Boolean</span></span>|<span data-ttu-id="9f1c3-116">**true** si se trata del dominio inicial asociado al inquilino; de lo contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="9f1c3-116">**true** if this is the initial domain associated with the tenant; otherwise, **false**</span></span>|
|<span data-ttu-id="9f1c3-117">name</span><span class="sxs-lookup"><span data-stu-id="9f1c3-117">name</span></span>|<span data-ttu-id="9f1c3-118">String</span><span class="sxs-lookup"><span data-stu-id="9f1c3-118">String</span></span>|<span data-ttu-id="9f1c3-119">Nombre del dominio; por ejemplo, "contoso.onmicrosoft.com".</span><span class="sxs-lookup"><span data-stu-id="9f1c3-119">The domain name; for example, “contoso.onmicrosoft.com”</span></span>|
|<span data-ttu-id="9f1c3-120">type</span><span class="sxs-lookup"><span data-stu-id="9f1c3-120">type</span></span>|<span data-ttu-id="9f1c3-121">String</span><span class="sxs-lookup"><span data-stu-id="9f1c3-121">String</span></span>|<span data-ttu-id="9f1c3-122">Por ejemplo, "Administrado".</span><span class="sxs-lookup"><span data-stu-id="9f1c3-122">For example, “Managed”.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9f1c3-123">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9f1c3-123">JSON representation</span></span>

<span data-ttu-id="9f1c3-124">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9f1c3-124">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.verifieddomain"
}-->

```json
{
  "capabilities": "string",
  "isDefault": true,
  "isInitial": true,
  "name": "string",
  "type": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "verifiedDomain resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
