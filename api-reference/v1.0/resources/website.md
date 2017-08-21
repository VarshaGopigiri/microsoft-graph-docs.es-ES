# <a name="website-resource-type"></a><span data-ttu-id="3f96e-101">Tipo de recurso website</span><span class="sxs-lookup"><span data-stu-id="3f96e-101">website resource type</span></span>

<span data-ttu-id="3f96e-102">Representa un sitio web.</span><span class="sxs-lookup"><span data-stu-id="3f96e-102">Represents a group on a wssnoverslong website.</span></span>


## <a name="properties"></a><span data-ttu-id="3f96e-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3f96e-103">Properties</span></span>
| <span data-ttu-id="3f96e-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="3f96e-104">Property</span></span>     | <span data-ttu-id="3f96e-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="3f96e-105">Type</span></span>   |<span data-ttu-id="3f96e-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f96e-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="3f96e-107">type</span><span class="sxs-lookup"><span data-stu-id="3f96e-107">type</span></span>|<span data-ttu-id="3f96e-108">String</span><span class="sxs-lookup"><span data-stu-id="3f96e-108">String</span></span>| <span data-ttu-id="3f96e-109">Valores posibles: `other`, `home`, `work`, `blog`, `profile`.</span><span class="sxs-lookup"><span data-stu-id="3f96e-109">Possible values are: `other`, `home`, `work`, `blog`, `profile`.</span></span>|
|<span data-ttu-id="3f96e-110">address</span><span class="sxs-lookup"><span data-stu-id="3f96e-110">address</span></span>|<span data-ttu-id="3f96e-111">string</span><span class="sxs-lookup"><span data-stu-id="3f96e-111">string</span></span>|<span data-ttu-id="3f96e-112">Dirección URL del sitio web.</span><span class="sxs-lookup"><span data-stu-id="3f96e-112">The URL of the current website.</span></span>|
|<span data-ttu-id="3f96e-113">displayName</span><span class="sxs-lookup"><span data-stu-id="3f96e-113">displayName</span></span>|<span data-ttu-id="3f96e-114">string</span><span class="sxs-lookup"><span data-stu-id="3f96e-114">string</span></span>|<span data-ttu-id="3f96e-115">Nombre para mostrar del sitio web.</span><span class="sxs-lookup"><span data-stu-id="3f96e-115">The display name of the web site.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="3f96e-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="3f96e-116">JSON representation</span></span>

<span data-ttu-id="3f96e-117">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="3f96e-117">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.website"
}-->

```json
{
  "type": "String",
  "address": "string",
  "displayName": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "webSite resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
