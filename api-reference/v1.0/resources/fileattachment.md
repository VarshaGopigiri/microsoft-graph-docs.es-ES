# <a name="fileattachment-resource-type"></a><span data-ttu-id="9ba62-101">Tipo de recurso fileAttachment</span><span class="sxs-lookup"><span data-stu-id="9ba62-101">fileAttachment resource type</span></span>

<span data-ttu-id="9ba62-p101">Un archivo (como un archivo de texto o un documento de Word) adjunto a un evento, mensaje o publicación. La propiedad **contentBytes** contiene el contenido codificado en base64 del archivo.</span><span class="sxs-lookup"><span data-stu-id="9ba62-p101">A file (such as a text file or Word document) attached to an event, message or post. The  **contentBytes** property contains the base64-encoded contents of the file.</span></span>  

<span data-ttu-id="9ba62-104">Al crear un archivo adjunto, incluya lo siguiente en el cuerpo de la solicitud:</span><span class="sxs-lookup"><span data-stu-id="9ba62-104">When creating a file attachment, include the following in the request body:</span></span>

* `"@odata.type": "#microsoft.graph.fileAttachment"`
* <span data-ttu-id="9ba62-105">Las propiedades requeridas **name** y **contentBytes**.</span><span class="sxs-lookup"><span data-stu-id="9ba62-105">The required properties **name** and **contentBytes**.</span></span>

