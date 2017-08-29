# <a name="attachment-resource-type"></a><span data-ttu-id="d9dcd-101">Tipo de recurso attachment</span><span class="sxs-lookup"><span data-stu-id="d9dcd-101">attachment resource type</span></span>

<span data-ttu-id="d9dcd-102">Puede agregar contenido relacionado a un [evento](../resources/event.md), [mensaje](../resources/message.md) o [publicación](../resources/post.md) en forma de datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-102">You can add related content to an [event](../resources/event.md), [message](../resources/message.md), or [post](../resources/post.md) in the form of an attachment.</span></span>

<span data-ttu-id="d9dcd-103">**datos adjuntos** es el recurso base para los siguientes tipos de datos adjuntos derivados:</span><span class="sxs-lookup"><span data-stu-id="d9dcd-103">**attachment** is the base resource for the following derived types of attachments:</span></span>

* <span data-ttu-id="d9dcd-104">Un archivo (recurso [fileAttachment](../resources/fileattachment.md))</span><span class="sxs-lookup"><span data-stu-id="d9dcd-104">A file ([fileAttachment](../resources/fileattachment.md) resource).</span></span>
* <span data-ttu-id="d9dcd-105">Un elemento (contacto, evento o mensaje, representado por un recurso [itemAttachment](../resources/itemattachment.md))</span><span class="sxs-lookup"><span data-stu-id="d9dcd-105">An item (contact, event or message, represented by an [itemAttachment](../resources/itemattachment.md) resource)</span></span>
* <span data-ttu-id="d9dcd-106">Un vínculo a un archivo (recurso [referenceAttachment](../resources/referenceAttachment.md))</span><span class="sxs-lookup"><span data-stu-id="d9dcd-106">A link to a file ([referenceAttachment](../resources/referenceAttachment.md) resource)</span></span>


## <a name="methods"></a><span data-ttu-id="d9dcd-107">Métodos</span><span class="sxs-lookup"><span data-stu-id="d9dcd-107">Methods</span></span>

<span data-ttu-id="d9dcd-108">Los métodos siguientes se aplican a cualquiera de los tipos derivados de los datos adjuntos (**fileAttachment**, **itemAttachment** o **referenceAttachment**).</span><span class="sxs-lookup"><span data-stu-id="d9dcd-108">The following methods apply to any of the derived types of attachments (**fileAttachment**, **itemAttachment**, or **referenceAttachment**).</span></span>

