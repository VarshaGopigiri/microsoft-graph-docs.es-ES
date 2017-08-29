# <a name="thumbnail-resource-type"></a><span data-ttu-id="fe752-101">Tipo de recurso thumbnail</span><span class="sxs-lookup"><span data-stu-id="fe752-101">Thumbnail resource type</span></span>

<span data-ttu-id="fe752-102">El tipo de recurso **thumbnail** representa una miniatura de una imagen, un vídeo, un documento o cualquier elemento que tenga una representación en mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="fe752-102">The **thumbnail** resource type represents a thumbnail for an image, video, document, or any item that has a bitmap representation.</span></span>

## <a name="json-representation"></a><span data-ttu-id="fe752-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="fe752-103">JSON representation</span></span>

<span data-ttu-id="fe752-104">A continuación se incluye una representación JSON del recurso **thumbnail**.</span><span class="sxs-lookup"><span data-stu-id="fe752-104">Here is a JSON representation of the **thumbnail** resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": ["content", "height", "width", "sourceItemId"],
  "@odata.type": "microsoft.graph.thumbnail"
}-->

```json
{
  "height": 1024,
  "sourceItemId": "string",
  "url": "string",
  "width": 1024,

  /* relationships */
  "content": "stream"
}
```

## <a name="properties"></a><span data-ttu-id="fe752-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fe752-105">Properties</span></span>

| <span data-ttu-id="fe752-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fe752-106">Property</span></span>     | <span data-ttu-id="fe752-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe752-107">Type</span></span>   | <span data-ttu-id="fe752-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe752-108">Description</span></span>                                                                                                                 |
| :----------- | :----- | :-------------------------------------------------------------------------------------------------------------------------- |
| <span data-ttu-id="fe752-109">height</span><span class="sxs-lookup"><span data-stu-id="fe752-109">height</span></span>       | <span data-ttu-id="fe752-110">Int32</span><span class="sxs-lookup"><span data-stu-id="fe752-110">Int32</span></span>  | <span data-ttu-id="fe752-111">Alto de la miniatura en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fe752-111">The height of the thumbnail, in pixels.</span></span>                                                                                     |
| <span data-ttu-id="fe752-112">sourceItemId</span><span class="sxs-lookup"><span data-stu-id="fe752-112">sourceItemId</span></span> | <span data-ttu-id="fe752-113">String</span><span class="sxs-lookup"><span data-stu-id="fe752-113">String</span></span> | <span data-ttu-id="fe752-p101">Identificador único del elemento que proporciona la vista en miniatura. Solo está disponible cuando se solicita la miniatura de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="fe752-p101">The unique identifier of the item that provided the thumbnail. This is only available when a folder thumbnail is requested.</span></span> |
| <span data-ttu-id="fe752-116">url</span><span class="sxs-lookup"><span data-stu-id="fe752-116">url</span></span>          | <span data-ttu-id="fe752-117">String</span><span class="sxs-lookup"><span data-stu-id="fe752-117">String</span></span> | <span data-ttu-id="fe752-118">Dirección URL usada para recuperar el contenido de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="fe752-118">The URL used to fetch the thumbnail content.</span></span>                                                                                |
| <span data-ttu-id="fe752-119">width</span><span class="sxs-lookup"><span data-stu-id="fe752-119">width</span></span>        | <span data-ttu-id="fe752-120">Int32</span><span class="sxs-lookup"><span data-stu-id="fe752-120">Int32</span></span>  | <span data-ttu-id="fe752-121">Ancho de la miniatura en píxeles.</span><span class="sxs-lookup"><span data-stu-id="fe752-121">The width of the thumbnail, in pixels.</span></span>                                                                                      |

## <a name="relationships"></a><span data-ttu-id="fe752-122">Relaciones</span><span class="sxs-lookup"><span data-stu-id="fe752-122">Relationships</span></span>

| <span data-ttu-id="fe752-123">Nombre</span><span class="sxs-lookup"><span data-stu-id="fe752-123">Name</span></span>    | <span data-ttu-id="fe752-124">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe752-124">Type</span></span>   | <span data-ttu-id="fe752-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe752-125">Description</span></span>                           |
| :------ | :----- | :------------------------------------ |
| <span data-ttu-id="fe752-126">content</span><span class="sxs-lookup"><span data-stu-id="fe752-126">content</span></span> | <span data-ttu-id="fe752-127">Secuencia</span><span class="sxs-lookup"><span data-stu-id="fe752-127">Stream</span></span> | <span data-ttu-id="fe752-128">La secuencia de contenido de la miniatura.</span><span class="sxs-lookup"><span data-stu-id="fe752-128">The content stream for the thumbnail.</span></span> |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "thumbnail resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
