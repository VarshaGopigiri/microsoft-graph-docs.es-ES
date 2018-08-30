# <a name="visualinfo-resource-type"></a><span data-ttu-id="90ca8-101">Tipo de recurso visualInfo</span><span class="sxs-lookup"><span data-stu-id="90ca8-101">visualInfo resource type</span></span>

<span data-ttu-id="90ca8-102">Un tipo complejo para que representa la propiedad **visualElements** en el objeto [activity](../resources/projectrome_activity.md).</span><span class="sxs-lookup"><span data-stu-id="90ca8-102">A complex type for representing the **attribution** property in the [visualInfo part of the activity](../resources/projectrome_activity.md) object.</span></span>

<span data-ttu-id="90ca8-103">Cada actividad del usuario se mostrará en la escala de tiempo como una tarjeta adaptable.</span><span class="sxs-lookup"><span data-stu-id="90ca8-103">Each user activity will be shown in Timeline as an Adaptive Card.</span></span> <span data-ttu-id="90ca8-104">Animamos a los programadores de la aplicación a proporcionar una tarjeta personalizada que capture la esencia de la actividad que tuvo lugar en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="90ca8-104">App developers are encouraged to provide a custom Card which captures the essence of the activity which took place in your app.</span></span> <span data-ttu-id="90ca8-105">Esto es posible, ya que proporciona una tarjeta de JSON personalizada en la propiedad de contenido.</span><span class="sxs-lookup"><span data-stu-id="90ca8-105">This is possible by providing a custom JSON card in the content property.</span></span>

<span data-ttu-id="90ca8-106">Además de metadatos visuales con una tarjeta adaptable, la aplicación puede especificar los metadatos de contenido: datos que se usaron para generar inferencias en la actividad de usuario con el fin de ofrecer nuevas actividades para lograr futuro compromiso.</span><span class="sxs-lookup"><span data-stu-id="90ca8-106">In addition to visual metadata with an Adaptive Card, app can specify content metadata – data that be used to build inferences on the user’s activity in order to offer new activities for future re-engagement.</span></span> <span data-ttu-id="90ca8-107">Esto es posible mediante el uso de propiedad de contentInfo de la actividad para proporcionar un objeto JSON que aproveche las propiedades schema.org para describir el contenido.</span><span class="sxs-lookup"><span data-stu-id="90ca8-107">This is possible by using the activity's contentInfo property to provide a JSON object which leverages schema.org properties to describe the content.</span></span>

<span data-ttu-id="90ca8-108">Si no se proporciona una ficha personalizada, se generará una tarjeta simple mediante las propiedades displayText y description.</span><span class="sxs-lookup"><span data-stu-id="90ca8-108">If a custom card is not provided, a simple card will be generated using displayText and description properties.</span></span> <span data-ttu-id="90ca8-109">Se recomiendan las tarjetas personalizadas para presentar el mejor contenido desde dentro de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="90ca8-109">Custom cards are recommended to showcase the best content from within your app.</span></span>

## <a name="properties"></a><span data-ttu-id="90ca8-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="90ca8-110">Properties</span></span>