<span data-ttu-id="9ba62-106">Derivadas de [attachment](attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9ba62-106">Derived from [attachment](attachment.md).</span></span>

## <a name="methods"></a><span data-ttu-id="9ba62-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="9ba62-107">Methods</span></span>

| <span data-ttu-id="9ba62-108">Método</span><span class="sxs-lookup"><span data-stu-id="9ba62-108">Method</span></span>       | <span data-ttu-id="9ba62-109">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9ba62-109">Return Type</span></span>  |<span data-ttu-id="9ba62-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ba62-110">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="9ba62-111">Get</span><span class="sxs-lookup"><span data-stu-id="9ba62-111">Get</span></span>](../api/attachment_get.md) | [<span data-ttu-id="9ba62-112">fileAttachment</span><span class="sxs-lookup"><span data-stu-id="9ba62-112">fileAttachment</span></span>](fileattachment.md) |<span data-ttu-id="9ba62-113">Lea las propiedades y las relaciones del objeto fileAttachment.</span><span class="sxs-lookup"><span data-stu-id="9ba62-113">Read properties and relationships of fileAttachment object.</span></span>|
|[<span data-ttu-id="9ba62-114">Eliminar</span><span class="sxs-lookup"><span data-stu-id="9ba62-114">Delete</span></span>](../api/attachment_delete.md) | <span data-ttu-id="9ba62-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9ba62-115">None</span></span> |<span data-ttu-id="9ba62-116">Elimine el objeto fileAttachment.</span><span class="sxs-lookup"><span data-stu-id="9ba62-116">Delete fileAttachment object.</span></span> |

## <a name="properties"></a><span data-ttu-id="9ba62-117">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9ba62-117">Properties</span></span>
| <span data-ttu-id="9ba62-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9ba62-118">Property</span></span>     | <span data-ttu-id="9ba62-119">Tipo</span><span class="sxs-lookup"><span data-stu-id="9ba62-119">Type</span></span>   |<span data-ttu-id="9ba62-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="9ba62-120">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9ba62-121">contentBytes</span><span class="sxs-lookup"><span data-stu-id="9ba62-121">contentBytes</span></span>|<span data-ttu-id="9ba62-122">Binario</span><span class="sxs-lookup"><span data-stu-id="9ba62-122">Binary</span></span>|<span data-ttu-id="9ba62-123">El contenido del archivo codificado en base64.</span><span class="sxs-lookup"><span data-stu-id="9ba62-123">The base64-encoded contents of the file.</span></span>|
|<span data-ttu-id="9ba62-124">contentId</span><span class="sxs-lookup"><span data-stu-id="9ba62-124">contentId</span></span>|<span data-ttu-id="9ba62-125">String</span><span class="sxs-lookup"><span data-stu-id="9ba62-125">String</span></span>|<span data-ttu-id="9ba62-126">El identificador de los datos de adjuntos del almacén de Exchange.</span><span class="sxs-lookup"><span data-stu-id="9ba62-126">The ID of the attachment in the Exchange store.</span></span>|
|<span data-ttu-id="9ba62-127">contentLocation</span><span class="sxs-lookup"><span data-stu-id="9ba62-127">contentLocation</span></span>|<span data-ttu-id="9ba62-128">String</span><span class="sxs-lookup"><span data-stu-id="9ba62-128">String</span></span>|<span data-ttu-id="9ba62-129">El identificador uniforme de recursos (URI) que corresponde a la ubicación del contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ba62-129">The Uniform Resource Identifier (URI) that corresponds to the location of the content of the attachment.</span></span>|
|<span data-ttu-id="9ba62-130">contentType</span><span class="sxs-lookup"><span data-stu-id="9ba62-130">contentType</span></span>|<span data-ttu-id="9ba62-131">String</span><span class="sxs-lookup"><span data-stu-id="9ba62-131">String</span></span>|<span data-ttu-id="9ba62-132">El tipo de contenido de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ba62-132">The content type of the attachment.</span></span>|
|<span data-ttu-id="9ba62-133">id</span><span class="sxs-lookup"><span data-stu-id="9ba62-133">id</span></span>|<span data-ttu-id="9ba62-134">String</span><span class="sxs-lookup"><span data-stu-id="9ba62-134">String</span></span>|<span data-ttu-id="9ba62-135">El identificador de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ba62-135">The attachment ID.</span></span>|
|<span data-ttu-id="9ba62-136">isInline</span><span class="sxs-lookup"><span data-stu-id="9ba62-136">isInline</span></span>|<span data-ttu-id="9ba62-137">Boolean</span><span class="sxs-lookup"><span data-stu-id="9ba62-137">Boolean</span></span>|<span data-ttu-id="9ba62-138">Se establece en true si se trata de datos adjuntos en línea.</span><span class="sxs-lookup"><span data-stu-id="9ba62-138">Set to true if this is an inline attachment.</span></span>|
|<span data-ttu-id="9ba62-139">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="9ba62-139">lastModifiedDateTime</span></span>|<span data-ttu-id="9ba62-140">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="9ba62-140">DateTimeOffset</span></span>|<span data-ttu-id="9ba62-141">La fecha y hora de la última modificación de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ba62-141">The date and time when the attachment was last modified.</span></span>|
|<span data-ttu-id="9ba62-142">name</span><span class="sxs-lookup"><span data-stu-id="9ba62-142">name</span></span>|<span data-ttu-id="9ba62-143">String</span><span class="sxs-lookup"><span data-stu-id="9ba62-143">String</span></span>|<span data-ttu-id="9ba62-144">El nombre que representa el texto que aparece debajo del icono que representa el archivo adjunto insertado. No tiene que ser el nombre de archivo real.</span><span class="sxs-lookup"><span data-stu-id="9ba62-144">The name representing the text that is displayed below the icon representing the embedded attachment.This does not need to be the actual file name.</span></span>|
|<span data-ttu-id="9ba62-145">size</span><span class="sxs-lookup"><span data-stu-id="9ba62-145">size</span></span>|<span data-ttu-id="9ba62-146">Int32</span><span class="sxs-lookup"><span data-stu-id="9ba62-146">Int32</span></span>|<span data-ttu-id="9ba62-147">El tamaño en bytes de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="9ba62-147">The size in bytes of the attachment.</span></span>|

## <a name="relationships"></a><span data-ttu-id="9ba62-148">Relaciones</span><span class="sxs-lookup"><span data-stu-id="9ba62-148">Relationships</span></span>
<span data-ttu-id="9ba62-149">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9ba62-149">None</span></span>


## <a name="json-representation"></a><span data-ttu-id="9ba62-150">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="9ba62-150">JSON representation</span></span>

<span data-ttu-id="9ba62-151">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="9ba62-151">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.attachment",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.fileAttachment"
}-->

```json
{
  "contentBytes": "binary",
  "contentId": "string",
  "contentLocation": "string",
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
  "description": "fileAttachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
