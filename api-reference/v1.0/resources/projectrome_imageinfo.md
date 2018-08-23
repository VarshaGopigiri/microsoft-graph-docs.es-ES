# <a name="imageinfo-resource-type"></a><span data-ttu-id="8fe91-101">tipo de recurso imageInfo</span><span class="sxs-lookup"><span data-stu-id="8fe91-101">imageInfo resource type</span></span>

<span data-ttu-id="8fe91-102">Tipo complejo para representar la propiedad **attribution** del elemento [visualInfo](../resources/projectrome_visualinfo.md) del objeto [activity](../resources/projectrome_activity.md).</span><span class="sxs-lookup"><span data-stu-id="8fe91-102">A complex type for representing the **attribution** property in the [visualInfo](../resources/projectrome_visualinfo.md) part of the [activity](../resources/projectrome_activity.md) object.</span></span>

## <a name="properties"></a><span data-ttu-id="8fe91-103">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8fe91-103">Properties</span></span>

|<span data-ttu-id="8fe91-104">Nombre</span><span class="sxs-lookup"><span data-stu-id="8fe91-104">Name</span></span> | <span data-ttu-id="8fe91-105">Tipo</span><span class="sxs-lookup"><span data-stu-id="8fe91-105">Type</span></span> | <span data-ttu-id="8fe91-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="8fe91-106">Description</span></span>|
|:----|:-----|:-----------|
|<span data-ttu-id="8fe91-107">iconUrl</span><span class="sxs-lookup"><span data-stu-id="8fe91-107">iconurl</span></span> | <span data-ttu-id="8fe91-108">Cadena</span><span class="sxs-lookup"><span data-stu-id="8fe91-108">String</span></span> | <span data-ttu-id="8fe91-109">Opcional; URI que apunta a un icono que representa la aplicación utilizada para generar la actividad</span><span class="sxs-lookup"><span data-stu-id="8fe91-109">Optional; URI that points to an icon which represents the application used to generate the activity</span></span>|
|<span data-ttu-id="8fe91-110">alternateText</span><span class="sxs-lookup"><span data-stu-id="8fe91-110">alternateText</span></span> | <span data-ttu-id="8fe91-111">Cadena</span><span class="sxs-lookup"><span data-stu-id="8fe91-111">String</span></span> | <span data-ttu-id="8fe91-112">Opcional; contenido accesible (texto alternativo) que se proporciona para la imagen</span><span class="sxs-lookup"><span data-stu-id="8fe91-112">Optional; alt-text accessible content for the image</span></span>|
|<span data-ttu-id="8fe91-113">addImageQuery</span><span class="sxs-lookup"><span data-stu-id="8fe91-113">addImageQuery</span></span> | <span data-ttu-id="8fe91-114">Booleano</span><span class="sxs-lookup"><span data-stu-id="8fe91-114">Boolean</span></span> | <span data-ttu-id="8fe91-115">Opcional; parámetro utilizado para indicar que el servidor es capaz de representar imágenes dinámicamente en respuesta a parametrización.</span><span class="sxs-lookup"><span data-stu-id="8fe91-115">Optional; parameter used to indicate the server is able to render image dynamically in response to parameterization.</span></span> <span data-ttu-id="8fe91-116">Por ejemplo: una imagen de contraste alto</span><span class="sxs-lookup"><span data-stu-id="8fe91-116">For example – a high contrast image</span></span>|

## <a name="json-representation"></a><span data-ttu-id="8fe91-117">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="8fe91-117">JSON Representation</span></span>

<span data-ttu-id="8fe91-118">He aquí una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="8fe91-118">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "iconUrl",
    "alternateText",
    "addImageQuery"
  ],
  "@odata.type": "microsoft.graph.imageInfo"
}-->

```json
{
    "@odata.type": "microsoft.graph.imageInfo",
    "iconUrl": "String (URL)",
    "alternateText": "String",
    "addImageQuery": "boolean"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "imageinfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->