|<span data-ttu-id="90ca8-111">Nombre</span><span class="sxs-lookup"><span data-stu-id="90ca8-111">Name</span></span> | <span data-ttu-id="90ca8-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="90ca8-112">Type</span></span> | <span data-ttu-id="90ca8-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="90ca8-113">Description</span></span>|
|:----|:------|:-----------|
|<span data-ttu-id="90ca8-114">displayText</span><span class="sxs-lookup"><span data-stu-id="90ca8-114">displayText</span></span> | <span data-ttu-id="90ca8-115">Cadena</span><span class="sxs-lookup"><span data-stu-id="90ca8-115">String</span></span> | <span data-ttu-id="90ca8-116">Necesario.</span><span class="sxs-lookup"><span data-stu-id="90ca8-116">Required.</span></span> <span data-ttu-id="90ca8-117">Breve descripción de texto de la actividad de usuario único (por ejemplo, el nombre de documento en los casos donde una actividad hace referencia a la creación de documentos)</span><span class="sxs-lookup"><span data-stu-id="90ca8-117">Short text description of the user's unique activity (for example, document name in cases where an activity refers to document creation)</span></span>|
|<span data-ttu-id="90ca8-118">description</span><span class="sxs-lookup"><span data-stu-id="90ca8-118">description</span></span> | <span data-ttu-id="90ca8-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="90ca8-119">String</span></span> | <span data-ttu-id="90ca8-120">Opcional.</span><span class="sxs-lookup"><span data-stu-id="90ca8-120">Optional.</span></span> <span data-ttu-id="90ca8-121">Descripción de texto más larga de la actividad de usuario único (ejemplo: nombre, primera oración y metadatos de documentos)</span><span class="sxs-lookup"><span data-stu-id="90ca8-121">Longer text description of the user's unique activity (example: document name, first sentence, and/or metadata)</span></span>|
|<span data-ttu-id="90ca8-122">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="90ca8-122">background-color</span></span> | <span data-ttu-id="90ca8-123">Cadena</span><span class="sxs-lookup"><span data-stu-id="90ca8-123">String</span></span> | <span data-ttu-id="90ca8-124">Opcional.</span><span class="sxs-lookup"><span data-stu-id="90ca8-124">Optional.</span></span> <span data-ttu-id="90ca8-125">Color de fondo utilizado para representar la actividad en la interfaz de usuario: color de marca para el origen de la aplicación de la actividad.</span><span class="sxs-lookup"><span data-stu-id="90ca8-125">Background color used to render the activity in the UI - brand color for the application source of the activity.</span></span> <span data-ttu-id="90ca8-126">Debe ser un color hexadecimal válido</span><span class="sxs-lookup"><span data-stu-id="90ca8-126">Must be a valid hex color</span></span>|
|<span data-ttu-id="90ca8-127">content</span><span class="sxs-lookup"><span data-stu-id="90ca8-127">content</span></span> | <span data-ttu-id="90ca8-128">Objeto JSON sin tipo</span><span class="sxs-lookup"><span data-stu-id="90ca8-128">Untyped JSON object</span></span> | <span data-ttu-id="90ca8-129">Opcional.</span><span class="sxs-lookup"><span data-stu-id="90ca8-129">Optional.</span></span> <span data-ttu-id="90ca8-130">Fragmento personalizado de datos: objeto JSON usado para proporcionar contenido personalizado para representar la actividad en la interfaz de usuario del núcleo de Windows</span><span class="sxs-lookup"><span data-stu-id="90ca8-130">Custom piece of data - JSON object used to provide custom content to render the activity in the Windows Shell UI</span></span>|
|<span data-ttu-id="90ca8-131">attribution</span><span class="sxs-lookup"><span data-stu-id="90ca8-131">attribution</span></span> | <span data-ttu-id="90ca8-132">[imageInfo](../resources/projectrome_imageinfo.md)</span><span class="sxs-lookup"><span data-stu-id="90ca8-132">Added [imageInfo](../resources/projectrome_imageinfo.md)</span></span> | <span data-ttu-id="90ca8-133">Opcional.</span><span class="sxs-lookup"><span data-stu-id="90ca8-133">Optional.</span></span> <span data-ttu-id="90ca8-134">Objeto JSON usado para representar un icono que representa la aplicación que se usa para generar la actividad</span><span class="sxs-lookup"><span data-stu-id="90ca8-134">Optional; URI that points to an icon which represents the application used to generate the activity</span></span>|

## <a name="json-representation"></a><span data-ttu-id="90ca8-135">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="90ca8-135">JSON Representation</span></span>

<span data-ttu-id="90ca8-136">La siguiente es una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="90ca8-136">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "attribution",
    "description",
    "backgroundColor",
    "content"
  ],
  "@odata.type": "microsoft.graph.visualInfo"
}-->

```json
{
    "@odata.type": "microsoft.graph.visualInfo",
    "attribution": {
        "@odata.type": "microsoft.graph.imageInfo",
        "iconUrl": "String (URL)",
        "alternateText": "String",
        "addImageQuery": "boolean"
    },
    "description": "String",
    "backgroundColor": "String",
    "displayText": "String",
    "content": {
        "@odata.type": "microsoft.graph.Json"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2017-06-07 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "visualinfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
