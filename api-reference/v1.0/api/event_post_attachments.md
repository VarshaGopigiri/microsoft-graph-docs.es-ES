# <a name="add-attachment"></a><span data-ttu-id="9cf4e-101">Agregar datos adjuntos</span><span class="sxs-lookup"><span data-stu-id="9cf4e-101">Add attachment</span></span>

<span data-ttu-id="9cf4e-p101">Use esta API para agregar un objeto [attachment](../resources/attachment.md) a un evento. Puesto que actualmente hay un límite de 4 MB en el tamaño total de cada solicitud REST, esto limita el tamaño de los datos adjuntos que agregar a menos de 4 MB.</span><span class="sxs-lookup"><span data-stu-id="9cf4e-p101">Use this API to add an [attachment](../resources/attachment.md) to an event. Since there is currently a limit of 4MB on the total size of each REST request, this limits the size of the attachment you can add to under 4MB.</span></span>
## <a name="permissions"></a><span data-ttu-id="9cf4e-104">Permisos</span><span class="sxs-lookup"><span data-stu-id="9cf4e-104">Permissions</span></span>
<span data-ttu-id="9cf4e-p102">Se requiere uno de los siguientes permisos para llamar a esta API. Para obtener más información, incluido cómo elegir permisos, vea [Permisos](../../../concepts/permissions_reference.md).</span><span class="sxs-lookup"><span data-stu-id="9cf4e-p102">One of the following permissions is required to call this API. To learn more, including how to choose permissions, see [Permissions](../../../concepts/permissions_reference.md).</span></span>

|<span data-ttu-id="9cf4e-107">Tipo de permiso</span><span class="sxs-lookup"><span data-stu-id="9cf4e-107">Permission type</span></span>      | <span data-ttu-id="9cf4e-108">Permisos (de menos a más privilegiados)</span><span class="sxs-lookup"><span data-stu-id="9cf4e-108">Permissions (from least to most privileged)</span></span>              |
|:--------------------|:---------------------------------------------------------|
|<span data-ttu-id="9cf4e-109">Delegado (cuenta profesional o educativa)</span><span class="sxs-lookup"><span data-stu-id="9cf4e-109">Delegated (work or school account)</span></span> | <span data-ttu-id="9cf4e-110">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9cf4e-110">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="9cf4e-111">Delegado (cuenta personal de Microsoft)</span><span class="sxs-lookup"><span data-stu-id="9cf4e-111">Delegated (personal Microsoft account)</span></span> | <span data-ttu-id="9cf4e-112">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9cf4e-112">Calendars.ReadWrite</span></span>    |
|<span data-ttu-id="9cf4e-113">Aplicación</span><span class="sxs-lookup"><span data-stu-id="9cf4e-113">Application</span></span> | <span data-ttu-id="9cf4e-114">Calendars.ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9cf4e-114">Calendars.ReadWrite</span></span> |

