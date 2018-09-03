# <a name="website-resource-type"></a><span data-ttu-id="ddea3-101">Tipo de recurso website</span><span class="sxs-lookup"><span data-stu-id="ddea3-101">website resource type</span></span>

<span data-ttu-id="ddea3-102">Representa un sitio web.</span><span class="sxs-lookup"><span data-stu-id="ddea3-102">Represents a website.</span></span>


## <a name="properties"></a><span data-ttu-id="ddea3-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ddea3-103">Properties</span></span>
| <span data-ttu-id="ddea3-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ddea3-104">Property</span></span>     | <span data-ttu-id="ddea3-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddea3-105">Type</span></span>   |<span data-ttu-id="ddea3-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddea3-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ddea3-107">type</span><span class="sxs-lookup"><span data-stu-id="ddea3-107">type</span></span>|<span data-ttu-id="ddea3-108">websiteType</span><span class="sxs-lookup"><span data-stu-id="ddea3-108">WebsiteType</span></span>| <span data-ttu-id="ddea3-109">Los valores posibles son: `other`, `home`, `work`, `blog` y`profile`.</span><span class="sxs-lookup"><span data-stu-id="ddea3-109">The possible values are `other`, `home`, `work`, `blog`, `profile`, , , , , , , or .</span></span>|
|<span data-ttu-id="ddea3-110">address</span><span class="sxs-lookup"><span data-stu-id="ddea3-110">address</span></span>|<span data-ttu-id="ddea3-111">cadena</span><span class="sxs-lookup"><span data-stu-id="ddea3-111">string</span></span>|<span data-ttu-id="ddea3-112">Dirección URL del sitio web.</span><span class="sxs-lookup"><span data-stu-id="ddea3-112">The URL of the website.</span></span>|
|<span data-ttu-id="ddea3-113">displayName</span><span class="sxs-lookup"><span data-stu-id="ddea3-113">displayName</span></span>|<span data-ttu-id="ddea3-114">cadena</span><span class="sxs-lookup"><span data-stu-id="ddea3-114">string</span></span>|<span data-ttu-id="ddea3-115">Nombre para mostrar del sitio web.</span><span class="sxs-lookup"><span data-stu-id="ddea3-115">The display name of the web site.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ddea3-116">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ddea3-116">JSON representation</span></span>

<span data-ttu-id="ddea3-117">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ddea3-117">The following is a JSON representation of the resource.</span></span>

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