| <span data-ttu-id="d9dcd-109">Método</span><span class="sxs-lookup"><span data-stu-id="d9dcd-109">Method</span></span>       | <span data-ttu-id="d9dcd-110">Tipo de valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d9dcd-110">Return Type</span></span>  |<span data-ttu-id="d9dcd-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9dcd-111">Description</span></span>|
|:---------------|:--------|:----------|
|[<span data-ttu-id="d9dcd-112">Obtener datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="d9dcd-112">Get attachment</span></span>](../api/attachment_get.md) | [<span data-ttu-id="d9dcd-113">dato adjunto</span><span class="sxs-lookup"><span data-stu-id="d9dcd-113">attachment</span></span>](attachment.md) |<span data-ttu-id="d9dcd-114">Lea las propiedades y relaciones de un archivo adjunto, conectado a un evento, mensaje o publicación.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-114">Read the properties and relationships of an attachment, attached to an event, message, or post.</span></span>|
|[<span data-ttu-id="d9dcd-115">Agregar datos adjuntos a un evento</span><span class="sxs-lookup"><span data-stu-id="d9dcd-115">Add attachment to an event</span></span>](../api/event_post_attachments.md) | [<span data-ttu-id="d9dcd-116">attachment</span><span class="sxs-lookup"><span data-stu-id="d9dcd-116">attachment</span></span>](attachment.md) |<span data-ttu-id="d9dcd-117">Agregue un archivo, elemento o vínculo adjunto a un evento.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-117">Add a file, item, or link attachment to an event.</span></span>|
|[<span data-ttu-id="d9dcd-118">Agregar datos adjuntos a un mensaje</span><span class="sxs-lookup"><span data-stu-id="d9dcd-118">Add attachment to a message</span></span>](../api/message_post_attachments.md) | [<span data-ttu-id="d9dcd-119">attachment</span><span class="sxs-lookup"><span data-stu-id="d9dcd-119">attachment</span></span>](attachment.md) |<span data-ttu-id="d9dcd-120">Agregue un archivo, elemento o vínculo adjunto a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-120">Add a file, item, or link attachment to a message.</span></span>|
|[<span data-ttu-id="d9dcd-121">Agregar datos adjuntos a una publicación</span><span class="sxs-lookup"><span data-stu-id="d9dcd-121">Add attachment to a post</span></span>](../api/post_post_attachments.md) | [<span data-ttu-id="d9dcd-122">attachment</span><span class="sxs-lookup"><span data-stu-id="d9dcd-122">attachment</span></span>](attachment.md) |<span data-ttu-id="d9dcd-123">Agregue un archivo, elemento o vínculo adjunto a una publicación.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-123">Add a file, item, or link attachment to a post.</span></span>|
|[<span data-ttu-id="d9dcd-124">Mostrar los datos adjuntos de un evento</span><span class="sxs-lookup"><span data-stu-id="d9dcd-124">List attachments of an event</span></span>](../api/event_list_attachments.md) | <span data-ttu-id="d9dcd-125">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="d9dcd-125">[attachment](attachment.md) collection</span></span> | <span data-ttu-id="d9dcd-126">Obtenga una lista de los datos adjuntos de un evento.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-126">Get a list of attachments for an event.</span></span> |
|[<span data-ttu-id="d9dcd-127">Mostrar los datos adjuntos de un mensaje</span><span class="sxs-lookup"><span data-stu-id="d9dcd-127">List attachments of a message</span></span>](../api/message_list_attachments.md) | <span data-ttu-id="d9dcd-128">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="d9dcd-128">[attachment](attachment.md) collection</span></span> | <span data-ttu-id="d9dcd-129">Obtenga una lista de los datos adjuntos de un mensaje.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-129">Get a list of attachments for a message.</span></span> |
|[<span data-ttu-id="d9dcd-130">Mostrar los datos adjuntos de una publicación</span><span class="sxs-lookup"><span data-stu-id="d9dcd-130">List attachments of a post</span></span>](../api/post_list_attachments.md) | <span data-ttu-id="d9dcd-131">Colección [attachment](attachment.md)</span><span class="sxs-lookup"><span data-stu-id="d9dcd-131">[attachment](attachment.md) collection</span></span> | <span data-ttu-id="d9dcd-132">Obtenga una lista de los datos adjuntos de una publicación.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-132">Get a list of attachments for a post.</span></span> |
|[<span data-ttu-id="d9dcd-133">Eliminar</span><span class="sxs-lookup"><span data-stu-id="d9dcd-133">Delete</span></span>](../api/attachment_delete.md) | <span data-ttu-id="d9dcd-134">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d9dcd-134">None</span></span> |<span data-ttu-id="d9dcd-135">Eliminar datos adjuntos en un evento, un mensaje o una publicación.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-135">Delete an attachment on an event, message, or post.</span></span> |

## <a name="properties"></a><span data-ttu-id="d9dcd-136">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9dcd-136">Properties</span></span>

<span data-ttu-id="d9dcd-p101">A continuación se muestran las propiedades base de cualquier recurso de datos adjuntos. Haga referencia al tipo específico de dato adjunto ([fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md) o [referenceAttachment](../resources/referenceAttachment.md)) para ver propiedades adicionales.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-p101">The following are the base properties of any attachment resource. Refer to the specific type of attachment ([fileAttachment](../resources/fileattachment.md), [itemAttachment](../resources/itemattachment.md), or [referenceAttachment](../resources/referenceAttachment.md)) for additional properties.</span></span>

