# <a name="onenoteresource-resource-type"></a><span data-ttu-id="aeb98-101">Tipo de recurso OneNoteResource</span><span class="sxs-lookup"><span data-stu-id="aeb98-101">OneNoteResource resource type</span></span>

<span data-ttu-id="aeb98-102">Imagen u otro recurso de archivo en una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="aeb98-102">An image or other file resource on a OneNote page.</span></span> 

<span data-ttu-id="aeb98-103">Puede obtener los datos binarios de un recurso, pero no puede obtener una representación JSON de un objeto de recurso o una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="aeb98-103">You can get the binary data of a resource, but getting a JSON representation of a resource object or a resource collection is not supported.</span></span>

<!--{
  "blockType": "resource",
  "baseType": "microsoft.graph.onenoteEntityBaseModel",
  "optionalProperties": [],
  "isMediaEntity": true,
  "@odata.type": "microsoft.graph.onenoteResource"
}-->

```json
{
  "content": { "@odata.type": "Edm.Stream" },
  "contentUrl": "string (url)"
}
```

<span data-ttu-id="aeb98-104">Obtenga los datos binarios de un recurso específico enviando una solicitud GET al punto de conexión `content` del recurso:</span><span class="sxs-lookup"><span data-stu-id="aeb98-104">Get the binary data of a specific resource by sending a GET request to the resource's `content` endpoint:</span></span>

```
GET ../onenote/resources/{id}/content
```

<span data-ttu-id="aeb98-105">El URI de recurso del archivo se devuelve al obtener el contenido HTML de una página mediante la siguiente solicitud:</span><span class="sxs-lookup"><span data-stu-id="aeb98-105">The file's resource URI is returned when you get a page's HTML content using the following request:</span></span>

```
GET ../onenote/pages/{id}/content
```

<span data-ttu-id="aeb98-106">En la página HTML, la etiqueta `img` incluye puntos de conexión del recurso de imagen original en el atributo `data-fullres-src` y de la imagen optimizada en el atributo `src`:</span><span class="sxs-lookup"><span data-stu-id="aeb98-106">In the page HTML, an `img` tag includes endpoints for the original image resource in the `data-fullres-src` attribute and the optimized image in the `src` attribute:</span></span>
```
<img 
    src="image-resource-url"  
    data-src-type="media-type"
    data-fullres-src="image-resource-url"  
    data-fullres-src-type="media-type" ... />
```

<span data-ttu-id="aeb98-107">La etiqueta `object` (que representa archivos como PDF, DOCX y PNG) incluye el punto de conexión del recurso de archivo en el atributo `data`:</span><span class="sxs-lookup"><span data-stu-id="aeb98-107">An `object` tag (which represents files such as PDF, DOCX, and PNG) includes the endpoint for the file resource in the `data` attribute:</span></span>

```
<object
    data="file-resource-url"
    data-attachment="file-name.file-type" 
    type="media-type" ... />
```

## <a name="properties"></a><span data-ttu-id="aeb98-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="aeb98-108">Properties</span></span>

| <span data-ttu-id="aeb98-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="aeb98-109">Property</span></span>             | <span data-ttu-id="aeb98-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="aeb98-110">Type</span></span>            | <span data-ttu-id="aeb98-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeb98-111">Description</span></span>
|:---------------------|:----------------|:---------------------------------
| <span data-ttu-id="aeb98-112">content</span><span class="sxs-lookup"><span data-stu-id="aeb98-112">content</span></span>              | <span data-ttu-id="aeb98-113">Secuencia</span><span class="sxs-lookup"><span data-stu-id="aeb98-113">Stream</span></span>          | <span data-ttu-id="aeb98-114">La secuencia de contenido</span><span class="sxs-lookup"><span data-stu-id="aeb98-114">The content stream.</span></span>
| <span data-ttu-id="aeb98-115">contentUrl</span><span class="sxs-lookup"><span data-stu-id="aeb98-115">contentUrl</span></span>           | <span data-ttu-id="aeb98-116">Cadena (url)</span><span class="sxs-lookup"><span data-stu-id="aeb98-116">string (url)</span></span>    | <span data-ttu-id="aeb98-117">La dirección URL para descargar el contenido</span><span class="sxs-lookup"><span data-stu-id="aeb98-117">The URL for the page's HTML content.  Read-only.</span></span>

## <a name="relationships"></a><span data-ttu-id="aeb98-118">Relaciones</span><span class="sxs-lookup"><span data-stu-id="aeb98-118">Relationships</span></span>
<span data-ttu-id="aeb98-119">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="aeb98-119">None.</span></span>


## <a name="methods"></a><span data-ttu-id="aeb98-120">Métodos</span><span class="sxs-lookup"><span data-stu-id="aeb98-120">Methods</span></span>
| <span data-ttu-id="aeb98-121">Método</span><span class="sxs-lookup"><span data-stu-id="aeb98-121">Method</span></span>           | <span data-ttu-id="aeb98-122">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aeb98-122">Return Type</span></span>    |<span data-ttu-id="aeb98-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="aeb98-123">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="aeb98-124">Obtener datos binarios de recursos</span><span class="sxs-lookup"><span data-stu-id="aeb98-124">Get resource binary data</span></span>](../api/resource_get.md) | <span data-ttu-id="aeb98-125">Secuencia</span><span class="sxs-lookup"><span data-stu-id="aeb98-125">Stream</span></span> |<span data-ttu-id="aeb98-126">Recuperar los datos binarios de un recurso de archivo o imagen.</span><span class="sxs-lookup"><span data-stu-id="aeb98-126">Retrieve the binary data of a file or image resource.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "resource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->