## <a name="http-request"></a><span data-ttu-id="9cf4e-115">Solicitud HTTP</span><span class="sxs-lookup"><span data-stu-id="9cf4e-115">HTTP request</span></span>
<!-- { "blockType": "ignored" } -->
<span data-ttu-id="9cf4e-116">Datos adjuntos de un [event](../resources/event.md) en el [calendar](../resources/calendar.md) predeterminado del usuario o del grupo.</span><span class="sxs-lookup"><span data-stu-id="9cf4e-116">Attachments for an [event](../resources/event.md) in the user's or group's default [calendar](../resources/calendar.md).</span></span>
```http
POST /me/events/{id}/attachments
POST /users/{id | userPrincipalName}/events/{id}/attachments
POST /groups/{id}/events/{id}/attachments

POST /me/calendar/events/{id}/attachments
POST /users/{id | userPrincipalName}/calendar/events/{id}/attachments
POST /groups/{id}/calendar/events/{id}/attachments
```
<span data-ttu-id="9cf4e-117">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="9cf4e-117">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to the user's default [calendarGroup](../resources/calendargroup.md).</span></span>
```http
POST /me/calendars/{id}/events/{id}/attachments
POST /users/{id | userPrincipalName}/calendars/{id}/events/{id}/attachments

POST /me/calendargroup/calendars/{id}/events/{id}/attachments
POST /users/{id | userPrincipalName}/calendargroup/calendars/{id}/events/{id}/attachments
```
<span data-ttu-id="9cf4e-118">Datos adjuntos de un [event](../resources/event.md) en un [calendar](../resources/calendar.md) perteneciente al [calendarGroup](../resources/calendargroup.md) de un usuario.</span><span class="sxs-lookup"><span data-stu-id="9cf4e-118">Attachments for an [event](../resources/event.md) in a [calendar](../resources/calendar.md) belonging to a user's [calendarGroup](../resources/calendargroup.md).</span></span>
```http
POST /me/calendargroups/{id}/calendars/{id}/events/{id}/attachments
POST /users/{id | userPrincipalName}/calendargroups/{id}/calendars/{id}/events/{id}/attachments
```
## <a name="request-headers"></a><span data-ttu-id="9cf4e-119">Encabezados de solicitud</span><span class="sxs-lookup"><span data-stu-id="9cf4e-119">Request headers</span></span>
| <span data-ttu-id="9cf4e-120">Nombre</span><span class="sxs-lookup"><span data-stu-id="9cf4e-120">Name</span></span>       | <span data-ttu-id="9cf4e-121">Tipo</span><span class="sxs-lookup"><span data-stu-id="9cf4e-121">Type</span></span> | <span data-ttu-id="9cf4e-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cf4e-122">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="9cf4e-123">Authorization</span><span class="sxs-lookup"><span data-stu-id="9cf4e-123">Authorization</span></span>  | <span data-ttu-id="9cf4e-124">string</span><span class="sxs-lookup"><span data-stu-id="9cf4e-124">string</span></span>  | <span data-ttu-id="9cf4e-p103">{token} de portador. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9cf4e-p103">Bearer {token}. Required.</span></span> |
| <span data-ttu-id="9cf4e-127">Content-Type</span><span class="sxs-lookup"><span data-stu-id="9cf4e-127">Content-Type</span></span> | <span data-ttu-id="9cf4e-128">string</span><span class="sxs-lookup"><span data-stu-id="9cf4e-128">string</span></span>  | <span data-ttu-id="9cf4e-p104">Naturaleza de los datos en el cuerpo de una entidad. Obligatorio.</span><span class="sxs-lookup"><span data-stu-id="9cf4e-p104">Nature of the data in the body of an entity. Required.</span></span> |

## <a name="request-body"></a><span data-ttu-id="9cf4e-131">Cuerpo de solicitud</span><span class="sxs-lookup"><span data-stu-id="9cf4e-131">Request body</span></span>
<span data-ttu-id="9cf4e-132">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9cf4e-132">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

## <a name="response"></a><span data-ttu-id="9cf4e-133">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9cf4e-133">Response</span></span>

<span data-ttu-id="9cf4e-134">Si se ejecuta correctamente, este método devuelve el código de respuesta `201 Created` y el objeto [attachment](../resources/attachment.md) en el cuerpo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cf4e-134">If successful, this method returns `201 Created` response code and [attachment](../resources/attachment.md) object in the response body.</span></span>