| <span data-ttu-id="d9dcd-139">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d9dcd-139">Property</span></span>     | <span data-ttu-id="d9dcd-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="d9dcd-140">Type</span></span>   |<span data-ttu-id="d9dcd-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="d9dcd-141">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="d9dcd-142">contentType</span><span class="sxs-lookup"><span data-stu-id="d9dcd-142">contentType</span></span>|<span data-ttu-id="d9dcd-143">String</span><span class="sxs-lookup"><span data-stu-id="d9dcd-143">String</span></span>|<span data-ttu-id="d9dcd-144">El tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-144">The MIME type.</span></span>|
|<span data-ttu-id="d9dcd-145">id</span><span class="sxs-lookup"><span data-stu-id="d9dcd-145">id</span></span>|<span data-ttu-id="d9dcd-146">Cadena</span><span class="sxs-lookup"><span data-stu-id="d9dcd-146">String</span></span>| <span data-ttu-id="d9dcd-147">Solo lectura.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-147">Read-only.</span></span>|
|<span data-ttu-id="d9dcd-148">isInline</span><span class="sxs-lookup"><span data-stu-id="d9dcd-148">isInline</span></span>|<span data-ttu-id="d9dcd-149">Boolean</span><span class="sxs-lookup"><span data-stu-id="d9dcd-149">Boolean</span></span>|<span data-ttu-id="d9dcd-150">`true` si los datos adjuntos son datos adjuntos en línea; de lo contrario, `false`.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-150">`true` if the attachment is an inline attachment; otherwise, `false`.</span></span>|
|<span data-ttu-id="d9dcd-151">lastModifiedDateTime</span><span class="sxs-lookup"><span data-stu-id="d9dcd-151">lastModifiedDateTime</span></span>|<span data-ttu-id="d9dcd-152">DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="d9dcd-152">DateTimeOffset</span></span>|<span data-ttu-id="d9dcd-p102">El tipo de marca de tiempo representa la información de fecha y hora con el formato ISO 8601 y está siempre en hora UTC. Por ejemplo, medianoche UTC del 1 de enero de 2014 sería así: `'2014-01-01T00:00:00Z'`</span><span class="sxs-lookup"><span data-stu-id="d9dcd-p102">The Timestamp type represents date and time information using ISO 8601 format and is always in UTC time. For example, midnight UTC on Jan 1, 2014 would look like this: `'2014-01-01T00:00:00Z'`</span></span>|
|<span data-ttu-id="d9dcd-155">name</span><span class="sxs-lookup"><span data-stu-id="d9dcd-155">name</span></span>|<span data-ttu-id="d9dcd-156">String</span><span class="sxs-lookup"><span data-stu-id="d9dcd-156">String</span></span>|<span data-ttu-id="d9dcd-157">El nombre de archivo de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-157">The attachment's file name.</span></span>|
|<span data-ttu-id="d9dcd-158">size</span><span class="sxs-lookup"><span data-stu-id="d9dcd-158">size</span></span>|<span data-ttu-id="d9dcd-159">Int32</span><span class="sxs-lookup"><span data-stu-id="d9dcd-159">Int32</span></span>|<span data-ttu-id="d9dcd-160">La longitud en bytes de los datos adjuntos.</span><span class="sxs-lookup"><span data-stu-id="d9dcd-160">The length of the attachment in bytes.</span></span>|

## <a name="relationships"></a><span data-ttu-id="d9dcd-161">Relaciones</span><span class="sxs-lookup"><span data-stu-id="d9dcd-161">Relationships</span></span>
<span data-ttu-id="d9dcd-162">Ninguno</span><span class="sxs-lookup"><span data-stu-id="d9dcd-162">None</span></span>

## <a name="json-representation"></a><span data-ttu-id="d9dcd-163">Representación JSON</span><span class="sxs-lookup"><span data-stu-id="d9dcd-163">JSON representation</span></span>

<span data-ttu-id="d9dcd-164">Aquí tiene una representación JSON del recurso</span><span class="sxs-lookup"><span data-stu-id="d9dcd-164">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.attachment"
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
  "description": "attachment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
