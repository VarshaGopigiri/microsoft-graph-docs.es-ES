# <a name="phone-resource-type"></a><span data-ttu-id="479bd-101">Tipo de recurso phone</span><span class="sxs-lookup"><span data-stu-id="479bd-101">phone resource type</span></span>

<span data-ttu-id="479bd-102">Representa un número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="479bd-102">Represents a phone number identified in an item.</span></span>


## <a name="properties"></a><span data-ttu-id="479bd-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="479bd-103">Properties</span></span>
| <span data-ttu-id="479bd-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="479bd-104">Property</span></span>     | <span data-ttu-id="479bd-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="479bd-105">Type</span></span>   |<span data-ttu-id="479bd-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="479bd-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="479bd-107">number</span><span class="sxs-lookup"><span data-stu-id="479bd-107">number</span></span>|<span data-ttu-id="479bd-108">string</span><span class="sxs-lookup"><span data-stu-id="479bd-108">string</span></span>|<span data-ttu-id="479bd-109">El número de teléfono.</span><span class="sxs-lookup"><span data-stu-id="479bd-109">The contact's mobile phone number.</span></span>|
|<span data-ttu-id="479bd-110">type</span><span class="sxs-lookup"><span data-stu-id="479bd-110">type</span></span>|<span data-ttu-id="479bd-111">String</span><span class="sxs-lookup"><span data-stu-id="479bd-111">String</span></span>|<span data-ttu-id="479bd-p101">El tipo de número de teléfono. Valores posibles: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span><span class="sxs-lookup"><span data-stu-id="479bd-p101">The type of phone number. Possible values are: `home`, `business`, `mobile`, `other`, `assistant`, `homeFax`, `businessFax`, `otherFax`, `pager`, `radio`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="479bd-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="479bd-114">JSON representation</span></span>

<span data-ttu-id="479bd-115">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="479bd-115">Here is a JSON representation of the resource.</span></span>

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