## <a name="example-file-attachment"></a><span data-ttu-id="9cf4e-135">Ejemplo (datos adjuntos del archivo)</span><span class="sxs-lookup"><span data-stu-id="9cf4e-135">Example (file attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="9cf4e-136">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9cf4e-136">Request</span></span>
<span data-ttu-id="9cf4e-137">Aquí tiene un ejemplo de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="9cf4e-137">Here is an example of the request.</span></span>
<!-- {
  "blockType": "request",
  "name": "create_file_attachment_from_event"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events('AAMkAGI1AAAt9AHjAAA=')/attachments 
Content-type: application/json
Content-length: 151

{
    "@odata.type": "#microsoft.graph.fileAttachment",
    "name": "menu.txt",
    "contentBytes": "bWFjIGFuZCBjaGVlc2UgdG9kYXk="   
}
```

<span data-ttu-id="9cf4e-138">En el cuerpo de la solicitud, proporcione una representación JSON del objeto [attachment](../resources/attachment.md).</span><span class="sxs-lookup"><span data-stu-id="9cf4e-138">In the request body, supply a JSON representation of [attachment](../resources/attachment.md) object.</span></span>

##### <a name="response"></a><span data-ttu-id="9cf4e-139">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9cf4e-139">Response</span></span>
<span data-ttu-id="9cf4e-140">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cf4e-140">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP 201 Created
Content-Length: 735

{
    "@odata.context":"https://graph.microsoft.com/v1.0/$metadata#users('cd209b0b-3f83-4c35-82d2-d88a61820480')/events('AAMkAGI1AAAt9AHjAAA%3D')/attachments/$entity",
    "@odata.type":"#microsoft.graph.fileAttachment",
    "id":"AAMkAGI1AAAt9AHjAAABEgAQAEdBogju-MJEu6Ngg-1_W0g=",
    "lastModifiedDateTime":"2017-04-15T03:21:49Z",
    "name":"menu.txt",
    "contentType":"text/plain",
    "size":178,
    "isInline":false,
    "contentId":null,
    "contentLocation":null,
    "contentBytes":"bWFjIGFuZCBjaGVlc2UgdG9kYXk="
}
```

## <a name="example-item-attachment"></a><span data-ttu-id="9cf4e-141">Ejemplo (datos adjuntos del elemento)</span><span class="sxs-lookup"><span data-stu-id="9cf4e-141">Example (item attachment)</span></span>

##### <a name="request"></a><span data-ttu-id="9cf4e-142">Solicitud</span><span class="sxs-lookup"><span data-stu-id="9cf4e-142">Request</span></span>

<span data-ttu-id="9cf4e-143">Este es un ejemplo que adjunta un evento con otro evento como datos adjuntos del elemento.</span><span class="sxs-lookup"><span data-stu-id="9cf4e-143">Here is an example which attaches an event with another event as an item attachment.</span></span>

<!-- {
  "blockType": "request",
  "name": "create_item_attachment_from_event"
}-->
```http
POST https://graph.microsoft.com/v1.0/me/events/{AAMkAGI1AAAt9AHjAAA=}/attachments
Content-type: application/json
Content-length: 600

{
  "@odata.type": "#microsoft.graph.itemAttachment",
  "name": "Holiday event", 
  "item": {
        "@odata.type": "microsoft.graph.event",
        "subject": "Discuss gifts for children",
        "body": {
            "contentType": "HTML",
            "content": "Let's look for funding!"
         },
         "start": {
             "dateTime": "2016-12-02T18:00:00",
             "timeZone": "Pacific Standard Time"
          },
          "end": {
             "dateTime": "2016-12-02T19:00:00",
             "timeZone": "Pacific Standard Time"
          }
    }
}
```

##### <a name="response"></a><span data-ttu-id="9cf4e-144">Respuesta</span><span class="sxs-lookup"><span data-stu-id="9cf4e-144">Response</span></span>
<span data-ttu-id="9cf4e-145">Aquí tiene un ejemplo de la respuesta.</span><span class="sxs-lookup"><span data-stu-id="9cf4e-145">Here is an example of the response.</span></span>
<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.attachment"
} -->
```http
HTTP 201 Created
Content-type: application/json
Content-length: 162

{
    "@odata.context":"https://graph.microsoft.com/api/v1.0/$metadata#me/events('AAMkAGI1AAAt9AHjAAA=')/attachments/$entity",
    "@odata.type":"#microsoft.graph.itemAttachment",
    "@odata.id":"https://graph.microsoft.com/api/v1.0/users('fdcbcf34-2505-4d07-be5b-0a55b699d157@41a5b830-45ac-4f1b-9bfc-baafa3b7db2e')/events('AAMkAGI1AAAt9AHjAAA=')/attachments('AAMkADNkN2Jp5JVnQIe9r0=')",
    "id":"AAMkADNkNJp5JVnQIe9r0=",
    "lastModifiedDateTime":"2016-12-01T22:27:13Z",
    "name":"Holiday event",
    "contentType":null,
    "size":2473,
    "isInline":false
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create Attachment",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
