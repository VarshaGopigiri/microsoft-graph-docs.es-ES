# <a name="itemattachment-resource-type"></a><span data-ttu-id="dab20-101">Tipo de recurso itemAttachment</span><span class="sxs-lookup"><span data-stu-id="dab20-101">itemAttachment resource type</span></span>

<span data-ttu-id="dab20-102">Contacto, evento o mensaje que se adjunta a otro evento, mensaje o publicación.</span><span class="sxs-lookup"><span data-stu-id="dab20-102">A contact, event, or message that's attached to another event, message, or post.</span></span>  

<span data-ttu-id="dab20-103">Derivado de [attachment](attachment.md).</span><span class="sxs-lookup"><span data-stu-id="dab20-103">Derived from [attachment](attachment.md).</span></span>

## <a name="methods"></a><span data-ttu-id="dab20-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="dab20-104">Methods</span></span>

| <span data-ttu-id="dab20-105">Método</span><span class="sxs-lookup"><span data-stu-id="dab20-105">Method</span></span>       | <span data-ttu-id="dab20-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dab20-106">Return Type</span></span>  |<span data-ttu-id="dab20-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="dab20-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="dab20-108">Get</span><span class="sxs-lookup"><span data-stu-id="dab20-108">Get</span></span>](../api/attachment_get.md) | <span data-ttu-id="dab20-109">[itemAttachment](itemattachment.md)</span><span class="sxs-lookup"><span data-stu-id="dab20-109">[itemAttachment](itemattachment.md),</span></span> |<span data-ttu-id="dab20-110">Lee las propiedades y relaciones del objeto itemAttachment.</span><span class="sxs-lookup"><span data-stu-id="dab20-110">Read properties and relationships of itemAttachment object.</span></span>|
|[<span data-ttu-id="dab20-111">Delete</span><span class="sxs-lookup"><span data-stu-id="dab20-111">Delete</span></span>](../api/attachment_delete.md) | <span data-ttu-id="dab20-112">Ninguno</span><span class="sxs-lookup"><span data-stu-id="dab20-112">None</span></span> |<span data-ttu-id="dab20-113">Elimina el objeto itemAttachment.</span><span class="sxs-lookup"><span data-stu-id="dab20-113">Delete itemAttachment object.</span></span> |

## <a name="properties"></a><span data-ttu-id="dab20-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dab20-114">Properties</span></span>
| <span data-ttu-id="dab20-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="dab20-115">Property</span></span>     | <span data-ttu-id="dab20-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="dab20-116">Type</span></span>   |<span data-ttu-id="dab20-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="dab20-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dab20-118">contentType</span><span class="sxs-lookup"><span data-stu-id="dab20-118">contentType</span></span>|<span data-ttu-id="dab20-119">Cadena</span><span class="sxs-lookup"><span data-stu-id="dab20-119">String</span></span>|<span data-ttu-id="dab20-120">El tipo de contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="dab20-120">The content type of the attachment.</span></span>|
|<span data-ttu-id="dab20-121">id</span><span class="sxs-lookup"><span data-stu-id="dab20-121">id</span></span>|<span data-ttu-id="dab20-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="dab20-122">String</span></span>| <span data-ttu-id="dab20-123">El identificador de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="dab20-123">The attachment ID.</span></span>|
|<span data-ttu-id="dab20-124">isInline</span><span class="sxs-lookup"><span data-stu-id="dab20-124">isInline</span></span>|<span data-ttu-id="dab20-125">Booleano</span><span class="sxs-lookup"><span data-stu-id="dab20-125">Boolean</span></span>|<span data-ttu-id="dab20-126">Se establece en true si los datos adjuntos están insertados, como una imagen incrustada en el cuerpo del elemento.</span><span class="sxs-lookup"><span data-stu-id="dab20-126">Set to true if the attachment is inline, such as an embedded image within the body of the item.</span></span>|
|<span data-ttu-id="dab20-127">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="dab20-127">lastModifiedDateTime</span></span>|<span data-ttu-id="dab20-128">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="dab20-128">DateTimeOffset</span></span>|<span data-ttu-id="dab20-129">Última fecha y hora en que se modificaron los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="dab20-129">The last time and date that the attachment was modified.</span></span>|
|<span data-ttu-id="dab20-130">name</span><span class="sxs-lookup"><span data-stu-id="dab20-130">name</span></span>|<span data-ttu-id="dab20-131">Cadena</span><span class="sxs-lookup"><span data-stu-id="dab20-131">String</span></span>|<span data-ttu-id="dab20-132">Nombre para mostrar de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="dab20-132">The display name of the attachment.</span></span>|
|<span data-ttu-id="dab20-133">size</span><span class="sxs-lookup"><span data-stu-id="dab20-133">size</span></span>|<span data-ttu-id="dab20-134">Int32</span><span class="sxs-lookup"><span data-stu-id="dab20-134">Int32</span></span>|<span data-ttu-id="dab20-135">El tamaño en bytes de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="dab20-135">The size in bytes of the attachment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="dab20-136">Relaciones</span><span class="sxs-lookup"><span data-stu-id="dab20-136">Relationships</span></span>
| <span data-ttu-id="dab20-137">Relación</span><span class="sxs-lookup"><span data-stu-id="dab20-137">Relationship</span></span> | <span data-ttu-id="dab20-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="dab20-138">Type</span></span>   |<span data-ttu-id="dab20-139">Descripción</span><span class="sxs-lookup"><span data-stu-id="dab20-139">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="dab20-140">item</span><span class="sxs-lookup"><span data-stu-id="dab20-140">item</span></span>|[<span data-ttu-id="dab20-141">OutlookItem</span><span class="sxs-lookup"><span data-stu-id="dab20-141">OutlookItem</span></span>](outlookitem.md)|<span data-ttu-id="dab20-p101">Evento o mensaje adjunto. Propiedad de navegación.</span><span class="sxs-lookup"><span data-stu-id="dab20-p101">The attached message or event. Navigation property.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="dab20-144">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="dab20-144">JSON representation</span></span>

<span data-ttu-id="dab20-145">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="dab20-145">Here is a JSON representation of the resource</span></span>

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "item"
  ],
  "baseType": "microsoft.graph.attachment",
  "@odata.type": "microsoft.graph.itemAttachment",
  "@odata.annotations": [
    {
      "property": "item",
      "capabilities": {
        "changeTracking": false,
        "deletable": false,
        "insertable": false,
        "searchable": false,
        "updatable": false
      }
    }
  ]
}-->

```json
{
  "contentType": "string",
  "id": "string (identifier)",
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "size": 1024,
  "item": { "@odata.type": "microsoft.graph.outlookItem" }
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "itemAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
