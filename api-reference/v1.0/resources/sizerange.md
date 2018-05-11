# <a name="sizerange-resource-type"></a><span data-ttu-id="c0d71-101">Tipo de recurso sizeRange</span><span class="sxs-lookup"><span data-stu-id="c0d71-101">sizeRange resource type</span></span>


<span data-ttu-id="c0d71-102">Especifica los tamaños máximo y mínimo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.</span><span class="sxs-lookup"><span data-stu-id="c0d71-102">Specifies the maximum and minimum sizes (in kilobytes) that an incoming message must have in order for a condition or exception to apply.</span></span>

## <a name="properties"></a><span data-ttu-id="c0d71-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c0d71-103">Properties</span></span>
| <span data-ttu-id="c0d71-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="c0d71-104">Property</span></span>     | <span data-ttu-id="c0d71-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="c0d71-105">Type</span></span>   |<span data-ttu-id="c0d71-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c0d71-106">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="c0d71-107">maximumSize</span><span class="sxs-lookup"><span data-stu-id="c0d71-107">maximumSize</span></span> | <span data-ttu-id="c0d71-108">Int32</span><span class="sxs-lookup"><span data-stu-id="c0d71-108">Int32</span></span> | <span data-ttu-id="c0d71-109">Tamaño máximo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.</span><span class="sxs-lookup"><span data-stu-id="c0d71-109">The maximum size (in kilobytes) that an incoming message must have in order for a condition or exception to apply.</span></span> |
| <span data-ttu-id="c0d71-110">minimumSize</span><span class="sxs-lookup"><span data-stu-id="c0d71-110">minimumSize</span></span> | <span data-ttu-id="c0d71-111">Int32</span><span class="sxs-lookup"><span data-stu-id="c0d71-111">Int32</span></span> | <span data-ttu-id="c0d71-112">Tamaño mínimo (en kilobytes) que un mensaje entrante debe tener para que una condición o excepción se aplique.</span><span class="sxs-lookup"><span data-stu-id="c0d71-112">The minimum size (in kilobytes) that an incoming message must have in order for a condition or exception to apply.</span></span> |


## <a name="json-representation"></a><span data-ttu-id="c0d71-113">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="c0d71-113">JSON representation</span></span>
<span data-ttu-id="c0d71-114">Aquí tiene una representación JSON del recurso.</span><span class="sxs-lookup"><span data-stu-id="c0d71-114">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
   ],
  "@odata.type": "microsoft.graph.sizeRange"
}-->

```json
{
  "maximumSize": "Int32",
  "minimumSize": "Int32"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "sizeRange resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->