# <a name="referenceattachment-resource-type"></a><span data-ttu-id="0c712-101">Tipo de recurso referenceAttachment</span><span class="sxs-lookup"><span data-stu-id="0c712-101">referenceAttachment resource type</span></span>

<span data-ttu-id="0c712-102">Vínculo a un archivo (como un archivo de texto o un documento de Word) en una unidad en la nube de OneDrive para la Empresa o en otras ubicaciones de almacenamiento compatibles asociadas a un evento, mensaje o publicación.</span><span class="sxs-lookup"><span data-stu-id="0c712-102">A link to a file (such as a text file or Word document) on a OneDrive for Business cloud drive or other supported storage locations, attached to an event, message, or post.</span></span>

<span data-ttu-id="0c712-103">Derivado de [attachment](attachment.md).</span><span class="sxs-lookup"><span data-stu-id="0c712-103">Derived from [attachment](attachment.md).</span></span>

## <a name="methods"></a><span data-ttu-id="0c712-104">Métodos</span><span class="sxs-lookup"><span data-stu-id="0c712-104">Methods</span></span>

| <span data-ttu-id="0c712-105">Método</span><span class="sxs-lookup"><span data-stu-id="0c712-105">Method</span></span>       | <span data-ttu-id="0c712-106">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c712-106">Return Type</span></span>  |<span data-ttu-id="0c712-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c712-107">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="0c712-108">Get</span><span class="sxs-lookup"><span data-stu-id="0c712-108">Get</span></span>](../api/attachment_get.md) | [<span data-ttu-id="0c712-109">referenceAttachment</span><span class="sxs-lookup"><span data-stu-id="0c712-109">referenceAttachment</span></span>](referenceattachment.md) |<span data-ttu-id="0c712-110">Lee las propiedades y relaciones del objeto referenceAttachment.</span><span class="sxs-lookup"><span data-stu-id="0c712-110">Read properties and relationships of referenceAttachment object.</span></span>|
|[<span data-ttu-id="0c712-111">Delete</span><span class="sxs-lookup"><span data-stu-id="0c712-111">Delete</span></span>](../api/attachment_delete.md) | <span data-ttu-id="0c712-112">None</span><span class="sxs-lookup"><span data-stu-id="0c712-112">None</span></span> |<span data-ttu-id="0c712-113">Elimina el objeto referenceAttachment.</span><span class="sxs-lookup"><span data-stu-id="0c712-113">Delete referenceAttachment object.</span></span> |

## <a name="properties"></a><span data-ttu-id="0c712-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c712-114">Properties</span></span>
| <span data-ttu-id="0c712-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="0c712-115">Property</span></span>     | <span data-ttu-id="0c712-116">Tipo</span><span class="sxs-lookup"><span data-stu-id="0c712-116">Type</span></span>   |<span data-ttu-id="0c712-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="0c712-117">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="0c712-118">contentType</span><span class="sxs-lookup"><span data-stu-id="0c712-118">contentType</span></span>|<span data-ttu-id="0c712-119">String</span><span class="sxs-lookup"><span data-stu-id="0c712-119">String</span></span>|<span data-ttu-id="0c712-120">El tipo de contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0c712-120">The content type of the attachment.</span></span>|
|<span data-ttu-id="0c712-121">id</span><span class="sxs-lookup"><span data-stu-id="0c712-121">id</span></span>|<span data-ttu-id="0c712-122">String</span><span class="sxs-lookup"><span data-stu-id="0c712-122">String</span></span>|<span data-ttu-id="0c712-p101">Identificador de los datos adjuntos  Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="0c712-p101">The attachment ID.  Read-only.</span></span>|
|<span data-ttu-id="0c712-125">isInline</span><span class="sxs-lookup"><span data-stu-id="0c712-125">isInline</span></span>|<span data-ttu-id="0c712-126">Boolean</span><span class="sxs-lookup"><span data-stu-id="0c712-126">Boolean</span></span>|<span data-ttu-id="0c712-127">Se establece en true si los datos adjuntos aparecen en insertados en el cuerpo del objeto embedding.</span><span class="sxs-lookup"><span data-stu-id="0c712-127">Set to true if the attachment appears inline in the body of the embedding object.</span></span>|
|<span data-ttu-id="0c712-128">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="0c712-128">lastModifiedDateTime</span></span>|<span data-ttu-id="0c712-129">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="0c712-129">DateTimeOffset</span></span>|<span data-ttu-id="0c712-p102">Fecha y hora de la última modificación de los datos adjuntos. El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, la medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="0c712-p102">The date and time when the attachment was last modified. The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="0c712-133">name</span><span class="sxs-lookup"><span data-stu-id="0c712-133">name</span></span>|<span data-ttu-id="0c712-134">String</span><span class="sxs-lookup"><span data-stu-id="0c712-134">String</span></span>|<span data-ttu-id="0c712-p103">Texto que aparece debajo del icono que representa al archivo adjunto incrustado. No tiene que ser el nombre de archivo real.</span><span class="sxs-lookup"><span data-stu-id="0c712-p103">The text that is displayed below the icon representing the embedded attachment. This does not need to be the actual file name.</span></span>|
|<span data-ttu-id="0c712-137">size</span><span class="sxs-lookup"><span data-stu-id="0c712-137">size</span></span>|<span data-ttu-id="0c712-138">Int32</span><span class="sxs-lookup"><span data-stu-id="0c712-138">Int32</span></span>|<span data-ttu-id="0c712-139">Tamaño en bytes de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="0c712-139">The size of the attachment in bytes.</span></span>|

## <a name="relationships"></a><span data-ttu-id="0c712-140">Relaciones</span><span class="sxs-lookup"><span data-stu-id="0c712-140">Relationships</span></span>
<span data-ttu-id="0c712-141">Ninguno</span><span class="sxs-lookup"><span data-stu-id="0c712-141">None</span></span>



## <a name="json-representation"></a><span data-ttu-id="0c712-142">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="0c712-142">JSON representation</span></span>

<span data-ttu-id="0c712-143">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="0c712-143">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.referenceAttachment"
}-->

```json
{
  "contentType": "string",
  "id": "string (identifier)",
  "isInline": true,
  "lastModifiedDateTime": "String (timestamp)",
  "name": "string",
  "size": 1024
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "referenceAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
