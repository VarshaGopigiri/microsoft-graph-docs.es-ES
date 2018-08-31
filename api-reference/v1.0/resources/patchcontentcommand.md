# <a name="patchcontentcommand-resource-type"></a><span data-ttu-id="37b2d-101">Tipo de recurso patchContentCommand</span><span class="sxs-lookup"><span data-stu-id="37b2d-101">patchContentCommand resource type</span></span>

<span data-ttu-id="37b2d-102">Cambios que se deben realizar en una solicitud de revisión de una página de OneNote.</span><span class="sxs-lookup"><span data-stu-id="37b2d-102">The changes to make to a OneNote page in a PATCH request.</span></span>

## <a name="json-representation"></a><span data-ttu-id="37b2d-103">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="37b2d-103">JSON representation</span></span>

<span data-ttu-id="37b2d-104">Aquí se muestra una representación JSON del recurso, que se envía en el cuerpo de la solicitud [PATCH pages/{id}\`](../api/page_update.md).</span><span class="sxs-lookup"><span data-stu-id="37b2d-104">Here is a JSON representation of the resource, which is sent in the body of the [PATCH pages/{id}\`](../api/page_update.md) request.</span></span> 

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.onenotePatchContentCommand"
}-->

```json
{
  "action": "String",
  "content": "string",
  "position": "String",
  "target": "string"
}

```

## <a name="properties"></a><span data-ttu-id="37b2d-105">Propiedades</span><span class="sxs-lookup"><span data-stu-id="37b2d-105">Properties</span></span>
| <span data-ttu-id="37b2d-106">Propiedad</span><span class="sxs-lookup"><span data-stu-id="37b2d-106">Property</span></span>     | <span data-ttu-id="37b2d-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="37b2d-107">Type</span></span>   |<span data-ttu-id="37b2d-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="37b2d-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="37b2d-109">action</span><span class="sxs-lookup"><span data-stu-id="37b2d-109">action</span></span>|<span data-ttu-id="37b2d-110">onenotePatchActionType</span><span class="sxs-lookup"><span data-stu-id="37b2d-110">onenotePatchActionType values</span></span>|<span data-ttu-id="37b2d-111">Acción que se debe efectuar en el elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="37b2d-111">The action to perform on the target element.</span></span> <span data-ttu-id="37b2d-112">Los valores posibles son: `replace`, `append`, `delete`, `insert` o `prepend`.</span><span class="sxs-lookup"><span data-stu-id="37b2d-112">The possible values are `replace`, `append`, `delete`, `insert`, , , , , , , , or `prepend`.</span></span>|
|<span data-ttu-id="37b2d-113">content</span><span class="sxs-lookup"><span data-stu-id="37b2d-113">content</span></span>|<span data-ttu-id="37b2d-114">Cadena</span><span class="sxs-lookup"><span data-stu-id="37b2d-114">String</span></span>|<span data-ttu-id="37b2d-p102">Cadena de HTML sintácticamente correcto para agregar a la página y datos binarios de cualquier imagen o archivo. Si el contenido incluye datos binarios, la solicitud se debe enviar mediante el tipo de contenido `multipart/form-data` con una parte "Comandos".</span><span class="sxs-lookup"><span data-stu-id="37b2d-p102">A string of well-formed HTML to add to the page, and any image or file binary data. If the content contains binary data, the request must be sent using the `multipart/form-data` content type with a "Commands" part.</span></span> |
|<span data-ttu-id="37b2d-117">position</span><span class="sxs-lookup"><span data-stu-id="37b2d-117">position</span></span>|<span data-ttu-id="37b2d-118">onenotePatchInsertPosition</span><span class="sxs-lookup"><span data-stu-id="37b2d-118">onenotePatchInsertPosition values</span></span>|<span data-ttu-id="37b2d-119">Ubicación donde se debe agregar el contenido provisto, en relación con el elemento de destino.</span><span class="sxs-lookup"><span data-stu-id="37b2d-119">The location to add the supplied content, relative to the target element.</span></span> <span data-ttu-id="37b2d-120">Los valores posibles son: `after` (valor predeterminado) o `before`.</span><span class="sxs-lookup"><span data-stu-id="37b2d-120">The possible values are , , , , , , , , , , , or .</span></span>|
|<span data-ttu-id="37b2d-121">target</span><span class="sxs-lookup"><span data-stu-id="37b2d-121">target</span></span>|<span data-ttu-id="37b2d-122">Cadena</span><span class="sxs-lookup"><span data-stu-id="37b2d-122">String</span></span>|<span data-ttu-id="37b2d-p104">Elemento que se va a actualizar. Debe ser el `#<data-id>` o el `<id>` generado del elemento, o bien la palabra clave `body` o `title`.</span><span class="sxs-lookup"><span data-stu-id="37b2d-p104">The element to update. Must be the `#<data-id>` or the generated `<id>` of the element, or the `body` or `title` keyword.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "patchContentCommand resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
