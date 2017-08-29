# <a name="itembody-resource-type"></a><span data-ttu-id="d7a2f-101">Tipo de recurso itemBody</span><span class="sxs-lookup"><span data-stu-id="d7a2f-101">itemBody resource type</span></span>

<span data-ttu-id="d7a2f-102">Representa las propiedades del cuerpo de un elemento, como un mensaje, un evento o una publicación de grupo.</span><span class="sxs-lookup"><span data-stu-id="d7a2f-102">Represents properties of the body of an item, such as a message, event or group post.</span></span>

## <a name="properties"></a><span data-ttu-id="d7a2f-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d7a2f-103">Properties</span></span>
| <span data-ttu-id="d7a2f-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d7a2f-104">Property</span></span>     | <span data-ttu-id="d7a2f-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7a2f-105">Type</span></span>   |<span data-ttu-id="d7a2f-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7a2f-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d7a2f-107">content</span><span class="sxs-lookup"><span data-stu-id="d7a2f-107">content</span></span>|<span data-ttu-id="d7a2f-108">String</span><span class="sxs-lookup"><span data-stu-id="d7a2f-108">String</span></span>|<span data-ttu-id="d7a2f-109">Contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="d7a2f-109">The content of the item.</span></span>|
|<span data-ttu-id="d7a2f-110">contentType</span><span class="sxs-lookup"><span data-stu-id="d7a2f-110">contentType</span></span>|<span data-ttu-id="d7a2f-111">String</span><span class="sxs-lookup"><span data-stu-id="d7a2f-111">String</span></span>|<span data-ttu-id="d7a2f-p101">Tipo de contenido. Valores posibles: `Text` y `HTML`.</span><span class="sxs-lookup"><span data-stu-id="d7a2f-p101">The type of the content. Possible values are `Text` and `HTML`.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="d7a2f-114">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d7a2f-114">JSON representation</span></span>

<span data-ttu-id="d7a2f-115">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d7a2f-115">Here is a JSON representation of the resource</span></span>

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
