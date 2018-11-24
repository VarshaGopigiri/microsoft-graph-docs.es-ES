# <a name="teamfunsettings-resource-type"></a><span data-ttu-id="ec439-101">tipo de recurso teamFunSettings</span><span class="sxs-lookup"><span data-stu-id="ec439-101">teamFunSettings resource type</span></span>



<span data-ttu-id="ec439-102">Opciones para configurar el uso de Giphy, memes y pegatinas en el [equipo](team.md).</span><span class="sxs-lookup"><span data-stu-id="ec439-102">Settings to configure use of Giphy, memes, and stickers in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="ec439-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ec439-103">Properties</span></span>
| <span data-ttu-id="ec439-104">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ec439-104">Property</span></span>     | <span data-ttu-id="ec439-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="ec439-105">Type</span></span>   |<span data-ttu-id="ec439-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="ec439-106">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="ec439-107">allowGiphy</span><span class="sxs-lookup"><span data-stu-id="ec439-107">allowGiphy</span></span>|<span data-ttu-id="ec439-108">Booleano</span><span class="sxs-lookup"><span data-stu-id="ec439-108">Boolean</span></span>|<span data-ttu-id="ec439-109">Si establece en verdadero, permite el uso de Giphy.</span><span class="sxs-lookup"><span data-stu-id="ec439-109">If set to true, enables Giphy use.</span></span>|
|<span data-ttu-id="ec439-110">giphyContentRating</span><span class="sxs-lookup"><span data-stu-id="ec439-110">giphyContentRating</span></span>|<span data-ttu-id="ec439-111">Cadena (enumeración)</span><span class="sxs-lookup"><span data-stu-id="ec439-111">String (enum)</span></span>|<span data-ttu-id="ec439-112">Clasificación de contenido de Giphy.</span><span class="sxs-lookup"><span data-stu-id="ec439-112">Giphy content rating.</span></span> <span data-ttu-id="ec439-113">Los valores posibles son: `moderate` y `strict`.</span><span class="sxs-lookup"><span data-stu-id="ec439-113">Possible values are: `moderate`, `strict`.</span></span>|
|<span data-ttu-id="ec439-114">allowStickersAndMemes</span><span class="sxs-lookup"><span data-stu-id="ec439-114">allowStickersAndMemes</span></span>|<span data-ttu-id="ec439-115">Booleano</span><span class="sxs-lookup"><span data-stu-id="ec439-115">Boolean</span></span>|<span data-ttu-id="ec439-116">Si establece en true, permite a los usuarios para que incluya pegatinas y memes.</span><span class="sxs-lookup"><span data-stu-id="ec439-116">If set to true, enables users to include stickers and memes.</span></span>|
|<span data-ttu-id="ec439-117">allowCustomMemes</span><span class="sxs-lookup"><span data-stu-id="ec439-117">allowCustomMemes</span></span>|<span data-ttu-id="ec439-118">Booleano</span><span class="sxs-lookup"><span data-stu-id="ec439-118">Boolean</span></span>|<span data-ttu-id="ec439-119">Si establece en true, permite a los usuarios para incluir memes personalizado.</span><span class="sxs-lookup"><span data-stu-id="ec439-119">If set to true, enables users to include custom memes.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="ec439-120">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="ec439-120">JSON representation</span></span>

<span data-ttu-id="ec439-121">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="ec439-121">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamFunSettings"
}-->

```json
{
  "allowGiphy": true,
  "giphyContentRating": "strict",
  "allowStickersAndMemes": true,
  "allowCustomMemes": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "team's funSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
