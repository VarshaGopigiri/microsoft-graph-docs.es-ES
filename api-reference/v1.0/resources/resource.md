# <a name="resource-resource-type"></a><span data-ttu-id="9fbbb-101">Tipo de recurso resource</span><span class="sxs-lookup"><span data-stu-id="9fbbb-101">resource resource type</span></span>

<span data-ttu-id="9fbbb-102">Imagen u otro recurso de archivo en una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="9fbbb-102">An image or other file resource on a OneNote page.</span></span> 

<span data-ttu-id="9fbbb-103">Puede obtener los datos binarios de un recurso, pero no puede obtener una representación JSON de un objeto de recurso o una colección de recursos.</span><span class="sxs-lookup"><span data-stu-id="9fbbb-103">You can get the binary data of a resource, but getting a JSON representation of a resource object or a resource collection is not supported.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenoteResource"
}-->

<span data-ttu-id="9fbbb-104">Obtenga los datos binarios de un recurso específico enviando una solicitud GET al punto de conexión `content` del recurso:</span><span class="sxs-lookup"><span data-stu-id="9fbbb-104">Get the binary data of a specific resource by sending a GET request to the resource's `content` endpoint:</span></span>

```
GET ../onenote/resources/{id}/content
```

<span data-ttu-id="9fbbb-105">El URI de recurso del archivo se devuelve al obtener el contenido HTML de una página mediante la siguiente solicitud:</span><span class="sxs-lookup"><span data-stu-id="9fbbb-105">The file's resource URI is returned when you get a page's HTML content using the following request:</span></span>

```
GET ../onenote/pages/{id}/content
```

<span data-ttu-id="9fbbb-106">En la página HTML, la etiqueta `img` incluye puntos de conexión del recurso de imagen original en el atributo `data-fullres-src` y de la imagen optimizada en el atributo `src`:</span><span class="sxs-lookup"><span data-stu-id="9fbbb-106">In the page HTML, an `img` tag includes endpoints for the original image resource in the `data-fullres-src` attribute and the optimized image in the `src` attribute:</span></span>
```
<img 
    src="image-resource-url"  
    data-src-type="media-type"
    data-fullres-src="image-resource-url"  
    data-fullres-src-type="media-type" ... />
```

<span data-ttu-id="9fbbb-107">La etiqueta `object` (que representa archivos como PDF, DOCX y PNG) incluye el punto de conexión del recurso de archivo en el atributo `data`:</span><span class="sxs-lookup"><span data-stu-id="9fbbb-107">An `object` tag (which represents files such as PDF, DOCX, and PNG) includes the endpoint for the file resource in the `data` attribute:</span></span>

```
<object
    data="file-resource-url"
    data-attachment="file-name.file-type" 
    type="media-type" ... />
```

## <a name="properties"></a><span data-ttu-id="9fbbb-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9fbbb-108">Properties</span></span>
<span data-ttu-id="9fbbb-109">Ninguna.</span><span class="sxs-lookup"><span data-stu-id="9fbbb-109">None.</span></span>

## <a name="relationships"></a><span data-ttu-id="9fbbb-110">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9fbbb-110">Relationships</span></span>
<span data-ttu-id="9fbbb-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="9fbbb-111">None.</span></span>


## <a name="methods"></a><span data-ttu-id="9fbbb-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9fbbb-112">Methods</span></span>
| <span data-ttu-id="9fbbb-113">Método</span><span class="sxs-lookup"><span data-stu-id="9fbbb-113">Method</span></span>           | <span data-ttu-id="9fbbb-114">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9fbbb-114">Return Type</span></span>    |<span data-ttu-id="9fbbb-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9fbbb-115">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9fbbb-116">Obtener datos binarios de recursos</span><span class="sxs-lookup"><span data-stu-id="9fbbb-116">Get resource binary data</span></span>](../api/resource_get.md) | <span data-ttu-id="9fbbb-117">Secuencia</span><span class="sxs-lookup"><span data-stu-id="9fbbb-117">Stream</span></span> |<span data-ttu-id="9fbbb-118">Recuperar los datos binarios de un recurso de archivo o imagen.</span><span class="sxs-lookup"><span data-stu-id="9fbbb-118">Retrieve the binary data of a file or image resource.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "resource resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->