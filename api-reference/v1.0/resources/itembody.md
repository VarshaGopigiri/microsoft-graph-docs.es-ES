# <a name="itembody-resource-type"></a><span data-ttu-id="89c51-101">Tipo de recurso itemBody</span><span class="sxs-lookup"><span data-stu-id="89c51-101">itemBody resource type</span></span>

<span data-ttu-id="89c51-102">Representa las propiedades del cuerpo de un elemento, como un mensaje, un evento o una publicación de grupo.</span><span class="sxs-lookup"><span data-stu-id="89c51-102">Represents properties of the body of an item, such as a message, event or group post.</span></span>

## <a name="properties"></a><span data-ttu-id="89c51-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="89c51-103">Properties</span></span>
| <span data-ttu-id="89c51-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="89c51-104">Property</span></span>     | <span data-ttu-id="89c51-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="89c51-105">Type</span></span>   |<span data-ttu-id="89c51-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="89c51-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="89c51-107">content</span><span class="sxs-lookup"><span data-stu-id="89c51-107">content</span></span>|<span data-ttu-id="89c51-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="89c51-108">String</span></span>|<span data-ttu-id="89c51-109">Contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="89c51-109">The content of the item.</span></span>|
|<span data-ttu-id="89c51-110">contentType</span><span class="sxs-lookup"><span data-stu-id="89c51-110">contentType</span></span>|<span data-ttu-id="89c51-111">bodyType</span><span class="sxs-lookup"><span data-stu-id="89c51-111">BodyType</span></span>|<span data-ttu-id="89c51-p101">Tipo de contenido. Valores posibles: `Text` y `HTML`.</span><span class="sxs-lookup"><span data-stu-id="89c51-p101">The type of the content. Possible values are `Text` and `HTML`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="89c51-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="89c51-114">JSON representation</span></span>

<span data-ttu-id="89c51-115">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="89c51-115">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.itemBody"
}-->

```json
{
  "content": "string",
  "contentType": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "itemBody resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
