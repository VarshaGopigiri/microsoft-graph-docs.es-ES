# <a name="phone-resource-type"></a><span data-ttu-id="9a8d3-101">Tipo de recurso phone</span><span class="sxs-lookup"><span data-stu-id="9a8d3-101">phone resource type</span></span>

<span data-ttu-id="9a8d3-102">Representa un número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="9a8d3-102">Represents a phone number.</span></span>


## <a name="properties"></a><span data-ttu-id="9a8d3-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9a8d3-103">Properties</span></span>
| <span data-ttu-id="9a8d3-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9a8d3-104">Property</span></span>     | <span data-ttu-id="9a8d3-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="9a8d3-105">Type</span></span>   |<span data-ttu-id="9a8d3-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="9a8d3-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9a8d3-107">number</span><span class="sxs-lookup"><span data-stu-id="9a8d3-107">number</span></span>|<span data-ttu-id="9a8d3-108">cadena</span><span class="sxs-lookup"><span data-stu-id="9a8d3-108">string</span></span>|<span data-ttu-id="9a8d3-109">El número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="9a8d3-109">The phone number.</span></span>|
|<span data-ttu-id="9a8d3-110">type</span><span class="sxs-lookup"><span data-stu-id="9a8d3-110">type</span></span>|<span data-ttu-id="9a8d3-111">phoneType</span><span class="sxs-lookup"><span data-stu-id="9a8d3-111">phoneType values</span></span>|<span data-ttu-id="9a8d3-112">El tipo de número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="9a8d3-112">The type of phone number.</span></span> <span data-ttu-id="9a8d3-113">Los valores posibles son: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager` y `radio`.</span><span class="sxs-lookup"><span data-stu-id="9a8d3-113">The possible values are `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`, , or .</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9a8d3-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9a8d3-114">JSON representation</span></span>

<span data-ttu-id="9a8d3-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="9a8d3-115">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.phone"
}-->

```json
{
  "number": "string",
  "type": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "phone resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
